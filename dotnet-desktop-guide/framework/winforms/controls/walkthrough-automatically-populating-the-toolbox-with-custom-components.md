---
title: 'Exemplarische Vorgehensweise: Automatisches Füllen der Toolbox mit benutzerdefinierten Komponenten'
ms.date: 03/30/2017
helpviewer_keywords:
- IToolboxService interface
- Toolbox [Windows Forms], populating
- custom components [Windows Forms], adding to Toolbox
ms.assetid: 2fa1e3e8-6b9f-42b2-97c0-2be57444dba4
ms.openlocfilehash: 3ceebbf07c0241996479a6f7f72ab19f4cd9aa05
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976684"
---
# <a name="walkthrough-automatically-populating-the-toolbox-with-custom-components"></a>Exemplarische Vorgehensweise: Automatisches Füllen der Toolbox mit benutzerdefinierten Komponenten

Wenn die Komponenten von einem Projekt in der aktuell geöffneten Projekt Mappe definiert werden, werden Sie automatisch in der **Toolbox** angezeigt, ohne dass eine Aktion durch Sie erforderlich ist. Sie können die **Toolbox** auch manuell mit den benutzerdefinierten Komponenten auffüllen, indem Sie das [Dialog Feld Toolbox Elemente auswählen (Visual Studio)](/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100))verwenden, aber die **Toolbox** berücksichtigt die Elemente in den Buildausgaben ihrer Projekt Mappe mit den folgenden Merkmalen:

- Implementiert <xref:System.ComponentModel.IComponent> ;

- Hat nicht <xref:System.ComponentModel.ToolboxItemAttribute> auf festgelegt `false` .

- Hat nicht <xref:System.ComponentModel.DesignTimeVisibleAttribute> auf festgelegt `false` .

> [!NOTE]
> Die **Toolbox** folgt nicht den Verweis Ketten, sodass keine Elemente angezeigt werden, die nicht von einem Projekt in der Projekt Mappe erstellt werden.

In dieser exemplarischen Vorgehensweise wird veranschaulicht, wie eine benutzerdefinierte Komponente automatisch in der **Toolbox** angezeigt wird, nachdem die Komponente erstellt wurde. In dieser exemplarischen Vorgehensweise werden u. a. folgende Aufgaben veranschaulicht:

- Erstellen eines Windows Forms Projekts

- Erstellen einer benutzerdefinierten Komponente.

- Erstellen einer Instanz einer benutzerdefinierten Komponente.

- Entladen und erneutes Laden einer benutzerdefinierten Komponente.

Wenn Sie fertig sind, werden Sie feststellen, dass die **Toolbox** mit einer Komponente aufgefüllt ist, die Sie erstellt haben.

## <a name="create-the-project"></a>Erstellen des Projekts

1. Erstellen Sie in Visual Studio ein Windows-basiertes Anwendungsprojekt mit dem Namen `ToolboxExample` (**File**  >  **New**  >  **Project**  >  **Visual c#** oder **Visual Basic**  >  **Classic Desktop**  >  **Windows Forms Anwendung**).

2. Fügen Sie dem Projekt eine neue Komponente hinzu. Geben Sie ihm den Namen `DemoComponent`.

     Weitere Informationen finden Sie unter Gewusst [wie: Hinzufügen neuer Projekt Elemente](/previous-versions/visualstudio/visual-studio-2010/w0572c5b(v=vs.100)).

3. Erstellen Sie das Projekt.

4. Klicken Sie **im Menü Extras** auf das **options** Element. Klicken Sie unter dem **Windows Forms-Designer** Element auf **Allgemein** , und stellen Sie sicher, dass die **autotoolboxpopulate** -Option auf **true** festgelegt ist.

## <a name="create-an-instance-of-a-custom-component"></a>Erstellen einer Instanz einer benutzerdefinierten Komponente

Der nächste Schritt ist das Erstellen einer Instanz der benutzerdefinierten Komponente auf dem Formular. Da die **Toolbox** automatisch die neue Komponente berücksichtigt, ist dies so einfach wie das Erstellen einer beliebigen anderen Komponente oder eines Steuer Elements.

1. Öffnen Sie das Projektformular im Formular- **Designer**.

2. Klicken Sie in der **Toolbox** auf die Registerkarte neu namens **ToolboxExample Components**.

     Wenn Sie auf die Registerkarte klicken, wird **DemoComponent** angezeigt.

    > [!NOTE]
    > Aus Leistungsgründen zeigen Komponenten im automatisch aufgefüllten Bereich der **Toolbox** keine benutzerdefinierten Bitmaps an, und <xref:System.Drawing.ToolboxBitmapAttribute> wird nicht unterstützt. Um ein Symbol für eine benutzerdefinierte Komponente in der **Toolbox** anzuzeigen, verwenden Sie das Dialogfeld **Toolbox Elemente auswählen** , um die Komponente zu laden.

3. Ziehen Sie die Komponente auf das Formular.

     Eine Instanz der Komponente wird erstellt und der **Komponenten Leiste** hinzugefügt.

## <a name="unload-and-reload-a-custom-component"></a>Entladen und erneutes Laden einer benutzerdefinierten Komponente

Die **Toolbox** berücksichtigt die Komponenten in jedem geladenen Projekt, und wenn ein Projekt entladen wird, werden die Verweise auf die Projektkomponenten entfernt.

1. Entladen Sie das Projekt aus der Projekt Mappe.

     Weitere Informationen zum Entladen von Projekten finden Sie unter Gewusst [wie: entladen und](/previous-versions/visualstudio/visual-studio-2010/tt479x1t(v=vs.100))erneutes Laden von Projekten. Wenn Sie zum Speichern aufgefordert werden, wählen Sie **Ja** aus.

2. Fügen Sie der Projekt Mappe ein neues **Windows-Anwendungs** Projekt hinzu. Öffnen Sie das Formular im **Designer**.

     Die **ToolboxExample-Komponenten** Registerkarte aus dem vorherigen Projekt ist nun nicht mehr vorhanden.

3. Laden Sie das `ToolboxExample` Projekt neu.

     Die **ToolboxExample-Komponenten** Registerkarte wird nun erneut angezeigt.

## <a name="next-steps"></a>Nächste Schritte

In dieser exemplarischen Vorgehensweise wird veranschaulicht, dass die **Toolbox** die Komponenten eines Projekts berücksichtigt, aber die **Toolbox** berücksichtigt auch die Steuerelemente. Experimentieren Sie mit ihren eigenen benutzerdefinierten Steuerelementen, indem Sie Steuerelemente hinzufügen und aus der Projekt Mappe entfernen.

## <a name="see-also"></a>Siehe auch

- [Allgemein, Windows Forms-Designer, Dialogfeld "Optionen"](/previous-versions/visualstudio/visual-studio-2010/5aazxs78(v=vs.100))
- [Vorgehensweise: Ändern von Registerkarten der Toolbox](/previous-versions/visualstudio/visual-studio-2010/66kwe227(v=vs.100))
- [Dialogfeld „Toolboxelemente auswählen“ (Visual Studio)](/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100))
- [Einfügen von Steuerelementen in Windows Forms](putting-controls-on-windows-forms.md)
