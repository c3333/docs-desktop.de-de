---
title: Entwickeln Sie ein einfaches Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms]
- custom controls [Windows Forms], creating simple controls using code
- Control class [Windows Forms], Windows Forms
ms.assetid: 86cbe435-45b7-4cb4-9b5a-47418369758d
ms.openlocfilehash: af8ba82cc5699a4b6a12eaf921dd9f4cbf3cecd1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975664"
---
# <a name="how-to-develop-a-simple-windows-forms-control"></a><span data-ttu-id="5cda6-102">Vorgehensweise: Entwickeln eines einfachen Windows Forms-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="5cda6-102">How to: Develop a Simple Windows Forms Control</span></span>

<span data-ttu-id="5cda6-103">Dieser Abschnitt führt Sie durch die wichtigsten Schritte zum Erstellen von benutzerdefinierten Windows Forms-Steuerelementen.</span><span class="sxs-lookup"><span data-stu-id="5cda6-103">This section walks you through the key steps for authoring a custom Windows Forms control.</span></span> <span data-ttu-id="5cda6-104">Das in dieser exemplarischen Vorgehensweise entwickelte einfache Steuerelement ermöglicht die Änderung der Ausrichtung der- <xref:System.Windows.Forms.Control.Text%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5cda6-104">The simple control developed in this walkthrough allows the alignment of its <xref:System.Windows.Forms.Control.Text%2A> property to be changed.</span></span> <span data-ttu-id="5cda6-105">Es löst keine Ereignisse aus oder behandelt sie.</span><span class="sxs-lookup"><span data-stu-id="5cda6-105">It does not raise or handle events.</span></span>

### <a name="to-create-a-simple-custom-control"></a><span data-ttu-id="5cda6-106">So erstellen Sie ein einfaches benutzerdefiniertes Steuerelement</span><span class="sxs-lookup"><span data-stu-id="5cda6-106">To create a simple custom control</span></span>

1. <span data-ttu-id="5cda6-107">Definieren Sie eine Klasse, die sich von <xref:System.Windows.Forms.Control?displayProperty=nameWithType> ableitet.</span><span class="sxs-lookup"><span data-stu-id="5cda6-107">Define a class that derives from <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span>

    ```vb
    Public Class FirstControl
       Inherits Control

    End Class
    ```

    ```csharp
    public class FirstControl:Control {}
    ```

2. <span data-ttu-id="5cda6-108">Definieren Sie Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5cda6-108">Define properties.</span></span> <span data-ttu-id="5cda6-109">(Sie müssen keine Eigenschaften definieren, da ein Steuerelement viele Eigenschaften von der-Klasse erbt <xref:System.Windows.Forms.Control> , aber die meisten benutzerdefinierten Steuerelemente definieren in der Regel zusätzliche Eigenschaften.) Das folgende Code Fragment definiert eine Eigenschaft mit dem Namen `TextAlignment` , die `FirstControl` verwendet, um die Anzeige der <xref:System.Windows.Forms.Control.Text%2A> von geerbten Eigenschaft zu formatieren <xref:System.Windows.Forms.Control> .</span><span class="sxs-lookup"><span data-stu-id="5cda6-109">(You are not required to define properties, because a control inherits many properties from the <xref:System.Windows.Forms.Control> class, but most custom controls generally do define additional properties.) The following code fragment defines a property named `TextAlignment` that `FirstControl` uses to format the display of the <xref:System.Windows.Forms.Control.Text%2A> property inherited from <xref:System.Windows.Forms.Control>.</span></span> <span data-ttu-id="5cda6-110">Weitere Informationen zum Definieren von Eigenschaften finden Sie in der [Übersicht über Eigenschaften](/previous-versions/visualstudio/visual-studio-2013/65zdfbdt(v%3dvs.120)).</span><span class="sxs-lookup"><span data-stu-id="5cda6-110">For more information about defining properties, see [Properties Overview](/previous-versions/visualstudio/visual-studio-2013/65zdfbdt(v%3dvs.120)).</span></span>

     [!code-csharp[System.Windows.Forms.FirstControl#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FirstControl/CS/FirstControl.cs#3)]
     [!code-vb[System.Windows.Forms.FirstControl#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FirstControl/VB/FirstControl.vb#3)]

     <span data-ttu-id="5cda6-111">Wenn Sie eine Eigenschaft festlegen, die die visuelle Darstellung des Steuer Elements ändert, müssen Sie die-Methode aufrufen, <xref:System.Windows.Forms.Control.Invalidate%2A> um das Steuerelement neu zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="5cda6-111">When you set a property that changes the visual display of the control, you must invoke the <xref:System.Windows.Forms.Control.Invalidate%2A> method to redraw the control.</span></span> <span data-ttu-id="5cda6-112"><xref:System.Windows.Forms.Control.Invalidate%2A> wird in der-Basisklasse definiert <xref:System.Windows.Forms.Control> .</span><span class="sxs-lookup"><span data-stu-id="5cda6-112"><xref:System.Windows.Forms.Control.Invalidate%2A> is defined in the base class <xref:System.Windows.Forms.Control>.</span></span>

3. <span data-ttu-id="5cda6-113">Überschreiben Sie die <xref:System.Windows.Forms.Control.OnPaint%2A> von geerbte geschützte Methode <xref:System.Windows.Forms.Control> , um dem Steuerelement Renderinglogik bereitzustellen</span><span class="sxs-lookup"><span data-stu-id="5cda6-113">Override the protected <xref:System.Windows.Forms.Control.OnPaint%2A> method inherited from <xref:System.Windows.Forms.Control> to provide rendering logic to your control.</span></span> <span data-ttu-id="5cda6-114">Wenn Sie nicht überschreiben <xref:System.Windows.Forms.Control.OnPaint%2A> , kann das Steuerelement nicht selbst gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="5cda6-114">If you do not override <xref:System.Windows.Forms.Control.OnPaint%2A>, your control will not be able to draw itself.</span></span> <span data-ttu-id="5cda6-115">Im folgenden Code Fragment zeigt die- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode die <xref:System.Windows.Forms.Control.Text%2A> von geerbte-Eigenschaft <xref:System.Windows.Forms.Control> mit der durch das-Feld angegebenen Ausrichtung an `alignmentValue` .</span><span class="sxs-lookup"><span data-stu-id="5cda6-115">In the following code fragment, the <xref:System.Windows.Forms.Control.OnPaint%2A> method displays the <xref:System.Windows.Forms.Control.Text%2A> property inherited from <xref:System.Windows.Forms.Control> with the alignment specified by the `alignmentValue` field.</span></span>

     [!code-csharp[System.Windows.Forms.FirstControl#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FirstControl/CS/FirstControl.cs#4)]
     [!code-vb[System.Windows.Forms.FirstControl#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FirstControl/VB/FirstControl.vb#4)]

4. <span data-ttu-id="5cda6-116">Stellen Sie Attribute für das Steuerelement bereit.</span><span class="sxs-lookup"><span data-stu-id="5cda6-116">Provide attributes for your control.</span></span> <span data-ttu-id="5cda6-117">Attribute ermöglichen es einem visuellen Designer, Ihr Steuerelement und dessen Eigenschaften und Ereignisse entsprechend zur Entwurfszeit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5cda6-117">Attributes enable a visual designer to display your control and its properties and events appropriately at design time.</span></span> <span data-ttu-id="5cda6-118">Das folgende Codefragment wendet die Attribute auf die Eigenschaft `TextAlignment` an.</span><span class="sxs-lookup"><span data-stu-id="5cda6-118">The following code fragment applies attributes to the `TextAlignment` property.</span></span> <span data-ttu-id="5cda6-119">In einem Designer, wie z. b. Visual Studio, bewirkt das- <xref:System.ComponentModel.CategoryAttribute.Category%2A> Attribut (im Code Fragment gezeigt), dass die Eigenschaft unter einer logischen Kategorie angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5cda6-119">In a designer such as Visual Studio, the <xref:System.ComponentModel.CategoryAttribute.Category%2A> attribute (shown in the code fragment) causes the property to be displayed under a logical category.</span></span> <span data-ttu-id="5cda6-120">Das- <xref:System.ComponentModel.DescriptionAttribute.Description%2A> Attribut bewirkt, dass eine beschreibende Zeichenfolge im unteren Bereich des **Eigenschaften** Fensters angezeigt wird, wenn die- `TextAlignment` Eigenschaft ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="5cda6-120">The <xref:System.ComponentModel.DescriptionAttribute.Description%2A> attribute causes a descriptive string to be displayed at the bottom of the **Properties** window when the `TextAlignment` property is selected.</span></span> <span data-ttu-id="5cda6-121">Weitere Informationen zu Attributen finden Sie unter [Entwurfszeitattribute für Komponenten](/previous-versions/visualstudio/visual-studio-2013/tk67c2t8(v=vs.120)).</span><span class="sxs-lookup"><span data-stu-id="5cda6-121">For more information about attributes, see [Design-Time Attributes for Components](/previous-versions/visualstudio/visual-studio-2013/tk67c2t8(v=vs.120)).</span></span>

     [!code-csharp[System.Windows.Forms.FirstControl#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FirstControl/CS/FirstControl.cs#5)]
     [!code-vb[System.Windows.Forms.FirstControl#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FirstControl/VB/FirstControl.vb#5)]

5. <span data-ttu-id="5cda6-122">(optional) Stellen Sie Ressourcen für Ihr Steuerelement zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="5cda6-122">(optional) Provide resources for your control.</span></span> <span data-ttu-id="5cda6-123">Sie können eine Ressource, z.B. eine Bitmap für das Steuerelement mit einer Compileroption bereitstellen (`/res` für C#), um Ressourcen mit dem Steuerelement zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="5cda6-123">You can provide a resource, such as a bitmap, for your control by using a compiler option (`/res` for C#) to package resources with your control.</span></span> <span data-ttu-id="5cda6-124">Zur Laufzeit kann die Ressource mithilfe der Methoden der-Klasse abgerufen werden <xref:System.Resources.ResourceManager> .</span><span class="sxs-lookup"><span data-stu-id="5cda6-124">At run time, the resource can be retrieved using the methods of the <xref:System.Resources.ResourceManager> class.</span></span> <span data-ttu-id="5cda6-125">Weitere Informationen zum Erstellen und Verwenden von Ressourcen finden Sie unter [Ressourcen in Desktop-Apps](/dotnet/framework/resources/index).</span><span class="sxs-lookup"><span data-stu-id="5cda6-125">For more information about creating and using resources, see the [Resources in Desktop Apps](/dotnet/framework/resources/index).</span></span>

6. <span data-ttu-id="5cda6-126">Kompilieren Sie das Steuerelement, und stellen Sie es bereit.</span><span class="sxs-lookup"><span data-stu-id="5cda6-126">Compile and deploy your control.</span></span> <span data-ttu-id="5cda6-127">Führen Sie die folgenden Schritte aus, um `FirstControl,` zu kompilieren und bereitzustellen:</span><span class="sxs-lookup"><span data-stu-id="5cda6-127">To compile and deploy `FirstControl,` execute the following steps:</span></span>

    1. <span data-ttu-id="5cda6-128">Speichern Sie den Code im folgenden Beispiel als Quelldatei (z.B. als „FirstControl.cs“ oder „FirstControl.vb“).</span><span class="sxs-lookup"><span data-stu-id="5cda6-128">Save the code in the following sample to a source file (such as FirstControl.cs or FirstControl.vb).</span></span>

    2. <span data-ttu-id="5cda6-129">Kompilieren Sie den Quellcode in eine Assembly, und speichern Sie sie im Verzeichnis der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5cda6-129">Compile the source code into an assembly and save it in your application's directory.</span></span> <span data-ttu-id="5cda6-130">Führen Sie hierfür den folgenden Befehl in dem Verzeichnis aus, das die Quelldatei enthält.</span><span class="sxs-lookup"><span data-stu-id="5cda6-130">To accomplish this, execute the following command from the directory that contains the source file.</span></span>

        ```console
        vbc -t:library -out:[path to your application's directory]/CustomWinControls.dll -r:System.dll -r:System.Windows.Forms.dll -r:System.Drawing.dll FirstControl.vb
        ```

        ```console
        csc -t:library -out:[path to your application's directory]/CustomWinControls.dll -r:System.dll -r:System.Windows.Forms.dll -r:System.Drawing.dll FirstControl.cs
        ```

         <span data-ttu-id="5cda6-131">Die Compileroption `/t:library` benachrichtigt den Compiler, dass es sich bei der erstellten Assembly um eine Bibliothek handelt (nicht um eine ausführbare Assembly).</span><span class="sxs-lookup"><span data-stu-id="5cda6-131">The `/t:library` compiler option tells the compiler that the assembly you are creating is a library (and not an executable).</span></span> <span data-ttu-id="5cda6-132">Die Option `/out` gibt den Pfad und den Namen der Assembly an.</span><span class="sxs-lookup"><span data-stu-id="5cda6-132">The `/out` option specifies the path and name of the assembly.</span></span> <span data-ttu-id="5cda6-133">Die Option `/r` gibt den Namen der Assembly an, auf die durch Ihren Code verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5cda6-133">The`/r` option provides the name of the assemblies that are referenced by your code.</span></span> <span data-ttu-id="5cda6-134">In diesem Beispiel erstellen Sie eine private Assembly, die ausschließlich von Ihren Anwendungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5cda6-134">In this example, you create a private assembly that only your applications can use.</span></span> <span data-ttu-id="5cda6-135">Daher müssen Sie sie im Verzeichnis der Anwendung speichern.</span><span class="sxs-lookup"><span data-stu-id="5cda6-135">Hence, you have to save it in your application's directory.</span></span> <span data-ttu-id="5cda6-136">Weitere Informationen über das Packen und Bereitstellen eines Steuerelements für die Verteilung finden Sie unter [Bereitstellung](/dotnet/framework/deployment/index).</span><span class="sxs-lookup"><span data-stu-id="5cda6-136">For more information about packaging and deploying a control for distribution, see [Deployment](/dotnet/framework/deployment/index).</span></span>

<span data-ttu-id="5cda6-137">Das folgende Beispiel zeigt den Code für `FirstControl`.</span><span class="sxs-lookup"><span data-stu-id="5cda6-137">The following sample shows the code for `FirstControl`.</span></span> <span data-ttu-id="5cda6-138">Das Steuerelement ist im Namespace `CustomWinControls` enthalten.</span><span class="sxs-lookup"><span data-stu-id="5cda6-138">The control is enclosed in the namespace `CustomWinControls`.</span></span> <span data-ttu-id="5cda6-139">Ein Namespace bietet eine logische Gruppierung von verwandten Typen.</span><span class="sxs-lookup"><span data-stu-id="5cda6-139">A namespace provides a logical grouping of related types.</span></span> <span data-ttu-id="5cda6-140">Sie können das Steuerelement in einem neuen oder vorhandenen Namespace erstellen.</span><span class="sxs-lookup"><span data-stu-id="5cda6-140">You can create your control in a new or existing namespace.</span></span> <span data-ttu-id="5cda6-141">In C# ermöglicht die Deklaration `using` (`Imports` in Visual Basic), dass auf Typen von einem Namespace zugegriffen wird, ohne dass der vollqualifizierte Name des Typs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5cda6-141">In C#, the `using` declaration (in Visual Basic, `Imports`) allows types to be accessed from a namespace without using the fully qualified name of the type.</span></span> <span data-ttu-id="5cda6-142">Im folgenden Beispiel ermöglicht die- `using` Deklaration, dass Code von einfach auf die-Klasse zugreifen kann, <xref:System.Windows.Forms.Control> <xref:System.Windows.Forms?displayProperty=nameWithType> <xref:System.Windows.Forms.Control> anstatt den voll qualifizierten Namen zu verwenden <xref:System.Windows.Forms.Control?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="5cda6-142">In the following example, the `using` declaration allows code to access the class <xref:System.Windows.Forms.Control> from <xref:System.Windows.Forms?displayProperty=nameWithType> as simply <xref:System.Windows.Forms.Control> instead of having to use the fully qualified name <xref:System.Windows.Forms.Control?displayProperty=nameWithType>.</span></span>

[!code-csharp[System.Windows.Forms.FirstControl#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FirstControl/CS/FirstControl.cs#1)]
[!code-vb[System.Windows.Forms.FirstControl#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FirstControl/VB/FirstControl.vb#1)]

## <a name="using-the-custom-control-on-a-form"></a><span data-ttu-id="5cda6-143">Verwenden des benutzerdefinierten Steuerelements in einem Formular</span><span class="sxs-lookup"><span data-stu-id="5cda6-143">Using the Custom Control on a Form</span></span>

<span data-ttu-id="5cda6-144">Im folgenden Beispiel wird ein einfaches Formular dargestellt, dass `FirstControl` verwendet.</span><span class="sxs-lookup"><span data-stu-id="5cda6-144">The following example shows a simple form that uses `FirstControl`.</span></span> <span data-ttu-id="5cda6-145">Es erstellt drei Instanzen von `FirstControl`, jede mit einem anderen Wert für die Eigenschaft `TextAlignment`.</span><span class="sxs-lookup"><span data-stu-id="5cda6-145">It creates three instances of `FirstControl`, each with a different value for the `TextAlignment` property.</span></span>

#### <a name="to-compile-and-run-this-sample"></a><span data-ttu-id="5cda6-146">So kompilieren Sie dieses Beispiel und führen es aus</span><span class="sxs-lookup"><span data-stu-id="5cda6-146">To compile and run this sample</span></span>

1. <span data-ttu-id="5cda6-147">Speichern Sie den Code im folgenden Beispiel als Quelldatei („SimpleForm.cs“ oder „SimpleForms.vb“).</span><span class="sxs-lookup"><span data-stu-id="5cda6-147">Save the code in the following example to a source file (SimpleForm.cs or SimpleForms.vb).</span></span>

2. <span data-ttu-id="5cda6-148">Kompilieren Sie den Quellcode in eine ausführbare Assembly, indem Sie den folgenden Befehl im Verzeichnis ausführen, das die Quelldatei enthält.</span><span class="sxs-lookup"><span data-stu-id="5cda6-148">Compile the source code into an executable assembly by executing the following command from the directory that contains the source file.</span></span>

    ```console
    vbc -r:CustomWinControls.dll -r:System.dll -r:System.Windows.Forms.dll -r:System.Drawing.dll SimpleForm.vb
    ```

    ```console
    csc -r:CustomWinControls.dll -r:System.dll -r:System.Windows.Forms.dll -r:System.Drawing.dll SimpleForm.cs
    ```

     <span data-ttu-id="5cda6-149">CustomWinControls.dll ist die Assembly, die die-Klasse enthält `FirstControl` .</span><span class="sxs-lookup"><span data-stu-id="5cda6-149">CustomWinControls.dll is the assembly that contains the class `FirstControl`.</span></span> <span data-ttu-id="5cda6-150">Diese Assembly muss sich im gleichen Verzeichnis befinden wie die Quelldatei für das Formular, das auf sie zugreift („SimpleForm.cs“ oder „SimpleForms.vb“).</span><span class="sxs-lookup"><span data-stu-id="5cda6-150">This assembly must be in the same directory as the source file for the form that accesses it (SimpleForm.cs or SimpleForms.vb).</span></span>

3. <span data-ttu-id="5cda6-151">Führen Sie „SimpleForm.exe“ mit dem folgenden Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="5cda6-151">Execute SimpleForm.exe using the following command.</span></span>

    ```console
    SimpleForm
    ```

[!code-csharp[System.Windows.Forms.FirstControl#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.FirstControl/CS/SimpleForm.cs#10)]
[!code-vb[System.Windows.Forms.FirstControl#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.FirstControl/VB/SimpleForm.vb#10)]

## <a name="see-also"></a><span data-ttu-id="5cda6-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cda6-152">See also</span></span>

- [<span data-ttu-id="5cda6-153">Eigenschaften von Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="5cda6-153">Properties in Windows Forms Controls</span></span>](properties-in-windows-forms-controls.md)
- [<span data-ttu-id="5cda6-154">Ereignisse in Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="5cda6-154">Events in Windows Forms Controls</span></span>](events-in-windows-forms-controls.md)
