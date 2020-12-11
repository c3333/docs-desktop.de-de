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
# <a name="handling-user-input"></a><span data-ttu-id="d4069-102">Behandeln von Benutzereingaben</span><span class="sxs-lookup"><span data-stu-id="d4069-102">Handling User Input</span></span>

<span data-ttu-id="d4069-103">Dieses Thema beschreibt die Haupt Tastatur-und Mausereignisse, die von bereitgestellt werden <xref:System.Windows.Forms.Control?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="d4069-103">This topic describes the main keyboard and mouse events provided by <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span> <span data-ttu-id="d4069-104">Beim Bearbeiten eines Ereignisses sollten Autoren von Steuerelementen die geschützte Methode `On`*EventName* überschreiben, statt einen Delegaten an das Ereignis anzuhängen.</span><span class="sxs-lookup"><span data-stu-id="d4069-104">When handling an event, control authors should override the protected `On`*EventName* method rather than attaching a delegate to the event.</span></span> <span data-ttu-id="d4069-105">Zum Überprüfen der Ereignisse siehe [Auslösen von Ereignissen aus einer Komponente](/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120)).</span><span class="sxs-lookup"><span data-stu-id="d4069-105">For a review of events, see [Raising Events from a Component](/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120)).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="d4069-106">Wenn einem Ereignis keine Daten zugeordnet sind, wird eine Instanz der Basisklasse <xref:System.EventArgs> als Argument an die `On` *EventName* -Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="d4069-106">If there is no data associated with an event, an instance of the base class <xref:System.EventArgs> is passed as an argument to the `On`*EventName* method.</span></span>  
  
## <a name="keyboard-events"></a><span data-ttu-id="d4069-107">Tastaturereignisse</span><span class="sxs-lookup"><span data-stu-id="d4069-107">Keyboard Events</span></span>  

 <span data-ttu-id="d4069-108">Die gängigen Tastatur Ereignisse, die von Ihrem Steuerelement behandelt werden können <xref:System.Windows.Forms.Control.KeyDown> , sind, <xref:System.Windows.Forms.Control.KeyPress> und <xref:System.Windows.Forms.Control.KeyUp> .</span><span class="sxs-lookup"><span data-stu-id="d4069-108">The common keyboard events that your control can handle are <xref:System.Windows.Forms.Control.KeyDown>, <xref:System.Windows.Forms.Control.KeyPress>, and <xref:System.Windows.Forms.Control.KeyUp>.</span></span>  
  
|<span data-ttu-id="d4069-109">Veranstaltungsname</span><span class="sxs-lookup"><span data-stu-id="d4069-109">Event Name</span></span>|<span data-ttu-id="d4069-110">Zu überschreibende Methode</span><span class="sxs-lookup"><span data-stu-id="d4069-110">Method to Override</span></span>|<span data-ttu-id="d4069-111">Beschreibung des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="d4069-111">Description of Event</span></span>|  
|----------------|------------------------|--------------------------|  
|`KeyDown`|`void OnKeyDown(KeyEventArgs)`|<span data-ttu-id="d4069-112">Wird nur ausgelöst, wenn anfangs eine Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="d4069-112">Raised only when a key is initially pressed.</span></span>|  
|`KeyPress`|`void OnKeyPress`<br /><br /> `(KeyPressEventArgs)`|<span data-ttu-id="d4069-113">Wird jedes Mal ausgelöst, wenn eine Taste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="d4069-113">Raised every time a key is pressed.</span></span> <span data-ttu-id="d4069-114">Wenn eine Taste angehalten wird, wird ein- <xref:System.Windows.Forms.Control.KeyPress> Ereignis mit der Wiederholungsrate ausgelöst, die vom Betriebssystem festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d4069-114">If a key is held down, a <xref:System.Windows.Forms.Control.KeyPress> event is raised at the repeat rate defined by the operating system.</span></span>|  
|`KeyUp`|`void OnKeyUp(KeyEventArgs)`|<span data-ttu-id="d4069-115">Wird ausgelöst, wenn eine Taste losgelassen wird.</span><span class="sxs-lookup"><span data-stu-id="d4069-115">Raised when a key is released.</span></span>|  
  
> [!NOTE]
> <span data-ttu-id="d4069-116">Das Bearbeiten von Tastatureingaben ist wesentlich komplexer als das Überschreiben der Ereignisse in der obigen Tabelle und würde Rahmen dieses Themas sprengen.</span><span class="sxs-lookup"><span data-stu-id="d4069-116">Handling keyboard input is considerably more complex than overriding the events in the preceding table and is beyond the scope of this topic.</span></span> <span data-ttu-id="d4069-117">Weitere Informationen finden Sie unter [Benutzereingaben in Windows Forms](../user-input-in-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="d4069-117">For more information, see [User Input in Windows Forms](../user-input-in-windows-forms.md).</span></span>  
  
## <a name="mouse-events"></a><span data-ttu-id="d4069-118">Mausereignisse</span><span class="sxs-lookup"><span data-stu-id="d4069-118">Mouse Events</span></span>  

 <span data-ttu-id="d4069-119">Die Mausereignisse, die von Ihrem Steuerelement behandelt werden können <xref:System.Windows.Forms.Control.MouseDown> , sind, <xref:System.Windows.Forms.Control.MouseEnter> , <xref:System.Windows.Forms.Control.MouseHover> , <xref:System.Windows.Forms.Control.MouseLeave> , <xref:System.Windows.Forms.Control.MouseMove> und <xref:System.Windows.Forms.Control.MouseUp> .</span><span class="sxs-lookup"><span data-stu-id="d4069-119">The mouse events that your control can handle are <xref:System.Windows.Forms.Control.MouseDown>, <xref:System.Windows.Forms.Control.MouseEnter>, <xref:System.Windows.Forms.Control.MouseHover>, <xref:System.Windows.Forms.Control.MouseLeave>, <xref:System.Windows.Forms.Control.MouseMove>, and <xref:System.Windows.Forms.Control.MouseUp>.</span></span>  
  
|<span data-ttu-id="d4069-120">Veranstaltungsname</span><span class="sxs-lookup"><span data-stu-id="d4069-120">Event Name</span></span>|<span data-ttu-id="d4069-121">Zu überschreibende Methode</span><span class="sxs-lookup"><span data-stu-id="d4069-121">Method to Override</span></span>|<span data-ttu-id="d4069-122">Beschreibung des Ereignisses</span><span class="sxs-lookup"><span data-stu-id="d4069-122">Description of Event</span></span>|  
|----------------|------------------------|--------------------------|  
|`MouseDown`|`void OnMouseDown(MouseEventArgs)`|<span data-ttu-id="d4069-123">Wird ausgelöst, wenn sich der Mauszeiger über dem Steuerelement befindet und eine Maustaste gedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="d4069-123">Raised when the mouse button is pressed while the pointer is over the control.</span></span>|  
|`MouseEnter`|`void OnMouseEnter(EventArgs)`|<span data-ttu-id="d4069-124">Wird ausgelöst, wenn der Mauszeiger zunächst auf den Bereich des Steuerelements trifft.</span><span class="sxs-lookup"><span data-stu-id="d4069-124">Raised when the pointer first enters the region of the control.</span></span>|  
|`MouseHover`|`void OnMouseHover(EventArgs)`|<span data-ttu-id="d4069-125">Wird ausgelöst, wenn der Mauszeiger über das Steuerelement bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="d4069-125">Raised when the pointer hovers over the control.</span></span>|  
|`MouseLeave`|`void OnMouseLeave(EventArgs)`|<span data-ttu-id="d4069-126">Wird ausgelöst, wenn der Mauszeiger den Bereich des Steuerelements verlässt.</span><span class="sxs-lookup"><span data-stu-id="d4069-126">Raised when the pointer leaves the region of the control.</span></span>|  
|`MouseMove`|`void OnMouseMove(MouseEventArgs)`|<span data-ttu-id="d4069-127">Wird ausgelöst, wenn der Mauszeiger in den Bereich des Steuerelements wechselt.</span><span class="sxs-lookup"><span data-stu-id="d4069-127">Raised when the pointer moves in the region of the control.</span></span>|  
|`MouseUp`|`void OnMouseUp(MouseEventArgs)`|<span data-ttu-id="d4069-128">Wird ausgelöst, wenn die Maustaste losgelassen wird, während sich der Mauszeiger über dem Steuerelement befindet oder den Bereich des Steuerelements verlässt.</span><span class="sxs-lookup"><span data-stu-id="d4069-128">Raised when the mouse button is released while the pointer is over the control or the pointer leaves the region of the control.</span></span>|  
  
 <span data-ttu-id="d4069-129">Das folgende Code Fragment zeigt ein Beispiel für das Überschreiben des <xref:System.Windows.Forms.Control.MouseDown> Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="d4069-129">The following code fragment shows an example of overriding the <xref:System.Windows.Forms.Control.MouseDown> event.</span></span>  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#7](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#7)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#7](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#7)]  
  
 <span data-ttu-id="d4069-130">Das folgende Code Fragment zeigt ein Beispiel für das Überschreiben des <xref:System.Windows.Forms.Control.MouseMove> Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="d4069-130">The following code fragment shows an example of overriding the <xref:System.Windows.Forms.Control.MouseMove> event.</span></span>  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#8](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#8)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#8](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#8)]  
  
 <span data-ttu-id="d4069-131">Das folgende Code Fragment zeigt ein Beispiel für das Überschreiben des <xref:System.Windows.Forms.Control.MouseUp> Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="d4069-131">The following code fragment shows an example of overriding the <xref:System.Windows.Forms.Control.MouseUp> event.</span></span>  
  
 [!code-csharp[System.Windows.Forms.FlashTrackBar#9](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/CS/FlashTrackBar.cs#9)]
 [!code-vb[System.Windows.Forms.FlashTrackBar#9](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FlashTrackBar/VB/FlashTrackBar.vb#9)]  
  
 <span data-ttu-id="d4069-132">Für den vollständigen Quellencode für das `FlashTrackBar`-Beispiel siehe [Vorgehensweise: Erstellen eines Windows Forms-Steuerelement, das den Fortschritt anzeigt](how-to-create-a-windows-forms-control-that-shows-progress.md).</span><span class="sxs-lookup"><span data-stu-id="d4069-132">For the complete source code for the `FlashTrackBar` sample, see [How to: Create a Windows Forms Control That Shows Progress](how-to-create-a-windows-forms-control-that-shows-progress.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d4069-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4069-133">See also</span></span>

- [<span data-ttu-id="d4069-134">Ereignisse in Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="d4069-134">Events in Windows Forms Controls</span></span>](events-in-windows-forms-controls.md)
- [<span data-ttu-id="d4069-135">Definieren eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="d4069-135">Defining an Event</span></span>](defining-an-event-in-windows-forms-controls.md)
- [<span data-ttu-id="d4069-136">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="d4069-136">Events</span></span>](/dotnet/standard/events/index)
- [<span data-ttu-id="d4069-137">Benutzereingabe in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d4069-137">User Input in Windows Forms</span></span>](../user-input-in-windows-forms.md)
