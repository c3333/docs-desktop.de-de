---
title: 'Vorgehensweise: Verwenden des Interpolationsmodus zum Steuern der Bildqualität während der Skalierung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- interpolation mode [Windows Forms], controlling image quality
- images [Windows Forms], scaling
- images [Windows Forms], controlling quality
ms.assetid: fde9bccf-8aa5-4b0d-ba4b-788740627b02
ms.openlocfilehash: ab0ff93b3ee26467c0de448efd31b698167f95c2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976101"
---
# <a name="how-to-use-interpolation-mode-to-control-image-quality-during-scaling"></a><span data-ttu-id="612aa-102">Vorgehensweise: Verwenden des Interpolationsmodus zum Steuern der Bildqualität während der Skalierung</span><span class="sxs-lookup"><span data-stu-id="612aa-102">How to: Use Interpolation Mode to Control Image Quality During Scaling</span></span>
<span data-ttu-id="612aa-103">Der Interpolations Modus eines- <xref:System.Drawing.Graphics> Objekts wirkt sich auf die Art der Skalierung (Streckung und Verkleinerung) von GDI+ aus.</span><span class="sxs-lookup"><span data-stu-id="612aa-103">The interpolation mode of a <xref:System.Drawing.Graphics> object influences the way GDI+ scales (stretches and shrinks) images.</span></span> <span data-ttu-id="612aa-104">Die- <xref:System.Drawing.Drawing2D.InterpolationMode> Enumeration definiert mehrere Interpolations Modi, von denen einige in der folgenden Liste aufgeführt sind:</span><span class="sxs-lookup"><span data-stu-id="612aa-104">The <xref:System.Drawing.Drawing2D.InterpolationMode> enumeration defines several interpolation modes, some of which are shown in the following list:</span></span>  
  
- <xref:System.Drawing.Drawing2D.InterpolationMode.NearestNeighbor>  
  
- <xref:System.Drawing.Drawing2D.InterpolationMode.Bilinear>  
  
- <xref:System.Drawing.Drawing2D.InterpolationMode.HighQualityBilinear>  
  
- <xref:System.Drawing.Drawing2D.InterpolationMode.Bicubic>  
  
- <xref:System.Drawing.Drawing2D.InterpolationMode.HighQualityBicubic>  
  
 <span data-ttu-id="612aa-105">Zum Strecken eines Bilds muss jedes Pixel im ursprünglichen Bild einer Gruppe von Pixeln im größeren Bild zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="612aa-105">To stretch an image, each pixel in the original image must be mapped to a group of pixels in the larger image.</span></span> <span data-ttu-id="612aa-106">Zum Verkleinern eines Bilds müssen Gruppen von Pixeln im ursprünglichen Bild einem einzelnen Pixel im kleineren Bild zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="612aa-106">To shrink an image, groups of pixels in the original image must be mapped to single pixels in the smaller image.</span></span> <span data-ttu-id="612aa-107">Die Effektivität der Algorithmen, die diese Zuordnungen durchführen, bestimmt die Qualität eines skalierten Bilds.</span><span class="sxs-lookup"><span data-stu-id="612aa-107">The effectiveness of the algorithms that perform these mappings determines the quality of a scaled image.</span></span> <span data-ttu-id="612aa-108">Algorithmen, die skalierbare Images höherer Qualität liefern, erfordern tendenziell mehr Verarbeitungszeit.</span><span class="sxs-lookup"><span data-stu-id="612aa-108">Algorithms that produce higher-quality scaled images tend to require more processing time.</span></span> <span data-ttu-id="612aa-109">In der vorangehenden Liste <xref:System.Drawing.Drawing2D.InterpolationMode.NearestNeighbor> ist der Modus der niedrigsten Qualität und <xref:System.Drawing.Drawing2D.InterpolationMode.HighQualityBicubic> der Modus mit der höchsten Qualität.</span><span class="sxs-lookup"><span data-stu-id="612aa-109">In the preceding list, <xref:System.Drawing.Drawing2D.InterpolationMode.NearestNeighbor> is the lowest-quality mode and <xref:System.Drawing.Drawing2D.InterpolationMode.HighQualityBicubic> is the highest-quality mode.</span></span>  
  
 <span data-ttu-id="612aa-110">Um den Interpolations Modus festzulegen, weisen Sie einen der Member der- <xref:System.Drawing.Drawing2D.InterpolationMode> Enumeration der- <xref:System.Drawing.Graphics.InterpolationMode%2A> Eigenschaft eines-Objekts zu <xref:System.Drawing.Graphics> .</span><span class="sxs-lookup"><span data-stu-id="612aa-110">To set the interpolation mode, assign one of the members of the <xref:System.Drawing.Drawing2D.InterpolationMode> enumeration to the <xref:System.Drawing.Graphics.InterpolationMode%2A> property of a <xref:System.Drawing.Graphics> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="612aa-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="612aa-111">Example</span></span>  
 <span data-ttu-id="612aa-112">Im folgenden Beispiel wird ein Bild gezeichnet und dann mit drei verschiedenen Interpolations Modi verkleinert.</span><span class="sxs-lookup"><span data-stu-id="612aa-112">The following example draws an image and then shrinks the image with three different interpolation modes.</span></span>  
  
 <span data-ttu-id="612aa-113">Die folgende Abbildung zeigt das ursprüngliche Bild und die drei kleineren Bilder.</span><span class="sxs-lookup"><span data-stu-id="612aa-113">The following illustration shows the original image and the three smaller images.</span></span>  
  
 ![Screenshot, der ein Bild mit unterschiedlichen Interpolations Einstellungen anzeigt.](./media/how-to-use-interpolation-mode-to-control-image-quality-during-scaling/varied-interpolation-settings.png)  
  
 [!code-csharp[System.Drawing.WorkingWithImages#81](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#81)]
 [!code-vb[System.Drawing.WorkingWithImages#81](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#81)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="612aa-115">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="612aa-115">Compiling the Code</span></span>  
 <span data-ttu-id="612aa-116">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="612aa-116">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="612aa-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="612aa-117">See also</span></span>

- [<span data-ttu-id="612aa-118">Bilder, Bitmaps und Metadatendateien</span><span class="sxs-lookup"><span data-stu-id="612aa-118">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
- [<span data-ttu-id="612aa-119">Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien</span><span class="sxs-lookup"><span data-stu-id="612aa-119">Working with Images, Bitmaps, Icons, and Metafiles</span></span>](working-with-images-bitmaps-icons-and-metafiles.md)
