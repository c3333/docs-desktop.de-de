---
title: Festlegen des von einem Steuerelement angezeigten Texts
description: Hier erfahren Sie, wie Sie den von einem Windows Forms-Steuerelement angezeigten Text festlegen. Legen Sie den Text mithilfe der Text-Eigenschaft fest, oder geben Sie ihn damit zurück. Außerdem können Sie die Schriftart mithilfe der Font-Eigenschaft ändern.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms, captions
- Button control [Windows Forms], button text
- StdFont object and CommandButton caption
- captions [Windows Forms], Windows Forms controls
- Text property [Windows Forms], Windows Forms control
- Button control [Windows Forms], text display
- labels [Windows Forms], adding to CommandButton control
- buttons [Windows Forms], text
- captions [Windows Forms], setting
- text
- examples [Windows Forms], controls
- text [Windows Forms], Windows Forms controls
- controls [Windows Forms], captions
- forms [Windows Forms], captions
ms.openlocfilehash: 2fd5a62310ae5e7d6e0528c7f12f37ed40f8a626
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942046"
---
# <a name="how-to-set-the-text-displayed-by-a-control-windows-forms-net"></a>Vorgehensweise: Festlegen des durch ein Steuerelement angezeigten Texts (Windows Forms .NET)

Windows Forms-Steuerelemente zeigen in der Regel Text an, der mit der Hauptfunktion des Steuerelements zusammenhängt. Beispielsweise zeigt ein <xref:System.Windows.Forms.Button>-Steuerelement in der Regel einen Beschriftungstext an, der auf die Aktion hinweist, die beim Klicken auf die Schaltfläche ausgeführt wird. Bei allen Steuerelementen können Sie den Text mithilfe der <xref:System.Windows.Forms.Control.Text%2A>-Eigenschaft festlegen oder zurückgeben. Sie können die Schriftart ändern, indem Sie die <xref:System.Windows.Forms.Control.Font%2A>-Eigenschaft verwenden.

Sie können den Text aber auch mithilfe des [Designers](#designer) festlegen.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="designer"></a>Designer

01. Legen Sie im Fenster **Eigenschaften** in Visual Studio die **Text**-Eigenschaft des Steuerelements auf eine entsprechende Zeichenfolge fest.

    Wenn Sie eine unterstrichene Tastenkombination erstellen möchten, setzen Sie ein Und-Zeichen (&) vor den Buchstaben der Tastenkombination.

    :::image type="content" source="media/how-to-set-the-text-displayed-by-a-windows-forms-control/properties-text.png" alt-text="Visual Studio-Bereich „Eigenschaften“ in Windows Forms für .NET mit angezeigter Text-Eigenschaft":::

01. Klicken Sie im Fenster **Eigenschaften** auf die Schaltfläche mit den Auslassungspunkten (![Schaltfläche mit Auslassungspunkten (...) im Eigenschaftenfenster von Visual Studio](../media/visual-studio-ellipsis-button.png)) neben der Eigenschaft **Font**.

    :::image type="content" source="media/how-to-set-the-text-displayed-by-a-windows-forms-control/properties-font.png" alt-text="Visual Studio-Bereich „Eigenschaften“ in Windows Forms für .NET mit angezeigter Font-Eigenschaft":::

    Passen Sie im Dialogfeld für die Standardschriftart die Schriftart mit Einstellungen für den Typ, die Größe und den Stil an.

    :::image type="content" source="media/how-to-set-the-text-displayed-by-a-windows-forms-control/font-window.png" alt-text="Visual Studio-Bereich „Eigenschaften“ in Windows Forms für .NET mit Fenster für die Einstellungen der Schrift":::

## <a name="programmatic"></a>Programmgesteuert

01. Legen Sie für die <xref:System.Windows.Forms.Control.Text%2A>-Eigenschaft eine Zeichenfolge fest.

    Wenn Sie eine unterstrichene Zugriffstaste erstellen möchten, setzen Sie ein Und-Zeichen (&) vor den Buchstaben der Zugriffstaste.

01. Legen Sie die <xref:System.Windows.Forms.Control.Font%2A>-Eigenschaft auf ein Objekt des Typs <xref:System.Drawing.Font> fest.

    ```vb
    Button1.Text = "Click here to save changes"
    Button1.Font = New Font("Arial", 10, FontStyle.Bold, GraphicsUnit.Point)
    ```

    ```csharp
    button1.Text = "Click here to save changes";
    button1.Font = new Font("Arial", 10, FontStyle.Bold, GraphicsUnit.Point);
    ```

    > [!NOTE]
    > Mit einem Escapezeichen können Sie ein Sonderzeichen in Benutzeroberflächenelementen anzeigen, das diese normalerweise anders interpretieren würde, z. B. Menüelemente. Mit der folgenden Codezeile wird der Text des Menüelements beispielsweise wie folgt festgelegt: "& Now For Something Completely Different":

    ```vb
    MPMenuItem.Text = "&& Now For Something Completely Different"
    ```

    ```csharp
    mpMenuItem.Text = "&& Now For Something Completely Different";
    ```

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Control.Text%2A?displayProperty=nameWithType>
- [Gewusst wie: Erstellen von Zugriffstasten für Windows Forms-Steuerelemente](how-to-create-access-keys.md)
