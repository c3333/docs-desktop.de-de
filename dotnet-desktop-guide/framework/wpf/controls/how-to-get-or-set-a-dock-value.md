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
# <a name="how-to-get-or-set-a-dock-value"></a>Gewusst wie: Abrufen oder Festlegen eines Dockwerts
Im folgenden Beispiel wird gezeigt, wie ein- <xref:System.Windows.Controls.Dock> Wert für ein-Objekt zugewiesen wird. Das Beispiel verwendet die <xref:System.Windows.Controls.DockPanel.GetDock%2A> -Methode und die- <xref:System.Windows.Controls.DockPanel.SetDock%2A> Methode von <xref:System.Windows.Controls.DockPanel> .  
  
## <a name="example"></a>Beispiel  
 Im Beispiel wird eine Instanz des <xref:System.Windows.Controls.TextBlock> -Elements, `txt1` , erstellt und <xref:System.Windows.Controls.Dock> `Top` mithilfe der- <xref:System.Windows.Controls.DockPanel.SetDock%2A> Methode von der Wert zugewiesen <xref:System.Windows.Controls.DockPanel> . Anschließend fügt Sie den Wert der- <xref:System.Windows.Controls.Dock> Eigenschaft <xref:System.Windows.Controls.TextBlock.Text%2A> mithilfe der-Methode an die des-Elements an <xref:System.Windows.Controls.TextBlock> <xref:System.Windows.Controls.DockPanel.GetDock%2A> . Schließlich wird das-Element im Beispiel dem <xref:System.Windows.Controls.TextBlock> übergeordneten Element hinzugefügt <xref:System.Windows.Controls.DockPanel> `dp1` .  
  
 [!code-csharp[DockPanelSetDock#1](~/samples/snippets/csharp/VS_Snippets_Wpf/DockPanelSetDock/CSharp/DockPanel_SetDock.cs#1)]
 [!code-vb[DockPanelSetDock#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DockPanelSetDock/VisualBasic/DockPanel_SetDock.vb#1)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.DockPanel>
- <xref:System.Windows.Controls.DockPanel.GetDock%2A>
- <xref:System.Windows.Controls.DockPanel.SetDock%2A>
- [Übersicht über Panel-Elemente](panels-overview.md)
