---
title: 'Vorgehensweise: Drehen, Spiegeln und Neigen von Bildern'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- images [Windows Forms], reflecting
- images [Windows Forms], rotating
- images [Windows Forms], skewing
ms.assetid: a3bf97eb-63ed-425a-ba07-dcc65efb567c
ms.openlocfilehash: 80ac92d545d9be7a4a611038eaaadbbdbe2e8ecf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975884"
---
# <a name="how-to-rotate-reflect-and-skew-images"></a><span data-ttu-id="b5b22-102">Vorgehensweise: Drehen, Spiegeln und Neigen von Bildern</span><span class="sxs-lookup"><span data-stu-id="b5b22-102">How to: Rotate, Reflect, and Skew Images</span></span>
<span data-ttu-id="b5b22-103">Sie können ein Bild drehen, reflektieren und verzerren, indem Sie Zielpunkte für die obere linke, obere Rechte und untere linke Ecke des ursprünglichen Bilds angeben.</span><span class="sxs-lookup"><span data-stu-id="b5b22-103">You can rotate, reflect, and skew an image by specifying destination points for the upper-left, upper-right, and lower-left corners of the original image.</span></span> <span data-ttu-id="b5b22-104">Die drei Zielpunkte bestimmen eine affine Transformation, die das ursprüngliche rechteckige Bild einem Parallelogram zuordnet.</span><span class="sxs-lookup"><span data-stu-id="b5b22-104">The three destination points determine an affine transformation that maps the original rectangular image to a parallelogram.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b5b22-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b5b22-105">Example</span></span>  
 <span data-ttu-id="b5b22-106">Angenommen, das ursprüngliche Bild ist ein Rechteck mit der oberen linken Ecke bei (0,0), der oberen rechten Ecke bei (100, 0) und der unteren linken Ecke bei (0, 50).</span><span class="sxs-lookup"><span data-stu-id="b5b22-106">For example, suppose the original image is a rectangle with upper-left corner at (0, 0), upper-right corner at (100, 0), and lower-left corner at (0, 50).</span></span> <span data-ttu-id="b5b22-107">Nehmen Sie nun an, dass Sie die drei Punkte den Zielpunkten wie folgt zuordnen.</span><span class="sxs-lookup"><span data-stu-id="b5b22-107">Now suppose you map those three points to destination points as follows.</span></span>  
  
|<span data-ttu-id="b5b22-108">Ursprünglicher Punkt</span><span class="sxs-lookup"><span data-stu-id="b5b22-108">Original point</span></span>|<span data-ttu-id="b5b22-109">Zielpunkt</span><span class="sxs-lookup"><span data-stu-id="b5b22-109">Destination point</span></span>|  
|--------------------|-----------------------|  
|<span data-ttu-id="b5b22-110">Oben links (0,0)</span><span class="sxs-lookup"><span data-stu-id="b5b22-110">Upper-left (0, 0)</span></span>|<span data-ttu-id="b5b22-111">(200, 20)</span><span class="sxs-lookup"><span data-stu-id="b5b22-111">(200, 20)</span></span>|  
|<span data-ttu-id="b5b22-112">Upper-Right (100, 0)</span><span class="sxs-lookup"><span data-stu-id="b5b22-112">Upper-right (100, 0)</span></span>|<span data-ttu-id="b5b22-113">(110, 100)</span><span class="sxs-lookup"><span data-stu-id="b5b22-113">(110, 100)</span></span>|  
|<span data-ttu-id="b5b22-114">Unten links (0, 50)</span><span class="sxs-lookup"><span data-stu-id="b5b22-114">Lower-left (0, 50)</span></span>|<span data-ttu-id="b5b22-115">(250, 30)</span><span class="sxs-lookup"><span data-stu-id="b5b22-115">(250, 30)</span></span>|  
  
 <span data-ttu-id="b5b22-116">Die folgende Abbildung zeigt das ursprüngliche Bild und das dem Parallelogram zugeordnete Bild.</span><span class="sxs-lookup"><span data-stu-id="b5b22-116">The following illustration shows the original image and the image mapped to the parallelogram.</span></span> <span data-ttu-id="b5b22-117">Das ursprüngliche Bild wurde verzerrt, reflektiert, gedreht und übersetzt.</span><span class="sxs-lookup"><span data-stu-id="b5b22-117">The original image has been skewed, reflected, rotated, and translated.</span></span> <span data-ttu-id="b5b22-118">Die x-Achse entlang des oberen Rands des ursprünglichen Bilds wird der Zeile zugeordnet, die durchlaufen wird (200, 20) und (110, 100).</span><span class="sxs-lookup"><span data-stu-id="b5b22-118">The x-axis along the top edge of the original image is mapped to the line that runs through (200, 20) and (110, 100).</span></span> <span data-ttu-id="b5b22-119">Die y-Achse entlang des linken Rands des ursprünglichen Bilds wird der Zeile zugeordnet, die durchlaufen wird (200, 20) und (250, 30).</span><span class="sxs-lookup"><span data-stu-id="b5b22-119">The y-axis along the left edge of the original image is mapped to the line that runs through (200, 20) and (250, 30).</span></span>  
  
 ![Das ursprüngliche Bild und das dem Parallelogram zugeordnete Bild.](./media/how-to-rotate-reflect-and-skew-images/reflected-skewed-rotated-illustration.gif)  
  
 <span data-ttu-id="b5b22-121">Die folgende Abbildung zeigt eine ähnliche Transformation, die auf ein Foto Bild angewendet wurde:</span><span class="sxs-lookup"><span data-stu-id="b5b22-121">The following illustration shows a similar transformation applied to a photographic image:</span></span>  
  
 ![Das Bild eines Kletterers und des Bilds, das dem Parallelogramm zugeordnet ist.](./media/how-to-rotate-reflect-and-skew-images/reflected-skewed-rotated-photo.png)  
  
 <span data-ttu-id="b5b22-123">Die folgende Abbildung zeigt eine ähnliche Transformation, die auf eine Metadatei angewendet wird:</span><span class="sxs-lookup"><span data-stu-id="b5b22-123">The following illustration shows a similar transformation applied to a metafile:</span></span>  
  
 ![Abbildung von Formen und Text, die dem Parallelogram zugeordnet sind.](./media/how-to-rotate-reflect-and-skew-images/reflected-skewed-rotated-metafile.png)  
  
 <span data-ttu-id="b5b22-125">Im folgenden Beispiel werden die in der ersten Abbildung gezeigten Bilder erzeugt.</span><span class="sxs-lookup"><span data-stu-id="b5b22-125">The following example produces the images shown in the first illustration.</span></span>  
  
 [!code-csharp[System.Drawing.WorkingWithImages#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#61)]
 [!code-vb[System.Drawing.WorkingWithImages#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#61)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="b5b22-126">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="b5b22-126">Compiling the Code</span></span>  
 <span data-ttu-id="b5b22-127">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="b5b22-127">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="b5b22-128">Stellen Sie sicher, `Stripes.bmp` dass Sie durch den Pfad zu einem Bild ersetzen, das auf Ihrem System gültig ist.</span><span class="sxs-lookup"><span data-stu-id="b5b22-128">Make sure to replace `Stripes.bmp` with the path to an image that is valid on your system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b5b22-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5b22-129">See also</span></span>

- [<span data-ttu-id="b5b22-130">Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien</span><span class="sxs-lookup"><span data-stu-id="b5b22-130">Working with Images, Bitmaps, Icons, and Metafiles</span></span>](working-with-images-bitmaps-icons-and-metafiles.md)
