---
title: 'Gewusst wie: Zeichnen eines Bereichs mit einer Volltonfarbe'
ms.date: 03/30/2017
helpviewer_keywords:
- solid colors [WPF], painting with
- brushes [WPF], painting with solid colors
- painting [WPF], with solid colors
ms.assetid: 5d27d8a7-4bd7-4063-bdf3-2c5c0f19f9d3
ms.openlocfilehash: be28a0af04c4e43cdf745a5429468aee99e34c40
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976539"
---
# <a name="how-to-paint-an-area-with-a-solid-color"></a><span data-ttu-id="bd66b-102">Gewusst wie: Zeichnen eines Bereichs mit einer Volltonfarbe</span><span class="sxs-lookup"><span data-stu-id="bd66b-102">How to: Paint an Area with a Solid Color</span></span>
<span data-ttu-id="bd66b-103">Um einen Bereich mit einer voll Tonfarbe zu zeichnen, können Sie einen vordefinierten System Pinsel verwenden, z. b. <xref:System.Windows.Media.Brushes.Red%2A> oder <xref:System.Windows.Media.Brushes.Blue%2A> , oder Sie können eine neue erstellen <xref:System.Windows.Media.SolidColorBrush> und deren <xref:System.Windows.Media.SolidColorBrush.Color%2A> mit Alpha-, rot-, grün-und blauen Werten beschreiben.</span><span class="sxs-lookup"><span data-stu-id="bd66b-103">To paint an area with a solid color, you can use a predefined system brush, such as <xref:System.Windows.Media.Brushes.Red%2A> or <xref:System.Windows.Media.Brushes.Blue%2A>, or you can create a new <xref:System.Windows.Media.SolidColorBrush> and describe its <xref:System.Windows.Media.SolidColorBrush.Color%2A> using alpha, red, green, and blue values.</span></span> <span data-ttu-id="bd66b-104">In XAML können Sie einen Bereich mit einer Volltonfarbe auch mit der Hexadezimalschreibweise zeichnen.</span><span class="sxs-lookup"><span data-stu-id="bd66b-104">In XAML, you may also paint an area with a solid color by using hexidecimal notation.</span></span>  
  
 <span data-ttu-id="bd66b-105">In den folgenden Beispielen wird jede dieser Techniken zum Zeichnen eines <xref:System.Windows.Shapes.Rectangle> blauen verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd66b-105">The following examples uses each of these techniques to paint a <xref:System.Windows.Shapes.Rectangle> blue.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bd66b-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bd66b-106">Example</span></span>  
 <span data-ttu-id="bd66b-107">**Verwenden eines vordefinierten Pinsels**</span><span class="sxs-lookup"><span data-stu-id="bd66b-107">**Using a Predefined Brush**</span></span>  
  
 <span data-ttu-id="bd66b-108">Im folgenden Beispiel wird der vordefinierte Pinsel <xref:System.Windows.Media.Brushes.Blue%2A> zum Zeichnen eines blauen Rechtecks verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd66b-108">In the following example uses the predefined brush <xref:System.Windows.Media.Brushes.Blue%2A> to paint a rectangle blue.</span></span>  
  
 [!code-xaml[brushsamples_snip#_graphicsmm_PredefinedBrush1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/SolidColorBrushExample.xaml#_graphicsmm_predefinedbrush1)]  
  
 [!code-csharp[brushsamples_procedural_snip#_graphicsmm_PredefinedBrush1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/SolidColorBrushExample.cs#_graphicsmm_predefinedbrush1)]  
  
 <span data-ttu-id="bd66b-109">**Hexadezimalnotation**</span><span class="sxs-lookup"><span data-stu-id="bd66b-109">**Using Hexadecimal Notation**</span></span>  
  
 <span data-ttu-id="bd66b-110">Im nächsten Beispiel wird die Hexadezimalschreibweise mit acht Ziffern verwendet.</span><span class="sxs-lookup"><span data-stu-id="bd66b-110">The next example uses 8-digit hexadecimal notation to paint a rectangle blue.</span></span>  
  
 [!code-xaml[brushsamples_snip#_graphicsmm_HexNotation8Digit1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/SolidColorBrushExample.xaml#_graphicsmm_hexnotation8digit1)]  
  
 <span data-ttu-id="bd66b-111">**Verwenden der ARGB-Werte**</span><span class="sxs-lookup"><span data-stu-id="bd66b-111">**Using ARGB Values**</span></span>  
  
 <span data-ttu-id="bd66b-112">Im nächsten Beispiel wird eine erstellt <xref:System.Windows.Media.SolidColorBrush> und <xref:System.Windows.Media.SolidColorBrush.Color%2A> die mit den ARGB-Werten für die Farbe blau beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bd66b-112">The next example creates a <xref:System.Windows.Media.SolidColorBrush> and describes its <xref:System.Windows.Media.SolidColorBrush.Color%2A> using the ARGB values for the color blue.</span></span>  
  
 [!code-xaml[brushsamples_snip#_graphicsmm_RgbNotation1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_snip/CS/SolidColorBrushExample.xaml#_graphicsmm_rgbnotation1)]  
  
 [!code-csharp[brushsamples_procedural_snip#_graphicsmm_RgbNotation1](~/samples/snippets/csharp/VS_Snippets_Wpf/brushsamples_procedural_snip/CSharp/SolidColorBrushExample.cs#_graphicsmm_rgbnotation1)]  
  
 <span data-ttu-id="bd66b-113">Weitere Methoden zum Beschreiben von Farben finden Sie in der <xref:System.Windows.Media.Color> Struktur.</span><span class="sxs-lookup"><span data-stu-id="bd66b-113">For other ways of describing color, see the <xref:System.Windows.Media.Color> structure.</span></span>  
  
 <span data-ttu-id="bd66b-114">**Verwandte Themen**</span><span class="sxs-lookup"><span data-stu-id="bd66b-114">**Related Topics**</span></span>  
  
 <span data-ttu-id="bd66b-115">Weitere Informationen zu <xref:System.Windows.Media.SolidColorBrush> und zusätzlichen Beispielen finden Sie unter Übersicht über das Zeichnen [mit voll Tonfarben und Farbverläufen](painting-with-solid-colors-and-gradients-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="bd66b-115">For more information about <xref:System.Windows.Media.SolidColorBrush> and additional examples, see the [Painting with Solid Colors and Gradients Overview](painting-with-solid-colors-and-gradients-overview.md) overview.</span></span>  
  
 <span data-ttu-id="bd66b-116">Dieses Codebeispiel ist Teil eines größeren Beispiels, das für die-Klasse bereitgestellt wird <xref:System.Windows.Media.SolidColorBrush> .</span><span class="sxs-lookup"><span data-stu-id="bd66b-116">This code example is part of a larger example provided for the <xref:System.Windows.Media.SolidColorBrush> class.</span></span> <span data-ttu-id="bd66b-117">Das vollständige Beispiel finden Sie unter der [Beispiel für Pinsel](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes).</span><span class="sxs-lookup"><span data-stu-id="bd66b-117">For the complete sample, see the [Brushes Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd66b-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd66b-118">See also</span></span>

- <xref:System.Windows.Media.Brushes>
