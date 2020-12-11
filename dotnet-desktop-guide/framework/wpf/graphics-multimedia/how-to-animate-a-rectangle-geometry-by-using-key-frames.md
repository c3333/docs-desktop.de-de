---
title: 'Gewusst wie: Animieren einer Rechteckgeometrie mithilfe von Keyframes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- key frames [WPF], animating RectangleGeometry objects with
- RectangleGeometry objects [WPF], animating with key frames
- animation [WPF], RectangleGeometry objects with key frames
ms.assetid: a8b45ceb-0e32-4ba1-928f-df6d30db17c6
ms.openlocfilehash: bcc9e7f198b8a20ffe13daf6508fb8a735937652
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974928"
---
# <a name="how-to-animate-a-rectangle-geometry-by-using-key-frames"></a><span data-ttu-id="15e07-102">Gewusst wie: Animieren einer Rechteckgeometrie mithilfe von Keyframes</span><span class="sxs-lookup"><span data-stu-id="15e07-102">How to: Animate a Rectangle Geometry by Using Key Frames</span></span>
<span data-ttu-id="15e07-103">In diesem Beispiel wird gezeigt, wie die- <xref:System.Windows.Media.RectangleGeometry.Rect%2A> Eigenschaft eines <xref:System.Windows.Media.RectangleGeometry> mithilfe von Keyframes animiert wird.</span><span class="sxs-lookup"><span data-stu-id="15e07-103">This example shows how to animate the <xref:System.Windows.Media.RectangleGeometry.Rect%2A> property of a <xref:System.Windows.Media.RectangleGeometry> by using key frames.</span></span>  
  
## <a name="example"></a><span data-ttu-id="15e07-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="15e07-104">Example</span></span>  
 <span data-ttu-id="15e07-105">Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.RectAnimationUsingKeyFrames> Klasse verwendet, um die- <xref:System.Windows.Media.RectangleGeometry.Rect%2A> Eigenschaft eines zu animieren <xref:System.Windows.Media.RectangleGeometry> .</span><span class="sxs-lookup"><span data-stu-id="15e07-105">The following example uses the <xref:System.Windows.Media.Animation.RectAnimationUsingKeyFrames> class to animate the <xref:System.Windows.Media.RectangleGeometry.Rect%2A> property of a <xref:System.Windows.Media.RectangleGeometry>.</span></span> <span data-ttu-id="15e07-106">In dieser Animation werden drei Keyframes folgendermaßen verwendet:</span><span class="sxs-lookup"><span data-stu-id="15e07-106">This animation uses three key frames in the following manner:</span></span>  
  
1. <span data-ttu-id="15e07-107">In den ersten zwei Sekunden wird eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.LinearRectKeyFrame> um eine schrittweise Änderung an Position, Breite und Höhe eines Rechtecks zu animieren.</span><span class="sxs-lookup"><span data-stu-id="15e07-107">During the first two seconds, uses an instance of the <xref:System.Windows.Media.Animation.LinearRectKeyFrame> class to animate a gradual change in the position, width, and height of a rectangle.</span></span> <span data-ttu-id="15e07-108">Lineare Keyframes, wie z <xref:System.Windows.Media.Animation.LinearRectKeyFrame> . b. eine glatte lineare Umstellung zwischen Werten.</span><span class="sxs-lookup"><span data-stu-id="15e07-108">Linear key frames like <xref:System.Windows.Media.Animation.LinearRectKeyFrame> create a smooth linear transition between values.</span></span>  
  
2. <span data-ttu-id="15e07-109">Am Ende der nächsten halben Sekunde wird von eine Instanz der-Klasse verwendet, <xref:System.Windows.Media.Animation.DiscreteRectKeyFrame> um die Höhe des Rechtecks plötzlich zu verringern.</span><span class="sxs-lookup"><span data-stu-id="15e07-109">During the end of the next half second, uses an instance of the <xref:System.Windows.Media.Animation.DiscreteRectKeyFrame> class to suddenly decrease the height of the rectangle.</span></span> <span data-ttu-id="15e07-110">Diskrete Keyframes, wie z. b. <xref:System.Windows.Media.Animation.DiscreteRectKeyFrame> plötzliche Änderungen zwischen Werten, d. h., die Abnahme der Höhe erfolgt schnell und ist nicht fein.</span><span class="sxs-lookup"><span data-stu-id="15e07-110">Discrete key frames like <xref:System.Windows.Media.Animation.DiscreteRectKeyFrame> create sudden changes between values, that is, the decrease in height occurs quickly and is not subtle.</span></span>  
  
3. <span data-ttu-id="15e07-111">In den letzten zwei Sekunden wird eine Instanz der <xref:System.Windows.Media.Animation.SplineRectKeyFrame> -Klasse verwendet, um das Rechteck wieder in seine ursprüngliche Größe und Position zu ändern.</span><span class="sxs-lookup"><span data-stu-id="15e07-111">During the final two seconds, uses an instance of the <xref:System.Windows.Media.Animation.SplineRectKeyFrame> class to change the rectangle back to its original size and position.</span></span> <span data-ttu-id="15e07-112">Spline-Keyframes wie <xref:System.Windows.Media.Animation.SplineRectKeyFrame> das Erstellen eines Variablen Übergangs zwischen Werten gemäß den Werten der- <xref:System.Windows.Media.Animation.SplineRectKeyFrame.KeySpline%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="15e07-112">Spline key frames like <xref:System.Windows.Media.Animation.SplineRectKeyFrame> create a variable transition between values according to the values of the <xref:System.Windows.Media.Animation.SplineRectKeyFrame.KeySpline%2A> property.</span></span> <span data-ttu-id="15e07-113">In diesem Beispiel beginnt die Veränderung zunächst langsam und beschleunigt dann exponentiell im letzten Bereich des Zeitabschnitts.</span><span class="sxs-lookup"><span data-stu-id="15e07-113">In this example, the change begins slowly and speeds up exponentially toward the end of the time segment.</span></span>  
  
 [!code-csharp[keyframes_snip#RectAnimationUsingKeyFramesWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/keyframes_snip/CSharp/RectAnimationUsingKeyFramesExample.cs#rectanimationusingkeyframeswholepage)]
 [!code-vb[keyframes_snip#RectAnimationUsingKeyFramesWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/keyframes_snip/visualbasic/rectanimationusingkeyframesexample.vb#rectanimationusingkeyframeswholepage)]
 [!code-xaml[keyframes_snip#RectAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/RectAnimationUsingKeyFramesExample.xaml#rectanimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="15e07-114">Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span><span class="sxs-lookup"><span data-stu-id="15e07-114">For the complete sample, see [KeyFrame Animation Sample](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="15e07-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15e07-115">See also</span></span>

- <xref:System.Windows.Media.RectangleGeometry>
- <xref:System.Windows.Media.RectangleGeometry.Rect%2A>
- <xref:System.Windows.Media.Animation.RectAnimationUsingKeyFrames>
- [<span data-ttu-id="15e07-116">Übersicht über Keyframe-Animationen</span><span class="sxs-lookup"><span data-stu-id="15e07-116">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="15e07-117">Themen zur Vorgehensweise mit Keyframes</span><span class="sxs-lookup"><span data-stu-id="15e07-117">Key-Frame How-to Topics</span></span>](key-frame-animation-how-to-topics.md)
