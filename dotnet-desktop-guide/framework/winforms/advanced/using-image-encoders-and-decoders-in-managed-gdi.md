---
title: Verwenden von Bildencodern und -decodern in Managed GDI+
ms.date: 03/30/2017
helpviewer_keywords:
- image encoders [Windows Forms], using
- image decoders [Windows Forms], using
ms.assetid: 0e838ea1-4e7e-4334-b882-ab25df607b8b
ms.openlocfilehash: 8cd66f3ce3da462867da9e23c38b3f6d877c058c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975834"
---
# <a name="using-image-encoders-and-decoders-in-managed-gdi"></a><span data-ttu-id="423dc-102">Verwenden von Bildencodern und -decodern in Managed GDI+</span><span class="sxs-lookup"><span data-stu-id="423dc-102">Using Image Encoders and Decoders in Managed GDI+</span></span>
<span data-ttu-id="423dc-103">Der <xref:System.Drawing> -Namespace stellt <xref:System.Drawing.Image> die <xref:System.Drawing.Bitmap> Klassen und zum Speichern und Bearbeiten von Bildern bereit.</span><span class="sxs-lookup"><span data-stu-id="423dc-103">The <xref:System.Drawing> namespace provides the <xref:System.Drawing.Image> and <xref:System.Drawing.Bitmap> classes for storing and manipulating images.</span></span> <span data-ttu-id="423dc-104">Mithilfe von Bild Encodern in GDI+ können Sie Bilder aus dem Arbeitsspeicher auf den Datenträger schreiben.</span><span class="sxs-lookup"><span data-stu-id="423dc-104">By using image encoders in GDI+, you can write images from memory to disk.</span></span> <span data-ttu-id="423dc-105">Mithilfe von Image-Decodern in GDI+ können Sie Images von einem Datenträger in den Arbeitsspeicher laden.</span><span class="sxs-lookup"><span data-stu-id="423dc-105">By using image decoders in GDI+, you can load images from disk into memory.</span></span> <span data-ttu-id="423dc-106">Ein Encoder übersetzt die Daten in einem <xref:System.Drawing.Image> - <xref:System.Drawing.Bitmap> Objekt oder-Objekt in ein festgelegte Datenträger Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="423dc-106">An encoder translates the data in an <xref:System.Drawing.Image> or <xref:System.Drawing.Bitmap> object into a designated disk file format.</span></span> <span data-ttu-id="423dc-107">Ein Decoder übersetzt die Daten in einer Datenträger Datei in das Format, das von den <xref:System.Drawing.Image> -und-Objekten benötigt wird <xref:System.Drawing.Bitmap> .</span><span class="sxs-lookup"><span data-stu-id="423dc-107">A decoder translates the data in a disk file to the format required by the <xref:System.Drawing.Image> and <xref:System.Drawing.Bitmap> objects.</span></span>  
  
 <span data-ttu-id="423dc-108">GDI+ verfügt über integrierte Encoder und decoderer, die die folgenden Dateitypen unterstützen:</span><span class="sxs-lookup"><span data-stu-id="423dc-108">GDI+ has built-in encoders and decoders that support the following file types:</span></span>  
  
- <span data-ttu-id="423dc-109">BMP</span><span class="sxs-lookup"><span data-stu-id="423dc-109">BMP</span></span>  
  
- <span data-ttu-id="423dc-110">GIF</span><span class="sxs-lookup"><span data-stu-id="423dc-110">GIF</span></span>  
  
- <span data-ttu-id="423dc-111">JPEG</span><span class="sxs-lookup"><span data-stu-id="423dc-111">JPEG</span></span>  
  
- <span data-ttu-id="423dc-112">PNG</span><span class="sxs-lookup"><span data-stu-id="423dc-112">PNG</span></span>  
  
- <span data-ttu-id="423dc-113">TIFF</span><span class="sxs-lookup"><span data-stu-id="423dc-113">TIFF</span></span>  
  
 <span data-ttu-id="423dc-114">GDI+ verfügt auch über integrierte decoderer, die die folgenden Dateitypen unterstützen:</span><span class="sxs-lookup"><span data-stu-id="423dc-114">GDI+ also has built-in decoders that support the following file types:</span></span>  
  
- <span data-ttu-id="423dc-115">WMF</span><span class="sxs-lookup"><span data-stu-id="423dc-115">WMF</span></span>  
  
- <span data-ttu-id="423dc-116">EMF</span><span class="sxs-lookup"><span data-stu-id="423dc-116">EMF</span></span>  
  
- <span data-ttu-id="423dc-117">ICON</span><span class="sxs-lookup"><span data-stu-id="423dc-117">ICON</span></span>  
  
 <span data-ttu-id="423dc-118">In den folgenden Themen werden Encoder und Decoder ausführlicher erläutert:</span><span class="sxs-lookup"><span data-stu-id="423dc-118">The following topics discuss encoders and decoders in more detail:</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="423dc-119">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="423dc-119">In This Section</span></span>  
 [<span data-ttu-id="423dc-120">Vorgehensweise: Auflisten installierter Encoder</span><span class="sxs-lookup"><span data-stu-id="423dc-120">How to: List Installed Encoders</span></span>](how-to-list-installed-encoders.md)  
 <span data-ttu-id="423dc-121">Hier wird beschrieben, wie Sie die auf einem Computer verfügbaren Encoder auflisten.</span><span class="sxs-lookup"><span data-stu-id="423dc-121">Describes how to list the encoders available on a computer.</span></span>  
  
 [<span data-ttu-id="423dc-122">Vorgehensweise: Auflisten installierter Decoder</span><span class="sxs-lookup"><span data-stu-id="423dc-122">How to: List Installed Decoders</span></span>](how-to-list-installed-decoders.md)  
 <span data-ttu-id="423dc-123">Hier wird beschrieben, wie Sie die auf einem Computer verfügbaren Decoder auflisten.</span><span class="sxs-lookup"><span data-stu-id="423dc-123">Describes how to list the decoders available on a computer.</span></span>  
  
 [<span data-ttu-id="423dc-124">Vorgehensweise: Ermitteln der von einem Encoder unterstützten Parameter</span><span class="sxs-lookup"><span data-stu-id="423dc-124">How to: Determine the Parameters Supported by an Encoder</span></span>](how-to-determine-the-parameters-supported-by-an-encoder.md)  
 <span data-ttu-id="423dc-125">Beschreibt, wie Sie die auflisten, die <xref:System.Drawing.Imaging.EncoderParameters> von einem Encoder unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="423dc-125">Describes how to list the <xref:System.Drawing.Imaging.EncoderParameters> supported by an encoder.</span></span>  
  
 [<span data-ttu-id="423dc-126">Vorgehensweise: Konvertieren eines BMP-Bilds in ein PNG-Bild</span><span class="sxs-lookup"><span data-stu-id="423dc-126">How to: Convert a BMP image to a PNG image</span></span>](how-to-convert-a-bmp-image-to-a-png-image.md)  
 <span data-ttu-id="423dc-127">Beschreibt, wie ein Bild in einem anderen Bildformat gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="423dc-127">Describes how to save a image in a different image format.</span></span>  
  
 [<span data-ttu-id="423dc-128">Vorgehensweise: Festlegen der JPEG-Komprimierungsebene</span><span class="sxs-lookup"><span data-stu-id="423dc-128">How to: Set JPEG Compression Level</span></span>](how-to-set-jpeg-compression-level.md)  
 <span data-ttu-id="423dc-129">Beschreibt, wie die Qualitätsstufe eines Bilds geändert wird.</span><span class="sxs-lookup"><span data-stu-id="423dc-129">Describes how to change the quality level of an image.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="423dc-130">Referenz</span><span class="sxs-lookup"><span data-stu-id="423dc-130">Reference</span></span>  
 <xref:System.Drawing.Image>  
  
 <xref:System.Drawing.Bitmap>  
  
 <xref:System.Drawing.Imaging.ImageCodecInfo>  
  
 <xref:System.Drawing.Imaging.EncoderParameter>  
  
 <xref:System.Drawing.Imaging.Encoder>  
  
## <a name="related-sections"></a><span data-ttu-id="423dc-131">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="423dc-131">Related Sections</span></span>  
 [<span data-ttu-id="423dc-132">Verwalteter Code in GDI+</span><span class="sxs-lookup"><span data-stu-id="423dc-132">About GDI+ Managed Code</span></span>](about-gdi-managed-code.md)  
  
 [<span data-ttu-id="423dc-133">Bilder, Bitmaps und Metadatendateien</span><span class="sxs-lookup"><span data-stu-id="423dc-133">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
