---
title: ToggleButton-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- states [WPF], ToggleButton
- ToggleButton [WPF], styles and templates
- ControlTemplate [WPF], ToggleButton
- styles [WPF], ToggleButton
- templates [WPF], ToggleButton
- parts [WPF], ToggleButton
ms.assetid: 54f23f30-4bcb-4f09-8ce4-376a13a255a1
ms.openlocfilehash: 2c5aee58878ea6199c07ee201882fd3ded97bdee
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976980"
---
# <a name="togglebutton-styles-and-templates"></a><span data-ttu-id="87288-102">ToggleButton-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="87288-102">ToggleButton Styles and Templates</span></span>

<span data-ttu-id="87288-103">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.Primitives.ToggleButton> .</span><span class="sxs-lookup"><span data-stu-id="87288-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Primitives.ToggleButton> control.</span></span> <span data-ttu-id="87288-104">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="87288-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="87288-105">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="87288-105">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>

## <a name="togglebutton-parts"></a><span data-ttu-id="87288-106">Teile</span><span class="sxs-lookup"><span data-stu-id="87288-106">ToggleButton Parts</span></span>

<span data-ttu-id="87288-107">Das- <xref:System.Windows.Controls.Primitives.ToggleButton> Steuerelement verfügt über keine benannten Teile.</span><span class="sxs-lookup"><span data-stu-id="87288-107">The <xref:System.Windows.Controls.Primitives.ToggleButton> control does not have any named parts.</span></span>

## <a name="togglebutton-states"></a><span data-ttu-id="87288-108">Objektstatus</span><span class="sxs-lookup"><span data-stu-id="87288-108">ToggleButton States</span></span>

<span data-ttu-id="87288-109">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.Primitives.ToggleButton> .</span><span class="sxs-lookup"><span data-stu-id="87288-109">The following table lists the visual states for the <xref:System.Windows.Controls.Primitives.ToggleButton> control.</span></span>

|<span data-ttu-id="87288-110">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="87288-110">VisualState Name</span></span>|<span data-ttu-id="87288-111">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="87288-111">VisualStateGroup Name</span></span>|<span data-ttu-id="87288-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87288-112">Description</span></span>|
|-|-|-|
|<span data-ttu-id="87288-113">Normal</span><span class="sxs-lookup"><span data-stu-id="87288-113">Normal</span></span>|<span data-ttu-id="87288-114">CommonStates</span><span class="sxs-lookup"><span data-stu-id="87288-114">CommonStates</span></span>|<span data-ttu-id="87288-115">Der Standardzustand</span><span class="sxs-lookup"><span data-stu-id="87288-115">The default state.</span></span>|
|<span data-ttu-id="87288-116">MouseOver</span><span class="sxs-lookup"><span data-stu-id="87288-116">MouseOver</span></span>|<span data-ttu-id="87288-117">CommonStates</span><span class="sxs-lookup"><span data-stu-id="87288-117">CommonStates</span></span>|<span data-ttu-id="87288-118">Der Mauszeiger ist über dem Steuerelement positioniert.</span><span class="sxs-lookup"><span data-stu-id="87288-118">The mouse pointer is positioned over the control.</span></span>|
|<span data-ttu-id="87288-119">Gedrückt</span><span class="sxs-lookup"><span data-stu-id="87288-119">Pressed</span></span>|<span data-ttu-id="87288-120">CommonStates</span><span class="sxs-lookup"><span data-stu-id="87288-120">CommonStates</span></span>|<span data-ttu-id="87288-121">Das Steuerelement wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="87288-121">The control is pressed.</span></span>|
|<span data-ttu-id="87288-122">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="87288-122">Disabled</span></span>|<span data-ttu-id="87288-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="87288-123">CommonStates</span></span>|<span data-ttu-id="87288-124">Das Steuerelement ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="87288-124">The control is disabled.</span></span>|
|<span data-ttu-id="87288-125">Focused</span><span class="sxs-lookup"><span data-stu-id="87288-125">Focused</span></span>|<span data-ttu-id="87288-126">FocusStates</span><span class="sxs-lookup"><span data-stu-id="87288-126">FocusStates</span></span>|<span data-ttu-id="87288-127">Der Fokus liegt auf dem Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="87288-127">The control has focus.</span></span>|
|<span data-ttu-id="87288-128">Ohne Fokus</span><span class="sxs-lookup"><span data-stu-id="87288-128">Unfocused</span></span>|<span data-ttu-id="87288-129">FocusStates</span><span class="sxs-lookup"><span data-stu-id="87288-129">FocusStates</span></span>|<span data-ttu-id="87288-130">Der Fokus liegt nicht auf dem Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="87288-130">The control does not have focus.</span></span>|
|<span data-ttu-id="87288-131">Überprüft</span><span class="sxs-lookup"><span data-stu-id="87288-131">Checked</span></span>|<span data-ttu-id="87288-132">CheckStates</span><span class="sxs-lookup"><span data-stu-id="87288-132">CheckStates</span></span>|<span data-ttu-id="87288-133"><xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> ist `true`.</span><span class="sxs-lookup"><span data-stu-id="87288-133"><xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> is `true`.</span></span>|
|<span data-ttu-id="87288-134">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="87288-134">Unchecked</span></span>|<span data-ttu-id="87288-135">CheckStates</span><span class="sxs-lookup"><span data-stu-id="87288-135">CheckStates</span></span>|<span data-ttu-id="87288-136"><xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> ist `false`.</span><span class="sxs-lookup"><span data-stu-id="87288-136"><xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> is `false`.</span></span>|
|<span data-ttu-id="87288-137">Unbestimmten</span><span class="sxs-lookup"><span data-stu-id="87288-137">Indeterminate</span></span>|<span data-ttu-id="87288-138">CheckStates</span><span class="sxs-lookup"><span data-stu-id="87288-138">CheckStates</span></span>|<span data-ttu-id="87288-139"><xref:System.Windows.Controls.Primitives.ToggleButton.IsThreeState%2A> ist `true`, und <xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> ist `null`.</span><span class="sxs-lookup"><span data-stu-id="87288-139"><xref:System.Windows.Controls.Primitives.ToggleButton.IsThreeState%2A> is `true`, and <xref:System.Windows.Controls.Primitives.ToggleButton.IsChecked%2A> is `null`.</span></span>|
|<span data-ttu-id="87288-140">Gültig</span><span class="sxs-lookup"><span data-stu-id="87288-140">Valid</span></span>|<span data-ttu-id="87288-141">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="87288-141">ValidationStates</span></span>|<span data-ttu-id="87288-142">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="87288-142">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|
|<span data-ttu-id="87288-143">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="87288-143">InvalidFocused</span></span>|<span data-ttu-id="87288-144">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="87288-144">ValidationStates</span></span>|<span data-ttu-id="87288-145">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, `true` und das Steuerelement besitzt den Fokus.</span><span class="sxs-lookup"><span data-stu-id="87288-145">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` and the control has focus.</span></span>|
|<span data-ttu-id="87288-146">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="87288-146">InvalidUnfocused</span></span>|<span data-ttu-id="87288-147">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="87288-147">ValidationStates</span></span>|<span data-ttu-id="87288-148">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, `true` und das Steuerelement besitzt keinen Fokus.</span><span class="sxs-lookup"><span data-stu-id="87288-148">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` and the control does not have focus.</span></span>|

> [!NOTE]
> <span data-ttu-id="87288-149">Wenn der Unbestimmtheit des visuellen Zustands nicht in der Steuerelement Vorlage vorhanden ist, wird der nicht überprüfte visuelle Zustand als visueller Standardzustand verwendet.</span><span class="sxs-lookup"><span data-stu-id="87288-149">If the Indeterminate visual state does not exist in your control template, then the Unchecked visual state will be used as default visual state.</span></span>

## <a name="togglebutton-controltemplate-example"></a><span data-ttu-id="87288-150">Beispiel für eine Beispiel-ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="87288-150">ToggleButton ControlTemplate Example</span></span>

<span data-ttu-id="87288-151">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.Primitives.ToggleButton> .</span><span class="sxs-lookup"><span data-stu-id="87288-151">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Primitives.ToggleButton> control.</span></span>

[!code-xaml[ControlTemplateExamples#ToggleButton](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/combobox.xaml#togglebutton)]

<span data-ttu-id="87288-152">Im vorhergehenden Beispiel wird mindestens eine der folgenden Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="87288-152">The preceding example uses one or more of the following resources.</span></span>

[!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]

<span data-ttu-id="87288-153">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="87288-153">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>

## <a name="see-also"></a><span data-ttu-id="87288-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87288-154">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="87288-155">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="87288-155">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="87288-156">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="87288-156">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="87288-157">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="87288-157">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="87288-158">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="87288-158">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
