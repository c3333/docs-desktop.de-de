---
title: 'Gewusst wie: Treffertest für eine Geometrie in einem visuellen Objekt'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hit tests [WPF], on visual objects comprising Geometry objects [WPF]
- visual objects [WPF], hit tests on
- Geometry objects [WPF], visual objects comprising
ms.assetid: 8bf2643f-d7f9-4cb4-9ea6-5b893c23200d
ms.openlocfilehash: 52b9b99b0af38d797e4a3c98dc0979211c930c1f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976780"
---
# <a name="how-to-hit-test-geometry-in-a-visual"></a>Gewusst wie: Treffertest für eine Geometrie in einem visuellen Objekt
Dieses Beispiel zeigt, wie Sie einen Treffer Test für ein visuelles Objekt ausführen, das aus einem oder mehreren- <xref:System.Windows.Media.Geometry> Objekten besteht.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird gezeigt, wie der <xref:System.Windows.Media.DrawingGroup> aus einem visuellen Objekt abgerufen wird, das die- <xref:System.Windows.Media.VisualTreeHelper.GetDrawing%2A> Methode verwendet. Ein Treffer Test wird dann für den gerenderten Inhalt jeder Zeichnung in der ausgeführt <xref:System.Windows.Media.DrawingGroup> , um zu bestimmen, welche Geometrie getroffen wurde.  
  
> [!NOTE]
> In den meisten Fällen verwenden Sie die- <xref:System.Windows.Media.VisualTreeHelper.HitTest%2A> Methode, um zu bestimmen, ob ein Punkt den gerenderten Inhalt eines visuellen Elements überschneidet.  
  
 [!code-csharp[VisualsOverview#VisualsOverviewSnippet4](~/samples/snippets/csharp/VS_Snippets_Wpf/VisualsOverview/CSharp/Window1.xaml.cs#visualsoverviewsnippet4)]
 [!code-vb[VisualsOverview#VisualsOverviewSnippet4](~/samples/snippets/visualbasic/VS_Snippets_Wpf/VisualsOverview/visualbasic/window1.xaml.vb#visualsoverviewsnippet4)]  
  
 Bei der- <xref:System.Windows.Media.Geometry.FillContains%2A> Methode handelt es sich um eine überladene Methode, die es Ihnen ermöglicht, mithilfe eines angegebenen- <xref:System.Windows.Point> oder- <xref:System.Windows.Media.Geometry> Wenn eine Geometrie gestrichelt ist, kann die Strichelung ggf. über die Füllbereichsgrenzen hinaus reichen. In diesem Fall möchten Sie möglicherweise zusätzlich zu aufgerufen werden <xref:System.Windows.Media.Geometry.StrokeContains%2A> <xref:System.Windows.Media.Geometry.FillContains%2A> .  
  
 Sie können auch eine bereitstellen <xref:System.Windows.Media.ToleranceType> , die für die Zwecke der Bezier-Vereinfachung verwendet wird.  
  
> [!NOTE]
> Bei diesem Beispiel werden keine Clippings oder Transformationen berücksichtigt, die ggf. auf die Geometrie angewendet werden. Außerdem funktioniert dieses Beispiel nicht mit einem formatierten Steuerelement, da diesem keine Zeichnungen direkt zugeordnet sind.  
  
## <a name="see-also"></a>Siehe auch

- [Treffertests in der visuellen Ebene](hit-testing-in-the-visual-layer.md)
- [Treffertest mit Geometrie als Parameter](how-to-hit-test-using-geometry-as-a-parameter.md)
