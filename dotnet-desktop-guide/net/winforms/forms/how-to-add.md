---
title: Hinzufügen eines Formulars zu einem Projekt
description: Hier erfahren Sie mehr über das Hinzufügen eines neuen Formulars zu einem .NET-Windows Forms-Projekt in Visual Studio.
ms.date: 10/26/2020
helpviewer_keywords:
- Windows Forms, create add form
ms.openlocfilehash: fb35c1b62ca0b7a21581c350ddca7f21f45ec27f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942081"
---
# <a name="how-to-add-a-form-to-a-project-windows-forms-net"></a>Hinzufügen eines Formulars zu einem Projekt (Windows Forms .NET)

Fügen Sie Ihrem Projekt mit Visual Studio Formulare hinzu. Wenn Ihre App über mehrere Formulare verfügt, können Sie auswählen, welches das Startformular für Ihre App ist, und Sie können mehrere Formulare gleichzeitig anzeigen.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="add-a-new-form"></a>Hinzufügen eines neuen Formulars

Fügen Sie mit Visual Studio ein neues Formular hinzu.

01. Suchen Sie in Visual Studio nach dem Bereich **Projektmappen-Explorer**. Klicken Sie mit der rechten Maustaste auf das Projekt und dann auf **Hinzufügen** > **Formular (Windows Forms)** .

    :::image type="content" source="media/how-to-add/right-click.png" alt-text="Rechtsklick auf den Projektmappen-Explorer, um dem Windows Forms-Projekt ein neues Formular hinzuzufügen":::

01. Geben Sie im Feld **Name** einen Namen für das Formular ein (z. B. *MyNewForm*). Visual Studio stellt einen eindeutigen Standardnamen bereit, den Sie verwenden können.

    :::image type="content" source="media/how-to-add/new-form-dialog.png" alt-text="Dialogfeld „Hinzufügen“ in Visual Studio für Windows Forms":::

Nachdem das Formular hinzugefügt wurde, öffnet Visual Studio den Formular-Designer für das Formular.

## <a name="add-a-project-reference-to-a-form"></a>Hinzufügen eines Projektverweises zu einem Formular

Wenn Sie über die Quelldateien für ein Formular verfügen, können Sie das Formular dem Projekt hinzufügen, indem Sie die Dateien in den gleichen Ordner kopieren, in dem sich das Projekt befindet. Das Projekt verweist automatisch auf alle Codedateien, die sich im selben Ordner oder untergeordneten Ordner Ihres Projekts befinden.

Formulare bestehen aus zwei Dateien, die denselben Namen haben: _form2.cs_ (_form2_ ist ein Beispiel für einen Dateinamen) und _form2.Designer.cs_. Manchmal gibt es eine Ressourcendatei, die denselben Namen hat (_form2.resx_). Im vorherigen Beispiel stellt _form2_ den Basisdateinamen dar. Sie müssen alle zugehörigen Dateien in den Projektordner kopieren.

Alternativ können Sie Visual Studio verwenden, um eine Datei in das Projekt zu importieren. Wenn Sie dem Projekt eine vorhandene Datei hinzufügen, wird die Datei in denselben Ordner wie das Projekt kopiert.

01. Suchen Sie in Visual Studio nach dem Bereich **Projektmappen-Explorer**. Klicken Sie dann mit der rechten Maustaste auf das Projekt und dann auf **Hinzufügen** > **Vorhandenes Element**.

    :::image type="content" source="media/how-to-add/existing-right-click.png" alt-text="Klicken mit der rechten Maustaste auf den Projektmappen-Explorer zum Hinzufügen eines vorhandenen Formulars zum Windows Forms-Projekt":::

02. Wechseln Sie zu dem Ordner, der die Formulardateien enthält.

03. Wählen Sie die _form2.cs_-Datei aus, wobei _form2_ der Basisdateiname der zugehörigen Formulardateien ist. Wählen Sie die anderen Dateien (z. B _form2.Designer.cs_) nicht aus.

## <a name="see-also"></a>Siehe auch

- [Festlegen der Position und Größe eines Formulars (Windows Forms .NET)](how-to-position-and-resize.md)
- [Übersicht über Ereignisse (Windows Forms .NET)](events.md)
- [Position und Layout von Steuerelementen (Windows Forms .NET)](../controls/layout.md)
