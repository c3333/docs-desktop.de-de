---
title: 'Gewusst wie: Festlegen der Dauer einer Animation'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], duration
- Timelines [WPF], description
- duration of animations [WPF]
ms.assetid: 155034ef-7d00-4416-a73c-b1713992d2eb
ms.openlocfilehash: bdae1689ffeb8c54d756b9debbd26d57a052892d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977939"
---
# <a name="how-to-set-a-duration-for-an-animation"></a><span data-ttu-id="4e2e4-102">Gewusst wie: Festlegen der Dauer einer Animation</span><span class="sxs-lookup"><span data-stu-id="4e2e4-102">How to: Set a Duration for an Animation</span></span>
<span data-ttu-id="4e2e4-103">Ein <xref:System.Windows.Media.Animation.Timeline> stellt einen Zeitabschnitt dar, und die Länge dieses Segments wird durch die der Zeitachse bestimmt <xref:System.Windows.Duration> .</span><span class="sxs-lookup"><span data-stu-id="4e2e4-103">A <xref:System.Windows.Media.Animation.Timeline> represents a segment of time and the length of that segment is determined by the timeline's <xref:System.Windows.Duration>.</span></span> <span data-ttu-id="4e2e4-104">Wenn ein <xref:System.Windows.Media.Animation.Timeline> das Ende seiner Dauer erreicht, wird die Wiedergabe beendet.</span><span class="sxs-lookup"><span data-stu-id="4e2e4-104">When a <xref:System.Windows.Media.Animation.Timeline> reaches the end of its duration, it stops playing.</span></span> <span data-ttu-id="4e2e4-105">Wenn das untergeordnete Zeit <xref:System.Windows.Media.Animation.Timeline> Achsen hat, wird die Wiedergabe ebenfalls beendet.</span><span class="sxs-lookup"><span data-stu-id="4e2e4-105">If the <xref:System.Windows.Media.Animation.Timeline> has child timelines, they stop playing as well.</span></span> <span data-ttu-id="4e2e4-106">Im Fall einer Animation gibt das an, <xref:System.Windows.Duration> wie lange die Animation für den Übergang vom Startwert zum Endwert benötigt.</span><span class="sxs-lookup"><span data-stu-id="4e2e4-106">In the case of an animation, the <xref:System.Windows.Duration> specifies how long the animation takes to transition from its starting value to its ending value.</span></span>  
  
 <span data-ttu-id="4e2e4-107">Sie können einen <xref:System.Windows.Duration> mit einer bestimmten, begrenzten Uhrzeit oder den speziellen Werten <xref:System.Windows.Duration.Automatic%2A> oder angeben <xref:System.Windows.Duration.Forever%2A> .</span><span class="sxs-lookup"><span data-stu-id="4e2e4-107">You can specify a <xref:System.Windows.Duration> with a specific, finite time or the special values <xref:System.Windows.Duration.Automatic%2A> or <xref:System.Windows.Duration.Forever%2A>.</span></span> <span data-ttu-id="4e2e4-108">Die Dauer einer Animation muss immer ein Uhrzeitwert sein, da eine Animation immer eine definierte, begrenzte Länge haben muss – andernfalls weiß die Animation nicht, wie Sie zwischen den Zielwerten wechseln kann.</span><span class="sxs-lookup"><span data-stu-id="4e2e4-108">An animation's duration must always be a time value, because an animation must always have a defined, finite length—otherwise, the animation would not know how to transition between its target values.</span></span> <span data-ttu-id="4e2e4-109">Containertimelines ( <xref:System.Windows.Media.Animation.TimelineGroup> -Objekte), wie z. b. <xref:System.Windows.Media.Animation.Storyboard> und <xref:System.Windows.Media.Animation.ParallelTimeline> , haben eine Standarddauer von. dies <xref:System.Windows.Duration.Automatic%2A> bedeutet, dass Sie automatisch enden, wenn das letzte untergeordnete Element beendet wird.</span><span class="sxs-lookup"><span data-stu-id="4e2e4-109">Container timelines (<xref:System.Windows.Media.Animation.TimelineGroup> objects), such as <xref:System.Windows.Media.Animation.Storyboard> and <xref:System.Windows.Media.Animation.ParallelTimeline>, have a default duration of <xref:System.Windows.Duration.Automatic%2A>, which means they automatically end when their last child stops playing.</span></span>  
  
 <span data-ttu-id="4e2e4-110">Im folgenden Beispiel wird die Breite, die Höhe und die Füllfarbe eines <xref:System.Windows.Shapes.Rectangle> animiert.</span><span class="sxs-lookup"><span data-stu-id="4e2e4-110">In the following example, the width, height and fill color of a <xref:System.Windows.Shapes.Rectangle> is animated.</span></span> <span data-ttu-id="4e2e4-111">Dauer werden für Animations-und Container Zeitachse festgelegt, was zu Animationseffekten führt, einschließlich der Steuerung der erkannten Geschwindigkeit einer Animation und Überschreiben der Dauer von untergeordneten Zeitachsen mit der Dauer einer Container Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="4e2e4-111">Durations are set on animation and container timelines resulting in animation effects including controlling the perceived speed of an animation and overriding the duration of child timelines with the duration of a container timeline.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4e2e4-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4e2e4-112">Example</span></span>  
 [!code-xaml[timingbehaviors_snip#DurationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/DurationExample.xaml#durationexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="4e2e4-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e2e4-113">See also</span></span>

- <xref:System.Windows.Duration>
- [<span data-ttu-id="4e2e4-114">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="4e2e4-114">Animation Overview</span></span>](animation-overview.md)
