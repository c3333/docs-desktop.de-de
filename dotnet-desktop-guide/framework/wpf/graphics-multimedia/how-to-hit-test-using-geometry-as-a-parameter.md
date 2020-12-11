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
# <a name="how-to-hit-test-using-geometry-as-a-parameter"></a>Gewusst wie: Treffertest mit Geometrie als Parameter
Dieses Beispiel zeigt, wie Sie einen Treffer Test für ein visuelles Objekt ausführen, indem Sie <xref:System.Windows.Media.Geometry> als Treffer Testparameter verwenden.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird gezeigt, wie Sie einen Treffer Test mithilfe <xref:System.Windows.Media.GeometryHitTestParameters> von für die- <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> Methode einrichten. Der <xref:System.Windows.Point> Wert, der an die-Methode weitergegeben wird, `OnMouseDown` wird verwendet, um ein-Objekt zu erstellen <xref:System.Windows.Media.Geometry> , um den Bereich des Treffer Tests zu erweitern.  
  
 [!code-csharp[HitTestingOverview#HitTestingOverviewSnippet10](~/samples/snippets/csharp/VS_Snippets_Wpf/HitTestingOverview/CSharp/GeometryHitTest.cs#hittestingoverviewsnippet10)]
 [!code-vb[HitTestingOverview#HitTestingOverviewSnippet10](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HitTestingOverview/visualbasic/geometryhittest.vb#hittestingoverviewsnippet10)]  
  
 Die- <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> Eigenschaft von <xref:System.Windows.Media.GeometryHitTestResult> enthält Informationen zu den Ergebnissen eines Treffer Tests, der einen <xref:System.Windows.Media.Geometry> als Treffer Testparameter verwendet. In der folgenden Abbildung wird die Beziehung zwischen der Treffertestgeometrie (blauer Kreis) und dem gerenderten Inhalt des Zielobjekts (rotes Quadrat) dargestellt.  
  
 ![Diagramm, das IntersectionDetail anzeigt, das bei Treffer Tests verwendet wird.](./media/how-to-hit-test-using-geometry-as-a-parameter/intersectiondetail-hit-test.png)  
  
 Im folgenden Beispiel wird gezeigt, wie Sie einen Treffer Test Rückruf implementieren, wenn ein <xref:System.Windows.Media.Geometry> als Treffer Testparameter verwendet wird. Der- `result` Parameter wird in einen umgewandelt, um <xref:System.Windows.Media.GeometryHitTestResult> den Wert der- <xref:System.Windows.Media.GeometryHitTestResult.IntersectionDetail%2A> Eigenschaft abzurufen. Mit dem Eigenschafts Wert können Sie feststellen, ob der <xref:System.Windows.Media.Geometry> Treffer Testparameter vollständig oder teilweise im gerenderten Inhalt des Treffer Test Ziels enthalten ist. In diesem Fall fügt der Beispielcode der Liste visueller Objekte nur Treffertestergebnisse hinzu, die vollständig im Zielbereich enthalten sind.  
  
 [!code-csharp[HitTestingOverview#HitTestingOverviewSnippet11](~/samples/snippets/csharp/VS_Snippets_Wpf/HitTestingOverview/CSharp/GeometryHitTest.cs#hittestingoverviewsnippet11)]
 [!code-vb[HitTestingOverview#HitTestingOverviewSnippet11](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HitTestingOverview/visualbasic/geometryhittest.vb#hittestingoverviewsnippet11)]  
  
> [!NOTE]
> Der <xref:System.Windows.Media.HitTestResult> Rückruf sollte nicht aufgerufen werden, wenn die Überschneidungs Details ist <xref:System.Windows.Media.IntersectionDetail.Empty> .  
  
## <a name="see-also"></a>Siehe auch

- [Treffertests in der visuellen Ebene](hit-testing-in-the-visual-layer.md)
- [Treffertest für eine Geometrie in einem visuellen Objekt](how-to-hit-test-geometry-in-a-visual.md)
