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
# <a name="walkthrough-automatically-populating-the-toolbox-with-custom-components"></a><span data-ttu-id="e6fed-102">Exemplarische Vorgehensweise: Automatisches Füllen der Toolbox mit benutzerdefinierten Komponenten</span><span class="sxs-lookup"><span data-stu-id="e6fed-102">Walkthrough: Automatically Populating the Toolbox with Custom Components</span></span>

<span data-ttu-id="e6fed-103">Wenn die Komponenten von einem Projekt in der aktuell geöffneten Projekt Mappe definiert werden, werden Sie automatisch in der **Toolbox** angezeigt, ohne dass eine Aktion durch Sie erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e6fed-103">If your components are defined by a project in the currently open solution, they will automatically appear in the **Toolbox**, with no action required by you.</span></span> <span data-ttu-id="e6fed-104">Sie können die **Toolbox** auch manuell mit den benutzerdefinierten Komponenten auffüllen, indem Sie das [Dialog Feld Toolbox Elemente auswählen (Visual Studio)](/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100))verwenden, aber die **Toolbox** berücksichtigt die Elemente in den Buildausgaben ihrer Projekt Mappe mit den folgenden Merkmalen:</span><span class="sxs-lookup"><span data-stu-id="e6fed-104">You can also manually populate the **Toolbox** with your custom components by using the [Choose Toolbox Items Dialog Box (Visual Studio)](/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100)), but the **Toolbox** takes account of items in your solution's build outputs with all the following characteristics:</span></span>

- <span data-ttu-id="e6fed-105">Implementiert <xref:System.ComponentModel.IComponent> ;</span><span class="sxs-lookup"><span data-stu-id="e6fed-105">Implements <xref:System.ComponentModel.IComponent>;</span></span>

- <span data-ttu-id="e6fed-106">Hat nicht <xref:System.ComponentModel.ToolboxItemAttribute> auf festgelegt `false` .</span><span class="sxs-lookup"><span data-stu-id="e6fed-106">Does not have <xref:System.ComponentModel.ToolboxItemAttribute> set to `false`;</span></span>

- <span data-ttu-id="e6fed-107">Hat nicht <xref:System.ComponentModel.DesignTimeVisibleAttribute> auf festgelegt `false` .</span><span class="sxs-lookup"><span data-stu-id="e6fed-107">Does not have <xref:System.ComponentModel.DesignTimeVisibleAttribute> set to `false`.</span></span>

> [!NOTE]
> <span data-ttu-id="e6fed-108">Die **Toolbox** folgt nicht den Verweis Ketten, sodass keine Elemente angezeigt werden, die nicht von einem Projekt in der Projekt Mappe erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="e6fed-108">The **Toolbox** does not follow reference chains, so it won't display items that are not built by a project in your solution.</span></span>

<span data-ttu-id="e6fed-109">In dieser exemplarischen Vorgehensweise wird veranschaulicht, wie eine benutzerdefinierte Komponente automatisch in der **Toolbox** angezeigt wird, nachdem die Komponente erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e6fed-109">This walkthrough demonstrates how a custom component automatically appears in the **Toolbox** once the component is built.</span></span> <span data-ttu-id="e6fed-110">In dieser exemplarischen Vorgehensweise werden u. a. folgende Aufgaben veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="e6fed-110">Tasks illustrated in this walkthrough include:</span></span>

- <span data-ttu-id="e6fed-111">Erstellen eines Windows Forms Projekts</span><span class="sxs-lookup"><span data-stu-id="e6fed-111">Creating a Windows Forms project.</span></span>

- <span data-ttu-id="e6fed-112">Erstellen einer benutzerdefinierten Komponente.</span><span class="sxs-lookup"><span data-stu-id="e6fed-112">Creating a custom component.</span></span>

- <span data-ttu-id="e6fed-113">Erstellen einer Instanz einer benutzerdefinierten Komponente.</span><span class="sxs-lookup"><span data-stu-id="e6fed-113">Creating an instance of a custom component.</span></span>

- <span data-ttu-id="e6fed-114">Entladen und erneutes Laden einer benutzerdefinierten Komponente.</span><span class="sxs-lookup"><span data-stu-id="e6fed-114">Unloading and reloading a custom component.</span></span>

<span data-ttu-id="e6fed-115">Wenn Sie fertig sind, werden Sie feststellen, dass die **Toolbox** mit einer Komponente aufgefüllt ist, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="e6fed-115">When you are finished, you will see that the **Toolbox** is populated with a component that you have created.</span></span>

## <a name="create-the-project"></a><span data-ttu-id="e6fed-116">Erstellen des Projekts</span><span class="sxs-lookup"><span data-stu-id="e6fed-116">Create the project</span></span>

1. <span data-ttu-id="e6fed-117">Erstellen Sie in Visual Studio ein Windows-basiertes Anwendungsprojekt mit dem Namen `ToolboxExample` (**File**  >  **New**  >  **Project**  >  **Visual c#** oder **Visual Basic**  >  **Classic Desktop**  >  **Windows Forms Anwendung**).</span><span class="sxs-lookup"><span data-stu-id="e6fed-117">In Visual Studio, create a Windows-based application project called `ToolboxExample` (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>

2. <span data-ttu-id="e6fed-118">Fügen Sie dem Projekt eine neue Komponente hinzu.</span><span class="sxs-lookup"><span data-stu-id="e6fed-118">Add a new component to the project.</span></span> <span data-ttu-id="e6fed-119">Geben Sie ihm den Namen `DemoComponent`.</span><span class="sxs-lookup"><span data-stu-id="e6fed-119">Call it `DemoComponent`.</span></span>

     <span data-ttu-id="e6fed-120">Weitere Informationen finden Sie unter Gewusst [wie: Hinzufügen neuer Projekt Elemente](/previous-versions/visualstudio/visual-studio-2010/w0572c5b(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="e6fed-120">For more information, see [How to: Add New Project Items](/previous-versions/visualstudio/visual-studio-2010/w0572c5b(v=vs.100)).</span></span>

3. <span data-ttu-id="e6fed-121">Erstellen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="e6fed-121">Build the project.</span></span>

4. <span data-ttu-id="e6fed-122">Klicken Sie **im Menü Extras** auf das **options** Element.</span><span class="sxs-lookup"><span data-stu-id="e6fed-122">From the **Tools** menu, click the **Options** item.</span></span> <span data-ttu-id="e6fed-123">Klicken Sie unter dem **Windows Forms-Designer** Element auf **Allgemein** , und stellen Sie sicher, dass die **autotoolboxpopulate** -Option auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e6fed-123">Click **General** under the **Windows Forms Designer** item and ensure that the **AutoToolboxPopulate** option is set to **True**.</span></span>

## <a name="create-an-instance-of-a-custom-component"></a><span data-ttu-id="e6fed-124">Erstellen einer Instanz einer benutzerdefinierten Komponente</span><span class="sxs-lookup"><span data-stu-id="e6fed-124">Create an instance of a custom component</span></span>

<span data-ttu-id="e6fed-125">Der nächste Schritt ist das Erstellen einer Instanz der benutzerdefinierten Komponente auf dem Formular.</span><span class="sxs-lookup"><span data-stu-id="e6fed-125">The next step is to create an instance of the custom component on the form.</span></span> <span data-ttu-id="e6fed-126">Da die **Toolbox** automatisch die neue Komponente berücksichtigt, ist dies so einfach wie das Erstellen einer beliebigen anderen Komponente oder eines Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="e6fed-126">Because the **Toolbox** automatically accounts for the new component, this is as easy as creating any other component or control.</span></span>

1. <span data-ttu-id="e6fed-127">Öffnen Sie das Projektformular im Formular- **Designer**.</span><span class="sxs-lookup"><span data-stu-id="e6fed-127">Open the project's form in the **Forms Designer**.</span></span>

2. <span data-ttu-id="e6fed-128">Klicken Sie in der **Toolbox** auf die Registerkarte neu namens **ToolboxExample Components**.</span><span class="sxs-lookup"><span data-stu-id="e6fed-128">In the **Toolbox**, click the new tab called **ToolboxExample Components**.</span></span>

     <span data-ttu-id="e6fed-129">Wenn Sie auf die Registerkarte klicken, wird **DemoComponent** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6fed-129">Once you click the tab, you will see **DemoComponent**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e6fed-130">Aus Leistungsgründen zeigen Komponenten im automatisch aufgefüllten Bereich der **Toolbox** keine benutzerdefinierten Bitmaps an, und <xref:System.Drawing.ToolboxBitmapAttribute> wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e6fed-130">For performance reasons, components in the auto-populated area of the **Toolbox** do not display custom bitmaps, and the <xref:System.Drawing.ToolboxBitmapAttribute> is not supported.</span></span> <span data-ttu-id="e6fed-131">Um ein Symbol für eine benutzerdefinierte Komponente in der **Toolbox** anzuzeigen, verwenden Sie das Dialogfeld **Toolbox Elemente auswählen** , um die Komponente zu laden.</span><span class="sxs-lookup"><span data-stu-id="e6fed-131">To display an icon for a custom component in the **Toolbox**, use the **Choose Toolbox Items** dialog box to load your component.</span></span>

3. <span data-ttu-id="e6fed-132">Ziehen Sie die Komponente auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="e6fed-132">Drag your component onto your form.</span></span>

     <span data-ttu-id="e6fed-133">Eine Instanz der Komponente wird erstellt und der **Komponenten Leiste** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="e6fed-133">An instance of the component is created and added to the **Component Tray**.</span></span>

## <a name="unload-and-reload-a-custom-component"></a><span data-ttu-id="e6fed-134">Entladen und erneutes Laden einer benutzerdefinierten Komponente</span><span class="sxs-lookup"><span data-stu-id="e6fed-134">Unload and reload a custom component</span></span>

<span data-ttu-id="e6fed-135">Die **Toolbox** berücksichtigt die Komponenten in jedem geladenen Projekt, und wenn ein Projekt entladen wird, werden die Verweise auf die Projektkomponenten entfernt.</span><span class="sxs-lookup"><span data-stu-id="e6fed-135">The **Toolbox** takes account of the components in each loaded project, and when a project is unloaded, it removes references to the project's components.</span></span>

1. <span data-ttu-id="e6fed-136">Entladen Sie das Projekt aus der Projekt Mappe.</span><span class="sxs-lookup"><span data-stu-id="e6fed-136">Unload the project from the solution.</span></span>

     <span data-ttu-id="e6fed-137">Weitere Informationen zum Entladen von Projekten finden Sie unter Gewusst [wie: entladen und](/previous-versions/visualstudio/visual-studio-2010/tt479x1t(v=vs.100))erneutes Laden von Projekten.</span><span class="sxs-lookup"><span data-stu-id="e6fed-137">For more information about unloading projects, see [How to: Unload and Reload Projects](/previous-versions/visualstudio/visual-studio-2010/tt479x1t(v=vs.100)).</span></span> <span data-ttu-id="e6fed-138">Wenn Sie zum Speichern aufgefordert werden, wählen Sie **Ja** aus.</span><span class="sxs-lookup"><span data-stu-id="e6fed-138">If you are prompted to save, choose **Yes**.</span></span>

2. <span data-ttu-id="e6fed-139">Fügen Sie der Projekt Mappe ein neues **Windows-Anwendungs** Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="e6fed-139">Add a new **Windows Application** project to the solution.</span></span> <span data-ttu-id="e6fed-140">Öffnen Sie das Formular im **Designer**.</span><span class="sxs-lookup"><span data-stu-id="e6fed-140">Open the form in the **Designer**.</span></span>

     <span data-ttu-id="e6fed-141">Die **ToolboxExample-Komponenten** Registerkarte aus dem vorherigen Projekt ist nun nicht mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e6fed-141">The **ToolboxExample Components** tab from the previous project is now gone.</span></span>

3. <span data-ttu-id="e6fed-142">Laden Sie das `ToolboxExample` Projekt neu.</span><span class="sxs-lookup"><span data-stu-id="e6fed-142">Reload the `ToolboxExample` project.</span></span>

     <span data-ttu-id="e6fed-143">Die **ToolboxExample-Komponenten** Registerkarte wird nun erneut angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e6fed-143">The **ToolboxExample Components** tab now reappears.</span></span>

## <a name="next-steps"></a><span data-ttu-id="e6fed-144">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="e6fed-144">Next steps</span></span>

<span data-ttu-id="e6fed-145">In dieser exemplarischen Vorgehensweise wird veranschaulicht, dass die **Toolbox** die Komponenten eines Projekts berücksichtigt, aber die **Toolbox** berücksichtigt auch die Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="e6fed-145">This walkthrough demonstrates that the **Toolbox** takes account of a project's components, but the **Toolbox** is also takes account of controls.</span></span> <span data-ttu-id="e6fed-146">Experimentieren Sie mit ihren eigenen benutzerdefinierten Steuerelementen, indem Sie Steuerelemente hinzufügen und aus der Projekt Mappe entfernen.</span><span class="sxs-lookup"><span data-stu-id="e6fed-146">Experiment with your own custom controls by adding and removing control projects from your solution.</span></span>

## <a name="see-also"></a><span data-ttu-id="e6fed-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6fed-147">See also</span></span>

- <span data-ttu-id="e6fed-148">[Allgemein, Windows Forms-Designer, Dialogfeld "Optionen"](/previous-versions/visualstudio/visual-studio-2010/5aazxs78(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e6fed-148">[General, Windows Forms Designer, Options Dialog Box](/previous-versions/visualstudio/visual-studio-2010/5aazxs78(v=vs.100))</span></span>
- <span data-ttu-id="e6fed-149">[Vorgehensweise: Ändern von Registerkarten der Toolbox](/previous-versions/visualstudio/visual-studio-2010/66kwe227(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e6fed-149">[How to: Manipulate Toolbox Tabs](/previous-versions/visualstudio/visual-studio-2010/66kwe227(v=vs.100))</span></span>
- <span data-ttu-id="e6fed-150">[Dialogfeld „Toolboxelemente auswählen“ (Visual Studio)](/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="e6fed-150">[Choose Toolbox Items Dialog Box (Visual Studio)](/previous-versions/visualstudio/visual-studio-2010/dyca0t6t(v=vs.100))</span></span>
- [<span data-ttu-id="e6fed-151">Einfügen von Steuerelementen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e6fed-151">Putting Controls on Windows Forms</span></span>](putting-controls-on-windows-forms.md)
