---
title: Hinzufügen von Steuerelementen
description: Erfahren Sie, wie Sie ein Steuerelement in einem Windows Form zeichnen. Ein-Steuerelement ist eine Komponente in einem Formular, das Sie verwenden können, um Informationen anzuzeigen oder Benutzereingaben zu akzeptieren.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms controls, adding to form
- controls [Windows Forms], adding
ms.assetid: 2af86001-9d62-4154-87fb-66db2c3cd9fd
ms.openlocfilehash: 890c9d636661a7772f1208936bb9d5c2d36ad16a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975103"
---
# <a name="how-to-add-controls-to-windows-forms"></a><span data-ttu-id="4bcca-104">Gewusst wie: Hinzufügen von Steuerelementen zu Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4bcca-104">How to: Add Controls to Windows Forms</span></span>

<span data-ttu-id="4bcca-105">Die meisten Formulare werden durch das Hinzufügen von Steuerelementen zur Oberfläche des Formulars entworfen, um eine Benutzeroberfläche (UI) zu definieren.</span><span class="sxs-lookup"><span data-stu-id="4bcca-105">Most forms are designed by adding controls to the surface of the form to define a user interface (UI).</span></span> <span data-ttu-id="4bcca-106">Ein- *Steuer* Element ist eine Komponente auf einem Formular, mit dem Informationen angezeigt oder Benutzereingaben akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="4bcca-106">A *control* is a component on a form used to display information or accept user input.</span></span> <span data-ttu-id="4bcca-107">Weitere Informationen zu-Steuerelementen finden Sie unter Windows Forms-Steuer [Elemente](index.md).</span><span class="sxs-lookup"><span data-stu-id="4bcca-107">For more information about controls, see [Windows Forms Controls](index.md).</span></span>

## <a name="to-draw-a-control-on-a-form"></a><span data-ttu-id="4bcca-108">So zeichnen Sie ein Steuerelement in einem Formular</span><span class="sxs-lookup"><span data-stu-id="4bcca-108">To draw a control on a form</span></span>

1. <span data-ttu-id="4bcca-109">Öffnen Sie das Formular.</span><span class="sxs-lookup"><span data-stu-id="4bcca-109">Open the form.</span></span> <span data-ttu-id="4bcca-110">Weitere Informationen finden Sie unter Gewusst [wie: Anzeigen von Windows Forms im Designer](/previous-versions/visualstudio/visual-studio-2010/w5yd62ts(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="4bcca-110">For more information, see [How to: Display Windows Forms in the Designer](/previous-versions/visualstudio/visual-studio-2010/w5yd62ts(v=vs.100)).</span></span>

2. <span data-ttu-id="4bcca-111">Klicken Sie in der **Toolbox** auf das Steuerelement, das Sie dem Formular hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="4bcca-111">In the **Toolbox**, click the control you want to add to your form.</span></span>

3. <span data-ttu-id="4bcca-112">Klicken Sie im Formular auf die Stelle, an der sich die obere linke Ecke des Steuer Elements befinden soll, und ziehen Sie an die Stelle, an der die untere rechte Ecke des Steuer Elements platziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="4bcca-112">On the form, click where you want the upper-left corner of the control to be located, and drag to where you want the lower-right corner of the control to be located.</span></span>

    <span data-ttu-id="4bcca-113">Das-Steuerelement wird dem Formular mit der angegebenen Position und Größe hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4bcca-113">The control is added to the form with the specified location and size.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4bcca-114">Für jedes Steuerelement ist eine Standardgröße definiert.</span><span class="sxs-lookup"><span data-stu-id="4bcca-114">Each control has a default size defined.</span></span> <span data-ttu-id="4bcca-115">Sie können dem Formular ein Steuerelement in der Standardgröße des Steuer Elements hinzufügen, indem Sie es aus der **Toolbox** in das Formular ziehen.</span><span class="sxs-lookup"><span data-stu-id="4bcca-115">You can add a control to your form in the control's default size by dragging it from the **Toolbox** to the form.</span></span>

## <a name="to-drag-a-control-to-a-form"></a><span data-ttu-id="4bcca-116">So ziehen Sie ein Steuerelement in ein Formular</span><span class="sxs-lookup"><span data-stu-id="4bcca-116">To drag a control to a form</span></span>

1. <span data-ttu-id="4bcca-117">Öffnen Sie das Formular.</span><span class="sxs-lookup"><span data-stu-id="4bcca-117">Open the form.</span></span> <span data-ttu-id="4bcca-118">Weitere Informationen finden Sie unter Gewusst [wie: Anzeigen von Windows Forms im Designer](/previous-versions/visualstudio/visual-studio-2010/w5yd62ts(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="4bcca-118">For more information, see [How to: Display Windows Forms in the Designer](/previous-versions/visualstudio/visual-studio-2010/w5yd62ts(v=vs.100)).</span></span>

2. <span data-ttu-id="4bcca-119">Klicken Sie in der **Toolbox** auf das gewünschte Steuerelement, und ziehen Sie es in das Formular.</span><span class="sxs-lookup"><span data-stu-id="4bcca-119">In the **Toolbox**, click the control you want and drag it to your form.</span></span>

    <span data-ttu-id="4bcca-120">Das-Steuerelement wird dem Formular an der angegebenen Position in seiner Standardgröße hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4bcca-120">The control is added to the form at the specified location in its default size.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4bcca-121">Sie können auf ein Steuerelement in der **Toolbox** doppelklicken, um es der oberen linken Ecke des Formulars in seiner Standardgröße hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4bcca-121">You can double-click a control in the **Toolbox** to add it to the upper-left corner of the form in its default size.</span></span>

    <span data-ttu-id="4bcca-122">Sie können einem Formular auch zur Laufzeit dynamisch Steuerelemente hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4bcca-122">You can also add controls dynamically to a form at run time.</span></span> <span data-ttu-id="4bcca-123">Im folgenden Codebeispiel <xref:System.Windows.Forms.TextBox> wird dem Formular ein-Steuerelement hinzugefügt, wenn auf ein- <xref:System.Windows.Forms.Button> Steuerelement geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="4bcca-123">In the following code example, a <xref:System.Windows.Forms.TextBox> control will be added to the form when a <xref:System.Windows.Forms.Button> control is clicked.</span></span>

    > [!NOTE]
    > <span data-ttu-id="4bcca-124">Für das folgende Verfahren ist es erforderlich, dass ein Formular mit einem **Schalt** Flächen-Steuerelement vorhanden ist, das `Button1` bereits darauf platziert ist.</span><span class="sxs-lookup"><span data-stu-id="4bcca-124">The following procedure requires the existence of a form with a **Button** control, `Button1`, already placed on it.</span></span>

## <a name="to-add-a-control-to-a-form-programmatically"></a><span data-ttu-id="4bcca-125">So fügen Sie einem Formular ein Steuerelement Programm gesteuert hinzu</span><span class="sxs-lookup"><span data-stu-id="4bcca-125">To add a control to a form programmatically</span></span>

1. <span data-ttu-id="4bcca-126">Fügen Sie in der-Methode, die das-Ereignis der Schaltfläche `Click` in der-Klasse des Formulars behandelt, Code ähnlich dem folgenden hinzu, um einen Verweis auf die Steuerelement Variable hinzuzufügen, die des Steuer Elements festzulegen `Location` und das Steuerelement hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="4bcca-126">In the method that handles the button's `Click` event within your form's class, insert code similar to the following to add a reference to your control variable, set the control's `Location`, and add the control.</span></span>

    ```vb
    Private Sub Button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles Button1.Click
       Dim MyText As New TextBox()
       MyText.Location = New Point(25, 25)
       Me.Controls.Add(MyText)
    End Sub
    ```

    ```csharp
    private void button1_Click(object sender, System.EventArgs e)
    {
       TextBox myText = new TextBox();
       myText.Location = new Point(25,25);
       this.Controls.Add (myText);
    }
    ```

    ```cpp
    private:
      System::Void button1_Click(System::Object ^  sender,
        System::EventArgs ^  e)
      {
        TextBox ^ myText = gcnew TextBox();
        myText->Location = Point(25,25);
        this->Controls->Add(myText);
      }
    ```

    > [!NOTE]
    > <span data-ttu-id="4bcca-127">Sie können auch Code hinzufügen, um andere Eigenschaften des Steuer Elements zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="4bcca-127">You can also add code to initialize other properties of the control.</span></span>
    > [!IMPORTANT]
    > <span data-ttu-id="4bcca-128">Sie können den lokalen Computer mit einem Sicherheitsrisiko über das Netzwerk verfügbar machen, indem Sie auf eine böswillige verweisen `UserControl` .</span><span class="sxs-lookup"><span data-stu-id="4bcca-128">You might expose your local computer to a security risk through the network by referencing a malicious `UserControl`.</span></span> <span data-ttu-id="4bcca-129">Dies wäre nur ein Problem, wenn eine böswillige Person ein schädliches benutzerdefiniertes Steuerelement erstellt, gefolgt von dem, das Sie versehentlich dem Projekt hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="4bcca-129">This would only be a concern in the case of a malicious person creating a damaging custom control, followed by you mistakenly adding it to your project.</span></span>

## <a name="see-also"></a><span data-ttu-id="4bcca-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bcca-130">See also</span></span>

- [<span data-ttu-id="4bcca-131">Windows Forms Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="4bcca-131">Windows Forms Controls</span></span>](index.md)
- [<span data-ttu-id="4bcca-132">Gewusst wie: Ändern der Größe von Steuerelementen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4bcca-132">How to: Resize Controls on Windows Forms</span></span>](how-to-resize-controls-on-windows-forms.md)
- [<span data-ttu-id="4bcca-133">Gewusst wie: Festlegen des durch ein Windows Forms-Steuerelement angezeigten Textes</span><span class="sxs-lookup"><span data-stu-id="4bcca-133">How to: Set the Text Displayed by a Windows Forms Control</span></span>](how-to-set-the-text-displayed-by-a-windows-forms-control.md)
- [<span data-ttu-id="4bcca-134">Steuerelemente für Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4bcca-134">Controls to Use on Windows Forms</span></span>](controls-to-use-on-windows-forms.md)
