---
title: 'Vorgehensweise: Verschieben von Bildfarben'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitmaps [Windows Forms], changing colors
- images [Windows Forms], changing colors
- image colors [Windows Forms]
ms.assetid: 2106fb9a-4d60-4dcf-9220-9f189a6c4d19
ms.openlocfilehash: fb9ec30c06740214b8dc6b65d32eba4e2920c89b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976111"
---
# <a name="how-to-translate-image-colors"></a><span data-ttu-id="c1177-102">Vorgehensweise: Verschieben von Bildfarben</span><span class="sxs-lookup"><span data-stu-id="c1177-102">How to: Translate Image Colors</span></span>
<span data-ttu-id="c1177-103">Eine Übersetzung Fügt einer oder mehreren der vier Farbkomponenten einen Wert hinzu.</span><span class="sxs-lookup"><span data-stu-id="c1177-103">A translation adds a value to one or more of the four color components.</span></span> <span data-ttu-id="c1177-104">Die Farbmatrix Einträge, die Übersetzungen darstellen, werden in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="c1177-104">The color matrix entries that represent translations are given in the following table.</span></span>  
  
|<span data-ttu-id="c1177-105">Zu über setzende Komponente</span><span class="sxs-lookup"><span data-stu-id="c1177-105">Component to be translated</span></span>|<span data-ttu-id="c1177-106">Matrix Eintrag</span><span class="sxs-lookup"><span data-stu-id="c1177-106">Matrix entry</span></span>|  
|--------------------------------|------------------|  
|<span data-ttu-id="c1177-107">Red</span><span class="sxs-lookup"><span data-stu-id="c1177-107">Red</span></span>|<span data-ttu-id="c1177-108">[4][0]</span><span class="sxs-lookup"><span data-stu-id="c1177-108">[4][0]</span></span>|  
|<span data-ttu-id="c1177-109">Grün</span><span class="sxs-lookup"><span data-stu-id="c1177-109">Green</span></span>|<span data-ttu-id="c1177-110">[4][1]</span><span class="sxs-lookup"><span data-stu-id="c1177-110">[4][1]</span></span>|  
|<span data-ttu-id="c1177-111">Blau</span><span class="sxs-lookup"><span data-stu-id="c1177-111">Blue</span></span>|<span data-ttu-id="c1177-112">[4][2]</span><span class="sxs-lookup"><span data-stu-id="c1177-112">[4][2]</span></span>|  
|<span data-ttu-id="c1177-113">Alpha</span><span class="sxs-lookup"><span data-stu-id="c1177-113">Alpha</span></span>|<span data-ttu-id="c1177-114">[4][3]</span><span class="sxs-lookup"><span data-stu-id="c1177-114">[4][3]</span></span>|  
  
## <a name="example"></a><span data-ttu-id="c1177-115">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c1177-115">Example</span></span>  
 <span data-ttu-id="c1177-116">Im folgenden Beispiel wird ein- <xref:System.Drawing.Image> Objekt aus der Datei ColorBars.bmp erstellt.</span><span class="sxs-lookup"><span data-stu-id="c1177-116">The following example constructs an <xref:System.Drawing.Image> object from the file ColorBars.bmp.</span></span> <span data-ttu-id="c1177-117">Anschließend fügt der Code der roten Komponente jedes Pixels im Bild 0,75 hinzu.</span><span class="sxs-lookup"><span data-stu-id="c1177-117">Then the code adds 0.75 to the red component of each pixel in the image.</span></span> <span data-ttu-id="c1177-118">Das ursprüngliche Bild wird neben dem transformierten Bild gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c1177-118">The original image is drawn alongside the transformed image.</span></span>  
  
 <span data-ttu-id="c1177-119">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das transformierte Bild auf der rechten Seite an:</span><span class="sxs-lookup"><span data-stu-id="c1177-119">The following illustration shows the original image on the left and the transformed image on the right:</span></span>  
  
 ![Screenshot des ursprünglichen und transformierten Bilds.](./media/how-to-translate-image-colors/original-image-translate-colors.png)  
  
 <span data-ttu-id="c1177-121">In der folgenden Tabelle sind die Farb Vektoren für die vier Balken vor und nach der roten Übersetzung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c1177-121">The following table lists the color vectors for the four bars before and after the red translation.</span></span> <span data-ttu-id="c1177-122">Beachten Sie, dass die rote Komponente in der zweiten Zeile nicht geändert wird, da der Höchstwert für eine Farbkomponente 1 ist.</span><span class="sxs-lookup"><span data-stu-id="c1177-122">Note that because the maximum value for a color component is 1, the red component in the second row does not change.</span></span> <span data-ttu-id="c1177-123">(Auf ähnliche Weise ist der minimale Wert für eine Farbkomponente 0.)</span><span class="sxs-lookup"><span data-stu-id="c1177-123">(Similarly, the minimum value for a color component is 0.)</span></span>  
  
|<span data-ttu-id="c1177-124">Original</span><span class="sxs-lookup"><span data-stu-id="c1177-124">Original</span></span>|<span data-ttu-id="c1177-125">Übersetzt</span><span class="sxs-lookup"><span data-stu-id="c1177-125">Translated</span></span>|  
|--------------|----------------|  
|<span data-ttu-id="c1177-126">Schwarz (0,0 (0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="c1177-126">Black (0, 0, 0, 1)</span></span>|<span data-ttu-id="c1177-127">(0.75, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="c1177-127">(0.75, 0, 0, 1)</span></span>|  
|<span data-ttu-id="c1177-128">Rot (1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="c1177-128">Red (1, 0, 0, 1)</span></span>|<span data-ttu-id="c1177-129">(1, 0, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="c1177-129">(1, 0, 0, 1)</span></span>|  
|<span data-ttu-id="c1177-130">Grün (0, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="c1177-130">Green (0, 1, 0, 1)</span></span>|<span data-ttu-id="c1177-131">(0.75, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="c1177-131">(0.75, 1, 0, 1)</span></span>|  
|<span data-ttu-id="c1177-132">Blau (0,0 (0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="c1177-132">Blue (0, 0, 1, 1)</span></span>|<span data-ttu-id="c1177-133">(0.75, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="c1177-133">(0.75, 0, 1, 1)</span></span>|  
  
 [!code-csharp[System.Drawing.RecoloringImages#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.RecoloringImages#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c1177-134">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="c1177-134">Compiling the Code</span></span>  
 <span data-ttu-id="c1177-135">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="c1177-135">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="c1177-136">Ersetzen `ColorBars.bmp` Sie dies durch einen Bilddateinamen und-Pfad, die auf Ihrem System gültig sind.</span><span class="sxs-lookup"><span data-stu-id="c1177-136">Replace `ColorBars.bmp` with an image file name and path that are valid on your system.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c1177-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1177-137">See also</span></span>

- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [<span data-ttu-id="c1177-138">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c1177-138">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="c1177-139">Neueinfärben von Bildern</span><span class="sxs-lookup"><span data-stu-id="c1177-139">Recoloring Images</span></span>](recoloring-images.md)
