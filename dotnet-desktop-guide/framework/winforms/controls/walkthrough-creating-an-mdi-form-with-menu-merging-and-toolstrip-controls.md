---
title: 'Exemplarische Vorgehensweise: Erstellen eines MDI-Formulars mit der Zusammenführungsfunktion für Menüs und ToolStrip-Steuerelemente'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toolbars [Windows Forms]
- ToolStripPanel control [Windows Forms]
- MDI [Windows Forms], creating forms
- multiple document interface forms
- MDI forms
- ToolStrip control [Windows Forms]
- MDI forms [Windows Forms], creating
- MDI forms [Windows Forms], walkthroughs
ms.assetid: fbab4221-74af-42d0-bbf4-3c97f7b2e544
ms.openlocfilehash: d71534bed0af142ff71ba9a0c01207b2c72a6d6a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976962"
---
# <a name="walkthrough-creating-an-mdi-form-with-menu-merging-and-toolstrip-controls"></a><span data-ttu-id="c9d77-102">Exemplarische Vorgehensweise: Erstellen eines MDI-Formulars mit der Zusammenführungsfunktion für Menüs und ToolStrip-Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="c9d77-102">Walkthrough: Creating an MDI Form with Menu Merging and ToolStrip Controls</span></span>

<span data-ttu-id="c9d77-103">Der <xref:System.Windows.Forms?displayProperty=nameWithType>-Namespace unterstützt MDI-Anwendungen (Multiple Document Interface, Schnittstelle für mehrere Dokumente), und das <xref:System.Windows.Forms.MenuStrip>-Steuerelement unterstützt das Zusammenführen von Menüs.</span><span class="sxs-lookup"><span data-stu-id="c9d77-103">The <xref:System.Windows.Forms?displayProperty=nameWithType> namespace supports multiple document interface (MDI) applications, and the <xref:System.Windows.Forms.MenuStrip> control supports menu merging.</span></span> <span data-ttu-id="c9d77-104">MDI-Formulare können auch <xref:System.Windows.Forms.ToolStrip>-Steuerelemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="c9d77-104">MDI forms can also <xref:System.Windows.Forms.ToolStrip> controls.</span></span>

<span data-ttu-id="c9d77-105">Diese exemplarische Vorgehensweise veranschaulicht, wie Steuer <xref:System.Windows.Forms.ToolStripPanel> Elemente mit einem MDI-Formular verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c9d77-105">This walkthrough demonstrates how to use <xref:System.Windows.Forms.ToolStripPanel> controls with an MDI form.</span></span> <span data-ttu-id="c9d77-106">Das Formular unterstützt auch Zusammenführen von Menüs mit untergeordneten Menüs.</span><span class="sxs-lookup"><span data-stu-id="c9d77-106">The form also supports menu merging with child menus.</span></span> <span data-ttu-id="c9d77-107">In dieser exemplarischen Vorgehensweise werden die folgenden Aufgaben veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="c9d77-107">The following tasks are illustrated in this walkthrough:</span></span>

- <span data-ttu-id="c9d77-108">Erstellen eines Windows Forms Projekts</span><span class="sxs-lookup"><span data-stu-id="c9d77-108">Creating a Windows Forms project.</span></span>

- <span data-ttu-id="c9d77-109">Erstellen des Hauptmenüs für das Formular.</span><span class="sxs-lookup"><span data-stu-id="c9d77-109">Creating the main menu for your form.</span></span> <span data-ttu-id="c9d77-110">Der tatsächliche Name des Menüs ist unterschiedlich.</span><span class="sxs-lookup"><span data-stu-id="c9d77-110">The actual name of the menu will vary.</span></span>

- <span data-ttu-id="c9d77-111">Hinzufügen des <xref:System.Windows.Forms.ToolStripPanel> Steuer Elements zur **Toolbox**.</span><span class="sxs-lookup"><span data-stu-id="c9d77-111">Adding the <xref:System.Windows.Forms.ToolStripPanel> control to the **Toolbox**.</span></span>

- <span data-ttu-id="c9d77-112">Erstellen eines untergeordneten Formulars.</span><span class="sxs-lookup"><span data-stu-id="c9d77-112">Creating a child form.</span></span>

- <span data-ttu-id="c9d77-113">Anordnen <xref:System.Windows.Forms.ToolStripPanel> von Steuerelementen nach z-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="c9d77-113">Arranging <xref:System.Windows.Forms.ToolStripPanel> controls by z-order.</span></span>

<span data-ttu-id="c9d77-114">Wenn Sie fertig sind, verfügen Sie über ein MDI-Formular, das Zusammenführen von Menüs und verschiebbaren Steuerelementen unterstützt <xref:System.Windows.Forms.ToolStrip> .</span><span class="sxs-lookup"><span data-stu-id="c9d77-114">When you are finished, you will have an MDI form that supports menu merging and movable <xref:System.Windows.Forms.ToolStrip> controls.</span></span>

<span data-ttu-id="c9d77-115">Informationen zum Kopieren des Codes in diesem Thema als einzelne Auflistung finden Sie unter Gewusst [wie: Erstellen eines MDI-Formulars mit der Zusammenführung von Menüs und ToolStrip-Steuerelementen](how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="c9d77-115">To copy the code in this topic as a single listing, see [How to: Create an MDI Form with Menu Merging and ToolStrip Controls](how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c9d77-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="c9d77-116">Prerequisites</span></span>

<span data-ttu-id="c9d77-117">Sie benötigen Visual Studio, um diese exemplarische Vorgehensweise abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c9d77-117">You'll need Visual Studio to complete this walkthrough.</span></span>

## <a name="create-the-project"></a><span data-ttu-id="c9d77-118">Erstellen des Projekts</span><span class="sxs-lookup"><span data-stu-id="c9d77-118">Create the project</span></span>

1. <span data-ttu-id="c9d77-119">Erstellen Sie in Visual Studio ein Windows-Anwendungsprojekt mit dem Namen **MDIForm** (**File**  >  **New**  >  **Project**  >  **Visual c#** oder **Visual Basic**  >  **Classic Desktop**  >  **Windows Forms Application**).</span><span class="sxs-lookup"><span data-stu-id="c9d77-119">In Visual Studio, create a Windows Application project called **MdiForm** (**File** > **New** > **Project** > **Visual C#** or **Visual Basic** > **Classic Desktop** > **Windows Forms Application**).</span></span>

2. <span data-ttu-id="c9d77-120">Wählen Sie im Windows Forms-Designer das Formular aus.</span><span class="sxs-lookup"><span data-stu-id="c9d77-120">In the Windows Forms Designer, select the form.</span></span>

3. <span data-ttu-id="c9d77-121">Legen Sie in der Eigenschaftenfenster den Wert von <xref:System.Windows.Forms.Form.IsMdiContainer%2A> auf fest `true` .</span><span class="sxs-lookup"><span data-stu-id="c9d77-121">In the Properties window, set the value of the <xref:System.Windows.Forms.Form.IsMdiContainer%2A> to `true`.</span></span>

## <a name="create-the-main-menu"></a><span data-ttu-id="c9d77-122">Erstellen des Hauptmenü</span><span class="sxs-lookup"><span data-stu-id="c9d77-122">Create the main menu</span></span>

<span data-ttu-id="c9d77-123">Das übergeordnete MDI-Formular enthält das Hauptmenü.</span><span class="sxs-lookup"><span data-stu-id="c9d77-123">The parent MDI form contains the main menu.</span></span> <span data-ttu-id="c9d77-124">Das Hauptmenü hat ein Menü Element mit dem Namen **Fenster**.</span><span class="sxs-lookup"><span data-stu-id="c9d77-124">The main menu has one menu item named **Window**.</span></span> <span data-ttu-id="c9d77-125">Mit dem Menü Element **Fenster** können Sie untergeordnete Formulare erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9d77-125">With the **Window** menu item, you can create child forms.</span></span> <span data-ttu-id="c9d77-126">Menü Elemente aus untergeordneten Formularen werden im Hauptmenü zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="c9d77-126">Menu items from child forms are merged into the main menu.</span></span>

1. <span data-ttu-id="c9d77-127">Ziehen Sie ein-Steuerelement aus der **Toolbox** <xref:System.Windows.Forms.MenuStrip> auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="c9d77-127">From the **Toolbox**, drag a <xref:System.Windows.Forms.MenuStrip> control onto the form.</span></span>

2. <span data-ttu-id="c9d77-128">Fügen Sie <xref:System.Windows.Forms.ToolStripMenuItem> dem Steuerelement ein hinzu, <xref:System.Windows.Forms.MenuStrip> und nennen Sie es **Window**.</span><span class="sxs-lookup"><span data-stu-id="c9d77-128">Add a <xref:System.Windows.Forms.ToolStripMenuItem> to the <xref:System.Windows.Forms.MenuStrip> control and name it **Window**.</span></span>

3. <span data-ttu-id="c9d77-129">Wählen Sie das <xref:System.Windows.Forms.MenuStrip>-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c9d77-129">Select the <xref:System.Windows.Forms.MenuStrip> control.</span></span>

4. <span data-ttu-id="c9d77-130">Legen Sie in der Eigenschaftenfenster den Wert der- <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> Eigenschaft auf fest `ToolStripMenuItem1` .</span><span class="sxs-lookup"><span data-stu-id="c9d77-130">In the Properties window, set the value of the <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> property to `ToolStripMenuItem1`.</span></span>

5. <span data-ttu-id="c9d77-131">Fügen Sie dem **Fenster** Menü Element ein Unterelement hinzu, und benennen Sie das Unterelement **neu**.</span><span class="sxs-lookup"><span data-stu-id="c9d77-131">Add a subitem to the **Window** menu item, and then name the subitem **New**.</span></span>

6. <span data-ttu-id="c9d77-132">Klicken Sie im Fenster Eigenschaften auf **Ereignisse**.</span><span class="sxs-lookup"><span data-stu-id="c9d77-132">In the Properties window, click **Events**.</span></span>

7. <span data-ttu-id="c9d77-133">Doppelklicken Sie auf das <xref:System.Windows.Forms.ToolStripItem.Click> Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c9d77-133">Double-click the <xref:System.Windows.Forms.ToolStripItem.Click> event.</span></span>

     <span data-ttu-id="c9d77-134">Der Windows Forms-Designer generiert einen Ereignishandler für das- <xref:System.Windows.Forms.ToolStripItem.Click> Ereignis.</span><span class="sxs-lookup"><span data-stu-id="c9d77-134">The Windows Forms Designer generates an event handler for the <xref:System.Windows.Forms.ToolStripItem.Click> event.</span></span>

8. <span data-ttu-id="c9d77-135">Fügen Sie den folgenden Code in den-Ereignishandler ein.</span><span class="sxs-lookup"><span data-stu-id="c9d77-135">Insert the following code into the event handler.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.MdiForm#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.ToolStrip.MdiForm#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.MdiForm/VB/Form1.vb#2)]

## <a name="add-the-toolstrippanel-control-to-the-toolbox"></a><span data-ttu-id="c9d77-136">Fügen Sie das ToolStripPanel-Steuerelement der Toolbox hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9d77-136">Add the ToolStripPanel control to the Toolbox</span></span>

<span data-ttu-id="c9d77-137">Wenn Sie <xref:System.Windows.Forms.MenuStrip> Steuerelemente mit einem MDI-Formular verwenden, müssen Sie über das-Steuerelement verfügen <xref:System.Windows.Forms.ToolStripPanel> .</span><span class="sxs-lookup"><span data-stu-id="c9d77-137">When you use <xref:System.Windows.Forms.MenuStrip> controls with an MDI form you must have the <xref:System.Windows.Forms.ToolStripPanel> control.</span></span> <span data-ttu-id="c9d77-138">Sie müssen das- <xref:System.Windows.Forms.ToolStripPanel> Steuerelement der **Toolbox** hinzufügen, um das MDI-Formular im Windows Forms-Designer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c9d77-138">You must add the <xref:System.Windows.Forms.ToolStripPanel> control to the **Toolbox** to build your MDI form in the Windows Forms Designer.</span></span>

1. <span data-ttu-id="c9d77-139">Öffnen Sie die **Toolbox**, und klicken Sie dann auf die Registerkarte **alle Windows Forms** , um die verfügbaren Windows Forms Steuerelemente anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c9d77-139">Open the **Toolbox**, and then click the **All Windows Forms** tab to show the available Windows Forms controls.</span></span>

2. <span data-ttu-id="c9d77-140">Klicken Sie mit der rechten Maustaste, um das Kontextmenü zu öffnen, und wählen Sie **Elemente auswählen**.</span><span class="sxs-lookup"><span data-stu-id="c9d77-140">Right-click to open the shortcut menu, and select **Choose Items**.</span></span>

3. <span data-ttu-id="c9d77-141">Führen Sie im Dialogfeld **Toolbox Elemente auswählen** einen **Bildlauf** nach unten in der Spalte Name aus, bis Sie **ToolStripPanel** gefunden haben.</span><span class="sxs-lookup"><span data-stu-id="c9d77-141">In the **Choose Toolbox Items** dialog box, scroll down the **Name** column until you find **ToolStripPanel**.</span></span>

4. <span data-ttu-id="c9d77-142">Aktivieren Sie das Kontrollkästchen von **ToolStripPanel**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9d77-142">Select the check box by **ToolStripPanel**, and then click **OK**.</span></span>

     <span data-ttu-id="c9d77-143">Das-Steuerelement wird <xref:System.Windows.Forms.ToolStripPanel> in der **Toolbox** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c9d77-143">The <xref:System.Windows.Forms.ToolStripPanel> control appears in the **Toolbox**.</span></span>

## <a name="create-a-child-form"></a><span data-ttu-id="c9d77-144">Erstellen eines untergeordneten Formulars</span><span class="sxs-lookup"><span data-stu-id="c9d77-144">Create a child form</span></span>

<span data-ttu-id="c9d77-145">In diesem Verfahren definieren Sie eine separate untergeordnete Formular Klasse, die über ein eigenes <xref:System.Windows.Forms.MenuStrip> Steuerelement verfügt.</span><span class="sxs-lookup"><span data-stu-id="c9d77-145">In this procedure, you will define a separate child form class that has its own <xref:System.Windows.Forms.MenuStrip> control.</span></span> <span data-ttu-id="c9d77-146">Die Menü Elemente für dieses Formular werden mit denen des übergeordneten Formulars zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="c9d77-146">The menu items for this form are merged with those of the parent form.</span></span>

1. <span data-ttu-id="c9d77-147">Fügen Sie dem Projekt ein neues Formular `ChildForm` mit dem Namen hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9d77-147">Add a new form named `ChildForm` to the project.</span></span>

     <span data-ttu-id="c9d77-148">Weitere Informationen finden Sie unter Gewusst [wie: Hinzufügen von Windows Forms zu einem Projekt](/previous-versions/visualstudio/visual-studio-2010/y2xxdce3(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="c9d77-148">For more information, see [How to: Add Windows Forms to a Project](/previous-versions/visualstudio/visual-studio-2010/y2xxdce3(v=vs.100)).</span></span>

2. <span data-ttu-id="c9d77-149">Ziehen Sie aus der **Toolbox** ein- <xref:System.Windows.Forms.MenuStrip> Steuerelement auf das untergeordnete Formular.</span><span class="sxs-lookup"><span data-stu-id="c9d77-149">From the **Toolbox**, drag a <xref:System.Windows.Forms.MenuStrip> control onto the child form.</span></span>

3. <span data-ttu-id="c9d77-150">Klicken Sie auf das <xref:System.Windows.Forms.MenuStrip> Designer-Aktions Symbol des Steuer Elements ( ![ kleiner schwarzer Pfeil ](./media/designer-actions-glyph.gif) ), und wählen Sie dann **Elemente bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="c9d77-150">Click the <xref:System.Windows.Forms.MenuStrip> control's designer actions glyph (![Small black arrow](./media/designer-actions-glyph.gif)), and then select **Edit Items**.</span></span>

4. <span data-ttu-id="c9d77-151">Fügen Sie im Dialogfeld Elementauflistungs- **Editor** dem untergeordneten Menü ein neues <xref:System.Windows.Forms.ToolStripMenuItem> benanntes **ChildMenuItem-Element** hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9d77-151">In the **Items Collection Editor** dialog box, add a new <xref:System.Windows.Forms.ToolStripMenuItem> named **ChildMenuItem** to the child menu.</span></span>

     <span data-ttu-id="c9d77-152">Weitere Informationen finden Sie unter [ToolStrip Items](/previous-versions/visualstudio/visual-studio-2010/ms233643(v=vs.100))-Auflistungs-Editor.</span><span class="sxs-lookup"><span data-stu-id="c9d77-152">For more information, see [ToolStrip Items Collection Editor](/previous-versions/visualstudio/visual-studio-2010/ms233643(v=vs.100)).</span></span>

## <a name="test-the-form"></a><span data-ttu-id="c9d77-153">Testen des Formulars</span><span class="sxs-lookup"><span data-stu-id="c9d77-153">Test the form</span></span>

1. <span data-ttu-id="c9d77-154">Drücken Sie **F5** , um das Formular zu kompilieren und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c9d77-154">Press **F5** to compile and run your form.</span></span>

2. <span data-ttu-id="c9d77-155">Klicken Sie auf das Menü Element **Fenster** , um das Menü zu öffnen, und klicken Sie dann auf **neu**.</span><span class="sxs-lookup"><span data-stu-id="c9d77-155">Click the **Window** menu item to open the menu, and then click **New**.</span></span>

     <span data-ttu-id="c9d77-156">Im MDI-Client Bereich des Formulars wird ein neues untergeordnetes Formular erstellt.</span><span class="sxs-lookup"><span data-stu-id="c9d77-156">A new child form is created in the form's MDI client area.</span></span> <span data-ttu-id="c9d77-157">Das Menü des untergeordneten Formulars wird mit dem Hauptmenü zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="c9d77-157">The child form's menu is merged with the main menu.</span></span>

3. <span data-ttu-id="c9d77-158">Schließen Sie das untergeordnete Formular.</span><span class="sxs-lookup"><span data-stu-id="c9d77-158">Close the child form.</span></span>

     <span data-ttu-id="c9d77-159">Das Menü des untergeordneten Formulars wird aus dem Hauptmenü entfernt.</span><span class="sxs-lookup"><span data-stu-id="c9d77-159">The child form's menu is removed from the main menu.</span></span>

4. <span data-ttu-id="c9d77-160">Klicken Sie mehrmals auf **neu** .</span><span class="sxs-lookup"><span data-stu-id="c9d77-160">Click **New** several times.</span></span>

     <span data-ttu-id="c9d77-161">Die untergeordneten Formulare werden automatisch unter dem Menü Element **Fenster** aufgeführt, da die <xref:System.Windows.Forms.MenuStrip> -Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c9d77-161">The child forms are automatically listed under the **Window** menu item because the <xref:System.Windows.Forms.MenuStrip> control's <xref:System.Windows.Forms.MenuStrip.MdiWindowListItem%2A> property is assigned.</span></span>

## <a name="add-toolstrip-support"></a><span data-ttu-id="c9d77-162">ToolStrip-Unterstützung hinzufügen</span><span class="sxs-lookup"><span data-stu-id="c9d77-162">Add ToolStrip support</span></span>

<span data-ttu-id="c9d77-163">In diesem Verfahren fügen Sie <xref:System.Windows.Forms.ToolStrip> dem übergeordneten MDI-Formular vier Steuerelemente hinzu.</span><span class="sxs-lookup"><span data-stu-id="c9d77-163">In this procedure, you will add four <xref:System.Windows.Forms.ToolStrip> controls to the MDI parent form.</span></span> <span data-ttu-id="c9d77-164">Jedes <xref:System.Windows.Forms.ToolStrip> Steuerelement wird in einem-Steuerelement hinzugefügt <xref:System.Windows.Forms.ToolStripPanel> , das an den Rand des Formulars angedockt wird.</span><span class="sxs-lookup"><span data-stu-id="c9d77-164">Each <xref:System.Windows.Forms.ToolStrip> control is added inside a <xref:System.Windows.Forms.ToolStripPanel> control, which is docked to the edge of the form.</span></span>

1. <span data-ttu-id="c9d77-165">Ziehen Sie ein-Steuerelement aus der **Toolbox** <xref:System.Windows.Forms.ToolStripPanel> auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="c9d77-165">From the **Toolbox**, drag a <xref:System.Windows.Forms.ToolStripPanel> control onto the form.</span></span>

2. <span data-ttu-id="c9d77-166"><xref:System.Windows.Forms.ToolStripPanel>Doppelklicken Sie bei ausgewähltem Steuerelement <xref:System.Windows.Forms.ToolStrip> in der **Toolbox** auf das-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c9d77-166">With the <xref:System.Windows.Forms.ToolStripPanel> control selected, double-click the <xref:System.Windows.Forms.ToolStrip> control in the **Toolbox**.</span></span>

     <span data-ttu-id="c9d77-167">Ein- <xref:System.Windows.Forms.ToolStrip> Steuerelement wird im-Steuerelement erstellt <xref:System.Windows.Forms.ToolStripPanel> .</span><span class="sxs-lookup"><span data-stu-id="c9d77-167">A <xref:System.Windows.Forms.ToolStrip> control is created in the <xref:System.Windows.Forms.ToolStripPanel> control.</span></span>

3. <span data-ttu-id="c9d77-168">Wählen Sie das <xref:System.Windows.Forms.ToolStripPanel>-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c9d77-168">Select the <xref:System.Windows.Forms.ToolStripPanel> control.</span></span>

4. <span data-ttu-id="c9d77-169">Ändern Sie in der Eigenschaftenfenster den Wert der-Eigenschaft des-Steuer Elements in <xref:System.Windows.Forms.Control.Dock%2A> <xref:System.Windows.Forms.DockStyle.Left> .</span><span class="sxs-lookup"><span data-stu-id="c9d77-169">In the Properties window, change the value of the control's <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Left>.</span></span>

     <span data-ttu-id="c9d77-170">Das- <xref:System.Windows.Forms.ToolStripPanel> Steuerelement wird auf der linken Seite des Formulars unterhalb des Hauptmenü andocken.</span><span class="sxs-lookup"><span data-stu-id="c9d77-170">The <xref:System.Windows.Forms.ToolStripPanel> control docks to the left side of the form, underneath the main menu.</span></span> <span data-ttu-id="c9d77-171">Der MDI-Client Bereich ändert sich in die Größe des- <xref:System.Windows.Forms.ToolStripPanel> Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="c9d77-171">The MDI client area resizes to fit the <xref:System.Windows.Forms.ToolStripPanel> control.</span></span>

5. <span data-ttu-id="c9d77-172">Wiederholen Sie die Schritte 1 bis 4.</span><span class="sxs-lookup"><span data-stu-id="c9d77-172">Repeat steps 1 through 4.</span></span>

     <span data-ttu-id="c9d77-173">Docken Sie das neue Steuerelement am <xref:System.Windows.Forms.ToolStripPanel> oberen Rand des Formulars an.</span><span class="sxs-lookup"><span data-stu-id="c9d77-173">Dock the new <xref:System.Windows.Forms.ToolStripPanel> control to the top of the form.</span></span>

     <span data-ttu-id="c9d77-174">Das <xref:System.Windows.Forms.ToolStripPanel> Steuerelement wird unter dem Hauptmenü angedockt, aber auf der rechten Seite des ersten <xref:System.Windows.Forms.ToolStripPanel> Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="c9d77-174">The <xref:System.Windows.Forms.ToolStripPanel> control is docked underneath the main menu, but to the right of the first <xref:System.Windows.Forms.ToolStripPanel> control.</span></span> <span data-ttu-id="c9d77-175">Dieser Schritt veranschaulicht die Wichtigkeit der z-Reihenfolge bei der ordnungsgemäßen Positionierung von Steuer <xref:System.Windows.Forms.ToolStripPanel> Elementen.</span><span class="sxs-lookup"><span data-stu-id="c9d77-175">This step illustrates the importance of z-order in correctly positioning <xref:System.Windows.Forms.ToolStripPanel> controls.</span></span>

6. <span data-ttu-id="c9d77-176">Wiederholen Sie die Schritte 1 bis 4 für zwei weitere Steuer <xref:System.Windows.Forms.ToolStripPanel> Elemente.</span><span class="sxs-lookup"><span data-stu-id="c9d77-176">Repeat steps 1 through 4 for two more <xref:System.Windows.Forms.ToolStripPanel> controls.</span></span>

     <span data-ttu-id="c9d77-177">Andocken der neuen Steuer <xref:System.Windows.Forms.ToolStripPanel> Elemente an der rechten und unteren Seite des Formulars.</span><span class="sxs-lookup"><span data-stu-id="c9d77-177">Dock the new <xref:System.Windows.Forms.ToolStripPanel> controls to the right and bottom of the form.</span></span>

## <a name="arrange-toolstrippanel-controls-by-z-order"></a><span data-ttu-id="c9d77-178">ToolStripPanel-Steuerelemente nach Z-Reihenfolge anordnen</span><span class="sxs-lookup"><span data-stu-id="c9d77-178">Arrange ToolStripPanel controls by Z-order</span></span>

<span data-ttu-id="c9d77-179">Die Position eines angedockten <xref:System.Windows.Forms.ToolStripPanel> Steuer Elements auf dem MDI-Formular hängt von der Position des Steuer Elements in der z-Reihenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="c9d77-179">The position of a docked <xref:System.Windows.Forms.ToolStripPanel> control on your MDI form is determined by the control's position in the z-order.</span></span> <span data-ttu-id="c9d77-180">Sie können die z-Reihenfolge der Steuerelemente im Fenster "Dokument Gliederung" problemlos anordnen.</span><span class="sxs-lookup"><span data-stu-id="c9d77-180">You can easily arrange the z-order of your controls in the Document Outline window.</span></span>

1. <span data-ttu-id="c9d77-181">Klicken Sie im Menü **Ansicht** auf **Weitere Fenster**, und klicken Sie dann auf **Dokument** Gliederung.</span><span class="sxs-lookup"><span data-stu-id="c9d77-181">In the **View** menu, click **Other Windows**, and then click **Document Outline**.</span></span>

     <span data-ttu-id="c9d77-182">Die Anordnung der Steuer <xref:System.Windows.Forms.ToolStripPanel> Elemente aus der vorherigen Prozedur entspricht nicht dem Standard.</span><span class="sxs-lookup"><span data-stu-id="c9d77-182">The arrangement of your <xref:System.Windows.Forms.ToolStripPanel> controls from the previous procedure is nonstandard.</span></span> <span data-ttu-id="c9d77-183">Dies liegt daran, dass die z-Reihenfolge nicht korrekt ist.</span><span class="sxs-lookup"><span data-stu-id="c9d77-183">This is because the z-order is not correct.</span></span> <span data-ttu-id="c9d77-184">Verwenden Sie das Fenster Dokument Gliederung, um die z-Reihenfolge der Steuerelemente zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c9d77-184">Use the Document Outline window to change the z-order of the controls.</span></span>

2. <span data-ttu-id="c9d77-185">Wählen Sie im Fenster Dokument Gliederung die Option **ToolStripPanel4** aus.</span><span class="sxs-lookup"><span data-stu-id="c9d77-185">In the Document Outline window, select **ToolStripPanel4**.</span></span>

3. <span data-ttu-id="c9d77-186">Klicken Sie wiederholt auf die Schaltfläche mit dem Pfeil nach unten, bis sich **ToolStripPanel4** am Ende der Liste befindet.</span><span class="sxs-lookup"><span data-stu-id="c9d77-186">Click the down-arrow button repeatedly, until **ToolStripPanel4** is at the bottom of the list.</span></span>

     <span data-ttu-id="c9d77-187">Das **ToolStripPanel4** -Steuerelement wird am unteren Rand des Formulars unterhalb der anderen Steuerelemente angedockt.</span><span class="sxs-lookup"><span data-stu-id="c9d77-187">The **ToolStripPanel4** control is docked to the bottom of the form, underneath the other controls.</span></span>

4. <span data-ttu-id="c9d77-188">Wählen Sie **ToolStripPanel2** aus.</span><span class="sxs-lookup"><span data-stu-id="c9d77-188">Select **ToolStripPanel2**.</span></span>

5. <span data-ttu-id="c9d77-189">Klicken Sie einmal auf die Schaltfläche mit dem Pfeil nach unten, um das dritte Steuerelement in der Liste zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="c9d77-189">Click the down-arrow button one time to position the control third in the list.</span></span>

     <span data-ttu-id="c9d77-190">Das **ToolStripPanel2** -Steuerelement wird am oberen Rand des Formulars unterhalb des Hauptmenü und über den anderen Steuerelementen angedockt.</span><span class="sxs-lookup"><span data-stu-id="c9d77-190">The **ToolStripPanel2** control is docked to the top of the form, underneath the main menu and above the other controls.</span></span>

6. <span data-ttu-id="c9d77-191">Wählen Sie im **Dokument** Gliederungs Fenster verschiedene Steuerelemente aus, und verschieben Sie Sie an verschiedene Positionen in der z-Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="c9d77-191">Select various controls in the **Document Outline** window and move them to different positions in the z-order.</span></span> <span data-ttu-id="c9d77-192">Beachten Sie die Auswirkung der z-Reihenfolge auf die Platzierung von angedockten Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="c9d77-192">Note the effect of the z-order on the placement of docked controls.</span></span> <span data-ttu-id="c9d77-193">Verwenden Sie STRG + Z oder **Rückgängig** im Menü **Bearbeiten** , um die Änderungen rückgängig zu machen.</span><span class="sxs-lookup"><span data-stu-id="c9d77-193">Use CTRL-Z or **Undo** on the **Edit** menu to undo your changes.</span></span>

## <a name="checkpoint---test-your-form"></a><span data-ttu-id="c9d77-194">Prüfpunkt: Testen des Formulars</span><span class="sxs-lookup"><span data-stu-id="c9d77-194">Checkpoint - test your form</span></span>

1. <span data-ttu-id="c9d77-195">Drücken Sie **F5** , um das Formular zu kompilieren und auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c9d77-195">Press **F5** to compile and run your form.</span></span>

2. <span data-ttu-id="c9d77-196">Klicken Sie auf den <xref:System.Windows.Forms.ToolStrip> Ziehpunkt eines Steuer Elements, und ziehen Sie das Steuerelement an verschiedene Positionen im Formular.</span><span class="sxs-lookup"><span data-stu-id="c9d77-196">Click the grip of a <xref:System.Windows.Forms.ToolStrip> control and drag the control to different positions on the form.</span></span>

     <span data-ttu-id="c9d77-197">Sie können ein- <xref:System.Windows.Forms.ToolStrip> Steuerelement von einem <xref:System.Windows.Forms.ToolStripPanel> Steuerelement zu einem anderen ziehen.</span><span class="sxs-lookup"><span data-stu-id="c9d77-197">You can drag a <xref:System.Windows.Forms.ToolStrip> control from one <xref:System.Windows.Forms.ToolStripPanel> control to another.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c9d77-198">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="c9d77-198">Next steps</span></span>

<span data-ttu-id="c9d77-199">In dieser exemplarischen Vorgehensweise haben Sie ein übergeordnetes MDI-Formular mit Steuer <xref:System.Windows.Forms.ToolStrip> Elementen und der Zusammenführung des Menüs erstellt.</span><span class="sxs-lookup"><span data-stu-id="c9d77-199">In this walkthrough, you have created an MDI parent form with <xref:System.Windows.Forms.ToolStrip> controls and menu merging.</span></span> <span data-ttu-id="c9d77-200">Sie können die-Steuerelement <xref:System.Windows.Forms.ToolStrip> Familie zu vielen anderen Zwecken verwenden:</span><span class="sxs-lookup"><span data-stu-id="c9d77-200">You can use the <xref:System.Windows.Forms.ToolStrip> family of controls for many other purposes:</span></span>

- <span data-ttu-id="c9d77-201">Erstellen Sie Kontextmenüs für Ihre Steuerelemente mit <xref:System.Windows.Forms.ContextMenuStrip> .</span><span class="sxs-lookup"><span data-stu-id="c9d77-201">Create shortcut menus for your controls with <xref:System.Windows.Forms.ContextMenuStrip>.</span></span> <span data-ttu-id="c9d77-202">Weitere Informationen finden Sie unter [Übersicht über die ContextMenu-Komponente](contextmenu-component-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="c9d77-202">For more information, see [ContextMenu Component Overview](contextmenu-component-overview-windows-forms.md).</span></span>

- <span data-ttu-id="c9d77-203">Erstellt ein Formular mit einem automatisch ausgefüllten Standardmenü.</span><span class="sxs-lookup"><span data-stu-id="c9d77-203">Created a form with an automatically populated standard menu.</span></span> <span data-ttu-id="c9d77-204">Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Bereitstellen von Standard Menü Elementen für ein Formular](walkthrough-providing-standard-menu-items-to-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="c9d77-204">For more information, see [Walkthrough: Providing Standard Menu Items to a Form](walkthrough-providing-standard-menu-items-to-a-form.md).</span></span>

- <span data-ttu-id="c9d77-205">Gestalten Sie Ihre Steuer <xref:System.Windows.Forms.ToolStrip> Elemente als professionelles Erscheinungsbild.</span><span class="sxs-lookup"><span data-stu-id="c9d77-205">Give your <xref:System.Windows.Forms.ToolStrip> controls a professional appearance.</span></span> <span data-ttu-id="c9d77-206">Weitere Informationen finden Sie unter Gewusst [wie: Festlegen des ToolStrip-Renderers für eine Anwendung](how-to-set-the-toolstrip-renderer-for-an-application.md).</span><span class="sxs-lookup"><span data-stu-id="c9d77-206">For more information, see [How to: Set the ToolStrip Renderer for an Application](how-to-set-the-toolstrip-renderer-for-an-application.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c9d77-207">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9d77-207">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="c9d77-208">Vorgehensweise: Erstellen von übergeordneten MDI-Formularen</span><span class="sxs-lookup"><span data-stu-id="c9d77-208">How to: Create MDI Parent Forms</span></span>](../advanced/how-to-create-mdi-parent-forms.md)
- [<span data-ttu-id="c9d77-209">Vorgehensweise: Erstellen von untergeordneten MDI-Formularen</span><span class="sxs-lookup"><span data-stu-id="c9d77-209">How to: Create MDI Child Forms</span></span>](../advanced/how-to-create-mdi-child-forms.md)
- [<span data-ttu-id="c9d77-210">Vorgehensweise: Einfügen eines MenuStrip in ein MDI-Dropdownmenü</span><span class="sxs-lookup"><span data-stu-id="c9d77-210">How to: Insert a MenuStrip into an MDI Drop-Down Menu</span></span>](how-to-insert-a-menustrip-into-an-mdi-drop-down-menu-windows-forms.md)
- [<span data-ttu-id="c9d77-211">ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c9d77-211">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
