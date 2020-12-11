---
title: Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien
ms.date: 03/30/2017
helpviewer_keywords:
- metafiles [Windows Forms], working with
- examples [Windows Forms], bitmaps
- examples [Windows Forms], images
- bitmaps [Windows Forms], working with
- images [Windows Forms], working with
- examples [Windows Forms], metafiles
ms.assetid: a626d701-bd99-4fd8-b92f-7b8f794e042b
ms.openlocfilehash: 8c778018a2d78fbec67a3bf41b5cbaa8e4bfb606
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975810"
---
# <a name="working-with-images-bitmaps-icons-and-metafiles"></a><span data-ttu-id="7bd52-102">Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien</span><span class="sxs-lookup"><span data-stu-id="7bd52-102">Working with Images, Bitmaps, Icons, and Metafiles</span></span>
<span data-ttu-id="7bd52-103">GDI+ stellt die `Bitmap` -Klasse zum Arbeiten mit Rasterbildern und die- `Metafile` Klasse zum Arbeiten mit Vektorbildern bereit.</span><span class="sxs-lookup"><span data-stu-id="7bd52-103">GDI+ provides the `Bitmap` class for working with raster images and the `Metafile` class for working with vector images.</span></span> <span data-ttu-id="7bd52-104">Sowohl die `Bitmap`-Klasse als auch die `Metafile`-Klasse erben von der `Image`-Klasse.</span><span class="sxs-lookup"><span data-stu-id="7bd52-104">The `Bitmap` and the `Metafile` classes both inherit from the `Image` class.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7bd52-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7bd52-105">In This Section</span></span>  
 [<span data-ttu-id="7bd52-106">Vorgehensweise: Zeichnen einer vorhandenen Bitmap auf dem Bildschirm</span><span class="sxs-lookup"><span data-stu-id="7bd52-106">How to: Draw an Existing Bitmap to the Screen</span></span>](how-to-draw-an-existing-bitmap-to-the-screen.md)  
 <span data-ttu-id="7bd52-107">Beschreibt das Laden und Zeichnen von Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="7bd52-107">Describes how to load and draw bitmaps.</span></span>  
  
 [<span data-ttu-id="7bd52-108">Vorgehensweise: Laden und Anzeigen von Metadateien</span><span class="sxs-lookup"><span data-stu-id="7bd52-108">How to: Load and Display Metafiles</span></span>](how-to-load-and-display-metafiles.md)  
 <span data-ttu-id="7bd52-109">Veranschaulicht das Laden und Zeichnen von Metadateien.</span><span class="sxs-lookup"><span data-stu-id="7bd52-109">Shows how to load and draw metafiles.</span></span>  
  
 [<span data-ttu-id="7bd52-110">Zuschneiden und Skalieren von Bildern in GDI+</span><span class="sxs-lookup"><span data-stu-id="7bd52-110">Cropping and Scaling Images in GDI+</span></span>](cropping-and-scaling-images-in-gdi.md)  
 <span data-ttu-id="7bd52-111">Erläutert das Zuschneiden und Skalieren von Vektor- und Rasterbildern.</span><span class="sxs-lookup"><span data-stu-id="7bd52-111">Explains how to crop and scale vector and raster images.</span></span>  
  
 [<span data-ttu-id="7bd52-112">Vorgehensweise: Drehen, Spiegeln und Neigen von Bildern</span><span class="sxs-lookup"><span data-stu-id="7bd52-112">How to: Rotate, Reflect, and Skew Images</span></span>](how-to-rotate-reflect-and-skew-images.md)  
 <span data-ttu-id="7bd52-113">Beschreibt das Zeichnen gedrehter, gespiegelter und gezerrter Bilder.</span><span class="sxs-lookup"><span data-stu-id="7bd52-113">Describes how to draw rotated, reflected and skewed images.</span></span>  
  
 [<span data-ttu-id="7bd52-114">Gewusst wie: Verwenden des Interpolations Modus zum Steuern der Bildqualität während der Skalierung</span><span class="sxs-lookup"><span data-stu-id="7bd52-114">How to: Use Interpolation Mode to Control Image Quality During Scaling</span></span>](how-to-use-interpolation-mode-to-control-image-quality-during-scaling.md)  
 <span data-ttu-id="7bd52-115">Veranschaulicht, wie die <xref:System.Drawing.Drawing2D.InterpolationMode>-Enumeration verwendet wird, um die Bildqualität zu ändern.</span><span class="sxs-lookup"><span data-stu-id="7bd52-115">Shows how to use the <xref:System.Drawing.Drawing2D.InterpolationMode> enumeration to change image quality.</span></span>  
  
 [<span data-ttu-id="7bd52-116">Vorgehensweise: Erstellen von Miniaturbildern</span><span class="sxs-lookup"><span data-stu-id="7bd52-116">How to: Create Thumbnail Images</span></span>](how-to-create-thumbnail-images.md)  
 <span data-ttu-id="7bd52-117">Beschreibt das Erstellen von Miniaturbildern.</span><span class="sxs-lookup"><span data-stu-id="7bd52-117">Describes how to create thumbnail images.</span></span>  
  
 [<span data-ttu-id="7bd52-118">Vorgehensweise: Verbessern der Leistung durch das Vermeiden der automatischen Skalierung</span><span class="sxs-lookup"><span data-stu-id="7bd52-118">How to: Improve Performance by Avoiding Automatic Scaling</span></span>](how-to-improve-performance-by-avoiding-automatic-scaling.md)  
 <span data-ttu-id="7bd52-119">Erläutert das Zeichnen eines Bildes ohne automatische Skalierung.</span><span class="sxs-lookup"><span data-stu-id="7bd52-119">Explains how to draw an image without automatic scaling.</span></span>  
  
 [<span data-ttu-id="7bd52-120">Vorgehensweise: Lesen von Bildmetadaten</span><span class="sxs-lookup"><span data-stu-id="7bd52-120">How to: Read Image Metadata</span></span>](how-to-read-image-metadata.md)  
 <span data-ttu-id="7bd52-121">Beschreibt das Lesen von Metadaten aus einem Bild.</span><span class="sxs-lookup"><span data-stu-id="7bd52-121">Describes how to read metadata from an image.</span></span>  
  
 [<span data-ttu-id="7bd52-122">Vorgehensweise: Erstellen einer Bitmap zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="7bd52-122">How to: Create a Bitmap at Run Time</span></span>](how-to-create-a-bitmap-at-run-time.md)  
 <span data-ttu-id="7bd52-123">Veranschaulicht das Zeichnen einer Bitmap zur Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="7bd52-123">Shows how to draw a bitmap at runtime.</span></span>  
  
 [<span data-ttu-id="7bd52-124">Vorgehensweise: Extrahieren eines mit einer Datei verknüpften Symbols in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7bd52-124">How to: Extract the Icon Associated with a File in Windows Forms</span></span>](how-to-extract-the-icon-associated-with-a-file-in-windows-forms.md)  
 <span data-ttu-id="7bd52-125">Beschreibt, wie ein Symbol extrahiert wird, das eine eingebettete Ressource einer Datei ist.</span><span class="sxs-lookup"><span data-stu-id="7bd52-125">Describes how to extract an icon that is an embedded resource of a file.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="7bd52-126">Verweis</span><span class="sxs-lookup"><span data-stu-id="7bd52-126">Reference</span></span>  
 <xref:System.Drawing.Image>  
 <span data-ttu-id="7bd52-127">Beschreibt diese Klasse und enthält Links zu allen Membern.</span><span class="sxs-lookup"><span data-stu-id="7bd52-127">Describes this class and has links to all of its members.</span></span>  
  
 <xref:System.Drawing.Imaging.Metafile>  
 <span data-ttu-id="7bd52-128">Beschreibt diese Klasse und enthält Links zu allen Membern.</span><span class="sxs-lookup"><span data-stu-id="7bd52-128">Describes this class and has links to all of its members.</span></span>  
  
 <xref:System.Drawing.Bitmap>  
 <span data-ttu-id="7bd52-129">Beschreibt diese Klasse und enthält Links zu allen Membern.</span><span class="sxs-lookup"><span data-stu-id="7bd52-129">Describes this class and has links to all of its members.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="7bd52-130">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="7bd52-130">Related Sections</span></span>  
 [<span data-ttu-id="7bd52-131">Bilder, Bitmaps und Metadatendateien</span><span class="sxs-lookup"><span data-stu-id="7bd52-131">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)  
 <span data-ttu-id="7bd52-132">Enthält Links zu Themen, in denen andere Typen von Bitmaps sowie deren Bearbeitung in Anwendungen erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="7bd52-132">Contains links to topics that discuss different types of bitmaps and manipulating them in your applications.</span></span>
