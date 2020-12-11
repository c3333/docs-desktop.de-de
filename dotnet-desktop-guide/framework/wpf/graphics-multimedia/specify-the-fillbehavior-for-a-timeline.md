---
title: 'Gewusst wie: Festlegen von FillBehavior für ein Timeline-Objekt, das das Ende des aktiven Zeitraums erreicht hat'
ms.date: 03/30/2017
helpviewer_keywords:
- FillBehavior property for inactive timelines [WPF]
- Timelines [WPF], FillBehavior property
ms.assetid: db805f59-d513-4dac-af15-47005dae3199
ms.openlocfilehash: 1f54f2c1bb49bb7a0301f112a109194ab1a8658e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976844"
---
# <a name="how-to-specify-the-fillbehavior-for-a-timeline-that-has-reached-the-end-of-its-active-period"></a><span data-ttu-id="7dfc1-102">Gewusst wie: Festlegen von FillBehavior für ein Timeline-Objekt, das das Ende des aktiven Zeitraums erreicht hat</span><span class="sxs-lookup"><span data-stu-id="7dfc1-102">How to: Specify the FillBehavior for a Timeline that has Reached the End of Its Active Period</span></span>
<span data-ttu-id="7dfc1-103">In diesem Beispiel wird gezeigt, wie das- <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> Objekt für die inaktive einer <xref:System.Windows.Media.Animation.Timeline> animierten Eigenschaft angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7dfc1-103">This example shows how to specify the <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> for the inactive <xref:System.Windows.Media.Animation.Timeline> of an animated property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7dfc1-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7dfc1-104">Example</span></span>  
 <span data-ttu-id="7dfc1-105">Die- <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> Eigenschaft eines <xref:System.Windows.Media.Animation.Timeline> bestimmt, was mit dem Wert einer animierten Eigenschaft geschieht, wenn es nicht animiert wird, d. h., wenn das inaktiv ist, das übergeordnete Element jedoch <xref:System.Windows.Media.Animation.Timeline> <xref:System.Windows.Media.Animation.Timeline> innerhalb des aktiven oder des beibehaltenen Zeitraums liegt.</span><span class="sxs-lookup"><span data-stu-id="7dfc1-105">The <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> property of a <xref:System.Windows.Media.Animation.Timeline> determines what happens to the value of an animated property when it is not being animated, that is, when the <xref:System.Windows.Media.Animation.Timeline> is inactive but its parent <xref:System.Windows.Media.Animation.Timeline> is inside its active or hold period.</span></span> <span data-ttu-id="7dfc1-106">Wenn z. b. eine animierte Eigenschaft an Ihrem Endwert verbleibt, nachdem die Animation beendet wurde, oder wird Sie auf den Wert zurückgesetzt, den Sie vor dem Start der Animation hatte?</span><span class="sxs-lookup"><span data-stu-id="7dfc1-106">For example, does an animated property remain at its end value after the animation ends or does it revert back to the value it had before the animation started?</span></span>  
  
 <span data-ttu-id="7dfc1-107">Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.Animation.DoubleAnimation> , um die <xref:System.Windows.FrameworkElement.Width%2A> von zwei Rechtecke zu animieren.</span><span class="sxs-lookup"><span data-stu-id="7dfc1-107">The following example uses a <xref:System.Windows.Media.Animation.DoubleAnimation> to animate the <xref:System.Windows.FrameworkElement.Width%2A> of two rectangles.</span></span> <span data-ttu-id="7dfc1-108">Jedes Rechteck verwendet ein anderes- <xref:System.Windows.Media.Animation.Timeline> Objekt.</span><span class="sxs-lookup"><span data-stu-id="7dfc1-108">Each rectangle uses a different <xref:System.Windows.Media.Animation.Timeline> object.</span></span>  
  
 <span data-ttu-id="7dfc1-109">Eine <xref:System.Windows.Media.Animation.Timeline> verfügt über einen, der <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> auf festgelegt ist <xref:System.Windows.Media.Animation.FillBehavior.Stop> , was bewirkt, dass die Breite des Rechtecks auf seinen nicht animierten Wert zurückgesetzt wird, wenn <xref:System.Windows.Media.Animation.Timeline> beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7dfc1-109">One <xref:System.Windows.Media.Animation.Timeline> has a <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> that is set to <xref:System.Windows.Media.Animation.FillBehavior.Stop>, which causes the width of the rectangle to revert back to its non-animated value when the <xref:System.Windows.Media.Animation.Timeline> ends.</span></span> <span data-ttu-id="7dfc1-110">Der andere <xref:System.Windows.Media.Animation.Timeline> verfügt über <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> einen <xref:System.Windows.Media.Animation.FillBehavior.HoldEnd> von, der bewirkt, dass die Breite beim Ende des am Endwert verbleibt <xref:System.Windows.Media.Animation.Timeline> .</span><span class="sxs-lookup"><span data-stu-id="7dfc1-110">The other <xref:System.Windows.Media.Animation.Timeline> has a <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A> of <xref:System.Windows.Media.Animation.FillBehavior.HoldEnd>, which causes the width to remain at its end value when the <xref:System.Windows.Media.Animation.Timeline> ends.</span></span>  
  
 [!code-xaml[timingbehaviors_snip#FillBehaviorWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/FillBehaviorExample.xaml#fillbehaviorwholepage)]  
  
 <span data-ttu-id="7dfc1-111">Das komplette Beispiel finden Sie unter [Animation Example Gallery](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/AnimationExamples).</span><span class="sxs-lookup"><span data-stu-id="7dfc1-111">For the complete sample, see [Animation Example Gallery](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/AnimationExamples).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7dfc1-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7dfc1-112">See also</span></span>

- <xref:System.Windows.Media.Animation.DoubleAnimation>
- <xref:System.Windows.FrameworkElement.Width%2A>
- <xref:System.Windows.Media.Animation.Timeline>
- <xref:System.Windows.Media.Animation.Timeline.FillBehavior%2A>
- <xref:System.Windows.Media.Animation.FillBehavior.Stop>
- <xref:System.Windows.Media.Animation.FillBehavior.HoldEnd>
- [<span data-ttu-id="7dfc1-113">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="7dfc1-113">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="7dfc1-114">Gewusst-wie-Themen zu Animation und Zeitsteuerung</span><span class="sxs-lookup"><span data-stu-id="7dfc1-114">Animation and Timing How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
