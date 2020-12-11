---
title: Anordnen von WPF-Inhalt auf Windows Forms zur Entwurfszeit
titleSuffix: ''
ms.date: 03/30/2017
helpviewer_keywords:
- WPF user control [Windows Forms], hosting in a layout panel
- WPF content [Windows Forms], arranging at design time
- Windows Forms, arranging WPF content at design time
- WPF content [Windows Forms], hosting in Windows Forms
- Windows Forms, anchoring and docking WPF content
- interoperability [WPF]
ms.assetid: 5efb1c53-1484-43d6-aa8a-f4861b99bb8a
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: b3acf39bdf6628737c328dc6e451c3ffac4896ee
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976043"
---
# <a name="walkthrough-arrange-wpf-content-on-windows-forms-at-design-time"></a><span data-ttu-id="798b7-102">Exemplarische Vorgehensweise: Anordnen von WPF-Inhalt auf Windows Forms zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="798b7-102">Walkthrough: Arrange WPF content on Windows Forms at design time</span></span>

<span data-ttu-id="798b7-103">In diesem Artikel erfahren Sie, wie Sie die Windows Forms Layoutfeatures, wie z. b. das verankern und ausrichten, verwenden, um Windows Presentation Foundation (WPF)-Steuerelemente anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="798b7-103">This article shows you how to use the Windows Forms layout features, such as anchoring and snaplines, to arrange Windows Presentation Foundation (WPF) controls.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="798b7-104">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="798b7-104">Prerequisites</span></span>

<span data-ttu-id="798b7-105">Für diese exemplarische Vorgehensweise benötigen Sie Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="798b7-105">You need Visual Studio to complete this walkthrough.</span></span>

## <a name="create-the-project"></a><span data-ttu-id="798b7-106">Erstellen des Projekts</span><span class="sxs-lookup"><span data-stu-id="798b7-106">Create the project</span></span>

<span data-ttu-id="798b7-107">Öffnen Sie Visual Studio, und erstellen Sie ein neues Windows Forms-Anwendungsprojekt in Visual Basic oder Visual c# mit dem Namen `ArrangeElementHost` .</span><span class="sxs-lookup"><span data-stu-id="798b7-107">Open Visual Studio and create a new Windows Forms Application project in Visual Basic or Visual C# named `ArrangeElementHost`.</span></span>

> [!NOTE]
> <span data-ttu-id="798b7-108">Beim Hosten von WPF-Inhalt werden nur C#- und Visual Basic-Projekte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="798b7-108">When hosting WPF content, only C# and Visual Basic projects are supported.</span></span>

## <a name="create-the-wpf-control"></a><span data-ttu-id="798b7-109">Erstellen des WPF-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="798b7-109">Create the WPF control</span></span>

<span data-ttu-id="798b7-110">Nachdem Sie dem Projekt ein WPF-Steuerelement hinzugefügt haben, können Sie dieses auf dem Formular anordnen.</span><span class="sxs-lookup"><span data-stu-id="798b7-110">After you add a WPF control to the project, you can arrange it on the form.</span></span>

1. <span data-ttu-id="798b7-111">Fügen Sie dem Projekt ein neues WPF-<xref:System.Windows.Controls.UserControl>-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="798b7-111">Add a new WPF <xref:System.Windows.Controls.UserControl> to the project.</span></span> <span data-ttu-id="798b7-112">Verwenden Sie den Standardnamen, `UserControl1.xaml`, für den Steuerelementtyp.</span><span class="sxs-lookup"><span data-stu-id="798b7-112">Use the default name for the control type, `UserControl1.xaml`.</span></span> <span data-ttu-id="798b7-113">Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Erstellen eines neuen WPF-Inhalts auf Windows Forms zur Entwurfszeit](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span><span class="sxs-lookup"><span data-stu-id="798b7-113">For more information, see [Walkthrough: Creating New WPF Content on Windows Forms at Design Time](walkthrough-creating-new-wpf-content-on-windows-forms-at-design-time.md).</span></span>

2. <span data-ttu-id="798b7-114">Stellen Sie in der Entwurfsansicht sicher, dass `UserControl1` ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="798b7-114">In Design view, make sure that `UserControl1` is selected.</span></span>

3. <span data-ttu-id="798b7-115">Legen Sie im Fenster **Eigenschaften** den Wert der-Eigenschaft <xref:System.Windows.FrameworkElement.Width%2A> und der-Eigenschaft <xref:System.Windows.FrameworkElement.Height%2A> auf **200** fest.</span><span class="sxs-lookup"><span data-stu-id="798b7-115">In the **Properties** window, set the value of the <xref:System.Windows.FrameworkElement.Width%2A> and <xref:System.Windows.FrameworkElement.Height%2A> properties to **200**.</span></span>

4. <span data-ttu-id="798b7-116">Legen Sie den Wert der- <xref:System.Windows.Controls.Control.Background%2A> Eigenschaft auf **Blue** fest.</span><span class="sxs-lookup"><span data-stu-id="798b7-116">Set the value of the <xref:System.Windows.Controls.Control.Background%2A> property to **Blue**.</span></span>

5. <span data-ttu-id="798b7-117">Erstellen Sie das Projekt.</span><span class="sxs-lookup"><span data-stu-id="798b7-117">Build the project.</span></span>

## <a name="host-wpf-controls-in-a-layout-panel"></a><span data-ttu-id="798b7-118">WPF-Steuerelemente in einem Layoutpanel hosten</span><span class="sxs-lookup"><span data-stu-id="798b7-118">Host WPF controls in a layout panel</span></span>

<span data-ttu-id="798b7-119">Sie können WPF-Steuerelemente in Layoutbereichen auf die gleiche Weise verwenden wie andere Windows Forms-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="798b7-119">You can use WPF controls in layout panels in the same way you use other Windows Forms controls.</span></span>

1. <span data-ttu-id="798b7-120">Öffnen Sie `Form1` im Windows Forms-Designer.</span><span class="sxs-lookup"><span data-stu-id="798b7-120">Open `Form1` in the Windows Forms Designer.</span></span>

2. <span data-ttu-id="798b7-121">Ziehen Sie ein-Steuerelement in der **Toolbox** <xref:System.Windows.Forms.TableLayoutPanel> auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="798b7-121">In the **Toolbox**, drag a <xref:System.Windows.Forms.TableLayoutPanel> control onto the form.</span></span>

3. <span data-ttu-id="798b7-122"><xref:System.Windows.Forms.TableLayoutPanel>Wählen Sie im Smarttagbereich des-Steuer Elements **letzte Zeile entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="798b7-122">On the <xref:System.Windows.Forms.TableLayoutPanel> control's smart tag panel, select **Remove Last Row**.</span></span>

4. <span data-ttu-id="798b7-123">Ändern Sie die Größe des <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelements, sodass es breiter und höher wird.</span><span class="sxs-lookup"><span data-stu-id="798b7-123">Resize the <xref:System.Windows.Forms.TableLayoutPanel> control to a larger width and height.</span></span>

5. <span data-ttu-id="798b7-124">Doppelklicken Sie in der **Toolbox** `UserControl1` auf, um `UserControl1` in der ersten Zelle des-Steuer Elements eine Instanz von zu erstellen <xref:System.Windows.Forms.TableLayoutPanel> .</span><span class="sxs-lookup"><span data-stu-id="798b7-124">In the **Toolbox**, double-click `UserControl1` to create an instance of `UserControl1` in the first cell of the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

   <span data-ttu-id="798b7-125">Die Instanz von `UserControl1` wird in einem neuen <xref:System.Windows.Forms.Integration.ElementHost>-Steuerelement namens `elementHost1` gehostet.</span><span class="sxs-lookup"><span data-stu-id="798b7-125">The instance of `UserControl1` is hosted in a new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost1`.</span></span>

6. <span data-ttu-id="798b7-126">Doppelklicken Sie in der **Toolbox** `UserControl1` auf, um eine weitere Instanz in der zweiten Zelle des-Steuer Elements zu erstellen <xref:System.Windows.Forms.TableLayoutPanel> .</span><span class="sxs-lookup"><span data-stu-id="798b7-126">In the **Toolbox**, double-click `UserControl1` to create another instance in the second cell of the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

7. <span data-ttu-id="798b7-127">Wählen Sie im Fenster " **Dokument** Gliederung" aus `tableLayoutPanel1` .</span><span class="sxs-lookup"><span data-stu-id="798b7-127">In the **Document Outline** window, select `tableLayoutPanel1`.</span></span>

8. <span data-ttu-id="798b7-128">Legen Sie im Fenster **Eigenschaften** den Wert der- <xref:System.Windows.Forms.Control.Padding%2A> Eigenschaft auf **10, 10, 10, 10** fest.</span><span class="sxs-lookup"><span data-stu-id="798b7-128">In the **Properties** window, set the value of the <xref:System.Windows.Forms.Control.Padding%2A> property to **10, 10, 10, 10**.</span></span>

   <span data-ttu-id="798b7-129">Die Größe beider <xref:System.Windows.Forms.Integration.ElementHost>-Steuerelemente wird entsprechend dem neuen Layout angepasst.</span><span class="sxs-lookup"><span data-stu-id="798b7-129">Both <xref:System.Windows.Forms.Integration.ElementHost> controls are resized to fit into the new layout.</span></span>

## <a name="use-snaplines-to-align-wpf-controls"></a><span data-ttu-id="798b7-130">Verwenden von Ausrichtungs Linien zum Ausrichten von WPF-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="798b7-130">Use snaplines to align WPF controls</span></span>

<span data-ttu-id="798b7-131">Ausrichtungslinien erleichtern die Ausrichtung von Steuerelementen auf einem Formular.</span><span class="sxs-lookup"><span data-stu-id="798b7-131">Snaplines enable easy alignment of controls on a form.</span></span> <span data-ttu-id="798b7-132">Sie können Ausrichtungslinien auch verwenden, um WPF-Steuerelemente auszurichten.</span><span class="sxs-lookup"><span data-stu-id="798b7-132">You can use snaplines to align your WPF controls as well.</span></span> <span data-ttu-id="798b7-133">Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Anordnen von Steuerelementen auf Windows Forms mithilfe](../controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)von Ausrichtungs Linien.</span><span class="sxs-lookup"><span data-stu-id="798b7-133">For more information, see [Walkthrough: Arranging Controls on Windows Forms Using Snaplines](../controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md).</span></span>

1. <span data-ttu-id="798b7-134">Ziehen Sie aus der **Toolbox** eine Instanz von `UserControl1` auf das Formular, und platzieren Sie Sie in dem Bereich unterhalb des <xref:System.Windows.Forms.TableLayoutPanel> Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="798b7-134">From the **Toolbox**, drag an instance of `UserControl1` onto the form, and place it in the space beneath the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

   <span data-ttu-id="798b7-135">Die Instanz von `UserControl1` wird in einem neuen <xref:System.Windows.Forms.Integration.ElementHost>-Steuerelement namens `elementHost3` gehostet.</span><span class="sxs-lookup"><span data-stu-id="798b7-135">The instance of `UserControl1` is hosted in a new <xref:System.Windows.Forms.Integration.ElementHost> control named `elementHost3`.</span></span>

2. <span data-ttu-id="798b7-136">Richten Sie den linken Rand von `elementHost3` mithilfe der Ausrichtungslinien am linken Rand des <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelements aus.</span><span class="sxs-lookup"><span data-stu-id="798b7-136">Using snaplines, align the left edge of `elementHost3` with the left edge of <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

3. <span data-ttu-id="798b7-137">Legen Sie die Breite von `elementHost3` mithilfe der Ausrichtungslinien auf dieselbe Breite wie das <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement fest.</span><span class="sxs-lookup"><span data-stu-id="798b7-137">Using snaplines, size `elementHost3` to the same width as the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

4. <span data-ttu-id="798b7-138">Verschieben Sie `elementHost3` in Richtung des <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelements,  steuern, bis zwischen den Steuerelementen eine mittige Ausrichtungslinie angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="798b7-138">Move `elementHost3` toward the <xref:System.Windows.Forms.TableLayoutPanel> control until a center snapline appears between the controls.</span></span>

5. <span data-ttu-id="798b7-139">Legen Sie im Fenster **Eigenschaften** den Wert der Margin-Eigenschaft auf **20, 20, 20, 20** fest.</span><span class="sxs-lookup"><span data-stu-id="798b7-139">In the **Properties** window, set the value of the Margin property to **20, 20, 20, 20**.</span></span>

6. <span data-ttu-id="798b7-140">Verschieben Sie `elementHost3` vom <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement weg, bis die mittige Ausrichtungslinie erneut angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="798b7-140">Move the `elementHost3` away from the <xref:System.Windows.Forms.TableLayoutPanel> control until the center snapline appears again.</span></span> <span data-ttu-id="798b7-141">Die mittige Ausrichtungslinie kennzeichnet jetzt einen Rand von 20.</span><span class="sxs-lookup"><span data-stu-id="798b7-141">The center snapline now indicates a margin of 20.</span></span>

7. <span data-ttu-id="798b7-142">`elementHost3`Nach rechts verschieben, bis der linke Rand am linken Rand von ausgerichtet ist `elementHost1` .</span><span class="sxs-lookup"><span data-stu-id="798b7-142">Move `elementHost3` to the right until its left edge aligns with the left edge of `elementHost1`.</span></span>

8. <span data-ttu-id="798b7-143">Ändern Sie die Breite von `elementHost3` bis dessen rechter Rand am rechten Rand von `elementHost2` ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="798b7-143">Change the width of `elementHost3` until its right edge aligns with the right edge of `elementHost2`.</span></span>

## <a name="anchor-and-dock-wpf-controls"></a><span data-ttu-id="798b7-144">WPF-Steuerelemente verankern und Andocken</span><span class="sxs-lookup"><span data-stu-id="798b7-144">Anchor and dock WPF controls</span></span>

<span data-ttu-id="798b7-145">Ein auf einem Formular gehostetes WPF-Steuerelement hat dasselbe Verankerungs- und Andockverhalten auf wie andere Windows Forms-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="798b7-145">A WPF control hosted on a form has the same anchoring and docking behavior as other Windows Forms controls.</span></span>

1. <span data-ttu-id="798b7-146">Wählen Sie `elementHost1`aus.</span><span class="sxs-lookup"><span data-stu-id="798b7-146">Select `elementHost1`.</span></span>

2. <span data-ttu-id="798b7-147">Legen Sie im Fenster **Eigenschaften** die- <xref:System.Windows.Forms.Control.Anchor%2A> Eigenschaft auf **oben, unten, Links und rechts** fest.</span><span class="sxs-lookup"><span data-stu-id="798b7-147">In the **Properties** window, set the <xref:System.Windows.Forms.Control.Anchor%2A> property to **Top, Bottom, Left, Right**.</span></span>

3. <span data-ttu-id="798b7-148">Vergrößern Sie das <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="798b7-148">Resize the <xref:System.Windows.Forms.TableLayoutPanel> control to a larger size.</span></span>

   <span data-ttu-id="798b7-149">Die Größe des `elementHost1`-Steuerelements wird geändert, sodass es die Zelle ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="798b7-149">The `elementHost1` control resizes to fill the cell.</span></span>

4. <span data-ttu-id="798b7-150">Wählen Sie `elementHost2`aus.</span><span class="sxs-lookup"><span data-stu-id="798b7-150">Select `elementHost2`.</span></span>

5. <span data-ttu-id="798b7-151">Legen Sie im Fenster **Eigenschaften** den Wert der- <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft auf fest <xref:System.Windows.Forms.DockStyle.Fill> .</span><span class="sxs-lookup"><span data-stu-id="798b7-151">In the **Properties** window, set the value of the <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Fill>.</span></span>

   <span data-ttu-id="798b7-152">Die Größe des `elementHost2`-Steuerelements wird geändert, sodass es die Zelle ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="798b7-152">The `elementHost2` control resizes to fill the cell.</span></span>

6. <span data-ttu-id="798b7-153">Wählen Sie das <xref:System.Windows.Forms.TableLayoutPanel>-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="798b7-153">Select the <xref:System.Windows.Forms.TableLayoutPanel> control.</span></span>

7. <span data-ttu-id="798b7-154">Legen Sie den Wert von dessen <xref:System.Windows.Forms.Control.Dock%2A>-Eigenschaft auf <xref:System.Windows.Forms.DockStyle.Top> fest.</span><span class="sxs-lookup"><span data-stu-id="798b7-154">Set the value of its <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Top>.</span></span>

8. <span data-ttu-id="798b7-155">Wählen Sie `elementHost3`aus.</span><span class="sxs-lookup"><span data-stu-id="798b7-155">Select `elementHost3`.</span></span>

9. <span data-ttu-id="798b7-156">Legen Sie den Wert von dessen <xref:System.Windows.Forms.Control.Dock%2A>-Eigenschaft auf <xref:System.Windows.Forms.DockStyle.Fill> fest.</span><span class="sxs-lookup"><span data-stu-id="798b7-156">Set the value of its <xref:System.Windows.Forms.Control.Dock%2A> property to <xref:System.Windows.Forms.DockStyle.Fill>.</span></span>

   <span data-ttu-id="798b7-157">Die Größe des `elementHost3`-Steuerelements wird so geändert, dass es den verbleibenden Platz auf dem Formular ausfüllt.</span><span class="sxs-lookup"><span data-stu-id="798b7-157">The `elementHost3` control resizes to fill the remaining space on the form.</span></span>

10. <span data-ttu-id="798b7-158">Ändern Sie die Größe des Formulars.</span><span class="sxs-lookup"><span data-stu-id="798b7-158">Resize the form.</span></span>

    <span data-ttu-id="798b7-159">Die Größen aller drei <xref:System.Windows.Forms.Integration.ElementHost>-Steuerelemente werden entsprechend angepasst.</span><span class="sxs-lookup"><span data-stu-id="798b7-159">All three <xref:System.Windows.Forms.Integration.ElementHost> controls resize appropriately.</span></span>

    <span data-ttu-id="798b7-160">Weitere Informationen finden Sie unter Gewusst [wie: verankern und Andocken von untergeordneten Steuerelementen in einem TableLayoutPanel-Steuer](../controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="798b7-160">For more information, see [How to: Anchor and Dock Child Controls in a TableLayoutPanel Control](../controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="798b7-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="798b7-161">See also</span></span>

- <xref:System.Windows.Forms.Integration.ElementHost>
- <xref:System.Windows.Forms.Integration.WindowsFormsHost>
- [<span data-ttu-id="798b7-162">Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem TableLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="798b7-162">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](../controls/how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [<span data-ttu-id="798b7-163">Gewusst wie: Ausrichten eines Steuerelements an den Rändern eines Formulars zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="798b7-163">How to: Align a Control to the Edges of Forms at Design Time</span></span>](../controls/how-to-align-a-control-to-the-edges-of-forms-at-design-time.md)
- [<span data-ttu-id="798b7-164">Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von Ausrichtungslinien</span><span class="sxs-lookup"><span data-stu-id="798b7-164">Walkthrough: Arranging Controls on Windows Forms Using Snaplines</span></span>](../controls/walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
- [<span data-ttu-id="798b7-165">Migration und Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="798b7-165">Migration and Interoperability</span></span>](/dotnet/framework/wpf/advanced/migration-and-interoperability)
- [<span data-ttu-id="798b7-166">Verwenden von WPF-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="798b7-166">Using WPF Controls</span></span>](using-wpf-controls.md)
- [<span data-ttu-id="798b7-167">Entwerfen von XAML-Code in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="798b7-167">Design XAML in Visual Studio</span></span>](/visualstudio/xaml-tools/designing-xaml-in-visual-studio)
