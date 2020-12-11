---
title: 'Vorgehensweise: Verwenden des Mischmodus zum Steuern des Alphablendings'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- alpha blending [Windows Forms], compositing
- colors [Windows Forms], blending
- colors [Windows Forms], controlling transparency
ms.assetid: f331df2d-b395-4b0a-95be-24fec8c9bbb5
ms.openlocfilehash: 6863e59efa25323f80933bf8ab595316b430ef53
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976102"
---
# <a name="how-to-use-compositing-mode-to-control-alpha-blending"></a><span data-ttu-id="8be49-102">Vorgehensweise: Verwenden des Mischmodus zum Steuern des Alphablendings</span><span class="sxs-lookup"><span data-stu-id="8be49-102">How to: Use Compositing Mode to Control Alpha Blending</span></span>
<span data-ttu-id="8be49-103">Es kann vorkommen, dass Sie eine Offscreen-Bitmap erstellen möchten, die über die folgenden Eigenschaften verfügt:</span><span class="sxs-lookup"><span data-stu-id="8be49-103">There may be times when you want to create an off-screen bitmap that has the following characteristics:</span></span>  
  
- <span data-ttu-id="8be49-104">Farben haben alpha-Werte, die kleiner als 255 sind.</span><span class="sxs-lookup"><span data-stu-id="8be49-104">Colors have alpha values that are less than 255.</span></span>  
  
- <span data-ttu-id="8be49-105">Farben werden bei der Erstellung der Bitmap nicht mit einander gemischt.</span><span class="sxs-lookup"><span data-stu-id="8be49-105">Colors are not alpha blended with each other as you create the bitmap.</span></span>  
  
- <span data-ttu-id="8be49-106">Wenn Sie die fertige Bitmap anzeigen, werden Farben in der Bitmap mit den Hintergrundfarben auf dem Anzeigegerät gemischt.</span><span class="sxs-lookup"><span data-stu-id="8be49-106">When you display the finished bitmap, colors in the bitmap are alpha blended with the background colors on the display device.</span></span>  
  
 <span data-ttu-id="8be49-107">Um eine solche Bitmap zu erstellen, erstellen Sie ein leeres <xref:System.Drawing.Bitmap> -Objekt, und erstellen Sie dann ein- <xref:System.Drawing.Graphics> Objekt, das auf dieser Bitmap basiert.</span><span class="sxs-lookup"><span data-stu-id="8be49-107">To create such a bitmap, construct a blank <xref:System.Drawing.Bitmap> object, and then construct a <xref:System.Drawing.Graphics> object based on that bitmap.</span></span> <span data-ttu-id="8be49-108">Legen Sie den Zusammensetzung-Modus des- <xref:System.Drawing.Graphics> Objekts auf fest <xref:System.Drawing.Drawing2D.CompositingMode.SourceCopy?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="8be49-108">Set the compositing mode of the <xref:System.Drawing.Graphics> object to <xref:System.Drawing.Drawing2D.CompositingMode.SourceCopy?displayProperty=nameWithType>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="8be49-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8be49-109">Example</span></span>  
 <span data-ttu-id="8be49-110">Im folgenden Beispiel wird ein- <xref:System.Drawing.Graphics> Objekt basierend auf einem- <xref:System.Drawing.Bitmap> Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="8be49-110">The following example creates a <xref:System.Drawing.Graphics> object based on a <xref:System.Drawing.Bitmap> object.</span></span> <span data-ttu-id="8be49-111">Der Code verwendet das- <xref:System.Drawing.Graphics> Objekt zusammen mit zwei semitransparenten Pinseln (Alpha = 160), um die Bitmap zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="8be49-111">The code uses the <xref:System.Drawing.Graphics> object along with two semitransparent brushes (alpha = 160) to paint on the bitmap.</span></span> <span data-ttu-id="8be49-112">Der Code füllt eine rote Ellipse und eine grüne Ellipse mithilfe der semitransparenten Pinsel.</span><span class="sxs-lookup"><span data-stu-id="8be49-112">The code fills a red ellipse and a green ellipse using the semitransparent brushes.</span></span> <span data-ttu-id="8be49-113">Die grüne Ellipse überlappt die rote Ellipse, das grüne wird jedoch nicht mit der roten Ellipse kombiniert, da der Zusammensetzung-Modus des- <xref:System.Drawing.Graphics> Objekts auf festgelegt ist <xref:System.Drawing.Drawing2D.CompositingMode.SourceCopy> .</span><span class="sxs-lookup"><span data-stu-id="8be49-113">The green ellipse overlaps the red ellipse, but the green is not blended with the red because the compositing mode of the <xref:System.Drawing.Graphics> object is set to <xref:System.Drawing.Drawing2D.CompositingMode.SourceCopy>.</span></span>  
  
 <span data-ttu-id="8be49-114">Der Code zeichnet die Bitmap zweimal auf dem Bildschirm: einmal auf einem weißen Hintergrund und einmal in einem mehrfarbigen Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="8be49-114">The code draws the bitmap on the screen twice: once on a white background and once on a multicolored background.</span></span> <span data-ttu-id="8be49-115">Die Pixel in der Bitmap, die Teil der beiden Ellipsen sind, haben eine Alpha Komponente von 160, sodass die Ellipsen mit den Hintergrundfarben auf dem Bildschirm kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="8be49-115">The pixels in the bitmap that are part of the two ellipses have an alpha component of 160, so the ellipses are blended with the background colors on the screen.</span></span>  
  
 <span data-ttu-id="8be49-116">Die folgende Abbildung zeigt die Ausgabe des Code Beispiels.</span><span class="sxs-lookup"><span data-stu-id="8be49-116">The following illustration shows the output of the code example.</span></span> <span data-ttu-id="8be49-117">Beachten Sie, dass die Ellipsen mit dem Hintergrund kombiniert werden, aber nicht miteinander vermischt werden.</span><span class="sxs-lookup"><span data-stu-id="8be49-117">Note that the ellipses are blended with the background, but they are not blended with each other.</span></span>  
  
 ![Das Diagramm zeigt Ellipsen, die mit dem Hintergrund gemischt sind, nicht gegenseitig.](./media/how-to-use-compositing-mode-to-control-alpha-blending/ellipses-blended-background.png)  
  
 <span data-ttu-id="8be49-119">Das Codebeispiel enthält diese Anweisung:</span><span class="sxs-lookup"><span data-stu-id="8be49-119">The code example contains this statement:</span></span>  
  
 [!code-csharp[System.Drawing.AlphaBlending#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlphaBlending/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.AlphaBlending#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlphaBlending/VB/Class1.vb#41)]  
  
 <span data-ttu-id="8be49-120">Wenn Sie möchten, dass die Ellipsen miteinander und mit dem Hintergrund kombiniert werden sollen, ändern Sie die Anweisung wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8be49-120">If you want the ellipses to be blended with each other as well as with the background, change that statement to the following:</span></span>  
  
 [!code-csharp[System.Drawing.AlphaBlending#42](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlphaBlending/CS/Class1.cs#42)]
 [!code-vb[System.Drawing.AlphaBlending#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlphaBlending/VB/Class1.vb#42)]  
  
 <span data-ttu-id="8be49-121">Die folgende Abbildung zeigt die Ausgabe des überarbeiteten Codes.</span><span class="sxs-lookup"><span data-stu-id="8be49-121">The following illustration shows the output of the revised code.</span></span>  
  
 ![Diagramm, das Ellipsen zeigt, die miteinander gemischt und mit Hintergrund kombiniert werden.](./media/how-to-use-compositing-mode-to-control-alpha-blending/blend-ellipses-background.png)  
  
 [!code-csharp[System.Drawing.AlphaBlending#43](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.AlphaBlending/CS/Class1.cs#43)]
 [!code-vb[System.Drawing.AlphaBlending#43](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.AlphaBlending/VB/Class1.vb#43)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="8be49-123">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="8be49-123">Compiling the Code</span></span>  
 <span data-ttu-id="8be49-124">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .</span><span class="sxs-lookup"><span data-stu-id="8be49-124">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8be49-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8be49-125">See also</span></span>

- <xref:System.Drawing.Color.FromArgb%2A>
- [<span data-ttu-id="8be49-126">Alphablending von Linien und Füllungen</span><span class="sxs-lookup"><span data-stu-id="8be49-126">Alpha Blending Lines and Fills</span></span>](alpha-blending-lines-and-fills.md)
