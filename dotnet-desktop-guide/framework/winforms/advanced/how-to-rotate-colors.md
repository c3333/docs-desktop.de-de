---
title: 'Vorgehensweise: Drehen von Farben'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [Windows Forms], rotating
- examples [Windows Forms], rotating colors
ms.assetid: e2e4c300-159c-4f4a-9b56-103b0f7cbc05
ms.openlocfilehash: 8d2717dd7b819e963126072279b361fda02188bc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976137"
---
# <a name="how-to-rotate-colors"></a><span data-ttu-id="a51a2-102">Vorgehensweise: Drehen von Farben</span><span class="sxs-lookup"><span data-stu-id="a51a2-102">How to: Rotate Colors</span></span>
<span data-ttu-id="a51a2-103">Die Drehung in einem vierdimensionalen Farbraum ist schwierig zu visualisieren.</span><span class="sxs-lookup"><span data-stu-id="a51a2-103">Rotation in a four-dimensional color space is difficult to visualize.</span></span> <span data-ttu-id="a51a2-104">Wir können das Visualisieren der Rotation vereinfachen, indem wir akzeptieren, dass eine der Farbkomponenten korrigiert wird.</span><span class="sxs-lookup"><span data-stu-id="a51a2-104">We can make it easier to visualize rotation by agreeing to keep one of the color components fixed.</span></span> <span data-ttu-id="a51a2-105">Angenommen, die Alpha Komponente muss bei 1 (vollständig nicht transparent) korrigiert bleiben.</span><span class="sxs-lookup"><span data-stu-id="a51a2-105">Suppose we agree to keep the alpha component fixed at 1 (fully opaque).</span></span> <span data-ttu-id="a51a2-106">Anschließend können wir einen dreidimensionalen Farbraum mit roten, grünen und blauen Achsen visualisieren, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="a51a2-106">Then we can visualize a three-dimensional color space with red, green, and blue axes as shown in the following illustration.</span></span>  
  
 ![Abbildung, die die Drehung mit roten, grünen und blauen Achsen anzeigt.](./media/how-to-rotate-colors/rotation-red-green-blue-axes.gif)  
  
 <span data-ttu-id="a51a2-108">Eine Farbe kann als Punkt im 3D-Raum betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="a51a2-108">A color can be thought of as a point in 3D space.</span></span> <span data-ttu-id="a51a2-109">Der Punkt (1, 0, 0) im Raum stellt z. b. die Farbe rot dar, und der Punkt (0, 1, 0) im Raum stellt die Farbe grün dar.</span><span class="sxs-lookup"><span data-stu-id="a51a2-109">For example, the point (1, 0, 0) in space represents the color red, and the point (0, 1, 0) in space represents the color green.</span></span>  
  
 <span data-ttu-id="a51a2-110">In der folgenden Abbildung wird gezeigt, was es bedeutet, die Farbe (1, 0, 0) durch einen Winkel von 60 Grad in der Red-Green Ebene zu drehen.</span><span class="sxs-lookup"><span data-stu-id="a51a2-110">The following illustration shows what it means to rotate the color (1, 0, 0) through an angle of 60 degrees in the Red-Green plane.</span></span> <span data-ttu-id="a51a2-111">Die Drehung in einer Ebene parallel zur Red-Green Ebene kann als Drehung der blauen Achse betrachtet werden.</span><span class="sxs-lookup"><span data-stu-id="a51a2-111">Rotation in a plane parallel to the Red-Green plane can be thought of as rotation about the blue axis.</span></span>  
  
 ![Abbildung, die die Drehung der blauen Achse anzeigt.](./media/how-to-rotate-colors/rotation-about-blue-axis.gif)  
  
 <span data-ttu-id="a51a2-113">In der folgenden Abbildung wird gezeigt, wie eine Farbmatrix initialisiert wird, um Drehungen zu jeder der drei Koordinatenachsen (rot, grün, blau) auszuführen:</span><span class="sxs-lookup"><span data-stu-id="a51a2-113">The following illustration shows how to initialize a color matrix to perform rotations about each of the three coordinate axes (red, green, blue):</span></span>  
  
 ![Initialisieren Sie eine Farbmatrix, um Drehungen zu drei Achsen auszuführen.](./media/how-to-rotate-colors/rotation-about-three-axes.gif)  
  
## <a name="example"></a><span data-ttu-id="a51a2-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a51a2-115">Example</span></span>  
 <span data-ttu-id="a51a2-116">Im folgenden Beispiel wird ein Bild, das alle eine Farbe (1, 0, 0,6) ist, und eine 60-Grad-Drehung der blauen Achse angewendet.</span><span class="sxs-lookup"><span data-stu-id="a51a2-116">The following example takes an image that is all one color (1, 0, 0.6) and applies a 60-degree rotation about the blue axis.</span></span> <span data-ttu-id="a51a2-117">Der Winkel der Drehung wird in einer Ebene durchlaufen, die parallel zur roten grünen Ebene ist.</span><span class="sxs-lookup"><span data-stu-id="a51a2-117">The angle of the rotation is swept out in a plane that is parallel to the red-green plane.</span></span>  
  
 <span data-ttu-id="a51a2-118">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das Farb gedrehte Bild auf der rechten Seite an:</span><span class="sxs-lookup"><span data-stu-id="a51a2-118">The following illustration shows the original image on the left and the color-rotated image on the right:</span></span>  
  
 ![Abbildung, die das ursprüngliche Bild und das Farb gedrehte Bild anzeigt.](./media/how-to-rotate-colors/original-color-rotated-images.png)  
  
 <span data-ttu-id="a51a2-120">Die folgende Abbildung zeigt eine Visualisierung der Farb Drehung, die im folgenden Code ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="a51a2-120">The following illustration shows a visualization of the color rotation performed in the following code:</span></span>
  
 ![Abbildung, die die Visualisierung der Farb Drehung anzeigt.](./media/how-to-rotate-colors/visualization-color-rotation.gif)  
  
 [!code-csharp[System.Drawing.RotateColors#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RotateColors/CS/Form1.cs#1)]
 [!code-vb[System.Drawing.RotateColors#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RotateColors/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="a51a2-122">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="a51a2-122">Compiling the Code</span></span>  
 <span data-ttu-id="a51a2-123">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="a51a2-123">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="a51a2-124">Ersetzen `RotationInput.bmp` Sie dies durch einen Bilddateinamen und Pfad, der auf Ihrem System gültig ist.</span><span class="sxs-lookup"><span data-stu-id="a51a2-124">Replace `RotationInput.bmp` with an image file name and path valid on your system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a51a2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a51a2-125">See also</span></span>

- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [<span data-ttu-id="a51a2-126">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="a51a2-126">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="a51a2-127">Neueinfärben von Bildern</span><span class="sxs-lookup"><span data-stu-id="a51a2-127">Recoloring Images</span></span>](recoloring-images.md)
