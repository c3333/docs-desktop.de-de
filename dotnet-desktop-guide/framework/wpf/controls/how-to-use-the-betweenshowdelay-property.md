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
# <a name="how-to-use-the-betweenshowdelay-property"></a><span data-ttu-id="4c937-102">Gewusst wie: Verwenden der BetweenShowDelay-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4c937-102">How to: Use the BetweenShowDelay Property</span></span>
<span data-ttu-id="4c937-103">In diesem Beispiel wird gezeigt, wie die Time-Eigenschaft verwendet wird <xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A> , damit Quick Infos schnell angezeigt werden – mit wenigen oder gar keinen Verzögerungen – wenn ein Benutzer den Mauszeiger von einer QuickInfo direkt zu einem anderen verschiebt.</span><span class="sxs-lookup"><span data-stu-id="4c937-103">This example shows how to use the <xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A> time property so that tooltips appear quickly—with little or no delay—when a user moves the mouse pointer from one tooltip directly to another.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4c937-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4c937-104">Example</span></span>  
 <span data-ttu-id="4c937-105">Im folgenden Beispiel <xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A> wird die-Eigenschaft auf eine Sekunde (1000 Millisekunden) und <xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A> auf zwei Sekunden (2000 Millisekunden) für die Quick Infos beider Steuerelemente festgelegt <xref:System.Windows.Shapes.Ellipse> .</span><span class="sxs-lookup"><span data-stu-id="4c937-105">In the following example, the <xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A> property is set to one second (1000 milliseconds) and the <xref:System.Windows.Controls.ToolTipService.BetweenShowDelay%2A> is set to two seconds (2000 milliseconds) for the tooltips of both <xref:System.Windows.Shapes.Ellipse> controls.</span></span> <span data-ttu-id="4c937-106">Wenn Sie die QuickInfo für eine der Ellipsen anzeigen und den Mauszeiger innerhalb von zwei Sekunden auf eine andere Ellipse bewegen und anhalten, wird die QuickInfo der zweiten Ellipse sofort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4c937-106">If you display the tooltip for one of the ellipses and then move the mouse pointer to another ellipse within two seconds and pause on it, the tooltip of the second ellipse displays immediately.</span></span>  
  
 <span data-ttu-id="4c937-107">In einem der folgenden Szenarien wird <xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A> angewendet, das bewirkt, dass die QuickInfo für die zweite Ellipse eine Sekunde wartet, bevor Sie angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="4c937-107">In either of the following scenarios, the <xref:System.Windows.Controls.ToolTipService.InitialShowDelay%2A> applies, which causes the tooltip for the second ellipse to wait one second before it appears:</span></span>  
  
- <span data-ttu-id="4c937-108">Wenn die Umstellung auf die zweite Schaltfläche mehr als zwei Sekunden dauert.</span><span class="sxs-lookup"><span data-stu-id="4c937-108">If the time it takes to move to the second button is more than two seconds.</span></span>  
  
- <span data-ttu-id="4c937-109">, Wenn die QuickInfo am Anfang des Zeitintervalls für die erste Ellipse nicht sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="4c937-109">If the tooltip is not visible at the beginning of the time interval for the first ellipse.</span></span>  
  
 [!code-xaml[ToolTipService#ToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#tooltip)]  
[!code-xaml[ToolTipService#NoToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#notooltip)]  
  
## <a name="see-also"></a><span data-ttu-id="4c937-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4c937-110">See also</span></span>

- <xref:System.Windows.Controls.ToolTip>
- <xref:System.Windows.Controls.ToolTipService>
- [<span data-ttu-id="4c937-111">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="4c937-111">How-to Topics</span></span>](tooltip-how-to-topics.md)
- [<span data-ttu-id="4c937-112">Übersicht über die QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4c937-112">ToolTip Overview</span></span>](tooltip-overview.md)
