---
title: 'Gewusst wie: Wiederholen einer Animation'
ms.date: 03/30/2017
helpviewer_keywords:
- RepeatBehavior property of timelines [WPF]
- repeating animating [WPF]
- Timelines RepeatBehavior property [WPF]
- animation [WPF], repeating
ms.assetid: e6f3b068-eeeb-47fd-8d40-8848c31f1e1e
ms.openlocfilehash: 1512c49a658c80f3ab6af652839c3562af3dd205
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978016"
---
# <a name="how-to-repeat-an-animation"></a><span data-ttu-id="ab7cf-102">Gewusst wie: Wiederholen einer Animation</span><span class="sxs-lookup"><span data-stu-id="ab7cf-102">How to: Repeat an Animation</span></span>
<span data-ttu-id="ab7cf-103">In diesem Beispiel wird gezeigt, wie die-Eigenschaft eines verwendet wird, um <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> <xref:System.Windows.Media.Animation.Timeline> das Wiederholungs Verhalten einer Animation zu steuern.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-103">This example shows how to use the <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> property of a <xref:System.Windows.Media.Animation.Timeline> in order to control the repeat behavior of an animation.</span></span>  
  
## <a name="example"></a><span data-ttu-id="ab7cf-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ab7cf-104">Example</span></span>  
 <span data-ttu-id="ab7cf-105">Die- <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> Eigenschaft eines <xref:System.Windows.Media.Animation.Timeline> steuert, wie oft eine Animation ihre einfache Dauer wiederholt.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-105">The <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> property of a <xref:System.Windows.Media.Animation.Timeline> controls how many times an animation repeats its simple duration.</span></span> <span data-ttu-id="ab7cf-106">Mithilfe von <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> können Sie angeben, dass eine <xref:System.Windows.Media.Animation.Timeline> für eine bestimmte Anzahl von vorkommen (eine Iterations Anzahl) oder für einen angegebenen Zeitraum wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-106">By using <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A>, you can specify that a <xref:System.Windows.Media.Animation.Timeline> repeats for a certain number of times (an iteration count) or for a specified time period.</span></span> <span data-ttu-id="ab7cf-107">In beiden Fällen durchläuft die Animation so viele End-to-End-Ausführungen, die Sie benötigen, um die angeforderte Anzahl oder Dauer auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-107">In either case, the animation goes through as many beginning-to-end runs that it needs in order to fill the requested count or duration.</span></span>  
  
 <span data-ttu-id="ab7cf-108">Standardmäßig haben Zeitachsen eine Wiederholungs Anzahl von 1,0. Dies bedeutet, dass Sie einmalig wiedergegeben werden und nicht wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-108">By default, timelines have a repeat count of 1.0, which means they play one time and do not repeat.</span></span> <span data-ttu-id="ab7cf-109">Wenn Sie jedoch die- <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> Eigenschaft eines auf festlegen <xref:System.Windows.Media.Animation.Timeline> <xref:System.Windows.Media.Animation.RepeatBehavior.Forever%2A> , wird die Zeitachse unbegrenzt wiederholt.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-109">However, if you set the <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> property of a <xref:System.Windows.Media.Animation.Timeline> to <xref:System.Windows.Media.Animation.RepeatBehavior.Forever%2A>, the timeline repeats indefinitely.</span></span>  
  
 <span data-ttu-id="ab7cf-110">Im folgenden Beispiel wird gezeigt, wie die-Eigenschaft verwendet wird <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> , um das Wiederholungs Verhalten einer Animation zu steuern.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-110">The following example shows how to use the <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> property to control the repeat behavior of an animation.</span></span> <span data-ttu-id="ab7cf-111">Im Beispiel wird die- <xref:System.Windows.FrameworkElement.Width%2A> Eigenschaft von fünf Rechtecke mit den einzelnen Rechtecks mit einem anderen Typ von Wiederholungs Verhalten animiert.</span><span class="sxs-lookup"><span data-stu-id="ab7cf-111">The example animates the <xref:System.Windows.FrameworkElement.Width%2A> property of five rectangles with each rectangle using a different type of repeat behavior.</span></span>  
  
 [!code-xaml[timingbehaviors_snip#RepeatBehaviorWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/RepeatBehaviorExample.xaml#repeatbehaviorwholepage)]  
  
 <span data-ttu-id="ab7cf-112">Das komplette Beispiel finden Sie unter [Beispiel für Animations Zeitverhalten](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/AnimationTiming).</span><span class="sxs-lookup"><span data-stu-id="ab7cf-112">For the complete sample, see [Animation Timing Behavior Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/AnimationTiming).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ab7cf-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab7cf-113">See also</span></span>

- [<span data-ttu-id="ab7cf-114">Sammeln von Animationen während Wiederholungszyklen</span><span class="sxs-lookup"><span data-stu-id="ab7cf-114">Accumulate Animation Values During Repeat Cycles</span></span>](how-to-accumulate-animation-values-during-repeat-cycles.md)
- [<span data-ttu-id="ab7cf-115">Festlegen, ob eine Zeitachse automatisch umgekehrt wird</span><span class="sxs-lookup"><span data-stu-id="ab7cf-115">Specify Whether a Timeline Automatically Reverses</span></span>](how-to-specify-whether-a-timeline-automatically-reverses.md)
- [<span data-ttu-id="ab7cf-116">Gewusst-wie-Themen zu Animation und Zeitsteuerung</span><span class="sxs-lookup"><span data-stu-id="ab7cf-116">Animation and Timing How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
- [<span data-ttu-id="ab7cf-117">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="ab7cf-117">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="ab7cf-118">Beispiel zum Verhalten der Animationszeitsteuerung</span><span class="sxs-lookup"><span data-stu-id="ab7cf-118">Animation Timing Behavior Sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/AnimationTiming)
