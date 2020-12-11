---
title: 'Gewusst wie: Animieren eines "EllipseGeometry"-Elements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- animation [WPF], EllipseGeometry objects [WPF]
- EllipseGeometry objects [WPF], animating
- graphics [WPF], animation
ms.assetid: 767b9b6e-9cb7-482e-b6c2-fee7750c3995
ms.openlocfilehash: 0f8174a2144435c9ad65904ee587355e8b38e935
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977287"
---
# <a name="how-to-animate-an-ellipsegeometry"></a><span data-ttu-id="adffc-102">Gewusst wie: Animieren eines "EllipseGeometry"-Elements</span><span class="sxs-lookup"><span data-stu-id="adffc-102">How to: Animate an EllipseGeometry</span></span>
<span data-ttu-id="adffc-103">Dieses Beispiel zeigt, wie ein <xref:System.Windows.Media.Geometry> in einem- <xref:System.Windows.Shapes.Path> Element animiert wird.</span><span class="sxs-lookup"><span data-stu-id="adffc-103">This example shows how to animate a <xref:System.Windows.Media.Geometry> within a <xref:System.Windows.Shapes.Path> element.</span></span> <span data-ttu-id="adffc-104">Im folgenden Beispiel <xref:System.Windows.Media.Animation.PointAnimation> wird ein verwendet, um den eines zu animieren <xref:System.Windows.Media.EllipseGeometry.Center%2A> <xref:System.Windows.Media.EllipseGeometry> .</span><span class="sxs-lookup"><span data-stu-id="adffc-104">In the following example, a <xref:System.Windows.Media.Animation.PointAnimation> is used to animate the <xref:System.Windows.Media.EllipseGeometry.Center%2A> of an <xref:System.Windows.Media.EllipseGeometry>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="adffc-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="adffc-105">Example</span></span>  
 [!code-xaml[animatepath_snip_XAML#1](~/samples/snippets/csharp/VS_Snippets_Wpf/animatepath_snip_XAML/CS/EllipseGeometryExample.xaml#1)]  
  
 [!code-csharp[animatepath_snip#101](~/samples/snippets/csharp/VS_Snippets_Wpf/animatepath_snip/CSharp/EllipseGeometryExample.cs#101)]  
  
 [!code-vb[animatepath_snip#201](~/samples/snippets/visualbasic/VS_Snippets_Wpf/animatepath_snip/VisualBasic/EllipseGeometryExample.vb#201)]  
  
## <a name="see-also"></a><span data-ttu-id="adffc-106">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="adffc-106">See also</span></span>

- [<span data-ttu-id="adffc-107">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="adffc-107">Animation Overview</span></span>](animation-overview.md)
- [<span data-ttu-id="adffc-108">Übersicht über die Geometrie</span><span class="sxs-lookup"><span data-stu-id="adffc-108">Geometry Overview</span></span>](geometry-overview.md)
