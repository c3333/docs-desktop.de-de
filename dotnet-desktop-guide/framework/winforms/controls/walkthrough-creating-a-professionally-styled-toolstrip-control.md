---
title: 'Exemplarische Vorgehensweise: Erstellen eines professionellen ToolStrip-Steuerelements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolStripProfessionalRenderer class [Windows Forms]
- ToolStripRenderer class [Windows Forms]
- toolbars [Windows Forms], walkthroughs
- ToolStrip control [Windows Forms], creating professionally styled controls
ms.assetid: b52339ae-f1d3-494e-996e-eb455614098a
ms.openlocfilehash: 3fd9175f47f9f1b35743dc69b462227fdfafe55d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976963"
---
# <a name="walkthrough-creating-a-professionally-styled-toolstrip-control"></a><span data-ttu-id="56c08-102">Exemplarische Vorgehensweise: Erstellen eines professionellen ToolStrip-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="56c08-102">Walkthrough: Creating a Professionally Styled ToolStrip Control</span></span>

<span data-ttu-id="56c08-103">Sie können den Steuerelementen Ihrer Anwendung <xref:System.Windows.Forms.ToolStrip> ein professionelles Aussehen und Verhalten geben, indem Sie eine eigene Klasse schreiben, die vom-Typ abgeleitet ist <xref:System.Windows.Forms.ToolStripProfessionalRenderer> .</span><span class="sxs-lookup"><span data-stu-id="56c08-103">You can give your application’s <xref:System.Windows.Forms.ToolStrip> controls a professional appearance and behavior by writing your own class derived from the <xref:System.Windows.Forms.ToolStripProfessionalRenderer> type.</span></span>

<span data-ttu-id="56c08-104">In dieser exemplarischen Vorgehensweise wird veranschaulicht, wie <xref:System.Windows.Forms.ToolStrip> Steuerelemente verwendet werden, um ein zusammengesetztes Steuerelement zu erstellen, das dem **Navigations** Bereich von Microsoft® Outlook®</span><span class="sxs-lookup"><span data-stu-id="56c08-104">This walkthrough demonstrates how to use <xref:System.Windows.Forms.ToolStrip> controls to create a composite control that resembles the **Navigation Pane** provided by Microsoft® Outlook®.</span></span> <span data-ttu-id="56c08-105">In dieser exemplarischen Vorgehensweise werden die folgenden Aufgaben veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="56c08-105">The following tasks are illustrated in this walkthrough:</span></span>

- <span data-ttu-id="56c08-106">Erstellen eines Windows-Steuerelement Bibliothek-Projekts.</span><span class="sxs-lookup"><span data-stu-id="56c08-106">Creating a Windows Control Library project.</span></span>

- <span data-ttu-id="56c08-107">Entwerfen des StackView-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="56c08-107">Designing the StackView Control.</span></span>

- <span data-ttu-id="56c08-108">Implementieren eines benutzerdefinierten Renderers.</span><span class="sxs-lookup"><span data-stu-id="56c08-108">Implementing a Custom Renderer.</span></span>

<span data-ttu-id="56c08-109">Wenn Sie fertig sind, verfügen Sie über ein wiederverwendbares benutzerdefiniertes Client Steuerelement, das die professionelle Darstellung eines Microsoft Office® XP-Steuer Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="56c08-109">When you are finished, you will have a reusable custom client control with the professional appearance of a Microsoft Office® XP control.</span></span>

<span data-ttu-id="56c08-110">Informationen zum Kopieren des Codes in diesem Thema als einzelne Auflistung finden Sie unter Gewusst [wie: Erstellen eines professionell formatierten ToolStrip-Steuer](how-to-create-a-professionally-styled-toolstrip-control.md)Elements.</span><span class="sxs-lookup"><span data-stu-id="56c08-110">To copy the code in this topic as a single listing, see [How to: Create a Professionally Styled ToolStrip Control](how-to-create-a-professionally-styled-toolstrip-control.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="56c08-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="56c08-111">Prerequisites</span></span>

<span data-ttu-id="56c08-112">Sie benötigen Visual Studio, um diese exemplarische Vorgehensweise abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="56c08-112">You'll need Visual Studio to complete this walkthrough.</span></span>

## <a name="create-the-control-library-project"></a><span data-ttu-id="56c08-113">Erstellen des Steuerelement Bibliothek-Projekts</span><span class="sxs-lookup"><span data-stu-id="56c08-113">Create the control library project</span></span>

1. <span data-ttu-id="56c08-114">Erstellen Sie in Visual Studio ein neues Windows-Steuerelement Bibliothek-Projekt mit dem Namen `StackViewLibrary` .</span><span class="sxs-lookup"><span data-stu-id="56c08-114">In Visual Studio, create a new Windows Control Library project named `StackViewLibrary`.</span></span>

2. <span data-ttu-id="56c08-115">Löschen Sie in **Projektmappen-Explorer** das Standard Steuerelement des Projekts, indem Sie die Quelldatei mit dem Namen "UserControl1.cs" oder "UserControl1. vb" löschen, je nach ihrer Sprache Ihrer Wahl.</span><span class="sxs-lookup"><span data-stu-id="56c08-115">In **Solution Explorer**, delete the project's default control by deleting the source file named "UserControl1.cs" or "UserControl1.vb", depending on your language of choice.</span></span>

     <span data-ttu-id="56c08-116">Weitere Informationen finden Sie unter Gewusst [wie: entfernen, löschen und Ausschließen von Elementen](/previous-versions/visualstudio/visual-studio-2010/0ebzhwsk(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="56c08-116">For more information, see [How to: Remove, Delete, and Exclude Items](/previous-versions/visualstudio/visual-studio-2010/0ebzhwsk(v=vs.100)).</span></span>

3. <span data-ttu-id="56c08-117">Fügen Sie <xref:System.Windows.Forms.UserControl> dem **StackViewLibrary** -Projekt ein neues Element hinzu.</span><span class="sxs-lookup"><span data-stu-id="56c08-117">Add a new <xref:System.Windows.Forms.UserControl> item to the **StackViewLibrary** project.</span></span> <span data-ttu-id="56c08-118">Benennen Sie die neue Quelldatei mit einem Basisnamen von `StackView` .</span><span class="sxs-lookup"><span data-stu-id="56c08-118">Give the new source file a base name of `StackView`.</span></span>

## <a name="design-the-stackview-control"></a><span data-ttu-id="56c08-119">Entwerfen des StackView-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="56c08-119">Design the StackView control</span></span>

<span data-ttu-id="56c08-120">Das `StackView` Steuerelement ist ein zusammengesetztes Steuerelement mit einem untergeordneten <xref:System.Windows.Forms.ToolStrip> Steuerelement</span><span class="sxs-lookup"><span data-stu-id="56c08-120">The `StackView` control is a composite control with one child <xref:System.Windows.Forms.ToolStrip> control.</span></span> <span data-ttu-id="56c08-121">Weitere Informationen zu zusammengesetzten Steuerelementen finden Sie unter [Varianten von benutzerdefinierten Steuerelementen](varieties-of-custom-controls.md).</span><span class="sxs-lookup"><span data-stu-id="56c08-121">For more information about composite controls, see [Varieties of Custom Controls](varieties-of-custom-controls.md).</span></span>

1. <span data-ttu-id="56c08-122">Ziehen Sie aus der **Toolbox** ein- <xref:System.Windows.Forms.ToolStrip> Steuerelement auf die Entwurfs Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="56c08-122">From the **Toolbox**, drag a <xref:System.Windows.Forms.ToolStrip> control to the design surface.</span></span>

2. <span data-ttu-id="56c08-123">Legen Sie im Fenster **Eigenschaften** die <xref:System.Windows.Forms.ToolStrip> Eigenschaften des Steuer Elements gemäß der folgenden Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="56c08-123">In the **Properties** window, set the <xref:System.Windows.Forms.ToolStrip> control's properties according to the following table.</span></span>

    |<span data-ttu-id="56c08-124">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="56c08-124">Property</span></span>|<span data-ttu-id="56c08-125">Wert</span><span class="sxs-lookup"><span data-stu-id="56c08-125">Value</span></span>|
    |--------------|-----------|
    |<span data-ttu-id="56c08-126">Name</span><span class="sxs-lookup"><span data-stu-id="56c08-126">Name</span></span>|`stackStrip`|
    |<span data-ttu-id="56c08-127">CanOverflow</span><span class="sxs-lookup"><span data-stu-id="56c08-127">CanOverflow</span></span>|`false`|
    |<span data-ttu-id="56c08-128">Dock</span><span class="sxs-lookup"><span data-stu-id="56c08-128">Dock</span></span>|<xref:System.Windows.Forms.DockStyle.Bottom>|
    |<span data-ttu-id="56c08-129">Schriftart</span><span class="sxs-lookup"><span data-stu-id="56c08-129">Font</span></span>|`Tahoma, 10pt, style=Bold`|
    |<span data-ttu-id="56c08-130">GripStyle</span><span class="sxs-lookup"><span data-stu-id="56c08-130">GripStyle</span></span>|<xref:System.Windows.Forms.ToolStripGripStyle.Hidden>|
    |<span data-ttu-id="56c08-131">LayoutStyle</span><span class="sxs-lookup"><span data-stu-id="56c08-131">LayoutStyle</span></span>|<xref:System.Windows.Forms.ToolStripLayoutStyle.VerticalStackWithOverflow>|
    |<span data-ttu-id="56c08-132">Auffüllen</span><span class="sxs-lookup"><span data-stu-id="56c08-132">Padding</span></span>|`0, 7, 0, 0`|
    |<span data-ttu-id="56c08-133">RenderMode</span><span class="sxs-lookup"><span data-stu-id="56c08-133">RenderMode</span></span>|<xref:System.Windows.Forms.ToolStripRenderMode.Professional>|

3. <span data-ttu-id="56c08-134">Klicken Sie im Windows Forms-Designer auf die <xref:System.Windows.Forms.ToolStrip> Schaltfläche **Hinzufügen** des Steuer Elements, und fügen Sie dem Steuerelement eine hinzu <xref:System.Windows.Forms.ToolStripButton> `stackStrip` .</span><span class="sxs-lookup"><span data-stu-id="56c08-134">In the Windows Forms Designer, click the <xref:System.Windows.Forms.ToolStrip> control's **Add** button and add a <xref:System.Windows.Forms.ToolStripButton> to the `stackStrip` control.</span></span>

4. <span data-ttu-id="56c08-135">Legen Sie im Fenster **Eigenschaften** die <xref:System.Windows.Forms.ToolStripButton> Eigenschaften des Steuer Elements gemäß der folgenden Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="56c08-135">In the **Properties** window, set the <xref:System.Windows.Forms.ToolStripButton> control's properties according to the following table.</span></span>

    |<span data-ttu-id="56c08-136">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="56c08-136">Property</span></span>|<span data-ttu-id="56c08-137">Wert</span><span class="sxs-lookup"><span data-stu-id="56c08-137">Value</span></span>|
    |--------------|-----------|
    |<span data-ttu-id="56c08-138">Name</span><span class="sxs-lookup"><span data-stu-id="56c08-138">Name</span></span>|`mailStackButton`|
    |<span data-ttu-id="56c08-139">CheckOnClick</span><span class="sxs-lookup"><span data-stu-id="56c08-139">CheckOnClick</span></span>|<span data-ttu-id="56c08-140">true</span><span class="sxs-lookup"><span data-stu-id="56c08-140">true</span></span>|
    |<span data-ttu-id="56c08-141">CheckState</span><span class="sxs-lookup"><span data-stu-id="56c08-141">CheckState</span></span>|<xref:System.Windows.Forms.CheckState.Checked>|
    |<span data-ttu-id="56c08-142">Display Style</span><span class="sxs-lookup"><span data-stu-id="56c08-142">DisplayStyle</span></span>|<xref:System.Windows.Forms.ToolStripItemDisplayStyle.ImageAndText>|
    |<span data-ttu-id="56c08-143">ImageAlign</span><span class="sxs-lookup"><span data-stu-id="56c08-143">ImageAlign</span></span>|<xref:System.Drawing.ContentAlignment.MiddleLeft>|
    |<span data-ttu-id="56c08-144">ImageScaling</span><span class="sxs-lookup"><span data-stu-id="56c08-144">ImageScaling</span></span>|<xref:System.Windows.Forms.ToolStripItemImageScaling.None>|
    |<span data-ttu-id="56c08-145">ImageTransparentColor</span><span class="sxs-lookup"><span data-stu-id="56c08-145">ImageTransparentColor</span></span>|`238, 238, 238`|
    |<span data-ttu-id="56c08-146">Margin</span><span class="sxs-lookup"><span data-stu-id="56c08-146">Margin</span></span>|`0, 0, 0, 0`|
    |<span data-ttu-id="56c08-147">Auffüllen</span><span class="sxs-lookup"><span data-stu-id="56c08-147">Padding</span></span>|`3, 3, 3, 3`|
    |<span data-ttu-id="56c08-148">Text</span><span class="sxs-lookup"><span data-stu-id="56c08-148">Text</span></span>|<span data-ttu-id="56c08-149">**Mail**</span><span class="sxs-lookup"><span data-stu-id="56c08-149">**Mail**</span></span>|
    |<span data-ttu-id="56c08-150">Textausrichtung</span><span class="sxs-lookup"><span data-stu-id="56c08-150">TextAlign</span></span>|<xref:System.Drawing.ContentAlignment.MiddleLeft>|

5. <span data-ttu-id="56c08-151">Wiederholen Sie Schritt 7 für drei weitere Steuer <xref:System.Windows.Forms.ToolStripButton> Elemente.</span><span class="sxs-lookup"><span data-stu-id="56c08-151">Repeat step 7 for three more <xref:System.Windows.Forms.ToolStripButton> controls.</span></span>

     <span data-ttu-id="56c08-152">Benennen Sie die Steuerelemente `calendarStackButton` , `contactsStackButton` und `tasksStackButton` .</span><span class="sxs-lookup"><span data-stu-id="56c08-152">Name the controls `calendarStackButton`, `contactsStackButton`, and `tasksStackButton`.</span></span> <span data-ttu-id="56c08-153">Legen Sie den Wert der- <xref:System.Windows.Forms.Control.Text%2A> Eigenschaft auf **Calendar**, **Contacts** bzw. **Tasks** fest.</span><span class="sxs-lookup"><span data-stu-id="56c08-153">Set the value of the <xref:System.Windows.Forms.Control.Text%2A> property to **Calendar**, **Contacts**, and **Tasks**, respectively.</span></span>

## <a name="handle-events"></a><span data-ttu-id="56c08-154">Behandeln von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="56c08-154">Handle events</span></span>

<span data-ttu-id="56c08-155">Zwei Ereignisse sind wichtig, damit das `StackView` Steuerelement ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="56c08-155">Two events are important to make the `StackView` control behave correctly.</span></span> <span data-ttu-id="56c08-156">Behandeln Sie das- <xref:System.Windows.Forms.UserControl.Load> Ereignis, um das Steuerelement korrekt zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="56c08-156">Handle the <xref:System.Windows.Forms.UserControl.Load> event to position the control correctly.</span></span> <span data-ttu-id="56c08-157">Behandeln Sie das- <xref:System.Windows.Forms.ToolStripItem.Click> Ereignis für jedes <xref:System.Windows.Forms.ToolStripButton> , um dem Steuerelement `StackView` Zustands Verhalten ähnlich wie das-Steuerelement zu übergeben <xref:System.Windows.Forms.RadioButton> .</span><span class="sxs-lookup"><span data-stu-id="56c08-157">Handle the <xref:System.Windows.Forms.ToolStripItem.Click> event for each <xref:System.Windows.Forms.ToolStripButton> to give the `StackView` control state behavior similar to the <xref:System.Windows.Forms.RadioButton> control.</span></span>

1. <span data-ttu-id="56c08-158">Wählen Sie im Windows Forms-Designer das Steuerelement aus `StackView` .</span><span class="sxs-lookup"><span data-stu-id="56c08-158">In the Windows Forms Designer, select the `StackView` control.</span></span>

2. <span data-ttu-id="56c08-159">Klicken Sie im Fenster **Eigenschaften** auf **Ereignisse**.</span><span class="sxs-lookup"><span data-stu-id="56c08-159">In the **Properties** window, click **Events**.</span></span>

3. <span data-ttu-id="56c08-160">Doppelklicken Sie auf das Lade Ereignis, um den `StackView_Load` Ereignishandler zu generieren.</span><span class="sxs-lookup"><span data-stu-id="56c08-160">Double-click the Load event to generate the `StackView_Load` event handler.</span></span>

4. <span data-ttu-id="56c08-161">Kopieren Sie den folgenden Code und fügen Sie ihn in den `StackView_Load`-Ereignishandler ein.</span><span class="sxs-lookup"><span data-stu-id="56c08-161">In the `StackView_Load` event handler, copy and paste the following code.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#3)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#3)]

5. <span data-ttu-id="56c08-162">Wählen Sie im Windows Forms-Designer das Steuerelement aus `mailStackButton` .</span><span class="sxs-lookup"><span data-stu-id="56c08-162">In the Windows Forms Designer, select the `mailStackButton` control.</span></span>

6. <span data-ttu-id="56c08-163">Klicken Sie im Fenster **Eigenschaften** auf **Ereignisse**.</span><span class="sxs-lookup"><span data-stu-id="56c08-163">In the **Properties** window, click **Events**.</span></span>

7. <span data-ttu-id="56c08-164">Doppelklicken Sie auf das Click-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="56c08-164">Double-click the Click event.</span></span>

     <span data-ttu-id="56c08-165">Der-Windows Forms-Designer generiert den- `mailStackButton_Click` Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="56c08-165">The Windows Forms Designer generates the `mailStackButton_Click` event handler.</span></span>

8. <span data-ttu-id="56c08-166">Benennen Sie den- `mailStackButton_Click` Ereignishandler in um `stackButton_Click` .</span><span class="sxs-lookup"><span data-stu-id="56c08-166">Rename the `mailStackButton_Click` event handler to `stackButton_Click`.</span></span>

     <span data-ttu-id="56c08-167">Weitere Informationen finden Sie unter [Umbenennen einer Code Symbol Umgestaltung](/visualstudio/ide/reference/rename).</span><span class="sxs-lookup"><span data-stu-id="56c08-167">For more information, see [Rename a code symbol refactoring](/visualstudio/ide/reference/rename).</span></span>

9. <span data-ttu-id="56c08-168">Fügen Sie den folgenden Code in den- `stackButton_Click` Ereignishandler ein.</span><span class="sxs-lookup"><span data-stu-id="56c08-168">Insert the following code into the `stackButton_Click` event handler.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#4)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#4)]

10. <span data-ttu-id="56c08-169">Wählen Sie im Windows Forms-Designer das Steuerelement aus `calendarStackButton` .</span><span class="sxs-lookup"><span data-stu-id="56c08-169">In the Windows Forms Designer, select the `calendarStackButton` control.</span></span>

11. <span data-ttu-id="56c08-170">Legen Sie im Fenster **Eigenschaften** das Click-Ereignis auf den `stackButton_Click` Ereignishandler fest.</span><span class="sxs-lookup"><span data-stu-id="56c08-170">In the **Properties** window, set the Click event to the `stackButton_Click` event handler.</span></span>

12. <span data-ttu-id="56c08-171">Wiederholen Sie die Schritte 10 und 11 für die Steuer `contactsStackButton` `tasksStackButton` Elemente und.</span><span class="sxs-lookup"><span data-stu-id="56c08-171">Repeat steps 10 and 11 for the `contactsStackButton` and `tasksStackButton` controls.</span></span>

## <a name="define-icons"></a><span data-ttu-id="56c08-172">Symbole definieren</span><span class="sxs-lookup"><span data-stu-id="56c08-172">Define icons</span></span>

<span data-ttu-id="56c08-173">Jede `StackView` Schaltfläche verfügt über ein zugeordnetes Symbol.</span><span class="sxs-lookup"><span data-stu-id="56c08-173">Each `StackView` button has an associated icon.</span></span> <span data-ttu-id="56c08-174">Aus praktischer Gründen wird jedes Symbol als Base64-codierte Zeichenfolge dargestellt, die deserialisiert wird, bevor ein <xref:System.Drawing.Bitmap> daraus erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="56c08-174">For convenience, each icon is represented as a Base64-encoded string, which is deserialized before a <xref:System.Drawing.Bitmap> is created from it.</span></span> <span data-ttu-id="56c08-175">In einer Produktionsumgebung speichern Sie Bitmapdaten als Ressource, und ihre Symbole werden in der Windows Forms-Designer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="56c08-175">In a production environment, you store bitmap data as a resource, and your icons appear in the Windows Forms Designer.</span></span> <span data-ttu-id="56c08-176">Weitere Informationen finden Sie unter Gewusst [wie: Hinzufügen von Hintergrundbildern zu Windows Forms](/previous-versions/visualstudio/visual-studio-2010/dff9f95f(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="56c08-176">For more information, see [How to: Add Background Images to Windows Forms](/previous-versions/visualstudio/visual-studio-2010/dff9f95f(v=vs.100)).</span></span>

1. <span data-ttu-id="56c08-177">Fügen Sie im Code-Editor den folgenden Code in die `StackView` Klassendefinition ein.</span><span class="sxs-lookup"><span data-stu-id="56c08-177">In the Code Editor, insert the following code into the `StackView` class definition.</span></span> <span data-ttu-id="56c08-178">Dieser Code initialisiert die Bitmaps für die <xref:System.Windows.Forms.ToolStripButton> Symbole.</span><span class="sxs-lookup"><span data-stu-id="56c08-178">This code initializes the bitmaps for the <xref:System.Windows.Forms.ToolStripButton> icons.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#2)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#2)]

2. <span data-ttu-id="56c08-179">Fügen Sie der- `InitializeImages` Methode im- `StackView` Klassenkonstruktor einen-Rückruf hinzu.</span><span class="sxs-lookup"><span data-stu-id="56c08-179">Add a call to the `InitializeImages` method in the `StackView` class constructor.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#5)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#5)]

## <a name="implement-a-custom-renderer"></a><span data-ttu-id="56c08-180">Implementieren eines benutzerdefinierten Renderers</span><span class="sxs-lookup"><span data-stu-id="56c08-180">Implement a custom renderer</span></span>

<span data-ttu-id="56c08-181">Sie können die meisten Elemente des Steuer Elements anpassen `StackView` , das eine Klasse implementiert, die von der-Klasse abgeleitet ist <xref:System.Windows.Forms.ToolStripRenderer> .</span><span class="sxs-lookup"><span data-stu-id="56c08-181">You can customize most elements of the `StackView` control my implementing a class that derives from the <xref:System.Windows.Forms.ToolStripRenderer> class.</span></span> <span data-ttu-id="56c08-182">In diesem Verfahren implementieren Sie eine Klasse, die <xref:System.Windows.Forms.ToolStripProfessionalRenderer> den Ziehpunkt anpasst und die Farbverlaufs Hintergründe der Steuer <xref:System.Windows.Forms.ToolStripButton> Elemente zeichnet.</span><span class="sxs-lookup"><span data-stu-id="56c08-182">In this procedure, you will implement a <xref:System.Windows.Forms.ToolStripProfessionalRenderer> class that customizes the grip and draws gradient backgrounds for the <xref:System.Windows.Forms.ToolStripButton> controls.</span></span>

1. <span data-ttu-id="56c08-183">Fügen Sie den folgenden Code in die `StackView` Steuerelement Definition ein.</span><span class="sxs-lookup"><span data-stu-id="56c08-183">Insert the following code into the `StackView` control definition.</span></span>

     <span data-ttu-id="56c08-184">Dies ist die Definition für die `StackRenderer` -Klasse, die die <xref:System.Windows.Forms.ToolStripRenderer.RenderGrip> Methoden, und überschreibt, <xref:System.Windows.Forms.ToolStripRenderer.RenderToolStripBorder> <xref:System.Windows.Forms.ToolStripRenderer.RenderButtonBackground> um ein benutzerdefiniertes aussehen zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="56c08-184">This is the definition for the `StackRenderer` class, which overrides the <xref:System.Windows.Forms.ToolStripRenderer.RenderGrip>, <xref:System.Windows.Forms.ToolStripRenderer.RenderToolStripBorder>, and <xref:System.Windows.Forms.ToolStripRenderer.RenderButtonBackground> methods to produce a custom appearance.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#10)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#10)]

2. <span data-ttu-id="56c08-185">`StackView`Erstellen Sie im Konstruktor des Steuer Elements eine neue Instanz der `StackRenderer` -Klasse, und weisen Sie diese Instanz der `stackStrip` -Eigenschaft des-Steuer Elements zu <xref:System.Windows.Forms.ToolStrip.Renderer%2A> .</span><span class="sxs-lookup"><span data-stu-id="56c08-185">In the `StackView` control's constructor, create a new instance of the `StackRenderer` class and assign this instance to the `stackStrip` control's <xref:System.Windows.Forms.ToolStrip.Renderer%2A> property.</span></span>

     [!code-csharp[System.Windows.Forms.ToolStrip.StackView#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/CS/StackView.cs#5)]
     [!code-vb[System.Windows.Forms.ToolStrip.StackView#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.StackView/VB/StackView.vb#5)]

## <a name="test-the-stackview-control"></a><span data-ttu-id="56c08-186">Testen des StackView-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="56c08-186">Test the StackView control</span></span>

<span data-ttu-id="56c08-187">Das-Steuerelement wird `StackView` von der- <xref:System.Windows.Forms.UserControl> Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="56c08-187">The `StackView` control derives from the <xref:System.Windows.Forms.UserControl> class.</span></span> <span data-ttu-id="56c08-188">Daher können Sie das Steuerelement mit dem **UserControl-Test Container** testen.</span><span class="sxs-lookup"><span data-stu-id="56c08-188">Therefore, you can test the control with the **UserControl Test Container**.</span></span> <span data-ttu-id="56c08-189">Weitere Informationen finden Sie unter Gewusst [wie: Testen des Run-Time Verhaltens eines UserControl-Steuer](how-to-test-the-run-time-behavior-of-a-usercontrol.md)Elements.</span><span class="sxs-lookup"><span data-stu-id="56c08-189">For more information, see [How to: Test the Run-Time Behavior of a UserControl](how-to-test-the-run-time-behavior-of-a-usercontrol.md).</span></span>

1. <span data-ttu-id="56c08-190">Drücken Sie **F5** , um das Projekt zu erstellen und den **UserControl-Test Container** zu starten.</span><span class="sxs-lookup"><span data-stu-id="56c08-190">Press **F5** to build the project and start the **UserControl Test Container**.</span></span>

2. <span data-ttu-id="56c08-191">Bewegen Sie den Mauszeiger über die Schaltflächen des `StackView` Steuer Elements, und klicken Sie dann auf eine Schaltfläche, um die Darstellung des ausgewählten Zustands anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="56c08-191">Move the pointer over the buttons of the `StackView` control, and then click a button to see the appearance of its selected state.</span></span>

## <a name="next-steps"></a><span data-ttu-id="56c08-192">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="56c08-192">Next steps</span></span>

<span data-ttu-id="56c08-193">In dieser exemplarischen Vorgehensweise haben Sie ein wiederverwendbares benutzerdefiniertes Client Steuerelement mit dem professionellen Aussehen eines Office XP-Steuer Elements erstellt.</span><span class="sxs-lookup"><span data-stu-id="56c08-193">In this walkthrough, you have created a reusable custom client control with the professional appearance of an Office XP control.</span></span> <span data-ttu-id="56c08-194">Sie können die-Steuerelement <xref:System.Windows.Forms.ToolStrip> Familie zu vielen anderen Zwecken verwenden:</span><span class="sxs-lookup"><span data-stu-id="56c08-194">You can use the <xref:System.Windows.Forms.ToolStrip> family of controls for many other purposes:</span></span>

- <span data-ttu-id="56c08-195">Erstellen Sie Kontextmenüs für Ihre Steuerelemente mit <xref:System.Windows.Forms.ContextMenuStrip> .</span><span class="sxs-lookup"><span data-stu-id="56c08-195">Create shortcut menus for your controls with <xref:System.Windows.Forms.ContextMenuStrip>.</span></span> <span data-ttu-id="56c08-196">Weitere Informationen finden Sie unter [Übersicht über die ContextMenu-Komponente](contextmenu-component-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="56c08-196">For more information, see [ContextMenu Component Overview](contextmenu-component-overview-windows-forms.md).</span></span>

- <span data-ttu-id="56c08-197">Erstellen Sie ein Formular mit einem automatisch ausgefüllten Standardmenü.</span><span class="sxs-lookup"><span data-stu-id="56c08-197">Create a form with an automatically populated standard menu.</span></span> <span data-ttu-id="56c08-198">Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Bereitstellen von Standard Menü Elementen für ein Formular](walkthrough-providing-standard-menu-items-to-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="56c08-198">For more information, see [Walkthrough: Providing Standard Menu Items to a Form](walkthrough-providing-standard-menu-items-to-a-form.md).</span></span>

- <span data-ttu-id="56c08-199">Erstellen Sie ein MDI-Formular (Multiple Document Interface) mit andockbaren Steuer <xref:System.Windows.Forms.ToolStrip> Elementen.</span><span class="sxs-lookup"><span data-stu-id="56c08-199">Create a multiple document interface (MDI) form with docking <xref:System.Windows.Forms.ToolStrip> controls.</span></span> <span data-ttu-id="56c08-200">Weitere Informationen finden Sie unter Gewusst [wie: Erstellen eines MDI-Formulars mit der Zusammenführung von Menüs und ToolStrip-Steuerelementen](how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span><span class="sxs-lookup"><span data-stu-id="56c08-200">For more information, see [How to: Create an MDI Form with Menu Merging and ToolStrip Controls](how-to-create-an-mdi-form-with-menu-merging-and-toolstrip-controls.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="56c08-201">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56c08-201">See also</span></span>

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.StatusStrip>
- [<span data-ttu-id="56c08-202">ToolStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="56c08-202">ToolStrip Control</span></span>](toolstrip-control-windows-forms.md)
- [<span data-ttu-id="56c08-203">Vorgehensweise: Bereitstellen von Standardmenüelementen für ein Formular</span><span class="sxs-lookup"><span data-stu-id="56c08-203">How to: Provide Standard Menu Items to a Form</span></span>](how-to-provide-standard-menu-items-to-a-form.md)
