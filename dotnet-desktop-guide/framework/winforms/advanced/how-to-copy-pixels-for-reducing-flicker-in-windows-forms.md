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
# <a name="how-to-copy-pixels-for-reducing-flicker-in-windows-forms"></a>Vorgehensweise: Kopieren von Pixeln zum Vermindern des Flackerns in Windows Forms
Wenn Sie eine einfache Grafik animieren, können Benutzer mitunter Flimmern oder andere unerwünschte visuelle Effekte erkennen. Eine Möglichkeit, dieses Problem einzuschränken, besteht darin, einen "Bitblt"-Prozess in der Grafik zu verwenden. BitBLT ist die "Bitblock Übertragung" der Farbdaten von einem Ursprungs Rechteck von Pixeln bis hin zu einem Ziel Rechteck von Pixeln.  
  
 Mit Windows Forms wird BitBLT mithilfe der- <xref:System.Drawing.Graphics.CopyFromScreen%2A> Methode der- <xref:System.Drawing.Graphics> Klasse erreicht. In den Parametern der-Methode geben Sie die Quelle und das Ziel (als Punkte), die Größe des zu kopierenden Bereichs und das Grafik Objekt an, das zum Zeichnen der neuen Form verwendet wird.  
  
 Im folgenden Beispiel wird eine Form im-Ereignishandler auf dem Formular gezeichnet <xref:System.Windows.Forms.Control.Paint> . Anschließend wird die- <xref:System.Drawing.Graphics.CopyFromScreen%2A> Methode verwendet, um die Form zu duplizieren.  
  
> [!NOTE]
> Das Festlegen der- <xref:System.Windows.Forms.Control.DoubleBuffered%2A> Eigenschaft des Formulars auf führt dazu, `true` dass Grafik basierter Code im- <xref:System.Windows.Forms.Control.Paint> Ereignis doppelt gepuffert wird. Obwohl dies bei der Verwendung des folgenden Codes keine erkennbaren Leistungssteigerungen hat, ist es bei der Arbeit mit komplexeren Grafik Bearbeitungs Codes zu beachten.  
  
## <a name="example"></a>Beispiel  
  
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
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Der obige Code wird im-Ereignishandler des Formulars ausgeführt <xref:System.Windows.Forms.Control.Paint> , sodass die Grafiken persistent bleiben, wenn das Formular neu gezeichnet wird. Daher sollten Sie keine Grafik bezogenen Methoden im- <xref:System.Windows.Forms.Form.Load> Ereignishandler aufzurufen, da der gezeichnete Inhalt nicht neu gezeichnet wird, wenn die Größe des Formulars geändert oder von einem anderen Formular verdeckt wird.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.CopyPixelOperation>
- <xref:System.Drawing.Graphics.FillRectangle%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.OnPaint%2A?displayProperty=nameWithType>
- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Verwenden eines Stifts zum Zeichnen von Linien und Formen](using-a-pen-to-draw-lines-and-shapes.md)
