---
title: 'Gewusst wie: Animieren einer Eigenschaft mit AnimationClock'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], properties [WPF], with AnimationClocks
- AnimationClocks [WPF]
ms.assetid: e6542021-714c-4675-9567-04f1c7380834
ms.openlocfilehash: 13d91e8589c40d84ba374ffc613388e24407796a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974931"
---
# <a name="how-to-animate-a-property-by-using-an-animationclock"></a><span data-ttu-id="e93b6-102">Gewusst wie: Animieren einer Eigenschaft mit AnimationClock</span><span class="sxs-lookup"><span data-stu-id="e93b6-102">How to: Animate a Property by Using an AnimationClock</span></span>
<span data-ttu-id="e93b6-103">In diesem Beispiel wird gezeigt, wie- <xref:System.Windows.Media.Animation.Clock> Objekte zum Animieren einer Eigenschaft verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e93b6-103">This example shows how to use <xref:System.Windows.Media.Animation.Clock> objects to animate a property.</span></span>  
  
 <span data-ttu-id="e93b6-104">Es gibt drei Möglichkeiten, eine Abhängigkeitseigenschaft zu animieren:</span><span class="sxs-lookup"><span data-stu-id="e93b6-104">There are three ways to animate a dependency property:</span></span>  
  
- <span data-ttu-id="e93b6-105">Erstellen <xref:System.Windows.Media.Animation.AnimationTimeline> Sie ein-Objekt, und ordnen Sie es der Eigenschaft mithilfe von zu <xref:System.Windows.Media.Animation.Storyboard> .</span><span class="sxs-lookup"><span data-stu-id="e93b6-105">Create an <xref:System.Windows.Media.Animation.AnimationTimeline> and associate it with that property by using a <xref:System.Windows.Media.Animation.Storyboard>.</span></span>  
  
- <span data-ttu-id="e93b6-106">Verwenden Sie die-Methode des-Objekts <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> , um eine einzelne <xref:System.Windows.Media.Animation.AnimationTimeline> auf eine Ziel Eigenschaft anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="e93b6-106">Use the object's <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> method to apply a single <xref:System.Windows.Media.Animation.AnimationTimeline> to a target property.</span></span>  
  
- <span data-ttu-id="e93b6-107">Erstellen <xref:System.Windows.Media.Animation.AnimationClock> Sie ein aus einem <xref:System.Windows.Media.Animation.AnimationTimeline> , und wenden Sie es auf eine Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="e93b6-107">Create an <xref:System.Windows.Media.Animation.AnimationClock> from an <xref:System.Windows.Media.Animation.AnimationTimeline> and apply it to a property.</span></span>  
  
 <span data-ttu-id="e93b6-108"><xref:System.Windows.Media.Animation.Storyboard> mithilfe von Objekten und der- <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> Methode können Sie Eigenschaften animieren, ohne Uhren direkt zu erstellen und zu verteilen (Beispiele finden Sie unter [Animieren einer Eigenschaft mithilfe eines Storyboards](how-to-animate-a-property-by-using-a-storyboard.md) und [Animieren einer Eigenschaft ohne Storyboard](how-to-animate-a-property-without-using-a-storyboard.md)); Uhren werden automatisch erstellt und verteilt.</span><span class="sxs-lookup"><span data-stu-id="e93b6-108"><xref:System.Windows.Media.Animation.Storyboard> objects and the <xref:System.Windows.Media.Animation.Animatable.BeginAnimation%2A> method enable you to animate properties without directly creating and distributing clocks (for examples, see [Animate a Property by Using a Storyboard](how-to-animate-a-property-by-using-a-storyboard.md) and [Animate a Property Without Using a Storyboard](how-to-animate-a-property-without-using-a-storyboard.md)); clocks are created and distributed for you automatically.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e93b6-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e93b6-109">Example</span></span>  
 <span data-ttu-id="e93b6-110">Im folgenden Beispiel wird gezeigt, wie ein erstellt <xref:System.Windows.Media.Animation.AnimationClock> und auf zwei ähnliche Eigenschaften angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="e93b6-110">The following example shows how to create an <xref:System.Windows.Media.Animation.AnimationClock> and apply it to two similar properties.</span></span>  
  
 [!code-csharp[timingbehaviors_procedural_snip#GraphicsMMCreateAnimationClockWholeClass](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_procedural_snip/CSharp/AnimationClockExample.cs#graphicsmmcreateanimationclockwholeclass)]
 [!code-vb[timingbehaviors_procedural_snip#GraphicsMMCreateAnimationClockWholeClass](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_procedural_snip/visualbasic/animationclockexample.vb#graphicsmmcreateanimationclockwholeclass)]  
  
 <span data-ttu-id="e93b6-111">Ein Beispiel, das zeigt, wie ein nach dem Start interaktiv gesteuert <xref:System.Windows.Media.Animation.Clock> wird, finden Sie unter [interaktiv Steuern einer Uhr](how-to-interactively-control-a-clock.md).</span><span class="sxs-lookup"><span data-stu-id="e93b6-111">For an example showing how to interactively control a <xref:System.Windows.Media.Animation.Clock> after it starts, see [Interactively Control a Clock](how-to-interactively-control-a-clock.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e93b6-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e93b6-112">See also</span></span>

- [<span data-ttu-id="e93b6-113">Animieren einer Eigenschaft unter Verwendung eines Storyboards</span><span class="sxs-lookup"><span data-stu-id="e93b6-113">Animate a Property by Using a Storyboard</span></span>](how-to-animate-a-property-by-using-a-storyboard.md)
- [<span data-ttu-id="e93b6-114">Animieren einer Eigenschaft ohne Storyboard</span><span class="sxs-lookup"><span data-stu-id="e93b6-114">Animate a Property Without Using a Storyboard</span></span>](how-to-animate-a-property-without-using-a-storyboard.md)
- [<span data-ttu-id="e93b6-115">Übersicht über die Verfahren zur Animation von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e93b6-115">Property Animation Techniques Overview</span></span>](property-animation-techniques-overview.md)
