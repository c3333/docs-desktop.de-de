---
title: Skalieren von Farben mithilfe von Transformationen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- transformations [Windows Forms], for scaling colors
- colors [Windows Forms], scaling
ms.assetid: df23c887-7fd6-4b15-ad94-e30b5bd4b849
ms.openlocfilehash: 81c0ddf5b937d604559a9eb1a8b598885546c97f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975830"
---
# <a name="using-transformations-to-scale-colors"></a><span data-ttu-id="3457c-102">Skalieren von Farben mithilfe von Transformationen</span><span class="sxs-lookup"><span data-stu-id="3457c-102">Using Transformations to Scale Colors</span></span>
<span data-ttu-id="3457c-103">Eine Skalierungs Transformation multipliziert eine oder mehrere der vier Farbkomponenten mit einer Zahl.</span><span class="sxs-lookup"><span data-stu-id="3457c-103">A scaling transformation multiplies one or more of the four color components by a number.</span></span> <span data-ttu-id="3457c-104">Die Farbmatrix Einträge, die die Skalierung darstellen, werden in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="3457c-104">The color matrix entries that represent scaling are given in the following table.</span></span>  
  
|<span data-ttu-id="3457c-105">Zu skalierbare Komponente</span><span class="sxs-lookup"><span data-stu-id="3457c-105">Component to be scaled</span></span>|<span data-ttu-id="3457c-106">Matrix Eintrag</span><span class="sxs-lookup"><span data-stu-id="3457c-106">Matrix entry</span></span>|  
|----------------------------|------------------|  
|<span data-ttu-id="3457c-107">Red</span><span class="sxs-lookup"><span data-stu-id="3457c-107">Red</span></span>|<span data-ttu-id="3457c-108">[0][0]</span><span class="sxs-lookup"><span data-stu-id="3457c-108">[0][0]</span></span>|  
|<span data-ttu-id="3457c-109">Grün</span><span class="sxs-lookup"><span data-stu-id="3457c-109">Green</span></span>|<span data-ttu-id="3457c-110">[1][1]</span><span class="sxs-lookup"><span data-stu-id="3457c-110">[1][1]</span></span>|  
|<span data-ttu-id="3457c-111">Blau</span><span class="sxs-lookup"><span data-stu-id="3457c-111">Blue</span></span>|<span data-ttu-id="3457c-112">[2][2]</span><span class="sxs-lookup"><span data-stu-id="3457c-112">[2][2]</span></span>|  
|<span data-ttu-id="3457c-113">Alpha</span><span class="sxs-lookup"><span data-stu-id="3457c-113">Alpha</span></span>|<span data-ttu-id="3457c-114">[3][3]</span><span class="sxs-lookup"><span data-stu-id="3457c-114">[3][3]</span></span>|  
  
## <a name="scaling-one-color"></a><span data-ttu-id="3457c-115">Skalieren einer Farbe</span><span class="sxs-lookup"><span data-stu-id="3457c-115">Scaling One Color</span></span>  
 <span data-ttu-id="3457c-116">Im folgenden Beispiel wird ein- <xref:System.Drawing.Image> Objekt aus der Datei ColorBars2.bmp erstellt.</span><span class="sxs-lookup"><span data-stu-id="3457c-116">The following example constructs an <xref:System.Drawing.Image> object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="3457c-117">Anschließend skaliert der Code die blaue Komponente jedes Pixels im Bild um den Faktor 2.</span><span class="sxs-lookup"><span data-stu-id="3457c-117">Then the code scales the blue component of each pixel in the image by a factor of 2.</span></span> <span data-ttu-id="3457c-118">Das ursprüngliche Bild wird neben dem transformierten Bild gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3457c-118">The original image is drawn alongside the transformed image.</span></span>  
  
 [!code-csharp[System.Drawing.RecoloringImages#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.RecoloringImages#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#41)]  
  
 <span data-ttu-id="3457c-119">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das skalierte Bild auf der rechten Seite an:</span><span class="sxs-lookup"><span data-stu-id="3457c-119">The following illustration shows the original image on the left and the scaled image on the right:</span></span>  
  
 ![Screenshot, der die ursprünglichen und skalierten Farben vergleicht.](./media/using-transformations-to-scale-colors/four-bar-scale-one-color.png)  
  
 <span data-ttu-id="3457c-121">In der folgenden Tabelle sind die Farb Vektoren für die vier Balken vor und nach der blauen Skalierung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3457c-121">The following table lists the color vectors for the four bars before and after the blue scaling.</span></span> <span data-ttu-id="3457c-122">Beachten Sie, dass die blaue Komponente in der vierten Farbleiste von 0,8 zu 0,6 gewechselt ist.</span><span class="sxs-lookup"><span data-stu-id="3457c-122">Note that the blue component in the fourth color bar went from 0.8 to 0.6.</span></span> <span data-ttu-id="3457c-123">Dies liegt daran, dass GDI+ nur den Bruch Teil des Ergebnisses beibehält.</span><span class="sxs-lookup"><span data-stu-id="3457c-123">That is because GDI+ retains only the fractional part of the result.</span></span> <span data-ttu-id="3457c-124">Beispiel: (2) (0,8) = 1,6 und der Bruchteil von 1,6 ist 0,6.</span><span class="sxs-lookup"><span data-stu-id="3457c-124">For example, (2)(0.8) = 1.6, and the fractional part of 1.6 is 0.6.</span></span> <span data-ttu-id="3457c-125">Wenn nur der Bruchteil beibehalten wird, wird sichergestellt, dass das Ergebnis immer im Intervall [0,0] liegt.</span><span class="sxs-lookup"><span data-stu-id="3457c-125">Retaining only the fractional part ensures that the result is always in the interval [0, 1].</span></span>  
  
|<span data-ttu-id="3457c-126">Original</span><span class="sxs-lookup"><span data-stu-id="3457c-126">Original</span></span>|<span data-ttu-id="3457c-127">Läufig</span><span class="sxs-lookup"><span data-stu-id="3457c-127">Scaled</span></span>|  
|--------------|------------|  
|<span data-ttu-id="3457c-128">(0.4, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-128">(0.4, 0.4, 0.4, 1)</span></span>|<span data-ttu-id="3457c-129">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-129">(0.4, 0.4, 0.8, 1)</span></span>|  
|<span data-ttu-id="3457c-130">(0.4, 0.2, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-130">(0.4, 0.2, 0.2, 1)</span></span>|<span data-ttu-id="3457c-131">(0.4, 0.2, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-131">(0.4, 0.2, 0.4, 1)</span></span>|  
|<span data-ttu-id="3457c-132">(0.2, 0.4, 0.2, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-132">(0.2, 0.4, 0.2, 1)</span></span>|<span data-ttu-id="3457c-133">(0.2, 0.4, 0.4, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-133">(0.2, 0.4, 0.4, 1)</span></span>|  
|<span data-ttu-id="3457c-134">(0.4, 0.4, 0.8, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-134">(0.4, 0.4, 0.8, 1)</span></span>|<span data-ttu-id="3457c-135">(0.4, 0.4, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-135">(0.4, 0.4, 0.6, 1)</span></span>|  
  
## <a name="scaling-multiple-colors"></a><span data-ttu-id="3457c-136">Skalieren mehrerer Farben</span><span class="sxs-lookup"><span data-stu-id="3457c-136">Scaling Multiple Colors</span></span>  
 <span data-ttu-id="3457c-137">Im folgenden Beispiel wird ein- <xref:System.Drawing.Image> Objekt aus der Datei ColorBars2.bmp erstellt.</span><span class="sxs-lookup"><span data-stu-id="3457c-137">The following example constructs an <xref:System.Drawing.Image> object from the file ColorBars2.bmp.</span></span> <span data-ttu-id="3457c-138">Anschließend werden im Code die roten, grünen und blauen Komponenten der einzelnen Pixel im Bild skaliert.</span><span class="sxs-lookup"><span data-stu-id="3457c-138">Then the code scales the red, green, and blue components of each pixel in the image.</span></span> <span data-ttu-id="3457c-139">Die roten Komponenten werden auf 25% herunterskaliert, die grünen Komponenten werden um 35% herunterskaliert, und die blauen Komponenten werden um 50% herunterskaliert.</span><span class="sxs-lookup"><span data-stu-id="3457c-139">The red components are scaled down 25 percent, the green components are scaled down 35 percent, and the blue components are scaled down 50 percent.</span></span>  
  
 [!code-csharp[System.Drawing.RecoloringImages#42](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#42)]
 [!code-vb[System.Drawing.RecoloringImages#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#42)]  
  
 <span data-ttu-id="3457c-140">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das skalierte Bild auf der rechten Seite an:</span><span class="sxs-lookup"><span data-stu-id="3457c-140">The following illustration shows the original image on the left and the scaled image on the right:</span></span>  
  
 ![Screenshot, der die ursprünglichen und skalierten Farben vergleicht.](./media/using-transformations-to-scale-colors/four-bar-scale-multiple-colors.png)  
  
 <span data-ttu-id="3457c-142">In der folgenden Tabelle sind die Farb Vektoren für die vier Balken vor und nach der roten, grünen und blauen Skalierung aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="3457c-142">The following table lists the color vectors for the four bars before and after the red, green and blue scaling.</span></span>  
  
|<span data-ttu-id="3457c-143">Original</span><span class="sxs-lookup"><span data-stu-id="3457c-143">Original</span></span>|<span data-ttu-id="3457c-144">Läufig</span><span class="sxs-lookup"><span data-stu-id="3457c-144">Scaled</span></span>|  
|--------------|------------|  
|<span data-ttu-id="3457c-145">(0.6, 0.6, 0.6, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-145">(0.6, 0.6, 0.6, 1)</span></span>|<span data-ttu-id="3457c-146">(0.45, 0.39, 0.3, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-146">(0.45, 0.39, 0.3, 1)</span></span>|  
|<span data-ttu-id="3457c-147">(0, 1, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-147">(0, 1, 1, 1)</span></span>|<span data-ttu-id="3457c-148">(0, 0.65, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-148">(0, 0.65, 0.5, 1)</span></span>|  
|<span data-ttu-id="3457c-149">(1, 1, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-149">(1, 1, 0, 1)</span></span>|<span data-ttu-id="3457c-150">(0.75, 0.65, 0, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-150">(0.75, 0.65, 0, 1)</span></span>|  
|<span data-ttu-id="3457c-151">(1, 0, 1, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-151">(1, 0, 1, 1)</span></span>|<span data-ttu-id="3457c-152">(0.75, 0, 0.5, 1)</span><span class="sxs-lookup"><span data-stu-id="3457c-152">(0.75, 0, 0.5, 1)</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="3457c-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3457c-153">See also</span></span>

- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [<span data-ttu-id="3457c-154">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3457c-154">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="3457c-155">Neueinfärben von Bildern</span><span class="sxs-lookup"><span data-stu-id="3457c-155">Recoloring Images</span></span>](recoloring-images.md)
