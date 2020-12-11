---
title: Erben von vorhandenen Steuerelementen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- inheritance [Windows Forms], Windows Forms custom controls
- custom controls [Windows Forms], inheritance
ms.assetid: 1e1fc8ea-c615-4cf0-a356-16d6df7444ab
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: de9e4dc9e358092934e9326dd08c687478fac57b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976292"
---
# <a name="how-to-inherit-from-existing-windows-forms-controls"></a><span data-ttu-id="61bbc-102">Gewusst wie: Erben von vorhandenen Windows Forms-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="61bbc-102">How to: Inherit from Existing Windows Forms Controls</span></span>

<span data-ttu-id="61bbc-103">Wenn Sie die Funktionalität eines vorhandenen Steuerelements erweitern möchten, können Sie ein Steuerelement erstellen, dass durch Vererbung von einem vorhandenen Steuerelement abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="61bbc-103">If you want to extend the functionality of an existing control, you can create a control derived from an existing control through inheritance.</span></span> <span data-ttu-id="61bbc-104">Beim Erben von einem vorhandenen Steuerelement erben Sie die gesamte Funktionalität und die visuellen Eigenschaften dieses Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="61bbc-104">When inheriting from an existing control, you inherit all of the functionality and visual properties of that control.</span></span> <span data-ttu-id="61bbc-105">Wenn Sie z. b. ein Steuerelement erstellen, das von geerbt <xref:System.Windows.Forms.Button> wurde, würde das neue Steuerelement Aussehen und genauso vorgehen wie ein Standard <xref:System.Windows.Forms.Button> Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="61bbc-105">For example, if you were creating a control that inherited from <xref:System.Windows.Forms.Button>, your new control would look and act exactly like a standard <xref:System.Windows.Forms.Button> control.</span></span> <span data-ttu-id="61bbc-106">Sie können die Funktionalität Ihres neuen Steuerelements durch Implementieren von benutzerdefinierten Methoden und Eigenschaften erweitern oder ändern.</span><span class="sxs-lookup"><span data-stu-id="61bbc-106">You could then extend or modify the functionality of your new control through the implementation of custom methods and properties.</span></span> <span data-ttu-id="61bbc-107">In einigen Steuerelementen können Sie auch die visuelle Darstellung des geerbten Steuer Elements ändern, indem Sie die zugehörige-Methode überschreiben <xref:System.Windows.Forms.Control.OnPaint%2A> .</span><span class="sxs-lookup"><span data-stu-id="61bbc-107">In some controls, you can also change the visual appearance of your inherited control by overriding its <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span>

## <a name="to-create-an-inherited-control"></a><span data-ttu-id="61bbc-108">So erstellen Sie ein geerbtes Steuerelement</span><span class="sxs-lookup"><span data-stu-id="61bbc-108">To create an inherited control</span></span>

1. <span data-ttu-id="61bbc-109">Erstellen Sie in Visual Studio ein neues **Windows Forms-Anwendungs** Projekt.</span><span class="sxs-lookup"><span data-stu-id="61bbc-109">In Visual Studio, create a new **Windows Forms Application** project.</span></span>

1. <span data-ttu-id="61bbc-110">Wählen Sie im Menü **Projekt** die Option **Neues Element hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="61bbc-110">From the **Project** menu, choose **Add New Item**.</span></span>

    <span data-ttu-id="61bbc-111">Das Dialogfeld **Neues Element hinzufügen** wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="61bbc-111">The **Add New Item** dialog box appears.</span></span>

1. <span data-ttu-id="61bbc-112">Doppelklicken Sie im Dialogfeld **Neues Element hinzufügen** auf **Benutzerdefiniertes Steuerelement**.</span><span class="sxs-lookup"><span data-stu-id="61bbc-112">In the **Add New Item** dialog box, double-click **Custom Control**.</span></span>

    <span data-ttu-id="61bbc-113">Ein neues benutzerdefiniertes Steuerelement wird zu Ihrem Projekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="61bbc-113">A new custom control is added to your project.</span></span>

1. <span data-ttu-id="61bbc-114">Wenn Sie Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="61bbc-114">If you're using:</span></span>

    - <span data-ttu-id="61bbc-115">Klicken Sie Visual Basic oben in **Projektmappen-Explorer** auf **alle Dateien anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="61bbc-115">Visual Basic, at the top of **Solution Explorer**, click **Show All Files**.</span></span> <span data-ttu-id="61bbc-116">Erweitern Sie „CustomControl1.vb“ und öffnen Sie „CustomControl1.Designer.vb“ im Code-Editor.</span><span class="sxs-lookup"><span data-stu-id="61bbc-116">Expand CustomControl1.vb and then open CustomControl1.Designer.vb in the Code Editor.</span></span>
    - <span data-ttu-id="61bbc-117">C#, öffnen Sie CustomControl1.cs im Code-Editor.</span><span class="sxs-lookup"><span data-stu-id="61bbc-117">C#, open CustomControl1.cs in the Code Editor.</span></span>

1. <span data-ttu-id="61bbc-118">Suchen Sie nach der Klassen Deklaration, die von erbt <xref:System.Windows.Forms.Control> .</span><span class="sxs-lookup"><span data-stu-id="61bbc-118">Locate the class declaration, which inherits from <xref:System.Windows.Forms.Control>.</span></span>

1. <span data-ttu-id="61bbc-119">Ändern Sie die Basisklasse in das Steuerelement, von dem Sie erben möchten.</span><span class="sxs-lookup"><span data-stu-id="61bbc-119">Change the base class to the control that you want to inherit from.</span></span>

     <span data-ttu-id="61bbc-120">Wenn Sie z. b. von erben möchten <xref:System.Windows.Forms.Button> , ändern Sie die Klassen Deklaration wie folgt:</span><span class="sxs-lookup"><span data-stu-id="61bbc-120">For example, if you want to inherit from <xref:System.Windows.Forms.Button>, change the class declaration to the following:</span></span>

    ```vb
    Partial Class CustomControl1
        Inherits System.Windows.Forms.Button
    ```

    ```csharp
    public partial class CustomControl1 : System.Windows.Forms.Button
    ```

1. <span data-ttu-id="61bbc-121">Wenn Sie Visual Basic verwenden, speichern und schließen Sie „CustomControl1.Designer.vb“.</span><span class="sxs-lookup"><span data-stu-id="61bbc-121">If you are using Visual Basic, save and close CustomControl1.Designer.vb.</span></span> <span data-ttu-id="61bbc-122">Öffnen Sie „CustomControl1.vb“ im Code-Editor.</span><span class="sxs-lookup"><span data-stu-id="61bbc-122">Open CustomControl1.vb in the Code Editor.</span></span>

1. <span data-ttu-id="61bbc-123">Implementieren Sie alle benutzerdefinierten Methoden oder Eigenschaften, die in das Steuerelement eingebunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="61bbc-123">Implement any custom methods or properties that your control will incorporate.</span></span>

1. <span data-ttu-id="61bbc-124">Wenn Sie die grafische Darstellung des Steuer Elements ändern möchten, überschreiben Sie die- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode.</span><span class="sxs-lookup"><span data-stu-id="61bbc-124">If you want to modify the graphical appearance of your control, override the <xref:System.Windows.Forms.Control.OnPaint%2A> method.</span></span>

    > [!NOTE]
    > <span data-ttu-id="61bbc-125">Wenn <xref:System.Windows.Forms.Control.OnPaint%2A> Sie überschreiben, können Sie die Darstellung aller Steuerelemente nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="61bbc-125">Overriding <xref:System.Windows.Forms.Control.OnPaint%2A> will not allow you to modify the appearance of all controls.</span></span> <span data-ttu-id="61bbc-126">Diese Steuerelemente, die alle Zeichnungen von Windows (z. b. <xref:System.Windows.Forms.TextBox> ) erledigen <xref:System.Windows.Forms.Control.OnPaint%2A> , werden nie Ihre-Methode aufruft und verwenden daher niemals den benutzerdefinierten Code.</span><span class="sxs-lookup"><span data-stu-id="61bbc-126">Those controls that have all of their painting done by Windows (for example, <xref:System.Windows.Forms.TextBox>) never call their <xref:System.Windows.Forms.Control.OnPaint%2A> method, and thus will never use the custom code.</span></span> <span data-ttu-id="61bbc-127">Informationen zur Verfügbarkeit der Methode finden Sie in der Hilfe Dokumentation für das jeweilige Steuerelement, das Sie ändern möchten <xref:System.Windows.Forms.Control.OnPaint%2A> .</span><span class="sxs-lookup"><span data-stu-id="61bbc-127">Refer to the Help documentation for the particular control you want to modify to see if the <xref:System.Windows.Forms.Control.OnPaint%2A> method is available.</span></span> <span data-ttu-id="61bbc-128">Eine Liste aller Windows Form-Steuerelemente finden Sie unter [Steuerelemente für Windows Forms](controls-to-use-on-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="61bbc-128">For a list of all the Windows Form Controls, see [Controls to Use on Windows Forms](controls-to-use-on-windows-forms.md).</span></span> <span data-ttu-id="61bbc-129">Wenn ein Steuerelement nicht <xref:System.Windows.Forms.Control.OnPaint%2A> als Element Methode aufgeführt ist, können Sie seine Darstellung nicht ändern, indem Sie diese Methode überschreiben.</span><span class="sxs-lookup"><span data-stu-id="61bbc-129">If a control does not have <xref:System.Windows.Forms.Control.OnPaint%2A> listed as a member method, you cannot alter its appearance by overriding this method.</span></span> <span data-ttu-id="61bbc-130">Weitere Informationen über benutzerdefinierte Darstellung finden Sie unter [Zeichnen und Ausgeben von benutzerdefinierten Steuerelementen](custom-control-painting-and-rendering.md).</span><span class="sxs-lookup"><span data-stu-id="61bbc-130">For more information about custom painting, see [Custom Control Painting and Rendering](custom-control-painting-and-rendering.md).</span></span>

    ```vb
    Protected Overrides Sub OnPaint(ByVal e As _
       System.Windows.Forms.PaintEventArgs)
       MyBase.OnPaint(e)
       ' Insert code to do custom painting.
       ' If you want to completely change the appearance of your control,
       ' do not call MyBase.OnPaint(e).
    End Sub
    ```

    ```csharp
    protected override void OnPaint(PaintEventArgs pe)
    {
       base.OnPaint(pe);
       // Insert code to do custom painting.
       // If you want to completely change the appearance of your control,
       // do not call base.OnPaint(pe).
    }
    ```

1. <span data-ttu-id="61bbc-131">Speichern und testen Sie das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="61bbc-131">Save and test your control.</span></span>

## <a name="see-also"></a><span data-ttu-id="61bbc-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61bbc-132">See also</span></span>

- [<span data-ttu-id="61bbc-133">Arten von benutzerdefinierten Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="61bbc-133">Varieties of Custom Controls</span></span>](varieties-of-custom-controls.md)
- [<span data-ttu-id="61bbc-134">Vorgehensweise: Erben von der Control-Klasse</span><span class="sxs-lookup"><span data-stu-id="61bbc-134">How to: Inherit from the Control Class</span></span>](how-to-inherit-from-the-control-class.md)
- [<span data-ttu-id="61bbc-135">How to: Erben von der UserControl-Klasse</span><span class="sxs-lookup"><span data-stu-id="61bbc-135">How to: Inherit from the UserControl Class</span></span>](how-to-inherit-from-the-usercontrol-class.md)
- [<span data-ttu-id="61bbc-136">Vorgehensweise: Erstellen von Steuerelementen für Windows Forms</span><span class="sxs-lookup"><span data-stu-id="61bbc-136">How to: Author Controls for Windows Forms</span></span>](how-to-author-controls-for-windows-forms.md)
- [<span data-ttu-id="61bbc-137">Problembehandlung für geerbte Ereignishandler in Visual Basic</span><span class="sxs-lookup"><span data-stu-id="61bbc-137">Troubleshooting Inherited Event Handlers in Visual Basic</span></span>](/dotnet/visual-basic/programming-guide/language-features/events/troubleshooting-inherited-event-handlers)
- [<span data-ttu-id="61bbc-138">Exemplarische Vorgehensweise: Vererben von einem Windows Forms-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="61bbc-138">Walkthrough: Inheriting from a Windows Forms Control</span></span>](walkthrough-inheriting-from-a-windows-forms-control-with-visual-csharp.md)
