---
title: 'Vorgehensweise: Anfügen eines Kontextmenüs an einen Strukturansichtsknoten'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- shortcut menus [Windows Forms], adding to TreeView controls
- TreeView control [Windows Forms], adding shortcut menus
- tree nodes in TreeView control [Windows Forms], shortcut menus
ms.assetid: a23c6752-fd8f-44ad-b781-bab37962fc7c
ms.openlocfilehash: f818cccb3103866af993f1aff527a9c1a7c82109
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975720"
---
# <a name="how-to-attach-a-shortcut-menu-to-a-treeview-node"></a>Vorgehensweise: Anfügen eines Kontextmenüs an einen Strukturansichtsknoten
Das Windows Forms <xref:System.Windows.Forms.TreeView> Steuerelement zeigt eine Hierarchie von Knoten an, ähnlich den Dateien und Ordnern, die im linken Fensterbereich von Windows-Explorer angezeigt werden. Durch Festlegen der <xref:System.Windows.Forms.Control.ContextMenuStrip%2A> -Eigenschaft können Sie dem Benutzer kontextabhängige Vorgänge bereitstellen, wenn Sie mit der rechten Maustaste auf das Steuerelement klicken <xref:System.Windows.Forms.TreeView> . Durch Zuordnen einer <xref:System.Windows.Forms.ContextMenuStrip> Komponente <xref:System.Windows.Forms.TreeNode> zu einzelnen Elementen können Sie den Steuerelementen eine angepasste Ebene von Kontextmenü Funktionen hinzufügen <xref:System.Windows.Forms.TreeView> .  
  
### <a name="to-associate-a-shortcut-menu-with-a-treenode-programmatically"></a>So ordnen Sie ein Kontextmenü Programm gesteuert einem TreeNode zu  
  
1. Instanziieren <xref:System.Windows.Forms.TreeView> Sie ein-Steuerelement mit den entsprechenden Eigenschaften Einstellungen, erstellen Sie ein Stamm <xref:System.Windows.Forms.TreeNode> Verzeichnis, und fügen Sie dann untergeordnete Knoten hinzu.  
  
2. Instanziieren <xref:System.Windows.Forms.ContextMenuStrip> Sie eine-Komponente, und fügen <xref:System.Windows.Forms.ToolStripMenuItem> Sie dann für jeden Vorgang, den Sie zur Laufzeit zur Verfügung stellen möchten, ein hinzu.  
  
3. Legen Sie die- <xref:System.Windows.Forms.TreeNode.ContextMenuStrip%2A> Eigenschaft der entsprechenden <xref:System.Windows.Forms.TreeNode> auf das Kontextmenü fest, das Sie erstellen.  
  
4. Wenn diese Eigenschaft festgelegt ist, wird das Kontextmenü angezeigt, wenn Sie mit der rechten Maustaste auf den Knoten klicken.  
  
 Im folgenden Codebeispiel wird ein einfaches-Element erstellt, das <xref:System.Windows.Forms.TreeView> <xref:System.Windows.Forms.ContextMenuStrip> dem Stamm des zugeordnet ist <xref:System.Windows.Forms.TreeNode> <xref:System.Windows.Forms.TreeView> . Sie müssen die Menü Optionen an die von <xref:System.Windows.Forms.TreeView> Ihnen entwickelten Optionen anpassen. Außerdem sollten Sie Code schreiben, um die <xref:System.Windows.Forms.ToolStripItem.Click> Ereignisse für diese Menü Elemente zu behandeln.  
  
 [!code-cpp[System.Windows.Forms.TreeNodeContextMenuStrip#1](~/samples/snippets/cpp/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/cpp/Form1.cpp#1)]
 [!code-csharp[System.Windows.Forms.TreeNodeContextMenuStrip#1](~/samples/snippets/csharp/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.TreeNodeContextMenuStrip#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/system.windows.forms.TreeNodeContextMenuStrip/VB/Form1.vb#1)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ContextMenuStrip>
- [TreeView-Steuerelement](treeview-control-windows-forms.md)
