---
title: 'Vorgehensweise: Zeichnen einer mit einer Textur ausgefüllten Linie'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drawing [Windows Forms], lines
- lines [Windows Forms], texture
- drawing lines [Windows Forms], texture
ms.assetid: dc9118cc-f3c2-42e5-8173-f46d41d18fd5
ms.openlocfilehash: c0f90c298f48aeb96893bb09241faddc08d8a49d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975954"
---
# <a name="how-to-draw-a-line-filled-with-a-texture"></a><span data-ttu-id="51bc2-102">Vorgehensweise: Zeichnen einer mit einer Textur ausgefüllten Linie</span><span class="sxs-lookup"><span data-stu-id="51bc2-102">How to: Draw a Line Filled with a Texture</span></span>
<span data-ttu-id="51bc2-103">Anstatt eine Linie mit einer voll Tonfarbe zu zeichnen, können Sie eine Linie mit einer Textur zeichnen.</span><span class="sxs-lookup"><span data-stu-id="51bc2-103">Instead of drawing a line with a solid color, you can draw a line with a texture.</span></span> <span data-ttu-id="51bc2-104">Um Linien und Kurven mit einer Textur zu zeichnen, erstellen Sie ein <xref:System.Drawing.TextureBrush> -Objekt, und übergeben <xref:System.Drawing.TextureBrush> Sie das Objekt an einen <xref:System.Drawing.Pen.%23ctor%2A> Konstruktor.</span><span class="sxs-lookup"><span data-stu-id="51bc2-104">To draw lines and curves with a texture, create a <xref:System.Drawing.TextureBrush> object, and pass that <xref:System.Drawing.TextureBrush> object to a <xref:System.Drawing.Pen.%23ctor%2A> constructor.</span></span> <span data-ttu-id="51bc2-105">Die Bitmap, die dem Textur Pinsel zugeordnet ist, wird verwendet, um die Ebene (unsichtbar) zu Kacheln, und wenn der Stift eine Linie oder Kurve zeichnet, wird der Strich des Stifts bestimmte Pixel der Kachel Textur nicht abdecken.</span><span class="sxs-lookup"><span data-stu-id="51bc2-105">The bitmap associated with the texture brush is used to tile the plane (invisibly), and when the pen draws a line or curve, the stroke of the pen uncovers certain pixels of the tiled texture.</span></span>  
  
## <a name="example"></a><span data-ttu-id="51bc2-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="51bc2-106">Example</span></span>  
 <span data-ttu-id="51bc2-107">Im folgenden Beispiel wird ein- <xref:System.Drawing.Bitmap> Objekt aus der-Datei erstellt `Texture1.jpg` .</span><span class="sxs-lookup"><span data-stu-id="51bc2-107">The following example creates a <xref:System.Drawing.Bitmap> object from the file `Texture1.jpg`.</span></span> <span data-ttu-id="51bc2-108">Diese Bitmap wird zum Erstellen eines <xref:System.Drawing.TextureBrush> -Objekts verwendet, und das- <xref:System.Drawing.TextureBrush> Objekt wird verwendet, um ein-Objekt zu erstellen <xref:System.Drawing.Pen> .</span><span class="sxs-lookup"><span data-stu-id="51bc2-108">That bitmap is used to construct a <xref:System.Drawing.TextureBrush> object, and the <xref:System.Drawing.TextureBrush> object is used to construct a <xref:System.Drawing.Pen> object.</span></span> <span data-ttu-id="51bc2-109">Der-Befehl <xref:System.Drawing.Graphics.DrawImage%2A> zeichnet die Bitmap mit der linken oberen Ecke bei (0,0).</span><span class="sxs-lookup"><span data-stu-id="51bc2-109">The call to <xref:System.Drawing.Graphics.DrawImage%2A> draws the bitmap with its upper-left corner at (0, 0).</span></span> <span data-ttu-id="51bc2-110">Der-Befehl <xref:System.Drawing.Graphics.DrawEllipse%2A> verwendet das- <xref:System.Drawing.Pen> Objekt, um eine strukturierte Ellipse zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="51bc2-110">The call to <xref:System.Drawing.Graphics.DrawEllipse%2A> uses the <xref:System.Drawing.Pen> object to draw a textured ellipse.</span></span>  
  
 <span data-ttu-id="51bc2-111">Die folgende Abbildung zeigt die Bitmap und die strukturierte Ellipse:</span><span class="sxs-lookup"><span data-stu-id="51bc2-111">The following illustration shows the bitmap and the textured ellipse:</span></span>  
  
 ![Screenshot, der die Bitmap und die strukturierte Ellipse anzeigt](./media/how-to-draw-a-line-filled-with-a-texture/bitmap-textured-ellipse.png)  
  
 [!code-csharp[System.Drawing.UsingAPen#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#61)]
 [!code-vb[System.Drawing.UsingAPen#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#61)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="51bc2-113">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="51bc2-113">Compiling the Code</span></span>  
 <span data-ttu-id="51bc2-114">Erstellen Sie ein Windows Form, und behandeln Sie das-Ereignis des Formulars <xref:System.Windows.Forms.Control.Paint> .</span><span class="sxs-lookup"><span data-stu-id="51bc2-114">Create a Windows Form and handle the form's <xref:System.Windows.Forms.Control.Paint> event.</span></span> <span data-ttu-id="51bc2-115">Fügen Sie den vorangehenden Code in den- <xref:System.Windows.Forms.Control.Paint> Ereignishandler ein.</span><span class="sxs-lookup"><span data-stu-id="51bc2-115">Paste the preceding code into the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="51bc2-116">Ersetzen `Texture.jpg` Sie dies durch ein gültiges Bild auf Ihrem System.</span><span class="sxs-lookup"><span data-stu-id="51bc2-116">Replace `Texture.jpg` with an image valid on your system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51bc2-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51bc2-117">See also</span></span>

- [<span data-ttu-id="51bc2-118">Verwenden eines Stifts zum Zeichnen von Linien und Formen</span><span class="sxs-lookup"><span data-stu-id="51bc2-118">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
- [<span data-ttu-id="51bc2-119">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="51bc2-119">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
