---
title: 'Exemplarische Vorgehensweise: Erstellen eines professionellen ToolStrip-Steuerelements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStripProfessionalRenderer class [Windows Forms]
- ToolStripRenderer class [Windows Forms]
- toolbars [Windows Forms], walkthroughs
- ToolStrip control [Windows Forms], creating professionally styled controls
ms.assetid: b52339ae-f1d3-494e-996e-eb455614098a
ms.openlocfilehash: 3fd9175f47f9f1b35743dc69b462227fdfafe55d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976963"
---
# <a name="walkthrough-creating-a-professionally-styled-toolstrip-control"></a>Exemplarische Vorgehensweise: Erstellen eines professionellen ToolStrip-Steuerelements

Sie können den Steuerelementen Ihrer Anwendung <xref:System.Windows.Forms.ToolStrip> ein professionelles Aussehen und Verhalten geben, indem Sie eine eigene Klasse schreiben, die vom-Typ abgeleitet ist <xref:System.Windows.Forms.ToolStripProfessionalRenderer> .

In dieser exemplarischen Vorgehensweise wird veranschaulicht, wie <xref:System.Windows.Forms.ToolStrip> Steuerelemente verwendet werden, um ein zusammengesetztes Steuerelement zu erstellen, das dem **Navigations** Bereich von Microsoft® Outlook® In dieser exemplarischen Vorgehensweise werden die folgenden Aufgaben veranschaulicht:

- Erstellen eines Windows-Steuerelement Bibliothek-Projekts.

- Entwerfen des StackView-Steuer Elements.

- Implementieren eines benutzerdefinierten Renderers.

Wenn Sie fertig sind, verfügen Sie über ein wiederverwendbares benutzerdefiniertes Client Steuerelement, das die professionelle Darstellung eines Microsoft Office® XP-Steuer Elements enthält.

Informationen zum Kopieren des Codes in diesem Thema als einzelne Auflistung finden Sie unter Gewusst [wie: Erstellen eines professionell formatierten ToolStrip-Steuer](how-to-create-a-professionally-styled-toolstrip-control.md)Elements.

## <a name="prerequisites"></a>Voraussetzungen

Sie benötigen Visual Studio, um diese exemplarische Vorgehensweise abzuschließen.

## <a name="create-the-control-library-project"></a>Erstellen des Steuerelement Bibliothek-Projekts

1. Erstellen Sie in Visual Studio ein neues Windows-Steuerelement Bibliothek-Projekt mit dem Namen `StackViewLibrary` .

2. Löschen Sie in **Projektmappen-Explorer** das Standard Steuerelement des Projekts, indem Sie die Quelldatei mit dem Namen "UserControl1.cs" oder "UserControl1. vb" löschen, je nach ihrer Sprache Ihrer Wahl.

     Weitere Informationen finden Sie unter Gewusst [wie: entfernen, löschen und Ausschließen von Elementen](/previous-versions/visualstudio/visual-studio-2010/0ebzhwsk(v=vs.100)).

3. Fügen Sie <xref:System.Windows.Forms.UserControl> dem **StackViewLibrary** -Projekt ein neues Element hinzu. Benennen Sie die neue Quelldatei mit einem Basisnamen von `StackView` .

## <a name="design-the-stackview-control"></a>Entwerfen des StackView-Steuer Elements

Das `StackView` Steuerelement ist ein zusammengesetztes Steuerelement mit einem untergeordneten <xref:System.Windows.Forms.ToolStrip> Steuerelement Weitere Informationen zu zusammengesetzten Steuerelementen finden Sie unter [Varianten von benutzerdefinierten Steuerelementen](varieties-of-custom-controls.md).

1. Ziehen Sie aus der **Toolbox** ein- <xref:System.Windows.Forms.ToolStrip> Steuerelement auf die Entwurfs Oberfläche.

2. Legen Sie im Fenster **Eigenschaften** die <xref:System.Windows.Forms.ToolStrip> Eigenschaften des Steuer Elements gemäß der folgenden Tabelle fest.

    |Eigenschaft|Wert|
    |--------------|-----------|
    |Name|`stackStrip`|
    |CanOverflow|`false`|
    |Dock|<xref:System.Windows.Forms.DockStyle.Bottom>|
    |Schriftart|`Tahoma, 10pt, style=Bold`|
    |GripStyle|<xref:System.Windows.Forms.ToolStripGripStyle.Hidden>|
    |LayoutStyle|<xref:System.Windows.Forms.ToolStripLayoutStyle.VerticalStackWithOverflow>|
    |Auffüllen|`0, 7, 0, 0`|
    |RenderMode|<xref:System.Windows.Forms.ToolStripRenderMode.Professional>|

3. Klicken Sie im Windows Forms-Designer auf die <xref:System.Windows.Forms.ToolStrip> Schaltfläche **Hinzufügen** des Steuer Elements, und fügen Sie dem Steuerelement eine hinzu <xref:System.Windows.Forms.ToolStripButton> `stackStrip` .

4. Legen Sie im Fenster **Eigenschaften** die <xref:System.Windows.Forms.ToolStripButton> Eigenschaften des Steuer Elements gemäß der folgenden Tabelle fest.

    |Eigenschaft|Wert|
    |--------------|-----------|
    |Name|`mailStackButton`|
    |CheckOnClick|true|
    |CheckState|<xref:System.Windows.Forms.CheckState.Checked>|
    |Display Style|<xref:System.Windows.Forms.ToolStripItemDisplayStyle.ImageAndText>|
    |ImageAlign|<xref:System.Drawing.ContentAlignment.MiddleLeft>|
    |ImageScaling|<xref:System.Windows.Forms.ToolStripItemImageScaling.None>|
    |ImageTransparentColor|`238, 238, 238`|
    |Margin|`0, 0, 0, 0`|
    |Auffüllen|`3, 3, 3, 3`|
    |Text|**Mail**|
    |Textausrichtung|<xref:System.Drawing.ContentAlignment.MiddleLeft>|

5. Wiederholen Sie Schritt 7 für drei weitere Steuer <xref:System.Windows.Forms.ToolStripButton> Elemente.

     Benennen Sie die Steuerelemente `calendarStackButton` , `contactsStackButton` und `tasksStackButton` . Legen Sie den Wert der- <xref:System.Windows.Forms.Control.Text%2A> Eigenschaft auf **Calendar**, **Contacts** bzw. **Tasks** fest.

## <a name="handle-events"></a>Behandeln von Ereignissen

Zwei Ereignisse sind wichtig, damit das `StackView` Steuerelement ordnungsgemäß funktioniert. Behandeln Sie das- <xref:System.Windows.Forms.UserControl.Load> Ereignis, um das Steuerelement korrekt zu positionieren. Behandeln Sie das- <xref:System.Windows.Forms.ToolStripItem.Click> Ereignis für jedes <xref:System.Windows.Forms.ToolStripButton> , um dem Steuerelement `StackView` Zustands Verhalten ähnlich wie das-Steuerelement zu übergeben <xref:System.Windows.Forms.RadioButton> .

1. Wählen Sie im Windows Forms-Designer das Steuerelement aus `StackView` .

2. Klicken Sie im Fenster **Eigenschaften** auf **Ereignisse**.

3. Doppelklicken Sie auf das Lade Ereignis, um den `StackView_Load` Ereignishandler zu generieren.

4. Kopieren Sie den folgenden Code und fügen Sie ihn in den `StackView_Load`-Ereignishandler ein.

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#3)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#3)]

5. Wählen Sie im Windows Forms-Designer das Steuerelement aus `mailStackButton` .

6. Klicken Sie im Fenster **Eigenschaften** auf **Ereignisse**.

7. Doppelklicken Sie auf das Click-Ereignis.

     Der-Windows Forms-Designer generiert den- `mailStackButton_Click` Ereignishandler.

8. Benennen Sie den- `mailStackButton_Click` Ereignishandler in um `stackButton_Click` .

     Weitere Informationen finden Sie unter [Umbenennen einer Code Symbol Umgestaltung](/visualstudio/ide/reference/rename).

9. Fügen Sie den folgenden Code in den- `stackButton_Click` Ereignishandler ein.

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#4)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#4)]

10. Wählen Sie im Windows Forms-Designer das Steuerelement aus `calendarStackButton` .

11. Legen Sie im Fenster **Eigenschaften** das Click-Ereignis auf den `stackButton_Click` Ereignishandler fest.

12. Wiederholen Sie die Schritte 10 und 11 für die Steuer `contactsStackButton` `tasksStackButton` Elemente und.

## <a name="define-icons"></a>Symbole definieren

Jede `StackView` Schaltfläche verfügt über ein zugeordnetes Symbol. Aus praktischer Gründen wird jedes Symbol als Base64-codierte Zeichenfolge dargestellt, die deserialisiert wird, bevor ein <xref:System.Drawing.Bitmap> daraus erstellt wird. In einer Produktionsumgebung speichern Sie Bitmapdaten als Ressource, und ihre Symbole werden in der Windows Forms-Designer angezeigt. Weitere Informationen finden Sie unter Gewusst [wie: Hinzufügen von Hintergrundbildern zu Windows Forms](/previous-versions/visualstudio/visual-studio-2010/dff9f95f(v=vs.100)).

1. Fügen Sie im Code-Editor den folgenden Code in die `StackView` Klassendefinition ein. Dieser Code initialisiert die Bitmaps für die <xref:System.Windows.Forms.ToolStripButton> Symbole.

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#2)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#2)]

2. Fügen Sie der- `InitializeImages` Methode im- `StackView` Klassenkonstruktor einen-Rückruf hinzu.

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#5)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#5)]

## <a name="implement-a-custom-renderer"></a>Implementieren eines benutzerdefinierten Renderers

Sie können die meisten Elemente des Steuer Elements anpassen `StackView` , das eine Klasse implementiert, die von der-Klasse abgeleitet ist <xref:System.Windows.Forms.ToolStripRenderer> . In diesem Verfahren implementieren Sie eine Klasse, die <xref:System.Windows.Forms.ToolStripProfessionalRenderer> den Ziehpunkt anpasst und die Farbverlaufs Hintergründe der Steuer <xref:System.Windows.Forms.ToolStripButton> Elemente zeichnet.

1. Fügen Sie den folgenden Code in die `StackView` Steuerelement Definition ein.

     Dies ist die Definition für die `StackRenderer` -Klasse, die die <xref:System.Windows.Forms.ToolStripRenderer.RenderGrip> Methoden, und überschreibt, <xref:System.Windows.Forms.ToolStripRenderer.RenderToolStripBorder> <xref:System.Windows.Forms.ToolStripRenderer.RenderButtonBackground> um ein benutzerdefiniertes aussehen zu schaffen.

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#10)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#10)]

2. `StackView`Erstellen Sie im Konstruktor des Steuer Elements eine neue Instanz der `StackRenderer` -Klasse, und weisen Sie diese Instanz der `stackStrip` -Eigenschaft des-Steuer Elements zu <xref:System.Windows.Forms.ToolStrip.Renderer%2A> .

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#5)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#5)]

## <a name="test-the-stackview-control"></a>Testen des StackView-Steuer Elements

Das-Steuerelement wird `StackView` von der- <xref:System.Windows.Forms.UserControl> Klasse abgeleitet. Daher können Sie das Steuerelement mit dem **UserControl-Test Container** testen. Weitere Informationen finden Sie unter Gewusst [wie: Testen des Run-Time Verhaltens eines UserControl-Steuer](how-to-test-the-run-time-behavior-of-a-usercontrol.md)Elements.

1. Drücken Sie **F5** , um das Projekt zu erstellen und den **UserControl-Test Container** zu starten.

2. Bewegen Sie den Mauszeiger über die Schaltflächen des `StackView` Steuer Elements, und klicken Sie dann auf eine Schaltfläche, um die Darstellung des ausgewählten Zustands anzuzeigen.

## <a name="next-steps"></a>Nächste Schritte

In dieser exemplarischen Vorgehensweise haben Sie ein wiederverwendbares benutzerdefiniertes Client Steuerelement mit dem professionellen Aussehen eines Office XP-Steuer Elements erstellt. Sie können die-Steuerelement <xref:System.Windows.Forms.ToolStrip> Familie zu vielen anderen Zwecken verwenden:

- Erstellen Sie Kontextmenüs für Ihre Steuerelemente mit <xref:System.Windows.Forms.ContextMenuStrip> . Weitere Informationen finden Sie unter [Übersicht über die ContextMenu-Komponente](contextmenu-component-overview-windows-forms.md).

- Erstellen Sie ein Formular mit einem automatisch ausgefüllten Standardmenü. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Bereitstellen von Standard Menü Elementen für ein Formular](walkthrough-providing-standard-menu-items-to-a-form.md).

- Erstellen Sie ein MDI-Formular (Multiple Document Interface) mit andockbaren Steuer <xref:System.Windows.Forms.ToolStrip> Elementen. Weitere Informationen finden Sie unter Gewusst [wie: Erstellen eines MDI-Formulars mit der Zusammenführung von Menüs und ToolStrip-Steuerelementen](how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [ToolStrip-Steuerelement](toolstrip-control-windows-forms.md)
- [Vorgehensweise: Bereitstellen von Standardmenüelementen für ein Formular](how-to-provide-standard-menu-items-to-a-form.md)
