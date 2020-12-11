---
title: Einschränkungen der Eigenschaft "Intervall für Timer-Komponenten"
ms.date: 03/30/2017
helpviewer_keywords:
- timers [Windows Forms], event intervals
- Interval property [Windows Forms], limitations
- timers [Windows Forms], Windows-based
- Timer component [Windows Forms], limitations of Interval property
ms.assetid: 7e5fb513-77e7-4046-a8e8-aab94e61ca0f
ms.openlocfilehash: 90023a20b32cc4f5709d35f4e8c0a339e1d46751
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976722"
---
# <a name="limitations-of-the-windows-forms-timer-components-interval-property"></a><span data-ttu-id="2893a-102">Einschränkungen für die Interval-Eigenschaft der Timer-Komponente in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2893a-102">Limitations of the Windows Forms Timer Component's Interval Property</span></span>

<span data-ttu-id="2893a-103">Die Windows Forms <xref:System.Windows.Forms.Timer> Komponente verfügt über eine- <xref:System.Windows.Forms.Timer.Interval%2A> Eigenschaft, die die Anzahl von Millisekunden angibt, die zwischen einem Zeit Geber Ereignis und dem nächsten übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="2893a-103">The Windows Forms <xref:System.Windows.Forms.Timer> component has an <xref:System.Windows.Forms.Timer.Interval%2A> property that specifies the number of milliseconds that pass between one timer event and the next.</span></span> <span data-ttu-id="2893a-104">Wenn die Komponente nicht deaktiviert ist, empfängt ein Timer das <xref:System.Windows.Forms.Timer.Tick> Ereignis weiterhin ungefähr gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="2893a-104">Unless the component is disabled, a timer continues to receive the <xref:System.Windows.Forms.Timer.Tick> event at roughly equal intervals of time.</span></span>  
  
 <span data-ttu-id="2893a-105">Diese Komponente wurde für eine Windows Forms-Umgebung entwickelt.</span><span class="sxs-lookup"><span data-stu-id="2893a-105">This component is designed for a Windows Forms environment.</span></span> <span data-ttu-id="2893a-106">Wenn Sie einen für eine Serverumgebung geeigneten Timer benötigen, lesen Sie die Informationen unter [Introduction to Server-Based Timers (Einführung in serverbasierte Timer)](/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).</span><span class="sxs-lookup"><span data-stu-id="2893a-106">If you need a timer that is suitable for a server environment, see [Introduction to Server-Based Timers](/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).</span></span>  
  
## <a name="the-interval-property"></a><span data-ttu-id="2893a-107">Die Interval-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="2893a-107">The Interval Property</span></span>  

 <span data-ttu-id="2893a-108">Die- <xref:System.Windows.Forms.Timer.Interval%2A> Eigenschaft hat einige Einschränkungen, die beim Programmieren einer-Komponente zu beachten sind <xref:System.Windows.Forms.Timer> :</span><span class="sxs-lookup"><span data-stu-id="2893a-108">The <xref:System.Windows.Forms.Timer.Interval%2A> property has a few limitations to consider when you are programming a <xref:System.Windows.Forms.Timer> component:</span></span>  
  
- <span data-ttu-id="2893a-109">Wenn Ihre Anwendung oder eine andere Anwendung hohe Anforderungen an das System – wie z. b. lange Schleifen, intensive Berechnungen oder Laufwerk-, Netzwerk-oder Port Zugriffe –, erhält die Anwendung möglicherweise keine Zeit Geber Ereignisse, die von der- <xref:System.Windows.Forms.Timer.Interval%2A> Eigenschaft angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2893a-109">If your application or another application is making heavy demands on the system — such as long loops, intensive calculations, or drive, network, or port access — your application may not get timer events as often as the <xref:System.Windows.Forms.Timer.Interval%2A> property specifies.</span></span>  
  
- <span data-ttu-id="2893a-110">Es ist nicht garantiert, dass das Intervall genau in der Zeit abläuft.</span><span class="sxs-lookup"><span data-stu-id="2893a-110">The interval is not guaranteed to elapse exactly on time.</span></span> <span data-ttu-id="2893a-111">Um die Genauigkeit zu gewährleisten, sollte der Timer die Systemuhr nach Bedarf überprüfen, anstatt zu versuchen, die kumulierte Zeit intern nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="2893a-111">To ensure accuracy, the timer should check the system clock as needed, rather than try to keep track of accumulated time internally.</span></span>  
  
- <span data-ttu-id="2893a-112">Die Genauigkeit der <xref:System.Windows.Forms.Timer.Interval%2A> Eigenschaft wird in Millisekunden angegeben.</span><span class="sxs-lookup"><span data-stu-id="2893a-112">The precision of the <xref:System.Windows.Forms.Timer.Interval%2A> property is in milliseconds.</span></span> <span data-ttu-id="2893a-113">Einige Computer bieten einen Leistungs befassleistungs-Leistungs Bewert, der eine höhere Auflösung als Millisekunden aufweist.</span><span class="sxs-lookup"><span data-stu-id="2893a-113">Some computers provide a high-resolution counter that has a resolution higher than milliseconds.</span></span> <span data-ttu-id="2893a-114">Die Verfügbarkeit eines solchen Zählers hängt von der Prozessor Hardware des Computers ab.</span><span class="sxs-lookup"><span data-stu-id="2893a-114">The availability of such a counter depends on the processor hardware of your computer.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2893a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2893a-115">See also</span></span>

- <xref:System.Windows.Forms.Timer>
- [<span data-ttu-id="2893a-116">Timer-Komponente</span><span class="sxs-lookup"><span data-stu-id="2893a-116">Timer Component</span></span>](timer-component-windows-forms.md)
- [<span data-ttu-id="2893a-117">Übersicht über die Timer-Komponente</span><span class="sxs-lookup"><span data-stu-id="2893a-117">Timer Component Overview</span></span>](timer-component-overview-windows-forms.md)
