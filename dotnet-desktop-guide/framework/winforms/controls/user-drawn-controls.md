---
title: Benutzerdefinierte Steuerelemente
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], user-drawn
- OnPaint method [Windows Forms]
- user-drawn controls [Windows Forms]
ms.assetid: 034af4b5-457f-4160-a937-22891817faa8
ms.openlocfilehash: c68c8c88376cfe7295962264c466030115f2f3db
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977256"
---
# <a name="user-drawn-controls"></a>Benutzerdefinierte Steuerelemente
Der .NET Framework bietet Ihnen die Möglichkeit, ihre eigenen Steuerelemente auf einfache Weise zu entwickeln. Sie können ein Benutzer Steuerelement erstellen, bei dem es sich um einen Satz von Standard Steuerelementen handelt, die durch Code verbunden sind, oder Sie können ein eigenes Steuerelement von Grund auf entwerfen. Sie können sogar Vererbung verwenden, um ein Steuerelement zu erstellen, das von einem vorhandenen Steuerelement erbt und seine inhärente Funktionalität hinzufügt. Der .NET Framework stellt die Funktionalität bereit, um eine benutzerdefinierte grafische Oberfläche für jedes von Ihnen erstellte Steuerelement zu zeichnen.  
  
 Das Zeichnen eines Steuer Elements wird durch die Ausführung von Code in der-Methode des Steuer Elements erreicht <xref:System.Windows.Forms.Control.OnPaint%2A> . Das einzige Argument der- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode ist ein <xref:System.Windows.Forms.PaintEventArgs> -Objekt, das alle Informationen und Funktionen bereitstellt, die zum Rendering des Steuer Elements erforderlich sind. Die <xref:System.Windows.Forms.PaintEventArgs> stellt als Eigenschaften zwei Prinzipal Objekte zur Verfügung, die beim Rendering des Steuer Elements verwendet werden:  
  
- <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> Object: das Rechteck, das den Teil des-Steuer Elements darstellt, der gezeichnet wird. Dies kann das gesamte Steuerelement oder ein Teil des Steuer Elements sein, je nachdem, wie das Steuerelement gezeichnet wird.  
  
- <xref:System.Drawing.Graphics> Object: kapselt verschiedene Grafik orientierte Objekte und Methoden, die die Funktionalität bereitstellen, die zum Zeichnen des Steuer Elements erforderlich ist.  
  
 Weitere Informationen zum <xref:System.Drawing.Graphics> Objekt und seiner Verwendung finden Sie unter Gewusst [wie: Erstellen von Grafikobjekten zum Zeichnen](../advanced/how-to-create-graphics-objects-for-drawing.md).  
  
 Das <xref:System.Windows.Forms.Control.OnPaint%2A> -Ereignis wird ausgelöst, wenn das-Steuerelement auf dem Bildschirm gezeichnet oder aktualisiert wird, und das- <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> Objekt stellt das Rechteck dar, in dem das Zeichnen stattfinden soll. Wenn das gesamte Steuerelement aktualisiert werden muss, stellt die <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> Größe des gesamten Steuer Elements dar. Wenn nur ein Teil des Steuer Elements aktualisiert werden muss, stellt das <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> Objekt jedoch nur den Bereich dar, der neu gezeichnet werden muss. Ein Beispiel für einen solchen Fall wäre, wenn ein Steuerelement teilweise von einem anderen Steuerelement oder Formular in der Benutzeroberfläche verdeckt wurde.  
  
 Wenn Sie von der- <xref:System.Windows.Forms.Control> Klasse erben, müssen Sie die <xref:System.Windows.Forms.Control.OnPaint%2A> -Methode überschreiben und Grafik Rendering-Code in bereitstellen. Wenn Sie eine benutzerdefinierte grafische Oberfläche für ein Benutzer Steuerelement oder ein geerbtes Steuerelement bereitstellen möchten, können Sie auch die-Methode überschreiben <xref:System.Windows.Forms.Control.OnPaint%2A> . Unten ist ein Beispiel angegeben:  
  
```vb  
Protected Overrides Sub OnPaint(ByVal e As PaintEventArgs)  
   ' Call the OnPaint method of the base class.  
   MyBase.OnPaint(e)  
  
   ' Declare and instantiate a drawing pen.  
   Using myPen As System.Drawing.Pen = New System.Drawing.Pen(Color.Aqua)  
      ' Draw an aqua rectangle in the rectangle represented by the control.  
      e.Graphics.DrawRectangle(myPen, New Rectangle(Me.Location, Me.Size))  
   End Using
End Sub  
```  
  
```csharp  
protected override void OnPaint(PaintEventArgs e)  
{  
   // Call the OnPaint method of the base class.  
   base.OnPaint(e);  
  
   // Declare and instantiate a new pen.  
   using (System.Drawing.Pen myPen = new System.Drawing.Pen(Color.Aqua))  
   {
      // Draw an aqua rectangle in the rectangle represented by the control.  
      e.Graphics.DrawRectangle(myPen, new Rectangle(this.Location,
         this.Size));  
   }
}  
```  
  
 Im vorangehenden Beispiel wird veranschaulicht, wie ein-Steuerelement mit einer sehr einfachen grafischen Darstellung dargestellt wird. Sie ruft die <xref:System.Windows.Forms.Control.OnPaint%2A> -Methode der Basisklasse auf, erstellt ein <xref:System.Drawing.Pen> -Objekt, mit dem gezeichnet werden soll, und zeichnet schließlich eine Ellipse in dem Rechteck, das von der <xref:System.Windows.Forms.Control.Location%2A> und des-Steuer Elements bestimmt wird <xref:System.Windows.Forms.Control.Size%2A> . Obwohl der größte Renderingcode deutlich komplizierter ist als dieser, wird in diesem Beispiel die Verwendung des-Objekts veranschaulicht, das <xref:System.Drawing.Graphics> im-Objekt enthalten ist <xref:System.Windows.Forms.PaintEventArgs> . Beachten Sie Folgendes: Wenn Sie von einer Klasse erben, die bereits über eine grafische Darstellung verfügt, z. b. <xref:System.Windows.Forms.UserControl> oder <xref:System.Windows.Forms.Button> , und Sie diese Darstellung nicht in das Rendering einbinden möchten, sollten Sie die-Methode der Basisklasse nicht aufzurufen <xref:System.Windows.Forms.Control.OnPaint%2A> .  
  
 Der Code in der <xref:System.Windows.Forms.Control.OnPaint%2A> -Methode des-Steuer Elements wird ausgeführt, wenn das Steuerelement zum ersten Mal gezeichnet wird, und wenn es aktualisiert wird. Fügen Sie dem Konstruktor des Steuer Elements die folgende Zeile hinzu, um sicherzustellen, dass das Steuerelement jedes Mal neu gezeichnet wird, wenn die Größe geändert wird:  
  
```vb  
SetStyle(ControlStyles.ResizeRedraw, True)  
```  
  
```csharp  
SetStyle(ControlStyles.ResizeRedraw, true);  
```  
  
> [!NOTE]
> Verwenden Sie die- <xref:System.Windows.Forms.Control.Region%2A?displayProperty=nameWithType> Eigenschaft zum Implementieren eines nicht rechteckigen Steuer Elements.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Control.Region%2A>
- <xref:System.Windows.Forms.ControlStyles>
- <xref:System.Drawing.Graphics>
- <xref:System.Windows.Forms.Control.OnPaint%2A>
- <xref:System.Windows.Forms.PaintEventArgs>
- [Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen](../advanced/how-to-create-graphics-objects-for-drawing.md)
- [Konstituierende Steuerelemente](constituent-controls.md)
- [Arten von benutzerdefinierten Steuerelementen](varieties-of-custom-controls.md)
