---
title: 'Vorgehensweise: Abrufen von Schriftarteigenschaften'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- fonts [Windows Forms], obtaining metrics
- font metrics [Windows Forms], obtaining
ms.assetid: ff7c0616-67f7-4fa2-84ee-b8d642f2b09b
ms.openlocfilehash: 7d7ad92199bb8a8f01290066f8ae023a14c2f9ce
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976144"
---
# <a name="how-to-obtain-font-metrics"></a><span data-ttu-id="3104e-102">Vorgehensweise: Abrufen von Schriftarteigenschaften</span><span class="sxs-lookup"><span data-stu-id="3104e-102">How to: Obtain Font Metrics</span></span>
<span data-ttu-id="3104e-103">Die- <xref:System.Drawing.FontFamily> Klasse stellt die folgenden Methoden bereit, die verschiedene Metriken für eine bestimmte Kombination aus Familie und Stil abrufen:</span><span class="sxs-lookup"><span data-stu-id="3104e-103">The <xref:System.Drawing.FontFamily> class provides the following methods that retrieve various metrics for a particular family/style combination:</span></span>  
  
- <span data-ttu-id="3104e-104"><xref:System.Drawing.FontFamily.GetEmHeight%2A>FontStyle</span><span class="sxs-lookup"><span data-stu-id="3104e-104"><xref:System.Drawing.FontFamily.GetEmHeight%2A>(FontStyle)</span></span>  
  
- <span data-ttu-id="3104e-105"><xref:System.Drawing.FontFamily.GetCellAscent%2A>FontStyle</span><span class="sxs-lookup"><span data-stu-id="3104e-105"><xref:System.Drawing.FontFamily.GetCellAscent%2A>(FontStyle)</span></span>  
  
- <span data-ttu-id="3104e-106"><xref:System.Drawing.FontFamily.GetCellDescent%2A>FontStyle</span><span class="sxs-lookup"><span data-stu-id="3104e-106"><xref:System.Drawing.FontFamily.GetCellDescent%2A>(FontStyle)</span></span>  
  
- <span data-ttu-id="3104e-107"><xref:System.Drawing.FontFamily.GetLineSpacing%2A>FontStyle</span><span class="sxs-lookup"><span data-stu-id="3104e-107"><xref:System.Drawing.FontFamily.GetLineSpacing%2A>(FontStyle)</span></span>  
  
 <span data-ttu-id="3104e-108">Die von diesen Methoden zurückgegebenen Werte sind in Schriftart Entwurfs Einheiten, sodass Sie unabhängig von der Größe und den Einheiten eines bestimmten <xref:System.Drawing.Font> Objekts sind.</span><span class="sxs-lookup"><span data-stu-id="3104e-108">The values returned by these methods are in font design units, so they are independent of the size and units of a particular <xref:System.Drawing.Font> object.</span></span>  
  
 <span data-ttu-id="3104e-109">Die folgende Abbildung zeigt die verschiedenen Metriken:</span><span class="sxs-lookup"><span data-stu-id="3104e-109">The following illustration shows the various metrics:</span></span>
  
 ![Abbildung der Schriftart Metriken: Aufstieg, Abstieg und Zeilenabstand.](./media/how-to-obtain-font-metrics/various-font-metrics.png)  
  
## <a name="example"></a><span data-ttu-id="3104e-111">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3104e-111">Example</span></span>  
 <span data-ttu-id="3104e-112">Im folgenden Beispiel werden die Metriken für den regulären Stil der Arial-Schriftfamilie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3104e-112">The following example displays the metrics for the regular style of the Arial font family.</span></span> <span data-ttu-id="3104e-113">Der Code erstellt auch ein <xref:System.Drawing.Font> -Objekt (basierend auf der Arial-Familie) mit einer Größe von 16 Pixel und zeigt die Metriken (in Pixel) für das jeweilige <xref:System.Drawing.Font> Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3104e-113">The code also creates a <xref:System.Drawing.Font> object (based on the Arial family) with size 16 pixels and displays the metrics (in pixels) for that particular <xref:System.Drawing.Font> object.</span></span>  
  
 <span data-ttu-id="3104e-114">Die folgende Abbildung zeigt die Ausgabe des Beispielcodes:</span><span class="sxs-lookup"><span data-stu-id="3104e-114">The following illustration shows the output of the example code:</span></span>
  
 ![Beispielcode Ausgabe von Arial Schriftart Metriken.](./media/how-to-obtain-font-metrics/example-output-code-arial-font.png)  
  
 <span data-ttu-id="3104e-116">Beachten Sie die ersten beiden Zeilen der Ausgabe in der obigen Abbildung.</span><span class="sxs-lookup"><span data-stu-id="3104e-116">Note the first two lines of output in the preceding illustration.</span></span> <span data-ttu-id="3104e-117">Das <xref:System.Drawing.Font> -Objekt gibt eine Größe von 16 zurück, und das- <xref:System.Drawing.FontFamily> Objekt gibt eine EM-Höhe von 2.048 zurück.</span><span class="sxs-lookup"><span data-stu-id="3104e-117">The <xref:System.Drawing.Font> object returns a size of 16, and the <xref:System.Drawing.FontFamily> object returns an em height of 2,048.</span></span> <span data-ttu-id="3104e-118">Diese beiden Zahlen (16 und 2.048) sind der Schlüssel für die Umstellung zwischen Schriftart Entwurfs Einheiten und den Einheiten (in diesem Fall Pixel) des- <xref:System.Drawing.Font> Objekts.</span><span class="sxs-lookup"><span data-stu-id="3104e-118">These two numbers (16 and 2,048) are the key to converting between font design units and the units (in this case pixels) of the <xref:System.Drawing.Font> object.</span></span>  
  
 <span data-ttu-id="3104e-119">Beispielsweise können Sie den Aufstieg wie folgt von Entwurfs Einheiten in Pixel konvertieren:</span><span class="sxs-lookup"><span data-stu-id="3104e-119">For example, you can convert the ascent from design units to pixels as follows:</span></span>  
  
 ![Formel, die die Konvertierung von Entwurfs Einheiten in Pixel anzeigt](./media/how-to-obtain-font-metrics/convert-font-units-example.png)  
  
 <span data-ttu-id="3104e-121">Der folgende Code positioniert Text vertikal, indem der <xref:System.Drawing.PointF.Y%2A> Datenmember eines-Objekts festgelegt wird <xref:System.Drawing.PointF> .</span><span class="sxs-lookup"><span data-stu-id="3104e-121">The following code positions text vertically by setting the <xref:System.Drawing.PointF.Y%2A> data member of a <xref:System.Drawing.PointF> object.</span></span> <span data-ttu-id="3104e-122">Die y-Koordinate wird von `font.Height` für jede neue Textzeile um erweitert.</span><span class="sxs-lookup"><span data-stu-id="3104e-122">The y-coordinate is increased by `font.Height` for each new line of text.</span></span> <span data-ttu-id="3104e-123">Die- <xref:System.Drawing.Font.Height%2A> Eigenschaft eines- <xref:System.Drawing.Font> Objekts gibt den Zeilenabstand (in Pixel) für dieses bestimmte <xref:System.Drawing.Font> Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="3104e-123">The <xref:System.Drawing.Font.Height%2A> property of a <xref:System.Drawing.Font> object returns the line spacing (in pixels) for that particular <xref:System.Drawing.Font> object.</span></span> <span data-ttu-id="3104e-124">In diesem Beispiel ist die von zurückgegebene Zahl <xref:System.Drawing.Font.Height%2A> 19.</span><span class="sxs-lookup"><span data-stu-id="3104e-124">In this example, the number returned by <xref:System.Drawing.Font.Height%2A> is 19.</span></span> <span data-ttu-id="3104e-125">Beachten Sie, dass dies mit der Zahl (aufgerundet auf eine ganze Zahl) identisch ist, die durch das umrechnen der Zeilen Abstands Metrik in Pixel erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="3104e-125">Note that this is the same as the number (rounded up to an integer) obtained by converting the line-spacing metric to pixels.</span></span>  
  
 <span data-ttu-id="3104e-126">Beachten Sie, dass die EM-Höhe (auch "size" oder "em size" genannt) nicht die Summe aus der Besteigung und der Abfahrt ist.</span><span class="sxs-lookup"><span data-stu-id="3104e-126">Note that the em height (also called size or em size) is not the sum of the ascent and the descent.</span></span> <span data-ttu-id="3104e-127">Die Summe des Aufstiegs und der Abstieg wird als Zellhöhe bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3104e-127">The sum of the ascent and the descent is called the cell height.</span></span> <span data-ttu-id="3104e-128">Die Zellen Höhe abzüglich der internen führenden ist gleich der EM-Höhe.</span><span class="sxs-lookup"><span data-stu-id="3104e-128">The cell height minus the internal leading is equal to the em height.</span></span> <span data-ttu-id="3104e-129">Die Zellen Höhe zuzüglich der externen führenden ist gleich dem Zeilenabstand.</span><span class="sxs-lookup"><span data-stu-id="3104e-129">The cell height plus the external leading is equal to the line spacing.</span></span>  
  
 [!code-csharp[System.Drawing.FontsAndText#71](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#71)]
 [!code-vb[System.Drawing.FontsAndText#71](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#71)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="3104e-130">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="3104e-130">Compiling the Code</span></span>  
 <span data-ttu-id="3104e-131">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .</span><span class="sxs-lookup"><span data-stu-id="3104e-131">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3104e-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3104e-132">See also</span></span>

- [<span data-ttu-id="3104e-133">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3104e-133">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="3104e-134">Verwenden von Schriftarten und Text</span><span class="sxs-lookup"><span data-stu-id="3104e-134">Using Fonts and Text</span></span>](using-fonts-and-text.md)
