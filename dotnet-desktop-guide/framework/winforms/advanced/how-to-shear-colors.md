---
title: 'Vorgehensweise: Scheren von Farben'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors [Windows Forms], transforming with color matrices
- colors [Windows Forms], shearing
ms.assetid: 0a424171-5b8b-45c4-afef-e9720a6c3e22
ms.openlocfilehash: 825e5a90ebb0d9df3b894ce7bd353e917b676939
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975876"
---
# <a name="how-to-shear-colors"></a><span data-ttu-id="e33c5-102">Vorgehensweise: Scheren von Farben</span><span class="sxs-lookup"><span data-stu-id="e33c5-102">How to: Shear Colors</span></span>
<span data-ttu-id="e33c5-103">Durch das Scheren wird eine Farbkomponente um einen in einer anderen Farbkomponente proportionalen Betrag vergrößert oder verringert.</span><span class="sxs-lookup"><span data-stu-id="e33c5-103">Shearing increases or decreases a color component by an amount proportional to another color component.</span></span> <span data-ttu-id="e33c5-104">Nehmen Sie z. b. die Transformation, bei der die rote Komponente um einen halben Wert der blauen Komponente erweitert wird.</span><span class="sxs-lookup"><span data-stu-id="e33c5-104">For example, consider the transformation where the red component is increased by one half the value of the blue component.</span></span> <span data-ttu-id="e33c5-105">Bei einer solchen Transformation würde die Farbe (0,2, 0,5, 1) zu (0,7, 0,5, 1) werden.</span><span class="sxs-lookup"><span data-stu-id="e33c5-105">Under such a transformation, the color (0.2, 0.5, 1) would become (0.7, 0.5, 1).</span></span> <span data-ttu-id="e33c5-106">Die neue rote Komponente ist 0,2 + (1/2) (1) = 0,7.</span><span class="sxs-lookup"><span data-stu-id="e33c5-106">The new red component is 0.2 + (1/2)(1) = 0.7.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e33c5-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e33c5-107">Example</span></span>  
 <span data-ttu-id="e33c5-108">Im folgenden Beispiel wird ein- <xref:System.Drawing.Image> Objekt aus der Datei ColorBars4.bmp erstellt.</span><span class="sxs-lookup"><span data-stu-id="e33c5-108">The following example constructs an <xref:System.Drawing.Image> object from the file ColorBars4.bmp.</span></span> <span data-ttu-id="e33c5-109">Anschließend wendet der Code die im vorherigen Absatz beschriebene Scheren Transformation auf jedes Pixel im Bild an.</span><span class="sxs-lookup"><span data-stu-id="e33c5-109">Then the code applies the shearing transformation described in the preceding paragraph to each pixel in the image.</span></span>  
  
 <span data-ttu-id="e33c5-110">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das auf der rechten Seite gelauftene Bild:</span><span class="sxs-lookup"><span data-stu-id="e33c5-110">The following illustration shows the original image on the left and the sheared image on the right:</span></span>
  
 ![Zwei Quadrate mit farbiger farbiger Seite und Darstellung des ursprünglichen Bilds und des gerenderten Bilds.](./media/how-to-shear-colors/original-image-sheared-image.png)  
  
 <span data-ttu-id="e33c5-112">In der folgenden Tabelle sind die Farb Vektoren für die vier Balken vor und nach der Transformation für das Scheren-Diagramm aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e33c5-112">The following table lists the color vectors for the four bars before and after the shearing transformation.</span></span>  
  
|<span data-ttu-id="e33c5-113">Original</span><span class="sxs-lookup"><span data-stu-id="e33c5-113">Original</span></span>|<span data-ttu-id="e33c5-114">Zert</span><span class="sxs-lookup"><span data-stu-id="e33c5-114">Sheared</span></span>|  
|--------------|-------------|  
|<span data-ttu-id="e33c5-115">(0, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="e33c5-115">(0, 0, 1, 1)</span></span>|<span data-ttu-id="e33c5-116">(0.5, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="e33c5-116">(0.5, 0, 1, 1)</span></span>|  
|<span data-ttu-id="e33c5-117">(0.5, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="e33c5-117">(0.5, 1, 0.5, 1)</span></span>|<span data-ttu-id="e33c5-118">(0.75, 1, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="e33c5-118">(0.75, 1, 0.5, 1)</span></span>|  
|<span data-ttu-id="e33c5-119">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="e33c5-119">(1, 1, 0, 1)</span></span>|<span data-ttu-id="e33c5-120">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="e33c5-120">(1, 1, 0, 1)</span></span>|  
|<span data-ttu-id="e33c5-121">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="e33c5-121">(0.4, 0.4, 0.4, 1)</span></span>|<span data-ttu-id="e33c5-122">(0.6, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="e33c5-122">(0.6, 0.4, 0.4, 1)</span></span>|  
  
 [!code-csharp[System.Drawing.Misc3#9](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Misc3/CS/Form1.cs#9)]
 [!code-vb[System.Drawing.Misc3#9](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Misc3/VB/Form1.vb#9)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="e33c5-123">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="e33c5-123">Compiling the Code</span></span>  
 <span data-ttu-id="e33c5-124">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="e33c5-124">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="e33c5-125">Ersetzen `ColorBars.bmp` Sie dies durch einen Bildnamen und einen Pfad, der auf Ihrem System gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e33c5-125">Replace `ColorBars.bmp` with an image name and path valid on your system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e33c5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e33c5-126">See also</span></span>

- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [<span data-ttu-id="e33c5-127">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e33c5-127">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="e33c5-128">Neueinfärben von Bildern</span><span class="sxs-lookup"><span data-stu-id="e33c5-128">Recoloring Images</span></span>](recoloring-images.md)
