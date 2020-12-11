---
title: 'Gewusst wie: Verwenden der BetweenShowDelay-Eigenschaft'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolTip control [WPF], BetweenShowDelay time property
- BetweenShowDelay time property [WPF]
ms.assetid: 984ea76d-f2a2-4326-a02e-f97ec3d036d6
ms.openlocfilehash: 9b63675ec21294496117860aa5b58af132c4284a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976560"
---
# <a name="how-to-use-the-betweenshowdelay-property"></a>Gewusst wie: Verwenden der BetweenShowDelay-Eigenschaft
In diesem Beispiel wird gezeigt, wie die Time-Eigenschaft verwendet wird <xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A> , damit Quick Infos schnell angezeigt werden – mit wenigen oder gar keinen Verzögerungen – wenn ein Benutzer den Mauszeiger von einer QuickInfo direkt zu einem anderen verschiebt.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel <xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A> wird die-Eigenschaft auf eine Sekunde (1000 Millisekunden) und <xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A> auf zwei Sekunden (2000 Millisekunden) für die Quick Infos beider Steuerelemente festgelegt <xref:System.Windows.Shapes.Ellipse> . Wenn Sie die QuickInfo für eine der Ellipsen anzeigen und den Mauszeiger innerhalb von zwei Sekunden auf eine andere Ellipse bewegen und anhalten, wird die QuickInfo der zweiten Ellipse sofort angezeigt.  
  
 In einem der folgenden Szenarien wird <xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A> angewendet, das bewirkt, dass die QuickInfo für die zweite Ellipse eine Sekunde wartet, bevor Sie angezeigt wird:  
  
- Wenn die Umstellung auf die zweite Schaltfläche mehr als zwei Sekunden dauert.  
  
- , Wenn die QuickInfo am Anfang des Zeitintervalls für die erste Ellipse nicht sichtbar ist.  
  
 [!code-xaml[ToolTipService#ToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#tooltip)]  
[!code-xaml[ToolTipService#NoToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#notooltip)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.ToolTip>
- <xref:System.Windows.Controls.ToolTipService>
- [Artikel zu Vorgehensweisen](tooltip-how-to-topics.md)
- [Übersicht über die QuickInfo](tooltip-overview.md)
