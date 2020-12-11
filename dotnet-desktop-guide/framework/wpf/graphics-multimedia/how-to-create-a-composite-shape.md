---
title: 'Gewusst wie: Erstellen einer zusammengesetzten Form'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- shapes [WPF], composite
- composite shapes [WPF]
- graphics [WPF], composite shapes
ms.assetid: 8e5c7ef4-d7ed-4c43-afc9-ca01325c300b
ms.openlocfilehash: c56053f2b07d6055deac5097a68fd7b80ad704ba
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977608"
---
# <a name="how-to-create-a-composite-shape"></a>Gewusst wie: Erstellen einer zusammengesetzten Form
In diesem Beispiel wird gezeigt, wie zusammengesetzte Formen mithilfe von <xref:System.Windows.Media.Geometry> Objekten erstellt und mit einem-Element angezeigt werden <xref:System.Windows.Shapes.Path> . Im folgenden Beispiel <xref:System.Windows.Media.LineGeometry> <xref:System.Windows.Media.EllipseGeometry> werden, und mit einem verwendet, <xref:System.Windows.Media.RectangleGeometry> <xref:System.Windows.Media.GeometryGroup> um eine zusammengesetzte Form zu erstellen. Die Geometrien werden dann mit einem- <xref:System.Windows.Shapes.Path> Element gezeichnet.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[GeometrySample#19](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#19)]  
  
 [!code-csharp[GeometriesMiscSnippets_procedural_snip#CompositeShapeCodeExampleInline1](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometriesMiscSnippets_procedural_snip/CSharp/CompositeShapeExample.cs#compositeshapecodeexampleinline1)]
 [!code-vb[GeometriesMiscSnippets_procedural_snip#CompositeShapeCodeExampleInline1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/GeometriesMiscSnippets_procedural_snip/visualbasic/compositeshapeexample.vb#compositeshapecodeexampleinline1)]  
  
 Die folgende Abbildung zeigt die im vorherigen Beispiel erstellte Form.  
  
 ![Eine zusammengesetzte Geometrie, die mit einer GeometryGroup erstellt wird](./media/wcpsdk-graphicsmm-compositegeometryexample1.jpg "wcpsdk_graphicsmm_compositegeometryexample1")  
Zusammengesetzte Geometrie  
  
 Komplexere Formen (z. b. Polygone und Formen mit gekrümmten Segmenten) können mithilfe von erstellt werden <xref:System.Windows.Media.PathGeometry> . Ein Beispiel, das zeigt, wie eine Form mithilfe <xref:System.Windows.Media.PathGeometry> von erstellt wird, finden Sie unter [Erstellen einer Form mithilfe von PathGeometry](how-to-create-a-shape-by-using-a-pathgeometry.md).  Obwohl in diesem Beispiel eine Form mit einem-Element auf dem Bildschirm gerendert <xref:System.Windows.Shapes.Path> wird, <xref:System.Windows.Media.Geometry> können-Objekte auch verwendet werden, um den Inhalt einer <xref:System.Windows.Media.GeometryDrawing> oder einer zu beschreiben <xref:System.Windows.Media.DrawingContext> . Sie können auch für Clipping-und Treffer Tests verwendet werden.  
  
 Dieses Beispiel ist Teil eines größeren Beispiels. Das vollständige Beispiel finden Sie unter [Beispiel für Geometrien](https://github.com/Microsoft/WPF-Samples/tree/master/Graphics/Geometry).
