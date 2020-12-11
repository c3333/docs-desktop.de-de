---
title: 'Gewusst wie: Animieren der Breite eines Rahmens mithilfe von Keyframes'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], border thickness with key frames
- key frames [WPF], animating border thickness with
- border thickness [WPF], animating with key frames
ms.assetid: 3a9cb463-0a63-407d-aae7-3fbb1a559947
ms.openlocfilehash: 884b62e88c347449ae39caa9c028d09db39b9f4b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975326"
---
# <a name="how-to-animate-the-thickness-of-a-border-by-using-key-frames"></a><span data-ttu-id="bb11f-102">Gewusst wie: Animieren der Breite eines Rahmens mithilfe von Keyframes</span><span class="sxs-lookup"><span data-stu-id="bb11f-102">How to: Animate the Thickness of a Border by Using Key Frames</span></span>
<span data-ttu-id="bb11f-103">Dieses Beispiel zeigt, wie Sie die- <xref:System.Windows.Controls.Control.BorderThickness%2A> Eigenschaft eines animieren <xref:System.Windows.Controls.Border> .</span><span class="sxs-lookup"><span data-stu-id="bb11f-103">This example shows how to animate the <xref:System.Windows.Controls.Control.BorderThickness%2A> property of a <xref:System.Windows.Controls.Border>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bb11f-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bb11f-104">Example</span></span>  
 <span data-ttu-id="bb11f-105">Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.ThicknessAnimationUsingKeyFrames> Klasse verwendet, um die- <xref:System.Windows.Controls.Control.BorderThickness%2A> Eigenschaft eines zu animieren <xref:System.Windows.Controls.Border> .</span><span class="sxs-lookup"><span data-stu-id="bb11f-105">The following example uses the <xref:System.Windows.Media.Animation.ThicknessAnimationUsingKeyFrames> class to animate the <xref:System.Windows.Controls.Control.BorderThickness%2A> property of a <xref:System.Windows.Controls.Border>.</span></span> <span data-ttu-id="bb11f-106">In dieser Animation werden drei Keyframes folgendermaßen verwendet:</span><span class="sxs-lookup"><span data-stu-id="bb11f-106">This animation uses three key frames in the following manner:</span></span>  
  
1. <span data-ttu-id="bb11f-107">In der ersten halben Sekunde wird von eine Instanz der- <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> Klasse verwendet, um die Stärke des Rahmens allmählich zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="bb11f-107">During the first half second, uses an instance of the <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> class to gradually increase the thickness of the border.</span></span> <span data-ttu-id="bb11f-108">Im Beispiel wird verwendet <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> , um eine glatte lineare Zunahme zwischen Werten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="bb11f-108">The example uses <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame> to create a smooth linear increase between values.</span></span>  
  
2. <span data-ttu-id="bb11f-109">Am Ende der nächsten halben Sekunde wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> um die Stärke des Rahmens plötzlich zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="bb11f-109">At the end of the next half second, uses an instance of the <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> class to suddenly increase the thickness of the border.</span></span> <span data-ttu-id="bb11f-110">Diskrete Keyframes wie diejenigen, die von abgeleitet <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> werden, erzeugen plötzliche Sprünge zwischen Werten, d. h., die Animation der Animation ist ruckartig.</span><span class="sxs-lookup"><span data-stu-id="bb11f-110">Discrete key frames like those derived from <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame> create sudden jumps between values, that is, the movement of the animation is jerky.</span></span>  
  
3. <span data-ttu-id="bb11f-111">In den letzten zwei Sekunden wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> um die Stärke des Rahmens zu verringern.</span><span class="sxs-lookup"><span data-stu-id="bb11f-111">During the final two seconds, uses an instance of the <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> class to decrease the thickness of the border.</span></span> <span data-ttu-id="bb11f-112">Spline-Keyframes wie die, die von abgeleitet werden <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> , erstellen einen variablen Übergang zwischen Werten gemäß den Werten der- <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame.KeySpline%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="bb11f-112">Spline key frames like those derived from <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame> create a variable transition between values according to the values of the <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="bb11f-113">In diesem Keyframe ist die Animation zunächst langsam und beschleunigt dann exponentiell im letzten Bereich des Zeitabschnitts.</span><span class="sxs-lookup"><span data-stu-id="bb11f-113">In this key frame, the animation starts off slow and speeds up exponentially toward the end of the time segment.</span></span>  
  
 [!code-xaml[keyframes_snip#ThicknessAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ThicknessAnimationUsingKeyFramesExample.xaml#thicknessanimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="bb11f-114">Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span><span class="sxs-lookup"><span data-stu-id="bb11f-114">For the complete sample, see [KeyFrame Animation Sample](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bb11f-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb11f-115">See also</span></span>

- <xref:System.Windows.Media.Animation.LinearThicknessKeyFrame>
- <xref:System.Windows.Media.Animation.DiscreteThicknessKeyFrame>
- <xref:System.Windows.Media.Animation.SplineThicknessKeyFrame>
- [<span data-ttu-id="bb11f-116">Übersicht über Keyframe-Animationen</span><span class="sxs-lookup"><span data-stu-id="bb11f-116">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="bb11f-117">Themen zur Vorgehensweise mit Keyframes</span><span class="sxs-lookup"><span data-stu-id="bb11f-117">Key-Frame How-to Topics</span></span>](key-frame-animation-how-to-topics.md)
- [<span data-ttu-id="bb11f-118">Animieren eines BorderThickness-Werts</span><span class="sxs-lookup"><span data-stu-id="bb11f-118">Animate a BorderThickness Value</span></span>](../controls/how-to-animate-a-borderthickness-value.md)
