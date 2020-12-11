---
title: 'Vorgehensweise: Zeichnen von umbrochenem Text in einem Rechteck'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms, drawing text in a rectangle
- text [Windows Forms], drawing in a rectangle
- strings [Windows Forms], drawing in a rectangle
ms.assetid: e1fb432a-dc90-48b5-9b6b-acc14507133d
ms.openlocfilehash: ace79e45737a3ce26d8bdcd603e923c1e6040d4d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975915"
---
# <a name="how-to-draw-wrapped-text-in-a-rectangle"></a><span data-ttu-id="99ccf-102">Vorgehensweise: Zeichnen von umbrochenem Text in einem Rechteck</span><span class="sxs-lookup"><span data-stu-id="99ccf-102">How to: Draw Wrapped Text in a Rectangle</span></span>
<span data-ttu-id="99ccf-103">Mit der <xref:System.Drawing.Graphics.DrawString%2A> überladenen-Methode der- <xref:System.Drawing.Graphics> Klasse, die einen-oder-Parameter annimmt, können Sie eingeschlossene Text in einem Rechteck zeichnen <xref:System.Drawing.Rectangle> <xref:System.Drawing.RectangleF> .</span><span class="sxs-lookup"><span data-stu-id="99ccf-103">You can draw wrapped text in a rectangle by using the <xref:System.Drawing.Graphics.DrawString%2A> overloaded method of the <xref:System.Drawing.Graphics> class that takes a <xref:System.Drawing.Rectangle> or <xref:System.Drawing.RectangleF> parameter.</span></span> <span data-ttu-id="99ccf-104">Außerdem verwenden Sie eine <xref:System.Drawing.Brush> und eine <xref:System.Drawing.Font> .</span><span class="sxs-lookup"><span data-stu-id="99ccf-104">You will also use a <xref:System.Drawing.Brush> and a <xref:System.Drawing.Font>.</span></span>  
  
 <span data-ttu-id="99ccf-105">Sie können auch eingeschlossene Text in einem Rechteck zeichnen, indem Sie die <xref:System.Windows.Forms.TextRenderer.DrawText%2A> überladene-Methode der verwenden <xref:System.Windows.Forms.TextRenderer> , die einen <xref:System.Drawing.Rectangle> -Parameter und einen- <xref:System.Windows.Forms.TextFormatFlags> Parameter annimmt.</span><span class="sxs-lookup"><span data-stu-id="99ccf-105">You can also draw wrapped text in a rectangle by using the <xref:System.Windows.Forms.TextRenderer.DrawText%2A> overloaded method of the <xref:System.Windows.Forms.TextRenderer> that takes a <xref:System.Drawing.Rectangle> and a <xref:System.Windows.Forms.TextFormatFlags> parameter.</span></span> <span data-ttu-id="99ccf-106">Außerdem verwenden Sie eine <xref:System.Drawing.Color> und eine <xref:System.Drawing.Font> .</span><span class="sxs-lookup"><span data-stu-id="99ccf-106">You will also use a <xref:System.Drawing.Color> and a <xref:System.Drawing.Font>.</span></span>  
  
 <span data-ttu-id="99ccf-107">Die folgende Abbildung zeigt die Ausgabe von Text, der im Rechteck gezeichnet wird, wenn Sie die- <xref:System.Drawing.Graphics.DrawString%2A> Methode verwenden:</span><span class="sxs-lookup"><span data-stu-id="99ccf-107">The following illustration shows the output of text drawn in the rectangle when you use the <xref:System.Drawing.Graphics.DrawString%2A> method:</span></span>
  
 ![Screenshot, der die Ausgabe zeigt, wenn die DrawString-Methode verwendet wird.](./media/how-to-draw-wrapped-text-in-a-rectangle/drawstring-method-font-text.png)  
  
### <a name="to-draw-wrapped-text-in-a-rectangle-with-gdi"></a><span data-ttu-id="99ccf-109">So zeichnen Sie umschließenen Text in einem Rechteck mit GDI+</span><span class="sxs-lookup"><span data-stu-id="99ccf-109">To draw wrapped text in a rectangle with GDI+</span></span>  
  
1. <span data-ttu-id="99ccf-110">Verwenden <xref:System.Drawing.Graphics.DrawString%2A> Sie die überladene-Methode, und übergeben Sie den gewünschten Text, <xref:System.Drawing.Rectangle> oder <xref:System.Drawing.RectangleF> <xref:System.Drawing.Font> und <xref:System.Drawing.Brush> .</span><span class="sxs-lookup"><span data-stu-id="99ccf-110">Use the <xref:System.Drawing.Graphics.DrawString%2A> overloaded method, passing the text you want, <xref:System.Drawing.Rectangle> or <xref:System.Drawing.RectangleF>, <xref:System.Drawing.Font> and <xref:System.Drawing.Brush>.</span></span>  
  
     [!code-csharp[System.Drawing.AlignDrawnText#50](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#50)]
     [!code-vb[System.Drawing.AlignDrawnText#50](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#50)]  
  
### <a name="to-draw-wrapped-text-in-a-rectangle-with-gdi"></a><span data-ttu-id="99ccf-111">So zeichnen Sie umschließenen Text in einem Rechteck mit GDI</span><span class="sxs-lookup"><span data-stu-id="99ccf-111">To draw wrapped text in a rectangle with GDI</span></span>  
  
1. <span data-ttu-id="99ccf-112">Verwenden Sie den- <xref:System.Windows.Forms.TextFormatFlags> Enumerationswert, um anzugeben, dass der Text mit der <xref:System.Windows.Forms.TextRenderer.DrawText%2A> überladenen Methode umschließt werden soll, und übergeben Sie den gewünschten Text, <xref:System.Drawing.Rectangle> <xref:System.Drawing.Font> und <xref:System.Drawing.Color> .</span><span class="sxs-lookup"><span data-stu-id="99ccf-112">Use the <xref:System.Windows.Forms.TextFormatFlags> enumeration value to specify the text should be wrapped with the <xref:System.Windows.Forms.TextRenderer.DrawText%2A> overloaded method, passing the text you want, <xref:System.Drawing.Rectangle>, <xref:System.Drawing.Font> and <xref:System.Drawing.Color>.</span></span>  
  
     [!code-csharp[System.Drawing.AlignDrawnText#60](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#60)]
     [!code-vb[System.Drawing.AlignDrawnText#60](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#60)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="99ccf-113">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="99ccf-113">Compiling the Code</span></span>  
 <span data-ttu-id="99ccf-114">In den vorherigen Beispielen ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="99ccf-114">The previous examples require:</span></span>  
  
- <span data-ttu-id="99ccf-115"><xref:System.Windows.Forms.PaintEventArgs>`e`, bei dem es sich um einen Parameter von handelt <xref:System.Windows.Forms.PaintEventHandler> .</span><span class="sxs-lookup"><span data-stu-id="99ccf-115"><xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="99ccf-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99ccf-116">See also</span></span>

- [<span data-ttu-id="99ccf-117">Vorgehensweise: Zeichnen von Text mit GDI</span><span class="sxs-lookup"><span data-stu-id="99ccf-117">How to: Draw Text with GDI</span></span>](how-to-draw-text-with-gdi.md)
- [<span data-ttu-id="99ccf-118">Verwenden von Schriftarten und Text</span><span class="sxs-lookup"><span data-stu-id="99ccf-118">Using Fonts and Text</span></span>](using-fonts-and-text.md)
- [<span data-ttu-id="99ccf-119">Vorgehensweise: Erstellen von Schriftartfamilien und Schriftarten</span><span class="sxs-lookup"><span data-stu-id="99ccf-119">How to: Construct Font Families and Fonts</span></span>](how-to-construct-font-families-and-fonts.md)
- [<span data-ttu-id="99ccf-120">Vorgehensweise: Zeichnen von Text an einer angegebenen Position</span><span class="sxs-lookup"><span data-stu-id="99ccf-120">How to: Draw Text at a Specified Location</span></span>](how-to-draw-text-at-a-specified-location.md)
