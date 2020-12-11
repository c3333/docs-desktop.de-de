---
title: 'Gewusst wie: Animieren einer Matrix mithilfe von Keyframes'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], Matrix properties with key frames
- Matrix properties [WPF], animating with key frames
- key frames [WPF], animating Matrix properties with
ms.assetid: b851a4c7-ecb1-420e-9203-83e7afd037fd
ms.openlocfilehash: eb596cf728f8a7cc1964963b8509f42bdd7a392a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977314"
---
# <a name="how-to-animate-a-matrix-by-using-key-frames"></a><span data-ttu-id="a5537-102">Gewusst wie: Animieren einer Matrix mithilfe von Keyframes</span><span class="sxs-lookup"><span data-stu-id="a5537-102">How to: Animate a Matrix by Using Key Frames</span></span>
<span data-ttu-id="a5537-103">In diesem Beispiel wird gezeigt, wie die- <xref:System.Windows.Media.MatrixTransform.Matrix%2A> Eigenschaft eines <xref:System.Windows.Media.MatrixTransform> mithilfe von Keyframes animiert wird.</span><span class="sxs-lookup"><span data-stu-id="a5537-103">This example shows how to animate the <xref:System.Windows.Media.MatrixTransform.Matrix%2A> property of a <xref:System.Windows.Media.MatrixTransform> by using key frames.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a5537-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a5537-104">Example</span></span>  
 <span data-ttu-id="a5537-105">Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.MatrixAnimationUsingKeyFrames> Klasse verwendet, um die- <xref:System.Windows.Media.MatrixTransform.Matrix%2A> Eigenschaft eines zu animieren <xref:System.Windows.Media.MatrixTransform> .</span><span class="sxs-lookup"><span data-stu-id="a5537-105">The following example uses the <xref:System.Windows.Media.Animation.MatrixAnimationUsingKeyFrames> class to animate the <xref:System.Windows.Media.MatrixTransform.Matrix%2A> property of a <xref:System.Windows.Media.MatrixTransform>.</span></span> <span data-ttu-id="a5537-106">Im Beispiel wird das <xref:System.Windows.Media.MatrixTransform> -Objekt verwendet, um die Darstellung und Position eines zu transformieren <xref:System.Windows.Controls.Button> .</span><span class="sxs-lookup"><span data-stu-id="a5537-106">The example uses the <xref:System.Windows.Media.MatrixTransform> object to transform the appearance and position of a <xref:System.Windows.Controls.Button>.</span></span>  
  
 <span data-ttu-id="a5537-107">Diese Animation verwendet die <xref:System.Windows.Media.Animation.DiscreteMatrixKeyFrame> -Klasse, um zwei Keyframes zu erstellen und mit Ihnen die folgenden Aktionen durchführen zu können:</span><span class="sxs-lookup"><span data-stu-id="a5537-107">This animation uses the <xref:System.Windows.Media.Animation.DiscreteMatrixKeyFrame> class to create two key frames and does the following with them:</span></span>  
  
1. <span data-ttu-id="a5537-108">Animiert den ersten <xref:System.Windows.Media.Matrix> während der ersten 0,2 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a5537-108">Animates the first <xref:System.Windows.Media.Matrix> during the first 0.2 seconds.</span></span> <span data-ttu-id="a5537-109">Im Beispiel werden die <xref:System.Windows.Media.Matrix.M11%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.Matrix.M12%2A> der geändert <xref:System.Windows.Media.Matrix> .</span><span class="sxs-lookup"><span data-stu-id="a5537-109">The example changes the <xref:System.Windows.Media.Matrix.M11%2A> and <xref:System.Windows.Media.Matrix.M12%2A> properties of the <xref:System.Windows.Media.Matrix>.</span></span> <span data-ttu-id="a5537-110">Diese Änderung bewirkt, dass die Schaltfläche gestreckt wird und verzerrt wird.</span><span class="sxs-lookup"><span data-stu-id="a5537-110">This change causes the button to stretch and become skewed.</span></span> <span data-ttu-id="a5537-111">Das Beispiel ändert auch die <xref:System.Windows.Media.Matrix.OffsetX%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Media.Matrix.OffsetY%2A> , sodass die Schaltfläche die Position ändert.</span><span class="sxs-lookup"><span data-stu-id="a5537-111">The example also changes the <xref:System.Windows.Media.Matrix.OffsetX%2A> and <xref:System.Windows.Media.Matrix.OffsetY%2A> properties so that the button changes position.</span></span>  
  
2. <span data-ttu-id="a5537-112">Animiert den zweiten <xref:System.Windows.Media.Matrix> um 1,0 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="a5537-112">Animates the second <xref:System.Windows.Media.Matrix> at 1.0 seconds.</span></span> <span data-ttu-id="a5537-113">Die Schaltfläche wird an eine andere Position verschoben, während die Schaltfläche nicht mehr verzerrt oder gestreckt wird.</span><span class="sxs-lookup"><span data-stu-id="a5537-113">The button moves to another position while the button is no longer skewed or stretched.</span></span>  
  
3. <span data-ttu-id="a5537-114">Wiederholt die Animation unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="a5537-114">Repeats the animation indefinitely.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="a5537-115">Keyframes, die vom- <xref:System.Windows.Media.Animation.DiscreteMatrixKeyFrame> Objekt abgeleitet werden, erzeugen plötzliche Sprünge zwischen Werten, d. h., dass die Bewegung der Animation ruckartig ist.</span><span class="sxs-lookup"><span data-stu-id="a5537-115">Key frames that derive from the <xref:System.Windows.Media.Animation.DiscreteMatrixKeyFrame> object create sudden jumps between values, that is, the movement of the animation is jerky.</span></span>  
  
 [!code-xaml[keyframes_snip#MatrixAnimationUsingKeyFramesWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/keyframes_snip/XAML/MatrixAnimationUsingKeyFramesExample.xaml#matrixanimationusingkeyframeswholepage)]  
  
 <span data-ttu-id="a5537-116">Das vollständige Beispiel finden Sie unter [Beispiel für eine Keyframe-Animation](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span><span class="sxs-lookup"><span data-stu-id="a5537-116">For the complete sample, see [KeyFrame Animation Sample](https://github.com/microsoft/WPF-Samples/tree/master/Animation/KeyFrameAnimation).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a5537-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5537-117">See also</span></span>

- <xref:System.Windows.Media.MatrixTransform.Matrix%2A>
- <xref:System.Windows.Media.MatrixTransform>
- [<span data-ttu-id="a5537-118">Übersicht über Keyframe-Animationen</span><span class="sxs-lookup"><span data-stu-id="a5537-118">Key-Frame Animations Overview</span></span>](key-frame-animations-overview.md)
- [<span data-ttu-id="a5537-119">Themen zur Vorgehensweise mit Keyframes</span><span class="sxs-lookup"><span data-stu-id="a5537-119">Key-Frame How-to Topics</span></span>](key-frame-animation-how-to-topics.md)
