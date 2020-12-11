---
title: 'Gewusst wie: Abrufen oder Festlegen eines Dockwerts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Dock values [WPF], setting
- Dock values [WPF], getting
ms.assetid: fcf4ab8a-c7cd-4835-8d04-de1c999ab4a8
ms.openlocfilehash: fb6c8a7d62aa09a6e1d82cb4079d1425a7f39f8c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976626"
---
# <a name="how-to-get-or-set-a-dock-value"></a><span data-ttu-id="7f255-102">Gewusst wie: Abrufen oder Festlegen eines Dockwerts</span><span class="sxs-lookup"><span data-stu-id="7f255-102">How to: Get or Set a Dock Value</span></span>
<span data-ttu-id="7f255-103">Im folgenden Beispiel wird gezeigt, wie ein- <xref:System.Windows.Controls.Dock> Wert für ein-Objekt zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7f255-103">The following example shows how to assign a <xref:System.Windows.Controls.Dock> value for an object.</span></span> <span data-ttu-id="7f255-104">Das Beispiel verwendet die <xref:System.Windows.Controls.DockPanel.GetDock%2A> -Methode und die- <xref:System.Windows.Controls.DockPanel.SetDock%2A> Methode von <xref:System.Windows.Controls.DockPanel> .</span><span class="sxs-lookup"><span data-stu-id="7f255-104">The example uses the <xref:System.Windows.Controls.DockPanel.GetDock%2A> and <xref:System.Windows.Controls.DockPanel.SetDock%2A> methods of <xref:System.Windows.Controls.DockPanel>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7f255-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7f255-105">Example</span></span>  
 <span data-ttu-id="7f255-106">Im Beispiel wird eine Instanz des <xref:System.Windows.Controls.TextBlock> -Elements, `txt1` , erstellt und <xref:System.Windows.Controls.Dock> `Top` mithilfe der- <xref:System.Windows.Controls.DockPanel.SetDock%2A> Methode von der Wert zugewiesen <xref:System.Windows.Controls.DockPanel> .</span><span class="sxs-lookup"><span data-stu-id="7f255-106">The example creates an instance of the <xref:System.Windows.Controls.TextBlock> element, `txt1`, and assigns a <xref:System.Windows.Controls.Dock> value of `Top` by using the <xref:System.Windows.Controls.DockPanel.SetDock%2A> method of <xref:System.Windows.Controls.DockPanel>.</span></span> <span data-ttu-id="7f255-107">Anschließend fügt Sie den Wert der- <xref:System.Windows.Controls.Dock> Eigenschaft <xref:System.Windows.Controls.TextBlock.Text%2A> mithilfe der-Methode an die des-Elements an <xref:System.Windows.Controls.TextBlock> <xref:System.Windows.Controls.DockPanel.GetDock%2A> .</span><span class="sxs-lookup"><span data-stu-id="7f255-107">It then appends the value of the <xref:System.Windows.Controls.Dock> property to the <xref:System.Windows.Controls.TextBlock.Text%2A> of the <xref:System.Windows.Controls.TextBlock> element by using the <xref:System.Windows.Controls.DockPanel.GetDock%2A> method.</span></span> <span data-ttu-id="7f255-108">Schließlich wird das-Element im Beispiel dem <xref:System.Windows.Controls.TextBlock> übergeordneten Element hinzugefügt <xref:System.Windows.Controls.DockPanel> `dp1` .</span><span class="sxs-lookup"><span data-stu-id="7f255-108">Finally, the example adds the <xref:System.Windows.Controls.TextBlock> element to the parent <xref:System.Windows.Controls.DockPanel>, `dp1`.</span></span>  
  
 [!code-csharp[DockPanelSetDock#1](~/samples/snippets/csharp/VS_Snippets_Wpf/DockPanelSetDock/CSharp/DockPanel_SetDock.cs#1)]
 [!code-vb[DockPanelSetDock#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DockPanelSetDock/VisualBasic/DockPanel_SetDock.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="7f255-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f255-109">See also</span></span>

- <xref:System.Windows.Controls.DockPanel>
- <xref:System.Windows.Controls.DockPanel.GetDock%2A>
- <xref:System.Windows.Controls.DockPanel.SetDock%2A>
- [<span data-ttu-id="7f255-110">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="7f255-110">Panels Overview</span></span>](panels-overview.md)
