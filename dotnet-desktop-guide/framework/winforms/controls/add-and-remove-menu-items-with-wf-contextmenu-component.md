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
# <a name="how-to-add-and-remove-menu-items-with-the-windows-forms-contextmenu-component"></a>Vorgehensweise: Hinzufügen und Entfernen von Menüelementen mit der ContextMenu-Komponente von Windows Forms
Erläutert das Hinzufügen und Entfernen von Kontextmenü Elementen in Windows Forms.  
  
 Die Windows Forms <xref:System.Windows.Forms.ContextMenu> Komponente enthält ein Menü mit häufig verwendeten Befehlen, die für das ausgewählte Objekt relevant sind. Sie können dem Kontextmenü Elemente hinzufügen, indem Sie der Auflistung Objekte hinzufügen <xref:System.Windows.Forms.MenuItem> <xref:System.Windows.Forms.Menu.MenuItems%2A> .  
  
 Elemente aus einem Kontextmenü können dauerhaft entfernt werden. zur Laufzeit ist es jedoch möglicherweise besser, die Elemente auszublenden oder zu deaktivieren.  
  
> [!IMPORTANT]
> Obwohl <xref:System.Windows.Forms.MenuStrip> und <xref:System.Windows.Forms.ContextMenuStrip> die <xref:System.Windows.Forms.MainMenu> -und-Steuerelemente früherer Versionen ersetzen und Funktionen hinzufügen <xref:System.Windows.Forms.ContextMenu> , <xref:System.Windows.Forms.MainMenu> <xref:System.Windows.Forms.ContextMenu> werden Sie sowohl für die Abwärtskompatibilität als auch für die zukünftige Verwendung beibehalten, wenn Sie auswählen.  
  
### <a name="to-remove-items-from-a-shortcut-menu"></a>So entfernen Sie Elemente aus einem Kontextmenü  
  
1. Verwenden Sie die-Methode oder die-Methode der-Auflistung der- <xref:System.Windows.Forms.Menu.MenuItemCollection.Remove%2A> <xref:System.Windows.Forms.Menu.MenuItemCollection.RemoveAt%2A> <xref:System.Windows.Forms.Menu.MenuItems%2A> <xref:System.Windows.Forms.ContextMenu> Komponente, um ein bestimmtes Menü Element zu entfernen.  
  
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
  
     Oder  
  
2. Verwenden Sie die-Methode der-Auflistung der- `Clear` `MenuItems` <xref:System.Windows.Forms.ContextMenu> Komponente, um alle Elemente aus dem Menü zu entfernen.  
  
    ```vb  
    ContextMenu1.MenuItems.Clear()  
    ```  
  
    ```csharp  
    contextMenu1.MenuItems.Clear();  
    ```  
  
    ```cpp  
    contextMenu1->MenuItems->Clear();  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ContextMenu>
- [ContextMenu-Komponente](contextmenu-component-windows-forms.md)
- [Übersicht über die ContextMenu-Komponente](contextmenu-component-overview-windows-forms.md)
