---
title: 'Gewusst wie: Zeitliche Steuerung einer Keyframe-Animation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- key frames [WPF], timing
- timing key-frame animation
ms.assetid: b059216f-7d4b-4ca8-a019-bc287ee7bf16
ms.openlocfilehash: 8cfd2be0bbc526ed92a5fb1b558a5a41dc9c3113
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977631"
---
# <a name="how-to-control-key-frame-animation-timing"></a><span data-ttu-id="24b43-102">Gewusst wie: Zeitliche Steuerung einer Keyframe-Animation</span><span class="sxs-lookup"><span data-stu-id="24b43-102">How to: Control Key-Frame Animation Timing</span></span>

<span data-ttu-id="24b43-103">In diesem Beispiel wird gezeigt, wie die zeitliche Steuerung von Keyframes innerhalb einer Keyframe-Animation gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="24b43-103">This example shows how to control the timing of key frames within a key-frame animation.</span></span> <span data-ttu-id="24b43-104">Wie andere Animationen verfügen Keyframe-Animationen über eine- <xref:System.Windows.Media.Animation.Timeline.Duration%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="24b43-104">Like other animations, key-frame animations have a <xref:System.Windows.Media.Animation.Timeline.Duration%2A> property.</span></span> <span data-ttu-id="24b43-105">Zusätzlich zur Angabe der Dauer einer Animation müssen Sie angeben, welcher Teil dieser Dauer den einzelnen Keyframes zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="24b43-105">In addition to specifying the duration of an animation, you need to specify what part of that duration is allotted to each of its key frames.</span></span> <span data-ttu-id="24b43-106">Um die Zeit festzulegen, geben Sie <xref:System.Windows.Media.Animation.KeyTime> für jeden Keyframe in der Animation ein an.</span><span class="sxs-lookup"><span data-stu-id="24b43-106">To allot the time, you specify a <xref:System.Windows.Media.Animation.KeyTime> for each key frame in the animation.</span></span>

<span data-ttu-id="24b43-107">Der <xref:System.Windows.Media.Animation.KeyTime> for each-Keyframe gibt an, wann ein Keyframe endet (er gibt nicht an, wie lange ein Keyframe wiedergegeben wird).</span><span class="sxs-lookup"><span data-stu-id="24b43-107">The <xref:System.Windows.Media.Animation.KeyTime> for each key frame specifies when a key frame ends (it does not specify the length of time a key frame plays).</span></span> <span data-ttu-id="24b43-108">Sie können als <xref:System.Windows.Media.Animation.KeyTime> <xref:System.TimeSpan> Wert, als Prozentsatz oder als <xref:System.Windows.Media.Animation.KeyTime.Uniform%2A> <xref:System.Windows.Media.Animation.KeyTime.Paced%2A> besonderen Wert angeben.</span><span class="sxs-lookup"><span data-stu-id="24b43-108">You can specify a <xref:System.Windows.Media.Animation.KeyTime> as a <xref:System.TimeSpan> value, as a percentage, or as the <xref:System.Windows.Media.Animation.KeyTime.Uniform%2A> or <xref:System.Windows.Media.Animation.KeyTime.Paced%2A> special value.</span></span>

## <a name="example"></a><span data-ttu-id="24b43-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="24b43-109">Example</span></span>

<span data-ttu-id="24b43-110">Im folgenden Beispiel wird verwendet <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> , um ein Rechteck auf dem Bildschirm zu animieren.</span><span class="sxs-lookup"><span data-stu-id="24b43-110">The following example uses a <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> to animate a rectangle across the screen.</span></span> <span data-ttu-id="24b43-111">Die Schlüssel Zeiten der Keyframes werden mit Werten festgelegt <xref:System.TimeSpan> .</span><span class="sxs-lookup"><span data-stu-id="24b43-111">The key frames' key times are set with <xref:System.TimeSpan> values.</span></span>

[!code-csharp[keyframes_snip#KeyTimesTimeSpanExample](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/KeyTimesExample.cs#keytimestimespanexample)]
[!code-vb[keyframes_snip#KeyTimesTimeSpanExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/keytimesexample.vb#keytimestimespanexample)]
[!code-xaml[keyframes_snip#KeyTimesTimeSpanExample](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/KeyTimesExample.xaml#keytimestimespanexample)]

<span data-ttu-id="24b43-112">In der folgenden Abbildung wird gezeigt, wann der Wert jedes Keyframes erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="24b43-112">The following illustration shows when the value of each key frame is reached.</span></span>

<span data-ttu-id="24b43-113">![Schlüsselwerte werden nach 3, 4 und 10 Sekunden erreicht](./media/graphicsmm-keyframe-keytime1-timespan.png "graphicsmm_keyframe_keytime1_timespan")</span><span class="sxs-lookup"><span data-stu-id="24b43-113">![Key values are reached at 3, 4, and 10 seconds](./media/graphicsmm-keyframe-keytime1-timespan.png "graphicsmm_keyframe_keytime1_timespan")</span></span>

<span data-ttu-id="24b43-114">Das nächste Beispiel zeigt eine identische Animation, mit der Ausnahme, dass die Schlüssel Zeiten der Keyframes mit Prozentwerten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="24b43-114">The next example shows an animation that is identical, except that the key frames' key times are set with percentage values.</span></span>

[!code-csharp[keyframes_snip#KeyTimesPercentageExample](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/KeyTimesExample.cs#keytimespercentageexample)]
[!code-vb[keyframes_snip#KeyTimesPercentageExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/keytimesexample.vb#keytimespercentageexample)]
[!code-xaml[keyframes_snip#KeyTimesPercentageExample](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/KeyTimesExample.xaml#keytimespercentageexample)]

<span data-ttu-id="24b43-115">In der folgenden Abbildung wird gezeigt, wann der Wert jedes Keyframes erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="24b43-115">The following illustration shows when the value of each key frame is reached.</span></span>

<span data-ttu-id="24b43-116">![Schlüsselwerte werden nach 3, 4 und 10 Sekunden erreicht](./media/graphicsmm-keyframe-keytime2-percentage.png "graphicsmm_keyframe_keytime2_percentage")</span><span class="sxs-lookup"><span data-stu-id="24b43-116">![Key values are reached at 3, 4, and 10 seconds](./media/graphicsmm-keyframe-keytime2-percentage.png "graphicsmm_keyframe_keytime2_percentage")</span></span>

<span data-ttu-id="24b43-117">Im nächsten Beispiel werden <xref:System.Windows.Media.Animation.KeyTime.Uniform%2A> Schlüssel Zeitwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="24b43-117">The next example uses <xref:System.Windows.Media.Animation.KeyTime.Uniform%2A> key time values.</span></span>

[!code-csharp[keyframes_snip#KeyTimesUniformExample](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/KeyTimesExample.cs#keytimesuniformexample)]
[!code-vb[keyframes_snip#KeyTimesUniformExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/keytimesexample.vb#keytimesuniformexample)]
[!code-xaml[keyframes_snip#KeyTimesUniformExample](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/KeyTimesExample.xaml#keytimesuniformexample)]

<span data-ttu-id="24b43-118">In der folgenden Abbildung wird gezeigt, wann der Wert jedes Keyframes erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="24b43-118">The following illustration shows when the value of each key frame is reached.</span></span>

<span data-ttu-id="24b43-119">![Schlüsselwerte werden nach 3,3, 6,6 und 9,9 Sekunden erreicht](./media/graphicsmm-keyframe-keytime3-uniform.png "graphicsmm_keyframe_keytime3_uniform")</span><span class="sxs-lookup"><span data-stu-id="24b43-119">![Key values are reached at 3.3,6.6, and 9.9 seconds](./media/graphicsmm-keyframe-keytime3-uniform.png "graphicsmm_keyframe_keytime3_uniform")</span></span>

<span data-ttu-id="24b43-120">Im letzten Beispiel werden <xref:System.Windows.Media.Animation.KeyTime.Paced%2A> Schlüssel Zeitwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="24b43-120">The final example uses <xref:System.Windows.Media.Animation.KeyTime.Paced%2A> key time values.</span></span>

[!code-csharp[keyframes_snip#KeyTimesPacedExample](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/KeyTimesExample.cs#keytimespacedexample)]
[!code-vb[keyframes_snip#KeyTimesPacedExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/keytimesexample.vb#keytimespacedexample)]
[!code-xaml[keyframes_snip#KeyTimesPacedExample](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/KeyTimesExample.xaml#keytimespacedexample)]

<span data-ttu-id="24b43-121">In der folgenden Abbildung wird gezeigt, wann der Wert jedes Keyframes erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="24b43-121">The following illustration shows when the value of each key frame is reached.</span></span>

<span data-ttu-id="24b43-122">![Schlüsselwerte werden nach 0, 5 und 10 Sekunden erreicht](./media/graphicsmm-keyframe-keytime4-paced.png "graphicsmm_keyframe_keytime4_paced")</span><span class="sxs-lookup"><span data-stu-id="24b43-122">![Key values are reached at 0, 5, and 10 seconds](./media/graphicsmm-keyframe-keytime4-paced.png "graphicsmm_keyframe_keytime4_paced")</span></span>

<span data-ttu-id="24b43-123">Der Einfachheit halber werden in den Code Versionen dieses Beispiels lokale Animationen verwendet, nicht Storyboards, da nur eine einzelne Animation auf eine einzelne Eigenschaft angewendet wird, die Beispiele jedoch möglicherweise so geändert werden, dass Storyboards verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="24b43-123">For simplicity, the code versions of this example use local animations, not storyboards, because only a single animation is being applied to a single property, but the examples may be modified to use storyboards instead.</span></span> <span data-ttu-id="24b43-124">Ein Beispiel für das Deklarieren eines Storyboards im Code finden Sie unter [Animieren einer Eigenschaft mithilfe eines Storyboards](how-to-animate-a-property-by-using-a-storyboard.md).</span><span class="sxs-lookup"><span data-stu-id="24b43-124">For an example showing how to declare a storyboard in code, see [Animate a Property by Using a Storyboard](how-to-animate-a-property-by-using-a-storyboard.md).</span></span>

<span data-ttu-id="24b43-125">Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span><span class="sxs-lookup"><span data-stu-id="24b43-125">For the complete sample, see [KeyFrame Animation Sample](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span></span> <span data-ttu-id="24b43-126">Weitere Informationen zu Keyframe-Animationen finden Sie unter [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md).</span><span class="sxs-lookup"><span data-stu-id="24b43-126">For more information about key frame animations, see the [Key-Frame Animations Overview](key-frame-animations-overview.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="24b43-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24b43-127">See also</span></span>

- [<span data-ttu-id="24b43-128">Übersicht über Keyframe-Animationen</span><span class="sxs-lookup"><span data-stu-id="24b43-128">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="24b43-129">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="24b43-129">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="24b43-130">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="24b43-130">How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
