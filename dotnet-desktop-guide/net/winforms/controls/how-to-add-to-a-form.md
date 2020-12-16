---
title: Hinzufügen von Steuerelementen zu einem Formular
description: Hier erfahren Sie, wie Sie einem Formular ein Steuerelement in Windows Forms für .NET hinzufügen.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms controls, adding to form
- controls [Windows Forms], adding
ms.openlocfilehash: 44a20f135eb0f1503a6e5204a33aa8dca092123f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942093"
---
# <a name="add-a-control-windows-forms-net"></a>Hinzufügen eines Steuerelements (Windows Forms .NET)

Die meisten Formulare werden durch das Hinzufügen von Steuerelementen zur Oberfläche des Formulars entworfen, um eine Benutzeroberfläche (UI) zu definieren. Ein *Steuerelement* ist eine Komponente in einem Formular, das zum Anzeigen von Informationen oder Akzeptieren von Benutzereingaben verwendet wird.<!-- TODO For more information about controls, see [Forms overview](..\forms\overview.md). -->

Die primäre Methode zum Hinzufügen eines Steuerelements zu einem Formular ist das Verwenden des Visual Studio-Designers, aber Sie können die Steuerelemente für ein Formular zur Laufzeit auch über Code verwalten.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="add-with-designer"></a>Hinzufügen mit dem Designer

Visual Studio verwendet den Formular-Designer zum Entwerfen von Formularen. Dort werden im Bereich „Steuerelemente“ alle für Ihre App verfügbaren Steuerelemente aufgeführt. Sie können Formularen auf zwei Arten Steuerelemente aus dem Bereich hinzufügen:

### <a name="add-the-control-by-double-clicking"></a>Hinzufügen des Steuerelements durch Doppelklicken

Wenn Sie auf ein Steuerelement doppelklicken, wird es mit den Standardeinstellungen automatisch zum aktuell geöffneten Formular hinzugefügt.

:::image type="content" source="media/how-to-add-to-a-form/toolbox-double-click.gif" alt-text="Doppelklicken auf ein Steuerelement in der Toolbox in Windows Forms für .NET in Visual Studio":::

### <a name="add-the-control-by-drawing"></a>Hinzufügen des Steuerelements durch Zeichnen

Wählen Sie das Steuerelement aus, indem Sie darauf klicken. Wählen Sie in Ihrem Formular mithilfe eines Ziehvorgangs einen Bereich aus. Das Steuerelement wird an die Größe des ausgewählten Bereichs angepasst.

:::image type="content" source="media/how-to-add-to-a-form/toolbox-drag-draw.gif" alt-text="Auswählen und Ziehen eines Steuerelements aus der Toolbox in Windows Forms für .NET in Visual Studio":::

## <a name="add-with-code"></a>Hinzufügen mit Code

Steuerelemente können erstellt und dann zur Laufzeit mithilfe der <xref:System.Windows.Forms.Control.Controls%2A>-Sammlung des Formulars zu einem Formular hinzugefügt werden. Diese Sammlung kann auch verwendet werden, um Steuerelemente aus einem Formular zu entfernen.

Der folgende Code fügt zwei Steuerelemente ([Label](xref:System.Windows.Forms.Label) und [TextBox](xref:System.Windows.Forms.TextBox)) hinzu und positioniert diese:

:::code language="csharp" source="snippets/how-to-add-to-a-form/cs/Form1.cs" id="CreateControl":::

:::code language="vb" source="snippets/how-to-add-to-a-form/vb/Form1.vb" id="CreateControl":::

## <a name="see-also"></a>Siehe auch

- [Gewusst wie: Festlegen des durch ein Windows Forms-Steuerelement angezeigten Textes](how-to-set-the-display-text.md)
- [Vorgehensweise: Hinzufügen eines Tastenkombinationskurzbefehls zu einem Steuerelement](how-to-create-access-keys.md)
- <xref:System.Windows.Forms.Label>
- <xref:System.Windows.Forms.TextBox>
- <xref:System.Windows.Forms.Button>
