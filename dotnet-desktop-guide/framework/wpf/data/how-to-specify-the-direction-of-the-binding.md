---
title: 'Gewusst wie: Angeben der Bindungsrichtung'
ms.date: 03/30/2017
helpviewer_keywords:
- direction of binding [WPF]
- binding direction [WPF]
- data binding [WPF], direction of binding
ms.assetid: 37334478-028b-4514-86c9-1420709f4818
ms.openlocfilehash: 6b3c6afde5e9fa1b778905b1a278bb295b6cbf11
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976551"
---
# <a name="how-to-specify-the-direction-of-the-binding"></a>Gewusst wie: Angeben der Bindungs Richtung

In diesem Beispiel wird erläutert, wie sich angeben lässt, ob die Bindung nur die Eigenschaft „Bindungsziel (Ziel)“, „Bindungsquelle (Quelle)“ oder sowohl die Ziel- als auch die Quelleigenschaft aktualisiert.  
  
## <a name="example"></a>Beispiel  
 Verwenden Sie die- <xref:System.Windows.Data.Binding.Mode%2A?displayProperty=nameWithType> Eigenschaft, um die Bindungs Richtung anzugeben. Im folgenden finden Sie die verfügbaren Optionen für das Binden von Updates:  
  
- <xref:System.Windows.Data.BindingMode.TwoWay?displayProperty=nameWithType> Aktualisiert die Ziel Eigenschaft oder die-Eigenschaft, wenn sich entweder die Ziel Eigenschaft oder die Quell Eigenschaft ändert.  
  
- <xref:System.Windows.Data.BindingMode.OneWay?displayProperty=nameWithType> Aktualisiert die Ziel Eigenschaft nur, wenn sich die Quell Eigenschaft ändert.  
  
- <xref:System.Windows.Data.BindingMode.OneTime?displayProperty=nameWithType> Aktualisiert die Ziel Eigenschaft nur, wenn die Anwendung gestartet wird oder wenn <xref:System.Windows.FrameworkElement.DataContext%2A> eine Änderung durchläuft.  
  
- <xref:System.Windows.Data.BindingMode.OneWayToSource?displayProperty=nameWithType> Aktualisiert die Quell Eigenschaft, wenn die Ziel Eigenschaft geändert wird.  
  
- <xref:System.Windows.Data.BindingMode.Default?displayProperty=nameWithType> bewirkt <xref:System.Windows.Data.Binding.Mode%2A> , dass der Standardwert der Ziel Eigenschaft verwendet wird.  
  
 Weitere Informationen finden Sie unter der <xref:System.Windows.Data.BindingMode>-Enumeration.  
  
 Im folgenden Beispiel wird das Festlegen der <xref:System.Windows.Data.Binding.Mode%2A>-Eigenschaft veranschaulicht.  
  
 [!code-xaml[DirectionalBinding#4](~/samples/snippets/csharp/VS_Snippets_Wpf/DirectionalBinding/CSharp/Page1.xaml#4)]  
  
 Zum Erkennen von Quelländerungen (das gilt für die <xref:System.Windows.Data.BindingMode.OneWay>-Bindung und die <xref:System.Windows.Data.BindingMode.TwoWay>-Bindung) muss die Quelle einen geeigneten Mechanismus für Benachrichtigungen bei Eigenschaftenänderungen implementieren, z. B. <xref:System.ComponentModel.INotifyPropertyChanged>. Ein Beispiel für eine-Implementierung finden Sie unter [Implementieren von Benachrichtigungen über Eigenschafts Änderungen](how-to-implement-property-change-notification.md) <xref:System.ComponentModel.INotifyPropertyChanged> .  
  
 Für- <xref:System.Windows.Data.BindingMode.TwoWay> oder- <xref:System.Windows.Data.BindingMode.OneWayToSource> Bindungen können Sie die zeitliche Steuerung der Quell Aktualisierungen steuern, indem Sie die- <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A> Eigenschaft festlegen. Weitere Informationen finden Sie unter <xref:System.Windows.Data.Binding.UpdateSourceTrigger%2A>.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Data.Binding>
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
