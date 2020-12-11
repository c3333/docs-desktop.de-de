---
title: 'Vorgehensweise: Zuschneiden und Skalieren von Bildern'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], cropping
- images [Windows Forms], scaling
ms.assetid: 053e3360-bca0-4b25-9afa-0e77a6f17b03
ms.openlocfilehash: 4257431881565f9160f45795111d374cc680dedd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972361"
---
# <a name="how-to-crop-and-scale-images"></a><span data-ttu-id="51af9-102">Vorgehensweise: Zuschneiden und Skalieren von Bildern</span><span class="sxs-lookup"><span data-stu-id="51af9-102">How to: Crop and Scale Images</span></span>
<span data-ttu-id="51af9-103">Die <xref:System.Drawing.Graphics> -Klasse stellt mehrere <xref:System.Drawing.Graphics.DrawImage%2A> Methoden bereit, von denen einige über Quell-und Ziel Rechteck Parameter verfügen, die Sie zum Zuschneiden und Skalieren von Bildern verwenden können.</span><span class="sxs-lookup"><span data-stu-id="51af9-103">The <xref:System.Drawing.Graphics> class provides several <xref:System.Drawing.Graphics.DrawImage%2A> methods, some of which have source and destination rectangle parameters that you can use to crop and scale images.</span></span>  
  
## <a name="example"></a><span data-ttu-id="51af9-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="51af9-104">Example</span></span>  
 <span data-ttu-id="51af9-105">Im folgenden Beispiel wird ein- <xref:System.Drawing.Image> Objekt aus der Datenträger Datei Apple.gif erstellt.</span><span class="sxs-lookup"><span data-stu-id="51af9-105">The following example constructs an <xref:System.Drawing.Image> object from the disk file Apple.gif.</span></span> <span data-ttu-id="51af9-106">Der Code zeichnet das gesamte Apple-Image in seiner ursprünglichen Größe.</span><span class="sxs-lookup"><span data-stu-id="51af9-106">The code draws the entire apple image in its original size.</span></span> <span data-ttu-id="51af9-107">Der Code ruft dann die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode eines- <xref:System.Drawing.Graphics> Objekts auf, um einen Teil des Apple-Bilds in einem Ziel Rechteck zu zeichnen, das größer ist als das ursprüngliche Apple-Image.</span><span class="sxs-lookup"><span data-stu-id="51af9-107">The code then calls the <xref:System.Drawing.Graphics.DrawImage%2A> method of a <xref:System.Drawing.Graphics> object to draw a portion of the apple image in a destination rectangle that is larger than the original apple image.</span></span>  
  
 <span data-ttu-id="51af9-108">Die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode bestimmt, welcher Teil des Apple gezeichnet werden soll, indem das Quell Rechteck betrachtet wird, das durch das dritte, vierte, fünfte und sechste Argument angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="51af9-108">The <xref:System.Drawing.Graphics.DrawImage%2A> method determines which portion of the apple to draw by looking at the source rectangle, which is specified by the third, fourth, fifth, and sixth arguments.</span></span> <span data-ttu-id="51af9-109">In diesem Fall wird Apple auf 75 Prozent seiner Breite und 75 Prozent seiner Höhe zugeschnitten.</span><span class="sxs-lookup"><span data-stu-id="51af9-109">In this case, the apple is cropped to 75 percent of its width and 75 percent of its height.</span></span>  
  
 <span data-ttu-id="51af9-110"><xref:System.Drawing.Graphics.DrawImage%2A>Mit der-Methode wird bestimmt, wo das gekippte Apple gezeichnet werden soll und wie groß das angeschnittenen Apple ist, indem das Ziel Rechteck, das durch das zweite Argument angegeben wird, durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="51af9-110">The <xref:System.Drawing.Graphics.DrawImage%2A> method determines where to draw the cropped apple and how big to make the cropped apple by looking at the destination rectangle, which is specified by the second argument.</span></span> <span data-ttu-id="51af9-111">In diesem Fall ist das Ziel Rechteck um 30 Prozent breiter und 30 Prozent höher als das ursprüngliche Bild.</span><span class="sxs-lookup"><span data-stu-id="51af9-111">In this case, the destination rectangle is 30 percent wider and 30 percent taller than the original image.</span></span>  
  
 <span data-ttu-id="51af9-112">Die folgende Abbildung zeigt das ursprüngliche Apple und das skalierte, ausgeschnittene Apple.</span><span class="sxs-lookup"><span data-stu-id="51af9-112">The following illustration shows the original apple and the scaled, cropped apple.</span></span>  
  
 ![Screenshot eines ursprünglichen Bilds und des abgeschnittenen Bilds.](./media/how-to-crop-and-scale-images/original-image-cropped-image.png)  
  
 [!code-csharp[System.Drawing.WorkingWithImages#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.WorkingWithImages#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="51af9-114">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="51af9-114">Compiling the Code</span></span>  
 <span data-ttu-id="51af9-115">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="51af9-115">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="51af9-116">Stellen Sie sicher, `Apple.gif` dass Sie durch einen Bilddateinamen und-Pfad ersetzen, die auf Ihrem System gültig sind.</span><span class="sxs-lookup"><span data-stu-id="51af9-116">Make sure to replace `Apple.gif` with an image file name and path that are valid on your system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51af9-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51af9-117">See also</span></span>

- [<span data-ttu-id="51af9-118">Bilder, Bitmaps und Metadatendateien</span><span class="sxs-lookup"><span data-stu-id="51af9-118">Images, Bitmaps, and Metafiles</span></span>](images-bitmaps-and-metafiles.md)
- [<span data-ttu-id="51af9-119">Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien</span><span class="sxs-lookup"><span data-stu-id="51af9-119">Working with Images, Bitmaps, Icons, and Metafiles</span></span>](working-with-images-bitmaps-icons-and-metafiles.md)
