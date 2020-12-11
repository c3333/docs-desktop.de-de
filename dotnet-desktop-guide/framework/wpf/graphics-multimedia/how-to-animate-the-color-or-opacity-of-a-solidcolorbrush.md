---
title: 'Gewusst wie: Animieren der Farbe oder der Durchlässigkeit von SolidColorBrush'
ms.date: 03/30/2017
helpviewer_keywords:
- SolidColorBrush [WPF], animating color of
- colors [WPF], animating
- opacity [WPF], animating
- animation [WPF], color of SolidColorBrush
- animation [WPF], opacity of SolidColorBrush
- SolidColorBrush [WPF], animating opacity of
ms.assetid: d9154354-843f-4713-bad1-35bb0ba6eaeb
ms.openlocfilehash: 08b85935e0cb1ababd1fb63b9d02518ea3fcfa17
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975410"
---
# <a name="how-to-animate-the-color-or-opacity-of-a-solidcolorbrush"></a><span data-ttu-id="5bfc6-102">Gewusst wie: Animieren der Farbe oder der Durchlässigkeit von SolidColorBrush</span><span class="sxs-lookup"><span data-stu-id="5bfc6-102">How to: Animate the Color or Opacity of a SolidColorBrush</span></span>
<span data-ttu-id="5bfc6-103">In diesem Beispiel wird gezeigt, wie die <xref:System.Windows.Media.SolidColorBrush.Color%2A> und eines animiert werden <xref:System.Windows.Media.Brush.Opacity%2A> <xref:System.Windows.Media.SolidColorBrush> .</span><span class="sxs-lookup"><span data-stu-id="5bfc6-103">This example shows how to animate the <xref:System.Windows.Media.SolidColorBrush.Color%2A> and <xref:System.Windows.Media.Brush.Opacity%2A> of a <xref:System.Windows.Media.SolidColorBrush>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5bfc6-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5bfc6-104">Example</span></span>  
 <span data-ttu-id="5bfc6-105">Im folgenden Beispiel werden drei Animationen zum Animieren der <xref:System.Windows.Media.SolidColorBrush.Color%2A> und <xref:System.Windows.Media.Brush.Opacity%2A> einer verwendet <xref:System.Windows.Media.SolidColorBrush> .</span><span class="sxs-lookup"><span data-stu-id="5bfc6-105">The following example uses three animations to animate the <xref:System.Windows.Media.SolidColorBrush.Color%2A> and <xref:System.Windows.Media.Brush.Opacity%2A> of a <xref:System.Windows.Media.SolidColorBrush>.</span></span>  
  
- <span data-ttu-id="5bfc6-106">Die erste Animation, a <xref:System.Windows.Media.Animation.ColorAnimation> , ändert die Farbe des Pinsels in, <xref:System.Windows.Media.Colors.Gray%2A> Wenn die Maus in das Rechteck eintritt.</span><span class="sxs-lookup"><span data-stu-id="5bfc6-106">The first animation, a <xref:System.Windows.Media.Animation.ColorAnimation>, changes the brush's color to <xref:System.Windows.Media.Colors.Gray%2A> when the mouse enters the rectangle.</span></span>  
  
- <span data-ttu-id="5bfc6-107">Die nächste Animation, eine andere <xref:System.Windows.Media.Animation.ColorAnimation> , ändert die Farbe des Pinsels in, <xref:System.Windows.Media.Colors.Orange%2A> Wenn der Mauszeiger das Rechteck verlässt.</span><span class="sxs-lookup"><span data-stu-id="5bfc6-107">The next animation, another <xref:System.Windows.Media.Animation.ColorAnimation>, changes the brush's color to <xref:System.Windows.Media.Colors.Orange%2A> when the mouse leaves the rectangle.</span></span>  
  
- <span data-ttu-id="5bfc6-108">Die letzte Animation, a <xref:System.Windows.Media.Animation.DoubleAnimation> , ändert die Deckkraft des Pinsels in 0,0, wenn die linke Maustaste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="5bfc6-108">The final animation, a <xref:System.Windows.Media.Animation.DoubleAnimation>, changes the brush's opacity to 0.0 when the left mouse button is pressed.</span></span>  
  
 [!code-csharp[brushanimations_snip#SolidColorBrushAnimationExample](~/samples/snippets/csharp/VS_Snippets_Wpf/brushanimations_snip/CSharp/SolidColorBrushExample.cs#solidcolorbrushanimationexample)]  
  
 <span data-ttu-id="5bfc6-109">Ein ausführeres Beispiel, das zeigt, wie Sie verschiedene Arten von Pinseln animieren, finden Sie im [Beispiel Pinsel](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes).</span><span class="sxs-lookup"><span data-stu-id="5bfc6-109">For a more complete sample, which shows how to animate different types of brushes, see the [Brushes Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes).</span></span> <span data-ttu-id="5bfc6-110">Weitere Informationen zur Animation finden Sie unter [Übersicht über Animationen](animation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5bfc6-110">For more information about animation, see the [Animation Overview](animation-overview.md).</span></span>  
  
 <span data-ttu-id="5bfc6-111">Aus Gründen der Konsistenz mit anderen Animations Beispielen wird in den Code Versionen dieses Beispiels ein-Objekt verwendet, <xref:System.Windows.Media.Animation.Storyboard> um Ihre Animationen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="5bfc6-111">For consistency with other animation examples, the code versions of this example use a <xref:System.Windows.Media.Animation.Storyboard> object to apply their animations.</span></span> <span data-ttu-id="5bfc6-112">Beim Anwenden einer einzelnen Animation im Code ist es jedoch einfacher, die-Methode zu verwenden, <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> anstatt eine zu verwenden <xref:System.Windows.Media.Animation.Storyboard> .</span><span class="sxs-lookup"><span data-stu-id="5bfc6-112">However, when applying a single animation in code, it's simpler to use the <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> method instead of using a <xref:System.Windows.Media.Animation.Storyboard>.</span></span> <span data-ttu-id="5bfc6-113">Ein Beispiel finden Sie unter [Animieren einer Eigenschaft ohne Storyboard](how-to-animate-a-property-without-using-a-storyboard.md).</span><span class="sxs-lookup"><span data-stu-id="5bfc6-113">For an example, see [Animate a Property Without Using a Storyboard](how-to-animate-a-property-without-using-a-storyboard.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5bfc6-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bfc6-114">See also</span></span>

- [<span data-ttu-id="5bfc6-115">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="5bfc6-115">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="5bfc6-116">Übersicht über Storyboards</span><span class="sxs-lookup"><span data-stu-id="5bfc6-116">Storyboards Overview</span></span>](storyboards-overview.md)
- [<span data-ttu-id="5bfc6-117">Beispiel für Pinsel</span><span class="sxs-lookup"><span data-stu-id="5bfc6-117">Brushes Sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes)
