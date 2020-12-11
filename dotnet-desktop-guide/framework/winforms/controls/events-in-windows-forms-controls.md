---
title: Ereignisse in Steuerelementen
ms.date: 03/30/2017
helpviewer_keywords:
- events [Windows Forms], custom controls (using code)
- custom controls [Windows Forms], events overview (using code)
ms.assetid: 7e3d1379-87aa-437c-afce-c99454eff30e
ms.openlocfilehash: 27edaf2d895453d64d35ba6eff724df583a9b7dd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975771"
---
# <a name="events-in-windows-forms-controls"></a><span data-ttu-id="23958-102">Ereignisse in Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="23958-102">Events in Windows Forms Controls</span></span>

<span data-ttu-id="23958-103">Ein Windows Forms-Steuerelement erbt mehr als 60 Ereignisse von <xref:System.Windows.Forms.Control?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="23958-103">A Windows Forms control inherits more than sixty events from <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span> <span data-ttu-id="23958-104">Dazu gehört das <xref:System.Windows.Forms.Control.Paint> -Ereignis, das bewirkt, dass ein Steuerelement gezeichnet wird, Ereignisse im Zusammenhang mit dem Anzeigen eines Fensters, z <xref:System.Windows.Forms.Control.Resize> <xref:System.Windows.Forms.Control.Layout> . b. die Ereignisse und</span><span class="sxs-lookup"><span data-stu-id="23958-104">These include the <xref:System.Windows.Forms.Control.Paint> event, which causes a control to be drawn, events related to displaying a window, such as the <xref:System.Windows.Forms.Control.Resize> and <xref:System.Windows.Forms.Control.Layout> events, and low-level mouse and keyboard events.</span></span> <span data-ttu-id="23958-105">Einige Ereignisse auf niedriger Ebene werden <xref:System.Windows.Forms.Control> in Semantik Ereignisse wie und synthetisiert <xref:System.Windows.Forms.Control.Click> <xref:System.Windows.Forms.Control.DoubleClick> .</span><span class="sxs-lookup"><span data-stu-id="23958-105">Some low-level events are synthesized by <xref:System.Windows.Forms.Control> into semantic events such as <xref:System.Windows.Forms.Control.Click> and <xref:System.Windows.Forms.Control.DoubleClick>.</span></span> <span data-ttu-id="23958-106">Ausführliche Informationen zu geerbten Ereignissen finden Sie unter <xref:System.Windows.Forms.Control> .</span><span class="sxs-lookup"><span data-stu-id="23958-106">For details about inherited events, see <xref:System.Windows.Forms.Control>.</span></span>  
  
 <span data-ttu-id="23958-107">Wenn das benutzerdefinierte Steuerelement geerbte Ereignisfunktionen überschreiben muss, hängen Sie keinen Delegaten an, sondern überschreiben Sie die geerbte Methode `On`*EventName*.</span><span class="sxs-lookup"><span data-stu-id="23958-107">If your custom control needs to override inherited event functionality, override the inherited `On`*EventName* method instead of attaching a delegate.</span></span> <span data-ttu-id="23958-108">Wenn Sie mit dem Ereignismodell in .NET Framework nicht vertraut sind, finden Sie unter [Auslösen von Ereignissen aus einer Komponente](/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120)) weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="23958-108">If you are not familiar with the event model in the .NET Framework, see [Raising Events from a Component](/previous-versions/visualstudio/visual-studio-2013/sh2e3k5z(v=vs.120)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="23958-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23958-109">See also</span></span>

- [<span data-ttu-id="23958-110">Überschreiben der OnPaint-Methode</span><span class="sxs-lookup"><span data-stu-id="23958-110">Overriding the OnPaint Method</span></span>](overriding-the-onpaint-method.md)
- [<span data-ttu-id="23958-111">Behandeln von Benutzereingaben</span><span class="sxs-lookup"><span data-stu-id="23958-111">Handling User Input</span></span>](handling-user-input.md)
- [<span data-ttu-id="23958-112">Definieren eines Ereignisses</span><span class="sxs-lookup"><span data-stu-id="23958-112">Defining an Event</span></span>](defining-an-event-in-windows-forms-controls.md)
- [<span data-ttu-id="23958-113">Ereignisse</span><span class="sxs-lookup"><span data-stu-id="23958-113">Events</span></span>](/dotnet/standard/events/index)
