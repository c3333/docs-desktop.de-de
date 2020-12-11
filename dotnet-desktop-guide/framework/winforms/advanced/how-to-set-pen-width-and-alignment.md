---
title: 'Vorgehensweise: Festlegen von Stiftbreite und -ausrichtung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- pens [Windows Forms], setting width
- pens [Windows Forms], setting alignment
ms.assetid: a202af36-4d31-4401-a126-b232f51db581
ms.openlocfilehash: 1f1ea6e8ef0b94aa46a4bf8177d59e59297d6e3f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976128"
---
# <a name="how-to-set-pen-width-and-alignment"></a><span data-ttu-id="cb9c5-102">Vorgehensweise: Festlegen von Stiftbreite und -ausrichtung</span><span class="sxs-lookup"><span data-stu-id="cb9c5-102">How to: Set Pen Width and Alignment</span></span>
<span data-ttu-id="cb9c5-103">Wenn Sie ein-Element erstellen <xref:System.Drawing.Pen> , können Sie die Stift Breite als eines der Argumente für den Konstruktor angeben.</span><span class="sxs-lookup"><span data-stu-id="cb9c5-103">When you create a <xref:System.Drawing.Pen>, you can supply the pen width as one of the arguments to the constructor.</span></span> <span data-ttu-id="cb9c5-104">Sie können auch die Stift Breite mit der- <xref:System.Drawing.Pen.Width%2A> Eigenschaft der- <xref:System.Drawing.Pen> Klasse ändern.</span><span class="sxs-lookup"><span data-stu-id="cb9c5-104">You can also change the pen width with the <xref:System.Drawing.Pen.Width%2A> property of the <xref:System.Drawing.Pen> class.</span></span>  
  
 <span data-ttu-id="cb9c5-105">Eine theoretische Linie hat eine Breite von 0.</span><span class="sxs-lookup"><span data-stu-id="cb9c5-105">A theoretical line has a width of 0.</span></span> <span data-ttu-id="cb9c5-106">Wenn Sie eine Linie zeichnen, die 1 Pixel breit ist, werden die Pixel auf der theoretischen Linie zentriert.</span><span class="sxs-lookup"><span data-stu-id="cb9c5-106">When you draw a line that is 1 pixel wide, the pixels are centered on the theoretical line.</span></span> <span data-ttu-id="cb9c5-107">Wenn Sie eine Linie zeichnen, die mehr als ein Pixel breit ist, werden die Pixel entweder in der theoretischen Linie zentriert oder bis zu einer Seite der theoretischen Linie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cb9c5-107">If you draw a line that is more than one pixel wide, the pixels are either centered on the theoretical line or appear to one side of the theoretical line.</span></span> <span data-ttu-id="cb9c5-108">Sie können die Eigenschaft Pen Alignment eines festlegen <xref:System.Drawing.Pen> , um zu bestimmen, wie die mit diesem Stift gezeichneten Pixel in Bezug auf die theoretischen Linien positioniert werden.</span><span class="sxs-lookup"><span data-stu-id="cb9c5-108">You can set the pen alignment property of a <xref:System.Drawing.Pen> to determine how the pixels drawn with that pen will be positioned relative to theoretical lines.</span></span>  
  
 <span data-ttu-id="cb9c5-109">Die Werte <xref:System.Drawing.Drawing2D.PenAlignment.Center> , <xref:System.Drawing.Drawing2D.PenAlignment.Outset> und <xref:System.Drawing.Drawing2D.PenAlignment.Inset> , die in den folgenden Codebeispielen angezeigt werden, sind Member der- <xref:System.Drawing.Drawing2D.PenAlignment> Enumeration.</span><span class="sxs-lookup"><span data-stu-id="cb9c5-109">The values <xref:System.Drawing.Drawing2D.PenAlignment.Center>, <xref:System.Drawing.Drawing2D.PenAlignment.Outset>, and <xref:System.Drawing.Drawing2D.PenAlignment.Inset> that appear in the following code examples are members of the <xref:System.Drawing.Drawing2D.PenAlignment> enumeration.</span></span>  
  
 <span data-ttu-id="cb9c5-110">Im folgenden Codebeispiel wird eine Linie zweimal gezeichnet: einmal mit einem schwarzen Stift der Breite 1 und einmal mit einem grünen Stift der Breite 10.</span><span class="sxs-lookup"><span data-stu-id="cb9c5-110">The following code example draws a line twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span>  
  
### <a name="to-vary-the-width-of-a-pen"></a><span data-ttu-id="cb9c5-111">So verändern Sie die Breite eines Stifts</span><span class="sxs-lookup"><span data-stu-id="cb9c5-111">To vary the width of a pen</span></span>  
  
- <span data-ttu-id="cb9c5-112">Legen Sie den Wert der- <xref:System.Drawing.Pen.Alignment%2A> Eigenschaft auf <xref:System.Drawing.Drawing2D.PenAlignment.Center> (die Standardeinstellung) fest, um anzugeben, dass die mit dem grünen Stift gezeichneten Pixel auf der theoretischen Linie zentriert werden.</span><span class="sxs-lookup"><span data-stu-id="cb9c5-112">Set the value of the <xref:System.Drawing.Pen.Alignment%2A> property to <xref:System.Drawing.Drawing2D.PenAlignment.Center> (the default) to specify that pixels drawn with the green pen will be centered on the theoretical line.</span></span> <span data-ttu-id="cb9c5-113">Die folgende Abbildung zeigt die resultierende Zeile.</span><span class="sxs-lookup"><span data-stu-id="cb9c5-113">The following illustration shows the resulting line.</span></span>  
  
     ![Eine schwarze dünne Linie mit grüner Hervorhebung.](./media/how-to-set-pen-width-and-alignment/green-pixels-centered-line.gif)  
  
     <span data-ttu-id="cb9c5-115">Im folgenden Codebeispiel wird ein Rechteck zweimal gezeichnet: einmal mit einem schwarzen Stift der Breite 1 und einmal mit einem grünen Stift der Breite 10.</span><span class="sxs-lookup"><span data-stu-id="cb9c5-115">The following code example draws a rectangle twice: once with a black pen of width 1 and once with a green pen of width 10.</span></span>  
  
     [!code-csharp[System.Drawing.UsingAPen#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#41)]
     [!code-vb[System.Drawing.UsingAPen#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#41)]  
  
### <a name="to-change-the-alignment-of-a-pen"></a><span data-ttu-id="cb9c5-116">So ändern Sie die Ausrichtung eines Stifts</span><span class="sxs-lookup"><span data-stu-id="cb9c5-116">To change the alignment of a pen</span></span>  
  
- <span data-ttu-id="cb9c5-117">Legen Sie den Wert der-Eigenschaft auf fest, <xref:System.Drawing.Pen.Alignment%2A> <xref:System.Drawing.Drawing2D.PenAlignment.Center> um anzugeben, dass die mit dem grünen Stift gezeichneten Pixel auf der Grenze des Rechtecks zentriert werden.</span><span class="sxs-lookup"><span data-stu-id="cb9c5-117">Set the value of the <xref:System.Drawing.Pen.Alignment%2A> property to <xref:System.Drawing.Drawing2D.PenAlignment.Center> to specify that the pixels drawn with the green pen will be centered on the boundary of the rectangle.</span></span>  
  
     <span data-ttu-id="cb9c5-118">Die folgende Abbildung zeigt das resultierende Rechteck:</span><span class="sxs-lookup"><span data-stu-id="cb9c5-118">The following illustration shows the resulting rectangle:</span></span>
  
     ![Ein Rechteck, das mit schwarzen, schmalen Linien mit grüner Hervorhebung gezeichnet wird.](./media/how-to-set-pen-width-and-alignment/green-pixels-centered-rectangle.gif)  
  
     [!code-csharp[System.Drawing.UsingAPen#42](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#42)]
     [!code-vb[System.Drawing.UsingAPen#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#42)]  
  
### <a name="to-create-an-inset-pen"></a><span data-ttu-id="cb9c5-120">So erstellen Sie einen einfügen-Stift</span><span class="sxs-lookup"><span data-stu-id="cb9c5-120">To create an inset pen</span></span>  
  
- <span data-ttu-id="cb9c5-121">Ändern Sie die Ausrichtung des grünen Stifts, indem Sie die dritte Anweisung im vorangehenden Codebeispiel wie folgt ändern:</span><span class="sxs-lookup"><span data-stu-id="cb9c5-121">Change the green pen's alignment by modifying the third statement in the preceding code example as follows:</span></span>  
  
     [!code-csharp[System.Drawing.UsingAPen#43](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#43)]
     [!code-vb[System.Drawing.UsingAPen#43](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#43)]  
  
     <span data-ttu-id="cb9c5-122">Nun werden die Pixel in der Breite grünen Linie im Inneren des Rechtecks angezeigt, wie in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="cb9c5-122">Now the pixels in the wide green line appear on the inside of the rectangle as shown in the following illustration:</span></span>
  
     ![Ein Rechteck, das mit schwarzen Linien mit der Breite grünen Linie in gezeichnet wird.](./media/how-to-set-pen-width-and-alignment/green-pixels-inside-rectangle.gif)  
  
## <a name="see-also"></a><span data-ttu-id="cb9c5-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb9c5-124">See also</span></span>

- [<span data-ttu-id="cb9c5-125">Verwenden eines Stifts zum Zeichnen von Linien und Formen</span><span class="sxs-lookup"><span data-stu-id="cb9c5-125">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
- [<span data-ttu-id="cb9c5-126">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cb9c5-126">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
