---
title: 'Vorgehensweise: Deaktivieren von ToolStripMenuItems'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ToolStripMenuItems [Windows Forms], enabling
- ToolStripMenuItems [Windows Forms], disabling
- menu items [Windows Forms], disabling
- disabling menu items
- menu items [Windows Forms], enabling
- menus [Windows Forms], disabling menu items
ms.assetid: bcc1da84-50fd-41d2-8475-103b581d5654
ms.openlocfilehash: f86a2934e799e4604693491dacbecc517d44d810
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976308"
---
# <a name="how-to-disable-toolstripmenuitems"></a>Vorgehensweise: Deaktivieren von ToolStripMenuItems
Sie können die Befehle, die ein Benutzer durchführen kann, einschränken oder erweitern, indem Sie Menü Elemente als Reaktion auf Benutzeraktivitäten aktivieren und deaktivieren. Menü Elemente werden standardmäßig aktiviert, wenn Sie erstellt werden, aber dies kann über die- <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> Eigenschaft angepasst werden. Sie können diese Eigenschaft zur Entwurfszeit im **Eigenschaften** Fenster oder Programm gesteuert bearbeiten, indem Sie Sie im Code festlegen.  
  
### <a name="to-disable-a-menu-item-programmatically"></a>So deaktivieren Sie ein Menü Element Programm gesteuert  
  
- Fügen Sie innerhalb der Methode, in der Sie die Eigenschaften des Menü Elements festgelegt haben, Code hinzu, um die- <xref:System.Windows.Forms.ToolStripMenuItem.Enabled%2A> Eigenschaft auf festzulegen `false` .  
  
    ```vb  
    MenuItem1.Enabled = False  
    ```  
  
    ```csharp  
    menuItem1.Enabled = false;  
    ```  
  
    ```cpp  
    menuItem1->Enabled = false;  
    ```  
  
    > [!TIP]
    > Wenn Sie das erste Menü Element der obersten Ebene in einem Menü deaktivieren, werden alle im Menü enthaltenen Menü Elemente ausgeblendet, nicht jedoch deaktiviert. Ebenso werden bei der Deaktivierung eines Menü Elements, das unter Menü Elemente enthält, die unter Menü Elemente ausgeblendet, aber nicht deaktiviert. Wenn alle Befehle in einem bestimmten Menü für den Benutzer nicht verfügbar sind, wird als bewährte Programmier Übung empfohlen, das gesamte Menü auszublenden und zu deaktivieren, da dadurch eine saubere Benutzeroberfläche dargestellt wird. Sie sollten das Menü ausblenden und deaktivieren und jedes Element und unter Menü Element im Menü deaktivieren, da durch das Ausblenden allein der Zugriff auf einen Menübefehl über eine Tastenkombination nicht verhindert wird. Legen <xref:System.Windows.Forms.ToolStripItem.Visible%2A> Sie die-Eigenschaft eines Menü Elements der obersten Ebene auf fest, `false` um das gesamte Menü auszublenden.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [Vorgehensweise: Ausblenden von ToolStripMenuItems](how-to-hide-toolstripmenuitems.md)
- [Übersicht über das MenuStrip-Steuerelement](menustrip-control-overview-windows-forms.md)
