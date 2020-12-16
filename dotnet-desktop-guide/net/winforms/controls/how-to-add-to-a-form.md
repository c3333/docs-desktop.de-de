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
# <a name="add-a-control-windows-forms-net"></a><span data-ttu-id="9e637-103">Hinzufügen eines Steuerelements (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="9e637-103">Add a control (Windows Forms .NET)</span></span>

<span data-ttu-id="9e637-104">Die meisten Formulare werden durch das Hinzufügen von Steuerelementen zur Oberfläche des Formulars entworfen, um eine Benutzeroberfläche (UI) zu definieren.</span><span class="sxs-lookup"><span data-stu-id="9e637-104">Most forms are designed by adding controls to the surface of the form to define a user interface (UI).</span></span> <span data-ttu-id="9e637-105">Ein *Steuerelement* ist eine Komponente in einem Formular, das zum Anzeigen von Informationen oder Akzeptieren von Benutzereingaben verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e637-105">A *control* is a component on a form used to display information or accept user input.</span></span><!-- TODO For more information about controls, see [Forms overview](..\forms\overview.md). -->

<span data-ttu-id="9e637-106">Die primäre Methode zum Hinzufügen eines Steuerelements zu einem Formular ist das Verwenden des Visual Studio-Designers, aber Sie können die Steuerelemente für ein Formular zur Laufzeit auch über Code verwalten.</span><span class="sxs-lookup"><span data-stu-id="9e637-106">The primary way a control is added to a form is through the Visual Studio Designer, but you can also manage the controls on a form at run time through code.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="add-with-designer"></a><span data-ttu-id="9e637-107">Hinzufügen mit dem Designer</span><span class="sxs-lookup"><span data-stu-id="9e637-107">Add with Designer</span></span>

<span data-ttu-id="9e637-108">Visual Studio verwendet den Formular-Designer zum Entwerfen von Formularen.</span><span class="sxs-lookup"><span data-stu-id="9e637-108">Visual Studio uses the Forms Designer to design forms.</span></span> <span data-ttu-id="9e637-109">Dort werden im Bereich „Steuerelemente“ alle für Ihre App verfügbaren Steuerelemente aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="9e637-109">There is a Controls pane which lists all the controls available to your app.</span></span> <span data-ttu-id="9e637-110">Sie können Formularen auf zwei Arten Steuerelemente aus dem Bereich hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="9e637-110">You can add controls from the pane in two ways:</span></span>

### <a name="add-the-control-by-double-clicking"></a><span data-ttu-id="9e637-111">Hinzufügen des Steuerelements durch Doppelklicken</span><span class="sxs-lookup"><span data-stu-id="9e637-111">Add the control by double-clicking</span></span>

<span data-ttu-id="9e637-112">Wenn Sie auf ein Steuerelement doppelklicken, wird es mit den Standardeinstellungen automatisch zum aktuell geöffneten Formular hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9e637-112">When a control is double-clicked, it is automatically added to the current open form with default settings.</span></span>

:::image type="content" source="media/how-to-add-to-a-form/toolbox-double-click.gif" alt-text="Doppelklicken auf ein Steuerelement in der Toolbox in Windows Forms für .NET in Visual Studio":::

### <a name="add-the-control-by-drawing"></a><span data-ttu-id="9e637-114">Hinzufügen des Steuerelements durch Zeichnen</span><span class="sxs-lookup"><span data-stu-id="9e637-114">Add the control by drawing</span></span>

<span data-ttu-id="9e637-115">Wählen Sie das Steuerelement aus, indem Sie darauf klicken.</span><span class="sxs-lookup"><span data-stu-id="9e637-115">Select the control by clicking on it.</span></span> <span data-ttu-id="9e637-116">Wählen Sie in Ihrem Formular mithilfe eines Ziehvorgangs einen Bereich aus.</span><span class="sxs-lookup"><span data-stu-id="9e637-116">In your form, drag-select a region.</span></span> <span data-ttu-id="9e637-117">Das Steuerelement wird an die Größe des ausgewählten Bereichs angepasst.</span><span class="sxs-lookup"><span data-stu-id="9e637-117">The control will be placed to fit the size of the region you selected.</span></span>

:::image type="content" source="media/how-to-add-to-a-form/toolbox-drag-draw.gif" alt-text="Auswählen und Ziehen eines Steuerelements aus der Toolbox in Windows Forms für .NET in Visual Studio":::

## <a name="add-with-code"></a><span data-ttu-id="9e637-119">Hinzufügen mit Code</span><span class="sxs-lookup"><span data-stu-id="9e637-119">Add with code</span></span>

<span data-ttu-id="9e637-120">Steuerelemente können erstellt und dann zur Laufzeit mithilfe der <xref:System.Windows.Forms.Control.Controls%2A>-Sammlung des Formulars zu einem Formular hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="9e637-120">Controls can be created and then added to a form at run time with the form's <xref:System.Windows.Forms.Control.Controls%2A> collection.</span></span> <span data-ttu-id="9e637-121">Diese Sammlung kann auch verwendet werden, um Steuerelemente aus einem Formular zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="9e637-121">This collection can also be used to remove controls from a form.</span></span>

<span data-ttu-id="9e637-122">Der folgende Code fügt zwei Steuerelemente ([Label](xref:System.Windows.Forms.Label) und [TextBox](xref:System.Windows.Forms.TextBox)) hinzu und positioniert diese:</span><span class="sxs-lookup"><span data-stu-id="9e637-122">The following code adds and positions two controls, a [Label](xref:System.Windows.Forms.Label) and a [TextBox](xref:System.Windows.Forms.TextBox):</span></span>

:::code language="csharp" source="snippets/how-to-add-to-a-form/cs/Form1.cs" id="CreateControl":::

:::code language="vb" source="snippets/how-to-add-to-a-form/vb/Form1.vb" id="CreateControl":::

## <a name="see-also"></a><span data-ttu-id="9e637-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e637-123">See also</span></span>

- [<span data-ttu-id="9e637-124">Gewusst wie: Festlegen des durch ein Windows Forms-Steuerelement angezeigten Textes</span><span class="sxs-lookup"><span data-stu-id="9e637-124">How to: Set the Text Displayed by a Windows Forms Control</span></span>](how-to-set-the-display-text.md)
- [<span data-ttu-id="9e637-125">Vorgehensweise: Hinzufügen eines Tastenkombinationskurzbefehls zu einem Steuerelement</span><span class="sxs-lookup"><span data-stu-id="9e637-125">How to: Add an access key shortcut to a control</span></span>](how-to-create-access-keys.md)
- <xref:System.Windows.Forms.Label>
- <xref:System.Windows.Forms.TextBox>
- <xref:System.Windows.Forms.Button>
