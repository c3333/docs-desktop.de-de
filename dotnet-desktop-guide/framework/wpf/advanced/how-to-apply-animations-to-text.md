---
title: 'Gewusst wie: Anwenden von Animationen auf Text'
ms.date: 03/30/2017
helpviewer_keywords:
- typography [WPF], animations
- animation [WPF], text
ms.assetid: eec3d26c-0a21-420f-8012-671621c47089
ms.openlocfilehash: ed2f3beb904f724ac93e2c4033aa6b2eb3fa1290
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976387"
---
# <a name="how-to-apply-animations-to-text"></a><span data-ttu-id="bb349-102">Gewusst wie: Anwenden von Animationen auf Text</span><span class="sxs-lookup"><span data-stu-id="bb349-102">How to: Apply Animations to Text</span></span>
<span data-ttu-id="bb349-103">Animationen können die Anzeige und die Darstellung von Text in Ihrer Anwendung ändern.</span><span class="sxs-lookup"><span data-stu-id="bb349-103">Animations can alter the display and appearance of text in your application.</span></span> <span data-ttu-id="bb349-104">In den folgenden Beispielen werden verschiedene Animations Typen verwendet, um die Anzeige von Text in einem-Steuerelement zu beeinflussen <xref:System.Windows.Controls.TextBlock> .</span><span class="sxs-lookup"><span data-stu-id="bb349-104">The following examples use different types of animations to affect the display of text in a <xref:System.Windows.Controls.TextBlock> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bb349-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bb349-105">Example</span></span>  
 <span data-ttu-id="bb349-106">Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.Animation.DoubleAnimation> , um die Breite des Textblocks zu animieren.</span><span class="sxs-lookup"><span data-stu-id="bb349-106">The following example uses a <xref:System.Windows.Media.Animation.DoubleAnimation> to animate the width of the text block.</span></span> <span data-ttu-id="bb349-107">Der Breitenwert ändert sich innerhalb von 10 Sekunden von der Breite des Textblocks auf 0. Anschließend werden die Breitenwerte umgekehrt und es wird fortgefahren.</span><span class="sxs-lookup"><span data-stu-id="bb349-107">The width value changes from the width of the text block to 0 over a duration of 10 seconds, and then reverses the width values and continues.</span></span> <span data-ttu-id="bb349-108">Dieser Animationstyp erstellt einen Wipe-Effekt.</span><span class="sxs-lookup"><span data-stu-id="bb349-108">This type of animation creates a wipe effect.</span></span>  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample1](~/samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample1)]  
  
 <span data-ttu-id="bb349-109">Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.Animation.DoubleAnimation> , um die Deckkraft des Textblocks zu animieren.</span><span class="sxs-lookup"><span data-stu-id="bb349-109">The following example uses a <xref:System.Windows.Media.Animation.DoubleAnimation> to animate the opacity of the text block.</span></span> <span data-ttu-id="bb349-110">Der Deckkraftwert wird über einen Zeitraum von 5 Sekunden von 1,0 auf 0 geändert. Anschließend werden die Deckkraftwerte umgekehrt und es wird fortgefahren.</span><span class="sxs-lookup"><span data-stu-id="bb349-110">The opacity value changes from 1.0 to 0 over a duration of 5 seconds, and then reverses the opacity values and continues.</span></span>  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample2)]  
  
 <span data-ttu-id="bb349-111">Im folgenden Diagramm wird dargestellt, wie sich das- <xref:System.Windows.Controls.TextBlock> Steuerelement `1.00` `0.00` im Rahmen des 5-Sekunden-Intervalls, das von definiert wird, durch die Deckkraft ändern <xref:System.Windows.Media.Animation.Timeline.Duration%2A> .</span><span class="sxs-lookup"><span data-stu-id="bb349-111">The following diagram shows the effect of the <xref:System.Windows.Controls.TextBlock> control changing its opacity from `1.00` to `0.00` during the 5-second interval defined by the <xref:System.Windows.Media.Animation.Timeline.Duration%2A>.</span></span>  
  
 ![Text, der die Deckkraft von 1,00 auf 0,00 ändert.](./media/how-to-apply-animations-to-text/faded-text-opacity-change.png)  

 <span data-ttu-id="bb349-113">Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.Animation.ColorAnimation> , um die Vordergrundfarbe des Textblocks zu animieren.</span><span class="sxs-lookup"><span data-stu-id="bb349-113">The following example uses a <xref:System.Windows.Media.Animation.ColorAnimation> to animate the foreground color of the text block.</span></span> <span data-ttu-id="bb349-114">Der Wert für die Vordergrundfarbe ändert sich im Verlauf von 5 Sekunden von einer Farbe in eine zweite Farbe. Anschließend werden die Farbwerte umgekehrt und es wird fortgefahren.</span><span class="sxs-lookup"><span data-stu-id="bb349-114">The foreground color value changes from one color to a second color over a duration of 5 seconds, and then reverses the color values and continues.</span></span>  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample3](~/samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample3)]  
  
 <span data-ttu-id="bb349-115">Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.Animation.DoubleAnimation> , um den TextBlock zu drehen.</span><span class="sxs-lookup"><span data-stu-id="bb349-115">The following example uses a <xref:System.Windows.Media.Animation.DoubleAnimation> to rotate the text block.</span></span> <span data-ttu-id="bb349-116">Der Textblock führt eine vollständige Drehung über einen Zeitraum von 20 Sekunden aus, und anschließend wird die Drehung wiederholt.</span><span class="sxs-lookup"><span data-stu-id="bb349-116">The text block performs a full rotation over a duration of 20 seconds, and then continues to repeat the rotation.</span></span>  
  
 [!code-xaml[TextAnimationSample#TextAnimationSample4](~/samples/snippets/csharp/VS_Snippets_Wpf/TextAnimationSample/CS/Window1.xaml#textanimationsample4)]  
  
## <a name="see-also"></a><span data-ttu-id="bb349-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb349-117">See also</span></span>

- [<span data-ttu-id="bb349-118">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="bb349-118">Animation Overview</span></span>](../graphics-multimedia/animation-overview.md)
