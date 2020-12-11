---
title: Polygone in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- polygons
- drawing [Windows Forms], polygons
- GDI+, polygons
ms.assetid: a72213d2-d69a-4c2b-a75c-be7b20390c13
ms.openlocfilehash: 2b1e3d387e4d056d9187c54dcef560544206c370
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975253"
---
# <a name="polygons-in-gdi"></a>Polygone in GDI+
Ein Polygon ist eine geschlossene Form mit drei oder mehr geraden Seiten. Ein Dreieck ist beispielsweise ein Polygon mit drei Seiten, ein Rechteck ist ein Polygon mit vier Seiten, und ein Pentagon ist ein Polygon mit fünf Seiten. Die folgende Abbildung zeigt mehrere Polygone.  
  
 ![Polygone](./media/aboutgdip02-art07.gif "Aboutgdip02_art07")  
  
## <a name="drawing-a-polygon"></a>Zeichnen eines Polygons  
 Zum Zeichnen eines Polygons benötigen Sie ein <xref:System.Drawing.Graphics> -Objekt, ein <xref:System.Drawing.Pen> -Objekt und ein Array von- <xref:System.Drawing.Point> Objekten (oder <xref:System.Drawing.PointF> ). Das- <xref:System.Drawing.Graphics> Objekt stellt die- <xref:System.Drawing.Graphics.DrawPolygon%2A> Methode bereit. Das <xref:System.Drawing.Pen> Objekt speichert Attribute, z. b. "width" und "Color", der zum Rendering des Polygons verwendeten Zeile, und das Array von- <xref:System.Drawing.Point> Objekten speichert die Punkte, die durch gerade Linien verbunden werden sollen. Das <xref:System.Drawing.Pen> -Objekt und das Array von- <xref:System.Drawing.Point> Objekten werden als Argumente an die-Methode übermittelt <xref:System.Drawing.Graphics.DrawPolygon%2A> . Im folgenden Beispiel wird ein dreiseitiges Polygon gezeichnet. Beachten Sie, dass es nur drei Punkte in gibt `myPointArray` : (0,0), (50, 30) und (30, 60). Die- <xref:System.Drawing.Graphics.DrawPolygon%2A> Methode schließt das Polygon automatisch durch Zeichnen einer Linie von (30, 60) zurück zum Startpunkt (0,0).  
  
 [!code-csharp[LinesCurvesAndShapes#111](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#111)]
 [!code-vb[LinesCurvesAndShapes#111](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#111)]  
  
 Die folgende Abbildung zeigt das Polygon.  
  
 ![Polygon](./media/aboutgdip02-art08.gif "Aboutgdip02_art08")  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Graphics?displayProperty=nameWithType>
- <xref:System.Drawing.Pen?displayProperty=nameWithType>
- [Linien, Kurven und Formen](lines-curves-and-shapes.md)
- [Vorgehensweise: Erstellen eines Stifts](how-to-create-a-pen.md)
