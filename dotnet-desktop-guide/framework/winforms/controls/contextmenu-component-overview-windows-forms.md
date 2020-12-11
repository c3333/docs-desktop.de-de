---
title: Übersicht über die ContextMenu-Komponente
ms.date: 03/30/2017
f1_keywords:
- ContextMenu
helpviewer_keywords:
- ContextMenu component [Windows Forms], about ContextMenu component
- context menus [Windows Forms], ContextMenu component
- shortcut menus [Windows Forms], ContextMenu component
ms.assetid: 49d6398f-d3c4-4679-84fa-1de07b68b05e
ms.openlocfilehash: 83740221894941d09d1014585513043851a518e5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972234"
---
# <a name="contextmenu-component-overview-windows-forms"></a>Übersicht über die ContextMenu-Komponente (Windows Forms)
> [!IMPORTANT]
> Obwohl <xref:System.Windows.Forms.MenuStrip> und <xref:System.Windows.Forms.ContextMenuStrip> die <xref:System.Windows.Forms.MainMenu> -und-Steuerelemente früherer Versionen ersetzen und Funktionen hinzufügen <xref:System.Windows.Forms.ContextMenu> , <xref:System.Windows.Forms.MainMenu> <xref:System.Windows.Forms.ContextMenu> werden Sie sowohl für die Abwärtskompatibilität als auch für die zukünftige Verwendung beibehalten, wenn Sie auswählen.  
  
 Mit der Windows Forms- <xref:System.Windows.Forms.ContextMenu> Komponente können Sie Benutzern ein leicht zugängliches Kontextmenü mit häufig verwendeten Befehlen bereitstellen, die dem ausgewählten Objekt zugeordnet sind. Die Elemente in einem Kontextmenü sind häufig eine Teilmenge der Elemente aus den Hauptmenüs, die an anderer Stelle in der Anwendung angezeigt werden. Benutzer können in der Regel auf ein Kontextmenü zugreifen, indem Sie mit der rechten Maustaste auf die Maus klicken. Auf Windows Forms werden Kontextmenüs Steuerelementen zugeordnet.  
  
## <a name="key-properties"></a>Schlüsseleigenschaften  
 Sie können ein Kontextmenü einem-Steuerelement zuordnen, indem Sie die-Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.ContextMenu%2A> auf die- <xref:System.Windows.Forms.ContextMenu> Komponente festlegen. Einem einzelnen Kontextmenü können mehrere Steuerelemente zugeordnet werden, aber jedes Steuerelement kann nur über ein Kontextmenü verfügen.  
  
 Die Schlüsseleigenschaft der <xref:System.Windows.Forms.ContextMenu> Komponente ist die- <xref:System.Windows.Forms.Menu.MenuItems%2A> Eigenschaft. Sie können Menü Elemente hinzufügen, indem Sie Objekte Programm gesteuert erstellen <xref:System.Windows.Forms.MenuItem> und Sie dem Kontextmenü hinzufügen <xref:System.Windows.Forms.Menu.MenuItemCollection> . Da die Elemente in einem Kontextmenü in der Regel aus anderen Menüs gezeichnet werden, fügen Sie Elemente häufig zu einem Kontextmenü hinzu, indem Sie Sie kopieren.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ContextMenu>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ContextMenuStrip>
