---
title: Button-Stile und -Vorlagen
description: Erfahren Sie mehr über Stile und Vorlagen für das Windows Presentation Foundation Button-Steuerelement. Ändern Sie ControlTemplate, um dem Steuerelement eine eindeutige Darstellung zu verschaffen.
ms.date: 03/30/2017
helpviewer_keywords:
- states [WPF], Button
- parts [WPF], Button
- styles [WPF], Button
- Button [WPF], styles and templates
- templates [WPF], Button
- ControlTemplate [WPF], Button
ms.assetid: e223c759-f8c4-4717-acfb-b1e40bdf5f3b
ms.openlocfilehash: 957c0663a8c444de71d2710bcff04cb73aaf3e27
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977369"
---
# <a name="button-styles-and-templates"></a><span data-ttu-id="9c59e-104">Button-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="9c59e-104">Button Styles and Templates</span></span>
<span data-ttu-id="9c59e-105">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.Button> .</span><span class="sxs-lookup"><span data-stu-id="9c59e-105">This topic describes the styles and templates for the <xref:System.Windows.Controls.Button> control.</span></span> <span data-ttu-id="9c59e-106">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="9c59e-106">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="9c59e-107">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="9c59e-107">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>  
  
## <a name="button-parts"></a><span data-ttu-id="9c59e-108">Schaltflächen Teile</span><span class="sxs-lookup"><span data-stu-id="9c59e-108">Button Parts</span></span>  
 <span data-ttu-id="9c59e-109">Das- <xref:System.Windows.Controls.Button> Steuerelement verfügt über keine benannten Teile.</span><span class="sxs-lookup"><span data-stu-id="9c59e-109">The <xref:System.Windows.Controls.Button> control does not have any named parts.</span></span>  
  
## <a name="button-states"></a><span data-ttu-id="9c59e-110">Schaltflächen Zustände</span><span class="sxs-lookup"><span data-stu-id="9c59e-110">Button States</span></span>  
 <span data-ttu-id="9c59e-111">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.Button> .</span><span class="sxs-lookup"><span data-stu-id="9c59e-111">The following table lists the visual states for the <xref:System.Windows.Controls.Button> control.</span></span>  
  
|<span data-ttu-id="9c59e-112">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="9c59e-112">VisualState Name</span></span>|<span data-ttu-id="9c59e-113">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="9c59e-113">VisualStateGroup Name</span></span>|<span data-ttu-id="9c59e-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c59e-114">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="9c59e-115">Normal</span><span class="sxs-lookup"><span data-stu-id="9c59e-115">Normal</span></span>|<span data-ttu-id="9c59e-116">CommonStates</span><span class="sxs-lookup"><span data-stu-id="9c59e-116">CommonStates</span></span>|<span data-ttu-id="9c59e-117">Der Standardzustand</span><span class="sxs-lookup"><span data-stu-id="9c59e-117">The default state.</span></span>|  
|<span data-ttu-id="9c59e-118">MouseOver</span><span class="sxs-lookup"><span data-stu-id="9c59e-118">MouseOver</span></span>|<span data-ttu-id="9c59e-119">CommonStates</span><span class="sxs-lookup"><span data-stu-id="9c59e-119">CommonStates</span></span>|<span data-ttu-id="9c59e-120">Der Mauszeiger ist über dem Steuerelement positioniert.</span><span class="sxs-lookup"><span data-stu-id="9c59e-120">The mouse pointer is positioned over the control.</span></span>|  
|<span data-ttu-id="9c59e-121">Gedrückt</span><span class="sxs-lookup"><span data-stu-id="9c59e-121">Pressed</span></span>|<span data-ttu-id="9c59e-122">CommonStates</span><span class="sxs-lookup"><span data-stu-id="9c59e-122">CommonStates</span></span>|<span data-ttu-id="9c59e-123">Das Steuerelement wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="9c59e-123">The control is pressed.</span></span>|  
|<span data-ttu-id="9c59e-124">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="9c59e-124">Disabled</span></span>|<span data-ttu-id="9c59e-125">CommonStates</span><span class="sxs-lookup"><span data-stu-id="9c59e-125">CommonStates</span></span>|<span data-ttu-id="9c59e-126">Das Steuerelement ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9c59e-126">The control is disabled.</span></span>|  
|<span data-ttu-id="9c59e-127">Focused</span><span class="sxs-lookup"><span data-stu-id="9c59e-127">Focused</span></span>|<span data-ttu-id="9c59e-128">FocusStates</span><span class="sxs-lookup"><span data-stu-id="9c59e-128">FocusStates</span></span>|<span data-ttu-id="9c59e-129">Der Fokus liegt auf dem Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9c59e-129">The control has focus.</span></span>|  
|<span data-ttu-id="9c59e-130">Ohne Fokus</span><span class="sxs-lookup"><span data-stu-id="9c59e-130">Unfocused</span></span>|<span data-ttu-id="9c59e-131">FocusStates</span><span class="sxs-lookup"><span data-stu-id="9c59e-131">FocusStates</span></span>|<span data-ttu-id="9c59e-132">Der Fokus liegt nicht auf dem Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9c59e-132">The control does not have focus.</span></span>|  
|<span data-ttu-id="9c59e-133">Gültig</span><span class="sxs-lookup"><span data-stu-id="9c59e-133">Valid</span></span>|<span data-ttu-id="9c59e-134">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="9c59e-134">ValidationStates</span></span>|<span data-ttu-id="9c59e-135">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="9c59e-135">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="9c59e-136">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="9c59e-136">InvalidFocused</span></span>|<span data-ttu-id="9c59e-137">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="9c59e-137">ValidationStates</span></span>|<span data-ttu-id="9c59e-138">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, `true` und das Steuerelement besitzt den Fokus.</span><span class="sxs-lookup"><span data-stu-id="9c59e-138">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` and the control has focus.</span></span>|  
|<span data-ttu-id="9c59e-139">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="9c59e-139">InvalidUnfocused</span></span>|<span data-ttu-id="9c59e-140">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="9c59e-140">ValidationStates</span></span>|<span data-ttu-id="9c59e-141">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, `true` und das Steuerelement besitzt keinen Fokus.</span><span class="sxs-lookup"><span data-stu-id="9c59e-141">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` and the control does not have focus.</span></span>|  
  
## <a name="button-controltemplate-example"></a><span data-ttu-id="9c59e-142">Schaltflächen-ControlTemplate-Beispiel</span><span class="sxs-lookup"><span data-stu-id="9c59e-142">Button ControlTemplate Example</span></span>  
 <span data-ttu-id="9c59e-143">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.Button> .</span><span class="sxs-lookup"><span data-stu-id="9c59e-143">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Button> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Button](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/button.xaml#button)]  
  
 <span data-ttu-id="9c59e-144">Im vorhergehenden Beispiel wird mindestens eine der folgenden Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c59e-144">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="9c59e-145">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="9c59e-145">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9c59e-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c59e-146">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="9c59e-147">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="9c59e-147">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="9c59e-148">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="9c59e-148">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="9c59e-149">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="9c59e-149">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="9c59e-150">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="9c59e-150">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
