---
title: Zeichnen, Positionieren und Klonen von Bildern in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- raster images [Windows Forms]
- images [Windows Forms], positioning
- drawing [Windows Forms], images
- drawing [Windows Forms], raster images
- images [Windows Forms], cloning
- images [Windows Forms], drawing
- GDI+, drawing images
- GDI+, cloning images
- GDI+, positioning images
ms.assetid: 09f0c07a-19c0-43b4-90a2-862a10545ce8
ms.openlocfilehash: b5f98e7bdef9ff8ed0a4cd0e040cb92a31f30503
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975290"
---
# <a name="drawing-positioning-and-cloning-images-in-gdi"></a><span data-ttu-id="ce3f8-102">Zeichnen, Positionieren und Klonen von Bildern in GDI+</span><span class="sxs-lookup"><span data-stu-id="ce3f8-102">Drawing, Positioning, and Cloning Images in GDI+</span></span>
<span data-ttu-id="ce3f8-103">Sie können die <xref:System.Drawing.Bitmap> -Klasse verwenden, um Rasterbilder zu laden und anzuzeigen, und Sie können die <xref:System.Drawing.Imaging.Metafile> -Klasse verwenden, um Vektorbilder zu laden und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ce3f8-103">You can use the <xref:System.Drawing.Bitmap> class to load and display raster images, and you can use the <xref:System.Drawing.Imaging.Metafile> class to load and display vector images.</span></span> <span data-ttu-id="ce3f8-104">Die <xref:System.Drawing.Bitmap> -und- <xref:System.Drawing.Imaging.Metafile> Klassen erben von der- <xref:System.Drawing.Image> Klasse.</span><span class="sxs-lookup"><span data-stu-id="ce3f8-104">The <xref:System.Drawing.Bitmap> and <xref:System.Drawing.Imaging.Metafile> classes inherit from the <xref:System.Drawing.Image> class.</span></span> <span data-ttu-id="ce3f8-105">Zum Anzeigen eines Vektor Bilds benötigen Sie eine Instanz der <xref:System.Drawing.Graphics> -Klasse und eine-Klasse <xref:System.Drawing.Imaging.Metafile> .</span><span class="sxs-lookup"><span data-stu-id="ce3f8-105">To display a vector image, you need an instance of the <xref:System.Drawing.Graphics> class and a <xref:System.Drawing.Imaging.Metafile>.</span></span> <span data-ttu-id="ce3f8-106">Zum Anzeigen eines Raster Bilds benötigen Sie eine Instanz der <xref:System.Drawing.Graphics> -Klasse und eine-Klasse <xref:System.Drawing.Bitmap> .</span><span class="sxs-lookup"><span data-stu-id="ce3f8-106">To display a raster image, you need an instance of the <xref:System.Drawing.Graphics> class and a <xref:System.Drawing.Bitmap>.</span></span> <span data-ttu-id="ce3f8-107">Die Instanz der- <xref:System.Drawing.Graphics> Klasse stellt die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode bereit, die die-oder-Methode <xref:System.Drawing.Imaging.Metafile> <xref:System.Drawing.Bitmap> als Argument empfängt.</span><span class="sxs-lookup"><span data-stu-id="ce3f8-107">The instance of the <xref:System.Drawing.Graphics> class provides the <xref:System.Drawing.Graphics.DrawImage%2A> method, which receives the <xref:System.Drawing.Imaging.Metafile> or <xref:System.Drawing.Bitmap> as an argument.</span></span>  
  
## <a name="file-types-and-cloning"></a><span data-ttu-id="ce3f8-108">Dateitypen und Klonen</span><span class="sxs-lookup"><span data-stu-id="ce3f8-108">File Types and Cloning</span></span>  
 <span data-ttu-id="ce3f8-109">Im folgenden Codebeispiel wird gezeigt, wie ein <xref:System.Drawing.Bitmap> aus dem Datei Climber.jpg erstellt und die Bitmap angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="ce3f8-109">The following code example shows how to construct a <xref:System.Drawing.Bitmap> from the file Climber.jpg and displays the bitmap.</span></span> <span data-ttu-id="ce3f8-110">Der Zielpunkt für die obere linke Ecke des Bilds (10, 10) wird in den zweiten und dritten Parametern angegeben.</span><span class="sxs-lookup"><span data-stu-id="ce3f8-110">The destination point for the upper-left corner of the image, (10, 10), is specified in the second and third parameters.</span></span>  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#11)]  
  
 <span data-ttu-id="ce3f8-111">In der folgenden Abbildung ist das Bild dargestellt.</span><span class="sxs-lookup"><span data-stu-id="ce3f8-111">The following illustration shows the image.</span></span>  
  
 <span data-ttu-id="ce3f8-112">![Bildbeispiel](./media/aboutgdip03-art04.gif "AboutGdip03_Art04")</span><span class="sxs-lookup"><span data-stu-id="ce3f8-112">![Image Sample](./media/aboutgdip03-art04.gif "AboutGdip03_Art04")</span></span>  
  
 <span data-ttu-id="ce3f8-113">Sie können <xref:System.Drawing.Bitmap> Objekte aus einer Vielzahl von Grafikdatei Formaten erstellen: BMP, GIF, JPEG, EXIF, PNG, TIFF und Symbol.</span><span class="sxs-lookup"><span data-stu-id="ce3f8-113">You can construct <xref:System.Drawing.Bitmap> objects from a variety of graphics file formats: BMP, GIF, JPEG, EXIF, PNG, TIFF, and ICON.</span></span>  
  
 <span data-ttu-id="ce3f8-114">Im folgenden Codebeispiel wird gezeigt, wie Sie <xref:System.Drawing.Bitmap> -Objekte aus einer Vielzahl von Dateitypen erstellen und dann die Bitmaps anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ce3f8-114">The following code example shows how to construct <xref:System.Drawing.Bitmap> objects from a variety of file types and then displays the bitmaps.</span></span>  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#12)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#12)]  
  
 <span data-ttu-id="ce3f8-115">Die- <xref:System.Drawing.Bitmap> Klasse stellt eine-Methode bereit, mit der <xref:System.Drawing.Bitmap.Clone%2A> Sie eine Kopie einer vorhandenen erstellen können <xref:System.Drawing.Bitmap> .</span><span class="sxs-lookup"><span data-stu-id="ce3f8-115">The <xref:System.Drawing.Bitmap> class provides a <xref:System.Drawing.Bitmap.Clone%2A> method that you can use to make a copy of an existing <xref:System.Drawing.Bitmap>.</span></span> <span data-ttu-id="ce3f8-116">Die- <xref:System.Drawing.Bitmap.Clone%2A> Methode verfügt über einen Parameter des Quell Rechtecks, mit dem Sie den Teil der ursprünglichen Bitmap angeben können, den Sie kopieren möchten.</span><span class="sxs-lookup"><span data-stu-id="ce3f8-116">The <xref:System.Drawing.Bitmap.Clone%2A> method has a source rectangle parameter that you can use to specify the portion of the original bitmap that you want to copy.</span></span> <span data-ttu-id="ce3f8-117">Im folgenden Codebeispiel wird gezeigt, wie ein erstellt <xref:System.Drawing.Bitmap> wird, indem die obere Hälfte eines vorhandenen geklont wird <xref:System.Drawing.Bitmap> .</span><span class="sxs-lookup"><span data-stu-id="ce3f8-117">The following code example shows how to create a <xref:System.Drawing.Bitmap> by cloning the top half of an existing <xref:System.Drawing.Bitmap>.</span></span> <span data-ttu-id="ce3f8-118">Anschließend werden beide Bilder gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ce3f8-118">Then both images are drawn.</span></span>  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#13](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#13)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#13](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#13)]  
  
 <span data-ttu-id="ce3f8-119">Die folgende Abbildung zeigt die beiden Bilder.</span><span class="sxs-lookup"><span data-stu-id="ce3f8-119">The following illustration shows the two images.</span></span>  
  
 <span data-ttu-id="ce3f8-120">![Zuschneiden](./media/aboutgdip03-art05.gif "AboutGdip03_Art05")</span><span class="sxs-lookup"><span data-stu-id="ce3f8-120">![Cropping](./media/aboutgdip03-art05.gif "AboutGdip03_Art05")</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ce3f8-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce3f8-121">See also</span></span>

- [<span data-ttu-id="ce3f8-122">Bilder, Bitmaps und Metadatendateien</span><span class="sxs-lookup"><span data-stu-id="ce3f8-122">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
- [<span data-ttu-id="ce3f8-123">Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen</span><span class="sxs-lookup"><span data-stu-id="ce3f8-123">How to: Create Graphics Objects for Drawing</span></span>](how-to-create-graphics-objects-for-drawing.md)
- [<span data-ttu-id="ce3f8-124">Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien</span><span class="sxs-lookup"><span data-stu-id="ce3f8-124">Working with Images, Bitmaps, Icons, and Metafiles</span></span>](working-with-images-bitmaps-icons-and-metafiles.md)
