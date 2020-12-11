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
# <a name="metafiles-in-gdi"></a><span data-ttu-id="a1801-102">Metadateien in GDI+</span><span class="sxs-lookup"><span data-stu-id="a1801-102">Metafiles in GDI+</span></span>
<span data-ttu-id="a1801-103">GDI+ stellt die <xref:System.Drawing.Imaging.Metafile> -Klasse bereit, sodass Metadateien aufgezeichnet und angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="a1801-103">GDI+ provides the <xref:System.Drawing.Imaging.Metafile> class so that you can record and display metafiles.</span></span> <span data-ttu-id="a1801-104">Eine Metadatei, auch als Vektorbild bezeichnet, ist ein Bild, das als Sequenz von Zeichnungs Befehlen und-Einstellungen gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="a1801-104">A metafile, also called a vector image, is an image that is stored as a sequence of drawing commands and settings.</span></span> <span data-ttu-id="a1801-105">Die in einem-Objekt aufgezeichneten Befehle und Einstellungen <xref:System.Drawing.Imaging.Metafile> können im Arbeitsspeicher gespeichert oder in einer Datei oder einem Stream gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="a1801-105">The commands and settings recorded in a <xref:System.Drawing.Imaging.Metafile> object can be stored in memory or saved to a file or stream.</span></span>  
  
## <a name="metafile-formats"></a><span data-ttu-id="a1801-106">Metadateiformate</span><span class="sxs-lookup"><span data-stu-id="a1801-106">Metafile Formats</span></span>  
 <span data-ttu-id="a1801-107">In GDI+ können Metadateien angezeigt werden, die in den folgenden Formaten gespeichert wurden:</span><span class="sxs-lookup"><span data-stu-id="a1801-107">GDI+ can display metafiles that have been stored in the following formats:</span></span>  
  
- <span data-ttu-id="a1801-108">Windows-Metadatendatei (WMF)</span><span class="sxs-lookup"><span data-stu-id="a1801-108">Windows Metafile (WMF)</span></span>  
  
- <span data-ttu-id="a1801-109">Erweiterte Metadatei (Enhanced Metafile, EMF)</span><span class="sxs-lookup"><span data-stu-id="a1801-109">Enhanced Metafile (EMF)</span></span>  
  
- <span data-ttu-id="a1801-110">EMF +</span><span class="sxs-lookup"><span data-stu-id="a1801-110">EMF+</span></span>  
  
 <span data-ttu-id="a1801-111">GDI+ kann Metadateien in den EMF-und EMF +-Formaten aufzeichnen, aber nicht im WMF-Format.</span><span class="sxs-lookup"><span data-stu-id="a1801-111">GDI+ can record metafiles in the EMF and EMF+ formats, but not in the WMF format.</span></span>  
  
 <span data-ttu-id="a1801-112">EMF + ist eine Erweiterung von EMF, mit der GDI+-Datensätze gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="a1801-112">EMF+ is an extension to EMF that allows GDI+ records to be stored.</span></span> <span data-ttu-id="a1801-113">Es gibt zwei Variationen des EMF +-Formats: EMF + only und EMF + Dual.</span><span class="sxs-lookup"><span data-stu-id="a1801-113">There are two variations on the EMF+ format: EMF+ Only and EMF+ Dual.</span></span> <span data-ttu-id="a1801-114">Nur "EMF +"-Metadateien enthalten nur GDI+-Datensätze.</span><span class="sxs-lookup"><span data-stu-id="a1801-114">EMF+ Only metafiles contain only GDI+ records.</span></span> <span data-ttu-id="a1801-115">Solche Metadatendateien können von GDI+, aber nicht von GDI angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a1801-115">Such metafiles can be displayed by GDI+ but not by GDI.</span></span> <span data-ttu-id="a1801-116">"EMF + Dual Metadateien" enthält GDI+-und GDI-Datensätze.</span><span class="sxs-lookup"><span data-stu-id="a1801-116">EMF+ Dual metafiles contain GDI+ and GDI records.</span></span> <span data-ttu-id="a1801-117">Jeder GDI+-Datensatz in einer EMF + Dual-Metadatei wird mit einem alternativen GDI-Datensatz gekoppelt.</span><span class="sxs-lookup"><span data-stu-id="a1801-117">Each GDI+ record in an EMF+ Dual metafile is paired with an alternate GDI record.</span></span> <span data-ttu-id="a1801-118">Solche Metadatendateien können von GDI+ oder GDI angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a1801-118">Such metafiles can be displayed by GDI+ or by GDI.</span></span>  
  
 <span data-ttu-id="a1801-119">Im folgenden Beispiel wird eine Metadatei angezeigt, die zuvor als Datei gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="a1801-119">The following example displays a metafile that was previously saved as a file.</span></span> <span data-ttu-id="a1801-120">Die Metadatendatei wird mit der linken oberen Ecke bei (100, 100) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a1801-120">The metafile is displayed with its upper-left corner at (100, 100).</span></span>  
  
 [!code-csharp[System.Drawing.ImagesBitmapsMetafiles#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.ImagesBitmapsMetafiles#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ImagesBitmapsMetafiles/VB/Class1.vb#21)]  
  
## <a name="see-also"></a><span data-ttu-id="a1801-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1801-121">See also</span></span>

- [<span data-ttu-id="a1801-122">Bilder, Bitmaps und Metadatendateien</span><span class="sxs-lookup"><span data-stu-id="a1801-122">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
