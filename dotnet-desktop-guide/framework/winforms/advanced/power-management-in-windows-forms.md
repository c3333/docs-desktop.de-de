---
title: Energieverwaltung
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- battery states
- power states
ms.assetid: ad04a801-5682-4d88-92c5-26eb9cdb209a
ms.openlocfilehash: 9ac39df43a08f62e50116c61c4bdeda4cd1c8281
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976070"
---
# <a name="power-management-in-windows-forms"></a><span data-ttu-id="a8ae6-102">Energieverwaltung in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="a8ae6-102">Power Management in Windows Forms</span></span>
<span data-ttu-id="a8ae6-103">Ihre Windows Forms Anwendungen können die Energie Verwaltungsfunktionen des Windows-Betriebssystems nutzen.</span><span class="sxs-lookup"><span data-stu-id="a8ae6-103">Your Windows Forms applications can take advantage of the power management features in the Windows operating system.</span></span> <span data-ttu-id="a8ae6-104">Ihre Anwendungen können den Energiestatus eines Computers überwachen und Maßnahmen ergreifen, wenn eine Statusänderung auftritt.</span><span class="sxs-lookup"><span data-stu-id="a8ae6-104">Your applications can monitor the power status of a computer and take action when a status change occurs.</span></span> <span data-ttu-id="a8ae6-105">Wenn Ihre Anwendung z. b. auf einem tragbaren Computer ausgeführt wird, möchten Sie möglicherweise bestimmte Features in Ihrer Anwendung deaktivieren, wenn die Akku Belastung des Computers unter einer bestimmten Ebene liegt.</span><span class="sxs-lookup"><span data-stu-id="a8ae6-105">For example, if your application is running on a portable computer, you might want to disable certain features in your application when the computer's battery charge falls under a certain level.</span></span>  
  
 <span data-ttu-id="a8ae6-106">Der .NET Framework stellt ein <xref:Microsoft.Win32.SystemEvents.PowerModeChanged> Ereignis bereit, das auftritt, wenn sich der Energiestatus ändert, z. b. Wenn ein Benutzer das Betriebssystem anhält oder fortsetzt oder wenn sich der Wechsel Stromstatus oder der Akku Status ändert.</span><span class="sxs-lookup"><span data-stu-id="a8ae6-106">The .NET Framework provides a <xref:Microsoft.Win32.SystemEvents.PowerModeChanged> event that occurs whenever there is a change in power status, such as when a user suspends or resumes the operating system, or when the AC power status or battery status changes.</span></span> <span data-ttu-id="a8ae6-107">Die- <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A> Eigenschaft der- <xref:System.Windows.Forms.SystemInformation> Klasse kann verwendet werden, um den aktuellen Status abzufragen, wie im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8ae6-107">The <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A> property of the <xref:System.Windows.Forms.SystemInformation> class can be used to query for the current status, as shown in the following code example.</span></span>  
  
 [!code-csharp[PowerMode#1](~/samples/snippets/csharp/VS_Snippets_Winforms/powermode/cs/form1.cs#1)]
 [!code-vb[PowerMode#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/powermode/vb/form1.vb#1)]  
  
 <span data-ttu-id="a8ae6-108">Neben den <xref:System.Windows.Forms.BatteryChargeStatus> Enumerationen enthält die- <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A> Eigenschaft auch Enumerationen zum Ermitteln der Akkukapazität ( <xref:System.Windows.Forms.PowerStatus.BatteryFullLifetime%2A> ) und des Akku Lade Prozentsatzes ( <xref:System.Windows.Forms.PowerStatus.BatteryLifePercent%2A> , <xref:System.Windows.Forms.PowerStatus.BatteryLifeRemaining%2A> ).</span><span class="sxs-lookup"><span data-stu-id="a8ae6-108">Besides the <xref:System.Windows.Forms.BatteryChargeStatus> enumerations, the <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A> property also contains enumerations for determining battery capacity (<xref:System.Windows.Forms.PowerStatus.BatteryFullLifetime%2A>) and battery charge percentage (<xref:System.Windows.Forms.PowerStatus.BatteryLifePercent%2A>, <xref:System.Windows.Forms.PowerStatus.BatteryLifeRemaining%2A>).</span></span>  
  
 <span data-ttu-id="a8ae6-109">Mit der-Methode von können Sie einen Computer in den Ruhezustand oder den Unterbrechungs <xref:System.Windows.Forms.Application.SetSuspendState%2A> <xref:System.Windows.Forms.Application> Modus versetzen.</span><span class="sxs-lookup"><span data-stu-id="a8ae6-109">You can use the <xref:System.Windows.Forms.Application.SetSuspendState%2A> method of the <xref:System.Windows.Forms.Application> to put a computer into hibernation or suspend mode.</span></span> <span data-ttu-id="a8ae6-110">Wenn das- `force` Argument auf festgelegt ist `false` , überträgt das Betriebssystem ein Ereignis an alle Anwendungen, die die Berechtigung zum aussetzen anfordern.</span><span class="sxs-lookup"><span data-stu-id="a8ae6-110">If the `force` argument is set to `false`, the operating system will broadcast an event to all applications requesting permission to suspend.</span></span> <span data-ttu-id="a8ae6-111">Wenn das- `disableWakeEvent` Argument auf festgelegt ist `true` , deaktiviert das Betriebssystem alle Wake-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="a8ae6-111">If the `disableWakeEvent` argument is set to `true`, the operating system disables all wake events.</span></span>  
  
 <span data-ttu-id="a8ae6-112">Im folgenden Codebeispiel wird veranschaulicht, wie ein Computer in den Ruhezustand versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="a8ae6-112">The following code example demonstrates how to put a computer into hibernation.</span></span>  
  
 [!code-csharp[PowerMode#2](~/samples/snippets/csharp/VS_Snippets_Winforms/powermode/cs/form1.cs#2)]
 [!code-vb[PowerMode#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/powermode/vb/form1.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="a8ae6-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8ae6-113">See also</span></span>

- <xref:Microsoft.Win32.SystemEvents.PowerModeChanged>
- <xref:System.Windows.Forms.SystemInformation.PowerStatus%2A>
- <xref:System.Windows.Forms.Application.SetSuspendState%2A>
- <xref:Microsoft.Win32.SystemEvents.SessionSwitch>
