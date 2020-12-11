---
title: Behandeln von Benutzereingaben
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], user input using code
- custom controls [Windows Forms], keyboard events using code
- custom controls [Windows Forms], mouse events using code
ms.assetid: d9b12787-86f6-4022-8e0f-e12d312c4af2
ms.openlocfilehash: a977061ab64dbecd5782645aa6929a77803b18c9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975762"
---
# <a name="handling-user-input"></a>Behandeln von Benutzereingaben

Dieses Thema beschreibt die Haupt Tastatur-und Mausereignisse, die von bereitgestellt werden <xref:System.Windows.Forms.Control?displayProperty=nameWithType> . Beim Bearbeiten eines Ereignisses sollten Autoren von Steuerelementen die geschützte Methode `On`*EventName* überschreiben, statt einen Delegaten an das Ereignis anzuhängen. Zum Überprüfen der Ereignisse siehe [Auslösen von Ereignissen aus einer Komponente](/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120)).  
  
> [!NOTE]
> Wenn einem Ereignis keine Daten zugeordnet sind, wird eine Instanz der Basisklasse <xref:System.EventArgs> als Argument an die `On` *EventName* -Methode übermittelt.  
  
## <a name="keyboard-events"></a>Tastaturereignisse  

 Die gängigen Tastatur Ereignisse, die von Ihrem Steuerelement behandelt werden können <xref:System.Windows.Forms.Control.KeyDown> , sind, <xref:System.Windows.Forms.Control.KeyPress> und <xref:System.Windows.Forms.Control.KeyUp> .  
  
|Veranstaltungsname|Zu überschreibende Methode|Beschreibung des Ereignisses|  
|----------------|------------------------|--------------------------|  
|`KeyDown`|`void OnKeyDown(KeyEventArgs)`|Wird nur ausgelöst, wenn anfangs eine Taste gedrückt wird.|  
|`KeyPress`|`void OnKeyPress`<br /><br /> `(KeyPressEventArgs)`|Wird jedes Mal ausgelöst, wenn eine Taste gedrückt wird. Wenn eine Taste angehalten wird, wird ein- <xref:System.Windows.Forms.Control.KeyPress> Ereignis mit der Wiederholungsrate ausgelöst, die vom Betriebssystem festgelegt wird.|  
|`KeyUp`|`void OnKeyUp(KeyEventArgs)`|Wird ausgelöst, wenn eine Taste losgelassen wird.|  
  
> [!NOTE]
> Das Bearbeiten von Tastatureingaben ist wesentlich komplexer als das Überschreiben der Ereignisse in der obigen Tabelle und würde Rahmen dieses Themas sprengen. Weitere Informationen finden Sie unter [Benutzereingaben in Windows Forms](../user-input-in-windows-forms.md).  
  
## <a name="mouse-events"></a>Mausereignisse  

 Die Mausereignisse, die von Ihrem Steuerelement behandelt werden können <xref:System.Windows.Forms.Control.MouseDown> , sind, <xref:System.Windows.Forms.Control.MouseEnter> , <xref:System.Windows.Forms.Control.MouseHover> , <xref:System.Windows.Forms.Control.MouseLeave> , <xref:System.Windows.Forms.Control.MouseMove> und <xref:System.Windows.Forms.Control.MouseUp> .  
  
|Veranstaltungsname|Zu überschreibende Methode|Beschreibung des Ereignisses|  
|----------------|------------------------|--------------------------|  
|`MouseDown`|`void OnMouseDown(MouseEventArgs)`|Wird ausgelöst, wenn sich der Mauszeiger über dem Steuerelement befindet und eine Maustaste gedrückt wird.|  
|`MouseEnter`|`void OnMouseEnter(EventArgs)`|Wird ausgelöst, wenn der Mauszeiger zunächst auf den Bereich des Steuerelements trifft.|  
|`MouseHover`|`void OnMouseHover(EventArgs)`|Wird ausgelöst, wenn der Mauszeiger über das Steuerelement bewegt wird.|  
|`MouseLeave`|`void OnMouseLeave(EventArgs)`|Wird ausgelöst, wenn der Mauszeiger den Bereich des Steuerelements verlässt.|  
|`MouseMove`|`void OnMouseMove(MouseEventArgs)`|Wird ausgelöst, wenn der Mauszeiger in den Bereich des Steuerelements wechselt.|  
|`MouseUp`|`void OnMouseUp(MouseEventArgs)`|Wird ausgelöst, wenn die Maustaste losgelassen wird, während sich der Mauszeiger über dem Steuerelement befindet oder den Bereich des Steuerelements verlässt.|  
  
 Das folgende Code Fragment zeigt ein Beispiel für das Überschreiben des <xref:System.Windows.Forms.Control.MouseDown> Ereignisses.  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#7](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#7)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#7](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#7)]  
  
 Das folgende Code Fragment zeigt ein Beispiel für das Überschreiben des <xref:System.Windows.Forms.Control.MouseMove> Ereignisses.  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#8](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#8)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#8](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#8)]  
  
 Das folgende Code Fragment zeigt ein Beispiel für das Überschreiben des <xref:System.Windows.Forms.Control.MouseUp> Ereignisses.  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#9](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#9)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#9](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#9)]  
  
 Für den vollständigen Quellencode für das `FlashTrackBar`-Beispiel siehe [Vorgehensweise: Erstellen eines Windows Forms-Steuerelement, das den Fortschritt anzeigt](how-to-create-a-windows-forms-control-that-shows-progress.md).  
  
## <a name="see-also"></a>Siehe auch

- [Ereignisse in Windows Forms-Steuerelementen](events-in-windows-forms-controls.md)
- [Definieren eines Ereignisses](defining-an-event-in-windows-forms-controls.md)
- [Ereignisse](/dotnet/standard/events/index)
- [Benutzereingabe in Windows Forms](../user-input-in-windows-forms.md)
