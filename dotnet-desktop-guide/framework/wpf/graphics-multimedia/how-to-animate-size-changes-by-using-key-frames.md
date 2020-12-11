---
title: 'Gewusst wie: Animieren von Größenänderungen mithilfe von Keyframes'
ms.date: 03/30/2017
helpviewer_keywords:
- key frames [WPF], animating size changes with
- animation [WPF], size changes with key frames
- size changes [WPF], animating with key frames
ms.assetid: 86bd2950-d4c9-4ec4-aa8d-7dc3ccadded4
ms.openlocfilehash: 42cecfc9df4304be4033ea39edc0517016de4a92
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975413"
---
# <a name="how-to-animate-size-changes-by-using-key-frames"></a><span data-ttu-id="3abd0-102">Gewusst wie: Animieren von Größenänderungen mithilfe von Keyframes</span><span class="sxs-lookup"><span data-stu-id="3abd0-102">How to: Animate Size Changes by Using Key Frames</span></span>
<span data-ttu-id="3abd0-103">In diesem Beispiel wird das Animieren von Größenänderungen mithilfe von Keyframes veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="3abd0-103">This example shows how to animate size changes by using key frames.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3abd0-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3abd0-104">Example</span></span>  
 <span data-ttu-id="3abd0-105">Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.SizeAnimationUsingKeyFrames> Klasse verwendet, um die- <xref:System.Windows.Media.ArcSegment.Size%2A> Eigenschaft eines zu animieren <xref:System.Windows.Media.ArcSegment> .</span><span class="sxs-lookup"><span data-stu-id="3abd0-105">The following example uses the <xref:System.Windows.Media.Animation.SizeAnimationUsingKeyFrames> class to animate the <xref:System.Windows.Media.ArcSegment.Size%2A> property of an <xref:System.Windows.Media.ArcSegment>.</span></span> <span data-ttu-id="3abd0-106">In dieser Animation werden drei Keyframes folgendermaßen verwendet:</span><span class="sxs-lookup"><span data-stu-id="3abd0-106">This animation uses three key frames in the following manner:</span></span>  
  
1. <span data-ttu-id="3abd0-107">In der ersten halben Sekunde der Animation wird von eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.LinearSizeKeyFrame> um die Größe des Bogens allmählich zu vergrößern. Lineare Keyframes, wie z <xref:System.Windows.Media.Animation.LinearSizeKeyFrame> . b. eine glatte lineare Umstellung zwischen Werten.</span><span class="sxs-lookup"><span data-stu-id="3abd0-107">During the first half second of the animation, uses an instance of the <xref:System.Windows.Media.Animation.LinearSizeKeyFrame> class to gradually increase the size of the arc. Linear key frames like <xref:System.Windows.Media.Animation.LinearSizeKeyFrame> create a smooth linear transition between values.</span></span>  
  
2. <span data-ttu-id="3abd0-108">Am Ende der nächsten halben Sekunde wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.DiscreteSizeKeyFrame> um die Größe des Bogens plötzlich zu vergrößern. Diskrete Keyframes wie z. b. <xref:System.Windows.Media.Animation.DiscreteSizeKeyFrame> die Erstellung plötzlicher Sprünge zwischen Werten, d. h. die Größenänderungen treten plötzlich auf und sind nicht fein.</span><span class="sxs-lookup"><span data-stu-id="3abd0-108">At the end of the next half second, uses an instance of the <xref:System.Windows.Media.Animation.DiscreteSizeKeyFrame> class to suddenly increase the size of the arc. Discrete key frames like <xref:System.Windows.Media.Animation.DiscreteSizeKeyFrame> create sudden jumps between values, that is, the size changes occur suddenly and are not subtle.</span></span>  
  
3. <span data-ttu-id="3abd0-109">In den letzten zwei Sekunden wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.SplineSizeKeyFrame> um die Größe des Bogens zu vergrößern. Spline-Keyframes wie <xref:System.Windows.Media.Animation.SplineSizeKeyFrame> das Erstellen eines Variablen Übergangs zwischen Werten gemäß den Werten der- <xref:System.Windows.Media.Animation.SplineSizeKeyFrame.KeySpline%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3abd0-109">Over the final two seconds, uses an instance of the <xref:System.Windows.Media.Animation.SplineSizeKeyFrame> class to increase the size of the arc. Spline key frames like <xref:System.Windows.Media.Animation.SplineSizeKeyFrame> create a variable transition between values according to the values of the <xref:System.Windows.Media.Animation.SplineSizeKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="3abd0-110">In diesem Beispiel wächst die Größe des Bogens zunächst nur langsam und steigt dann exponentiell zum Ende des Zeitabschnitts.</span><span class="sxs-lookup"><span data-stu-id="3abd0-110">In this example, the size of the arc increases slowly at first and then increases exponentially toward the end of the time segment.</span></span>  
  
 [!code-xaml[keyframes_snip#SizeAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/SizeAnimationUsingKeyFramesExample.xaml#sizeanimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="3abd0-111">Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span><span class="sxs-lookup"><span data-stu-id="3abd0-111">For the complete sample, see [KeyFrame Animation Sample](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3abd0-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3abd0-112">See also</span></span>

- <xref:System.Windows.Media.Animation.SizeAnimationUsingKeyFrames>
- <xref:System.Windows.Media.ArcSegment.Size%2A>
- <xref:System.Windows.Media.ArcSegment>
- <xref:System.Windows.Media.Animation.LinearSizeKeyFrame>
- <xref:System.Windows.Media.Animation.DiscreteSizeKeyFrame>
- <xref:System.Windows.Media.Animation.SplineSizeKeyFrame>
- [<span data-ttu-id="3abd0-113">Übersicht über Keyframe-Animationen</span><span class="sxs-lookup"><span data-stu-id="3abd0-113">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="3abd0-114">Themen zur Vorgehensweise mit Keyframes</span><span class="sxs-lookup"><span data-stu-id="3abd0-114">Key-Frame How-to Topics</span></span>](key-frame-animation-how-to-topics.md)
