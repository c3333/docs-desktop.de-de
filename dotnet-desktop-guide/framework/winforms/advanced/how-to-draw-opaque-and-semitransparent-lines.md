---
title: 'Vorgehensweise: Zeichnen deckender und halbtransparenter Linien'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drawing [Windows Forms], lines
- transparency [Windows Forms], lines
- lines [Windows Forms], drawing alpha blended
- alpha blending [Windows Forms], drawing lines
ms.assetid: 8f2508af-f495-4223-b5cc-646cbbb520eb
ms.openlocfilehash: 547c748451e9f7f91dcbe7595d4418835bac9f67
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975930"
---
# <a name="how-to-draw-opaque-and-semitransparent-lines"></a><span data-ttu-id="f799c-102">Vorgehensweise: Zeichnen deckender und halbtransparenter Linien</span><span class="sxs-lookup"><span data-stu-id="f799c-102">How to: Draw Opaque and Semitransparent Lines</span></span>
<span data-ttu-id="f799c-103">Wenn Sie eine Linie zeichnen, müssen Sie ein <xref:System.Drawing.Pen>-Objekt an die <xref:System.Drawing.Graphics.DrawLine%2A>-Methode der <xref:System.Drawing.Graphics>-Klasse übergeben.</span><span class="sxs-lookup"><span data-stu-id="f799c-103">When you draw a line, you must pass a <xref:System.Drawing.Pen> object to the <xref:System.Drawing.Graphics.DrawLine%2A> method of the <xref:System.Drawing.Graphics> class.</span></span> <span data-ttu-id="f799c-104">Einer der Parameter des <xref:System.Drawing.Pen.%23ctor%2A>-Konstruktors ist ein <xref:System.Drawing.Color>-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f799c-104">One of the parameters of the <xref:System.Drawing.Pen.%23ctor%2A> constructor is a <xref:System.Drawing.Color> object.</span></span> <span data-ttu-id="f799c-105">Um eine nicht transparente Linie zu zeichnen, legen Sie den Alphaanteil der Farbe auf 255 fest.</span><span class="sxs-lookup"><span data-stu-id="f799c-105">To draw an opaque line, set the alpha component of the color to 255.</span></span> <span data-ttu-id="f799c-106">Um eine halb transparente Linie zu zeichnen, legen Sie den Alphaanteil auf einen beliebigen Wert von 1 bis 254 fest.</span><span class="sxs-lookup"><span data-stu-id="f799c-106">To draw a semitransparent line, set the alpha component to any value from 1 through 254.</span></span>  
  
 <span data-ttu-id="f799c-107">Wenn Sie eine halb transparente Linie vor einem Hintergrund zeichnen, wird Linienfarbe mit den Hintergrundfarben gemischt.</span><span class="sxs-lookup"><span data-stu-id="f799c-107">When you draw a semitransparent line over a background, the color of the line is blended with the colors of the background.</span></span> <span data-ttu-id="f799c-108">Mit dem Alphaanteil wird das Mischungsverhältnis zwischen Linien- und Hintergrundfarben angegeben. Bei Alphawerten nahe 0 werden die Hintergrundfarben höher gewichtet, und bei Alphawerten nahe 255 wird die Linienfarbe höher gewichtet.</span><span class="sxs-lookup"><span data-stu-id="f799c-108">The alpha component specifies how the line and background colors are mixed; alpha values near 0 place more weight on the background colors, and alpha values near 255 place more weight on the line color.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f799c-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f799c-109">Example</span></span>  
 <span data-ttu-id="f799c-110">Im folgenden Beispiel werden erst eine Bitmap und dann drei Linien gezeichnet, die die Bitmap als Hintergrund verwenden.</span><span class="sxs-lookup"><span data-stu-id="f799c-110">The following example draws a bitmap and then draws three lines that use the bitmap as a background.</span></span> <span data-ttu-id="f799c-111">Für die erste Linie wird ein Alphaanteil von 255 verwendet. Die Linie ist daher nicht transparent.</span><span class="sxs-lookup"><span data-stu-id="f799c-111">The first line uses an alpha component of 255, so it is opaque.</span></span> <span data-ttu-id="f799c-112">Die zweite und die dritte Linie verwenden einen Alphaanteil von 128. Sie sind daher halb transparent. Das Hintergrundbild scheint also durch die Linien hindurch.</span><span class="sxs-lookup"><span data-stu-id="f799c-112">The second and third lines use an alpha component of 128, so they are semitransparent; you can see the background image through the lines.</span></span> <span data-ttu-id="f799c-113">Die Anweisung, mit der die <xref:System.Drawing.Graphics.CompositingQuality%2A>-Eigenschaft festgelegt wird, sorgt dafür, dass die Mischung für die dritte Linie unter Verwendung der Gammakorrektur erfolgt.</span><span class="sxs-lookup"><span data-stu-id="f799c-113">The statement that sets the <xref:System.Drawing.Graphics.CompositingQuality%2A> property causes the blending for the third line to be done in conjunction with gamma correction.</span></span>  
  
 [!code-csharp[System.Drawing.AlphaBlending#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlphaBlending/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.AlphaBlending#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlphaBlending/VB/Class1.vb#11)]  
  
 <span data-ttu-id="f799c-114">Die folgende Abbildung zeigt die Ausgabe des folgenden Codes:</span><span class="sxs-lookup"><span data-stu-id="f799c-114">The following illustration shows the output of the following code:</span></span>  
  
 ![Darstellung der nicht transparenten und halbtransparenten Ausgabe](./media/how-to-draw-opaque-and-semitransparent-lines/opaque-semitransparent-lines.png)  

## <a name="compiling-the-code"></a><span data-ttu-id="f799c-116">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="f799c-116">Compiling the Code</span></span>  
 <span data-ttu-id="f799c-117">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="f799c-117">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f799c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f799c-118">See also</span></span>

- [<span data-ttu-id="f799c-119">Alphablending von Linien und Füllungen</span><span class="sxs-lookup"><span data-stu-id="f799c-119">Alpha Blending Lines and Fills</span></span>](alpha-blending-lines-and-fills.md)
- [<span data-ttu-id="f799c-120">Vorgehensweise: Verwenden eines transparenten Hintergrunds für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="f799c-120">How to: Give Your Control a Transparent Background</span></span>](../controls/how-to-give-your-control-a-transparent-background.md)
- [<span data-ttu-id="f799c-121">Vorgehensweise: Zeichnen mit nicht transparenten und halb transparenten Pinseln</span><span class="sxs-lookup"><span data-stu-id="f799c-121">How to: Draw with Opaque and Semitransparent Brushes</span></span>](how-to-draw-with-opaque-and-semitransparent-brushes.md)
