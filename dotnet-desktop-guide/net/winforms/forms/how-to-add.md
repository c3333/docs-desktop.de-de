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
# <a name="how-to-add-a-form-to-a-project-windows-forms-net"></a><span data-ttu-id="58925-103">Hinzufügen eines Formulars zu einem Projekt (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="58925-103">How to add a form to a project (Windows Forms .NET)</span></span>

<span data-ttu-id="58925-104">Fügen Sie Ihrem Projekt mit Visual Studio Formulare hinzu.</span><span class="sxs-lookup"><span data-stu-id="58925-104">Add forms to your project with Visual Studio.</span></span> <span data-ttu-id="58925-105">Wenn Ihre App über mehrere Formulare verfügt, können Sie auswählen, welches das Startformular für Ihre App ist, und Sie können mehrere Formulare gleichzeitig anzeigen.</span><span class="sxs-lookup"><span data-stu-id="58925-105">When your app has multiple forms, you can choose which is the startup form for your app, and you can display multiple forms at the same time.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="add-a-new-form"></a><span data-ttu-id="58925-106">Hinzufügen eines neuen Formulars</span><span class="sxs-lookup"><span data-stu-id="58925-106">Add a new form</span></span>

<span data-ttu-id="58925-107">Fügen Sie mit Visual Studio ein neues Formular hinzu.</span><span class="sxs-lookup"><span data-stu-id="58925-107">Add a new form with Visual Studio.</span></span>

01. <span data-ttu-id="58925-108">Suchen Sie in Visual Studio nach dem Bereich **Projektmappen-Explorer**.</span><span class="sxs-lookup"><span data-stu-id="58925-108">In Visual Studio, find the **Project Explorer** pane.</span></span> <span data-ttu-id="58925-109">Klicken Sie mit der rechten Maustaste auf das Projekt und dann auf **Hinzufügen** > **Formular (Windows Forms)** .</span><span class="sxs-lookup"><span data-stu-id="58925-109">Right-click on the project and choose **Add** > **Form (Windows Forms)**.</span></span>

    :::image type="content" source="media/how-to-add/right-click.png" alt-text="Rechtsklick auf den Projektmappen-Explorer, um dem Windows Forms-Projekt ein neues Formular hinzuzufügen":::

01. <span data-ttu-id="58925-111">Geben Sie im Feld **Name** einen Namen für das Formular ein (z. B. *MyNewForm*).</span><span class="sxs-lookup"><span data-stu-id="58925-111">In the **Name** box, type a name for your form, such as *MyNewForm*.</span></span> <span data-ttu-id="58925-112">Visual Studio stellt einen eindeutigen Standardnamen bereit, den Sie verwenden können.</span><span class="sxs-lookup"><span data-stu-id="58925-112">Visual Studio will provide a default and unique name that you may use.</span></span>

    :::image type="content" source="media/how-to-add/new-form-dialog.png" alt-text="Dialogfeld „Hinzufügen“ in Visual Studio für Windows Forms":::

<span data-ttu-id="58925-114">Nachdem das Formular hinzugefügt wurde, öffnet Visual Studio den Formular-Designer für das Formular.</span><span class="sxs-lookup"><span data-stu-id="58925-114">Once the form has been added, Visual Studio opens the form designer for the form.</span></span>

## <a name="add-a-project-reference-to-a-form"></a><span data-ttu-id="58925-115">Hinzufügen eines Projektverweises zu einem Formular</span><span class="sxs-lookup"><span data-stu-id="58925-115">Add a project reference to a form</span></span>

<span data-ttu-id="58925-116">Wenn Sie über die Quelldateien für ein Formular verfügen, können Sie das Formular dem Projekt hinzufügen, indem Sie die Dateien in den gleichen Ordner kopieren, in dem sich das Projekt befindet.</span><span class="sxs-lookup"><span data-stu-id="58925-116">If you have the source files to a form, you can add the form to your project by copying the files into the same folder as your project.</span></span> <span data-ttu-id="58925-117">Das Projekt verweist automatisch auf alle Codedateien, die sich im selben Ordner oder untergeordneten Ordner Ihres Projekts befinden.</span><span class="sxs-lookup"><span data-stu-id="58925-117">The project automatically references any code files that are in the same folder or child folder of your project.</span></span>

<span data-ttu-id="58925-118">Formulare bestehen aus zwei Dateien, die denselben Namen haben: _form2.cs_ (_form2_ ist ein Beispiel für einen Dateinamen) und _form2.Designer.cs_.</span><span class="sxs-lookup"><span data-stu-id="58925-118">Forms are made up of two files that share the same name: _form2.cs_ (_form2_ being an example of a file name) and _form2.Designer.cs_.</span></span> <span data-ttu-id="58925-119">Manchmal gibt es eine Ressourcendatei, die denselben Namen hat (_form2.resx_).</span><span class="sxs-lookup"><span data-stu-id="58925-119">Sometimes a resource file exists, sharing the same name, _form2.resx_.</span></span> <span data-ttu-id="58925-120">Im vorherigen Beispiel stellt _form2_ den Basisdateinamen dar.</span><span class="sxs-lookup"><span data-stu-id="58925-120">In in the previous example, _form2_ represents the base file name.</span></span> <span data-ttu-id="58925-121">Sie müssen alle zugehörigen Dateien in den Projektordner kopieren.</span><span class="sxs-lookup"><span data-stu-id="58925-121">You'll want to copy all related files to your project folder.</span></span>

<span data-ttu-id="58925-122">Alternativ können Sie Visual Studio verwenden, um eine Datei in das Projekt zu importieren.</span><span class="sxs-lookup"><span data-stu-id="58925-122">Alternatively, you can use Visual Studio to import a file into your project.</span></span> <span data-ttu-id="58925-123">Wenn Sie dem Projekt eine vorhandene Datei hinzufügen, wird die Datei in denselben Ordner wie das Projekt kopiert.</span><span class="sxs-lookup"><span data-stu-id="58925-123">When you add an existing file to your project, the file is copied into the same folder as your project.</span></span>

01. <span data-ttu-id="58925-124">Suchen Sie in Visual Studio nach dem Bereich **Projektmappen-Explorer**.</span><span class="sxs-lookup"><span data-stu-id="58925-124">In Visual Studio, find the **Project Explorer** pane.</span></span> <span data-ttu-id="58925-125">Klicken Sie dann mit der rechten Maustaste auf das Projekt und dann auf **Hinzufügen** > **Vorhandenes Element**.</span><span class="sxs-lookup"><span data-stu-id="58925-125">Right-click on the project and choose **Add** > **Existing Item**.</span></span>

    :::image type="content" source="media/how-to-add/existing-right-click.png" alt-text="Klicken mit der rechten Maustaste auf den Projektmappen-Explorer zum Hinzufügen eines vorhandenen Formulars zum Windows Forms-Projekt":::

02. <span data-ttu-id="58925-127">Wechseln Sie zu dem Ordner, der die Formulardateien enthält.</span><span class="sxs-lookup"><span data-stu-id="58925-127">Navigate to the folder containing your form files.</span></span>

03. <span data-ttu-id="58925-128">Wählen Sie die _form2.cs_-Datei aus, wobei _form2_ der Basisdateiname der zugehörigen Formulardateien ist.</span><span class="sxs-lookup"><span data-stu-id="58925-128">Select the _form2.cs_ file, where _form2_ is the base file name of the related form files.</span></span> <span data-ttu-id="58925-129">Wählen Sie die anderen Dateien (z. B _form2.Designer.cs_) nicht aus.</span><span class="sxs-lookup"><span data-stu-id="58925-129">Don't select the other files, such as _form2.Designer.cs_.</span></span>

## <a name="see-also"></a><span data-ttu-id="58925-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58925-130">See also</span></span>

- [<span data-ttu-id="58925-131">Festlegen der Position und Größe eines Formulars (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="58925-131">How to position and size a form (Windows Forms .NET)</span></span>](how-to-position-and-resize.md)
- [<span data-ttu-id="58925-132">Übersicht über Ereignisse (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="58925-132">Events overview (Windows Forms .NET)</span></span>](events.md)
- [<span data-ttu-id="58925-133">Position und Layout von Steuerelementen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="58925-133">Position and layout of controls (Windows Forms .NET)</span></span>](../controls/layout.md)
