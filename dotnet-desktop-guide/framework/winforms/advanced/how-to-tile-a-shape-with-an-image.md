---
title: 'Vorgehensweise: Anordnen einer Form neben bzw. unter einem Bild'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- texture brushes [Windows Forms], tiling images with
- images [Windows Forms], filling shapes with
- shapes [Windows Forms], tiling with images
- bitmaps [Windows Forms], filling shapes with
ms.assetid: 6d407891-6e5c-4495-a546-3da5604e9fb8
ms.openlocfilehash: a906db44a548361df2822efa24d1dd1849cb5a24
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975865"
---
# <a name="how-to-tile-a-shape-with-an-image"></a>Vorgehensweise: Anordnen einer Form neben bzw. unter einem Bild
Ebenso wie Kacheln nebeneinander nebeneinander angeordnet werden können, können rechteckige Bilder nebeneinander platziert werden, um eine Form zu füllen (Kachel). Um das Innere einer Form zu Kacheln, verwenden Sie einen Textur Pinsel. Wenn Sie ein- <xref:System.Drawing.TextureBrush> Objekt erstellen, ist eines der Argumente, die Sie an den-Konstruktor übergeben, ein- <xref:System.Drawing.Image> Objekt. Wenn Sie den Textur Pinsel verwenden, um das Innere einer Form zu zeichnen, wird die Form mit wiederholten Kopien dieses Bilds aufgefüllt.  
  
 Die Wrap Mode-Eigenschaft des- <xref:System.Drawing.TextureBrush> Objekts bestimmt, wie das Bild ausgerichtet wird, da es in einem rechteckigen Raster wiederholt wird. Sie können festlegen, dass alle Kacheln im Raster die gleiche Ausrichtung aufweisen, oder Sie können das Bild von einer Raster Position zum nächsten kippen lassen. Die flippingoptionen können horizontal, vertikal oder beides sein. In den folgenden Beispielen wird das Ticken mit unterschiedlichen Arten von kippen veranschaulicht.  
  
### <a name="to-tile-an-image"></a>So Kacheln Sie ein Bild  
  
- In diesem Beispiel wird das folgende 75 × 75-Bild zum Kacheln eines 200 × 200-Rechtecks verwendet.  
  
 ![Das Kachel Bild, das ein rotes Haus und eine Baumstruktur anzeigt.](./media/how-to-tile-a-shape-with-an-image/rectangle-tile-200x200.gif)  
  
- In der folgenden Abbildung wird gezeigt, wie das Rechteck mit dem Bild gekachelt wird. Beachten Sie, dass alle Kacheln die gleiche Ausrichtung aufweisen. Es gibt kein Flipping.  
  
 ![Ein Rechteck mit dem Bild, das die gleiche Ausrichtung für alle Kacheln verwendet.](./media/how-to-tile-a-shape-with-an-image/rectangle-tiled-image-no-flip.gif)  
  
 [!code-csharp[System.Drawing.UsingABrush#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.UsingABrush#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#31)]  
  
### <a name="to-flip-an-image-horizontally-while-tiling"></a>So kippen Sie ein Bild beim ticken horizontal  
  
- In diesem Beispiel wird das gleiche 75 × 75-Image zum Auffüllen eines 200 × 200-Rechtecks verwendet. Der Umbruch Modus ist so festgelegt, dass das Bild horizontal gekippt wird. In der folgenden Abbildung wird gezeigt, wie das Rechteck mit dem Bild gekachelt wird. Beachten Sie, dass das Bild beim Wechsel von einer Kachel zum nächsten in einer bestimmten Zeile horizontal gekippt wird.  
  
 ![Ein Rechteck, das mit dem Bild horizontal geflippt wird.](./media/how-to-tile-a-shape-with-an-image/rectangle-tiled-image-horizontal-flip.gif)  
  
 [!code-csharp[System.Drawing.UsingABrush#32](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#32)]
 [!code-vb[System.Drawing.UsingABrush#32](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#32)]  
  
### <a name="to-flip-an-image-vertically-while-tiling"></a>So kippen Sie ein Bild beim ticken vertikal  
  
- In diesem Beispiel wird das gleiche 75 × 75-Image zum Auffüllen eines 200 × 200-Rechtecks verwendet. Der Umbruch Modus ist so festgelegt, dass das Bild vertikal gedreht wird.  
  
     [!code-csharp[System.Drawing.UsingABrush#33](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#33)]
     [!code-vb[System.Drawing.UsingABrush#33](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#33)]  
  
### <a name="to-flip-an-image-horizontally-and-vertically-while-tiling"></a>So kippen Sie ein Bild beim ticken horizontal und vertikal  
  
- In diesem Beispiel wird das gleiche 75 × 75-Image für die Kachel eines 200 × 200-Rechtecks verwendet. Der Umbruch Modus ist so festgelegt, dass das Bild sowohl horizontal als auch vertikal gekippt wird. In der folgenden Abbildung wird gezeigt, wie das Rechteck durch das Bild gekachelt wird. Beachten Sie, dass beim Wechsel von einer Kachel zum nächsten in einer bestimmten Zeile das Bild horizontal gekippt wird, und wenn Sie in einer bestimmten Spalte von einer Kachel zum nächsten wechseln, wird das Bild vertikal gekippt.  
  
 ![Ein Rechteck, das bei horizontaler und vertikaler geflipptem Bild angezeigt wird.](./media/how-to-tile-a-shape-with-an-image/rectangle-tiled-image-horizontal-vertical-flip.gif)  
  
 [!code-csharp[System.Drawing.UsingABrush#34](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#34)]
 [!code-vb[System.Drawing.UsingABrush#34](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#34)]  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden eines Pinsels zum Ausfüllen von Formen](using-a-brush-to-fill-shapes.md)
