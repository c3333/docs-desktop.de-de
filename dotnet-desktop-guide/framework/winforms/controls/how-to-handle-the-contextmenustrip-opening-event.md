---
title: 'Vorgehensweise: Behandeln des Opening-Ereignisses von ContextMenuStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ContextMenuStrip control [Windows Forms]
- context menus [Windows Forms], event handling
- ToolStrip control [Windows Forms]
- event handling [Windows Forms], context menus
- shortcut menus [Windows Forms], event handling
ms.assetid: b661b3dd-7815-4cc2-a1aa-a9a391ab3427
ms.openlocfilehash: 3001480959ef90cb31048cbcf70aeff1632979fb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976297"
---
# <a name="how-to-handle-the-contextmenustrip-opening-event"></a>Vorgehensweise: Behandeln des Opening-Ereignisses von ContextMenuStrip
Sie können das Verhalten des Steuer Elements anpassen, <xref:System.Windows.Forms.ContextMenuStrip> indem Sie das- <xref:System.Windows.Forms.ToolStripDropDown.Opening> Ereignis behandeln.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird veranschaulicht, wie das-Ereignis behandelt wird <xref:System.Windows.Forms.ToolStripDropDown.Opening> . Der-Ereignishandler fügt einem-Steuerelement dynamisch Elemente hinzu <xref:System.Windows.Forms.ContextMenuStrip> . Das gesamte Codebeispiel finden Sie unter Gewusst [wie: Dynamisches Hinzufügen von ToolStrip-Elementen](how-to-add-toolstrip-items-dynamically.md).  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#42](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#42)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#42)]  
  
 Legen Sie die- <xref:System.ComponentModel.CancelEventArgs.Cancel%2A?displayProperty=nameWithType> Eigenschaft auf fest `true` , um das Öffnen des Menüs zu verhindern.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.ComponentModel.CancelEventArgs.Cancel%2A>
- <xref:System.Windows.Forms.ToolStripDropDown>
- [ToolStrip-Steuerelement](toolstrip-control-windows-forms.md)
