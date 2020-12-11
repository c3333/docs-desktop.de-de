---
title: 'Vorgehensweise: Erstellen eines linearen Farbverlaufs'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- linear gradients [Windows Forms], creating
- gradients [Windows Forms], creating linear
- colors [Windows Forms], creating linear gradients
- gradients
ms.assetid: 6c88e1cc-1217-4399-ac12-cb37592b9f01
ms.openlocfilehash: e55d27b454579268658192ae56daa52e0b28bb83
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974988"
---
# <a name="how-to-create-a-linear-gradient"></a><span data-ttu-id="d7878-102">Vorgehensweise: Erstellen eines linearen Farbverlaufs</span><span class="sxs-lookup"><span data-stu-id="d7878-102">How to: Create a Linear Gradient</span></span>
<span data-ttu-id="d7878-103">GDI+ stellt horizontale, vertikale und diagonale lineare Farbverläufe bereit.</span><span class="sxs-lookup"><span data-stu-id="d7878-103">GDI+ provides horizontal, vertical, and diagonal linear gradients.</span></span> <span data-ttu-id="d7878-104">Standardmäßig ändert sich die Farbe in einem linearen Farbverlauf gleichmäßig.</span><span class="sxs-lookup"><span data-stu-id="d7878-104">By default, the color in a linear gradient changes uniformly.</span></span> <span data-ttu-id="d7878-105">Sie können jedoch einen linearen Farbverlauf anpassen, sodass sich die Farbe auf nicht einheitliche Weise ändert.</span><span class="sxs-lookup"><span data-stu-id="d7878-105">However, you can customize a linear gradient so that the color changes in a non-uniform fashion.</span></span>  

> [!NOTE]
> <span data-ttu-id="d7878-106">Die Beispiele in diesem Artikel sind Methoden, die vom-Ereignishandler eines Steuer Elements aufgerufen werden <xref:System.Windows.Forms.Control.Paint> .</span><span class="sxs-lookup"><span data-stu-id="d7878-106">The examples in this article are methods that are called from a control's <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  

<span data-ttu-id="d7878-107">Im folgenden Beispiel werden eine Linie, eine Ellipse und ein Rechteck mit einem horizontalen linearen Farbverlaufs Pinsel gefüllt.</span><span class="sxs-lookup"><span data-stu-id="d7878-107">The following example fills a line, an ellipse, and a rectangle with a horizontal linear gradient brush.</span></span>  
  
<span data-ttu-id="d7878-108">Der <xref:System.Drawing.Drawing2D.LinearGradientBrush.%23ctor%2A> Konstruktor empfängt vier Argumente: zwei Punkte und zwei Farben.</span><span class="sxs-lookup"><span data-stu-id="d7878-108">The <xref:System.Drawing.Drawing2D.LinearGradientBrush.%23ctor%2A> constructor receives four arguments: two points and two colors.</span></span> <span data-ttu-id="d7878-109">Der erste Punkt (0, 10) ist mit der ersten Farbe (rot) verknüpft, und der zweite Punkt (200, 10) wird der zweiten Farbe (blau) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d7878-109">The first point (0, 10) is associated with the first color (red), and the second point (200, 10) is associated with the second color (blue).</span></span> <span data-ttu-id="d7878-110">Erwartungsgemäß wird die von (0, 10) zu (200, 10) gezogene Linie allmählich von rot in blau geändert.</span><span class="sxs-lookup"><span data-stu-id="d7878-110">As you would expect, the line drawn from (0, 10) to (200, 10) changes gradually from red to blue.</span></span>  
  
 <span data-ttu-id="d7878-111">Die 10S in den Punkten (0,0) und (200, 10) sind nicht wichtig.</span><span class="sxs-lookup"><span data-stu-id="d7878-111">The 10s in the points (0, 10) and (200, 10) are not important.</span></span> <span data-ttu-id="d7878-112">Wichtig ist, dass die beiden Punkte dieselbe zweite Koordinate aufweisen – die Linie, die Sie verbindet, ist horizontal.</span><span class="sxs-lookup"><span data-stu-id="d7878-112">What is important is that the two points have the same second coordinate — the line connecting them is horizontal.</span></span> <span data-ttu-id="d7878-113">Die Ellipse und das Rechteck ändern sich auch allmählich von rot in blau, wenn die horizontale Koordinate von 0 bis 200 wechselt.</span><span class="sxs-lookup"><span data-stu-id="d7878-113">The ellipse and the rectangle also change gradually from red to blue as the horizontal coordinate goes from 0 to 200.</span></span>  
  
 <span data-ttu-id="d7878-114">Die folgende Abbildung zeigt die Zeile, die Ellipse und das Rechteck.</span><span class="sxs-lookup"><span data-stu-id="d7878-114">The following illustration shows the line, the ellipse, and the rectangle.</span></span> <span data-ttu-id="d7878-115">Beachten Sie, dass der Farbverlauf selbst wiederholt wird, wenn sich die horizontale Koordinate über 200 erhöht.</span><span class="sxs-lookup"><span data-stu-id="d7878-115">Note that the color gradient repeats itself as the horizontal coordinate increases beyond 200.</span></span>  
  
 ![Eine Linie, eine Ellipse und ein Rechteck, das mit einem Farbverlauf gefüllt ist.](./media/how-to-create-a-linear-gradient/gradient-line-ellipse-rectangle.png)  
  
## <a name="to-use-horizontal-linear-gradients"></a><span data-ttu-id="d7878-117">So verwenden Sie horizontale lineare Farbverläufe</span><span class="sxs-lookup"><span data-stu-id="d7878-117">To use horizontal linear gradients</span></span>  
  
- <span data-ttu-id="d7878-118">Übergeben Sie als drittes und viertes Argument das nicht transparente rote und undurchsichtiges blau.</span><span class="sxs-lookup"><span data-stu-id="d7878-118">Pass in the opaque red and opaque blue as the third and fourth argument, respectively.</span></span>  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#21)]
     [!code-vb[System.Drawing.UsingaGradientBrush#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#21)]  
  
 <span data-ttu-id="d7878-119">Im vorherigen Beispiel ändern sich die Farbkomponenten linear, wenn Sie von einer horizontalen Koordinate von 0 zu einer horizontalen Koordinate von 200 wechseln.</span><span class="sxs-lookup"><span data-stu-id="d7878-119">In the preceding example, the color components change linearly as you move from a horizontal coordinate of 0 to a horizontal coordinate of 200.</span></span> <span data-ttu-id="d7878-120">Beispielsweise weist ein Punkt, dessen erste Koordinate die Hälfte zwischen 0 und 200 ist, eine blaue Komponente auf, die sich in der Mitte zwischen 0 und 255 befindet.</span><span class="sxs-lookup"><span data-stu-id="d7878-120">For example, a point whose first coordinate is halfway between 0 and 200 will have a blue component that is halfway between 0 and 255.</span></span>  
  
 <span data-ttu-id="d7878-121">Mit GDI+ können Sie die Art und Weise anpassen, in der eine Farbe von einem Rand eines Farbverlaufs zum anderen abweicht.</span><span class="sxs-lookup"><span data-stu-id="d7878-121">GDI+ allows you to adjust the way a color varies from one edge of a gradient to the other.</span></span> <span data-ttu-id="d7878-122">Angenommen, Sie möchten einen Farbverlaufs Pinsel erstellen, der gemäß der folgenden Tabelle von schwarz in rot geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d7878-122">Suppose you want to create a gradient brush that changes from black to red according to the following table.</span></span>  
  
|<span data-ttu-id="d7878-123">Horizontale Koordinate</span><span class="sxs-lookup"><span data-stu-id="d7878-123">Horizontal coordinate</span></span>|<span data-ttu-id="d7878-124">RGB-Komponenten</span><span class="sxs-lookup"><span data-stu-id="d7878-124">RGB components</span></span>|  
|---------------------------|--------------------|  
|<span data-ttu-id="d7878-125">0</span><span class="sxs-lookup"><span data-stu-id="d7878-125">0</span></span>|<span data-ttu-id="d7878-126">(0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="d7878-126">(0, 0, 0)</span></span>|  
|<span data-ttu-id="d7878-127">40</span><span class="sxs-lookup"><span data-stu-id="d7878-127">40</span></span>|<span data-ttu-id="d7878-128">(128, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="d7878-128">(128, 0, 0)</span></span>|  
|<span data-ttu-id="d7878-129">200</span><span class="sxs-lookup"><span data-stu-id="d7878-129">200</span></span>|<span data-ttu-id="d7878-130">(255, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="d7878-130">(255, 0, 0)</span></span>|  
  
 <span data-ttu-id="d7878-131">Beachten Sie, dass die rote Komponente die halbe Intensität hat, wenn die horizontale Koordinate nur 20 Prozent der Art von 0 bis 200 ist.</span><span class="sxs-lookup"><span data-stu-id="d7878-131">Note that the red component is at half intensity when the horizontal coordinate is only 20 percent of the way from 0 to 200.</span></span>  
  
 <span data-ttu-id="d7878-132">Im folgenden Beispiel wird die-Eigenschaft so festgelegt <xref:System.Drawing.Drawing2D.LinearGradientBrush.Blend%2A?displayProperty=nameWithType> , dass drei relative Intensitäten mit drei relativen Positionen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="d7878-132">The following example sets the <xref:System.Drawing.Drawing2D.LinearGradientBrush.Blend%2A?displayProperty=nameWithType> property to associate three relative intensities with three relative positions.</span></span> <span data-ttu-id="d7878-133">Wie in der obigen Tabelle ist eine relative Intensität von 0,5 mit einer relativen Position von 0,2 verknüpft.</span><span class="sxs-lookup"><span data-stu-id="d7878-133">As in the preceding table, a relative intensity of 0.5 is associated with a relative position of 0.2.</span></span> <span data-ttu-id="d7878-134">Der Code füllt eine Ellipse und ein Rechteck mit dem Farbverlaufs Pinsel.</span><span class="sxs-lookup"><span data-stu-id="d7878-134">The code fills an ellipse and a rectangle with the gradient brush.</span></span>  
  
 <span data-ttu-id="d7878-135">In der folgenden Abbildung werden die resultierende Ellipse und das Rechteck gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d7878-135">The following illustration shows the resulting ellipse and rectangle.</span></span>  
  
 ![Eine Ellipse und ein Rechteck, das mit einem horizontalen Farbverlauf gefüllt ist.](./media/how-to-create-a-linear-gradient/gradient-ellipse-rectangle.png)  

## <a name="to-customize-linear-gradients"></a><span data-ttu-id="d7878-137">So passen Sie lineare Farbverläufe an</span><span class="sxs-lookup"><span data-stu-id="d7878-137">To customize linear gradients</span></span>  
  
- <span data-ttu-id="d7878-138">Übergeben Sie als drittes und viertes Argument das nicht transparente schwarze und undurchsichtiges rot.</span><span class="sxs-lookup"><span data-stu-id="d7878-138">Pass in the opaque black and opaque red as the third and fourth argument, respectively.</span></span>  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#22)]
     [!code-vb[System.Drawing.UsingaGradientBrush#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#22)]  
  
 <span data-ttu-id="d7878-139">Die Farbverläufe in den vorangehenden Beispielen waren horizontal. Das heißt, die Farbe ändert sich allmählich, wenn Sie sich entlang einer horizontalen Linie bewegen.</span><span class="sxs-lookup"><span data-stu-id="d7878-139">The gradients in the preceding examples have been horizontal; that is, the color changes gradually as you move along any horizontal line.</span></span> <span data-ttu-id="d7878-140">Sie können auch vertikale Farbverläufe und diagonale Farbverläufe definieren.</span><span class="sxs-lookup"><span data-stu-id="d7878-140">You can also define vertical gradients and diagonal gradients.</span></span>  
  
 <span data-ttu-id="d7878-141">Im folgenden Beispiel werden die Punkte (0,0) und (200, 100) an einen- <xref:System.Drawing.Drawing2D.LinearGradientBrush.%23ctor%2A> Konstruktor übergeben.</span><span class="sxs-lookup"><span data-stu-id="d7878-141">The following example passes the points (0, 0) and (200, 100) to a <xref:System.Drawing.Drawing2D.LinearGradientBrush.%23ctor%2A> constructor.</span></span> <span data-ttu-id="d7878-142">Die Farbe blau ist (0,0) zugeordnet, und die Farbe grün ist zugeordnet (200, 100).</span><span class="sxs-lookup"><span data-stu-id="d7878-142">The color blue is associated with (0, 0), and the color green is associated with (200, 100).</span></span> <span data-ttu-id="d7878-143">Eine Linie (mit der Stift Breite 10) und eine Ellipse werden mit dem linearen Farbverlaufs Pinsel gefüllt.</span><span class="sxs-lookup"><span data-stu-id="d7878-143">A line (with pen width 10) and an ellipse are filled with the linear gradient brush.</span></span>  
  
 <span data-ttu-id="d7878-144">Die folgende Abbildung zeigt die Zeile und die Ellipse.</span><span class="sxs-lookup"><span data-stu-id="d7878-144">The following illustration shows the line and the ellipse.</span></span> <span data-ttu-id="d7878-145">Beachten Sie, dass sich die Farbe in der Ellipse allmählich ändert, wenn Sie eine beliebige Zeile bewegen, die parallel zur Zeile, die durchläuft (0,0) und (200, 100).</span><span class="sxs-lookup"><span data-stu-id="d7878-145">Note that the color in the ellipse changes gradually as you move along any line that is parallel to the line passing through (0, 0) and (200, 100).</span></span>  
  
 ![Eine Linie und eine Ellipse, die mit einem diagonalen Farbverlauf gefüllt sind.](./media/how-to-create-a-linear-gradient/gradient-line-ellipse.png)  
  
## <a name="to-create-diagonal-linear-gradients"></a><span data-ttu-id="d7878-147">So erstellen Sie diagonal lineare Farbverläufe</span><span class="sxs-lookup"><span data-stu-id="d7878-147">To create diagonal linear gradients</span></span>  
  
- <span data-ttu-id="d7878-148">Übergeben Sie als drittes und viertes Argument das nicht transparente blaue und undurchsichtiges grün.</span><span class="sxs-lookup"><span data-stu-id="d7878-148">Pass in the opaque blue and opaque green as the third and fourth argument, respectively.</span></span>  
  
     [!code-csharp[System.Drawing.UsingaGradientBrush#23](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/CS/Class1.cs#23)]
     [!code-vb[System.Drawing.UsingaGradientBrush#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingaGradientBrush/VB/Class1.vb#23)]  
  
## <a name="see-also"></a><span data-ttu-id="d7878-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7878-149">See also</span></span>

- [<span data-ttu-id="d7878-150">Verwenden eines Pinsels für Farbverläufe zum Ausfüllen von Formen</span><span class="sxs-lookup"><span data-stu-id="d7878-150">Using a Gradient Brush to Fill Shapes</span></span>](using-a-gradient-brush-to-fill-shapes.md)
- [<span data-ttu-id="d7878-151">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d7878-151">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
