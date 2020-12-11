---
title: 'Gewusst wie: Konvertieren von gebundenen Daten'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- converting [WPF], bound data
- data binding [WPF], converting bound data
- binding data [WPF], converting bound data
ms.assetid: b00aaa19-c6df-4c3b-a9fd-88a0b488df2b
ms.openlocfilehash: 981994426afd173fa8560d3ee24c6cf24c0c24aa
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977183"
---
# <a name="how-to-convert-bound-data"></a>Gewusst wie: Konvertieren von gebundenen Daten
In diesem Beispiel wird gezeigt, wie die Konvertierung auf Daten angewendet wird, die in Bindungen verwendet werden.  
  
 Zum Konvertieren von Daten während der Bindung müssen Sie eine Klasse erstellen, die die <xref:System.Windows.Data.IValueConverter> -Schnittstelle implementiert, die die <xref:System.Windows.Data.IValueConverter.Convert%2A> -Methode und die- <xref:System.Windows.Data.IValueConverter.ConvertBack%2A> Methode enthält.  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt die Implementierung eines Datums Konverters, der den Wert für den Datumswert konvertiert, sodass er nur das Jahr, den Monat und den Tag anzeigt. Beim Implementieren der- <xref:System.Windows.Data.IValueConverter> Schnittstelle empfiehlt es sich, die-Implementierung mit einem- <xref:System.Windows.Data.ValueConversionAttribute> Attribut zu versehen, um den Entwicklungs Tools die Datentypen anzuzeigen, die an der Konvertierung beteiligt sind, wie im folgenden Beispiel gezeigt:  
  
 [!code-csharp[DataBindingLab#18](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/DateConverter.cs#18)]
 [!code-vb[DataBindingLab#18](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DataBindingLab/VisualBasic/DateConverter.vb#18)]  
  
 Nachdem Sie einen Konverter erstellt haben, können Sie ihn als Ressource in Ihrer Datei hinzufügen [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] . Im folgenden Beispiel wird *src* dem-Namespace zugeordnet, in dem *DateConverter* definiert ist.  
  
 [!code-xaml[DataBindingLab#15](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/DataBindingLabApp.xaml#15)]  
  
 Schließlich können Sie den Konverter in der Bindung verwenden, indem Sie die folgende Syntax verwenden. Im folgenden Beispiel wird der Text Inhalt des <xref:System.Windows.Controls.TextBlock> an *StartDate* gebunden, das eine Eigenschaft einer externen Datenquelle ist.  
  
 [!code-xaml[DataBindingLab#17](~/samples/snippets/csharp/VS_Snippets_Wpf/DataBindingLab/CSharp/DataBindingLabApp.xaml#17)]  
  
 Die im obigen Beispiel referenzierten Stil Ressourcen werden in einem Ressourcenabschnitt definiert, der in diesem Thema nicht angezeigt wird.  
  
## <a name="see-also"></a>Siehe auch

- [Implementieren der Bindungs Validierung](how-to-implement-binding-validation.md)
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
