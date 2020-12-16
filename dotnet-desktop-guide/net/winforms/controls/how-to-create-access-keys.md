---
title: Erstellen von Zugriffstasten für Steuerelemente
description: In diesem Artikel erfahren Sie, wie Sie eine Zugriffstastenverknüpfung für ein Steuerelement oder eine Bezeichnung in Windows Forms für .NET festlegen.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms], access keys
- Button control [Windows Forms], access keys
- dialog box controls [Windows Forms], mnemonics
- access keys [Windows Forms], creating for controls
- mnemonics
- ampersand character in shortcut key
- Windows Forms controls, access keys
- examples [Windows Forms], controls
- Text property [Windows Forms], specifying access keys for controls
- keyboard shortcuts [Windows Forms], creating for controls
- access keys [Windows Forms], Windows Forms
- ALT key
ms.openlocfilehash: 4d746082ffbaa749b882dcb1a769b5f9541c6fe8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942122"
---
# <a name="add-an-access-key-shortcut-to-a-control-windows-forms-net"></a>Hinzufügen einer Zugriffstastenverknüpfung zu einem Steuerelement (Windows Forms .NET)

Eine *Zugriffstaste* ist ein unterstrichenes Zeichen im Text eines Menüs, Menüelements oder in der Bezeichnung eines Steuerelements wie einer Schaltfläche. Mit einer Zugriffstaste kann der Benutzer auf eine Schaltfläche „klicken“, indem er die Taste <kbd>ALT</kbd> in Kombination mit der vordefinierten Zugriffstaste drückt. Wenn eine Schaltfläche beispielsweise eine Prozedur ausführt, um ein Formular zu drucken, und deshalb die dazugehörige `Text`-Eigenschaft auf „Print“ festgelegt ist, führt ein Hinzufügen eines Et-Zeichens (&) vor dem Buchstaben „P“ dazu, dass der Buchstabe „P“ zur Laufzeit im Schaltflächentext unterstrichen ist. Der Benutzer kann den der Schaltfläche zugeordneten Befehl ausführen, indem er <kbd>ALT</kbd> drückt.

Steuerelemente, die nicht fokussiert werden können, können mit Ausnahme von Bezeichnungssteuerelementen keine Zugriffstasten haben.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="designer"></a>Designer

Legen Sie im Fenster **Eigenschaften** in Visual Studio die Eigenschaft **Text** auf eine Zeichenfolge fest, die ein Et-Zeichen (&) vor dem Buchstaben enthält, der Zugriffstaste sein wird. Wenn Sie beispielsweise den Buchstaben „P“ als Zugriffstaste festlegen möchten, geben Sie **&Print** ein.

:::image type="content" source="media/how-to-create-access-keys/properties-text.png" alt-text="Dialogfeld „Eigenschaften“ mit ausgewählter Eigenschaft „Text“ und Zugriffstaste":::

## <a name="programmatic"></a>Programmgesteuert

Legen Sie die `Text`-Eigenschaft auf eine Zeichenfolge fest, die ein Et-Zeichen (&) vor dem Buchstaben enthält, der Verknüpfung sein wird.

```vb
' Set the letter "P" as an access key.
Button1.Text = "&Print"
```

```csharp
// Set the letter "P" as an access key.
button1.Text = "&Print";
```

## <a name="use-a-label-to-focus-a-control"></a>Verwenden einer Bezeichnung als Fokus für ein Steuerelement

Obwohl eine Bezeichnung nicht fokussiert werden kann, besteht die Möglichkeit, das nächste Steuerelement in der Aktivierreihenfolge des Formulars in den Fokus zu nehmen. Jedem Steuerelement wird in der <xref:System.Windows.Forms.Control.TabIndex>-Eigenschaft ein Wert zugewiesen, in der Regel in aufsteigender Reihenfolge. Wenn die Zugriffstaste der Eigenschaft [Label.Text](xref:System.Windows.Forms.Label.Text) zugewiesen wird, wird der Fokus auf das nächste Steuerelement in Aktivierreihenfolge gelegt.

Für das Beispiel im Abschnitt [Programmgesteuert](#programmatic) könnten Sie eine Bezeichnung verwenden, um den Fokus auf die Schaltfläche zu legen, wenn für die Schaltfläche kein Text festgelegt wäre, sondern stattdessen ein Bild eines Druckers angezeigt würde.

```vb
' Set the letter "P" as an access key.
Label1.Text = "&Print"
Label1.TabIndex = 9
Button1.TabIndex = 10
```

```csharp
// Set the letter "P" as an access key.
label1.Text = "&Print";
label1.TabIndex = 9
button1.TabIndex = 10
```

## <a name="display-an-ampersand"></a>Anzeigen eines Et-Zeichens

Wenn Sie den Text oder die Beschriftung für ein Steuerelement festlegen, das ein Et-Zeichen (&) als Zugriffstaste interpretiert, verwenden Sie zwei aufeinander folgende Et-Zeichen (&&), damit ein einzelnes Et-Zeichen angezeigt wird. Wenn der Text einer Schaltfläche beispielsweise auf `"Print && Close"` festgelegt wird, wird in der Beschriftung für `Print & Close` Folgendes angezeigt:

```vb
' Set the letter "P" as an access key.
Button1.Text = "Print && Close"
```

```csharp
// Set the letter "P" as an access key.
button1.Text = "Print && Close";
```

:::image type="content" source="media/how-to-create-access-keys/double-ampersand.png" alt-text="Anzeige eines Et-Zeichens auf einer Schaltfläche":::

## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Festlegen des durch ein Windows Forms-Steuerelement angezeigten Texts](how-to-set-the-display-text.md)
- <xref:System.Windows.Forms.Button>
- <xref:System.Windows.Forms.Label>
