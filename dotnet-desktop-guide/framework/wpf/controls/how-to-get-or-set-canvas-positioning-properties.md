---
title: 'Gewusst wie: Abrufen und Festlegen von Canvas-Positionierungseigenschaften'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Canvas control [WPF], setting positioning properties
ms.assetid: 1636b950-2b5a-4507-8a10-c5034cc58b1c
ms.openlocfilehash: 06508e1198736ccb1cbda41641dff4bc634ef82b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975498"
---
# <a name="how-to-get-or-set-canvas-positioning-properties"></a><span data-ttu-id="1e431-102">Gewusst wie: Abrufen und Festlegen von Canvas-Positionierungseigenschaften</span><span class="sxs-lookup"><span data-stu-id="1e431-102">How to: Get or Set Canvas Positioning Properties</span></span>
<span data-ttu-id="1e431-103">In diesem Beispiel wird gezeigt, wie die Positions Methoden des-Elements verwendet werden <xref:System.Windows.Controls.Canvas> , um untergeordneten Inhalt zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="1e431-103">This example shows how to use the positioning methods of the <xref:System.Windows.Controls.Canvas> element to position child content.</span></span> <span data-ttu-id="1e431-104">In diesem Beispiel wird der Inhalt in einem verwendet <xref:System.Windows.Controls.ListBoxItem> , um Positionierungs Werte darzustellen, und die Werte werden in Instanzen von konvertiert <xref:System.Double> . Dies ist ein erforderliches Argument für die Positionierung.</span><span class="sxs-lookup"><span data-stu-id="1e431-104">This example uses content in a <xref:System.Windows.Controls.ListBoxItem> to represent positioning values and converts the values into instances of <xref:System.Double>, which is a required argument for positioning.</span></span> <span data-ttu-id="1e431-105">Die Werte werden dann wieder in Zeichen folgen konvertiert und als Text in einem- <xref:System.Windows.Controls.TextBlock> Element mithilfe der- <xref:System.Windows.Controls.Canvas.GetLeft%2A> Methode angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1e431-105">The values are then converted back into strings and displayed as text in a <xref:System.Windows.Controls.TextBlock> element by using the <xref:System.Windows.Controls.Canvas.GetLeft%2A> method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1e431-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1e431-106">Example</span></span>  
 <span data-ttu-id="1e431-107">Im folgenden Beispiel wird ein- <xref:System.Windows.Controls.ListBox> Element erstellt, das elf auswählbare <xref:System.Windows.Controls.ListBoxItem> Elemente aufweist.</span><span class="sxs-lookup"><span data-stu-id="1e431-107">The following example creates a <xref:System.Windows.Controls.ListBox> element that has eleven selectable <xref:System.Windows.Controls.ListBoxItem> elements.</span></span> <span data-ttu-id="1e431-108">Das- <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> Ereignis löst die `ChangeLeft` benutzerdefinierte-Methode aus, die der nachfolgende Codeblock definiert.</span><span class="sxs-lookup"><span data-stu-id="1e431-108">The <xref:System.Windows.Controls.Primitives.Selector.SelectionChanged> event triggers the `ChangeLeft` custom method, which the subsequent code block defines.</span></span>  
  
 <span data-ttu-id="1e431-109">Jeder <xref:System.Windows.Controls.ListBoxItem> stellt einen- <xref:System.Double> Wert dar, der eines der Argumente ist, die von der- <xref:System.Windows.Controls.Canvas.SetLeft%2A> Methode akzeptiert werden <xref:System.Windows.Controls.Canvas> .</span><span class="sxs-lookup"><span data-stu-id="1e431-109">Each <xref:System.Windows.Controls.ListBoxItem> represents a <xref:System.Double> value, which is one of the arguments that the <xref:System.Windows.Controls.Canvas.SetLeft%2A> method of <xref:System.Windows.Controls.Canvas> accepts.</span></span> <span data-ttu-id="1e431-110">Um einen <xref:System.Windows.Controls.ListBoxItem> zur Darstellung einer Instanz von verwenden zu <xref:System.Double> können, müssen Sie zuerst den <xref:System.Windows.Controls.ListBoxItem> in den richtigen Datentyp konvertieren.</span><span class="sxs-lookup"><span data-stu-id="1e431-110">In order to use a <xref:System.Windows.Controls.ListBoxItem> to represent an instance of <xref:System.Double>, you must first convert the <xref:System.Windows.Controls.ListBoxItem> to the correct data type.</span></span>  
  
 [!code-xaml[CanvasPositioningProperties#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasPositioningProperties/CSharp/Window1.xaml#1)]  
  
 <span data-ttu-id="1e431-111">Wenn ein Benutzer die <xref:System.Windows.Controls.ListBox> Auswahl ändert, wird die Benutzer `ChangeLeft` definierte Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1e431-111">When a user changes the <xref:System.Windows.Controls.ListBox> selection, it invokes the `ChangeLeft` custom method.</span></span> <span data-ttu-id="1e431-112">Diese Methode übergibt das <xref:System.Windows.Controls.ListBoxItem> an ein- <xref:System.Windows.LengthConverter> Objekt, das den einer <xref:System.Windows.Controls.ContentControl.Content%2A> <xref:System.Windows.Controls.ListBoxItem> in eine-Instanz konvertiert <xref:System.Double> (Beachten Sie, dass dieser Wert bereits mit der-Methode in eine konvertiert wurde <xref:System.String> <xref:System.Windows.Controls.Control.ToString%2A> ).</span><span class="sxs-lookup"><span data-stu-id="1e431-112">This method passes the <xref:System.Windows.Controls.ListBoxItem> to a <xref:System.Windows.LengthConverter> object, which converts the <xref:System.Windows.Controls.ContentControl.Content%2A> of a <xref:System.Windows.Controls.ListBoxItem> to an instance of <xref:System.Double> (notice that this value has already been converted to a <xref:System.String> by using the <xref:System.Windows.Controls.Control.ToString%2A> method).</span></span> <span data-ttu-id="1e431-113">Dieser Wert wird dann an die <xref:System.Windows.Controls.Canvas.SetLeft%2A> -Methode und die- <xref:System.Windows.Controls.Canvas.GetLeft%2A> Methode von zurückgegeben, um <xref:System.Windows.Controls.Canvas> die Position des-Objekts zu ändern `text1` .</span><span class="sxs-lookup"><span data-stu-id="1e431-113">This value is then passed back to the <xref:System.Windows.Controls.Canvas.SetLeft%2A> and <xref:System.Windows.Controls.Canvas.GetLeft%2A> methods of <xref:System.Windows.Controls.Canvas> in order to change the position of the `text1` object.</span></span>  
  
 [!code-csharp[CanvasPositioningProperties#2](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasPositioningProperties/CSharp/Window1.xaml.cs#2)]
 [!code-vb[CanvasPositioningProperties#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasPositioningProperties/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="1e431-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e431-114">See also</span></span>

- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.ListBoxItem>
- <xref:System.Windows.LengthConverter>
- [<span data-ttu-id="1e431-115">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="1e431-115">Panels Overview</span></span>](panels-overview.md)
