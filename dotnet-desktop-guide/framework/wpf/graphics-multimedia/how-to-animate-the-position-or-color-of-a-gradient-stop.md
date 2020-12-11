---
title: 'Gewusst wie: Animieren der Position oder Farbe eines Farbverlaufunterbrechungspunkts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- position [WPF], animating
- animation [WPF], position of GradientStop objects
- GradientStop objects [WPF], animating color of
- colors [WPF], animating
- animation [WPF], color of GradientStop objects
- GradientStop objects [WPF], animating position of
ms.assetid: 6f5b8b47-6c32-4b8e-98ee-fdf6515ec843
ms.openlocfilehash: aeae33f5f3c8016808988f58d61969e9b6f05039
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975330"
---
# <a name="how-to-animate-the-position-or-color-of-a-gradient-stop"></a><span data-ttu-id="2c919-102">Gewusst wie: Animieren der Position oder Farbe eines Farbverlaufunterbrechungspunkts</span><span class="sxs-lookup"><span data-stu-id="2c919-102">How to: Animate the Position or Color of a Gradient Stop</span></span>
<span data-ttu-id="2c919-103">Dieses Beispiel zeigt, wie das <xref:System.Windows.Media.GradientStop.Color%2A> -Objekt und das-Objekt animiert werden <xref:System.Windows.Media.GradientStop.Offset%2A> <xref:System.Windows.Media.GradientStop> .</span><span class="sxs-lookup"><span data-stu-id="2c919-103">This example shows how to animate the <xref:System.Windows.Media.GradientStop.Color%2A> and <xref:System.Windows.Media.GradientStop.Offset%2A> of <xref:System.Windows.Media.GradientStop> objects.</span></span>  
  
## <a name="example"></a><span data-ttu-id="2c919-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2c919-104">Example</span></span>  
 <span data-ttu-id="2c919-105">Im folgenden Beispiel werden drei Farbverlaufs Stopps in einem animiert <xref:System.Windows.Media.LinearGradientBrush> .</span><span class="sxs-lookup"><span data-stu-id="2c919-105">The following example animates three gradient stops inside a <xref:System.Windows.Media.LinearGradientBrush>.</span></span> <span data-ttu-id="2c919-106">In diesem Beispiel werden drei Animationen verwendet, von denen jede einen anderen Farbverlaufs-halte Vorgang animiert:</span><span class="sxs-lookup"><span data-stu-id="2c919-106">The example uses three animations, each of which animates a different gradient stop:</span></span>  
  
- <span data-ttu-id="2c919-107">Die erste Animation, a <xref:System.Windows.Media.Animation.DoubleAnimation> , animiert den ersten Farbverlaufs anzuhalten <xref:System.Windows.Media.GradientStop.Offset%2A> von 0,0 bis 1,0 und dann zurück zu 0,0.</span><span class="sxs-lookup"><span data-stu-id="2c919-107">The first animation, a <xref:System.Windows.Media.Animation.DoubleAnimation>, animates the first gradient stop's <xref:System.Windows.Media.GradientStop.Offset%2A> from 0.0 to 1.0 and then back to 0.0.</span></span> <span data-ttu-id="2c919-108">Folglich verschiebt sich die erste Farbe im Farbverlauf von der linken zum rechten Rand des Rechtecks und dann zurück zur linken Seite.</span><span class="sxs-lookup"><span data-stu-id="2c919-108">As a result, the first color in the gradient shifts from the left side to the right side of the rectangle and then back to the left side.</span></span>  
  
- <span data-ttu-id="2c919-109">Die zweite Animation, a <xref:System.Windows.Media.Animation.ColorAnimation> , animiert die zweite Farbverlaufs Stopps <xref:System.Windows.Media.GradientStop.Color%2A> von <xref:System.Windows.Media.Colors.Purple%2A> auf <xref:System.Windows.Media.Colors.Yellow%2A> und dann zurück zu <xref:System.Windows.Media.Colors.Purple%2A> .</span><span class="sxs-lookup"><span data-stu-id="2c919-109">The second animation, a <xref:System.Windows.Media.Animation.ColorAnimation>, animates the second gradient stop's <xref:System.Windows.Media.GradientStop.Color%2A> from <xref:System.Windows.Media.Colors.Purple%2A> to <xref:System.Windows.Media.Colors.Yellow%2A> and then back to <xref:System.Windows.Media.Colors.Purple%2A>.</span></span> <span data-ttu-id="2c919-110">Folglich wechselt die Mittel Farbe im Farbverlauf von lila in gelb und zurück zu Lila.</span><span class="sxs-lookup"><span data-stu-id="2c919-110">As a result, the middle color in the gradient changes from purple to yellow and back to purple.</span></span>  
  
- <span data-ttu-id="2c919-111">Die dritte Animation, eine andere <xref:System.Windows.Media.Animation.ColorAnimation> , animiert die Deckkraft des dritten Farbverlaufs Stopps <xref:System.Windows.Media.GradientStop.Color%2A> durch-1 und dann zurück.</span><span class="sxs-lookup"><span data-stu-id="2c919-111">The third animation, another <xref:System.Windows.Media.Animation.ColorAnimation>, animates the opacity of the third gradient stop's <xref:System.Windows.Media.GradientStop.Color%2A> by -1 and then back.</span></span> <span data-ttu-id="2c919-112">Folglich wird die dritte Farbe im Farbverlauf ausgeblendet und dann wieder transparent.</span><span class="sxs-lookup"><span data-stu-id="2c919-112">As a result, the third color in the gradient fades away and then becomes opaque again.</span></span>  
  
 [!code-csharp[BrushesIntroduction_snip#GraphicsMMGradientAnimationExamplesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BrushesIntroduction_snip/CSharp/GradientStopAnimationExample.cs#graphicsmmgradientanimationexampleswholepage)]
 [!code-vb[BrushesIntroduction_snip#GraphicsMMGradientAnimationExamplesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BrushesIntroduction_snip/visualbasic/gradientstopanimationexample.vb#graphicsmmgradientanimationexampleswholepage)]
 [!code-xaml[BrushesIntroduction_snip#GraphicsMMGradientAnimationExamplesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/BrushesIntroduction_snip/XAML/GradientStopAnimationExample.xaml#graphicsmmgradientanimationexampleswholepage)]  
  
 <span data-ttu-id="2c919-113">Obwohl in diesem Beispiel ein verwendet <xref:System.Windows.Media.LinearGradientBrush> wird, ist der Prozess für das Animieren von <xref:System.Windows.Media.GradientStop> Objekten in einer identisch <xref:System.Windows.Media.RadialGradientBrush> .</span><span class="sxs-lookup"><span data-stu-id="2c919-113">Although this example uses a <xref:System.Windows.Media.LinearGradientBrush>, the process is the same for animating <xref:System.Windows.Media.GradientStop> objects inside a <xref:System.Windows.Media.RadialGradientBrush>.</span></span>  
  
 <span data-ttu-id="2c919-114">Weitere Beispiele finden Sie im [Beispiel Pinsel](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes).</span><span class="sxs-lookup"><span data-stu-id="2c919-114">For additional examples, see the [Brushes Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Brushes).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2c919-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2c919-115">See also</span></span>

- <xref:System.Windows.Media.GradientStop>
- [<span data-ttu-id="2c919-116">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="2c919-116">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="2c919-117">Übersicht über Storyboards</span><span class="sxs-lookup"><span data-stu-id="2c919-117">Storyboards Overview</span></span>](storyboards-overview.md)
