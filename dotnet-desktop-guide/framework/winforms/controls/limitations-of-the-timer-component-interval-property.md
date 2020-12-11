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
# <a name="limitations-of-the-windows-forms-timer-components-interval-property"></a>Einschränkungen für die Interval-Eigenschaft der Timer-Komponente in Windows Forms

Die Windows Forms <xref:System.Windows.Forms.Timer> Komponente verfügt über eine- <xref:System.Windows.Forms.Timer.Interval%2A> Eigenschaft, die die Anzahl von Millisekunden angibt, die zwischen einem Zeit Geber Ereignis und dem nächsten übergeben werden. Wenn die Komponente nicht deaktiviert ist, empfängt ein Timer das <xref:System.Windows.Forms.Timer.Tick> Ereignis weiterhin ungefähr gleichzeitig.  
  
 Diese Komponente wurde für eine Windows Forms-Umgebung entwickelt. Wenn Sie einen für eine Serverumgebung geeigneten Timer benötigen, lesen Sie die Informationen unter [Introduction to Server-Based Timers (Einführung in serverbasierte Timer)](/previous-versions/visualstudio/visual-studio-2008/tb9yt5e6(v=vs.90)).  
  
## <a name="the-interval-property"></a>Die Interval-Eigenschaft  

 Die- <xref:System.Windows.Forms.Timer.Interval%2A> Eigenschaft hat einige Einschränkungen, die beim Programmieren einer-Komponente zu beachten sind <xref:System.Windows.Forms.Timer> :  
  
- Wenn Ihre Anwendung oder eine andere Anwendung hohe Anforderungen an das System – wie z. b. lange Schleifen, intensive Berechnungen oder Laufwerk-, Netzwerk-oder Port Zugriffe –, erhält die Anwendung möglicherweise keine Zeit Geber Ereignisse, die von der- <xref:System.Windows.Forms.Timer.Interval%2A> Eigenschaft angegeben werden.  
  
- Es ist nicht garantiert, dass das Intervall genau in der Zeit abläuft. Um die Genauigkeit zu gewährleisten, sollte der Timer die Systemuhr nach Bedarf überprüfen, anstatt zu versuchen, die kumulierte Zeit intern nachzuverfolgen.  
  
- Die Genauigkeit der <xref:System.Windows.Forms.Timer.Interval%2A> Eigenschaft wird in Millisekunden angegeben. Einige Computer bieten einen Leistungs befassleistungs-Leistungs Bewert, der eine höhere Auflösung als Millisekunden aufweist. Die Verfügbarkeit eines solchen Zählers hängt von der Prozessor Hardware des Computers ab.
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Timer>
- [Timer-Komponente](timer-component-windows-forms.md)
- [Übersicht über die Timer-Komponente](timer-component-overview-windows-forms.md)
