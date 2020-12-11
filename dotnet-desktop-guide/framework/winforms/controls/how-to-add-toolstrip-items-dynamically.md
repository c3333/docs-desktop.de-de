---
title: 'Vorgehensweise: Dynamisches Hinzufügen von ToolStrip-Elementen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ContextMenuStrip control [Windows Forms]
- toolbars [Windows Forms], adding items dynamically
- ToolStrip control [Windows Forms]
ms.assetid: 0e8dea56-5f46-408b-914d-7e360341a234
ms.openlocfilehash: 08d08a292995cc5e12fbab3e91a0962c3b895a02
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976370"
---
# <a name="how-to-add-toolstrip-items-dynamically"></a>Vorgehensweise: Dynamisches Hinzufügen von ToolStrip-Elementen
Sie können die Auflistung von Menüelementen eines <xref:System.Windows.Forms.ToolStrip>-Steuerelements dynamisch ausfüllen, wenn das Menü geöffnet wird.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird veranschaulicht, wie Elemente einem <xref:System.Windows.Forms.ContextMenuStrip>-Steuerelement dynamisch hinzufügt werden. Außerdem wird gezeigt, wie Sie die gleiche <xref:System.Windows.Forms.ContextMenuStrip> für drei verschiedene Steuerelemente im Formular wiederverwenden.  
  
 Im Beispiel füllt ein <xref:System.Windows.Forms.ToolStripDropDown.Opening>-Ereignishandler die Auflistung von Menüelementen aus. Der <xref:System.Windows.Forms.ToolStripDropDown.Opening>-Ereignishandler überprüft die <xref:System.Windows.Forms.ContextMenuStrip.SourceControl%2A?displayProperty=nameWithType> und die <xref:System.Windows.Forms.ToolStripItem.OwnerItem%2A?displayProperty=nameWithType>-Eigenschaften und fügt eine <xref:System.Windows.Forms.ToolStripItem> hinzu, die die Quellcodeverwaltung beschreibt.  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#40](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#40)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#40](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#40)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Verweise auf die Assemblys ""System.Drawing" und "System.Windows.Forms".  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ContextMenuStrip>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- <xref:System.Windows.Forms.ToolStripDropDownButton>
- [ToolStrip-Steuerelement](toolstrip-control-windows-forms.md)
