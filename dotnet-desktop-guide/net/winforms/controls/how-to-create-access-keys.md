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
# <a name="add-an-access-key-shortcut-to-a-control-windows-forms-net"></a><span data-ttu-id="83d3a-103">Hinzufügen einer Zugriffstastenverknüpfung zu einem Steuerelement (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="83d3a-103">Add an access key shortcut to a control (Windows Forms .NET)</span></span>

<span data-ttu-id="83d3a-104">Eine *Zugriffstaste* ist ein unterstrichenes Zeichen im Text eines Menüs, Menüelements oder in der Bezeichnung eines Steuerelements wie einer Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="83d3a-104">An *access key* is an underlined character in the text of a menu, menu item, or the label of a control such as a button.</span></span> <span data-ttu-id="83d3a-105">Mit einer Zugriffstaste kann der Benutzer auf eine Schaltfläche „klicken“, indem er die Taste <kbd>ALT</kbd> in Kombination mit der vordefinierten Zugriffstaste drückt.</span><span class="sxs-lookup"><span data-stu-id="83d3a-105">With an access key, the user can "click" a button by pressing the <kbd>Alt</kbd> key in combination with the predefined access key.</span></span> <span data-ttu-id="83d3a-106">Wenn eine Schaltfläche beispielsweise eine Prozedur ausführt, um ein Formular zu drucken, und deshalb die dazugehörige `Text`-Eigenschaft auf „Print“ festgelegt ist, führt ein Hinzufügen eines Et-Zeichens (&) vor dem Buchstaben „P“ dazu, dass der Buchstabe „P“ zur Laufzeit im Schaltflächentext unterstrichen ist.</span><span class="sxs-lookup"><span data-stu-id="83d3a-106">For example, if a button runs a procedure to print a form, and therefore its `Text` property is set to "Print," adding an ampersand (&) before the letter "P" causes the letter "P" to be underlined in the button text at run time.</span></span> <span data-ttu-id="83d3a-107">Der Benutzer kann den der Schaltfläche zugeordneten Befehl ausführen, indem er <kbd>ALT</kbd> drückt.</span><span class="sxs-lookup"><span data-stu-id="83d3a-107">The user can run the command associated with the button by pressing <kbd>Alt</kbd>.</span></span>

<span data-ttu-id="83d3a-108">Steuerelemente, die nicht fokussiert werden können, können mit Ausnahme von Bezeichnungssteuerelementen keine Zugriffstasten haben.</span><span class="sxs-lookup"><span data-stu-id="83d3a-108">Controls that cannot receive focus can't have access keys, except label controls.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="designer"></a><span data-ttu-id="83d3a-109">Designer</span><span class="sxs-lookup"><span data-stu-id="83d3a-109">Designer</span></span>

<span data-ttu-id="83d3a-110">Legen Sie im Fenster **Eigenschaften** in Visual Studio die Eigenschaft **Text** auf eine Zeichenfolge fest, die ein Et-Zeichen (&) vor dem Buchstaben enthält, der Zugriffstaste sein wird.</span><span class="sxs-lookup"><span data-stu-id="83d3a-110">In the **Properties** window of Visual Studio, set the **Text** property to a string that includes an ampersand (&) before the letter that will be the access key.</span></span> <span data-ttu-id="83d3a-111">Wenn Sie beispielsweise den Buchstaben „P“ als Zugriffstaste festlegen möchten, geben Sie **&Print** ein.</span><span class="sxs-lookup"><span data-stu-id="83d3a-111">For example, to set the letter "P" as the access key, enter **&Print**.</span></span>

:::image type="content" source="media/how-to-create-access-keys/properties-text.png" alt-text="Dialogfeld „Eigenschaften“ mit ausgewählter Eigenschaft „Text“ und Zugriffstaste":::

## <a name="programmatic"></a><span data-ttu-id="83d3a-113">Programmgesteuert</span><span class="sxs-lookup"><span data-stu-id="83d3a-113">Programmatic</span></span>

<span data-ttu-id="83d3a-114">Legen Sie die `Text`-Eigenschaft auf eine Zeichenfolge fest, die ein Et-Zeichen (&) vor dem Buchstaben enthält, der Verknüpfung sein wird.</span><span class="sxs-lookup"><span data-stu-id="83d3a-114">Set the `Text` property to a string that includes an ampersand (&) before the letter that will be the shortcut.</span></span>

```vb
' Set the letter "P" as an access key.
Button1.Text = "&Print"
```

```csharp
// Set the letter "P" as an access key.
button1.Text = "&Print";
```

## <a name="use-a-label-to-focus-a-control"></a><span data-ttu-id="83d3a-115">Verwenden einer Bezeichnung als Fokus für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="83d3a-115">Use a label to focus a control</span></span>

<span data-ttu-id="83d3a-116">Obwohl eine Bezeichnung nicht fokussiert werden kann, besteht die Möglichkeit, das nächste Steuerelement in der Aktivierreihenfolge des Formulars in den Fokus zu nehmen.</span><span class="sxs-lookup"><span data-stu-id="83d3a-116">Even though a label cannot be focused, it has the ability to focus the next control in the tab order of the form.</span></span> <span data-ttu-id="83d3a-117">Jedem Steuerelement wird in der <xref:System.Windows.Forms.Control.TabIndex>-Eigenschaft ein Wert zugewiesen, in der Regel in aufsteigender Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="83d3a-117">Each control is assigned a value to the <xref:System.Windows.Forms.Control.TabIndex> property, generally in ascending sequential order.</span></span> <span data-ttu-id="83d3a-118">Wenn die Zugriffstaste der Eigenschaft [Label.Text](xref:System.Windows.Forms.Label.Text) zugewiesen wird, wird der Fokus auf das nächste Steuerelement in Aktivierreihenfolge gelegt.</span><span class="sxs-lookup"><span data-stu-id="83d3a-118">When the access key is assigned to the [Label.Text](xref:System.Windows.Forms.Label.Text) property, the next control in the sequential tab order is focused.</span></span>

<span data-ttu-id="83d3a-119">Für das Beispiel im Abschnitt [Programmgesteuert](#programmatic) könnten Sie eine Bezeichnung verwenden, um den Fokus auf die Schaltfläche zu legen, wenn für die Schaltfläche kein Text festgelegt wäre, sondern stattdessen ein Bild eines Druckers angezeigt würde.</span><span class="sxs-lookup"><span data-stu-id="83d3a-119">Using the example from the [Programmatic](#programmatic) section, if the button didn't have any text set, but instead presented an image of a printer, you could use a label to focus the button.</span></span>

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

## <a name="display-an-ampersand"></a><span data-ttu-id="83d3a-120">Anzeigen eines Et-Zeichens</span><span class="sxs-lookup"><span data-stu-id="83d3a-120">Display an ampersand</span></span>

<span data-ttu-id="83d3a-121">Wenn Sie den Text oder die Beschriftung für ein Steuerelement festlegen, das ein Et-Zeichen (&) als Zugriffstaste interpretiert, verwenden Sie zwei aufeinander folgende Et-Zeichen (&&), damit ein einzelnes Et-Zeichen angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="83d3a-121">When setting the text or caption of a control that interprets an ampersand (&) as an access key, use two consecutive ampersands (&&) to display a single ampersand.</span></span> <span data-ttu-id="83d3a-122">Wenn der Text einer Schaltfläche beispielsweise auf `"Print && Close"` festgelegt wird, wird in der Beschriftung für `Print & Close` Folgendes angezeigt:</span><span class="sxs-lookup"><span data-stu-id="83d3a-122">For example, the text of a button set to `"Print && Close"` displays in the caption of `Print & Close`:</span></span>

```vb
' Set the letter "P" as an access key.
Button1.Text = "Print && Close"
```

```csharp
// Set the letter "P" as an access key.
button1.Text = "Print && Close";
```

:::image type="content" source="media/how-to-create-access-keys/double-ampersand.png" alt-text="Anzeige eines Et-Zeichens auf einer Schaltfläche":::

## <a name="see-also"></a><span data-ttu-id="83d3a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83d3a-124">See also</span></span>

- [<span data-ttu-id="83d3a-125">Vorgehensweise: Festlegen des durch ein Windows Forms-Steuerelement angezeigten Texts</span><span class="sxs-lookup"><span data-stu-id="83d3a-125">How to: Set the text displayed by a Windows Forms control</span></span>](how-to-set-the-display-text.md)
- <xref:System.Windows.Forms.Button>
- <xref:System.Windows.Forms.Label>
