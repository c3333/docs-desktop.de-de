---
title: 'Exemplarische Vorgehensweise: Demonstrieren der visuellen Vererbung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- form inheritance [Windows Forms], walkthroughs
- visual inheritance
- inheritance [Windows Forms], walkthroughs
- walkthroughs [Windows Forms], visual inheritance
- Windows Forms, inheritance
ms.assetid: 01966086-3142-450e-8210-3fd4cb33f591
ms.openlocfilehash: af59383472ed4a5b8ca9585ba359c3bb8bb4e912
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976041"
---
# <a name="walkthrough-demonstrating-visual-inheritance"></a><span data-ttu-id="f7b39-102">Exemplarische Vorgehensweise: Demonstrieren der visuellen Vererbung</span><span class="sxs-lookup"><span data-stu-id="f7b39-102">Walkthrough: Demonstrating Visual Inheritance</span></span>

<span data-ttu-id="f7b39-103">Mit visueller Vererbung können Sie die Steuerelemente auf dem Basisformular anzeigen und neue Steuerelemente hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f7b39-103">Visual inheritance enables you to see the controls on the base form and to add new controls.</span></span> <span data-ttu-id="f7b39-104">In dieser exemplarischen Vorgehensweise erstellen Sie ein Basisformular und kompilieren es in eine Klassenbibliothek.</span><span class="sxs-lookup"><span data-stu-id="f7b39-104">In this walkthrough you will create a base form and compile it into a class library.</span></span> <span data-ttu-id="f7b39-105">Sie importieren diese Klassenbibliothek in ein anderes Projekt und erstellen ein neues Formular, das vom Basisformular erbt.</span><span class="sxs-lookup"><span data-stu-id="f7b39-105">You will import this class library into another project and create a new form that inherits from the base form.</span></span> <span data-ttu-id="f7b39-106">Bei dieser exemplarischen Vorgehensweise lernen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f7b39-106">During this walkthrough, you will learn how to:</span></span>

- <span data-ttu-id="f7b39-107">Erstellen eines Klassenbibliotheksprojekts, das ein Basisformular enthält.</span><span class="sxs-lookup"><span data-stu-id="f7b39-107">Create a class library project containing a base form.</span></span>

- <span data-ttu-id="f7b39-108">Hinzufügen einer Schaltfläche mit Eigenschaften, die abgeleitete Klassen des Basisformulars ändern können.</span><span class="sxs-lookup"><span data-stu-id="f7b39-108">Add a button with properties that derived classes of the base form can modify.</span></span>

- <span data-ttu-id="f7b39-109">Hinzufügen einer Schaltfläche, die von Erben des Basisformulars nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f7b39-109">Add a button that cannot be modified by inheritors of the base form.</span></span>

- <span data-ttu-id="f7b39-110">Erstellen eines Projekts, das ein Formular enthält, das von `BaseForm` erbt.</span><span class="sxs-lookup"><span data-stu-id="f7b39-110">Create a project containing a form that inherits from `BaseForm`.</span></span>

<span data-ttu-id="f7b39-111">Schließlich wird in dieser exemplarischen Vorgehensweise der Unterschied zwischen privaten und geschützten Steuerelementen in einem geerbten Formular gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f7b39-111">Ultimately, this walkthrough will demonstrate the difference between private and protected controls on an inherited form.</span></span>

> [!CAUTION]
> <span data-ttu-id="f7b39-112">Nicht alle Steuerelemente unterstützen visuelle Vererbung von einem Basisformular.</span><span class="sxs-lookup"><span data-stu-id="f7b39-112">Not all controls support visual inheritance from a base form.</span></span> <span data-ttu-id="f7b39-113">Die folgenden Steuerelemente unterstützen das in dieser exemplarischen Vorgehensweise beschriebene Szenario nicht:</span><span class="sxs-lookup"><span data-stu-id="f7b39-113">The following controls do not support the scenario described in this walkthrough:</span></span>
>
> - <xref:System.Windows.Forms.WebBrowser>
>
> - <xref:System.Windows.Forms.ToolStrip>
>
> - <xref:System.Windows.Forms.ToolStripPanel>
>
> - <xref:System.Windows.Forms.TableLayoutPanel>
>
> - <xref:System.Windows.Forms.FlowLayoutPanel>
>
> - <xref:System.Windows.Forms.DataGridView>
>
> <span data-ttu-id="f7b39-114">Diese Steuerelemente im geerbten Formular sind immer schreibgeschützt, unabhängig von den verwendeten Modifizierern (`private`, `protected` oder `public`).</span><span class="sxs-lookup"><span data-stu-id="f7b39-114">These controls in the inherited form are always read-only regardless of the modifiers you use (`private`, `protected`, or `public`).</span></span>

## <a name="create-a-class-library-project-containing-a-base-form"></a><span data-ttu-id="f7b39-115">Erstellen eines Klassen Bibliotheks Projekts, das ein Basis Formular enthält</span><span class="sxs-lookup"><span data-stu-id="f7b39-115">Create a class library project containing a base form</span></span>

1. <span data-ttu-id="f7b39-116">Wählen Sie in Visual Studio im Menü **Datei** die Option **Neues**  >  **Projekt** aus, um das Dialogfeld **Neues Projekt** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f7b39-116">In Visual Studio, from the **File** menu, choose **New** > **Project** to open the **New Project** dialog box.</span></span>

2. <span data-ttu-id="f7b39-117">Erstellen Sie eine Windows Forms Anwendung mit dem Namen `BaseFormLibrary` .</span><span class="sxs-lookup"><span data-stu-id="f7b39-117">Create a Windows Forms application named `BaseFormLibrary`.</span></span>

3. <span data-ttu-id="f7b39-118">Um eine Klassenbibliothek anstelle einer Standard Windows Forms Anwendung zu erstellen, klicken Sie in **Projektmappen-Explorer** mit der rechten Maustaste auf den Projekt Knoten **BaseFormLibrary** , und wählen Sie dann **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="f7b39-118">To create a class library instead of a standard Windows Forms application, in **Solution Explorer**, right-click the **BaseFormLibrary** project node and then select **Properties**.</span></span>

4. <span data-ttu-id="f7b39-119">Ändern Sie in den Eigenschaften für das Projekt den **Ausgabetyp** aus der **Windows-Anwendung** in die **Klassenbibliothek**.</span><span class="sxs-lookup"><span data-stu-id="f7b39-119">In the properties for the project, change the **Output type** from **Windows Application** to **Class Library**.</span></span>

5. <span data-ttu-id="f7b39-120">Wählen Sie im Menü **Datei** die Option **Alle speichern** aus, um das Projekt und die Dateien am Standard Speicherort zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f7b39-120">From the **File** menu, choose **Save All** to save the project and files to the default location.</span></span>

<span data-ttu-id="f7b39-121">Mit den nächsten zwei Verfahren werden dem Basisformular Schaltflächen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f7b39-121">The next two procedures add buttons to the base form.</span></span> <span data-ttu-id="f7b39-122">Zur Demonstration der visuellen Vererbung weisen Sie den Schaltflächen verschiedene Zugriffsebenen zu, indem Sie ihre `Modifiers`Eigenschaften festlegen.</span><span class="sxs-lookup"><span data-stu-id="f7b39-122">To demonstrate visual inheritance, you will give the buttons different access levels by setting their `Modifiers` properties.</span></span>

## <a name="add-a-button-that-inheritors-of-the-base-form-can-modify"></a><span data-ttu-id="f7b39-123">Fügen Sie eine Schaltfläche hinzu, die von Vererbung des Basis Formulars geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="f7b39-123">Add a button that inheritors of the base form can modify</span></span>

1. <span data-ttu-id="f7b39-124">Öffnen Sie **Form1** im Designer.</span><span class="sxs-lookup"><span data-stu-id="f7b39-124">Open **Form1** in the designer.</span></span>

2. <span data-ttu-id="f7b39-125">Doppelklicken Sie auf der Registerkarte **alle Windows Forms** der **Toolbox** auf die **Schaltfläche** , um dem Formular eine Schaltfläche hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f7b39-125">On the **All Windows Forms** tab of the **Toolbox**, double-click **Button** to add a button to the form.</span></span> <span data-ttu-id="f7b39-126">Verwenden Sie die Maus, um die Position und Größe der Schaltfläche anzupassen.</span><span class="sxs-lookup"><span data-stu-id="f7b39-126">Use the mouse to position and resize the button.</span></span>

3. <span data-ttu-id="f7b39-127">Legen Sie im "Eigenschaftenfenster" die folgenden Eigenschaften der Schaltfläche fest:</span><span class="sxs-lookup"><span data-stu-id="f7b39-127">In the Properties window, set the following properties of the button:</span></span>

    - <span data-ttu-id="f7b39-128">Legen Sie die **Text** -Eigenschaft auf **Hello** fest.</span><span class="sxs-lookup"><span data-stu-id="f7b39-128">Set the **Text** property to **Say Hello**.</span></span>

    - <span data-ttu-id="f7b39-129">Legen Sie die Eigenschaft **(Name)** auf **btnProtected** fest.</span><span class="sxs-lookup"><span data-stu-id="f7b39-129">Set the **(Name)** property to **btnProtected**.</span></span>

    - <span data-ttu-id="f7b39-130">Legen Sie die **modifizierereigenschaft** auf **Protected** fest.</span><span class="sxs-lookup"><span data-stu-id="f7b39-130">Set the **Modifiers** property to **Protected**.</span></span> <span data-ttu-id="f7b39-131">Dadurch können Formulare, die von **Form1** erben, die Eigenschaften von **btnProtected** ändern.</span><span class="sxs-lookup"><span data-stu-id="f7b39-131">This makes it possible for forms that inherit from **Form1** to modify the properties of **btnProtected**.</span></span>

4. <span data-ttu-id="f7b39-132">Doppelklicken Sie auf die Schaltfläche " **Say Hello** ", um einen Ereignishandler für das **Click** -Ereignis hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f7b39-132">Double-click the **Say Hello** button to add an event handler for the **Click** event.</span></span>

5. <span data-ttu-id="f7b39-133">Fügen Sie dem Ereignishandler folgende Codezeile hinzu:</span><span class="sxs-lookup"><span data-stu-id="f7b39-133">Add the following line of code to the event handler:</span></span>

    ```vb
    MessageBox.Show("Hello, World!")
    ```

    ```csharp
    MessageBox.Show("Hello, World!");
    ```

## <a name="add-a-button-that-cannot-be-modified-by-inheritors-of-the-base-form"></a><span data-ttu-id="f7b39-134">Hinzufügen einer Schaltfläche, die von Vererber des Basis Formulars nicht geändert werden kann</span><span class="sxs-lookup"><span data-stu-id="f7b39-134">Add a button that cannot be modified by inheritors of the base form</span></span>

1. <span data-ttu-id="f7b39-135">Wechseln Sie zur Entwurfs Ansicht, indem Sie über dem Code-Editor auf die Registerkarte **Form1. vb [Entwurf], Form1.cs [Entwurf] oder Form1.jsl [Entwurf]** klicken oder indem Sie F7 drücken.</span><span class="sxs-lookup"><span data-stu-id="f7b39-135">Switch to design view by clicking the **Form1.vb [Design], Form1.cs [Design], or Form1.jsl [Design]** tab above the code editor, or by pressing F7.</span></span>

2. <span data-ttu-id="f7b39-136">Fügen Sie eine zweite Schaltfläche hinzu, und legen Sie deren Eigenschaften wie folgt fest:</span><span class="sxs-lookup"><span data-stu-id="f7b39-136">Add a second button and set its properties as follows:</span></span>

    - <span data-ttu-id="f7b39-137">Legen Sie die **Text** -Eigenschaft auf " **Goodbye**" fest.</span><span class="sxs-lookup"><span data-stu-id="f7b39-137">Set the **Text** property to **Say Goodbye**.</span></span>

    - <span data-ttu-id="f7b39-138">Legen Sie die Eigenschaft **(Name)** auf **btnPrivate** fest.</span><span class="sxs-lookup"><span data-stu-id="f7b39-138">Set the **(Name)** property to **btnPrivate**.</span></span>

    - <span data-ttu-id="f7b39-139">Legen Sie die **modifizierereigenschaft** auf **Privat** fest.</span><span class="sxs-lookup"><span data-stu-id="f7b39-139">Set the **Modifiers** property to **Private**.</span></span> <span data-ttu-id="f7b39-140">Dies macht es für Formulare, die von **Form1** erben, nicht möglich, die Eigenschaften von **btnPrivate** zu ändern.</span><span class="sxs-lookup"><span data-stu-id="f7b39-140">This makes it impossible for forms that inherit from **Form1** to modify the properties of **btnPrivate**.</span></span>

3. <span data-ttu-id="f7b39-141">Doppelklicken Sie auf die Schaltfläche " **Say Goodbye** ", um einen Ereignishandler für das **Click** -Ereignis hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="f7b39-141">Double-click the **Say Goodbye** button to add an event handler for the **Click** event.</span></span> <span data-ttu-id="f7b39-142">Platzieren Sie die folgende Codezeile in der Ereignisprozedur:</span><span class="sxs-lookup"><span data-stu-id="f7b39-142">Place the following line of code in the event procedure:</span></span>

    ```vb
    MessageBox.Show("Goodbye!")
    ```

    ```csharp
    MessageBox.Show("Goodbye!");
    ```

4. <span data-ttu-id="f7b39-143">Wählen Sie im Menü **Erstellen** die Option **BaseForm-Bibliothek erstellen** aus, um die Klassenbibliothek zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7b39-143">From the **Build** menu, choose **Build BaseForm Library** to build the class library.</span></span>

     <span data-ttu-id="f7b39-144">Nachdem die Bibliothek erstellt wurde, können Sie ein neues Projekt erstellen, das von dem Formular erbt, das Sie gerade erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="f7b39-144">Once the library is built, you can create a new project that inherits from the form you just created.</span></span>

## <a name="create-a-project-containing-a-form-that-inherits-from-the-base-form"></a><span data-ttu-id="f7b39-145">Erstellen Sie ein Projekt, das ein Formular enthält, das vom Basis Formular erbt.</span><span class="sxs-lookup"><span data-stu-id="f7b39-145">Create a project containing a form that inherits from the base form</span></span>

1. <span data-ttu-id="f7b39-146">Wählen Sie im Menü **Datei** die Option **Hinzufügen** und dann **Neues Projekt** aus, um das Dialogfeld **Neues Projekt hinzufügen** zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="f7b39-146">From the **File** menu, choose **Add** and then **New Project** to open the **Add New Project** dialog box.</span></span>

2. <span data-ttu-id="f7b39-147">Erstellen Sie eine Windows Forms Anwendung mit dem Namen `InheritanceTest` .</span><span class="sxs-lookup"><span data-stu-id="f7b39-147">Create a Windows Forms application named `InheritanceTest`.</span></span>

## <a name="add-an-inherited-form"></a><span data-ttu-id="f7b39-148">Ein geerbtes Formular hinzufügen</span><span class="sxs-lookup"><span data-stu-id="f7b39-148">Add an inherited form</span></span>

1. <span data-ttu-id="f7b39-149">Klicken Sie in **Projektmappen-Explorer** mit der rechten Maustaste auf das Projekt " **vererancetest** ", und wählen Sie **Hinzufügen** und dann **Neues Element** aus.</span><span class="sxs-lookup"><span data-stu-id="f7b39-149">In **Solution Explorer**, right-click the **InheritanceTest** project, select **Add**, and then select **New Item**.</span></span>

2. <span data-ttu-id="f7b39-150">Wählen Sie im Dialogfeld **Neues Element hinzufügen** die Kategorie **Windows Forms** aus (wenn Sie eine Liste mit Kategorien haben), und wählen Sie dann die Vorlage **geerbte Formulare aus** .</span><span class="sxs-lookup"><span data-stu-id="f7b39-150">In the **Add New Item** dialog box, select the **Windows Forms** category (if you have a list of categories) and then select the **Inherited Form** template.</span></span>

3. <span data-ttu-id="f7b39-151">Belassen Sie den Standardnamen von, `Form2` und klicken Sie dann auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="f7b39-151">Leave the default name of `Form2` and then click **Add**.</span></span>

4. <span data-ttu-id="f7b39-152">Wählen Sie im Dialogfeld **Vererbungs** Auswahl die Option **Form1** aus dem **BaseFormLibrary** -Projekt als Formular aus, von dem geerbt werden soll, und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="f7b39-152">In the **Inheritance Picker** dialog box, select **Form1** from the **BaseFormLibrary** project as the form to inherit from and click **OK**.</span></span>

     <span data-ttu-id="f7b39-153">Dadurch wird ein Formular im **vererancetest** -Projekt erstellt, das aus dem Formular in **BaseFormLibrary** abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="f7b39-153">This creates a form in the **InheritanceTest** project that derives from the form in **BaseFormLibrary**.</span></span>

5. <span data-ttu-id="f7b39-154">Öffnen Sie das geerbte Formular (**Form2**) im Designer, indem Sie darauf doppelklicken, wenn es nicht bereits geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="f7b39-154">Open the inherited form (**Form2**) in the designer by double-clicking it, if it is not already open.</span></span>

    <span data-ttu-id="f7b39-155">Im Designer verfügen die geerbten Schaltflächen über ein Symbol (</span><span class="sxs-lookup"><span data-stu-id="f7b39-155">In the designer, the inherited buttons have a symbol (</span></span>![Screenshot des Visual Basic Vererbungs Symbols](./media/walkthrough-demonstrating-visual-inheritance/visual-basic-inheritance-glyph.gif)<span data-ttu-id="f7b39-157">) in der oberen Ecke, das angibt, dass Sie geerbt werden.</span><span class="sxs-lookup"><span data-stu-id="f7b39-157">) in their upper corner, indicating they are inherited.</span></span>

6. <span data-ttu-id="f7b39-158">Wählen Sie die Schaltfläche "Hello" ( **Hallo** ) aus, und beobachten Sie die Handles</span><span class="sxs-lookup"><span data-stu-id="f7b39-158">Select the **Say Hello** button and observe the resize handles.</span></span> <span data-ttu-id="f7b39-159">Da diese Schaltfläche geschützt ist, können die Erben sie verschieben, ihre Größe ändern, ihre Beschriftung ändern und andere Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="f7b39-159">Because this button is protected, the inheritors can move it, resize it, change its caption, and make other modifications.</span></span>

7. <span data-ttu-id="f7b39-160">Wählen Sie die private Schaltfläche " **Goodbye** " aus, und beachten Sie, dass Sie keine Handles zur Größenänderung hat.</span><span class="sxs-lookup"><span data-stu-id="f7b39-160">Select the private **Say Goodbye** button, and notice that it does not have resize handles.</span></span> <span data-ttu-id="f7b39-161">Außerdem sind im **Eigenschaften** Fenster die Eigenschaften dieser Schaltfläche ausgegraut, um anzugeben, dass Sie nicht geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="f7b39-161">Additionally, in the **Properties** window, the properties of this button are grayed to indicate they cannot be modified.</span></span>

8. <span data-ttu-id="f7b39-162">Bei Verwendung von Visual c#:</span><span class="sxs-lookup"><span data-stu-id="f7b39-162">If you are using Visual C#:</span></span>

    1. <span data-ttu-id="f7b39-163">Klicken Sie in **Projektmappen-Explorer** mit der rechten Maustaste im Projekt " **vererancetest** " auf **Form1** , und wählen Sie dann **Löschen** aus.</span><span class="sxs-lookup"><span data-stu-id="f7b39-163">In **Solution Explorer**, right-click **Form1** in the **InheritanceTest** project and then choose **Delete**.</span></span> <span data-ttu-id="f7b39-164">Klicken Sie im angezeigten Meldungs Feld auf **OK** , um den Löschvorgang zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="f7b39-164">In the message box that appears, click **OK** to confirm the deletion.</span></span>

    2. <span data-ttu-id="f7b39-165">Öffnen Sie die Datei "Program.cs", und ändern Sie die Zeile `Application.Run(new Form1());` in `Application.Run(new Form2());`.</span><span class="sxs-lookup"><span data-stu-id="f7b39-165">Open the Program.cs file and change the line `Application.Run(new Form1());` to `Application.Run(new Form2());`.</span></span>

9. <span data-ttu-id="f7b39-166">Klicken Sie in **Projektmappen-Explorer** mit der rechten Maustaste auf das Projekt **vererancetest** , und wählen Sie **als Startprojekt festlegen** aus.</span><span class="sxs-lookup"><span data-stu-id="f7b39-166">In **Solution Explorer**, right-click the **InheritanceTest** project and select **Set As Startup Project**.</span></span>

10. <span data-ttu-id="f7b39-167">Klicken Sie in **Projektmappen-Explorer** mit der rechten Maustaste auf das Projekt **vererancetest** , und wählen Sie **Eigenschaften** aus.</span><span class="sxs-lookup"><span data-stu-id="f7b39-167">In **Solution Explorer**, right-click the **InheritanceTest** project and select **Properties**.</span></span>

11. <span data-ttu-id="f7b39-168">Legen Sie auf den Eigenschaften Seiten von **vererancetest** das **Start Objekt** auf das geerbte Formular (**Form2**) fest.</span><span class="sxs-lookup"><span data-stu-id="f7b39-168">In the **InheritanceTest** property pages, set the **Startup object** to be the inherited form (**Form2**).</span></span>

12. <span data-ttu-id="f7b39-169">Drücken Sie **F5** , um die Anwendung auszuführen, und beobachten Sie das Verhalten des geerbten Formulars.</span><span class="sxs-lookup"><span data-stu-id="f7b39-169">Press **F5** to run the application, and observe the behavior of the inherited form.</span></span>

## <a name="next-steps"></a><span data-ttu-id="f7b39-170">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="f7b39-170">Next steps</span></span>

<span data-ttu-id="f7b39-171">Die Vererbung bei Benutzersteuerelementen funktioniert größtenteils auf die gleiche Weise.</span><span class="sxs-lookup"><span data-stu-id="f7b39-171">Inheritance for user controls works in much the same way.</span></span> <span data-ttu-id="f7b39-172">Öffnen Sie ein neues Klassenbibliotheksprojekt, und fügen Sie ein Benutzersteuerelement hinzu.</span><span class="sxs-lookup"><span data-stu-id="f7b39-172">Open a new class library project and add a user control.</span></span> <span data-ttu-id="f7b39-173">Platzieren Sie konstituierende Steuerelemente darauf, und kompilieren Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="f7b39-173">Place constituent controls on it and compile the project.</span></span> <span data-ttu-id="f7b39-174">Öffnen Sie ein weiteres, neues Klassenbibliotheksprojekt, und fügen Sie einen Verweis auf die kompilierte Klassenbibliothek hinzu.</span><span class="sxs-lookup"><span data-stu-id="f7b39-174">Open another new class library project and add a reference to the compiled class library.</span></span> <span data-ttu-id="f7b39-175">Fügen Sie dem Projekt außerdem ein geerbtes Steuerelement (über das Dialogfeld **neue Elemente hinzufügen** ) hinzu, und verwenden Sie die **Vererbungs** Auswahl.</span><span class="sxs-lookup"><span data-stu-id="f7b39-175">Also, try adding an inherited control (through the **Add New Items** dialog box) to the project and using the **Inheritance Picker**.</span></span> <span data-ttu-id="f7b39-176">Fügen Sie ein Benutzer Steuerelement hinzu, und ändern Sie die- `Inherits` `:` Anweisung (in Visual c#).</span><span class="sxs-lookup"><span data-stu-id="f7b39-176">Add a user control, and change the `Inherits` (`:` in Visual C#) statement.</span></span> <span data-ttu-id="f7b39-177">Weitere Informationen finden Sie unter Gewusst [wie: Erben von Windows Forms](how-to-inherit-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="f7b39-177">For more information, see [How to: Inherit Windows Forms](how-to-inherit-windows-forms.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="f7b39-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7b39-178">See also</span></span>

- [<span data-ttu-id="f7b39-179">Vorgehensweise: Erben von Windows Forms</span><span class="sxs-lookup"><span data-stu-id="f7b39-179">How to: Inherit Windows Forms</span></span>](how-to-inherit-windows-forms.md)
- [<span data-ttu-id="f7b39-180">Visuelle Vererbung in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="f7b39-180">Windows Forms Visual Inheritance</span></span>](windows-forms-visual-inheritance.md)
- [<span data-ttu-id="f7b39-181">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="f7b39-181">Windows Forms</span></span>](../index.yml)
