---
title: 'Gewusst wie: Animieren eines Objekts mithilfe von Keyframes'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], objects with key frames
- key frames [WPF], animating objects with
ms.assetid: b1f15ba9-cac7-4cea-8699-5c6b55c05c5e
ms.openlocfilehash: 0bc33b189fd856dbe8106c1db35bc18e27ea131e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977274"
---
# <a name="how-to-animate-an-object-by-using-key-frames"></a><span data-ttu-id="22a0a-102">Gewusst wie: Animieren eines Objekts mithilfe von Keyframes</span><span class="sxs-lookup"><span data-stu-id="22a0a-102">How to: Animate an Object by Using Key Frames</span></span>
<span data-ttu-id="22a0a-103">In diesem Beispiel wird gezeigt, wie ein Objekt, das in diesem Beispiel die- <xref:System.Windows.Controls.Page.Background%2A> Eigenschaft eines-Steuer Elements ist <xref:System.Windows.Controls.Page> , mithilfe von Keyframes animiert wird.</span><span class="sxs-lookup"><span data-stu-id="22a0a-103">This example shows how to animate an object, which in this example is the <xref:System.Windows.Controls.Page.Background%2A> property of a <xref:System.Windows.Controls.Page> control, by using key frames.</span></span>  
  
## <a name="example"></a><span data-ttu-id="22a0a-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="22a0a-104">Example</span></span>  
 <span data-ttu-id="22a0a-105">Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames> Klasse verwendet, um Farbänderungen für die-Eigenschaft eines-Steuer Elements zu animieren <xref:System.Windows.Controls.Page.Background%2A> <xref:System.Windows.Controls.Page> .</span><span class="sxs-lookup"><span data-stu-id="22a0a-105">The following example uses the <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames> class to animate color changes for the <xref:System.Windows.Controls.Page.Background%2A> property of a <xref:System.Windows.Controls.Page> control.</span></span> <span data-ttu-id="22a0a-106">Die Beispiel Animation ändert sich in regelmäßigen Abständen in einen anderen Hintergrund Pinsel.</span><span class="sxs-lookup"><span data-stu-id="22a0a-106">The example animation changes to a different background brush at regular intervals.</span></span> <span data-ttu-id="22a0a-107">Diese Animation verwendet die- <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> Klasse, um drei verschiedene Keyframes zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="22a0a-107">This animation uses the <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> class to create three different key frames.</span></span> <span data-ttu-id="22a0a-108">Die Animation verwendet Keyframes wie folgt:</span><span class="sxs-lookup"><span data-stu-id="22a0a-108">The animation uses key frames in the following manner:</span></span>  
  
1. <span data-ttu-id="22a0a-109">Am Ende der ersten Sekunde animiert eine Instanz der- <xref:System.Windows.Media.LinearGradientBrush> Klasse.</span><span class="sxs-lookup"><span data-stu-id="22a0a-109">At the end of the first second, animates an instance of the <xref:System.Windows.Media.LinearGradientBrush> class.</span></span> <span data-ttu-id="22a0a-110">In diesem Abschnitt des Beispiels wird ein linearer Farbverlauf auf die Hintergrundfarbe angewendet, sodass die Farbe von Gelb in Orange in rot übergeht.</span><span class="sxs-lookup"><span data-stu-id="22a0a-110">This section of the example applies a linear gradient to the background color so that the color transitions from yellow to orange to red.</span></span>  
  
2. <span data-ttu-id="22a0a-111">Am Ende der nächsten Sekunde animiert eine Instanz der- <xref:System.Windows.Media.RadialGradientBrush> Klasse.</span><span class="sxs-lookup"><span data-stu-id="22a0a-111">At the end of the next second, animates an instance of the <xref:System.Windows.Media.RadialGradientBrush> class.</span></span> <span data-ttu-id="22a0a-112">In diesem Abschnitt des Beispiels wird ein Radialer Farbverlauf auf die Hintergrundfarbe angewendet, sodass die Farbe von weiß zu blau in schwarz übergeht.</span><span class="sxs-lookup"><span data-stu-id="22a0a-112">This section of the example applies a radial gradient to the background color so that the color transitions from white to blue to black.</span></span>  
  
3. <span data-ttu-id="22a0a-113">Am Ende der dritten Sekunde animiert eine Instanz der- <xref:System.Windows.Media.DrawingBrush> Klasse.</span><span class="sxs-lookup"><span data-stu-id="22a0a-113">At the end of the third second, animates an instance of the <xref:System.Windows.Media.DrawingBrush> class.</span></span> <span data-ttu-id="22a0a-114">In diesem Abschnitt des Beispiels wird ein checkboard-Muster auf den Hintergrund angewendet.</span><span class="sxs-lookup"><span data-stu-id="22a0a-114">This section of the example applies a checkerboard pattern to the background.</span></span>  
  
4. <span data-ttu-id="22a0a-115">Die Animation beginnt wieder und wird unbegrenzt wiederholt.</span><span class="sxs-lookup"><span data-stu-id="22a0a-115">The animation begins again and repeats indefinitely.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="22a0a-116"><xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> ist der einzige schlüsselframe, den Sie mit der-Klasse verwenden können <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames> .</span><span class="sxs-lookup"><span data-stu-id="22a0a-116"><xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> is the only type of key frame that you can use with the <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames> class.</span></span> <span data-ttu-id="22a0a-117">Keyframes wie z <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> . b. eine plötzliche Änderung von Werten, d. h. die Farbänderungen in diesem Beispiel treten plötzlich auf.</span><span class="sxs-lookup"><span data-stu-id="22a0a-117">Key frames like <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame> create sudden changes in values, that is, the color changes in this example occur suddenly.</span></span>  
  
 [!code-xaml[keyframes_snip#ObjectAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/ObjectAnimationUsingKeyFramesExample.xaml#objectanimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="22a0a-118">Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span><span class="sxs-lookup"><span data-stu-id="22a0a-118">For the complete sample, see [KeyFrame Animation Sample](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="22a0a-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22a0a-119">See also</span></span>

- <xref:System.Windows.Media.Animation.ObjectAnimationUsingKeyFrames>
- <xref:System.Windows.Controls.Page.Background%2A>
- <xref:System.Windows.Controls.Page>
- <xref:System.Windows.Media.Animation.DiscreteObjectKeyFrame>
- <xref:System.Windows.Media.LinearGradientBrush>
- <xref:System.Windows.Media.RadialGradientBrush>
- <xref:System.Windows.Media.DrawingBrush>
- [<span data-ttu-id="22a0a-120">Übersicht über Keyframe-Animationen</span><span class="sxs-lookup"><span data-stu-id="22a0a-120">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="22a0a-121">Themen zur Vorgehensweise mit Keyframes</span><span class="sxs-lookup"><span data-stu-id="22a0a-121">Key-Frame How-to Topics</span></span>](key-frame-animation-how-to-topics.md)
