---
title: Metadateien in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], metafiles
- GDI+, metafiles
- metafiles
ms.assetid: 51da872c-c783-440f-8bf6-1e580a966c31
ms.openlocfilehash: df54289722cf12bad840722c6eafdaa43279a5dc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975266"
---
# <a name="metafiles-in-gdi"></a>Metadateien in GDI+
GDI+ stellt die <xref:System.Drawing.Imaging.Metafile> -Klasse bereit, sodass Metadateien aufgezeichnet und angezeigt werden können. Eine Metadatei, auch als Vektorbild bezeichnet, ist ein Bild, das als Sequenz von Zeichnungs Befehlen und-Einstellungen gespeichert wird. Die in einem-Objekt aufgezeichneten Befehle und Einstellungen <xref:System.Drawing.Imaging.Metafile> können im Arbeitsspeicher gespeichert oder in einer Datei oder einem Stream gespeichert werden.  
  
## <a name="metafile-formats"></a>Metadateiformate  
 In GDI+ können Metadateien angezeigt werden, die in den folgenden Formaten gespeichert wurden:  
  
- Windows-Metadatendatei (WMF)  
  
- Erweiterte Metadatei (Enhanced Metafile, EMF)  
  
- EMF +  
  
 GDI+ kann Metadateien in den EMF-und EMF +-Formaten aufzeichnen, aber nicht im WMF-Format.  
  
 EMF + ist eine Erweiterung von EMF, mit der GDI+-Datensätze gespeichert werden können. Es gibt zwei Variationen des EMF +-Formats: EMF + only und EMF + Dual. Nur "EMF +"-Metadateien enthalten nur GDI+-Datensätze. Solche Metadatendateien können von GDI+, aber nicht von GDI angezeigt werden. "EMF + Dual Metadateien" enthält GDI+-und GDI-Datensätze. Jeder GDI+-Datensatz in einer EMF + Dual-Metadatei wird mit einem alternativen GDI-Datensatz gekoppelt. Solche Metadatendateien können von GDI+ oder GDI angezeigt werden.  
  
 Im folgenden Beispiel wird eine Metadatei angezeigt, die zuvor als Datei gespeichert wurde. Die Metadatendatei wird mit der linken oberen Ecke bei (100, 100) angezeigt.  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#21)]  
  
## <a name="see-also"></a>Siehe auch

- [Bilder, Bitmaps und Metadatendateien](images-bitmaps-and-metafiles.md)
