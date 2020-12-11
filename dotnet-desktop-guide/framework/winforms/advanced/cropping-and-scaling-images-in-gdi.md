---
title: Zuschneiden und Skalieren von Bildern in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- GDI+, scaling images
- GDI+, cropping images
- images [Windows Forms], cropping
- compressing data [Windows Forms], images
- images [Windows Forms], expansion
- images [Windows Forms], scaling
- rectangles [Windows Forms], source
- rectangles [Windows Forms], destination
- images [Windows Forms], compression
ms.assetid: ad5daf26-005f-45bc-a2af-e0e97777a21a
ms.openlocfilehash: c3cdb06e99770808461f9266fb5f07df9074149b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975039"
---
# <a name="cropping-and-scaling-images-in-gdi"></a><span data-ttu-id="58f17-102">Zuschneiden und Skalieren von Bildern in GDI+</span><span class="sxs-lookup"><span data-stu-id="58f17-102">Cropping and Scaling Images in GDI+</span></span>
<span data-ttu-id="58f17-103">Sie können die <xref:System.Drawing.Graphics.DrawImage%2A> -Methode der- <xref:System.Drawing.Graphics> Klasse verwenden, um Vektorbilder und Rasterbilder zu zeichnen und zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="58f17-103">You can use the <xref:System.Drawing.Graphics.DrawImage%2A> method of the <xref:System.Drawing.Graphics> class to draw and position vector images and raster images.</span></span> <span data-ttu-id="58f17-104"><xref:System.Drawing.Graphics.DrawImage%2A> ist eine überladene Methode, daher gibt es mehrere Möglichkeiten, Sie mit Argumenten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="58f17-104"><xref:System.Drawing.Graphics.DrawImage%2A> is an overloaded method, so there are several ways you can supply it with arguments.</span></span>  
  
## <a name="drawimage-variations"></a><span data-ttu-id="58f17-105">DrawImage-Variationen</span><span class="sxs-lookup"><span data-stu-id="58f17-105">DrawImage Variations</span></span>  
 <span data-ttu-id="58f17-106">Eine Variation der <xref:System.Drawing.Graphics.DrawImage%2A> -Methode empfängt eine <xref:System.Drawing.Bitmap> und eine <xref:System.Drawing.Rectangle> .</span><span class="sxs-lookup"><span data-stu-id="58f17-106">One variation of the <xref:System.Drawing.Graphics.DrawImage%2A> method receives a <xref:System.Drawing.Bitmap> and a <xref:System.Drawing.Rectangle>.</span></span> <span data-ttu-id="58f17-107">Das Rechteck gibt das Ziel für den Zeichnungs Vorgang an. Das heißt, es gibt das Rechteck an, in dem das Bild gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="58f17-107">The rectangle specifies the destination for the drawing operation; that is, it specifies the rectangle in which to draw the image.</span></span> <span data-ttu-id="58f17-108">Wenn sich die Größe des Ziel Rechtecks von der Größe des ursprünglichen Bilds unterscheidet, wird das Bild so skaliert, dass es an das Ziel Rechteck angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="58f17-108">If the size of the destination rectangle is different from the size of the original image, the image is scaled to fit the destination rectangle.</span></span> <span data-ttu-id="58f17-109">Im folgenden Codebeispiel wird gezeigt, wie Sie das gleiche Bild dreimal zeichnen: einmal ohne Skalierung, einmal mit einer Erweiterung und einmal mit einer Komprimierung:</span><span class="sxs-lookup"><span data-stu-id="58f17-109">The following code example shows how to draw the same image three times: once with no scaling, once with an expansion, and once with a compression:</span></span>  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#31)]  
  
 <span data-ttu-id="58f17-110">Die folgende Abbildung zeigt die drei Abbildungen.</span><span class="sxs-lookup"><span data-stu-id="58f17-110">The following illustration shows the three pictures.</span></span>  
  
 <span data-ttu-id="58f17-111">![Skalieren](./media/aboutgdip03-art06.gif "AboutGdip03_Art06")</span><span class="sxs-lookup"><span data-stu-id="58f17-111">![Scaling](./media/aboutgdip03-art06.gif "AboutGdip03_Art06")</span></span>  
  
 <span data-ttu-id="58f17-112">Einige Variationen der <xref:System.Drawing.Graphics.DrawImage%2A> Methode verfügen über einen Quell Rechteck Parameter sowie einen Parameter für einen Ziel Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="58f17-112">Some variations of the <xref:System.Drawing.Graphics.DrawImage%2A> method have a source-rectangle parameter as well as a destination-rectangle parameter.</span></span> <span data-ttu-id="58f17-113">Der Source-Rechteck-Parameter gibt den Teil des zu zeichnenden ursprünglichen Bilds an.</span><span class="sxs-lookup"><span data-stu-id="58f17-113">The source-rectangle parameter specifies the portion of the original image to draw.</span></span> <span data-ttu-id="58f17-114">Das Ziel Rechteck gibt das Rechteck an, in dem dieser Teil des Bilds gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="58f17-114">The destination rectangle specifies the rectangle in which to draw that portion of the image.</span></span> <span data-ttu-id="58f17-115">Wenn sich die Größe des Ziel Rechtecks von der Größe des Quell Rechtecks unterscheidet, wird das Bild so skaliert, dass es an das Ziel Rechteck angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="58f17-115">If the size of the destination rectangle is different from the size of the source rectangle, the picture is scaled to fit the destination rectangle.</span></span>  
  
 <span data-ttu-id="58f17-116">Im folgenden Codebeispiel wird gezeigt, wie ein <xref:System.Drawing.Bitmap> aus dem Datei Runner.jpg erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="58f17-116">The following code example shows how to construct a <xref:System.Drawing.Bitmap> from the file Runner.jpg.</span></span> <span data-ttu-id="58f17-117">Das gesamte Bild wird ohne Skalierung bei (0,0) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="58f17-117">The entire image is drawn with no scaling at (0, 0).</span></span> <span data-ttu-id="58f17-118">Anschließend wird ein kleiner Teil des Bilds zweimal gezeichnet: einmal mit einer Komprimierung und einmal mit einer Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="58f17-118">Then a small portion of the image is drawn twice: once with a compression and once with an expansion.</span></span>  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#32](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#32)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#32](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#32)]  
  
 <span data-ttu-id="58f17-119">Die folgende Abbildung zeigt das nicht skalierte Bild und die komprimierten und erweiterten Bild Teile.</span><span class="sxs-lookup"><span data-stu-id="58f17-119">The following illustration shows the unscaled image, and the compressed and expanded image portions.</span></span>  
  
 <span data-ttu-id="58f17-120">![Zuschneiden und Skalieren](./media/aboutgdip03-art07.gif "AboutGdip03_Art07")</span><span class="sxs-lookup"><span data-stu-id="58f17-120">![Cropping and Scaling](./media/aboutgdip03-art07.gif "AboutGdip03_Art07")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="58f17-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58f17-121">See also</span></span>

- [<span data-ttu-id="58f17-122">Bilder, Bitmaps und Metadatendateien</span><span class="sxs-lookup"><span data-stu-id="58f17-122">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
- [<span data-ttu-id="58f17-123">Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien</span><span class="sxs-lookup"><span data-stu-id="58f17-123">Working with Images, Bitmaps, Icons, and Metafiles</span></span>](working-with-images-bitmaps-icons-and-metafiles.md)
