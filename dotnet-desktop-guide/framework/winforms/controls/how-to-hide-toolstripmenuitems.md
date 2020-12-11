---
title: 'Vorgehensweise: Ausblenden von ToolStripMenuItems'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ToolStripMenuItems [Windows Forms], hiding
- MenuStrip control [Windows Forms], hiding menu items
- menus [Windows Forms], hiding menu items
- menu items [Windows Forms], hiding
- hiding menu items
ms.assetid: 418a768f-808a-44cd-8cef-f4e161883621
ms.openlocfilehash: 64c0f093063357c1e8db5933c035cc8295ad4f1e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976293"
---
# <a name="how-to-hide-toolstripmenuitems"></a>Vorgehensweise: Ausblenden von ToolStripMenuItems
Das Ausblenden von Menü Elementen ist eine Möglichkeit, die Benutzeroberfläche Ihrer Anwendung zu steuern und Benutzer Befehle einzuschränken. Häufig ist es ratsam, ein gesamtes Menü auszublenden, wenn alle Menü Elemente darin nicht verfügbar sind. Dies stellt weniger Ablenkungen für den Benutzer dar. Außerdem empfiehlt es sich, das Menü oder das Menü Element auszublenden und zu deaktivieren, da durch das Ausblenden allein nicht verhindert wird, dass der Benutzer über eine Tastenkombination auf einen Menübefehl zugreift.  
  
### <a name="to-hide-any-menu-item-programmatically"></a>So blenden Sie ein beliebiges Menü Element Programm gesteuert aus  
  
- Fügen Sie innerhalb der Methode, in der Sie die Eigenschaften des Menü Elements festgelegt haben, Code hinzu, um die- <xref:System.Windows.Forms.ToolStripItem.Visible%2A> Eigenschaft auf festzulegen `false` .  
  
    ```vb  
    MenuItem3.Visible = False  
    ```  
  
    ```csharp  
    menuItem3.Visible = false;  
    ```  
  
    ```cpp  
    menuItem3->Visible = false;  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStripItem.Visible%2A>
- <xref:System.Windows.Forms.MenuStrip>
- [Übersicht über das MenuStrip-Steuerelement](menustrip-control-overview-windows-forms.md)
- [Vorgehensweise: Deaktivieren von ToolStripMenuItems](how-to-disable-toolstripmenuitems.md)
