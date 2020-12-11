---
title: 'Gewusst wie: Animieren eines Objekts auf einem Pfad (Matrixanimation mit Offsetakkumulation)'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- offset accumulation [WPF]
- animation [WPF], objects along paths (matrix animation with offset accumulation)
- matrix animation with offset accumulation [WPF]
ms.assetid: 1bca90ef-9832-4128-8ed6-62908e7ec146
ms.openlocfilehash: 8b3975ef5031b50381dfa9baf7f34a58fc05ab4e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977329"
---
# <a name="how-to-animate-an-object-along-a-path-matrix-animation-with-offset-accumulation"></a><span data-ttu-id="28854-102">Gewusst wie: Animieren eines Objekts auf einem Pfad (Matrixanimation mit Offsetakkumulation)</span><span class="sxs-lookup"><span data-stu-id="28854-102">How to: Animate an Object Along a Path (Matrix Animation with Offset Accumulation)</span></span>
<span data-ttu-id="28854-103">In diesem Beispiel wird gezeigt, wie die <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> -Klasse verwendet wird, um ein Objekt entlang eines Pfads zu animieren, und dass diese Animation ihre offset Werte bei der Wiederholung sammelt.</span><span class="sxs-lookup"><span data-stu-id="28854-103">This example shows how to use the <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> class to animate an object along a path and have that animation accumulate its offset values as it repeats.</span></span>  
  
## <a name="example"></a><span data-ttu-id="28854-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="28854-104">Example</span></span>  
 <span data-ttu-id="28854-105">Im folgenden Beispiel wird das- <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> Objekt verwendet, um die- <xref:System.Windows.Media.MatrixTransform.Matrix%2A> Eigenschaft eines <xref:System.Windows.Media.MatrixTransform> auf eine Schaltfläche angewendeten zu animieren.</span><span class="sxs-lookup"><span data-stu-id="28854-105">The following example uses the <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath> object to animate the <xref:System.Windows.Media.MatrixTransform.Matrix%2A> property of a <xref:System.Windows.Media.MatrixTransform> applied to a button.</span></span> <span data-ttu-id="28854-106">Das Ergebnis ist eine Schaltfläche, die entlang eines gekrümmten Pfads verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="28854-106">As a result, a button moves along a curved path.</span></span>  
  
 <span data-ttu-id="28854-107">Außerdem wird in diesem Beispiel die- <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.IsOffsetCumulative%2A> Eigenschaft auf festgelegt `true` . Dies bewirkt, dass sich der Offset der animierten Matrix bei Wiederholung der Animation ansammelt.</span><span class="sxs-lookup"><span data-stu-id="28854-107">In addition, the example sets the <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.IsOffsetCumulative%2A> property to `true`, which causes the offset of the animated matrix to accumulate as the animation repeats.</span></span> <span data-ttu-id="28854-108">Durch die Offsetakkumulation bewegt sich die Schaltfläche bei Wiederholung der Animation weiter über den Bildschirm und wird nicht auf die Startposition zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="28854-108">Because the offset accumulates, the button moves farther across the screen when the animation repeats, rather than resetting to the starting position.</span></span>  
  
 [!code-xaml[PathAnimationGallery_snippet#MatrixAnimationUsingPathOffsetCumulativeWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_snippet/CS/matrixanimationusingpathexampleoffsetcumulative.xaml#matrixanimationusingpathoffsetcumulativewholepage)]  
  
 [!code-csharp[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathOffsetCumulativeWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/CSharp/MatrixAnimationUsingPathExampleOffsetCumulative.cs#matrixanimationusingpathoffsetcumulativewholepage)]
 [!code-vb[PathAnimationGallery_procedural_snip#MatrixAnimationUsingPathOffsetCumulativeWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PathAnimationGallery_procedural_snip/VisualBasic/MatrixAnimationUsingPathExampleOffsetCumulative.vb#matrixanimationusingpathoffsetcumulativewholepage)]  
  
 <span data-ttu-id="28854-109">Beachten Sie, dass, obwohl die- <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.IsOffsetCumulative%2A> Eigenschaft bewirkt, dass Offset-Werte über Wiederholungen gesammelt werden, keine Rotations Werte gesammelt werden.</span><span class="sxs-lookup"><span data-stu-id="28854-109">Note that, although the <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.IsOffsetCumulative%2A> property causes offset values to accumulate over repetitions, it doesn't cause rotation values to accumulate.</span></span> <span data-ttu-id="28854-110">Um Rotations Werte zu sammeln, legen Sie die-Eigenschaft und die-Eigenschaft der Animation <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.IsAngleCumulative%2A> auf fest `true` .</span><span class="sxs-lookup"><span data-stu-id="28854-110">To make rotation values accumulate, set the animation's <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.DoesRotateWithTangent%2A> and <xref:System.Windows.Media.Animation.MatrixAnimationUsingPath.IsAngleCumulative%2A> properties to `true`.</span></span>  
  
 <span data-ttu-id="28854-111">Das komplette Beispiel finden Sie unter [Beispiel für Pfad Animation](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations).</span><span class="sxs-lookup"><span data-stu-id="28854-111">For the complete sample, see [Path Animation Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Animation/PathAnimations).</span></span> <span data-ttu-id="28854-112">Ein Beispiel, das zeigt, wie Sie einen <xref:System.Windows.Media.Matrix> Wert entlang eines Pfades ohne Offset-Akkumulation animieren, finden Sie unter [Animieren eines Objekts entlang eines Pfads (Matrix Animation)](how-to-animate-an-object-along-a-path-matrix-animation.md).</span><span class="sxs-lookup"><span data-stu-id="28854-112">For an example showing how to animate a <xref:System.Windows.Media.Matrix> value along a path without offset accumulation, see [Animate an Object Along a Path (Matrix Animation)](how-to-animate-an-object-along-a-path-matrix-animation.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28854-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28854-113">See also</span></span>

- [<span data-ttu-id="28854-114">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="28854-114">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="28854-115">Gewusst-wie-Themen zur Pfadanimation</span><span class="sxs-lookup"><span data-stu-id="28854-115">Path Animation How-to Topics</span></span>](path-animation-how-to-topics.md)
