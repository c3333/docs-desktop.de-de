---
title: 'Gewusst wie: Animieren einer Zeichenfolge mithilfe von Keyframes'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], strings with key frames
- strings [WPF], animating with key frames
- key frames [WPF], animating strings with
ms.assetid: c62bc9fd-c09a-4227-bce0-0a1ab82049dd
ms.openlocfilehash: c954806ca901bbfc3ab6d4bbcc237cd0e404f154
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977021"
---
# <a name="how-to-animate-a-string-by-using-key-frames"></a><span data-ttu-id="66692-102">Gewusst wie: Animieren einer Zeichenfolge mithilfe von Keyframes</span><span class="sxs-lookup"><span data-stu-id="66692-102">How to: Animate a String by Using Key Frames</span></span>
<span data-ttu-id="66692-103">Dieses Beispiel zeigt, wie eine Zeichenfolge, die in diesem Beispiel die- <xref:System.Windows.Controls.ContentControl.Content%2A> Eigenschaft eines- <xref:System.Windows.Controls.Button> Steuer Elements ist, mithilfe von Keyframes animiert wird.</span><span class="sxs-lookup"><span data-stu-id="66692-103">This example shows how to animate a string, which in this example is the <xref:System.Windows.Controls.ContentControl.Content%2A> property of a <xref:System.Windows.Controls.Button> control, by using key frames.</span></span>  
  
## <a name="example"></a><span data-ttu-id="66692-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="66692-104">Example</span></span>  
 <span data-ttu-id="66692-105">Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.StringAnimationUsingKeyFrames> Klasse verwendet, um die- <xref:System.Windows.Controls.ContentControl.Content%2A> Eigenschaft eines zu animieren <xref:System.Windows.Controls.Button> .</span><span class="sxs-lookup"><span data-stu-id="66692-105">The following example uses the <xref:System.Windows.Media.Animation.StringAnimationUsingKeyFrames> class to animate the <xref:System.Windows.Controls.ContentControl.Content%2A> property of a <xref:System.Windows.Controls.Button>.</span></span>  
  
 <span data-ttu-id="66692-106">Alle Keyframes in diesem Beispiel verwenden eine Instanz der- <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> Klasse, da eine Zeichen folgen Animation, die mit Keyframes erstellt wird, nur diskrete Keyframes verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="66692-106">All the key frames in this example use an instance of the <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> class because a string animation that is created with key frames can only use discrete key frames.</span></span> <span data-ttu-id="66692-107">Diskrete Keyframes wie z. b. <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> plötzliche Sprünge zwischen Werten, d. h. Änderungen an der Animation werden schnell ausgeführt und sind nicht fein.</span><span class="sxs-lookup"><span data-stu-id="66692-107">Discrete key frames like <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame> create sudden jumps between values, that is, changes to the animation occur quickly and are not subtle.</span></span>  
  
 [!code-xaml[keyframes_snip#StringAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/StringAnimationUsingKeyFramesExample.xaml#stringanimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="66692-108">Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span><span class="sxs-lookup"><span data-stu-id="66692-108">For the complete sample, see [KeyFrame Animation Sample](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="66692-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66692-109">See also</span></span>

- <xref:System.Windows.Media.Animation.StringAnimationUsingKeyFrames>
- <xref:System.Windows.Controls.ContentControl.Content%2A>
- <xref:System.Windows.Controls.Button>
- <xref:System.Windows.Media.Animation.DiscreteStringKeyFrame>
- [<span data-ttu-id="66692-110">Übersicht über Keyframe-Animationen</span><span class="sxs-lookup"><span data-stu-id="66692-110">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="66692-111">Themen zur Vorgehensweise mit Keyframes</span><span class="sxs-lookup"><span data-stu-id="66692-111">Key-Frame How-to Topics</span></span>](key-frame-animation-how-to-topics.md)
