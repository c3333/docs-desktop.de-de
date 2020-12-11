---
title: 'Gewusst wie: Ändern der Geschwindigkeit einer Uhr, ohne die Geschwindigkeit ihrer Zeitachse zu ändern'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- speed of Clock [WPF], changing
- clocks [WPF], changing speed of
ms.assetid: 72f36dd0-f085-445d-8589-19a83fe74f5e
ms.openlocfilehash: 19e6874b9b472cb4a5f716677f99af03f2b73b10
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972134"
---
# <a name="how-to-change-the-speed-of-a-clock-without-changing-the-speed-of-its-timeline"></a>Gewusst wie: Ändern der Geschwindigkeit einer Uhr, ohne die Geschwindigkeit ihrer Zeitachse zu ändern
Die <xref:System.Windows.Media.Animation.ClockController> -Eigenschaft eines-Objekts <xref:System.Windows.Media.Animation.ClockController.SpeedRatio%2A> ermöglicht es Ihnen, die Geschwindigkeit eines zu ändern, <xref:System.Windows.Media.Animation.Clock> ohne die <xref:System.Windows.Media.Animation.Timeline.SpeedRatio%2A> der der Uhr zu ändern <xref:System.Windows.Media.Animation.Timeline> . Im folgenden Beispiel <xref:System.Windows.Media.Animation.ClockController> wird ein verwendet, um die einer Uhr interaktiv zu ändern <xref:System.Windows.Media.Animation.ClockController.SpeedRatio%2A> . Das- <xref:System.Windows.Media.Animation.Clock.CurrentGlobalSpeedInvalidated> Ereignis und die- <xref:System.Windows.Media.Animation.Clock.CurrentGlobalSpeed%2A> Eigenschaft der Uhr werden verwendet, um die aktuelle globale Geschwindigkeit der Uhr jedes Mal anzuzeigen, wenn der interaktive Wert <xref:System.Windows.Media.Animation.ClockController.SpeedRatio%2A> geändert wird.  
  
## <a name="example"></a>Beispiel  
 [!code-csharp[timingbehaviors_procedural_snip#GraphicsMMClockControllerSpeedRatioExample](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_procedural_snip/CSharp/ClockControllerSpeedRatioExample.cs#graphicsmmclockcontrollerspeedratioexample)]
 [!code-vb[timingbehaviors_procedural_snip#GraphicsMMClockControllerSpeedRatioExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_procedural_snip/visualbasic/clockcontrollerspeedratioexample.vb#graphicsmmclockcontrollerspeedratioexample)]
