---
title: 'Vorgehensweise: Verwenden einer Farbmatrix zum Transformieren einer Farbe'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- image colors [Windows Forms], transforming
- color matrices [Windows Forms], using
ms.assetid: 44df4556-a433-49c0-ac0f-9a12063a5860
ms.openlocfilehash: 2df74e022b842f7e5c9ff80f6aeddfce51af5eab
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976116"
---
# <a name="how-to-use-a-color-matrix-to-transform-a-single-color"></a><span data-ttu-id="93b50-102">Vorgehensweise: Verwenden einer Farbmatrix zum Transformieren einer Farbe</span><span class="sxs-lookup"><span data-stu-id="93b50-102">How to: Use a Color Matrix to Transform a Single Color</span></span>
<span data-ttu-id="93b50-103">GDI+ stellt die <xref:System.Drawing.Image> -Klasse und die- <xref:System.Drawing.Bitmap> Klasse zum Speichern und Bearbeiten von Bildern bereit.</span><span class="sxs-lookup"><span data-stu-id="93b50-103">GDI+ provides the <xref:System.Drawing.Image> and <xref:System.Drawing.Bitmap> classes for storing and manipulating images.</span></span> <span data-ttu-id="93b50-104"><xref:System.Drawing.Image> -und <xref:System.Drawing.Bitmap> -Objekte speichern die Farbe jedes Pixels als 32-Bit-Zahl: 8 Bits für Rot, grün, blau und alpha.</span><span class="sxs-lookup"><span data-stu-id="93b50-104"><xref:System.Drawing.Image> and <xref:System.Drawing.Bitmap> objects store the color of each pixel as a 32-bit number: 8 bits each for red, green, blue, and alpha.</span></span> <span data-ttu-id="93b50-105">Jede der vier Komponenten ist eine Zahl zwischen 0 und 255, wobei 0 keine Intensität und 255 die volle Intensität darstellt.</span><span class="sxs-lookup"><span data-stu-id="93b50-105">Each of the four components is a number from 0 through 255, with 0 representing no intensity and 255 representing full intensity.</span></span> <span data-ttu-id="93b50-106">Die Alpha Komponente gibt die Transparenz der Farbe an: 0 ist vollständig transparent, und 255 ist vollständig undurchsichtig.</span><span class="sxs-lookup"><span data-stu-id="93b50-106">The alpha component specifies the transparency of the color: 0 is fully transparent, and 255 is fully opaque.</span></span>  
  
 <span data-ttu-id="93b50-107">Ein Farb Vektor ist ein 4-Tupel im Formular (rot, grün, blau, Alpha).</span><span class="sxs-lookup"><span data-stu-id="93b50-107">A color vector is a 4-tuple of the form (red, green, blue, alpha).</span></span> <span data-ttu-id="93b50-108">Der Farb Vektor (0, 255, 0, 255) stellt z. b. eine nicht transparente Farbe dar, die nicht rot oder blau ist, aber grün mit voller Intensität aufweist.</span><span class="sxs-lookup"><span data-stu-id="93b50-108">For example, the color vector (0, 255, 0, 255) represents an opaque color that has no red or blue, but has green at full intensity.</span></span>  
  
 <span data-ttu-id="93b50-109">Eine weitere Konvention für das darstellen von Farben verwendet die Zahl 1 für die volle Intensität.</span><span class="sxs-lookup"><span data-stu-id="93b50-109">Another convention for representing colors uses the number 1 for full intensity.</span></span> <span data-ttu-id="93b50-110">Mithilfe dieser Konvention würde die im vorangehenden Absatz beschriebene Farbe durch den Vektor (0, 1, 0, 1) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="93b50-110">Using that convention, the color described in the preceding paragraph would be represented by the vector (0, 1, 0, 1).</span></span> <span data-ttu-id="93b50-111">GDI+ verwendet die Konvention 1 als vollständige Intensität, wenn Farb Transformationen durchführt werden.</span><span class="sxs-lookup"><span data-stu-id="93b50-111">GDI+ uses the convention of 1 as full intensity when it performs color transformations.</span></span>  
  
 <span data-ttu-id="93b50-112">Sie können lineare Transformationen (Drehung, Skalierung und ähnliches) auf Farb Vektoren anwenden, indem Sie die Farb Vektoren mit einer 4 × 4-Matrix multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="93b50-112">You can apply linear transformations (rotation, scaling, and the like) to color vectors by multiplying the color vectors by a 4×4 matrix.</span></span> <span data-ttu-id="93b50-113">Es ist jedoch nicht möglich, eine 4 × 4-Matrix zum Durchführen einer Übersetzung (Nonlinear) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="93b50-113">However, you cannot use a 4×4 matrix to perform a translation (nonlinear).</span></span> <span data-ttu-id="93b50-114">Wenn Sie jedem der Farb Vektoren eine dummyminietkoordinate (z. b. die Zahl 1) hinzufügen, können Sie eine beliebige Kombination aus linearen Transformationen und Übersetzungen mit einer 5 × 5-Matrix anwenden.</span><span class="sxs-lookup"><span data-stu-id="93b50-114">If you add a dummy fifth coordinate (for example, the number 1) to each of the color vectors, you can use a 5×5 matrix to apply any combination of linear transformations and translations.</span></span> <span data-ttu-id="93b50-115">Eine Transformation, die aus einer linearen Transformation, gefolgt von einer Übersetzung, besteht, wird als affine Transformation bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="93b50-115">A transformation consisting of a linear transformation followed by a translation is called an affine transformation.</span></span>  
  
 <span data-ttu-id="93b50-116">Nehmen Sie beispielsweise an, Sie möchten mit der Farbe (0,2, 0,0, 0,4, 1,0) beginnen und die folgenden Transformationen anwenden:</span><span class="sxs-lookup"><span data-stu-id="93b50-116">For example, suppose you want to start with the color (0.2, 0.0, 0.4, 1.0) and apply the following transformations:</span></span>  
  
1. <span data-ttu-id="93b50-117">Doppelte der roten Komponente</span><span class="sxs-lookup"><span data-stu-id="93b50-117">Double the red component</span></span>  
  
2. <span data-ttu-id="93b50-118">Fügen Sie 0,2 der roten, grünen und blauen Komponenten hinzu.</span><span class="sxs-lookup"><span data-stu-id="93b50-118">Add 0.2 to the red, green, and blue components</span></span>  
  
 <span data-ttu-id="93b50-119">Die folgende Matrix Multiplikation führt das Transformations Paar in der aufgeführten Reihenfolge aus.</span><span class="sxs-lookup"><span data-stu-id="93b50-119">The following matrix multiplication will perform the pair of transformations in the order listed.</span></span>  
  
 ![Screenshot einer Transformationsmatrix für Transformationen.](./media/how-to-use-a-color-matrix-to-transform-a-single-color/multiplication-color-matrix.gif)
  
 <span data-ttu-id="93b50-121">Die Elemente einer Farbmatrix werden nach Zeile und Spalte indiziert (null basiert).</span><span class="sxs-lookup"><span data-stu-id="93b50-121">The elements of a color matrix are indexed (zero-based) by row and then column.</span></span> <span data-ttu-id="93b50-122">Der Eintrag in der fünften Zeile und die dritte Spalte der Matrix M werden z. b. durch M [4] [2] bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="93b50-122">For example, the entry in the fifth row and third column of matrix M is denoted by M[4][2].</span></span>  
  
 <span data-ttu-id="93b50-123">Die 5 × 5-Identitätsmatrix (in der folgenden Abbildung dargestellt) verfügt über 1 s auf der diagonalen und an allen anderen Orten.</span><span class="sxs-lookup"><span data-stu-id="93b50-123">The 5×5 identity matrix (shown in the following illustration) has 1s on the diagonal and 0s everywhere else.</span></span> <span data-ttu-id="93b50-124">Wenn Sie einen Farb Vektor anhand der Identitätsmatrix multiplizieren, wird der Farb Vektor nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="93b50-124">If you multiply a color vector by the identity matrix, the color vector does not change.</span></span> <span data-ttu-id="93b50-125">Eine bequeme Möglichkeit zum bilden der Matrix einer Farb Transformation besteht darin, mit der Identitätsmatrix zu beginnen und eine kleine Änderung vorzunehmen, die die gewünschte Transformation erzeugt.</span><span class="sxs-lookup"><span data-stu-id="93b50-125">A convenient way to form the matrix of a color transformation is to start with the identity matrix and make a small change that produces the desired transformation.</span></span>  
  
 ![Screenshot einer 5 x 5-Identitätsmatrix für die Farb Transformation.](./media/how-to-use-a-color-matrix-to-transform-a-single-color/5x5-identity-matrix-color-transformation.gif)  
  
 <span data-ttu-id="93b50-127">Eine ausführlichere Erörterung von Matrizen und Transformationen finden Sie unter [Koordinatensysteme und Transformationen](coordinate-systems-and-transformations.md).</span><span class="sxs-lookup"><span data-stu-id="93b50-127">For a more detailed discussion of matrices and transformations, see [Coordinate Systems and Transformations](coordinate-systems-and-transformations.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="93b50-128">Beispiel</span><span class="sxs-lookup"><span data-stu-id="93b50-128">Example</span></span>  
 <span data-ttu-id="93b50-129">Im folgenden Beispiel wird ein Bild mit allen Farben (0,2, 0,0, 0,4, 1,0) angenommen, und die in den vorherigen Abschnitten beschriebene Transformation wird angewendet.</span><span class="sxs-lookup"><span data-stu-id="93b50-129">The following example takes an image that is all one color (0.2, 0.0, 0.4, 1.0) and applies the transformation described in the preceding paragraphs.</span></span>  
  
 <span data-ttu-id="93b50-130">Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das transformierte Bild auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="93b50-130">The following illustration shows the original image on the left and the transformed image on the right.</span></span>  
  
 ![Ein Violettes Quadrat auf der linken Seite und ein Fuchsia-Quadrat auf der rechten Seite.](./media/how-to-use-a-color-matrix-to-transform-a-single-color/color-transformation.png)  
  
 <span data-ttu-id="93b50-132">Der Code im folgenden Beispiel verwendet die folgenden Schritte, um die Neueinfärbung durchzuführen:</span><span class="sxs-lookup"><span data-stu-id="93b50-132">The code in the following example uses the following steps to perform the recoloring:</span></span>  
  
1. <span data-ttu-id="93b50-133">Initialisieren Sie ein- <xref:System.Drawing.Imaging.ColorMatrix> Objekt.</span><span class="sxs-lookup"><span data-stu-id="93b50-133">Initialize a <xref:System.Drawing.Imaging.ColorMatrix> object.</span></span>  
  
2. <span data-ttu-id="93b50-134">Erstellen <xref:System.Drawing.Imaging.ImageAttributes> Sie ein-Objekt, und übergeben Sie das- <xref:System.Drawing.Imaging.ColorMatrix> Objekt an die- <xref:System.Drawing.Imaging.ImageAttributes.SetColorMatrix%2A> Methode des- <xref:System.Drawing.Imaging.ImageAttributes> Objekts.</span><span class="sxs-lookup"><span data-stu-id="93b50-134">Create an <xref:System.Drawing.Imaging.ImageAttributes> object and pass the <xref:System.Drawing.Imaging.ColorMatrix> object to the <xref:System.Drawing.Imaging.ImageAttributes.SetColorMatrix%2A> method of the <xref:System.Drawing.Imaging.ImageAttributes> object.</span></span>  
  
3. <span data-ttu-id="93b50-135">Übergeben Sie das- <xref:System.Drawing.Imaging.ImageAttributes> Objekt an die- <xref:System.Drawing.Graphics.DrawImage%2A> Methode eines- <xref:System.Drawing.Graphics> Objekts.</span><span class="sxs-lookup"><span data-stu-id="93b50-135">Pass the <xref:System.Drawing.Imaging.ImageAttributes> object to the <xref:System.Drawing.Graphics.DrawImage%2A> method of a <xref:System.Drawing.Graphics> object.</span></span>  
  
 [!code-csharp[System.Drawing.RecoloringImages#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.RecoloringImages#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#21)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="93b50-136">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="93b50-136">Compiling the Code</span></span>  
 <span data-ttu-id="93b50-137">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="93b50-137">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="93b50-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93b50-138">See also</span></span>

- [<span data-ttu-id="93b50-139">Neueinfärben von Bildern</span><span class="sxs-lookup"><span data-stu-id="93b50-139">Recoloring Images</span></span>](recoloring-images.md)
- [<span data-ttu-id="93b50-140">Koordinatensysteme und Transformationen</span><span class="sxs-lookup"><span data-stu-id="93b50-140">Coordinate Systems and Transformations</span></span>](coordinate-systems-and-transformations.md)
