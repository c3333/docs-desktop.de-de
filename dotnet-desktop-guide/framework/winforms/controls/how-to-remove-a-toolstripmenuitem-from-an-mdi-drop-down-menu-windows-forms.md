---
title: 'Vorgehensweise: Entfernen eines ToolStripMenuItem aus einem MDI-Dropdownmenü'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- menu items [Windows Forms], removing from MDI drop-down menus
- MenuStrip control [Windows Forms], merging
- MenuStrip control [Windows Forms], removing
- MDI [Windows Forms], merging menu items
ms.assetid: bdafe60d-82ee-45bc-97fe-eeefca6e54c1
ms.openlocfilehash: 3198195cf0991734826508aa65818505bf2038c8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975607"
---
# <a name="how-to-remove-a-toolstripmenuitem-from-an-mdi-drop-down-menu-windows-forms"></a>Gewusst wie: Entfernen eines ToolStripMenuItem aus einem MDI-Dropdownmenü (Windows Forms)
In einigen Anwendungen kann sich die Art eines untergeordneten MDI-Fensters (Multiple-Document Interface) von der des übergeordneten MDI-Fensters unterscheiden. Beispielsweise könnte das übergeordnete MDI-Fenster eine Kalkulationstabelle und das untergeordnete MDI-Fenster ein Diagramm enthalten. In diesem Fall möchten Sie möglicherweise den Inhalt des Menüs des übergeordneten MDI-Fensters mit dem Inhalt des Menüs des untergeordneten MDI-Fensters aktualisieren, da untergeordnete MDI-Fenster unterschiedlicher Arten aktiviert werden.  
  
 Im folgenden Verfahren wird die <xref:System.Windows.Forms.Form.IsMdiContainer%2A> -Eigenschaft, die-Eigenschaft und die-Eigenschaft verwendet <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A> <xref:System.Windows.Forms.MergeAction> <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> , um ein Menü Element aus dem Dropdown Bereich des übergeordneten MDI-Menüs zu entfernen. Durch das Schließen des untergeordneten MDI-Fensters werden die entfernten Menü Elemente im übergeordneten MDI-Menü wieder hergestellt.  
  
### <a name="to-remove-a-menustrip-from-an-mdi-drop-down-menu"></a>So entfernen Sie ein MenuStrip aus einem MDI-Dropdown Menü  
  
1. Erstellen Sie ein Formular, und legen Sie dessen <xref:System.Windows.Forms.Form.IsMdiContainer%2A>-Eigenschaft auf `true` fest.  
  
2. Fügen Sie einen <xref:System.Windows.Forms.MenuStrip> zu `Form1` hinzu, und legen Sie die <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A>-Eigenschaft des <xref:System.Windows.Forms.MenuStrip> auf `true` fest  
  
3. Fügen Sie ein Menüelement der obersten Ebene zu `Form1`<xref:System.Windows.Forms.MenuStrip> hinzu, und legen Sie dessen <xref:System.Windows.Forms.Control.Text%2A>-Eigenschaft auf `&File` fest.  
  
4. Fügen Sie dem Menü Element drei unter Menü Elemente hinzu `&File` , und legen Sie deren <xref:System.Windows.Forms.ToolStripItem.Text%2A> Eigenschaften auf `&Open` , `&Import from` und fest `E&xit` .  
  
5. Fügen Sie dem unter Menü Element zwei unter Menü Elemente hinzu, `&Import from` und legen Sie deren <xref:System.Windows.Forms.ToolStripItem.Text%2A> Eigenschaften auf `&Word` und fest `&Excel` .  
  
6. Fügen Sie dem Projekt ein Formular hinzu, fügen Sie dem Formular ein <xref:System.Windows.Forms.MenuStrip> hinzu, und legen die <xref:System.Windows.Forms.ToolStrip.AllowMerge%2A>-Eigenschaft von `Form2`<xref:System.Windows.Forms.MenuStrip> auf `true` fest.  
  
7. Fügen Sie ein Menüelement der obersten Ebene zu `Form2`<xref:System.Windows.Forms.MenuStrip> hinzu, und legen Sie dessen <xref:System.Windows.Forms.ToolStripItem.Text%2A>-Eigenschaft auf `&File` fest.  
  
8. Fügen Sie `&Import from` dem Menü von ein unter Menü Element hinzu `&File` `Form2` , und fügen Sie `&Word` dem Menü ein unter Menü Element hinzu `&File` .  
  
9. Legen Sie die <xref:System.Windows.Forms.MergeAction> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.ToolStripItem.MergeIndex%2A> der Menü Elemente fest, `Form2` wie in der folgenden Tabelle gezeigt.  
  
    |Form2 (Menü Element)|MergeAction-Wert|Mergeingedex-Wert|  
    |---------------------|-----------------------|----------------------|  
    |Datei|Nur MatchOnly|-1|  
    |Importieren aus|Nur MatchOnly|-1|  
    |Word|Remove (Entfernen)|-1|  
  
10. Erstellen Sie in `Form1` einen Ereignishandler für das- <xref:System.Windows.Forms.Control.Click> Ereignis von `&Open` <xref:System.Windows.Forms.ToolStripMenuItem> .  
  
11. Fügen Sie im-Ereignishandler Code hinzu, der dem folgenden Codebeispiel ähnelt, um neue Instanzen von als untergeordnete MDI-Elemente von zu erstellen und anzuzeigen `Form2` `Form1` :  
  
    ```vb  
    Private Sub openToolStripMenuItem_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles openToolStripMenuItem.Click  
        Dim NewMDIChild As New Form2()  
        'Set the parent form of the child window.  
            NewMDIChild.MdiParent = Me  
        'Display the new form.  
            NewMDIChild.Show()  
    End Sub  
    ```  
  
    ```csharp  
    private void openToolStripMenuItem_Click(object sender, EventArgs e)  
    {  
        Form2 newMDIChild = new Form2();  
        // Set the parent form of the child window.  
            newMDIChild.MdiParent = this;  
        // Display the new form.  
            newMDIChild.Show();  
    }  
    ```  
  
12. Fügen Sie Code, der dem folgenden Codebeispiel ähnelt, in `&Open`<xref:System.Windows.Forms.ToolStripMenuItem> ein, um den Ereignishandler zu registrieren.  
  
    ```vb  
    Private Sub openToolStripMenuItem_Click(sender As Object, e As _  
    EventArgs) Handles openToolStripMenuItem.Click  
    ```  
  
    ```csharp  
    this.openToolStripMenuItem.Click += new _  
    System.EventHandler(this.openToolStripMenuItem_Click);  
    ```  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Zwei <xref:System.Windows.Forms.Form>-Steuerelemente namens `Form1` und `Form2`.  
  
- Ein <xref:System.Windows.Forms.MenuStrip>-Steuerelement auf `Form1`, das den Namen `menuStrip1` hat, und ein <xref:System.Windows.Forms.MenuStrip>-Steuerelement auf `Form2`, das den Namen `menuStrip2` hat.  
  
- Verweise auf die Assemblys <xref:System?displayProperty=nameWithType> und <xref:System.Windows.Forms?displayProperty=nameWithType>.  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Erstellen von übergeordneten MDI-Formularen](../advanced/how-to-create-mdi-parent-forms.md)
- [Vorgehensweise: Erstellen von untergeordneten MDI-Formularen](../advanced/how-to-create-mdi-child-forms.md)
- [Übersicht über das MenuStrip-Steuerelement](menustrip-control-overview-windows-forms.md)
