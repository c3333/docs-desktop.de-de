---
title: Wählen Sie WPF-Steuerelemente für Windows Forms
titleSuffix: ''
ms.date: 03/30/2017
helpviewer_keywords:
- WPF content [Windows Forms], assigning at design time
- ElementHost control [Windows Forms], assigning WPF content at design time
- interoperability [WPF]
- Windows Forms, content assignments
- WPF user control [Windows Forms], hosting in Windows Forms
ms.assetid: b3e9ef93-7e0f-4a2f-8f1e-3437609a1eb7
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: c1532206b467c523ffd8e4cf4f85c168a4aad80b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975824"
---
# <a name="walkthrough-assign-wpf-content-on-windows-forms-at-design-time"></a><span data-ttu-id="f7c37-102">Exemplarische Vorgehensweise: Zuweisen von WPF-Inhalt zu Windows Forms zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="f7c37-102">Walkthrough: Assign WPF content on Windows Forms at design time</span></span>

<span data-ttu-id="f7c37-103">In diesem Artikel wird gezeigt, wie Sie die Windows Presentation Foundation (WPF)-Steuerelement Typen auswählen, die auf dem Formular angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f7c37-103">This article show you how to select the Windows Presentation Foundation (WPF) control types you want to display on your form.</span></span> <span data-ttu-id="f7c37-104">Sie können beliebige WPF-Steuerelement Typen auswählen, die in Ihrem Projekt enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="f7c37-104">You can select any WPF control types that are included in your project.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f7c37-105">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="f7c37-105">Prerequisites</span></span>

<span data-ttu-id="f7c37-106">Für diese exemplarische Vorgehensweise benötigen Sie Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="f7c37-106">You need Visual Studio to complete this walkthrough.</span></span>

## <a name="create-the-project"></a><span data-ttu-id="f7c37-107">Erstellen des Projekts</span><span class="sxs-lookup"><span data-stu-id="f7c37-107">Create the project</span></span>

<span data-ttu-id="f7c37-108">Öffnen Sie Visual Studio, und erstellen Sie ein neues Windows Forms-Anwendungsprojekt in Visual Basic oder Visual c# mit dem Namen `SelectingWpfContent` .</span><span class="sxs-lookup"><span data-stu-id="f7c37-108">Open Visual Studio and create a new Windows Forms Application project in Visual Basic or Visual C# named `SelectingWpfContent`.</span></span>

> [!NOTE]
> <span data-ttu-id="f7c37-109">Beim Hosten von WPF-Inhalt werden nur C#- und Visual Basic-Projekte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f7c37-109">When hosting WPF content, only C# and Visual Basic projects are supported.</span></span>

## <a name="create-the-wpf-control-types"></a><span data-ttu-id="f7c37-110">Erstellen der WPF-Steuerelement Typen</span><span class="sxs-lookup"><span data-stu-id="f7c37-110">Create the WPF control types</span></span>

<span data-ttu-id="f7c37-111">Nachdem Sie dem Projekt WPF-Steuerelementtypen hinzugefügt haben, können Sie diese in verschiedenen <xref:System.Windows.Forms.Integration.ElementHost>-Steuerelementen hosten.</span><span class="sxs-lookup"><span data-stu-id="f7c37-111">After you add WPF control types to the project, you can host them in different <xref:System.Windows.Forms.Integration.ElementHost> controls.</span></span>

1. <span data-ttu-id="f7c37-112">Fügen Sie der Projektmappe ein neues WPF-<xref:System.Windows.Controls.UserControl>-Projekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="f7c37-112">Add a new WPF <xref:System.Windows.Controls.UserControl> project to the solution.</span></span> <span data-ttu-id="f7c37-113">Verwenden Sie den Standardnamen, `UserControl1.xaml`, für den Steuerelementtyp.</span><span class="sxs-lookup"><span data-stu-id="f7c37-113">Use the default name for the control type, `UserControl1.xaml`.</span></span> <span data-ttu-id="f7c37-114">Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Erstellen eines neuen WPF-Inhalts auf Windows Forms zur Entwurfszeit](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span><span class="sxs-lookup"><span data-stu-id="f7c37-114">For more information, see [Walkthrough: Creating New WPF Content on Windows Forms at Design Time](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span></span>

2. <span data-ttu-id="f7c37-115">Stellen Sie in der Entwurfsansicht sicher, dass `UserControl1` ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="f7c37-115">In Design view, make sure that `UserControl1` is selected.</span></span>

3. <span data-ttu-id="f7c37-116">Legen Sie im Fenster **Eigenschaften** den Wert der-Eigenschaft <xref:System.Windows.FrameworkElement.Width%2A> und der-Eigenschaft <xref:System.Windows.FrameworkElement.Height%2A> auf **200** fest.</span><span class="sxs-lookup"><span data-stu-id="f7c37-116">In the **Properties** window, set the value of the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> properties to **200**.</span></span>

4. <span data-ttu-id="f7c37-117">Fügen Sie ein <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> -Steuerelement hinzu, <xref:System.Windows.Controls.UserControl> und legen Sie den Wert der- <xref:System.Windows.Controls.TextBox.Text%2A> Eigenschaft auf **gehosteten Inhalt** fest.</span><span class="sxs-lookup"><span data-stu-id="f7c37-117">Add a <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> control to the <xref:System.Windows.Controls.UserControl> and set the value of the <xref:System.Windows.Controls.TextBox.Text%2A> property to **Hosted Content**.</span></span>

5. <span data-ttu-id="f7c37-118">Fügen Sie dem Projekt ein zweites WPF-<xref:System.Windows.Controls.UserControl> hinzu.</span><span class="sxs-lookup"><span data-stu-id="f7c37-118">Add a second WPF <xref:System.Windows.Controls.UserControl> to the project.</span></span> <span data-ttu-id="f7c37-119">Verwenden Sie den Standardnamen, `UserControl2.xaml`, für den Steuerelementtyp.</span><span class="sxs-lookup"><span data-stu-id="f7c37-119">Use the default name for the control type, `UserControl2.xaml`.</span></span>

6. <span data-ttu-id="f7c37-120">Legen Sie im Fenster **Eigenschaften** den Wert der-Eigenschaft <xref:System.Windows.FrameworkElement.Width%2A> und der-Eigenschaft <xref:System.Windows.FrameworkElement.Height%2A> auf **200** fest.</span><span class="sxs-lookup"><span data-stu-id="f7c37-120">In the **Properties** window, set the value of the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> properties to **200**.</span></span>

7. <span data-ttu-id="f7c37-121">Fügen Sie ein <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> -Steuerelement hinzu, <xref:System.Windows.Controls.UserControl> und legen Sie den Wert der- <xref:System.Windows.Controls.TextBox.Text%2A> Eigenschaft auf **Hosted Content 2** fest.</span><span class="sxs-lookup"><span data-stu-id="f7c37-121">Add a <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> control to the <xref:System.Windows.Controls.UserControl> and set the value of the <xref:System.Windows.Controls.TextBox.Text%2A> property to **Hosted Content 2**.</span></span>

   > [!NOTE]
   > <span data-ttu-id="f7c37-122">Normalerweise sollten Sie anspruchsvolleren WPF-Inhalt hosten.</span><span class="sxs-lookup"><span data-stu-id="f7c37-122">In general, you should host more sophisticated WPF content.</span></span> <span data-ttu-id="f7c37-123"><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType>-Steuerelement wird hier nur zur Veranschaulichung verwendet. </span><span class="sxs-lookup"><span data-stu-id="f7c37-123">The <xref:System.Windows.Controls.TextBox?displayProperty=nameWithType> control is used here for illustrative purposes only.</span></span>

8. <span data-ttu-id="f7c37-124">Erstellen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="f7c37-124">Build the project.</span></span>

## <a name="select-wpf-controls"></a><span data-ttu-id="f7c37-125">WPF-Steuerelemente auswählen</span><span class="sxs-lookup"><span data-stu-id="f7c37-125">Select WPF controls</span></span>

<span data-ttu-id="f7c37-126">Sie können einem <xref:System.Windows.Forms.Integration.ElementHost>-Steuerelement, das bereits Inhalte hostet, verschiedene WPF-Inhalte zuweisen.</span><span class="sxs-lookup"><span data-stu-id="f7c37-126">You can assign different WPF content to an <xref:System.Windows.Forms.Integration.ElementHost> control, which is already hosting content.</span></span>

1. <span data-ttu-id="f7c37-127">Öffnen Sie `Form1` im Windows Forms-Designer.</span><span class="sxs-lookup"><span data-stu-id="f7c37-127">Open `Form1` in the Windows Forms Designer.</span></span>

2. <span data-ttu-id="f7c37-128">Doppelklicken Sie in der **Toolbox** auf, `UserControl1` um eine Instanz von `UserControl1` auf dem Formular zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7c37-128">In the **Toolbox**, double-click `UserControl1` to create an instance of `UserControl1` on the form.</span></span>

   <span data-ttu-id="f7c37-129">Eine Instanz von `UserControl1` wird in einem neuen <xref:System.Windows.Forms.Integration.ElementHost>-Steuerelement namens `elementHost1` gehostet.</span><span class="sxs-lookup"><span data-stu-id="f7c37-129">An instance of `UserControl1` is hosted in a new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost1`.</span></span>

3. <span data-ttu-id="f7c37-130">Öffnen Sie im smarttagpanel für `elementHost1` die Dropdown Liste **gehostete Inhalte auswählen** .</span><span class="sxs-lookup"><span data-stu-id="f7c37-130">In the smart tag panel for `elementHost1`, open the **Select Hosted Content** drop-down list.</span></span>

4. <span data-ttu-id="f7c37-131">Wählen Sie **UserControl2** aus dem Dropdown-Listenfeld aus.</span><span class="sxs-lookup"><span data-stu-id="f7c37-131">Select **UserControl2** from the drop-down list box.</span></span>

   <span data-ttu-id="f7c37-132">Das `elementHost1`-Steuerelement hostet jetzt eine Instanz des `UserControl2`-Typs.</span><span class="sxs-lookup"><span data-stu-id="f7c37-132">The `elementHost1` control now hosts an instance of the `UserControl2` type.</span></span>

5. <span data-ttu-id="f7c37-133">Vergewissern Sie sich im Fenster **Eigenschaften** , dass die- <xref:System.Windows.Forms.Integration.ElementHost.Child%2A> Eigenschaft auf **UserControl2** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f7c37-133">In the **Properties** window, confirm that the <xref:System.Windows.Forms.Integration.ElementHost.Child%2A> property is set to **UserControl2**.</span></span>

6. <span data-ttu-id="f7c37-134">Ziehen Sie ein-Steuerelement aus der **Toolbox** in der **WPF-Interoperabilitäts** Gruppe <xref:System.Windows.Forms.Integration.ElementHost> auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="f7c37-134">From the **Toolbox**, in the **WPF Interoperability** group, drag an <xref:System.Windows.Forms.Integration.ElementHost> control onto the form.</span></span>

   <span data-ttu-id="f7c37-135">Der Standardname für das neue Steuerelement ist `elementHost2`.</span><span class="sxs-lookup"><span data-stu-id="f7c37-135">The default name for the new control is `elementHost2`.</span></span>

7. <span data-ttu-id="f7c37-136">Öffnen Sie im smarttagpanel für `elementHost2` die Dropdown Liste **gehostete Inhalte auswählen** .</span><span class="sxs-lookup"><span data-stu-id="f7c37-136">In the smart tag panel for `elementHost2`, open the **Select Hosted Content** drop-down list.</span></span>

8. <span data-ttu-id="f7c37-137">Wählen Sie in der Dropdown Liste **UserControl1** aus.</span><span class="sxs-lookup"><span data-stu-id="f7c37-137">Select **UserControl1** from the drop-down list.</span></span>

9. <span data-ttu-id="f7c37-138">Das `elementHost2`-Steuerelement hostet jetzt eine Instanz des `UserControl1`-Typs.</span><span class="sxs-lookup"><span data-stu-id="f7c37-138">The `elementHost2` control now hosts an instance of the `UserControl1` type.</span></span>

## <a name="see-also"></a><span data-ttu-id="f7c37-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7c37-139">See also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="f7c37-140">Migration und Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="f7c37-140">Migration and Interoperability</span></span>](/dotnet/framework/wpf/advanced/migration-and-interoperability)
- [<span data-ttu-id="f7c37-141">Verwenden von WPF-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="f7c37-141">Using WPF Controls</span></span>](using-wpf-controls.md)
- [<span data-ttu-id="f7c37-142">Entwerfen von XAML-Code in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f7c37-142">Design XAML in Visual Studio</span></span>](/visualstudio/xaml-tools/designing-xaml-in-visual-studio)
