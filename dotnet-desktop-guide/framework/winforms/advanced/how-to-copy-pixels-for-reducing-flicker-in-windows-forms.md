---
title: 'Gewusst wie: Kopieren von Pixeln zum Reduzieren von Flimmern'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bitblt
- graphics [Windows Forms], copying
- flicker [Windows Forms], reducing in Windows Forms
- graphics [Windows Forms], reducing flicker
- pixels [Windows Forms], copying
- flicker
- bit-block transfer
ms.assetid: 33b76910-13a3-4521-be98-5c097341ae3b
ms.openlocfilehash: a25295532d7123d92bcacc6828d3e8cfcc839d6e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974999"
---
# <a name="how-to-copy-pixels-for-reducing-flicker-in-windows-forms"></a><span data-ttu-id="51760-102">Vorgehensweise: Kopieren von Pixeln zum Vermindern des Flackerns in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="51760-102">How to: Copy Pixels for Reducing Flicker in Windows Forms</span></span>
<span data-ttu-id="51760-103">Wenn Sie eine einfache Grafik animieren, können Benutzer mitunter Flimmern oder andere unerwünschte visuelle Effekte erkennen.</span><span class="sxs-lookup"><span data-stu-id="51760-103">When you animate a simple graphic, users can sometimes encounter flicker or other undesirable visual effects.</span></span> <span data-ttu-id="51760-104">Eine Möglichkeit, dieses Problem einzuschränken, besteht darin, einen "Bitblt"-Prozess in der Grafik zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="51760-104">One way to limit this problem is to use a "bitblt" process on the graphic.</span></span> <span data-ttu-id="51760-105">BitBLT ist die "Bitblock Übertragung" der Farbdaten von einem Ursprungs Rechteck von Pixeln bis hin zu einem Ziel Rechteck von Pixeln.</span><span class="sxs-lookup"><span data-stu-id="51760-105">Bitblt is the "bit-block transfer" of the color data from an origin rectangle of pixels to a destination rectangle of pixels.</span></span>  
  
 <span data-ttu-id="51760-106">Mit Windows Forms wird BitBLT mithilfe der- <xref:System.Drawing.Graphics.CopyFromScreen%2A> Methode der- <xref:System.Drawing.Graphics> Klasse erreicht.</span><span class="sxs-lookup"><span data-stu-id="51760-106">With Windows Forms, bitblt is accomplished using the <xref:System.Drawing.Graphics.CopyFromScreen%2A> method of the <xref:System.Drawing.Graphics> class.</span></span> <span data-ttu-id="51760-107">In den Parametern der-Methode geben Sie die Quelle und das Ziel (als Punkte), die Größe des zu kopierenden Bereichs und das Grafik Objekt an, das zum Zeichnen der neuen Form verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51760-107">In the parameters of the method, you specify the source and destination (as points), the size of the area to be copied, and the graphics object used to draw the new shape.</span></span>  
  
 <span data-ttu-id="51760-108">Im folgenden Beispiel wird eine Form im-Ereignishandler auf dem Formular gezeichnet <xref:System.Windows.Forms.Control.Paint> .</span><span class="sxs-lookup"><span data-stu-id="51760-108">In the example below, a shape is drawn on the form in its <xref:System.Windows.Forms.Control.Paint> event handler.</span></span> <span data-ttu-id="51760-109">Anschließend wird die- <xref:System.Drawing.Graphics.CopyFromScreen%2A> Methode verwendet, um die Form zu duplizieren.</span><span class="sxs-lookup"><span data-stu-id="51760-109">Then, the <xref:System.Drawing.Graphics.CopyFromScreen%2A> method is used to duplicate the shape.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="51760-110">Das Festlegen der- <xref:System.Windows.Forms.Control.DoubleBuffered%2A> Eigenschaft des Formulars auf führt dazu, `true` dass Grafik basierter Code im- <xref:System.Windows.Forms.Control.Paint> Ereignis doppelt gepuffert wird.</span><span class="sxs-lookup"><span data-stu-id="51760-110">Setting the form's <xref:System.Windows.Forms.Control.DoubleBuffered%2A> property to `true` will make graphics-based code in the <xref:System.Windows.Forms.Control.Paint> event be double-buffered.</span></span> <span data-ttu-id="51760-111">Obwohl dies bei der Verwendung des folgenden Codes keine erkennbaren Leistungssteigerungen hat, ist es bei der Arbeit mit komplexeren Grafik Bearbeitungs Codes zu beachten.</span><span class="sxs-lookup"><span data-stu-id="51760-111">While this will not have any discernible performance gains when using the code below, it is something to keep in mind when working with more complex graphics-manipulation code.</span></span>  
  
## <a name="example"></a><span data-ttu-id="51760-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="51760-112">Example</span></span>  
  
```vb  
Private Sub Form1_Paint(ByVal sender As Object, ByVal e As _  
    System.Windows.Forms.PaintEventArgs) Handles MyBase.Paint  
    ' Draw a circle with a bar on top.  
        e.Graphics.FillEllipse(Brushes.DarkBlue, New Rectangle _  
             (10, 10, 60, 60))  
        e.Graphics.FillRectangle(Brushes.Khaki, New Rectangle _  
             (20, 30, 60, 10))  
    ' Copy the graphic to a new location.  
        e.Graphics.CopyFromScreen(New Point(10, 10), New Point _  
             (100, 100), New Size(70, 70))  
End Sub  
```  
  
```csharp  
private void Form1_Paint(System.Object sender,  
    System.Windows.Forms.PaintEventArgs e)  
        {  
        e.Graphics.FillEllipse(Brushes.DarkBlue, new  
            Rectangle(10,10,60,60));  
        e.Graphics.FillRectangle(Brushes.Khaki, new  
            Rectangle(20,30,60,10));  
        e.Graphics.CopyFromScreen(new Point(10, 10), new Point(100, 100),
            new Size(70, 70));  
}  
```  
  
## <a name="compiling-the-code"></a><span data-ttu-id="51760-113">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="51760-113">Compiling the Code</span></span>  
 <span data-ttu-id="51760-114">Der obige Code wird im-Ereignishandler des Formulars ausgeführt <xref:System.Windows.Forms.Control.Paint> , sodass die Grafiken persistent bleiben, wenn das Formular neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="51760-114">The code above is run in the form's <xref:System.Windows.Forms.Control.Paint> event handler so that the graphics persist when the form is redrawn.</span></span> <span data-ttu-id="51760-115">Daher sollten Sie keine Grafik bezogenen Methoden im- <xref:System.Windows.Forms.Form.Load> Ereignishandler aufzurufen, da der gezeichnete Inhalt nicht neu gezeichnet wird, wenn die Größe des Formulars geändert oder von einem anderen Formular verdeckt wird.</span><span class="sxs-lookup"><span data-stu-id="51760-115">As such, do not call graphics-related methods in the <xref:System.Windows.Forms.Form.Load> event handler, because the drawn content will not be redrawn if the form is resized or obscured by another form.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="51760-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51760-116">See also</span></span>

- <xref:System.Drawing.CopyPixelOperation>
- <xref:System.Drawing.Graphics.FillRectangle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.OnPaint%2A?displayProperty=nameWithType>
- [<span data-ttu-id="51760-117">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="51760-117">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
- [<span data-ttu-id="51760-118">Verwenden eines Stifts zum Zeichnen von Linien und Formen</span><span class="sxs-lookup"><span data-stu-id="51760-118">Using a Pen to Draw Lines and Shapes</span></span>](using-a-pen-to-draw-lines-and-shapes.md)
