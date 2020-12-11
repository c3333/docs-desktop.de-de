---
title: 'Vorgehensweise: Zeichnen einer vorhandenen Bitmap auf dem Bildschirm'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [Windows Forms], displaying in Windows Forms
- bitmaps [Windows Forms], loading in Windows Forms applications
- images [Windows Forms], displaying on Windows Forms
ms.assetid: 5bc558d7-b326-4050-a834-b8600da0de95
ms.openlocfilehash: 90511adf9caffe7952e270d6fe32dd85162a29d7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975936"
---
# <a name="how-to-draw-an-existing-bitmap-to-the-screen"></a><span data-ttu-id="1da93-102">Vorgehensweise: Zeichnen einer vorhandenen Bitmap auf dem Bildschirm</span><span class="sxs-lookup"><span data-stu-id="1da93-102">How to: Draw an Existing Bitmap to the Screen</span></span>
<span data-ttu-id="1da93-103">Sie können ein vorhandenes Bild problemlos auf dem Bildschirm zeichnen.</span><span class="sxs-lookup"><span data-stu-id="1da93-103">You can easily draw an existing image on the screen.</span></span> <span data-ttu-id="1da93-104">Zunächst müssen Sie ein- <xref:System.Drawing.Bitmap> Objekt erstellen, indem Sie den Bitmap-Konstruktor verwenden, der einen Dateinamen annimmt <xref:System.Drawing.Bitmap.%23ctor%28System.String%29> .</span><span class="sxs-lookup"><span data-stu-id="1da93-104">First you need to create a <xref:System.Drawing.Bitmap> object by using the bitmap constructor that takes a file name, <xref:System.Drawing.Bitmap.%23ctor%28System.String%29>.</span></span> <span data-ttu-id="1da93-105">Dieser Konstruktor akzeptiert Bilder mit verschiedenen Dateiformaten, einschließlich BMP, GIF, JPEG, PNG und TIFF.</span><span class="sxs-lookup"><span data-stu-id="1da93-105">This constructor accepts images with several different file formats, including BMP, GIF, JPEG, PNG, and TIFF.</span></span> <span data-ttu-id="1da93-106">Nachdem Sie das-Objekt erstellt haben <xref:System.Drawing.Bitmap> , übergeben Sie dieses <xref:System.Drawing.Bitmap> Objekt an die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode eines- <xref:System.Drawing.Graphics> Objekts.</span><span class="sxs-lookup"><span data-stu-id="1da93-106">After you have created the <xref:System.Drawing.Bitmap> object, pass that <xref:System.Drawing.Bitmap> object to the <xref:System.Drawing.Graphics.DrawImage%2A> method of a <xref:System.Drawing.Graphics> object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="1da93-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1da93-107">Example</span></span>  
 <span data-ttu-id="1da93-108">In diesem Beispiel <xref:System.Drawing.Bitmap> wird ein-Objekt aus einer JPEG-Datei erstellt, und anschließend wird die Bitmap mit der linken oberen Ecke bei (60, 10) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1da93-108">This example creates a <xref:System.Drawing.Bitmap> object from a JPEG file and then draws the bitmap with its upper-left corner at (60, 10).</span></span>  
  
 <span data-ttu-id="1da93-109">In der folgenden Abbildung wird die Bitmap gezeigt, die an der angegebenen Position gezeichnet wurde:</span><span class="sxs-lookup"><span data-stu-id="1da93-109">The following illustration shows the bitmap drawn at the specified location:</span></span>  
  
 ![Screenshot, der ein Bild an einer bestimmten Position anzeigt.](./media/how-to-draw-an-existing-bitmap-to-the-screen/bitmap-specified-position.png)  
  
 [!code-csharp[System.Drawing.WorkingWithImages#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.WorkingWithImages#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.WorkingWithImages/VB/Class1.vb#21)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="1da93-111">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="1da93-111">Compiling the Code</span></span>  
 <span data-ttu-id="1da93-112">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="1da93-112">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1da93-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1da93-113">See also</span></span>

- [<span data-ttu-id="1da93-114">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="1da93-114">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="1da93-115">Arbeiten mit Bildern, Bitmaps, Symbolen und Metadateien</span><span class="sxs-lookup"><span data-stu-id="1da93-115">Working with Images, Bitmaps, Icons, and Metafiles</span></span>](working-with-images-bitmaps-icons-and-metafiles.md)
