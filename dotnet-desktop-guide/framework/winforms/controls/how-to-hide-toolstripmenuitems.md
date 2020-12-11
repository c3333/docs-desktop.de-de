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
# <a name="how-to-hide-toolstripmenuitems"></a><span data-ttu-id="b4ad7-102">Vorgehensweise: Ausblenden von ToolStripMenuItems</span><span class="sxs-lookup"><span data-stu-id="b4ad7-102">How to: Hide ToolStripMenuItems</span></span>
<span data-ttu-id="b4ad7-103">Das Ausblenden von Menü Elementen ist eine Möglichkeit, die Benutzeroberfläche Ihrer Anwendung zu steuern und Benutzer Befehle einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-103">Hiding menu items is a way to control the user interface of your application and restrict user commands.</span></span> <span data-ttu-id="b4ad7-104">Häufig ist es ratsam, ein gesamtes Menü auszublenden, wenn alle Menü Elemente darin nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-104">Often, you will want to hide an entire menu when all of the menu items on it are unavailable.</span></span> <span data-ttu-id="b4ad7-105">Dies stellt weniger Ablenkungen für den Benutzer dar.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-105">This presents fewer distractions for the user.</span></span> <span data-ttu-id="b4ad7-106">Außerdem empfiehlt es sich, das Menü oder das Menü Element auszublenden und zu deaktivieren, da durch das Ausblenden allein nicht verhindert wird, dass der Benutzer über eine Tastenkombination auf einen Menübefehl zugreift.</span><span class="sxs-lookup"><span data-stu-id="b4ad7-106">Furthermore, you might want to both hide and disable the menu or menu item, as hiding alone does not prevent the user from accessing a menu command by using a shortcut key.</span></span>  
  
### <a name="to-hide-any-menu-item-programmatically"></a><span data-ttu-id="b4ad7-107">So blenden Sie ein beliebiges Menü Element Programm gesteuert aus</span><span class="sxs-lookup"><span data-stu-id="b4ad7-107">To hide any menu item programmatically</span></span>  
  
- <span data-ttu-id="b4ad7-108">Fügen Sie innerhalb der Methode, in der Sie die Eigenschaften des Menü Elements festgelegt haben, Code hinzu, um die- <xref:System.Windows.Forms.ToolStripItem.Visible%2A> Eigenschaft auf festzulegen `false` .</span><span class="sxs-lookup"><span data-stu-id="b4ad7-108">Within the method where you set the properties of the menu item, add code to set the <xref:System.Windows.Forms.ToolStripItem.Visible%2A> property to `false`.</span></span>  
  
    ```vb  
    MenuItem3.Visible = False  
    ```  
  
    ```csharp  
    menuItem3.Visible = false;  
    ```  
  
    ```cpp  
    menuItem3->Visible = false;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="b4ad7-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b4ad7-109">See also</span></span>

- <xref:System.Windows.Forms.ToolStripItem.Visible%2A>
- <xref:System.Windows.Forms.MenuStrip>
- [<span data-ttu-id="b4ad7-110">Übersicht über das MenuStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b4ad7-110">MenuStrip Control Overview</span></span>](menustrip-control-overview-windows-forms.md)
- [<span data-ttu-id="b4ad7-111">Vorgehensweise: Deaktivieren von ToolStripMenuItems</span><span class="sxs-lookup"><span data-stu-id="b4ad7-111">How to: Disable ToolStripMenuItems</span></span>](how-to-disable-toolstripmenuitems.md)
