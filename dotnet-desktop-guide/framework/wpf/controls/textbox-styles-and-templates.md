---
title: TextBox-Stile und -Vorlagen
description: Erfahren Sie mehr über Stile und Vorlagen für das Windows Presentation Foundation TextBox-Steuerelement. Ändern Sie ControlTemplate, um dem Steuerelement eine eindeutige Darstellung zu verschaffen.
ms.date: 03/30/2017
helpviewer_keywords:
- ControlTemplate [WPF], TextBox
- parts [WPF], TextBox
- states [WPF], TextBox
- styles [WPF], TextBox
- templates [WPF], TextBox
- TextBox [WPF], styles and templates
ms.assetid: aa99130c-43a1-450f-9b46-c40ae0db0cca
ms.openlocfilehash: e8c1bcbdeaf8b9b6d8bba2ccaf802e48dca02047
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974543"
---
# <a name="textbox-styles-and-templates"></a><span data-ttu-id="c488d-104">TextBox-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="c488d-104">TextBox Styles and Templates</span></span>
<span data-ttu-id="c488d-105">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="c488d-105">This topic describes the styles and templates for the <xref:System.Windows.Controls.TextBox> control.</span></span> <span data-ttu-id="c488d-106">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="c488d-106">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="c488d-107">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="c488d-107">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>  
  
## <a name="textbox-parts"></a><span data-ttu-id="c488d-108">Text Feld Teile</span><span class="sxs-lookup"><span data-stu-id="c488d-108">TextBox Parts</span></span>  
 <span data-ttu-id="c488d-109">In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="c488d-109">The following table lists the named parts for the <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
|<span data-ttu-id="c488d-110">Teil</span><span class="sxs-lookup"><span data-stu-id="c488d-110">Part</span></span>|<span data-ttu-id="c488d-111">type</span><span class="sxs-lookup"><span data-stu-id="c488d-111">Type</span></span>|<span data-ttu-id="c488d-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c488d-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="c488d-113">PART_ContentHost</span><span class="sxs-lookup"><span data-stu-id="c488d-113">PART_ContentHost</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="c488d-114">Ein visuelles Element, das ein enthalten kann <xref:System.Windows.FrameworkElement> .</span><span class="sxs-lookup"><span data-stu-id="c488d-114">A visual element that can contain a <xref:System.Windows.FrameworkElement>.</span></span> <span data-ttu-id="c488d-115">Der Text des <xref:System.Windows.Controls.TextBox> wird in diesem Element angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c488d-115">The text of the <xref:System.Windows.Controls.TextBox> is displayed in this element.</span></span>|  
  
## <a name="textbox-states"></a><span data-ttu-id="c488d-116">TextBox-Zustände</span><span class="sxs-lookup"><span data-stu-id="c488d-116">TextBox States</span></span>  
 <span data-ttu-id="c488d-117">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="c488d-117">The following table lists the visual states for the <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
|<span data-ttu-id="c488d-118">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="c488d-118">VisualState Name</span></span>|<span data-ttu-id="c488d-119">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="c488d-119">VisualStateGroup Name</span></span>|<span data-ttu-id="c488d-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c488d-120">Description</span></span>|  
|----------------------|---------------------------|-----------------|  
|<span data-ttu-id="c488d-121">Normal</span><span class="sxs-lookup"><span data-stu-id="c488d-121">Normal</span></span>|<span data-ttu-id="c488d-122">CommonStates</span><span class="sxs-lookup"><span data-stu-id="c488d-122">CommonStates</span></span>|<span data-ttu-id="c488d-123">Der Standardzustand</span><span class="sxs-lookup"><span data-stu-id="c488d-123">The default state.</span></span>|  
|<span data-ttu-id="c488d-124">MouseOver</span><span class="sxs-lookup"><span data-stu-id="c488d-124">MouseOver</span></span>|<span data-ttu-id="c488d-125">CommonStates</span><span class="sxs-lookup"><span data-stu-id="c488d-125">CommonStates</span></span>|<span data-ttu-id="c488d-126">Der Mauszeiger ist über dem Steuerelement positioniert.</span><span class="sxs-lookup"><span data-stu-id="c488d-126">The mouse pointer is positioned over the control.</span></span>|  
|<span data-ttu-id="c488d-127">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="c488d-127">Disabled</span></span>|<span data-ttu-id="c488d-128">CommonStates</span><span class="sxs-lookup"><span data-stu-id="c488d-128">CommonStates</span></span>|<span data-ttu-id="c488d-129">Das Steuerelement ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c488d-129">The control is disabled.</span></span>|  
|<span data-ttu-id="c488d-130">ReadOnly</span><span class="sxs-lookup"><span data-stu-id="c488d-130">ReadOnly</span></span>|<span data-ttu-id="c488d-131">CommonStates</span><span class="sxs-lookup"><span data-stu-id="c488d-131">CommonStates</span></span>|<span data-ttu-id="c488d-132">Der Benutzer kann den Text in der nicht ändern <xref:System.Windows.Controls.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="c488d-132">The user cannot change the text in the <xref:System.Windows.Controls.TextBox>.</span></span>|  
|<span data-ttu-id="c488d-133">Focused</span><span class="sxs-lookup"><span data-stu-id="c488d-133">Focused</span></span>|<span data-ttu-id="c488d-134">FocusStates</span><span class="sxs-lookup"><span data-stu-id="c488d-134">FocusStates</span></span>|<span data-ttu-id="c488d-135">Der Fokus liegt auf dem Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c488d-135">The control has focus.</span></span>|  
|<span data-ttu-id="c488d-136">Ohne Fokus</span><span class="sxs-lookup"><span data-stu-id="c488d-136">Unfocused</span></span>|<span data-ttu-id="c488d-137">FocusStates</span><span class="sxs-lookup"><span data-stu-id="c488d-137">FocusStates</span></span>|<span data-ttu-id="c488d-138">Der Fokus liegt nicht auf dem Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="c488d-138">The control does not have focus.</span></span>|  
|<span data-ttu-id="c488d-139">Gültig</span><span class="sxs-lookup"><span data-stu-id="c488d-139">Valid</span></span>|<span data-ttu-id="c488d-140">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="c488d-140">ValidationStates</span></span>|<span data-ttu-id="c488d-141">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="c488d-141">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="c488d-142">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="c488d-142">InvalidFocused</span></span>|<span data-ttu-id="c488d-143">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="c488d-143">ValidationStates</span></span>|<span data-ttu-id="c488d-144">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="c488d-144">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="c488d-145">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="c488d-145">InvalidUnfocused</span></span>|<span data-ttu-id="c488d-146">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="c488d-146">ValidationStates</span></span>|<span data-ttu-id="c488d-147">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="c488d-147">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="textbox-controltemplate-example"></a><span data-ttu-id="c488d-148">TextBox-ControlTemplate-Beispiel</span><span class="sxs-lookup"><span data-stu-id="c488d-148">TextBox ControlTemplate Example</span></span>  
 <span data-ttu-id="c488d-149">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="c488d-149">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.TextBox> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#TextBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/textbox.xaml#textbox)]  
  
 <span data-ttu-id="c488d-150">Im vorhergehenden Beispiel wird mindestens eine der folgenden Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c488d-150">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="c488d-151">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="c488d-151">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c488d-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c488d-152">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="c488d-153">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="c488d-153">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="c488d-154">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="c488d-154">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="c488d-155">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="c488d-155">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="c488d-156">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c488d-156">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
