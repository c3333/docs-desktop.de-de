---
title: 'Exemplarische Vorgehensweise: Bereitstellen von Standardmenüelementen für ein Formular'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- menu items [Windows Forms], standard
- toolbars [Windows Forms], walkthroughs
- StatusStrip control [Windows Forms]
- ToolStrip control [Windows Forms]
ms.assetid: dac37d98-589e-4d6d-9673-6437e8943122
ms.openlocfilehash: ee80aad445c00bb4b98b49c80495fa512150bcef
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976595"
---
# <a name="walkthrough-providing-standard-menu-items-to-a-form"></a>Exemplarische Vorgehensweise: Bereitstellen von Standardmenüelementen für ein Formular

Mit dem <xref:System.Windows.Forms.MenuStrip>-Steuerelement können Sie ein Standardmenü für Formulare bereitstellen.

Diese exemplarische Vorgehensweise veranschaulicht, wie ein-Steuerelement verwendet wird <xref:System.Windows.Forms.MenuStrip> , um ein Standardmenü zu erstellen. Das Formular antwortet auch, wenn ein Benutzer ein Menü Element auswählt. In dieser exemplarischen Vorgehensweise werden die folgenden Aufgaben veranschaulicht:

- Erstellen eines Windows Forms Projekts

- Erstellen eines Standardmenüs.

- Erstellen eines- <xref:System.Windows.Forms.StatusStrip> Steuer Elements.

- Menü Elementauswahl wird verarbeitet.

Wenn Sie fertig sind, verfügen Sie über ein Formular mit einem Standardmenü, in dem die Auswahl von Menü Elementen in einem-Steuerelement angezeigt wird <xref:System.Windows.Forms.StatusStrip> .

Informationen zum Kopieren des Codes in diesem Thema als einzelne Auflistung finden Sie unter Gewusst [wie: Bereitstellen von Standard Menü Elementen für ein Formular](how-to-provide-standard-menu-items-to-a-form.md).

## <a name="prerequisites"></a>Voraussetzungen

Sie benötigen Visual Studio, um diese exemplarische Vorgehensweise abzuschließen.

## <a name="create-the-project"></a>Erstellen des Projekts

1. Erstellen Sie in Visual Studio ein Windows-Anwendungsprojekt mit dem Namen **StandardMenuForm** (**Datei**  >  **neu**  >  **Projekt**  >  **Visual c#** oder **Visual Basic**  >  **klassische Desktop**  >  **Windows Forms Anwendung**).

2. Wählen Sie im Windows Forms-Designer das Formular aus.

## <a name="create-a-standard-menu"></a>Standardmenü erstellen

Der Windows Forms-Designer kann ein Steuerelement automatisch <xref:System.Windows.Forms.MenuStrip> mit Standardmenü Elementen auffüllen.

1. Ziehen Sie aus der **Toolbox** ein- <xref:System.Windows.Forms.MenuStrip> Steuerelement auf das Formular.

2. Klicken Sie auf das <xref:System.Windows.Forms.MenuStrip> Designer-Aktions Symbol des Steuer Elements ( ![ kleiner schwarzer Pfeil ](./media/designer-actions-glyph.gif) ), und wählen Sie **Standard Elemente einfügen** aus.

     Das- <xref:System.Windows.Forms.MenuStrip> Steuerelement wird mit den Standardmenü Elementen aufgefüllt.

3. Klicken Sie auf das Menü Element **Datei** , um die Standardmenü Elemente und zugehörige Symbole anzuzeigen.

## <a name="create-a-statusstrip-control"></a>Erstellen eines Status Strip-Steuer Elements

Verwenden Sie das- <xref:System.Windows.Forms.StatusStrip> Steuerelement, um den Status für Ihre Windows Forms Anwendungen anzuzeigen. Im aktuellen Beispiel werden vom Benutzer ausgewählte Menü Elemente in einem-Steuerelement angezeigt <xref:System.Windows.Forms.StatusStrip> .

1. Ziehen Sie aus der **Toolbox** ein- <xref:System.Windows.Forms.StatusStrip> Steuerelement auf das Formular.

     Das-Steuerelement wird <xref:System.Windows.Forms.StatusStrip> automatisch am Ende des Formulars angedockt.

2. Klicken Sie auf die <xref:System.Windows.Forms.StatusStrip> Dropdown Schaltfläche des Steuer Elements, und wählen Sie **Status Bezeichnung** , um dem Steuerelement ein Steuerelement hinzuzufügen <xref:System.Windows.Forms.ToolStripStatusLabel> <xref:System.Windows.Forms.StatusStrip> .

## <a name="handle-item-selection"></a>Elementauswahl behandeln

Behandeln Sie das- <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> Ereignis, um zu reagieren, wenn der Benutzer ein Menü Element auswählt.

1. Klicken Sie auf das Menü Element **Datei** , das Sie im Abschnitt Erstellen eines Standard Menüs erstellt haben.

2. Klicken Sie im Fenster **Eigenschaften** auf **Ereignisse**.

3. Doppelklicken Sie auf das <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> Ereignis.

     Der Windows Forms-Designer generiert einen Ereignishandler für das- <xref:System.Windows.Forms.ToolStripDropDownItem.DropDownItemClicked> Ereignis.

4. Fügen Sie den folgenden Code in den-Ereignishandler ein.

     [!code-csharp[System.Windows.Forms.ToolStrip.StandardMenu#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.ToolStrip.StandardMenu#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/VB/Form1.vb#3)]

5. Fügen Sie die `UpdateStatus` Definition der hilfsprogrammmethode in das Formular ein.

     [!code-csharp[System.Windows.Forms.ToolStrip.StandardMenu#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.ToolStrip.StandardMenu#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StandardMenu/VB/Form1.vb#2)]

## <a name="checkpoint--test-your-form"></a>Prüfpunkt: Testen des Formulars

1. Drücken Sie **F5** , um das Formular zu kompilieren und auszuführen.

2. Klicken Sie auf das Menü Element **Datei** , um das Menü zu öffnen.

3. Klicken Sie im Menü **Datei** auf eines der Elemente, um es auszuwählen.

     Das- <xref:System.Windows.Forms.StatusStrip> Steuerelement zeigt das ausgewählte Element an.

## <a name="next-steps"></a>Nächste Schritte

In dieser exemplarischen Vorgehensweise haben Sie ein Formular mit einem Standardmenü erstellt. Sie können die-Steuerelement <xref:System.Windows.Forms.ToolStrip> Familie zu vielen anderen Zwecken verwenden:

- Erstellen Sie Kontextmenüs für Ihre Steuerelemente mit <xref:System.Windows.Forms.ContextMenuStrip> . Weitere Informationen finden Sie unter [Übersicht über die ContextMenu-Komponente](contextmenu-component-overview-windows-forms.md).

- Erstellen Sie ein MDI-Formular (Multiple Document Interface) mit andockbaren Steuer <xref:System.Windows.Forms.ToolStrip> Elementen. Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Erstellen eines MDI-Formulars mit der Zusammenführung von Menüs und ToolStrip-Steuerelementen](walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).

- Gestalten Sie Ihre Steuer <xref:System.Windows.Forms.ToolStrip> Elemente als professionelles Erscheinungsbild. Weitere Informationen finden Sie unter Gewusst [wie: Festlegen des ToolStrip-Renderers für eine Anwendung](how-to-set-the-toolstrip-renderer-for-an-application.md).

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [MenuStrip-Steuerelement](menustrip-control-windows-forms.md)
