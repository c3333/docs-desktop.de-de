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
# <a name="how-to-set-the-text-displayed-by-a-control-windows-forms-net"></a><span data-ttu-id="d00ed-104">Vorgehensweise: Festlegen des durch ein Steuerelement angezeigten Texts (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="d00ed-104">How to: Set the text displayed by a control (Windows Forms .NET)</span></span>

<span data-ttu-id="d00ed-105">Windows Forms-Steuerelemente zeigen in der Regel Text an, der mit der Hauptfunktion des Steuerelements zusammenhängt.</span><span class="sxs-lookup"><span data-stu-id="d00ed-105">Windows Forms controls usually display some text that's related to the primary function of the control.</span></span> <span data-ttu-id="d00ed-106">Beispielsweise zeigt ein <xref:System.Windows.Forms.Button>-Steuerelement in der Regel einen Beschriftungstext an, der auf die Aktion hinweist, die beim Klicken auf die Schaltfläche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d00ed-106">For example, a <xref:System.Windows.Forms.Button> control usually displays a caption indicating what action will be performed if the button is clicked.</span></span> <span data-ttu-id="d00ed-107">Bei allen Steuerelementen können Sie den Text mithilfe der <xref:System.Windows.Forms.Control.Text%2A>-Eigenschaft festlegen oder zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d00ed-107">For all controls, you can set or return the text by using the <xref:System.Windows.Forms.Control.Text%2A> property.</span></span> <span data-ttu-id="d00ed-108">Sie können die Schriftart ändern, indem Sie die <xref:System.Windows.Forms.Control.Font%2A>-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="d00ed-108">You can change the font by using the <xref:System.Windows.Forms.Control.Font%2A> property.</span></span>

<span data-ttu-id="d00ed-109">Sie können den Text aber auch mithilfe des [Designers](#designer) festlegen.</span><span class="sxs-lookup"><span data-stu-id="d00ed-109">You can also set the text by using the [designer](#designer).</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="designer"></a><span data-ttu-id="d00ed-110">Designer</span><span class="sxs-lookup"><span data-stu-id="d00ed-110">Designer</span></span>

01. <span data-ttu-id="d00ed-111">Legen Sie im Fenster **Eigenschaften** in Visual Studio die **Text**-Eigenschaft des Steuerelements auf eine entsprechende Zeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="d00ed-111">In the **Properties** window in Visual Studio, set the **Text** property of the control to an appropriate string.</span></span>

    <span data-ttu-id="d00ed-112">Wenn Sie eine unterstrichene Tastenkombination erstellen möchten, setzen Sie ein Und-Zeichen (&) vor den Buchstaben der Tastenkombination.</span><span class="sxs-lookup"><span data-stu-id="d00ed-112">To create an underlined shortcut key, include an ampersand (&) before the letter that will be the shortcut key.</span></span>

    :::image type="content" source="media/how-to-set-the-text-displayed-by-a-windows-forms-control/properties-text.png" alt-text="Visual Studio-Bereich „Eigenschaften“ in Windows Forms für .NET mit angezeigter Text-Eigenschaft":::

01. <span data-ttu-id="d00ed-114">Klicken Sie im Fenster **Eigenschaften** auf die Schaltfläche mit den Auslassungspunkten (![Schaltfläche mit Auslassungspunkten (...) im Eigenschaftenfenster von Visual Studio](../media/visual-studio-ellipsis-button.png)) neben der Eigenschaft **Font**.</span><span class="sxs-lookup"><span data-stu-id="d00ed-114">In the **Properties** window, select the ellipsis button (![Ellipsis button (...) in the Properties window of Visual Studio](../media/visual-studio-ellipsis-button.png)) next to the **Font** property.</span></span>

    :::image type="content" source="media/how-to-set-the-text-displayed-by-a-windows-forms-control/properties-font.png" alt-text="Visual Studio-Bereich „Eigenschaften“ in Windows Forms für .NET mit angezeigter Font-Eigenschaft":::

    <span data-ttu-id="d00ed-116">Passen Sie im Dialogfeld für die Standardschriftart die Schriftart mit Einstellungen für den Typ, die Größe und den Stil an.</span><span class="sxs-lookup"><span data-stu-id="d00ed-116">In the standard font dialog box, adjust the font with settings such as type, size, and style.</span></span>

    :::image type="content" source="media/how-to-set-the-text-displayed-by-a-windows-forms-control/font-window.png" alt-text="Visual Studio-Bereich „Eigenschaften“ in Windows Forms für .NET mit Fenster für die Einstellungen der Schrift":::

## <a name="programmatic"></a><span data-ttu-id="d00ed-118">Programmgesteuert</span><span class="sxs-lookup"><span data-stu-id="d00ed-118">Programmatic</span></span>

01. <span data-ttu-id="d00ed-119">Legen Sie für die <xref:System.Windows.Forms.Control.Text%2A>-Eigenschaft eine Zeichenfolge fest.</span><span class="sxs-lookup"><span data-stu-id="d00ed-119">Set the <xref:System.Windows.Forms.Control.Text%2A> property to a string.</span></span>

    <span data-ttu-id="d00ed-120">Wenn Sie eine unterstrichene Zugriffstaste erstellen möchten, setzen Sie ein Und-Zeichen (&) vor den Buchstaben der Zugriffstaste.</span><span class="sxs-lookup"><span data-stu-id="d00ed-120">To create an underlined access key, include an ampersand (&) before the letter that will be the access key.</span></span>

01. <span data-ttu-id="d00ed-121">Legen Sie die <xref:System.Windows.Forms.Control.Font%2A>-Eigenschaft auf ein Objekt des Typs <xref:System.Drawing.Font> fest.</span><span class="sxs-lookup"><span data-stu-id="d00ed-121">Set the <xref:System.Windows.Forms.Control.Font%2A> property to an object of type <xref:System.Drawing.Font>.</span></span>

    ```vb
    Button1.Text = "Click here to save changes"
    Button1.Font = New Font("Arial", 10, FontStyle.Bold, GraphicsUnit.Point)
    ```

    ```csharp
    button1.Text = "Click here to save changes";
    button1.Font = new Font("Arial", 10, FontStyle.Bold, GraphicsUnit.Point);
    ```

    > [!NOTE]
    > <span data-ttu-id="d00ed-122">Mit einem Escapezeichen können Sie ein Sonderzeichen in Benutzeroberflächenelementen anzeigen, das diese normalerweise anders interpretieren würde, z. B. Menüelemente.</span><span class="sxs-lookup"><span data-stu-id="d00ed-122">You can use an escape character to display a special character in user-interface elements that would normally interpret them differently, such as menu items.</span></span> <span data-ttu-id="d00ed-123">Mit der folgenden Codezeile wird der Text des Menüelements beispielsweise wie folgt festgelegt: "& Now For Something Completely Different":</span><span class="sxs-lookup"><span data-stu-id="d00ed-123">For example, the following line of code sets the menu item's text to read "& Now For Something Completely Different":</span></span>

    ```vb
    MPMenuItem.Text = "&& Now For Something Completely Different"
    ```

    ```csharp
    mpMenuItem.Text = "&& Now For Something Completely Different";
    ```

## <a name="see-also"></a><span data-ttu-id="d00ed-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d00ed-124">See also</span></span>

- <xref:System.Windows.Forms.Control.Text%2A?displayProperty=nameWithType>
- [<span data-ttu-id="d00ed-125">Gewusst wie: Erstellen von Zugriffstasten für Windows Forms-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d00ed-125">How to: Create Access Keys for Windows Forms Controls</span></span>](how-to-create-access-keys.md)
