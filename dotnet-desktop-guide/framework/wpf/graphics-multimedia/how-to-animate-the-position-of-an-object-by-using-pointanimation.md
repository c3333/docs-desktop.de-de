---
title: 'Gewusst wie: Animieren der Position eines Objekts mit PointAnimation'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [WPF], animation
- animation [WPF], PointAnimation
ms.assetid: 42310977-cc90-438a-8a47-0345898e01be
ms.openlocfilehash: 1ef3f77e551affaa7e61d2aabf95f10c29275417
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975331"
---
# <a name="how-to-animate-the-position-of-an-object-by-using-pointanimation"></a><span data-ttu-id="41ace-102">Gewusst wie: Animieren der Position eines Objekts mit PointAnimation</span><span class="sxs-lookup"><span data-stu-id="41ace-102">How to: Animate the Position of an Object by Using PointAnimation</span></span>
<span data-ttu-id="41ace-103">In diesem Beispiel wird gezeigt, wie die-Klasse verwendet wird <xref:System.Windows.Media.Animation.PointAnimation> , um ein Objekt entlang eines zu animieren <xref:System.Windows.Shapes.Path> .</span><span class="sxs-lookup"><span data-stu-id="41ace-103">This example shows how to use the <xref:System.Windows.Media.Animation.PointAnimation> class to animate an object along a <xref:System.Windows.Shapes.Path>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="41ace-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="41ace-104">Example</span></span>  
 <span data-ttu-id="41ace-105">Im folgenden Beispiel wird eine Ellipse entlang eines <xref:System.Windows.Shapes.Path> von einem Punkt auf dem Bildschirm zu einem anderen verschoben.</span><span class="sxs-lookup"><span data-stu-id="41ace-105">The following example moves an ellipse along a <xref:System.Windows.Shapes.Path> from one point on the screen to another.</span></span> <span data-ttu-id="41ace-106">Im Beispiel wird die Position eines animiert <xref:System.Windows.Media.EllipseGeometry> <xref:System.Windows.Media.Animation.PointAnimation> , indem zum Animieren der Eigenschaft verwendet wird <xref:System.Windows.Media.EllipseGeometry.Center%2A> .</span><span class="sxs-lookup"><span data-stu-id="41ace-106">The example animates the position of an <xref:System.Windows.Media.EllipseGeometry> by using <xref:System.Windows.Media.Animation.PointAnimation> to animate the <xref:System.Windows.Media.EllipseGeometry.Center%2A> property.</span></span>  
  
 [!code-csharp[BasicAnimations_snip#PointAnimationWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/BasicAnimations_snip/CSharp/PointAnimationExample.cs#pointanimationwholepage)]
 [!code-vb[BasicAnimations_snip#PointAnimationWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/BasicAnimations_snip/VisualBasic/PointAnimationExample.vb#pointanimationwholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="41ace-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41ace-107">See also</span></span>

- <xref:System.Windows.Media.Animation.PointAnimation>
- <xref:System.Windows.Shapes.Path>
- <xref:System.Windows.Media.EllipseGeometry>
- <xref:System.Windows.Media.EllipseGeometry.Center%2A>
- [<span data-ttu-id="41ace-108">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="41ace-108">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="41ace-109">Grafiken und Multimedia</span><span class="sxs-lookup"><span data-stu-id="41ace-109">Graphics and Multimedia</span></span>](index.md)
- [<span data-ttu-id="41ace-110">Gewusst-wie-Themen zu Grafiken</span><span class="sxs-lookup"><span data-stu-id="41ace-110">Graphics How-to Topics</span></span>](graphics-how-to-topics.md)
- [<span data-ttu-id="41ace-111">Gewusst-wie-Themen zu Animation und Zeitsteuerung</span><span class="sxs-lookup"><span data-stu-id="41ace-111">Animation and Timing How-to Topics</span></span>](animation-and-timing-how-to-topics.md)
