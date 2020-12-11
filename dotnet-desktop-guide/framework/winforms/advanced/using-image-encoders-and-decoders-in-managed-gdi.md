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
# <a name="using-image-encoders-and-decoders-in-managed-gdi"></a>Verwenden von Bildencodern und -decodern in Managed GDI+
Der <xref:System.Drawing> -Namespace stellt <xref:System.Drawing.Image> die <xref:System.Drawing.Bitmap> Klassen und zum Speichern und Bearbeiten von Bildern bereit. Mithilfe von Bild Encodern in GDI+ können Sie Bilder aus dem Arbeitsspeicher auf den Datenträger schreiben. Mithilfe von Image-Decodern in GDI+ können Sie Images von einem Datenträger in den Arbeitsspeicher laden. Ein Encoder übersetzt die Daten in einem <xref:System.Drawing.Image> - <xref:System.Drawing.Bitmap> Objekt oder-Objekt in ein festgelegte Datenträger Dateiformat. Ein Decoder übersetzt die Daten in einer Datenträger Datei in das Format, das von den <xref:System.Drawing.Image> -und-Objekten benötigt wird <xref:System.Drawing.Bitmap> .  
  
 GDI+ verfügt über integrierte Encoder und decoderer, die die folgenden Dateitypen unterstützen:  
  
- BMP  
  
- GIF  
  
- JPEG  
  
- PNG  
  
- TIFF  
  
 GDI+ verfügt auch über integrierte decoderer, die die folgenden Dateitypen unterstützen:  
  
- WMF  
  
- EMF  
  
- ICON  
  
 In den folgenden Themen werden Encoder und Decoder ausführlicher erläutert:  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Vorgehensweise: Auflisten installierter Encoder](how-to-list-installed-encoders.md)  
 Hier wird beschrieben, wie Sie die auf einem Computer verfügbaren Encoder auflisten.  
  
 [Vorgehensweise: Auflisten installierter Decoder](how-to-list-installed-decoders.md)  
 Hier wird beschrieben, wie Sie die auf einem Computer verfügbaren Decoder auflisten.  
  
 [Vorgehensweise: Ermitteln der von einem Encoder unterstützten Parameter](how-to-determine-the-parameters-supported-by-an-encoder.md)  
 Beschreibt, wie Sie die auflisten, die <xref:System.Drawing.Imaging.EncoderParameters> von einem Encoder unterstützt wird.  
  
 [Vorgehensweise: Konvertieren eines BMP-Bilds in ein PNG-Bild](how-to-convert-a-bmp-image-to-a-png-image.md)  
 Beschreibt, wie ein Bild in einem anderen Bildformat gespeichert wird.  
  
 [Vorgehensweise: Festlegen der JPEG-Komprimierungsebene](how-to-set-jpeg-compression-level.md)  
 Beschreibt, wie die Qualitätsstufe eines Bilds geändert wird.  
  
## <a name="reference"></a>Referenz  
 <xref:System.Drawing.Image>  
  
 <xref:System.Drawing.Bitmap>  
  
 <xref:System.Drawing.Imaging.ImageCodecInfo>  
  
 <xref:System.Drawing.Imaging.EncoderParameter>  
  
 <xref:System.Drawing.Imaging.Encoder>  
  
## <a name="related-sections"></a>Verwandte Abschnitte  
 [Verwalteter Code in GDI+](about-gdi-managed-code.md)  
  
 [Bilder, Bitmaps und Metadatendateien](images-bitmaps-and-metafiles.md)
