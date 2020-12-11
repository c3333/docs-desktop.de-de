---
title: Abhängigkeitseigenschaften vom Auflistungstyp
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- properties [WPF], dependency
- properties [WPF], collection-type
- dependency properties [WPF]
- collection-type properties [WPF]
ms.assetid: 99f96a42-3ab7-4f64-a16b-2e10d654e97c
ms.openlocfilehash: 8da798b3d7254d10d8da7ca6df335f63e4890763
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976421"
---
# <a name="collection-type-dependency-properties"></a>Abhängigkeitseigenschaften vom Auflistungstyp
Dieses Thema enthält einen Leitfaden und empfohlene Muster zur Implementierung einer Abhängigkeitseigenschaft für Eigenschaften vom Auflistungstyp.  

<a name="implementing"></a>
## <a name="implementing-a-collection-type-dependency-property"></a>Implementieren einer Abhängigkeitseigenschaft vom Auflistungstyp  
 Für eine Abhängigkeits Eigenschaft im Allgemeinen ist das folgende Implementierungs Muster, dass Sie einen CLR-Eigenschafts Wrapper definieren, bei dem diese Eigenschaft durch einen <xref:System.Windows.DependencyProperty> Bezeichner und nicht durch ein Feld oder ein anderes Konstrukt gestützt wird. Folgen Sie diesem Muster auch bei der Implementierung einer Eigenschaft vom Auflistungstyp. Eine Auflistungstyp Eigenschaft führt jedoch zu einer gewissen Komplexität des Musters, wenn der in der Auflistung enthaltene Typ selbst eine <xref:System.Windows.DependencyObject> oder eine <xref:System.Windows.Freezable> abgeleitete Klasse ist.  
  
<a name="initializing"></a>
## <a name="initializing-the-collection-beyond-the-default-value"></a>Initialisieren der Auflistung für einen anderen Wert als den Standardwert  
 Beim Erstellen einer Abhängigkeitseigenschaft geben Sie nicht den Standardwert der Eigenschaft als Anfangsfeldwert an. Geben Sie den Standardwert stattdessen über die Metadaten für Abhängigkeitseigenschaften an. Handelt es sich bei der Eigenschaft um einen Verweistyp, ist der in den Metadaten für Abhängigkeitseigenschaften angegebene Standardwert kein Standardwert pro Instanz. Er stellt vielmehr einen Standardwert dar, der für alle Instanzen des Typs gilt. Achten Sie also darauf, dass Sie nicht die durch die Metadaten für Auflistungseigenschaften definierte, einzelne statische Auflistung als funktionierenden Standardwert für neu erstellte Instanzen des Typs verwenden. Vergewissern Sie sich stattdessen, dass Sie den Auflistungswert bewusst als eine eindeutige (Instanz-)Auflistung als Teil Ihrer Klassenkonstruktorlogik festlegen. Andernfalls erstellen Sie unbeabsichtigterweise eine Singleton-Klasse.  
  
 Betrachten Sie das folgende Beispiel. Der folgende Abschnitt des Beispiels zeigt die Definition für eine-Klasse `Aquarium` , die einen Fehler mit dem Standardwert enthält. Die-Klasse definiert die Auflistungstyp-Abhängigkeits Eigenschaft `AquariumObjects` , die den generischen <xref:System.Collections.Generic.List%601> Typ mit einer <xref:System.Windows.FrameworkElement> Typeinschränkung verwendet. Im-Befehl <xref:System.Windows.DependencyProperty.Register%28System.String%2CSystem.Type%2CSystem.Type%2CSystem.Windows.PropertyMetadata%29> für die-Abhängigkeits Eigenschaft wird der Standardwert von den Metadaten als neuer generischer Wert festgelegt <xref:System.Collections.Generic.List%601> .

> [!WARNING]
> Der folgende Code verhält sich nicht ordnungsgemäß.

 [!code-csharp[PropertiesOvwSupport2#CollectionProblemDefinition](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertiesOvwSupport2/CSharp/page.xaml.cs#collectionproblemdefinition)]
 [!code-vb[PropertiesOvwSupport2#CollectionProblemDefinition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertiesOvwSupport2/visualbasic/page.xaml.vb#collectionproblemdefinition)]  
  
 Wenn Sie den Code unverändert lassen, wird dieser einzelne Listenstandardwert für alle Instanzen von `Aquarium` freigegeben. Beim Ausführen des folgenden Testcodes, der zeigen soll, wie zwei getrennte `Aquarium`-Instanzen instanziiert und jeder ein einzelner unterschiedlicher `Fish` hinzugefügt würde, käme es zu einem überraschenden Ergebnis:  
  
 [!code-csharp[PropertiesOvwSupport#CollectionProblemTestCode](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertiesOvwSupport/CSharp/page4.xaml.cs#collectionproblemtestcode)]
 [!code-vb[PropertiesOvwSupport#CollectionProblemTestCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertiesOvwSupport/visualbasic/page4.xaml.vb#collectionproblemtestcode)]  
  
 Anstatt eines Eintrags besitzt jede Auflistung nun zwei! Das liegt daran, dass jedes `Aquarium` seinen `Fish` der Standardwertauflistung hinzugefügt hat, die das Ergebnis eines einzelnen Konstruktoraufrufs in den Metadaten ist und daher für alle Instanzen freigegeben ist. Diese Situation ist so gut wie nie erwünscht.  
  
 Zur Behebung des Problems müssen Sie den Abhängigkeitseigenschaftswert der Auflistung auf eine eindeutige Instanz als Teil des Klassenkonstruktoraufrufs zurücksetzen. Da die-Eigenschaft eine schreibgeschützte Abhängigkeits Eigenschaft ist, verwenden Sie die- <xref:System.Windows.DependencyObject.SetValue%28System.Windows.DependencyPropertyKey%2CSystem.Object%29> Methode, um Sie mithilfe von festzulegen, auf die <xref:System.Windows.DependencyPropertyKey> nur innerhalb der-Klasse zugegriffen werden kann.  
  
 [!code-csharp[PropertiesOvwSupport#CollectionProblemCtor](~/samples/snippets/csharp/VS_Snippets_Wpf/PropertiesOvwSupport/CSharp/page4.xaml.cs#collectionproblemctor)]
 [!code-vb[PropertiesOvwSupport#CollectionProblemCtor](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PropertiesOvwSupport/visualbasic/page4.xaml.vb#collectionproblemctor)]  
  
 Bei einer erneuten Ausführung des Testcodes wären die Ergebnisse nun eher wie erwartet, da jedes `Aquarium` seine eigene eindeutige Auflistung unterstützen würde.  
  
 Dieses Muster wäre geringfügig abgewandelt, wenn Sie die Auflistungseigenschaft mit Lese-/Schreibzugriff wählen würden. In diesem Fall könnten Sie den Public-Set-Accessor vom Konstruktor aufrufen, um die Initialisierung durchzuführen, die nach wie vor die nicht Schlüssel Signatur von <xref:System.Windows.DependencyObject.SetValue%28System.Windows.DependencyProperty%2CSystem.Object%29> innerhalb des Set-Wrappers mit einem öffentlichen <xref:System.Windows.DependencyProperty> Bezeichner aufruft.  
  
## <a name="reporting-binding-value-changes-from-collection-properties"></a>Melden von Bindungswertänderungen durch Auflistungseigenschaften  
 Eine Auflistungseigenschaft, die selbst eine Abhängigkeitseigenschaft ist, meldet nicht automatisch Änderungen an die ihr untergeordneten Eigenschaften. Wenn Sie in einer Auflistung Bindungen erstellen, kann möglicherweise das Melden von Änderungen durch die Bindung verhindert werden, wodurch einige Datenbindungsszenarios ungültig gemacht werden können. Wenn Sie jedoch den Sammlungstyp <xref:System.Windows.FreezableCollection%601> als Auflistungstyp verwenden, werden Änderungen der untergeordneten Eigenschaft an enthaltene Elemente in der Auflistung ordnungsgemäß gemeldet, und die Bindung funktioniert wie erwartet.  
  
 Um die Bindung von untergeordneten Eigenschaften in einer Auflistung von Abhängigkeits Objekten zu aktivieren, erstellen Sie die Auflistungs Eigenschaft als Typ <xref:System.Windows.FreezableCollection%601> mit einer Typeinschränkung für diese Auflistung in eine beliebige <xref:System.Windows.DependencyObject> abgeleitete Klasse.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.FreezableCollection%601>
- [XAML- und benutzerdefinierte Klassen für WPF](xaml-and-custom-classes-for-wpf.md)
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Übersicht über Abhängigkeitseigenschaften](dependency-properties-overview.md)
- [Benutzerdefinierte Abhängigkeits Eigenschaften](custom-dependency-properties.md)
- [Metadaten für Abhängigkeitseigenschaften](dependency-property-metadata.md)
