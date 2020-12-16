---
title: 'Tutorial: Erstellen einer neuen App mit Visual Studio'
description: In diesem Tutorial erfahren Sie, wie Sie mit Visual Studio 2019 eine neue Windows Forms-App für .NET erstellen.
ms.date: 10/26/2020
ms.topic: tutorial
dev_langs:
- csharp
- vb
ms.openlocfilehash: db0712aa642e54373f686fdd24a4747bf2d195e3
ms.sourcegitcommit: e8e3f6f23b5ddf9f5c4fe1ec5f6e0a8a609d49c8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "97004731"
---
# <a name="tutorial-create-a-new-winforms-app-windows-forms-net"></a>Tutorial: Erstellen einer neuen WinForms-App (Windows Forms .NET)

In diesem kurzen Tutorial wird beschrieben, wie Sie mit Visual Studio eine neue Windows Forms-App (WinForms) erstellen. Nachdem Sie die vorläufige App generiert haben, erfahren Sie, wie Sie Steuerelemente hinzufügen und Ereignisse verarbeiten. Am Ende dieses Tutorials verfügen Sie über eine einfache App, die einem Listenfeld Namen hinzufügt.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

In diesem Tutorial lernen Sie Folgendes:

> [!div class="checklist"]
>
> - Erstellen einer neuen WinForms-App
> - Hinzufügen von Steuerelementen zu einem Formular
> - Verarbeiten von Steuerungsereignissen zum Bereitstellen von App-Funktionalität
> - Ausführen der App

## <a name="prerequisites"></a>Voraussetzungen

- [Visual Studio 2019, Version 16.8 oder höher](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019+desktopguide+winforms)
  - Wählen Sie die [Visual Studio-Desktopworkload](/visualstudio/install/modify-visual-studio?view=vs-2019&preserve-view=true#modify-workloads) aus.
  - Wählen Sie eine [einzelne .NET 5-Komponente](/visualstudio/install/modify-visual-studio?view=vs-2019&preserve-view=true#modify-individual-components) aus.

## <a name="create-a-winforms-app"></a>Erstellen einer WinForms-App

Für die Erstellung einer neuen App müssen Sie erst Visual Studio öffnen und die App dann aus einer Vorlage erstellen.

01. Öffnen Sie Visual Studio.
01. Wählen Sie **Neues Projekt erstellen** aus.

    :::image type="content" source="media/create-app-visual-studio/vs-create-new-project.png" alt-text="Erstellen eines neuen Windows Forms-Projekts in Visual Studio 2019 für .NET":::

01. Geben Sie in das Feld **Search for templates** (Vorlagen suchen) **winforms** ein, und drücken Sie die <kbd>EINGABETASTE</kbd>.
01. Wählen Sie aus der Dropdownliste **Codesprache** die Option **C#** oder **Visual Basic** aus.
01. Wählen Sie aus der Vorlagenliste **Windows Forms App (.NET)** (Windows Forms-App (.NET)) aus, und klicken Sie dann auf **Weiter**.

    > [!IMPORTANT]
    > Wählen Sie nicht die Vorlage **Windows Forms-App (.NET _Framework_)** aus.

    :::image type="content" source="media/create-app-visual-studio/vs-template-search.png" alt-text="Suche nach der Windows Forms-Vorlage in Visual Studio 2019 für .NET":::

01. Legen Sie das Feld **Projektname** im Fenster **Neues Projekt konfigurieren** auf **Namen** fest, und klicken Sie auf **Erstellen**.

    Sie können Ihr Projekt auch in einem anderen Ordner speichern, indem Sie die Einstellung **Speicherort** anpassen.

    :::image type="content" source="media/create-app-visual-studio/vs-config-new-project.png" alt-text="Konfigurieren eines neuen Windows Forms-Projekts in Visual Studio 2019 für .NET":::

Nachdem die App generiert wurde, sollte Visual Studio den Designbereich für das Standardformular _Form1_ öffnen. Wenn der Formular-Designer nicht angezeigt wird, doppelklicken Sie im Bereich **Projektmappen-Explorer** auf das Formular, um das Designer-Fenster zu öffnen.

### <a name="important-parts-of-visual-studio"></a>Wichtige Visual Studio-Komponenten

WinForms wird in Visual Studio durch vier wichtige Komponenten unterstützt, mit denen Sie bei der App-Erstellung interagieren:

:::image type="content" source="media/create-app-visual-studio/vs-main-window.png" alt-text="Die wichtigen Visual Studio-Komponenten, die Sie beim Erstellen eines Windows Forms-Projekts für .NET kennen sollten":::

01. Projektmappen-Explorer

    Alle Ihre Projektdateien, Formulare und Ressourcen sowie Ihr gesamter Code wird in diesem Bereich angezeigt.

02. Eigenschaften

    In diesem Bereich werden die Eigenschafteneinstellungen angezeigt, die Sie für das ausgewählte Element konfigurieren können. Wenn Sie z. B. ein Element im **Projektmappen-Explorer** auswählen, werden die Eigenschafteneinstellungen für diese Datei angezeigt. Wenn Sie ein Objekt im **Designer** anklicken, werden die Einstellungen für das Steuerelement oder Formular angezeigt.

03. Formular-Designer

    Dies ist der Designer für das Formular. Hierbei handelt es sich um eine interaktive Oberfläche, in die Sie Objekte per Drag & Drop aus der **Toolbox** verschieben können. Wenn Sie Elemente im Designer auswählen und verschieben, können Sie die Benutzeroberfläche für Ihre App visuell zusammenstellen.

04. Werkzeugkasten

    Die Toolbox enthält alle Steuerelemente, die Sie einem Formular hinzufügen können. Doppelklicken Sie zum Hinzufügen eines Steuerelements zum aktuellen Formular auf ein Steuerelement, oder verschieben Sie das Steuerelement per Drag & Drop.

## <a name="add-controls-to-the-form"></a>Hinzufügen von Steuerelementen zu dem Formular

Wenn der Formular-Designer für _Form1_ geöffnet ist, fügen Sie dem Formular über den Bereich **Toolbox** die folgenden Steuerelemente hinzu:

- Bezeichnung
- Schaltfläche
- Listenfeld
- Textfeld

Sie können die Steuerelemente gemäß den folgenden Einstellungen positionieren und in der Größe anpassen. Verschieben Sie sie entweder visuell, sodass sie dem folgenden Screenshot entsprechen, oder klicken Sie auf jedes Steuerelement, und konfigurieren Sie die Einstellungen im Bereich **Eigenschaften**. Sie können auch auf den Titelbereich des Formulars klicken, um das Formular auszuwählen:

| Object      | Einstellung  | Wert      |
|-------------|----------|------------|
| **Form**    | Text     | `Names`    |
|             | Größe     | `268, 180` |
|             |          |            |
| **Label**   | Standort | `12, 9`    |
|             | Text     | `Names`    |
|             |          |            |
| **Listenfeld** | Name     | `lstNames` |
|             | Standort | `12, 27`   |
|             | Größe     | `120, 94`  |
|             |          |            |
| **Textfeld** | Name     | `txtName`  |
|             | Standort | `138, 26`  |
|             | Größe     | `100, 23`  |
|             |          |            |
| **Schaltfläche**  | Name     | `btnAdd`   |
|             | Standort | `138, 55`  |
|             | Größe     | `100, 23`  |
|             | Text     | `Add Name` |

Im Designer sollte Ihnen ein Formular angezeigt werden, das in etwa wie folgt aussieht:

:::image type="content" source="media/create-app-visual-studio/vs-form-preview.png" alt-text="Visual Studio 2019-Designer mit dem geöffneten Formular für Windows Forms für .NET":::

## <a name="handle-events"></a>Behandeln von Ereignissen

Wenn das Formular über alle Steuerelemente verfügt, müssen Sie die Verarbeitung der dazugehörigen Ereignisse konfigurieren, damit Ihre App auf Benutzereingaben reagieren kann. Führen Sie die folgenden Schritte aus, wobei der Formular-Designer weiterhin geöffnet bleibt:

01. Klicken Sie auf das Schaltflächen-Steuerelement im Formular.
01. Klicken Sie im Bereich **Eigenschaften** auf das Ereignissymbol :::image type="icon" source="media/create-app-visual-studio/icon-events.png" border="false":::, um die Ereignisse der Schaltfläche aufzulisten.
01. Suchen Sie nach dem **Click**-Ereignis, und doppelklicken Sie darauf, um einen Ereignishandler zu erzeugen.

    Durch diese Aktion wird dem Formular der folgende Code hinzugefügt:

    ```csharp
    private void btnAdd_Click(object sender, EventArgs e)
    {

    }
    ```

    ```vb
    Private Sub btnAdd_Click(sender As Object, e As EventArgs) Handles btnAdd.Click

    End Sub
    ```

    Der Code, den Sie in diesen Handler einfügen, fügt dem `lstNames`-Listensteuerelement den Namen hinzu, der im `txtName`-Textsteuerelement angegeben ist. Für das Hinzufügen des Namens sollen jedoch zwei Bedingungen gelten: der angegebene Name darf nicht leer sein, und der Name darf noch nicht vorhanden sein.

01. Im folgenden Code wird veranschaulicht, wie dem `lstNames`-Steuerelement ein Name hinzugefügt wird:

    ```csharp
    private void btnAdd_Click(object sender, EventArgs e)
    {
        if (!string.IsNullOrWhiteSpace(txtName.Text) && !lstNames.Items.Contains(txtName.Text))
            lstNames.Items.Add(txtName.Text);
    }
    ```

    ```vb
    Private Sub btnAdd_Click(sender As Object, e As EventArgs) Handles btnAdd.Click
        If Not String.IsNullOrWhiteSpace(txtName.Text) And Not lstNames.Items.Contains(txtName.Text) Then
            lstNames.Items.Add(txtName.Text)
        End If
    End Sub
    ```

## <a name="run-the-app"></a>Ausführen der App

Nachdem das Ereignis programmiert wurde, können Sie die App ausführen, indem Sie auf <kbd>F5</kbd> drücken oder im Menü auf **Debuggen** > **Debuggen starten** klicken. Das Formular wird angezeigt, und Sie können einen Namen in das Textfeld eingeben und diesen durch Klicken auf die Schaltfläche hinzufügen.

:::image type="content" source="media/create-app-visual-studio/app-running.png" alt-text="Ausführen einer Windows Forms-App für .NET":::

## <a name="next-steps"></a>Nächste Schritte

> [!div class="nextstepaction"]
> [Weitere Informationen zu Windows Forms](../overview/index.md)
