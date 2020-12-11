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
# <a name="overriding-the-onpaint-method"></a><span data-ttu-id="c0c87-102">Überschreiben der OnPaint-Methode</span><span class="sxs-lookup"><span data-stu-id="c0c87-102">Overriding the OnPaint Method</span></span>

<span data-ttu-id="c0c87-103">Die grundlegenden Schritte zum Überschreiben der in der .NET Framework definierten Ereignisse sind identisch und werden in der folgenden Liste zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="c0c87-103">The basic steps for overriding any event defined in the .NET Framework are identical and are summarized in the following list.</span></span>  
  
#### <a name="to-override-an-inherited-event"></a><span data-ttu-id="c0c87-104">Überschreiben eines geerbten Ereignisses</span><span class="sxs-lookup"><span data-stu-id="c0c87-104">To override an inherited event</span></span>  
  
1. <span data-ttu-id="c0c87-105">Überschreiben Sie die geschützte `On` *EventName* -Methode.</span><span class="sxs-lookup"><span data-stu-id="c0c87-105">Override the protected `On`*EventName* method.</span></span>  
  
2. <span data-ttu-id="c0c87-106">Die `On` *EventName* -Methode der Basisklasse wird von der überschriebenen `On` *EventName* -Methode aufgerufen, sodass registrierte Delegaten das Ereignis empfangen.</span><span class="sxs-lookup"><span data-stu-id="c0c87-106">Call the `On`*EventName* method of the base class from the overridden `On`*EventName* method, so that registered delegates receive the event.</span></span>  
  
 <span data-ttu-id="c0c87-107">Das <xref:System.Windows.Forms.Control.Paint> Ereignis wird hier ausführlich erläutert, da jedes Windows Forms Steuerelement das Ereignis überschreiben muss <xref:System.Windows.Forms.Control.Paint> , von dem es erbt <xref:System.Windows.Forms.Control> .</span><span class="sxs-lookup"><span data-stu-id="c0c87-107">The <xref:System.Windows.Forms.Control.Paint> event is discussed in detail here because every Windows Forms control must override the <xref:System.Windows.Forms.Control.Paint> event that it inherits from <xref:System.Windows.Forms.Control>.</span></span> <span data-ttu-id="c0c87-108">Die Basis <xref:System.Windows.Forms.Control> Klasse weiß nicht, wie ein abgeleitetes Steuerelement gezeichnet werden muss, und stellt keine Zeichnungs Logik in der- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode bereit.</span><span class="sxs-lookup"><span data-stu-id="c0c87-108">The base <xref:System.Windows.Forms.Control> class does not know how a derived control needs to be drawn and does not provide any painting logic in the <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span> <span data-ttu-id="c0c87-109">Die- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode von <xref:System.Windows.Forms.Control> sendet das <xref:System.Windows.Forms.Control.Paint> Ereignis einfach an registrierte Ereignis Empfänger.</span><span class="sxs-lookup"><span data-stu-id="c0c87-109">The <xref:System.Windows.Forms.Control.OnPaint%2A> method of <xref:System.Windows.Forms.Control> simply dispatches the <xref:System.Windows.Forms.Control.Paint> event to registered event receivers.</span></span>  
  
 <span data-ttu-id="c0c87-110">Wenn Sie das Beispiel unter Gewusst [wie: Entwickeln eines einfachen Windows Forms Steuer](how-to-develop-a-simple-windows-forms-control.md)Elements gearbeitet haben, haben Sie ein Beispiel für das Überschreiben der- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode gesehen.</span><span class="sxs-lookup"><span data-stu-id="c0c87-110">If you worked through the sample in [How to: Develop a Simple Windows Forms Control](how-to-develop-a-simple-windows-forms-control.md), you have seen an example of overriding the <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span> <span data-ttu-id="c0c87-111">Das folgende Code Fragment wird aus diesem Beispiel entnommen.</span><span class="sxs-lookup"><span data-stu-id="c0c87-111">The following code fragment is taken from that sample.</span></span>  
  
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
  
 <span data-ttu-id="c0c87-112">Die- <xref:System.Windows.Forms.PaintEventArgs> Klasse enthält Daten für das- <xref:System.Windows.Forms.Control.Paint> Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c0c87-112">The <xref:System.Windows.Forms.PaintEventArgs> class contains data for the <xref:System.Windows.Forms.Control.Paint> event.</span></span> <span data-ttu-id="c0c87-113">Sie verfügt über zwei Eigenschaften, wie im folgenden Code dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c0c87-113">It has two properties, as shown in the following code.</span></span>  
  
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
  
 <span data-ttu-id="c0c87-114"><xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> das zu zeichnende Rechteck, und die- <xref:System.Windows.Forms.PaintEventArgs.Graphics%2A> Eigenschaft verweist auf ein- <xref:System.Drawing.Graphics> Objekt.</span><span class="sxs-lookup"><span data-stu-id="c0c87-114"><xref:System.Windows.Forms.PaintEventArgs.ClipRectangle%2A> is the rectangle to be painted, and the <xref:System.Windows.Forms.PaintEventArgs.Graphics%2A> property refers to a <xref:System.Drawing.Graphics> object.</span></span> <span data-ttu-id="c0c87-115">Die Klassen im- <xref:System.Drawing?displayProperty=nameWithType> Namespace sind verwaltete Klassen, die den Zugriff auf die Funktionalität von GDI+, der neuen Windows-Grafikbibliothek, ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c0c87-115">The classes in the <xref:System.Drawing?displayProperty=nameWithType> namespace are managed classes that provide access to the functionality of GDI+, the new Windows graphics library.</span></span> <span data-ttu-id="c0c87-116">Das <xref:System.Drawing.Graphics> -Objekt verfügt über Methoden zum Zeichnen von Punkten, Zeichen folgen, Zeilen, Bögen, Ellipsen und vielen anderen Formen.</span><span class="sxs-lookup"><span data-stu-id="c0c87-116">The <xref:System.Drawing.Graphics> object has methods to draw points, strings, lines, arcs, ellipses, and many other shapes.</span></span>  
  
 <span data-ttu-id="c0c87-117">Ein-Steuerelement ruft seine- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode auf, wenn es seine visuelle Darstellung ändern muss.</span><span class="sxs-lookup"><span data-stu-id="c0c87-117">A control invokes its <xref:System.Windows.Forms.Control.OnPaint%2A> method whenever it needs to change its visual display.</span></span> <span data-ttu-id="c0c87-118">Diese Methode löst wiederum das- <xref:System.Windows.Forms.Control.Paint> Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="c0c87-118">This method in turn raises the <xref:System.Windows.Forms.Control.Paint> event.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c0c87-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0c87-119">See also</span></span>

- [<span data-ttu-id="c0c87-120">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="c0c87-120">Events</span></span>](/dotnet/standard/events/index)
- [<span data-ttu-id="c0c87-121">Wiedergeben eines Windows Forms-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="c0c87-121">Rendering a Windows Forms Control</span></span>](rendering-a-windows-forms-control.md)
- [<span data-ttu-id="c0c87-122">Definieren eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="c0c87-122">Defining an Event</span></span>](defining-an-event-in-windows-forms-controls.md)
