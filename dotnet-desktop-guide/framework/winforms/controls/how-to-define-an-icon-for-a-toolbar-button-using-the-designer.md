---
title: 'Vorgehensweise: Definieren eines Symbols für eine Symbolleistenschaltfläche mithilfe des Designers'
ms.date: 03/30/2017
helpviewer_keywords:
- toolbars [Windows Forms], adding icons to buttons
- examples [Windows Forms], toolbars
- images [Windows Forms], toolbar buttons
- buttons [Windows Forms], images
- icons [Windows Forms], toolbar buttons
- ToolBar control [Windows Forms], adding icons to buttons
ms.assetid: d848f38e-67f2-49d4-8e88-01c845c06c02
ms.openlocfilehash: 49e93f12bebbf409e6b3a06634556b9103c85f44
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975679"
---
# <a name="how-to-define-an-icon-for-a-toolbar-button-using-the-designer"></a>Vorgehensweise: Definieren eines Symbols für eine Symbolleistenschaltfläche mithilfe des Designers

> [!NOTE]
> Obwohl das <xref:System.Windows.Forms.ToolStrip>-Steuerelement das <xref:System.Windows.Forms.ToolBar>-Steuerelement ersetzt und funktionell erweitert, wird das <xref:System.Windows.Forms.ToolBar>-Steuerelement sowohl aus Gründen der Abwärtskompatibilität als auch, falls gewünscht, für die zukünftige Verwendung beibehalten.

<xref:System.Windows.Forms.ToolBar> mithilfe von Schaltflächen können darin Symbole angezeigt werden, die von Benutzern leichter identifiziert werden können. Dies wird erreicht, indem der Komponente Bilder hinzugefügt <xref:System.Windows.Forms.ImageList> und dem Steuerelement zugeordnet wird <xref:System.Windows.Forms.ToolBar> .

Das folgende Verfahren erfordert ein **Windows-Anwendungs** Projekt mit einem Formular, das ein <xref:System.Windows.Forms.ToolBar> -Steuerelement und eine- <xref:System.Windows.Forms.ImageList> Komponente enthält. Weitere Informationen zum Einrichten eines solchen Projekts finden Sie unter Gewusst [wie: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project) und Gewusst [wie: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).

### <a name="to-set-an-icon-for-a-toolbar-button-at-design-time"></a>So legen Sie ein Symbol für eine Symbolleisten-Schaltfläche zur Entwurfszeit fest

1. Fügen Sie der Komponente Bilder hinzu <xref:System.Windows.Forms.ImageList> . Weitere Informationen finden Sie unter Gewusst [wie: Hinzufügen oder Entfernen von ImageList-Bildern mit dem Designer](how-to-add-or-remove-imagelist-images-with-the-designer.md).

2. Wählen Sie das <xref:System.Windows.Forms.ToolBar> Steuerelement auf dem Formular aus.

3. Legen Sie im Fenster **Eigenschaften** die <xref:System.Windows.Forms.ToolBar> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.ToolBar.ImageList%2A> auf die-Komponente fest <xref:System.Windows.Forms.ImageList> .

4. Klicken Sie <xref:System.Windows.Forms.ToolBar> auf die-Eigenschaft des Steuer Elements, um es auszuwählen, und klicken Sie auf die Schaltfläche mit den Auslassungs Punkten ( <xref:System.Windows.Forms.ToolBar.Buttons%2A> ![ ...) in der Eigenschaftenfenster von Visual Studio. ](./media/visual-studio-ellipsis-button.png) ), um den **ToolBarButton**-Auflistungs-Editor zu öffnen.

5. Mithilfe der Schaltfläche **Hinzufügen** können Sie dem Steuerelement Schaltflächen hinzufügen <xref:System.Windows.Forms.ToolBar> .

6. Legen Sie im Fenster **Eigenschaften** , das im Bereich auf der rechten Seite des **ToolBarButton**-Auflistungs-Editors angezeigt wird, die- <xref:System.Windows.Forms.ToolBarButton.ImageIndex%2A> Eigenschaft jeder Symbolleisten-Schaltfläche auf einen der Werte in der Liste fest, der aus den Bildern gezeichnet wird, die Sie der Komponente hinzugefügt haben <xref:System.Windows.Forms.ImageList> .

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolBar>
- [Vorgehensweise: Auslösen von Menüereignissen für Symbolleistenschaltflächen](how-to-trigger-menu-events-for-toolbar-buttons.md)
- [ToolBar-Steuerelement](toolbar-control-windows-forms.md)
- [ImageList-Komponente](imagelist-component-windows-forms.md)
