---
title: Übersicht über die MainMenu-Komponente
ms.date: 03/30/2017
f1_keywords:
- MenuItem
- MainMenu
helpviewer_keywords:
- MainMenu control [Windows Forms], about MainMenu control
- menus
ms.assetid: b41cc5a3-cc59-4996-aa3c-8dd9c17d3c90
ms.openlocfilehash: 8bc35de239429214d6b493b343d1dd6c898f4d37
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975553"
---
# <a name="mainmenu-component-overview-windows-forms"></a>Übersicht über die MainMenu-Komponente (Windows Forms)
> [!IMPORTANT]
> Obwohl <xref:System.Windows.Forms.MenuStrip> und <xref:System.Windows.Forms.ContextMenuStrip> die <xref:System.Windows.Forms.MainMenu> -und-Steuerelemente früherer Versionen ersetzen und Funktionen hinzufügen <xref:System.Windows.Forms.ContextMenu> , <xref:System.Windows.Forms.MainMenu> <xref:System.Windows.Forms.ContextMenu> werden Sie sowohl für die Abwärtskompatibilität als auch für die zukünftige Verwendung beibehalten, wenn Sie auswählen.  
  
 Die Windows Forms <xref:System.Windows.Forms.MainMenu> Komponente zeigt ein Menü zur Laufzeit an. Alle Untermenüs des Hauptmenüs und der einzelnen Elemente sind <xref:System.Windows.Forms.MenuItem> Objekte.  
  
## <a name="key-properties"></a>Schlüsseleigenschaften  
 Ein Menü Element kann als Standardelement festgelegt werden, indem die-Eigenschaft auf festgelegt wird <xref:System.Windows.Forms.MenuItem.DefaultItem%2A> `true` . Das Standardelement wird in fettem Text angezeigt, wenn auf das Menü geklickt wird. Die-Eigenschaft des Menü Elements <xref:System.Windows.Forms.MenuItem.Checked%2A> ist entweder `true` oder `false` und gibt an, ob das Menü Element ausgewählt ist. Die-Eigenschaft des Menü Elements <xref:System.Windows.Forms.MenuItem.RadioCheck%2A> passt die Darstellung des ausgewählten Elements an: Wenn <xref:System.Windows.Forms.MenuItem.RadioCheck%2A> auf festgelegt ist `true` , wird neben dem Element ein Optionsfeld angezeigt <xref:System.Windows.Forms.MenuItem.RadioCheck%2A> . wenn auf festgelegt ist `false` , wird neben dem Element ein Häkchen angezeigt.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.MainMenu>
- <xref:System.Windows.Forms.Menu>
- <xref:System.Windows.Forms.MenuItem>
- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ContextMenuStrip>
- [Übersicht über das MenuStrip-Steuerelement](menustrip-control-overview-windows-forms.md)
