---
title: 'Vorgehensweise: Zeichnen von Text an einer angegebenen Position'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [Windows Forms], drawing at specified locations [Windows Forms]
- drawing text
- drawing text [Windows Forms], specified locations [Windows Forms]
- Windows Forms, drawing text at a specified location
ms.assetid: 60816423-1c38-465e-980d-2c2b64d74086
ms.openlocfilehash: 0c36b00e4f6f71f0ecf8042853bb8e99e57854da
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975927"
---
# <a name="how-to-draw-text-at-a-specified-location"></a><span data-ttu-id="b8256-102">Vorgehensweise: Zeichnen von Text an einer angegebenen Position</span><span class="sxs-lookup"><span data-stu-id="b8256-102">How to: Draw Text at a Specified Location</span></span>
<span data-ttu-id="b8256-103">Wenn Sie eine benutzerdefinierte Zeichnung ausführen, können Sie Text in einer einzelnen horizontalen Linie beginnend an einem angegebenen Punkt zeichnen.</span><span class="sxs-lookup"><span data-stu-id="b8256-103">When you perform custom drawing, you can draw text in a single horizontal line starting at a specified point.</span></span> <span data-ttu-id="b8256-104">Sie können Text auf diese Weise zeichnen, indem Sie die <xref:System.Drawing.Graphics.DrawString%2A> überladene-Methode der- <xref:System.Drawing.Graphics> Klasse verwenden, die einen-oder-Parameter annimmt <xref:System.Drawing.Point> <xref:System.Drawing.PointF> .</span><span class="sxs-lookup"><span data-stu-id="b8256-104">You can draw text in this manner by using the <xref:System.Drawing.Graphics.DrawString%2A> overloaded method of the <xref:System.Drawing.Graphics> class that takes a <xref:System.Drawing.Point> or <xref:System.Drawing.PointF> parameter.</span></span> <span data-ttu-id="b8256-105">Die <xref:System.Drawing.Graphics.DrawString%2A> -Methode erfordert auch <xref:System.Drawing.Brush> und. <xref:System.Drawing.Font></span><span class="sxs-lookup"><span data-stu-id="b8256-105">The <xref:System.Drawing.Graphics.DrawString%2A> method also requires a <xref:System.Drawing.Brush> and <xref:System.Drawing.Font></span></span>  
  
 <span data-ttu-id="b8256-106">Sie können auch die <xref:System.Windows.Forms.TextRenderer.DrawText%2A> überladene-Methode der verwenden <xref:System.Windows.Forms.TextRenderer> , die einen annimmt <xref:System.Drawing.Point> .</span><span class="sxs-lookup"><span data-stu-id="b8256-106">You can also use the <xref:System.Windows.Forms.TextRenderer.DrawText%2A> overloaded method of the <xref:System.Windows.Forms.TextRenderer> that takes a <xref:System.Drawing.Point>.</span></span> <span data-ttu-id="b8256-107"><xref:System.Windows.Forms.TextRenderer.DrawText%2A> erfordert auch <xref:System.Drawing.Color> und <xref:System.Drawing.Font> .</span><span class="sxs-lookup"><span data-stu-id="b8256-107"><xref:System.Windows.Forms.TextRenderer.DrawText%2A> also requires a <xref:System.Drawing.Color> and a <xref:System.Drawing.Font>.</span></span>  
  
 <span data-ttu-id="b8256-108">Die folgende Abbildung zeigt die Ausgabe von Text, der an einem angegebenen Punkt gezeichnet wird, wenn Sie die <xref:System.Drawing.Graphics.DrawString%2A> überladene-Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8256-108">The following illustration shows the output of text drawn at a specified point when you use the <xref:System.Drawing.Graphics.DrawString%2A> overloaded method.</span></span>  
  
 ![Screenshot, der die Ausgabe von Text an einem angegebenen Punkt anzeigt.](./media/how-to-draw-text-at-a-specified-location/font-text-specified-point.png)  
  
### <a name="to-draw-a-line-of-text-with-gdi"></a><span data-ttu-id="b8256-110">So zeichnen Sie eine Textzeile mit GDI+</span><span class="sxs-lookup"><span data-stu-id="b8256-110">To draw a line of text with GDI+</span></span>  
  
1. <span data-ttu-id="b8256-111">Verwenden Sie die- <xref:System.Drawing.Graphics.DrawString%2A> Methode, und übergeben Sie den gewünschten Text <xref:System.Drawing.Point> oder <xref:System.Drawing.PointF> , <xref:System.Drawing.Font> und <xref:System.Drawing.Brush> .</span><span class="sxs-lookup"><span data-stu-id="b8256-111">Use the <xref:System.Drawing.Graphics.DrawString%2A> method, passing the text you want, <xref:System.Drawing.Point> or <xref:System.Drawing.PointF>, <xref:System.Drawing.Font>, and <xref:System.Drawing.Brush>.</span></span>  
  
     [!code-csharp[System.Drawing.AlignDrawnText#30](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#30)]
     [!code-vb[System.Drawing.AlignDrawnText#30](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#30)]  
  
### <a name="to-draw-a-line-of-text-with-gdi"></a><span data-ttu-id="b8256-112">So zeichnen Sie eine Textzeile mit GDI</span><span class="sxs-lookup"><span data-stu-id="b8256-112">To draw a line of text with GDI</span></span>  
  
1. <span data-ttu-id="b8256-113">Verwenden Sie die- <xref:System.Windows.Forms.TextRenderer.DrawText%2A> Methode, und übergeben Sie den gewünschten Text,, <xref:System.Drawing.Point> <xref:System.Drawing.Font> und <xref:System.Drawing.Color> .</span><span class="sxs-lookup"><span data-stu-id="b8256-113">Use the <xref:System.Windows.Forms.TextRenderer.DrawText%2A> method, passing the text you want, <xref:System.Drawing.Point>, <xref:System.Drawing.Font>, and <xref:System.Drawing.Color>.</span></span>  
  
     [!code-csharp[System.Drawing.AlignDrawnText#40](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/CS/Form1.cs#40)]
     [!code-vb[System.Drawing.AlignDrawnText#40](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlignDrawnText/VB/Form1.vb#40)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="b8256-114">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="b8256-114">Compiling the Code</span></span>  
 <span data-ttu-id="b8256-115">In den vorherigen Beispielen ist Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="b8256-115">The previous examples require:</span></span>  
  
- <span data-ttu-id="b8256-116"><xref:System.Windows.Forms.PaintEventArgs>  `e`, bei dem es sich um einen Parameter von handelt <xref:System.Windows.Forms.PaintEventHandler> .</span><span class="sxs-lookup"><span data-stu-id="b8256-116"><xref:System.Windows.Forms.PaintEventArgs>  `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="b8256-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8256-117">See also</span></span>

- [<span data-ttu-id="b8256-118">Vorgehensweise: Zeichnen von Text mit GDI</span><span class="sxs-lookup"><span data-stu-id="b8256-118">How to: Draw Text with GDI</span></span>](how-to-draw-text-with-gdi.md)
- [<span data-ttu-id="b8256-119">Verwenden von Schriftarten und Text</span><span class="sxs-lookup"><span data-stu-id="b8256-119">Using Fonts and Text</span></span>](using-fonts-and-text.md)
- [<span data-ttu-id="b8256-120">Vorgehensweise: Erstellen von Schriftartfamilien und Schriftarten</span><span class="sxs-lookup"><span data-stu-id="b8256-120">How to: Construct Font Families and Fonts</span></span>](how-to-construct-font-families-and-fonts.md)
- [<span data-ttu-id="b8256-121">Vorgehensweise: Zeichnen von umbrochenem Text in einem Rechteck</span><span class="sxs-lookup"><span data-stu-id="b8256-121">How to: Draw Wrapped Text in a Rectangle</span></span>](how-to-draw-wrapped-text-in-a-rectangle.md)
