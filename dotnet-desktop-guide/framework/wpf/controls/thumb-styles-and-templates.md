---
title: Thumb-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- states [WPF], Thumb
- styles [WPF], Thumb
- templates [WPF], Thumb
- Thumb [WPF], styles and templates
- ControlTemplate [WPF], Thumb
- parts [WPF], Thumb
ms.assetid: 86a49235-62d9-414e-923e-53126e3f930a
ms.openlocfilehash: 6c14280f9514e3c9b1716b55410a46cf843f6b8c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974563"
---
# <a name="thumb-styles-and-templates"></a><span data-ttu-id="57bc4-102">Thumb-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="57bc4-102">Thumb Styles and Templates</span></span>

<span data-ttu-id="57bc4-103">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.Primitives.Thumb> .</span><span class="sxs-lookup"><span data-stu-id="57bc4-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Primitives.Thumb> control.</span></span> <span data-ttu-id="57bc4-104">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="57bc4-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="57bc4-105">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="57bc4-105">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>

## <a name="thumb-parts"></a><span data-ttu-id="57bc4-106">Thumb-Teile</span><span class="sxs-lookup"><span data-stu-id="57bc4-106">Thumb Parts</span></span>

<span data-ttu-id="57bc4-107">Das- <xref:System.Windows.Controls.Primitives.Thumb> Steuerelement verfügt über keine benannten Teile.</span><span class="sxs-lookup"><span data-stu-id="57bc4-107">The <xref:System.Windows.Controls.Primitives.Thumb> control does not have any named parts.</span></span>

## <a name="thumb-states"></a><span data-ttu-id="57bc4-108">Thumb-Zustände</span><span class="sxs-lookup"><span data-stu-id="57bc4-108">Thumb States</span></span>

<span data-ttu-id="57bc4-109">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.Primitives.Thumb> .</span><span class="sxs-lookup"><span data-stu-id="57bc4-109">The following table lists the visual states for the <xref:System.Windows.Controls.Primitives.Thumb> control.</span></span>

|<span data-ttu-id="57bc4-110">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="57bc4-110">VisualState Name</span></span>|<span data-ttu-id="57bc4-111">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="57bc4-111">VisualStateGroup Name</span></span>|<span data-ttu-id="57bc4-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57bc4-112">Description</span></span>|
|-|-|-|
|<span data-ttu-id="57bc4-113">Normal</span><span class="sxs-lookup"><span data-stu-id="57bc4-113">Normal</span></span>|<span data-ttu-id="57bc4-114">CommonStates</span><span class="sxs-lookup"><span data-stu-id="57bc4-114">CommonStates</span></span>|<span data-ttu-id="57bc4-115">Der Standardzustand</span><span class="sxs-lookup"><span data-stu-id="57bc4-115">The default state.</span></span>|
|<span data-ttu-id="57bc4-116">MouseOver</span><span class="sxs-lookup"><span data-stu-id="57bc4-116">MouseOver</span></span>|<span data-ttu-id="57bc4-117">CommonStates</span><span class="sxs-lookup"><span data-stu-id="57bc4-117">CommonStates</span></span>|<span data-ttu-id="57bc4-118">Der Mauszeiger ist über dem Steuerelement positioniert.</span><span class="sxs-lookup"><span data-stu-id="57bc4-118">The mouse pointer is positioned over the control.</span></span>|
|<span data-ttu-id="57bc4-119">Gedrückt</span><span class="sxs-lookup"><span data-stu-id="57bc4-119">Pressed</span></span>|<span data-ttu-id="57bc4-120">CommonStates</span><span class="sxs-lookup"><span data-stu-id="57bc4-120">CommonStates</span></span>|<span data-ttu-id="57bc4-121">Das Steuerelement wird gedrückt.</span><span class="sxs-lookup"><span data-stu-id="57bc4-121">The control is pressed.</span></span>|
|<span data-ttu-id="57bc4-122">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="57bc4-122">Disabled</span></span>|<span data-ttu-id="57bc4-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="57bc4-123">CommonStates</span></span>|<span data-ttu-id="57bc4-124">Das Steuerelement ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="57bc4-124">The control is disabled.</span></span>|
|<span data-ttu-id="57bc4-125">Focused</span><span class="sxs-lookup"><span data-stu-id="57bc4-125">Focused</span></span>|<span data-ttu-id="57bc4-126">FocusStates</span><span class="sxs-lookup"><span data-stu-id="57bc4-126">FocusStates</span></span>|<span data-ttu-id="57bc4-127">Der Fokus liegt auf dem Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="57bc4-127">The control has focus.</span></span>|
|<span data-ttu-id="57bc4-128">Ohne Fokus</span><span class="sxs-lookup"><span data-stu-id="57bc4-128">Unfocused</span></span>|<span data-ttu-id="57bc4-129">FocusStates</span><span class="sxs-lookup"><span data-stu-id="57bc4-129">FocusStates</span></span>|<span data-ttu-id="57bc4-130">Der Fokus liegt nicht auf dem Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="57bc4-130">The control does not have focus.</span></span>|
|<span data-ttu-id="57bc4-131">Gültig</span><span class="sxs-lookup"><span data-stu-id="57bc4-131">Valid</span></span>|<span data-ttu-id="57bc4-132">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="57bc4-132">ValidationStates</span></span>|<span data-ttu-id="57bc4-133">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="57bc4-133">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|
|<span data-ttu-id="57bc4-134">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="57bc4-134">InvalidFocused</span></span>|<span data-ttu-id="57bc4-135">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="57bc4-135">ValidationStates</span></span>|<span data-ttu-id="57bc4-136">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="57bc4-136">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|
|<span data-ttu-id="57bc4-137">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="57bc4-137">InvalidUnfocused</span></span>|<span data-ttu-id="57bc4-138">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="57bc4-138">ValidationStates</span></span>|<span data-ttu-id="57bc4-139">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="57bc4-139">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|

## <a name="thumb-controltemplate-example"></a><span data-ttu-id="57bc4-140">Thumb ControlTemplate-Beispiel</span><span class="sxs-lookup"><span data-stu-id="57bc4-140">Thumb ControlTemplate Example</span></span>

<span data-ttu-id="57bc4-141">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.Primitives.Thumb> .</span><span class="sxs-lookup"><span data-stu-id="57bc4-141">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Primitives.Thumb> control.</span></span>

[!code-xaml[ControlTemplateExamples#Thumb](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/slider.xaml#thumb)]

<span data-ttu-id="57bc4-142">Im vorhergehenden Beispiel wird mindestens eine der folgenden Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="57bc4-142">The preceding example uses one or more of the following resources.</span></span>

[!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]

<span data-ttu-id="57bc4-143">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="57bc4-143">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>

## <a name="see-also"></a><span data-ttu-id="57bc4-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57bc4-144">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="57bc4-145">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="57bc4-145">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="57bc4-146">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="57bc4-146">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="57bc4-147">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="57bc4-147">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="57bc4-148">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="57bc4-148">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
