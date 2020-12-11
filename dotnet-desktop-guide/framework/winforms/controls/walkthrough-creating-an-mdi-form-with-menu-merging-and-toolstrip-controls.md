---
title: 'Exemplarische Vorgehensweise: Erstellen eines MDI-Formulars mit der Zusammenführungsfunktion für Menüs und ToolStrip-Steuerelemente'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStripPanel control [Windows Forms]
- MDI [Windows Forms], creating forms
- multiple document interface forms
- MDI forms
- ToolStrip control [Windows Forms]
- MDI forms [Windows Forms], creating
- MDI forms [Windows Forms], walkthroughs
ms.assetid: fbab4221-74af-42d0-bbf4-3c97f7b2e544
ms.openlocfilehash: d71534bed0af142ff71ba9a0c01207b2c72a6d6a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976962"
---
# <a name="walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls"></a>Exemplarische Vorgehensweise: Erstellen eines MDI-Formulars mit der Zusammenführungsfunktion für Menüs und ToolStrip-Steuerelemente

Der <xref:System.Windows.Forms?displayProperty=nameWithType>-Namespace unterstützt MDI-Anwendungen (Multiple Document Interface, Schnittstelle für mehrere Dokumente), und das <xref:System.Windows.Forms.MenuStrip>-Steuerelement unterstützt das Zusammenführen von Menüs. MDI-Formulare können auch <xref:System.Windows.Forms.ToolStrip>-Steuerelemente enthalten.

Diese exemplarische Vorgehensweise veranschaulicht, wie Steuer <xref:System.Windows.Forms.ToolStripPanel> Elemente mit einem MDI-Formular verwendet werden. Das Formular unterstützt auch Zusammenführen von Menüs mit untergeordneten Menüs. In dieser exemplarischen Vorgehensweise werden die folgenden Aufgaben veranschaulicht:

- Erstellen eines Windows Forms Projekts

- Erstellen des Hauptmenüs für das Formular. Der tatsächliche Name des Menüs ist unterschiedlich.

- Hinzufügen des <xref:System.Windows.Forms.ToolStripPanel> Steuer Elements zur **Toolbox**.

- Erstellen eines untergeordneten Formulars.

- Anordnen <xref:System.Windows.Forms.ToolStripPanel> von Steuerelementen nach z-Reihenfolge.

Wenn Sie fertig sind, verfügen Sie über ein MDI-Formular, das Zusammenführen von Menüs und verschiebbaren Steuerelementen unterstützt <xref:System.Windows.Forms.ToolStrip> .

Informationen zum Kopieren des Codes in diesem Thema als einzelne Auflistung finden Sie unter Gewusst [wie: Erstellen eines MDI-Formulars mit der Zusammenführung von Menüs und ToolStrip-Steuerelementen](how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).

## <a name="prerequisites"></a>Voraussetzungen

Sie benötigen Visual Studio, um diese exemplarische Vorgehensweise abzuschließen.

## <a name="create-the-project"></a>Erstellen des Projekts

1. Erstellen Sie in Visual Studio ein Windows-Anwendungsprojekt mit dem Namen **MDIForm** (**File**  >  **New**  >  **Project**  >  **Visual c#** oder **Visual Basic**  >  **Classic Desktop**  >  **Windows Forms Application**).

2. Wählen Sie im Windows Forms-Designer das Formular aus.

3. Legen Sie in der Eigenschaftenfenster den Wert von <xref:System.Windows.Forms.Form.IsMdiContainer%2A> auf fest `true` .

## <a name="create-the-main-menu"></a>Erstellen des Hauptmenü

Das übergeordnete MDI-Formular enthält das Hauptmenü. Das Hauptmenü hat ein Menü Element mit dem Namen **Fenster**. Mit dem Menü Element **Fenster** können Sie untergeordnete Formulare erstellen. Menü Elemente aus untergeordneten Formularen werden im Hauptmenü zusammengeführt.

1. Ziehen Sie ein-Steuerelement aus der **Toolbox** <xref:System.Windows.Forms.MenuStrip> auf das Formular.

2. Fügen Sie <xref:System.Windows.Forms.ToolStripMenuItem> dem Steuerelement ein hinzu, <xref:System.Windows.Forms.MenuStrip> und nennen Sie es **Window**.

3. Wählen Sie das <xref:System.Windows.Forms.MenuStrip>-Steuerelement.

4. Legen Sie in der Eigenschaftenfenster den Wert der- <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> Eigenschaft auf fest `ToolStripMenuItem1` .

5. Fügen Sie dem **Fenster** Menü Element ein Unterelement hinzu, und benennen Sie das Unterelement **neu**.

6. Klicken Sie im Fenster Eigenschaften auf **Ereignisse**.

7. Doppelklicken Sie auf das <xref:System.Windows.Forms.ToolStripItem.Click> Ereignis.

     Der Windows Forms-Designer generiert einen Ereignishandler für das- <xref:System.Windows.Forms.ToolStripItem.Click> Ereignis.

8. Fügen Sie den folgenden Code in den-Ereignishandler ein.

     [!code-csharp[System.Windows.Forms.ToolStrip.MdiForm#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.ToolStrip.MdiForm#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/VB/Form1.vb#2)]

## <a name="add-the-toolstrippanel-control-to-the-toolbox"></a>Fügen Sie das ToolStripPanel-Steuerelement der Toolbox hinzu.

Wenn Sie <xref:System.Windows.Forms.MenuStrip> Steuerelemente mit einem MDI-Formular verwenden, müssen Sie über das-Steuerelement verfügen <xref:System.Windows.Forms.ToolStripPanel> . Sie müssen das- <xref:System.Windows.Forms.ToolStripPanel> Steuerelement der **Toolbox** hinzufügen, um das MDI-Formular im Windows Forms-Designer zu erstellen.

1. Öffnen Sie die **Toolbox**, und klicken Sie dann auf die Registerkarte **alle Windows Forms** , um die verfügbaren Windows Forms Steuerelemente anzuzeigen.

2. Klicken Sie mit der rechten Maustaste, um das Kontextmenü zu öffnen, und wählen Sie **Elemente auswählen**.

3. Führen Sie im Dialogfeld **Toolbox Elemente auswählen** einen **Bildlauf** nach unten in der Spalte Name aus, bis Sie **ToolStripPanel** gefunden haben.

4. Aktivieren Sie das Kontrollkästchen von **ToolStripPanel**, und klicken Sie dann auf **OK**.

     Das-Steuerelement wird <xref:System.Windows.Forms.ToolStripPanel> in der **Toolbox** angezeigt.

## <a name="create-a-child-form"></a>Erstellen eines untergeordneten Formulars

In diesem Verfahren definieren Sie eine separate untergeordnete Formular Klasse, die über ein eigenes <xref:System.Windows.Forms.MenuStrip> Steuerelement verfügt. Die Menü Elemente für dieses Formular werden mit denen des übergeordneten Formulars zusammengeführt.

1. Fügen Sie dem Projekt ein neues Formular `ChildForm` mit dem Namen hinzu.

     Weitere Informationen finden Sie unter Gewusst [wie: Hinzufügen von Windows Forms zu einem Projekt](/previous-versions/visualstudio/visual-studio-2010/y2xxdce3(v=vs.100)).

2. Ziehen Sie aus der **Toolbox** ein- <xref:System.Windows.Forms.MenuStrip> Steuerelement auf das untergeordnete Formular.

3. Klicken Sie auf das <xref:System.Windows.Forms.MenuStrip> Designer-Aktions Symbol des Steuer Elements ( ![ kleiner schwarzer Pfeil ](./media/designer-actions-glyph.gif) ), und wählen Sie dann **Elemente bearbeiten** aus.

4. Fügen Sie im Dialogfeld Elementauflistungs- **Editor** dem untergeordneten Menü ein neues <xref:System.Windows.Forms.ToolStripMenuItem> benanntes **ChildMenuItem-Element** hinzu.

     Weitere Informationen finden Sie unter [ToolStrip Items](/previous-versions/visualstudio/visual-studio-2010/ms233643(v=vs.100))-Auflistungs-Editor.

## <a name="test-the-form"></a>Testen des Formulars

1. Drücken Sie **F5** , um das Formular zu kompilieren und auszuführen.

2. Klicken Sie auf das Menü Element **Fenster** , um das Menü zu öffnen, und klicken Sie dann auf **neu**.

     Im MDI-Client Bereich des Formulars wird ein neues untergeordnetes Formular erstellt. Das Menü des untergeordneten Formulars wird mit dem Hauptmenü zusammengeführt.

3. Schließen Sie das untergeordnete Formular.

     Das Menü des untergeordneten Formulars wird aus dem Hauptmenü entfernt.

4. Klicken Sie mehrmals auf **neu** .

     Die untergeordneten Formulare werden automatisch unter dem Menü Element **Fenster** aufgeführt, da die <xref:System.Windows.Forms.MenuStrip> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> zugewiesen wird.

## <a name="add-toolstrip-support"></a>ToolStrip-Unterstützung hinzufügen

In diesem Verfahren fügen Sie <xref:System.Windows.Forms.ToolStrip> dem übergeordneten MDI-Formular vier Steuerelemente hinzu. Jedes <xref:System.Windows.Forms.ToolStrip> Steuerelement wird in einem-Steuerelement hinzugefügt <xref:System.Windows.Forms.ToolStripPanel> , das an den Rand des Formulars angedockt wird.

1. Ziehen Sie ein-Steuerelement aus der **Toolbox** <xref:System.Windows.Forms.ToolStripPanel> auf das Formular.

2. <xref:System.Windows.Forms.ToolStripPanel>Doppelklicken Sie bei ausgewähltem Steuerelement <xref:System.Windows.Forms.ToolStrip> in der **Toolbox** auf das-Steuerelement.

     Ein- <xref:System.Windows.Forms.ToolStrip> Steuerelement wird im-Steuerelement erstellt <xref:System.Windows.Forms.ToolStripPanel> .

3. Wählen Sie das <xref:System.Windows.Forms.ToolStripPanel>-Steuerelement.

4. Ändern Sie in der Eigenschaftenfenster den Wert der-Eigenschaft des-Steuer Elements in <xref:System.Windows.Forms.Control.Dock%2A> <xref:System.Windows.Forms.DockStyle.Left> .

     Das- <xref:System.Windows.Forms.ToolStripPanel> Steuerelement wird auf der linken Seite des Formulars unterhalb des Hauptmenü andocken. Der MDI-Client Bereich ändert sich in die Größe des- <xref:System.Windows.Forms.ToolStripPanel> Steuer Elements.

5. Wiederholen Sie die Schritte 1 bis 4.

     Docken Sie das neue Steuerelement am <xref:System.Windows.Forms.ToolStripPanel> oberen Rand des Formulars an.

     Das <xref:System.Windows.Forms.ToolStripPanel> Steuerelement wird unter dem Hauptmenü angedockt, aber auf der rechten Seite des ersten <xref:System.Windows.Forms.ToolStripPanel> Steuer Elements. Dieser Schritt veranschaulicht die Wichtigkeit der z-Reihenfolge bei der ordnungsgemäßen Positionierung von Steuer <xref:System.Windows.Forms.ToolStripPanel> Elementen.

6. Wiederholen Sie die Schritte 1 bis 4 für zwei weitere Steuer <xref:System.Windows.Forms.ToolStripPanel> Elemente.

     Andocken der neuen Steuer <xref:System.Windows.Forms.ToolStripPanel> Elemente an der rechten und unteren Seite des Formulars.

## <a name="arrange-toolstrippanel-controls-by-z-order"></a>ToolStripPanel-Steuerelemente nach Z-Reihenfolge anordnen

Die Position eines angedockten <xref:System.Windows.Forms.ToolStripPanel> Steuer Elements auf dem MDI-Formular hängt von der Position des Steuer Elements in der z-Reihenfolge ab. Sie können die z-Reihenfolge der Steuerelemente im Fenster "Dokument Gliederung" problemlos anordnen.

1. Klicken Sie im Menü **Ansicht** auf **Weitere Fenster**, und klicken Sie dann auf **Dokument** Gliederung.

     Die Anordnung der Steuer <xref:System.Windows.Forms.ToolStripPanel> Elemente aus der vorherigen Prozedur entspricht nicht dem Standard. Dies liegt daran, dass die z-Reihenfolge nicht korrekt ist. Verwenden Sie das Fenster Dokument Gliederung, um die z-Reihenfolge der Steuerelemente zu ändern.

2. Wählen Sie im Fenster Dokument Gliederung die Option **ToolStripPanel4** aus.

3. Klicken Sie wiederholt auf die Schaltfläche mit dem Pfeil nach unten, bis sich **ToolStripPanel4** am Ende der Liste befindet.

     Das **ToolStripPanel4** -Steuerelement wird am unteren Rand des Formulars unterhalb der anderen Steuerelemente angedockt.

4. Wählen Sie **ToolStripPanel2** aus.

5. Klicken Sie einmal auf die Schaltfläche mit dem Pfeil nach unten, um das dritte Steuerelement in der Liste zu positionieren.

     Das **ToolStripPanel2** -Steuerelement wird am oberen Rand des Formulars unterhalb des Hauptmenü und über den anderen Steuerelementen angedockt.

6. Wählen Sie im **Dokument** Gliederungs Fenster verschiedene Steuerelemente aus, und verschieben Sie Sie an verschiedene Positionen in der z-Reihenfolge. Beachten Sie die Auswirkung der z-Reihenfolge auf die Platzierung von angedockten Steuerelementen. Verwenden Sie STRG + Z oder **Rückgängig** im Menü **Bearbeiten** , um die Änderungen rückgängig zu machen.

## <a name="checkpoint---test-your-form"></a>Prüfpunkt: Testen des Formulars

1. Drücken Sie **F5** , um das Formular zu kompilieren und auszuführen.

2. Klicken Sie auf den <xref:System.Windows.Forms.ToolStrip> Ziehpunkt eines Steuer Elements, und ziehen Sie das Steuerelement an verschiedene Positionen im Formular.

     Sie können ein- <xref:System.Windows.Forms.ToolStrip> Steuerelement von einem <xref:System.Windows.Forms.ToolStripPanel> Steuerelement zu einem anderen ziehen.

## <a name="next-steps"></a>Nächste Schritte

In dieser exemplarischen Vorgehensweise haben Sie ein übergeordnetes MDI-Formular mit Steuer <xref:System.Windows.Forms.ToolStrip> Elementen und der Zusammenführung des Menüs erstellt. Sie können die-Steuerelement <xref:System.Windows.Forms.ToolStrip> Familie zu vielen anderen Zwecken verwenden:

- Erstellen Sie Kontextmenüs für Ihre Steuerelemente mit <xref:System.Windows.Forms.ContextMenuStrip> . Weitere Informationen finden Sie unter [Übersicht über die ContextMenu-Komponente](contextmenu-component-overview-windows-forms.md).

- Erstellt ein Formular mit einem automatisch ausgefüllten Standardmenü. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Bereitstellen von Standard Menü Elementen für ein Formular](walkthrough-providing-standard-menu-items-to-a-form.md).

- Gestalten Sie Ihre Steuer <xref:System.Windows.Forms.ToolStrip> Elemente als professionelles Erscheinungsbild. Weitere Informationen finden Sie unter Gewusst [wie: Festlegen des ToolStrip-Renderers für eine Anwendung](how-to-set-the-toolstrip-renderer-for-an-application.md).

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [Vorgehensweise: Erstellen von übergeordneten MDI-Formularen](../advanced/how-to-create-mdi-parent-forms.md)
- [Vorgehensweise: Erstellen von untergeordneten MDI-Formularen](../advanced/how-to-create-mdi-child-forms.md)
- [Vorgehensweise: Einfügen eines MenuStrip in ein MDI-Dropdownmenü](how-to-insert-a-menustrip-into-an-mdi-drop-down-menu-windows-forms.md)
- [ToolStrip-Steuerelement](toolstrip-control-windows-forms.md)
