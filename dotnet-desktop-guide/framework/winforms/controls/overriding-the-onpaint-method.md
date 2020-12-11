---
title: Überschreiben der OnPaint-Methode
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Paint event [Windows Forms], handling in Windows Forms custom control
- OnPaint method [Windows Forms], overriding in Windows Forms custom controls
ms.assetid: e9ca2723-0107-4540-bb21-4f5ffb4a9906
ms.openlocfilehash: 140c3e880300f8b1428dd23d946f25d095189fb3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976698"
---
# <a name="overriding-the-onpaint-method"></a>Überschreiben der OnPaint-Methode

Die grundlegenden Schritte zum Überschreiben der in der .NET Framework definierten Ereignisse sind identisch und werden in der folgenden Liste zusammengefasst.  
  
#### <a name="to-override-an-inherited-event"></a>Überschreiben eines geerbten Ereignisses  
  
1. Überschreiben Sie die geschützte `On` *EventName* -Methode.  
  
2. Die `On` *EventName* -Methode der Basisklasse wird von der überschriebenen `On` *EventName* -Methode aufgerufen, sodass registrierte Delegaten das Ereignis empfangen.  
  
 Das <xref:System.Windows.Forms.Control.Paint> Ereignis wird hier ausführlich erläutert, da jedes Windows Forms Steuerelement das Ereignis überschreiben muss <xref:System.Windows.Forms.Control.Paint> , von dem es erbt <xref:System.Windows.Forms.Control> . Die Basis <xref:System.Windows.Forms.Control> Klasse weiß nicht, wie ein abgeleitetes Steuerelement gezeichnet werden muss, und stellt keine Zeichnungs Logik in der- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode bereit. Die- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode von <xref:System.Windows.Forms.Control> sendet das <xref:System.Windows.Forms.Control.Paint> Ereignis einfach an registrierte Ereignis Empfänger.  
  
 Wenn Sie das Beispiel unter Gewusst [wie: Entwickeln eines einfachen Windows Forms Steuer](how-to-develop-a-simple-windows-forms-control.md)Elements gearbeitet haben, haben Sie ein Beispiel für das Überschreiben der- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode gesehen. Das folgende Code Fragment wird aus diesem Beispiel entnommen.  
  
```vb  
Public Class FirstControl  
   Inherits Control  
  
   Public Sub New()  
   End Sub  
  
   Protected Overrides Sub OnPaint(e As PaintEventArgs)  
      ' Call the OnPaint method of the base class.  
      MyBase.OnPaint(e)  
      ' Call methods of the System.Drawing.Graphics object.  
      e.Graphics.DrawString(Text, Font, New SolidBrush(ForeColor), RectangleF.op_Implicit(ClientRectangle))  
   End Sub  
End Class
```  
  
```csharp  
public class FirstControl : Control {  
   public FirstControl() {}  
   protected override void OnPaint(PaintEventArgs e) {  
      // Call the OnPaint method of the base class.  
      base.OnPaint(e);  
      // Call methods of the System.Drawing.Graphics object.  
      e.Graphics.DrawString(Text, Font, new SolidBrush(ForeColor), ClientRectangle);  
   }
}
```  
  
 Die- <xref:System.Windows.Forms.PaintEventArgs> Klasse enthält Daten für das- <xref:System.Windows.Forms.Control.Paint> Ereignis. Sie verfügt über zwei Eigenschaften, wie im folgenden Code dargestellt.  
  
```vb  
Public Class PaintEventArgs  
   Inherits EventArgs  
   ...  
   Public ReadOnly Property ClipRectangle() As System.Drawing.Rectangle  
      ...  
   End Property  
  
   Public ReadOnly Property Graphics() As System.Drawing.Graphics  
      ...  
   End Property
   ...  
End Class  
```  
  
```csharp  
public class PaintEventArgs : EventArgs {  
...  
    public System.Drawing.Rectangle ClipRectangle {}  
    public System.Drawing.Graphics Graphics {}  
...  
}  
```  
  
 <xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> das zu zeichnende Rechteck, und die- <xref:System.Windows.Forms.PaintEventArgs.Graphics%2A> Eigenschaft verweist auf ein- <xref:System.Drawing.Graphics> Objekt. Die Klassen im- <xref:System.Drawing?displayProperty=nameWithType> Namespace sind verwaltete Klassen, die den Zugriff auf die Funktionalität von GDI+, der neuen Windows-Grafikbibliothek, ermöglichen. Das <xref:System.Drawing.Graphics> -Objekt verfügt über Methoden zum Zeichnen von Punkten, Zeichen folgen, Zeilen, Bögen, Ellipsen und vielen anderen Formen.  
  
 Ein-Steuerelement ruft seine- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode auf, wenn es seine visuelle Darstellung ändern muss. Diese Methode löst wiederum das- <xref:System.Windows.Forms.Control.Paint> Ereignis aus.  
  
## <a name="see-also"></a>Siehe auch

- [Ereignisse](/dotnet/standard/events/index)
- [Wiedergeben eines Windows Forms-Steuerelements](rendering-a-windows-forms-control.md)
- [Definieren eines Ereignisses](defining-an-event-in-windows-forms-controls.md)
