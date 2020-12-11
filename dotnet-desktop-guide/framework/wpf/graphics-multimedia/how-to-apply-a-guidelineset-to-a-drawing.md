---
title: 'Gewusst wie: Anwenden eines Führungsliniensatzes auf eine Zeichnung'
ms.date: 03/30/2017
helpviewer_keywords:
- GuidelineSet property [WPF], applying to drawings
- graphics [WPF], GuidelineSet property
ms.assetid: 45f3e0b4-8820-45a7-b865-b8ea5b17b0c8
ms.openlocfilehash: 134236c5beca806b747d45f20764cc82ddd8a4e8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977765"
---
# <a name="how-to-apply-a-guidelineset-to-a-drawing"></a><span data-ttu-id="45604-102">Gewusst wie: Anwenden eines Führungsliniensatzes auf eine Zeichnung</span><span class="sxs-lookup"><span data-stu-id="45604-102">How to: Apply a GuidelineSet to a Drawing</span></span>
<span data-ttu-id="45604-103">In diesem Beispiel wird gezeigt, wie ein <xref:System.Windows.Media.GuidelineSet> auf einen angewendet wird <xref:System.Windows.Media.DrawingGroup> .</span><span class="sxs-lookup"><span data-stu-id="45604-103">This example shows how to apply a <xref:System.Windows.Media.GuidelineSet> to a <xref:System.Windows.Media.DrawingGroup>.</span></span>  
  
 <span data-ttu-id="45604-104">Die- <xref:System.Windows.Media.DrawingGroup> Klasse ist der einzige Typ von <xref:System.Windows.Media.Drawing> , der über eine-Eigenschaft verfügt <xref:System.Windows.Media.DrawingGroup.GuidelineSet%2A> .</span><span class="sxs-lookup"><span data-stu-id="45604-104">The <xref:System.Windows.Media.DrawingGroup> class is the only type of <xref:System.Windows.Media.Drawing> that has a <xref:System.Windows.Media.DrawingGroup.GuidelineSet%2A> property.</span></span> <span data-ttu-id="45604-105">Wenn Sie ein <xref:System.Windows.Media.GuidelineSet> auf einen anderen Typ von anwenden möchten <xref:System.Windows.Media.Drawing> , fügen Sie es einem hinzu, <xref:System.Windows.Media.DrawingGroup> und wenden Sie dann <xref:System.Windows.Media.GuidelineSet> auf den an <xref:System.Windows.Media.DrawingGroup> .</span><span class="sxs-lookup"><span data-stu-id="45604-105">To apply a <xref:System.Windows.Media.GuidelineSet> to another type of <xref:System.Windows.Media.Drawing>, add it to a <xref:System.Windows.Media.DrawingGroup> and then apply the <xref:System.Windows.Media.GuidelineSet> to your <xref:System.Windows.Media.DrawingGroup>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="45604-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="45604-106">Example</span></span>  
 <span data-ttu-id="45604-107">Im folgenden Beispiel werden zwei <xref:System.Windows.Media.DrawingGroup> -Objekte erstellt, die fast identisch sind. der einzige Unterschied besteht darin, dass der zweite <xref:System.Windows.Media.DrawingGroup> <xref:System.Windows.Media.GuidelineSet> -Wert und der erste nicht ist.</span><span class="sxs-lookup"><span data-stu-id="45604-107">The following example creates two <xref:System.Windows.Media.DrawingGroup> objects that are almost identical; the only difference is: the second <xref:System.Windows.Media.DrawingGroup> has a <xref:System.Windows.Media.GuidelineSet> and the first does not.</span></span>  
  
 <span data-ttu-id="45604-108">Die folgende Abbildung zeigt die Ausgabe des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="45604-108">The following illustration shows the output from the example.</span></span> <span data-ttu-id="45604-109">Da der renderingunterschied zwischen den beiden- <xref:System.Windows.Media.DrawingGroup> Objekten so gering ist, werden Teile der Zeichnungen vergrößert.</span><span class="sxs-lookup"><span data-stu-id="45604-109">Because the rendering difference between the two <xref:System.Windows.Media.DrawingGroup> objects is so subtle, portions of the drawings are enlarged.</span></span>  
  
 <span data-ttu-id="45604-110">![Eine DrawingGroup mit und ohne ein GuidelineSet](./media/graphicsmm-drawinggroup-guidelineset.png "graphicsmm_drawinggroup_guidelineset")</span><span class="sxs-lookup"><span data-stu-id="45604-110">![A DrawingGroup with and without a GuidelineSet](./media/graphicsmm-drawinggroup-guidelineset.png "graphicsmm_drawinggroup_guidelineset")</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#GraphicsMMDrawingGroupGuidelineSetExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/DrawingGroupGuidelineSetExample.cs#graphicsmmdrawinggroupguidelinesetexamplewholepage)]
 [!code-xaml[DrawingMiscSnippets_snip#GraphicsMMDrawingGroupGuidelineSetExampleWholePage](~/samples/snippets/xaml/VS_Snippets_Wpf/DrawingMiscSnippets_snip/XAML/DrawingGroupGuidelineSetExample.xaml#graphicsmmdrawinggroupguidelinesetexamplewholepage)]  
  
## <a name="see-also"></a><span data-ttu-id="45604-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="45604-111">See also</span></span>

- <xref:System.Windows.Media.DrawingGroup>
- <xref:System.Windows.Media.GuidelineSet>
- [<span data-ttu-id="45604-112">Übersicht über Zeichnungsobjekte</span><span class="sxs-lookup"><span data-stu-id="45604-112">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
