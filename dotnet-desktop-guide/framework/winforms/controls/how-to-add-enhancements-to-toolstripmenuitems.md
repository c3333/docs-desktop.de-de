---
title: 'Vorgehensweise: Hinzufügen von Erweiterungen zu ToolStripMenuItems'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- commands [Windows Forms], grouping on menus
- check marks [Windows Forms], adding to menus
- ToolStripMenuItems [Windows Forms], displaying access keys
- menus [Windows Forms], grouping commands
- menu items [Windows Forms], displaying shortcut keys
- ToolStripMenuItems
- separators [Windows Forms], displaying on menus
- menu items [Windows Forms], showing separators
- menu items [Windows Forms], adding check marks
- ToolStripMenuItems [Windows Forms], adding check marks
- menu items [Windows Forms], adding images
- ToolStripSeparators [Windows Forms], displaying on MenuStrips
- menu items [Windows Forms], displaying access keys
- ToolStripMenuItems [Windows Forms], displaying shortcut keys
- ToolStripMenuItems [Windows Forms], adding images
- keyboard shortcuts [Windows Forms], displaying on menus
- images [Windows Forms], adding to menus
- ToolStripMenuItems [Windows Forms], showing separator bars
ms.assetid: aa5f19bb-b545-4378-bfa6-36ba592f0d7c
ms.openlocfilehash: 61a79b9bbe101d7bf694240bdffdecee5187adf2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976374"
---
# <a name="how-to-add-enhancements-to-toolstripmenuitems"></a>Vorgehensweise: Hinzufügen von Erweiterungen zu ToolStripMenuItems
Es gibt folgende Möglichkeiten, um die Verwendbarkeit von <xref:System.Windows.Forms.MenuStrip> -und-Steuerelementen zu verbessern <xref:System.Windows.Forms.ContextMenuStrip> :  
  
- Fügen Sie Kontrollzeichen hinzu, um anzugeben, ob eine Funktion aktiviert oder deaktiviert ist, z. b. ob ein Lineal am Rand einer Textverarbeitungsanwendung angezeigt wird, oder um anzugeben, welche Datei in einer Liste von Dateien angezeigt wird, z. b. in einem **Fenster** Menü.  
  
- Fügen Sie Bilder hinzu, die Menübefehle visuell darstellen.  
  
- Zeigen Sie Tastenkombinationen an, um eine Tastatur Alternative zur Maus zum Ausführen von Befehlen bereitzustellen. Wenn Sie z. b. STRG + C drücken, wird der Befehl **Kopieren** durchführt.  
  
- Zeigen Sie Zugriffstasten an, um eine Tastatur Alternative zur Maus zur Menü Navigation bereitzustellen. Wenn Sie z. b. ALT + F drücken, wird das Menü **Datei** ausgewählt.  
  
- Trennlinien zum Gruppieren verwandter Befehle anzeigen und Menüs besser lesbar machen.  
  
### <a name="to-display-a-check-mark-on-a-menu-command"></a>So zeigen Sie ein Häkchen in einem Menübefehl an  
  
- Legen Sie die- <xref:System.Windows.Forms.ToolStripMenuItem.Checked%2A> Eigenschaft auf fest `true` .  
  
     Dadurch wird auch die- <xref:System.Windows.Forms.ToolStripMenuItem.CheckState%2A> Eigenschaft auf festgelegt `true` . Verwenden Sie dieses Verfahren nur, wenn der Menübefehl standardmäßig als aktiviert angezeigt werden soll, unabhängig davon, ob er ausgewählt ist.  
  
### <a name="to-display-a-check-mark-that-changes-state-with-each-click"></a>So zeigen Sie ein Häkchen an, das den Zustand bei jedem Klick ändert  
  
- Legen Sie die-Eigenschaft des Menübefehls <xref:System.Windows.Forms.ToolStripMenuItem.CheckOnClick%2A> auf fest `true` .  
  
### <a name="to-add-an-image-to-a-menu-command"></a>So fügen Sie einem Menübefehl ein Bild hinzu  
  
- Legen Sie die-Eigenschaft des Menübefehls <xref:System.Windows.Forms.ToolStripItem.Image%2A> auf den Namen des Bilds fest. Wenn die- <xref:System.Windows.Forms.ToolStripItemDisplayStyle> Eigenschaft dieses Menübefehls auf oder festgelegt ist <xref:System.Windows.Forms.ToolStripItemDisplayStyle.Text> <xref:System.Windows.Forms.ToolStripItemDisplayStyle.None> , kann das Bild nicht angezeigt werden.  
  
> [!NOTE]
> Der Bildrand kann auch ein Häkchen anzeigen, wenn Sie diese Option auswählen. Außerdem können Sie die <xref:System.Windows.Forms.ToolStripMenuItem.Checked%2A> -Eigenschaft des Bilds auf festlegen `true` , und das Bild wird zur Laufzeit mit einem ausgebrüpften Rahmen herum angezeigt.  
  
### <a name="to-display-a-shortcut-key-for-a-menu-command"></a>So zeigen Sie eine Tastenkombination für einen Menübefehl an  
  
- Legen Sie die-Eigenschaft des Menübefehls <xref:System.Windows.Forms.ToolStripMenuItem.ShortcutKeys%2A> auf die gewünschte Tastaturkombination fest, z. b. STRG + O für den Menübefehl **Öffnen** , und legen Sie die- <xref:System.Windows.Forms.ToolStripMenuItem.ShowShortcutKeys%2A> Eigenschaft auf fest `true` .  
  
### <a name="to-display-custom-shortcut-keys-for-a-menu-command"></a>So zeigen Sie benutzerdefinierte Tastenkombinationen für einen Menübefehl an  
  
- Legen Sie die-Eigenschaft des Menübefehls <xref:System.Windows.Forms.ToolStripMenuItem.ShortcutKeyDisplayString%2A> auf die gewünschte Tastaturkombination fest, z. b. STRG + UMSCHALT + o anstelle von Umschalt + Strg + o, und legen Sie die- <xref:System.Windows.Forms.ToolStripMenuItem.ShowShortcutKeys%2A> Eigenschaft auf fest `true` .  
  
### <a name="to-display-an-access-key-for-a-menu-command"></a>So zeigen Sie eine Zugriffstaste für einen Menübefehl an  
  
- Wenn Sie die <xref:System.Windows.Forms.ToolStripItem.Text%2A> -Eigenschaft für den Menübefehl festgelegt haben, geben Sie vor dem Buchstaben, den Sie als Zugriffsschlüssel unterstrichen möchten, ein kaufmännisches und-Objekt (&) ein. Wenn Sie z `&Open` <xref:System.Windows.Forms.ToolStripItem.Text%2A> . b. als Eigenschaft eines Menü Elements eingeben, führt dies zu einem Menübefehl, der als <u>O</u>Pen angezeigt wird.
  
     Zum Navigieren zu diesem Menübefehl drücken Sie alt, um den Fokus auf zu setzen <xref:System.Windows.Forms.MenuStrip> , und drücken Sie die Zugriffstaste des Menü namens. Wenn das Menü geöffnet wird und Elemente mit Zugriffs Schlüsseln angezeigt werden, müssen Sie nur die Zugriffstaste drücken, um den Menübefehl auszuwählen.  
  
> [!NOTE]
> Vermeiden Sie das definieren doppelter Zugriffsschlüssel, z. b. das doppelte definieren von Alt + F im gleichen Menüsystem. Die Auswahl Reihenfolge doppelter Zugriffsschlüssel kann nicht garantiert werden.  
  
### <a name="to-display-a-separator-bar-between-menu-commands"></a>So zeigen Sie eine Trennlinie zwischen Menübefehlen an  
  
- Nachdem Sie das <xref:System.Windows.Forms.MenuStrip> und die darin enthaltenen Elemente definiert haben, verwenden Sie die- <xref:System.Windows.Forms.ToolStripItemCollection.AddRange%2A> Methode oder die-Methode, um die <xref:System.Windows.Forms.ToolStripItemCollection.Add%2A> Menübefehle und-Steuer <xref:System.Windows.Forms.ToolStripSeparator> Elemente <xref:System.Windows.Forms.MenuStrip> in der gewünschten Reihenfolge hinzuzufügen.  
  
    ```vb  
    ' This code adds a top-level File menu to the MenuStrip.  
    Me.menuStrip1.Items.Add(New ToolStripMenuItem() _  
    {Me.fileToolStripMenuItem})  
  
    ' This code adds the New and Open menu commands, a separator bar,
    ' and the Save and Exit menu commands to the top-level File menu,
    ' in that order.  
    Me.fileToolStripMenuItem.DropDownItems.AddRange(New _  
    ToolStripMenuItem() {Me.newToolStripMenuItem, _  
    Me.openToolStripMenuItem, Me.toolStripSeparator1, _  
    Me.saveToolStripMenuItem, Me.exitToolStripMenuItem})  
    ```  
  
    ```csharp  
    // This code adds a top-level File menu to the MenuStrip.  
    this.menuStrip1.Items.Add(new ToolStripItem[]_  
    {this.fileToolStripMenuItem});  
  
    // This code adds the New and Open menu commands, a separator bar,
    // and the Save and Exit menu commands to the top-level File menu,
    // in that order.  
    this.fileToolStripMenuItem.DropDownItems.AddRange(new _  
    ToolStripItem[] {  
    this.newToolStripMenuItem,  
    this.openToolStripMenuItem,  
    this.toolStripSeparator1,  
    this.saveToolStripMenuItem,  
    this.exitToolStripMenuItem});  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [Übersicht über das MenuStrip-Steuerelement](menustrip-control-overview-windows-forms.md)
