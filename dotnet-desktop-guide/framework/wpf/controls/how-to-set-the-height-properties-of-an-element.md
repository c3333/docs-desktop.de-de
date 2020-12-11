---
title: 'Gewusst wie: Festlegen der Höheneigenschaften eines Elements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- height properties [WPF]
- Panel control [WPF], height properties of elements
ms.assetid: 5ab9e781-dbb8-469a-a3c8-cf38ce312647
ms.openlocfilehash: f18612d66c477562eb387b76ea30e71dd5f4e8d7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977905"
---
# <a name="how-to-set-the-height-properties-of-an-element"></a>Gewusst wie: Festlegen der Höheneigenschaften eines Elements
## <a name="example"></a>Beispiel  
 In diesem Beispiel werden die Unterschiede im Renderingverhalten zwischen den vier Höhen bezogenen Eigenschaften in visuell dargestellt [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] .  
  
 Die- <xref:System.Windows.FrameworkElement> Klasse macht vier Eigenschaften verfügbar, die die Höhen Merkmale eines Elements beschreiben. Diese vier Eigenschaften können in Konflikt stehen. Wenn Sie dies tun, wird der Wert, der Vorrang hat, wie folgt bestimmt: der <xref:System.Windows.FrameworkElement.MinHeight%2A> Wert hat Vorrang vor dem Wert <xref:System.Windows.FrameworkElement.MaxHeight%2A> , der wiederum Vorrang vor dem <xref:System.Windows.FrameworkElement.Height%2A> Wert hat. Die vierte Eigenschaft, <xref:System.Windows.FrameworkElement.ActualHeight%2A> , ist schreibgeschützt und meldet die tatsächliche Höhe gemäß der durch Interaktionen mit dem Layoutprozess festgelegten Höhe.  
  
 In den folgenden [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beispielen wird ein- <xref:System.Windows.Shapes.Rectangle> Element ( `rect1` ) als untergeordnetes Element von gezeichnet <xref:System.Windows.Controls.Canvas> . Sie können die Height-Eigenschaften einer <xref:System.Windows.Shapes.Rectangle> mithilfe einer Reihe von-Elementen ändern, die <xref:System.Windows.Controls.ListBox> die Eigenschaftswerte von <xref:System.Windows.FrameworkElement.MinHeight%2A> , und darstellen <xref:System.Windows.FrameworkElement.MaxHeight%2A> <xref:System.Windows.FrameworkElement.Height%2A> . Auf diese Weise wird die Rangfolge der einzelnen Eigenschaften visuell angezeigt.  
  
 [!code-xaml[HeightMinHeightMaxHeight#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HeightMinHeightMaxHeight/CSharp/Window1.xaml#1)]  
[!code-xaml[HeightMinHeightMaxHeight#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HeightMinHeightMaxHeight/CSharp/Window1.xaml#2)]  
  
 In den folgenden Code Behind-Beispielen werden die Ereignisse behandelt, die das <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> Ereignis auslöst. Jeder Handler nimmt die Eingabe aus <xref:System.Windows.Controls.ListBox> , analysiert den Wert als <xref:System.Double> und wendet den Wert auf die angegebene Height-bezogene Eigenschaft an. Die Height-Werte werden auch in eine Zeichenfolge konvertiert und in verschiedene <xref:System.Windows.Controls.TextBlock> Elemente geschrieben (Definition dieser Elemente wird im ausgewählten XAML-Code nicht angezeigt).  
  
 [!code-csharp[HeightMinHeightMaxHeight#3](~/samples/snippets/csharp/VS_Snippets_Wpf/HeightMinHeightMaxHeight/CSharp/Window1.xaml.cs#3)]
 [!code-vb[HeightMinHeightMaxHeight#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HeightMinHeightMaxHeight/VisualBasic/Window1.xaml.vb#3)]  
  
 Das komplette Beispiel finden Sie unter [height Properties Sample](https://github.com/microsoft/WPF-Samples/tree/master/Elements/HeightProperties).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.FrameworkElement>
- <xref:System.Windows.Controls.ListBox>
- <xref:System.Windows.FrameworkElement.ActualHeight%2A>
- <xref:System.Windows.FrameworkElement.MaxHeight%2A>
- <xref:System.Windows.FrameworkElement.MinHeight%2A>
- <xref:System.Windows.FrameworkElement.Height%2A>
- [Festlegen der Breiteneigenschaften eines Elements](how-to-set-the-width-properties-of-an-element.md)
- [Übersicht über Panel-Elemente](panels-overview.md)
- [Beispiel für Height-Eigenschaften](https://github.com/microsoft/WPF-Samples/tree/master/Elements/HeightProperties)
