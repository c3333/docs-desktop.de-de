---
title: 'Gewusst wie: Treffertest mit Geometrie als Parameter'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hit tests [WPF], on visual objects using Geometry objects [WPF]
- visual objects [WPF], hit tests on
- Geometry objects [WPF], hit tests on visual objects [WPF]
ms.assetid: 6c8bdbf2-19e0-4fbb-bf89-c1252b2ebc61
ms.openlocfilehash: 8bed7784b00f49178c9a87def74b62f7ce620ec7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976778"
---
# <a name="how-to-hit-test-using-geometry-as-a-parameter"></a><span data-ttu-id="7728b-102">Gewusst wie: Treffertest mit Geometrie als Parameter</span><span class="sxs-lookup"><span data-stu-id="7728b-102">How to: Hit Test Using Geometry as a Parameter</span></span>
<span data-ttu-id="7728b-103">Dieses Beispiel zeigt, wie Sie einen Treffer Test für ein visuelles Objekt ausführen, indem Sie <xref:System.Windows.Media.Geometry> als Treffer Testparameter verwenden.</span><span class="sxs-lookup"><span data-stu-id="7728b-103">This example shows how to perform a hit test on a visual object using a <xref:System.Windows.Media.Geometry> as a hit test parameter.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7728b-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7728b-104">Example</span></span>  
 <span data-ttu-id="7728b-105">Im folgenden Beispiel wird gezeigt, wie Sie einen Treffer Test mithilfe <xref:System.Windows.Media.GeometryHitTestParameters> von für die- <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> Methode einrichten.</span><span class="sxs-lookup"><span data-stu-id="7728b-105">The following example shows how to set up a hit test using <xref:System.Windows.Media.GeometryHitTestParameters> for the <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> method.</span></span> <span data-ttu-id="7728b-106">Der <xref:System.Windows.Point> Wert, der an die-Methode weitergegeben wird, `OnMouseDown` wird verwendet, um ein-Objekt zu erstellen <xref:System.Windows.Media.Geometry> , um den Bereich des Treffer Tests zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="7728b-106">The <xref:System.Windows.Point> value that is passed to the `OnMouseDown` method is used to create a <xref:System.Windows.Media.Geometry> object in order to expand the range of the hit test.</span></span>  
  
 [!code-csharp[HitTestingOverview#HitTestingOverviewSnippet10](~/samples/snippets/csharp/VS_Snippets_Wpf/HitTestingOverview/CSharp/GeometryHitTest.cs#hittestingoverviewsnippet10)]
 [!code-vb[HitTestingOverview#HitTestingOverviewSnippet10](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HitTestingOverview/visualbasic/geometryhittest.vb#hittestingoverviewsnippet10)]  
  
 <span data-ttu-id="7728b-107">Die- <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> Eigenschaft von <xref:System.Windows.Media.GeometryHitTestResult> enthält Informationen zu den Ergebnissen eines Treffer Tests, der einen <xref:System.Windows.Media.Geometry> als Treffer Testparameter verwendet.</span><span class="sxs-lookup"><span data-stu-id="7728b-107">The <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> property of <xref:System.Windows.Media.GeometryHitTestResult> provides information about the results of a hit test that uses a <xref:System.Windows.Media.Geometry> as a hit test parameter.</span></span> <span data-ttu-id="7728b-108">In der folgenden Abbildung wird die Beziehung zwischen der Treffertestgeometrie (blauer Kreis) und dem gerenderten Inhalt des Zielobjekts (rotes Quadrat) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7728b-108">The following illustration shows the relationship between the hit test geometry (the blue circle) and the rendered content of the target visual object (the red square).</span></span>  
  
 ![Diagramm, das IntersectionDetail anzeigt, das bei Treffer Tests verwendet wird.](./media/how-to-hit-test-using-geometry-as-a-parameter/intersectiondetail-hit-test.png)  
  
 <span data-ttu-id="7728b-110">Im folgenden Beispiel wird gezeigt, wie Sie einen Treffer Test Rückruf implementieren, wenn ein <xref:System.Windows.Media.Geometry> als Treffer Testparameter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7728b-110">The following example shows how to implement a hit test callback when a <xref:System.Windows.Media.Geometry> is used as a hit test parameter.</span></span> <span data-ttu-id="7728b-111">Der- `result` Parameter wird in einen umgewandelt, um <xref:System.Windows.Media.GeometryHitTestResult> den Wert der- <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> Eigenschaft abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7728b-111">The `result` parameter is cast to a <xref:System.Windows.Media.GeometryHitTestResult> in order to retrieve the value of the <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> property.</span></span> <span data-ttu-id="7728b-112">Mit dem Eigenschafts Wert können Sie feststellen, ob der <xref:System.Windows.Media.Geometry> Treffer Testparameter vollständig oder teilweise im gerenderten Inhalt des Treffer Test Ziels enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7728b-112">The property value allows you to determine if the <xref:System.Windows.Media.Geometry> hit test parameter is fully or partially contained within the rendered content of the hit test target.</span></span> <span data-ttu-id="7728b-113">In diesem Fall fügt der Beispielcode der Liste visueller Objekte nur Treffertestergebnisse hinzu, die vollständig im Zielbereich enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="7728b-113">In this case, the sample code is only adding hit test results to the list for visuals that are fully contained within the target boundary.</span></span>  
  
 [!code-csharp[HitTestingOverview#HitTestingOverviewSnippet11](~/samples/snippets/csharp/VS_Snippets_Wpf/HitTestingOverview/CSharp/GeometryHitTest.cs#hittestingoverviewsnippet11)]
 [!code-vb[HitTestingOverview#HitTestingOverviewSnippet11](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HitTestingOverview/visualbasic/geometryhittest.vb#hittestingoverviewsnippet11)]  
  
> [!NOTE]
> <span data-ttu-id="7728b-114">Der <xref:System.Windows.Media.HitTestResult> Rückruf sollte nicht aufgerufen werden, wenn die Überschneidungs Details ist <xref:System.Windows.Media.IntersectionDetail.Empty> .</span><span class="sxs-lookup"><span data-stu-id="7728b-114">The <xref:System.Windows.Media.HitTestResult> callback should not be called when the intersection detail is <xref:System.Windows.Media.IntersectionDetail.Empty>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7728b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7728b-115">See also</span></span>

- [<span data-ttu-id="7728b-116">Treffertests in der visuellen Ebene</span><span class="sxs-lookup"><span data-stu-id="7728b-116">Hit Testing in the Visual Layer</span></span>](hit-testing-in-the-visual-layer.md)
- [<span data-ttu-id="7728b-117">Treffertest für eine Geometrie in einem visuellen Objekt</span><span class="sxs-lookup"><span data-stu-id="7728b-117">Hit Test Geometry in a Visual</span></span>](how-to-hit-test-geometry-in-a-visual.md)
