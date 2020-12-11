---
title: 'Gewusst wie: Festlegen der Breiteneigenschaften eines Elements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- width properties [WPF]
- Panel control [WPF], width properties of elements
ms.assetid: 6ee04a9d-63f0-4f5b-a406-0a8cd4c35729
ms.openlocfilehash: fcdb8d58c17137d22edd4ee8cf6768c5d7def7c5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975338"
---
# <a name="how-to-set-the-width-properties-of-an-element"></a>Gewusst wie: Festlegen der Breiteneigenschaften eines Elements
## <a name="example"></a>Beispiel  
 In diesem Beispiel werden die Unterschiede im Renderingverhalten zwischen den vier breiten bezogenen Eigenschaften in visuell dargestellt [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] .  
  
 Die- <xref:System.Windows.FrameworkElement> Klasse macht vier Eigenschaften verfügbar, die die Breite Merkmale eines Elements beschreiben. Diese vier Eigenschaften können in Konflikt stehen. Wenn Sie dies tun, wird der Wert, der Vorrang hat, wie folgt bestimmt: der <xref:System.Windows.FrameworkElement.MinWidth%2A> Wert hat Vorrang vor dem Wert <xref:System.Windows.FrameworkElement.MaxWidth%2A> , der wiederum Vorrang vor dem <xref:System.Windows.FrameworkElement.Width%2A> Wert hat. Eine vierte Eigenschaft, <xref:System.Windows.FrameworkElement.ActualWidth%2A> , ist schreibgeschützt und meldet die tatsächliche Breite, wie durch Interaktionen mit dem Layoutprozess festgelegt.  
  
 In den folgenden [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beispielen wird ein- <xref:System.Windows.Shapes.Rectangle> Element ( `rect1` ) als untergeordnetes Element von gezeichnet <xref:System.Windows.Controls.Canvas> . Sie können die Width-Eigenschaften einer <xref:System.Windows.Shapes.Rectangle> mithilfe einer Reihe von-Elementen ändern, die <xref:System.Windows.Controls.ListBox> die Eigenschaftswerte von <xref:System.Windows.FrameworkElement.MinWidth%2A> , und darstellen <xref:System.Windows.FrameworkElement.MaxWidth%2A> <xref:System.Windows.FrameworkElement.Width%2A> . Auf diese Weise wird die Rangfolge der einzelnen Eigenschaften visuell angezeigt.  
  
 [!code-xaml[WidthMinWidthMaxWidth#1](~/samples/snippets/csharp/VS_Snippets_Wpf/WidthMinWidthMaxWidth/CSharp/Window1.xaml#1)]  
[!code-xaml[WidthMinWidthMaxWidth#2](~/samples/snippets/csharp/VS_Snippets_Wpf/WidthMinWidthMaxWidth/CSharp/Window1.xaml#2)]  
  
 In den folgenden Code Behind-Beispielen werden die Ereignisse behandelt, die das <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> Ereignis auslöst. Jede benutzerdefinierte Methode nimmt die Eingabe aus <xref:System.Windows.Controls.ListBox> , analysiert den Wert als <xref:System.Double> und wendet den Wert auf die angegebene Width-bezogene Eigenschaft an. Die Width-Werte werden auch in eine Zeichenfolge konvertiert und in verschiedene <xref:System.Windows.Controls.TextBlock> Elemente geschrieben (Definition dieser Elemente wird im ausgewählten XAML-Code nicht angezeigt).  
  
 [!code-csharp[WidthMinWidthMaxWidth#3](~/samples/snippets/csharp/VS_Snippets_Wpf/WidthMinWidthMaxWidth/CSharp/Window1.xaml.cs#3)]
 [!code-vb[WidthMinWidthMaxWidth#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WidthMinWidthMaxWidth/VisualBasic/Window1.xaml.vb#3)]  
  
 Das komplette Beispiel finden Sie unter [Width Properties Comparison Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Elements/WidthProperties).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.ListBox>
- <xref:System.Windows.FrameworkElement>
- <xref:System.Windows.FrameworkElement.ActualWidth%2A>
- <xref:System.Windows.FrameworkElement.MaxWidth%2A>
- <xref:System.Windows.FrameworkElement.MinWidth%2A>
- <xref:System.Windows.FrameworkElement.Width%2A>
- [Übersicht über Panel-Elemente](panels-overview.md)
- [Festlegen der Höheneigenschaften eines Elements](how-to-set-the-height-properties-of-an-element.md)
- [Vergleichsbeispiel für Width Properties](https://github.com/Microsoft/WPF-Samples/tree/master/Elements/WidthProperties)
