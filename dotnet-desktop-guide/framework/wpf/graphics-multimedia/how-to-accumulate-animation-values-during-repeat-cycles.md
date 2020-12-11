---
title: 'Gewusst wie: Sammeln von Animationswerten während Wiederholungszyklen'
ms.date: 03/30/2017
helpviewer_keywords:
- accumulating animation values across repeating cycles [WPF]
- animation [WPF], accumulating values across repeating cycles
ms.assetid: 548df369-c7cc-4dab-b569-08b95ced2e7e
ms.openlocfilehash: bccdc9b7bf2d5a0ea476e39e8d54107854db7ae3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977677"
---
# <a name="how-to-accumulate-animation-values-during-repeat-cycles"></a><span data-ttu-id="41b79-102">Gewusst wie: Sammeln von Animationswerten während Wiederholungszyklen</span><span class="sxs-lookup"><span data-stu-id="41b79-102">How to: Accumulate Animation Values During Repeat Cycles</span></span>
<span data-ttu-id="41b79-103">In diesem Beispiel wird gezeigt, wie die-Eigenschaft verwendet wird <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> , um Animations Werte in wiederkehrenden Zyklen zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="41b79-103">This example shows how to use the <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> property to accumulate animation values across repeating cycles.</span></span>  
  
## <a name="example"></a><span data-ttu-id="41b79-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="41b79-104">Example</span></span>  
 <span data-ttu-id="41b79-105">Verwenden Sie die- <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> Eigenschaft, um Basiswerte einer Animation über sich wiederholende Zyklen hinweg zu sammeln.</span><span class="sxs-lookup"><span data-stu-id="41b79-105">Use the <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> property to accumulate base values of an animation across repeating cycles.</span></span> <span data-ttu-id="41b79-106">Wenn Sie z. b. eine Animation so festlegen, dass Sie 9-Mal wiederholt <xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> wird (= "9X"), und Sie die-Eigenschaft auf animieren zwischen 10 und 15 festlegen (von = 10 bis = 15), wird die-Eigenschaft während des ersten Durchlaufs zwischen 10 und 15 animiert.</span><span class="sxs-lookup"><span data-stu-id="41b79-106">For example, if you set an animation to repeat 9 times (<xref:System.Windows.Media.Animation.Timeline.RepeatBehavior%2A> = "9x") and you set the property to animate between 10 and 15 (From = 10 To = 15), the property animates from 10 to 15 during the first cycle, from 15 to 20 during the second cycle, from 20 to 25 during the third cycle, and so on.</span></span> <span data-ttu-id="41b79-107">Daher wird für jeden Animations Durchlauf der Wert "End Animation" aus dem vorherigen Animations Cycle als Basiswert verwendet.</span><span class="sxs-lookup"><span data-stu-id="41b79-107">Hence, each animation cycle uses the ending animation value from the previous animation cycle as its base value.</span></span>  
  
 <span data-ttu-id="41b79-108">Sie können die `IsCumulative` -Eigenschaft mit den meisten grundlegenden Animationen und den meisten Keyframe-Animationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="41b79-108">You can use the `IsCumulative` property with most basic animations and most key frame animations.</span></span> <span data-ttu-id="41b79-109">Weitere Informationen finden Sie unter Übersicht über [Animationen](animation-overview.md) und [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md).</span><span class="sxs-lookup"><span data-stu-id="41b79-109">For more information, see [Animation Overview](animation-overview.md) and [Key-Frame Animations Overview](key-frame-animations-overview.md).</span></span>  
  
 <span data-ttu-id="41b79-110">Das folgende Beispiel zeigt dieses Verhalten, indem Sie die Breite von vier Rechtecke animieren.</span><span class="sxs-lookup"><span data-stu-id="41b79-110">The following example shows this behavior by animating the width of four rectangles.</span></span> <span data-ttu-id="41b79-111">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="41b79-111">The example:</span></span>  
  
- <span data-ttu-id="41b79-112">Animiert das erste Rechteck mit <xref:System.Windows.Media.Animation.DoubleAnimation> und legt die- <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> Eigenschaft auf fest `true` .</span><span class="sxs-lookup"><span data-stu-id="41b79-112">Animates the first rectangle with <xref:System.Windows.Media.Animation.DoubleAnimation> and sets the <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> property to `true`.</span></span>  
  
- <span data-ttu-id="41b79-113">Animiert das zweite Rechteck mit <xref:System.Windows.Media.Animation.DoubleAnimation> und legt die- <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> Eigenschaft auf den Standardwert von fest `false` .</span><span class="sxs-lookup"><span data-stu-id="41b79-113">Animates the second rectangle with <xref:System.Windows.Media.Animation.DoubleAnimation> and sets the <xref:System.Windows.Media.Animation.DoubleAnimation.IsCumulative%2A> property to the default value of `false`.</span></span>  
  
- <span data-ttu-id="41b79-114">Animiert das dritte Rechteck mit <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> und legt die- <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsCumulative%2A> Eigenschaft auf fest `true` .</span><span class="sxs-lookup"><span data-stu-id="41b79-114">Animates the third rectangle with <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> and sets the <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsCumulative%2A> property to `true`.</span></span>  
  
- <span data-ttu-id="41b79-115">Animiert das letzte Rechteck mit <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> und legt die- <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsCumulative%2A> Eigenschaft auf fest `false` .</span><span class="sxs-lookup"><span data-stu-id="41b79-115">Animates the last rectangle with <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> and sets the <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsCumulative%2A> property to `false`.</span></span>  
  
 [!code-xaml[timingbehaviors_snip#IsCumulativeWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/IsCumulativeExample.xaml#iscumulativewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="41b79-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41b79-116">See also</span></span>

- [<span data-ttu-id="41b79-117">Hinzufügen eines Animationsausgabewerts zu einem Animationsstartwert</span><span class="sxs-lookup"><span data-stu-id="41b79-117">Add an Animation Output Value to an Animation Starting Value</span></span>](how-to-add-an-animation-output-value-to-an-animation-starting-value.md)
- [<span data-ttu-id="41b79-118">Wiederholen einer Animation</span><span class="sxs-lookup"><span data-stu-id="41b79-118">Repeat an Animation</span></span>](how-to-repeat-an-animation.md)
- [<span data-ttu-id="41b79-119">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="41b79-119">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="41b79-120">Übersicht über Keyframe-Animationen</span><span class="sxs-lookup"><span data-stu-id="41b79-120">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="41b79-121">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="41b79-121">How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
