---
title: Hinzufügen und Entfernen von Menü Elementen mit der ContextMenu-Komponente
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- context menus [Windows Forms], removing items
- ContextMenu component [Windows Forms], adding items
- shortcut menus [Windows Forms], removing items
- shortcut menus [Windows Forms], examples
- context menus [Windows Forms], adding items
- shortcut menus [Windows Forms], adding items
- ContextMenu component [Windows Forms], removing items
- context menus [Windows Forms], examples
- examples [Windows Forms], context menus
ms.assetid: 426d1eaf-7fb8-4b0b-8a33-5e8721786ea4
ms.openlocfilehash: 989ab6d47ec761930a32f542b5fa1136e831f73d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975802"
---
# <a name="how-to-add-and-remove-menu-items-with-the-windows-forms-contextmenu-component"></a><span data-ttu-id="2cd88-102">Vorgehensweise: Hinzufügen und Entfernen von Menüelementen mit der ContextMenu-Komponente von Windows Forms</span><span class="sxs-lookup"><span data-stu-id="2cd88-102">How to: Add and Remove Menu Items with the Windows Forms ContextMenu Component</span></span>
<span data-ttu-id="2cd88-103">Erläutert das Hinzufügen und Entfernen von Kontextmenü Elementen in Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="2cd88-103">Explains how to add and remove shortcut menu items in Windows Forms.</span></span>  
  
 <span data-ttu-id="2cd88-104">Die Windows Forms <xref:System.Windows.Forms.ContextMenu> Komponente enthält ein Menü mit häufig verwendeten Befehlen, die für das ausgewählte Objekt relevant sind.</span><span class="sxs-lookup"><span data-stu-id="2cd88-104">The Windows Forms <xref:System.Windows.Forms.ContextMenu> component provides a menu of frequently used commands that are relevant to the selected object.</span></span> <span data-ttu-id="2cd88-105">Sie können dem Kontextmenü Elemente hinzufügen, indem Sie der Auflistung Objekte hinzufügen <xref:System.Windows.Forms.MenuItem> <xref:System.Windows.Forms.Menu.MenuItems%2A> .</span><span class="sxs-lookup"><span data-stu-id="2cd88-105">You can add items to the shortcut menu by adding <xref:System.Windows.Forms.MenuItem> objects to the <xref:System.Windows.Forms.Menu.MenuItems%2A> collection.</span></span>  
  
 <span data-ttu-id="2cd88-106">Elemente aus einem Kontextmenü können dauerhaft entfernt werden. zur Laufzeit ist es jedoch möglicherweise besser, die Elemente auszublenden oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="2cd88-106">You can remove items from a shortcut menu permanently; however, at run time it may be more appropriate to hide or disable the items instead.</span></span>  
  
> [!IMPORTANT]
> <span data-ttu-id="2cd88-107">Obwohl <xref:System.Windows.Forms.MenuStrip> und <xref:System.Windows.Forms.ContextMenuStrip> die <xref:System.Windows.Forms.MainMenu> -und-Steuerelemente früherer Versionen ersetzen und Funktionen hinzufügen <xref:System.Windows.Forms.ContextMenu> , <xref:System.Windows.Forms.MainMenu> <xref:System.Windows.Forms.ContextMenu> werden Sie sowohl für die Abwärtskompatibilität als auch für die zukünftige Verwendung beibehalten, wenn Sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="2cd88-107">Although <xref:System.Windows.Forms.MenuStrip> and <xref:System.Windows.Forms.ContextMenuStrip> replace and add functionality to the <xref:System.Windows.Forms.MainMenu> and <xref:System.Windows.Forms.ContextMenu> controls of previous versions, <xref:System.Windows.Forms.MainMenu> and <xref:System.Windows.Forms.ContextMenu> are retained for both backward compatibility and future use if you choose.</span></span>  
  
### <a name="to-remove-items-from-a-shortcut-menu"></a><span data-ttu-id="2cd88-108">So entfernen Sie Elemente aus einem Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="2cd88-108">To remove items from a shortcut menu</span></span>  
  
1. <span data-ttu-id="2cd88-109">Verwenden Sie die-Methode oder die-Methode der-Auflistung der- <xref:System.Windows.Forms.Menu.MenuItemCollection.Remove%2A> <xref:System.Windows.Forms.Menu.MenuItemCollection.RemoveAt%2A> <xref:System.Windows.Forms.Menu.MenuItems%2A> <xref:System.Windows.Forms.ContextMenu> Komponente, um ein bestimmtes Menü Element zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="2cd88-109">Use the <xref:System.Windows.Forms.Menu.MenuItemCollection.Remove%2A> or <xref:System.Windows.Forms.Menu.MenuItemCollection.RemoveAt%2A> method of the <xref:System.Windows.Forms.Menu.MenuItems%2A> collection of the <xref:System.Windows.Forms.ContextMenu> component to remove a particular menu item.</span></span>  
  
    ```vb  
    ' Removes the first item in the shortcut menu.  
    ContextMenu1.MenuItems.RemoveAt(0)  
    ' Removes a particular object from the shortcut menu.  
    ContextMenu1.MenuItems.Remove(mnuItemNew)  
    ```  
  
    ```csharp  
    // Removes the first item in the shortcut menu.  
    contextMenu1.MenuItems.RemoveAt(0);  
    // Removes a particular object from the shortcut menu.  
    contextMenu1.MenuItems.Remove(mnuItemNew);  
    ```  
  
    ```cpp  
    // Removes the first item in the shortcut menu.  
    contextMenu1->MenuItems->RemoveAt(0);  
    // Removes a particular object from the shortcut menu.  
    contextMenu1->MenuItems->Remove(mnuItemNew);  
    ```  
  
     <span data-ttu-id="2cd88-110">Oder</span><span class="sxs-lookup"><span data-stu-id="2cd88-110">-or-</span></span>  
  
2. <span data-ttu-id="2cd88-111">Verwenden Sie die-Methode der-Auflistung der- `Clear` `MenuItems` <xref:System.Windows.Forms.ContextMenu> Komponente, um alle Elemente aus dem Menü zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="2cd88-111">Use the `Clear` method of the `MenuItems` collection of the <xref:System.Windows.Forms.ContextMenu> component to remove all items from the menu.</span></span>  
  
    ```vb  
    ContextMenu1.MenuItems.Clear()  
    ```  
  
    ```csharp  
    contextMenu1.MenuItems.Clear();  
    ```  
  
    ```cpp  
    contextMenu1->MenuItems->Clear();  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="2cd88-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cd88-112">See also</span></span>

- <xref:System.Windows.Forms.ContextMenu>
- [<span data-ttu-id="2cd88-113">ContextMenu-Komponente</span><span class="sxs-lookup"><span data-stu-id="2cd88-113">ContextMenu Component</span></span>](contextmenu-component-windows-forms.md)
- [<span data-ttu-id="2cd88-114">Übersicht über die ContextMenu-Komponente</span><span class="sxs-lookup"><span data-stu-id="2cd88-114">ContextMenu Component Overview</span></span>](contextmenu-component-overview-windows-forms.md)
