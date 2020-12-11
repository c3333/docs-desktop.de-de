---
title: 'Gewusst wie: Hinzufügen eines Animationsausgabewerts zu einem Animationsstartwert'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF]
ms.assetid: b89a82be-b03d-481e-a8d3-cc513d09ca00
ms.openlocfilehash: 945675d03a280e2394fdb0eab27c0978dc7cc320
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975333"
---
# <a name="how-to-add-an-animation-output-value-to-an-animation-starting-value"></a><span data-ttu-id="5f033-102">Gewusst wie: Hinzufügen eines Animationsausgabewerts zu einem Animationsstartwert</span><span class="sxs-lookup"><span data-stu-id="5f033-102">How to: Add an Animation Output Value to an Animation Starting Value</span></span>
<span data-ttu-id="5f033-103">In diesem Beispiel wird gezeigt, wie Sie einen Animations Ausgabewert zu einem Animations Start Wert hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5f033-103">This example shows how to add an animation output value to an animation starting value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5f033-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5f033-104">Example</span></span>  
 <span data-ttu-id="5f033-105">Die- <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A> Eigenschaft gibt an, ob der Ausgabewert einer Animation dem Startwert (Basiswert) einer animierten Eigenschaft hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f033-105">The <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A> property specifies whether you want the output value of an animation added to the starting value (base value) of an animated property.</span></span> <span data-ttu-id="5f033-106">Sie können die <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A> -Eigenschaft mit den meisten grundlegenden Animationen und den meisten Keyframe-Animationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f033-106">You can use the <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A> property with most basic animations and most key frame animations.</span></span> <span data-ttu-id="5f033-107">Weitere Informationen finden Sie unter Übersicht über [Animationen](animation-overview.md) und [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5f033-107">For more information, see [Animation Overview](animation-overview.md) and [Key-Frame Animations Overview](key-frame-animations-overview.md).</span></span>  
  
 <span data-ttu-id="5f033-108">Das folgende Beispiel zeigt die Auswirkung der Verwendung der <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A?displayProperty=nameWithType> -Eigenschaft mit <xref:System.Windows.Media.Animation.DoubleAnimation> und die Verwendung der- <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsAdditive%2A?displayProperty=nameWithType> Eigenschaft mit <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> .</span><span class="sxs-lookup"><span data-stu-id="5f033-108">The following example shows the effect of using the <xref:System.Windows.Media.Animation.DoubleAnimation.IsAdditive%2A?displayProperty=nameWithType> property with <xref:System.Windows.Media.Animation.DoubleAnimation> and using the <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames.IsAdditive%2A?displayProperty=nameWithType> property with <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>.</span></span>  
  
 [!code-xaml[timingbehaviors_snip#IsAdditiveWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/IsAdditiveExample.xaml#isadditivewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="5f033-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f033-109">See also</span></span>

- [<span data-ttu-id="5f033-110">Sammeln von Animationen während Wiederholungszyklen</span><span class="sxs-lookup"><span data-stu-id="5f033-110">Accumulate Animation Values During Repeat Cycles</span></span>](how-to-accumulate-animation-values-during-repeat-cycles.md)
- [<span data-ttu-id="5f033-111">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="5f033-111">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="5f033-112">Übersicht über Keyframe-Animationen</span><span class="sxs-lookup"><span data-stu-id="5f033-112">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="5f033-113">Gewusst-wie-Themen zu Animation und Zeitsteuerung</span><span class="sxs-lookup"><span data-stu-id="5f033-113">Animation and Timing How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
