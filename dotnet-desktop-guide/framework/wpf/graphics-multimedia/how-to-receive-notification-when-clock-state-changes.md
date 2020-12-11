---
title: 'Gewusst wie: Empfangen von Benachrichtigungen bei Statusänderungen der Uhr'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- clocks [WPF], notification of state changes
- notifications [WPF], clocks' state changes
ms.assetid: ecb10fc9-d0c2-45c3-b0a1-7b11baa733da
ms.openlocfilehash: dc3fffb88ce59ceb908d6febd2f078820513b641
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975310"
---
# <a name="how-to-receive-notification-when-a-clocks-state-changes"></a>Gewusst wie: Empfangen von Benachrichtigungen bei Statusänderungen der Uhr
Das-Ereignis einer Uhr <xref:System.Windows.Media.Animation.Clock.CurrentStateInvalidated> tritt auf <xref:System.Windows.Media.Animation.Clock.CurrentState%2A> , wenn Ihr ungültig wird, z. b. wenn die Uhr startet oder beendet wird. Sie können sich für dieses Ereignis direkt mit einem registrieren <xref:System.Windows.Media.Animation.Clock> , oder Sie können sich mithilfe eines registrieren <xref:System.Windows.Media.Animation.Timeline> .  
  
 Im folgenden Beispiel <xref:System.Windows.Media.Animation.Storyboard> werden ein-und zwei- <xref:System.Windows.Media.Animation.DoubleAnimation> Objekte verwendet, um die Breite von zwei Rechtecke zu animieren. Das- <xref:System.Windows.Media.Animation.Timeline.CurrentStateInvalidated> Ereignis wird verwendet, um auf Änderungen am Uhr Zustand zu lauschen.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[timingbehaviors_snip#_graphicsmm_StateExampleMarkupWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/StateExample.xaml#_graphicsmm_stateexamplemarkupwholepage)]  
  
 [!code-csharp[timingbehaviors_snip#_graphicsmm_StateEventHandlers](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/StateExample.xaml.cs#_graphicsmm_stateeventhandlers)]
 [!code-vb[timingbehaviors_snip#_graphicsmm_StateEventHandlers](~/samples/snippets/visualbasic/VS_Snippets_Wpf/timingbehaviors_snip/visualbasic/stateexample.xaml.vb#_graphicsmm_stateeventhandlers)]  
  
 Die folgende Abbildung zeigt die verschiedenen Zustände, die die Animationen als übergeordnete Zeitachse (*Storyboard*) eingeben.  
  
 ![Uhr-Zustände für ein Drehbuch mit zwei Animationen](./media/graphicsmm-3timelines.png "graphicsmm_3timelines")  
  
 Die folgende Tabelle zeigt die Zeiten, zu denen das Ereignis von *animation1* ausgelöst wird <xref:System.Windows.Media.Animation.Timeline.CurrentStateInvalidated> :  
  
||||||||  
|-|-|-|-|-|-|-|  
|Zeit (Sekunden)|1|10|19|21|30|39|  
|State|Aktiv|Aktiv|Beendet|Aktiv|Aktiv|Beendet|  
  
 Die folgende Tabelle zeigt die Zeiten, zu denen das Ereignis von *Animation2* ausgelöst wird <xref:System.Windows.Media.Animation.Timeline.CurrentStateInvalidated> :  
  
||||||||||  
|-|-|-|-|-|-|-|-|-|  
|Zeit (Sekunden)|1|9|11|19|21|29|31|39|  
|State|Aktiv|Ausfüllen|Aktiv|Beendet|Aktiv|Ausfüllen|Aktiv|Beendet|  
  
 Beachten Sie, dass das *animation1*-  <xref:System.Windows.Media.Animation.Timeline.CurrentStateInvalidated> Ereignis bei 10 Sekunden ausgelöst wird, auch wenn sein Zustand weiterhin besteht <xref:System.Windows.Media.Animation.ClockState.Active> . Dies liegt daran, dass sich der Zustand in 10 Sekunden geändert hat, sich jedoch von <xref:System.Windows.Media.Animation.ClockState.Active> zu <xref:System.Windows.Media.Animation.ClockState.Filling> und dann wieder zu <xref:System.Windows.Media.Animation.ClockState.Active> im gleichen Tick geändert hat.
