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
# <a name="how-to-tile-a-shape-with-an-image"></a><span data-ttu-id="f1381-102">Vorgehensweise: Anordnen einer Form neben bzw. unter einem Bild</span><span class="sxs-lookup"><span data-stu-id="f1381-102">How to: Tile a Shape with an Image</span></span>
<span data-ttu-id="f1381-103">Ebenso wie Kacheln nebeneinander nebeneinander angeordnet werden können, können rechteckige Bilder nebeneinander platziert werden, um eine Form zu füllen (Kachel).</span><span class="sxs-lookup"><span data-stu-id="f1381-103">Just as tiles can be placed next to each other to cover a floor, rectangular images can be placed next to each other to fill (tile) a shape.</span></span> <span data-ttu-id="f1381-104">Um das Innere einer Form zu Kacheln, verwenden Sie einen Textur Pinsel.</span><span class="sxs-lookup"><span data-stu-id="f1381-104">To tile the interior of a shape, use a texture brush.</span></span> <span data-ttu-id="f1381-105">Wenn Sie ein- <xref:System.Drawing.TextureBrush> Objekt erstellen, ist eines der Argumente, die Sie an den-Konstruktor übergeben, ein- <xref:System.Drawing.Image> Objekt.</span><span class="sxs-lookup"><span data-stu-id="f1381-105">When you construct a <xref:System.Drawing.TextureBrush> object, one of the arguments you pass to the constructor is an <xref:System.Drawing.Image> object.</span></span> <span data-ttu-id="f1381-106">Wenn Sie den Textur Pinsel verwenden, um das Innere einer Form zu zeichnen, wird die Form mit wiederholten Kopien dieses Bilds aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f1381-106">When you use the texture brush to paint the interior of a shape, the shape is filled with repeated copies of this image.</span></span>  
  
 <span data-ttu-id="f1381-107">Die Wrap Mode-Eigenschaft des- <xref:System.Drawing.TextureBrush> Objekts bestimmt, wie das Bild ausgerichtet wird, da es in einem rechteckigen Raster wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="f1381-107">The wrap mode property of the <xref:System.Drawing.TextureBrush> object determines how the image is oriented as it is repeated in a rectangular grid.</span></span> <span data-ttu-id="f1381-108">Sie können festlegen, dass alle Kacheln im Raster die gleiche Ausrichtung aufweisen, oder Sie können das Bild von einer Raster Position zum nächsten kippen lassen.</span><span class="sxs-lookup"><span data-stu-id="f1381-108">You can make all the tiles in the grid have the same orientation, or you can make the image flip from one grid position to the next.</span></span> <span data-ttu-id="f1381-109">Die flippingoptionen können horizontal, vertikal oder beides sein.</span><span class="sxs-lookup"><span data-stu-id="f1381-109">The flipping can be horizontal, vertical, or both.</span></span> <span data-ttu-id="f1381-110">In den folgenden Beispielen wird das Ticken mit unterschiedlichen Arten von kippen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f1381-110">The following examples demonstrate tiling with different types of flipping.</span></span>  
  
### <a name="to-tile-an-image"></a><span data-ttu-id="f1381-111">So Kacheln Sie ein Bild</span><span class="sxs-lookup"><span data-stu-id="f1381-111">To tile an image</span></span>  
  
- <span data-ttu-id="f1381-112">In diesem Beispiel wird das folgende 75 × 75-Bild zum Kacheln eines 200 × 200-Rechtecks verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1381-112">This example uses the following 75×75 image to tile a 200×200 rectangle.</span></span>  
  
 ![Das Kachel Bild, das ein rotes Haus und eine Baumstruktur anzeigt.](./media/how-to-tile-a-shape-with-an-image/rectangle-tile-200x200.gif)  
  
- <span data-ttu-id="f1381-114">In der folgenden Abbildung wird gezeigt, wie das Rechteck mit dem Bild gekachelt wird.</span><span class="sxs-lookup"><span data-stu-id="f1381-114">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="f1381-115">Beachten Sie, dass alle Kacheln die gleiche Ausrichtung aufweisen. Es gibt kein Flipping.</span><span class="sxs-lookup"><span data-stu-id="f1381-115">Note that all tiles have the same orientation; there is no flipping.</span></span>  
  
 ![Ein Rechteck mit dem Bild, das die gleiche Ausrichtung für alle Kacheln verwendet.](./media/how-to-tile-a-shape-with-an-image/rectangle-tiled-image-no-flip.gif)  
  
 [!code-csharp[System.Drawing.UsingABrush#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.UsingABrush#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#31)]  
  
### <a name="to-flip-an-image-horizontally-while-tiling"></a><span data-ttu-id="f1381-117">So kippen Sie ein Bild beim ticken horizontal</span><span class="sxs-lookup"><span data-stu-id="f1381-117">To flip an image horizontally while tiling</span></span>  
  
- <span data-ttu-id="f1381-118">In diesem Beispiel wird das gleiche 75 × 75-Image zum Auffüllen eines 200 × 200-Rechtecks verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1381-118">This example uses the same 75×75 image to fill a 200×200 rectangle.</span></span> <span data-ttu-id="f1381-119">Der Umbruch Modus ist so festgelegt, dass das Bild horizontal gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="f1381-119">The wrap mode is set to flip the image horizontally.</span></span> <span data-ttu-id="f1381-120">In der folgenden Abbildung wird gezeigt, wie das Rechteck mit dem Bild gekachelt wird.</span><span class="sxs-lookup"><span data-stu-id="f1381-120">The following illustration shows how the rectangle is tiled with the image.</span></span> <span data-ttu-id="f1381-121">Beachten Sie, dass das Bild beim Wechsel von einer Kachel zum nächsten in einer bestimmten Zeile horizontal gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="f1381-121">Note that as you move from one tile to the next in a given row, the image is flipped horizontally.</span></span>  
  
 ![Ein Rechteck, das mit dem Bild horizontal geflippt wird.](./media/how-to-tile-a-shape-with-an-image/rectangle-tiled-image-horizontal-flip.gif)  
  
 [!code-csharp[System.Drawing.UsingABrush#32](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#32)]
 [!code-vb[System.Drawing.UsingABrush#32](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#32)]  
  
### <a name="to-flip-an-image-vertically-while-tiling"></a><span data-ttu-id="f1381-123">So kippen Sie ein Bild beim ticken vertikal</span><span class="sxs-lookup"><span data-stu-id="f1381-123">To flip an image vertically while tiling</span></span>  
  
- <span data-ttu-id="f1381-124">In diesem Beispiel wird das gleiche 75 × 75-Image zum Auffüllen eines 200 × 200-Rechtecks verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1381-124">This example uses the same 75×75 image to fill a 200×200 rectangle.</span></span> <span data-ttu-id="f1381-125">Der Umbruch Modus ist so festgelegt, dass das Bild vertikal gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="f1381-125">The wrap mode is set to flip the image vertically.</span></span>  
  
     [!code-csharp[System.Drawing.UsingABrush#33](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#33)]
     [!code-vb[System.Drawing.UsingABrush#33](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#33)]  
  
### <a name="to-flip-an-image-horizontally-and-vertically-while-tiling"></a><span data-ttu-id="f1381-126">So kippen Sie ein Bild beim ticken horizontal und vertikal</span><span class="sxs-lookup"><span data-stu-id="f1381-126">To flip an image horizontally and vertically while tiling</span></span>  
  
- <span data-ttu-id="f1381-127">In diesem Beispiel wird das gleiche 75 × 75-Image für die Kachel eines 200 × 200-Rechtecks verwendet.</span><span class="sxs-lookup"><span data-stu-id="f1381-127">This example uses the same 75×75 image to tile a 200×200 rectangle.</span></span> <span data-ttu-id="f1381-128">Der Umbruch Modus ist so festgelegt, dass das Bild sowohl horizontal als auch vertikal gekippt wird.</span><span class="sxs-lookup"><span data-stu-id="f1381-128">The wrap mode is set to flip the image both horizontally and vertically.</span></span> <span data-ttu-id="f1381-129">In der folgenden Abbildung wird gezeigt, wie das Rechteck durch das Bild gekachelt wird.</span><span class="sxs-lookup"><span data-stu-id="f1381-129">The following illustration shows how the rectangle is tiled by the image.</span></span> <span data-ttu-id="f1381-130">Beachten Sie, dass beim Wechsel von einer Kachel zum nächsten in einer bestimmten Zeile das Bild horizontal gekippt wird, und wenn Sie in einer bestimmten Spalte von einer Kachel zum nächsten wechseln, wird das Bild vertikal gekippt.</span><span class="sxs-lookup"><span data-stu-id="f1381-130">Note that as you move from one tile to the next in a given row, the image is flipped horizontally, and as you move from one tile to the next in a given column, the image is flipped vertically.</span></span>  
  
 ![Ein Rechteck, das bei horizontaler und vertikaler geflipptem Bild angezeigt wird.](./media/how-to-tile-a-shape-with-an-image/rectangle-tiled-image-horizontal-vertical-flip.gif)  
  
 [!code-csharp[System.Drawing.UsingABrush#34](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#34)]
 [!code-vb[System.Drawing.UsingABrush#34](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#34)]  
  
## <a name="see-also"></a><span data-ttu-id="f1381-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1381-132">See also</span></span>

- [<span data-ttu-id="f1381-133">Verwenden eines Pinsels zum Ausfüllen von Formen</span><span class="sxs-lookup"><span data-stu-id="f1381-133">Using a Brush to Fill Shapes</span></span>](using-a-brush-to-fill-shapes.md)
