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
# <a name="how-to-set-the-width-properties-of-an-element"></a><span data-ttu-id="38fbf-102">Gewusst wie: Festlegen der Breiteneigenschaften eines Elements</span><span class="sxs-lookup"><span data-stu-id="38fbf-102">How to: Set the Width Properties of an Element</span></span>
## <a name="example"></a><span data-ttu-id="38fbf-103">Beispiel</span><span class="sxs-lookup"><span data-stu-id="38fbf-103">Example</span></span>  
 <span data-ttu-id="38fbf-104">In diesem Beispiel werden die Unterschiede im Renderingverhalten zwischen den vier breiten bezogenen Eigenschaften in visuell dargestellt [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="38fbf-104">This example visually shows the differences in rendering behavior among the four width-related properties in [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)].</span></span>  
  
 <span data-ttu-id="38fbf-105">Die- <xref:System.Windows.FrameworkElement> Klasse macht vier Eigenschaften verfügbar, die die Breite Merkmale eines Elements beschreiben.</span><span class="sxs-lookup"><span data-stu-id="38fbf-105">The <xref:System.Windows.FrameworkElement> class exposes four properties that describe the width characteristics of an element.</span></span> <span data-ttu-id="38fbf-106">Diese vier Eigenschaften können in Konflikt stehen. Wenn Sie dies tun, wird der Wert, der Vorrang hat, wie folgt bestimmt: der <xref:System.Windows.FrameworkElement.MinWidth%2A> Wert hat Vorrang vor dem Wert <xref:System.Windows.FrameworkElement.MaxWidth%2A> , der wiederum Vorrang vor dem <xref:System.Windows.FrameworkElement.Width%2A> Wert hat.</span><span class="sxs-lookup"><span data-stu-id="38fbf-106">These four properties can conflict, and when they do, the value that takes precedence is determined as follows: the <xref:System.Windows.FrameworkElement.MinWidth%2A> value takes precedence over the <xref:System.Windows.FrameworkElement.MaxWidth%2A> value, which in turn takes precedence over the <xref:System.Windows.FrameworkElement.Width%2A> value.</span></span> <span data-ttu-id="38fbf-107">Eine vierte Eigenschaft, <xref:System.Windows.FrameworkElement.ActualWidth%2A> , ist schreibgeschützt und meldet die tatsächliche Breite, wie durch Interaktionen mit dem Layoutprozess festgelegt.</span><span class="sxs-lookup"><span data-stu-id="38fbf-107">A fourth property, <xref:System.Windows.FrameworkElement.ActualWidth%2A>, is read-only, and reports the actual width as determined by interactions with the layout process.</span></span>  
  
 <span data-ttu-id="38fbf-108">In den folgenden [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beispielen wird ein- <xref:System.Windows.Shapes.Rectangle> Element ( `rect1` ) als untergeordnetes Element von gezeichnet <xref:System.Windows.Controls.Canvas> .</span><span class="sxs-lookup"><span data-stu-id="38fbf-108">The following [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] examples draw a <xref:System.Windows.Shapes.Rectangle> element (`rect1`) as a child of <xref:System.Windows.Controls.Canvas>.</span></span> <span data-ttu-id="38fbf-109">Sie können die Width-Eigenschaften einer <xref:System.Windows.Shapes.Rectangle> mithilfe einer Reihe von-Elementen ändern, die <xref:System.Windows.Controls.ListBox> die Eigenschaftswerte von <xref:System.Windows.FrameworkElement.MinWidth%2A> , und darstellen <xref:System.Windows.FrameworkElement.MaxWidth%2A> <xref:System.Windows.FrameworkElement.Width%2A> .</span><span class="sxs-lookup"><span data-stu-id="38fbf-109">You can change the width properties of a <xref:System.Windows.Shapes.Rectangle> by using a series of <xref:System.Windows.Controls.ListBox> elements that represent the property values of <xref:System.Windows.FrameworkElement.MinWidth%2A>, <xref:System.Windows.FrameworkElement.MaxWidth%2A>, and <xref:System.Windows.FrameworkElement.Width%2A>.</span></span> <span data-ttu-id="38fbf-110">Auf diese Weise wird die Rangfolge der einzelnen Eigenschaften visuell angezeigt.</span><span class="sxs-lookup"><span data-stu-id="38fbf-110">In this manner, the precedence of each property is visually displayed.</span></span>  
  
 [!code-xaml[WidthMinWidthMaxWidth#1](~/samples/snippets/csharp/VS_Snippets_Wpf/WidthMinWidthMaxWidth/CSharp/Window1.xaml#1)]  
[!code-xaml[WidthMinWidthMaxWidth#2](~/samples/snippets/csharp/VS_Snippets_Wpf/WidthMinWidthMaxWidth/CSharp/Window1.xaml#2)]  
  
 <span data-ttu-id="38fbf-111">In den folgenden Code Behind-Beispielen werden die Ereignisse behandelt, die das <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="38fbf-111">The following code-behind examples handle the events that the <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> event raises.</span></span> <span data-ttu-id="38fbf-112">Jede benutzerdefinierte Methode nimmt die Eingabe aus <xref:System.Windows.Controls.ListBox> , analysiert den Wert als <xref:System.Double> und wendet den Wert auf die angegebene Width-bezogene Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="38fbf-112">Each custom method takes the input from the <xref:System.Windows.Controls.ListBox>, parses the value as a <xref:System.Double>, and applies the value to the specified width-related property.</span></span> <span data-ttu-id="38fbf-113">Die Width-Werte werden auch in eine Zeichenfolge konvertiert und in verschiedene <xref:System.Windows.Controls.TextBlock> Elemente geschrieben (Definition dieser Elemente wird im ausgewählten XAML-Code nicht angezeigt).</span><span class="sxs-lookup"><span data-stu-id="38fbf-113">The width values are also converted to a string and written to various <xref:System.Windows.Controls.TextBlock> elements (definition of those elements is not shown in the selected XAML).</span></span>  
  
 [!code-csharp[WidthMinWidthMaxWidth#3](~/samples/snippets/csharp/VS_Snippets_Wpf/WidthMinWidthMaxWidth/CSharp/Window1.xaml.cs#3)]
 [!code-vb[WidthMinWidthMaxWidth#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/WidthMinWidthMaxWidth/VisualBasic/Window1.xaml.vb#3)]  
  
 <span data-ttu-id="38fbf-114">Das komplette Beispiel finden Sie unter [Width Properties Comparison Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Elements/WidthProperties).</span><span class="sxs-lookup"><span data-stu-id="38fbf-114">For the complete sample, see [Width Properties Comparison Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Elements/WidthProperties).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38fbf-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38fbf-115">See also</span></span>

- <xref:System.Windows.Controls.ListBox>
- <xref:System.Windows.FrameworkElement>
- <xref:System.Windows.FrameworkElement.ActualWidth%2A>
- <xref:System.Windows.FrameworkElement.MaxWidth%2A>
- <xref:System.Windows.FrameworkElement.MinWidth%2A>
- <xref:System.Windows.FrameworkElement.Width%2A>
- [<span data-ttu-id="38fbf-116">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="38fbf-116">Panels Overview</span></span>](panels-overview.md)
- [<span data-ttu-id="38fbf-117">Festlegen der Höheneigenschaften eines Elements</span><span class="sxs-lookup"><span data-stu-id="38fbf-117">Set the Height Properties of an Element</span></span>](how-to-set-the-height-properties-of-an-element.md)
- [<span data-ttu-id="38fbf-118">Vergleichsbeispiel für Width Properties</span><span class="sxs-lookup"><span data-stu-id="38fbf-118">Width Properties Comparison Sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Elements/WidthProperties)
