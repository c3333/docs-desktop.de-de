---
title: Slider-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], Slider
- states [WPF], Slider
- Slider [WPF], styles and templates
- styles [WPF], Slider
- templates [WPF], Slider
- ControlTemplate [WPF], Slider
ms.assetid: d89aa97b-075a-4752-9c41-9679df65c491
ms.openlocfilehash: d97e9c1e2783d2c348955622fbe98ea3916726d6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976987"
---
# <a name="slider-styles-and-templates"></a><span data-ttu-id="9ca74-102">Slider-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="9ca74-102">Slider Styles and Templates</span></span>
<span data-ttu-id="9ca74-103">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.Slider> .</span><span class="sxs-lookup"><span data-stu-id="9ca74-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Slider> control.</span></span> <span data-ttu-id="9ca74-104">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="9ca74-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="9ca74-105">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="9ca74-105">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>  
  
## <a name="slider-parts"></a><span data-ttu-id="9ca74-106">Schieberegler-Teile</span><span class="sxs-lookup"><span data-stu-id="9ca74-106">Slider Parts</span></span>  
 <span data-ttu-id="9ca74-107">In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.Slider> .</span><span class="sxs-lookup"><span data-stu-id="9ca74-107">The following table lists the named parts for the <xref:System.Windows.Controls.Slider> control.</span></span>  
  
|<span data-ttu-id="9ca74-108">Teil</span><span class="sxs-lookup"><span data-stu-id="9ca74-108">Part</span></span>|<span data-ttu-id="9ca74-109">type</span><span class="sxs-lookup"><span data-stu-id="9ca74-109">Type</span></span>|<span data-ttu-id="9ca74-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9ca74-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="9ca74-111">PART_Track</span><span class="sxs-lookup"><span data-stu-id="9ca74-111">PART_Track</span></span>|<xref:System.Windows.Controls.Primitives.Track>|<span data-ttu-id="9ca74-112">Der Container für das Element, das die Position der angibt <xref:System.Windows.Controls.Slider> .</span><span class="sxs-lookup"><span data-stu-id="9ca74-112">The container for the element that indicates the position of the <xref:System.Windows.Controls.Slider>.</span></span>|  
|<span data-ttu-id="9ca74-113">PART_SelectionRange</span><span class="sxs-lookup"><span data-stu-id="9ca74-113">PART_SelectionRange</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="9ca74-114">Das Element, das einen Auswahlbereich entlang der anzeigt <xref:System.Windows.Controls.Slider> .</span><span class="sxs-lookup"><span data-stu-id="9ca74-114">The element that displays a selection range along the <xref:System.Windows.Controls.Slider>.</span></span>  <span data-ttu-id="9ca74-115">Der Auswahlbereich ist nur sichtbar, wenn die- <xref:System.Windows.Controls.Slider.IsSelectionRangeEnabled%2A> Eigenschaft ist `true` .</span><span class="sxs-lookup"><span data-stu-id="9ca74-115">The selection range is visible only if the <xref:System.Windows.Controls.Slider.IsSelectionRangeEnabled%2A> property is `true`.</span></span>|  
  
## <a name="slider-states"></a><span data-ttu-id="9ca74-116">Schieberegler-Zustände</span><span class="sxs-lookup"><span data-stu-id="9ca74-116">Slider States</span></span>  
 <span data-ttu-id="9ca74-117">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.Slider> .</span><span class="sxs-lookup"><span data-stu-id="9ca74-117">The following table lists the visual states for the <xref:System.Windows.Controls.Slider> control.</span></span>  
  
|<span data-ttu-id="9ca74-118">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="9ca74-118">VisualState Name</span></span>|<span data-ttu-id="9ca74-119">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="9ca74-119">VisualStateGroup Name</span></span>|<span data-ttu-id="9ca74-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ca74-120">Description</span></span>|  
|----------------------|---------------------------|-----------------|  
|<span data-ttu-id="9ca74-121">Normal</span><span class="sxs-lookup"><span data-stu-id="9ca74-121">Normal</span></span>|<span data-ttu-id="9ca74-122">CommonStates</span><span class="sxs-lookup"><span data-stu-id="9ca74-122">CommonStates</span></span>|<span data-ttu-id="9ca74-123">Der Standardzustand</span><span class="sxs-lookup"><span data-stu-id="9ca74-123">The default state.</span></span>|  
|<span data-ttu-id="9ca74-124">MouseOver</span><span class="sxs-lookup"><span data-stu-id="9ca74-124">MouseOver</span></span>|<span data-ttu-id="9ca74-125">CommonStates</span><span class="sxs-lookup"><span data-stu-id="9ca74-125">CommonStates</span></span>|<span data-ttu-id="9ca74-126">Der Mauszeiger ist über dem Steuerelement positioniert.</span><span class="sxs-lookup"><span data-stu-id="9ca74-126">The mouse pointer is positioned over the control.</span></span>|  
|<span data-ttu-id="9ca74-127">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="9ca74-127">Disabled</span></span>|<span data-ttu-id="9ca74-128">CommonStates</span><span class="sxs-lookup"><span data-stu-id="9ca74-128">CommonStates</span></span>|<span data-ttu-id="9ca74-129">Das Steuerelement ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="9ca74-129">The control is disabled.</span></span>|  
|<span data-ttu-id="9ca74-130">Focused</span><span class="sxs-lookup"><span data-stu-id="9ca74-130">Focused</span></span>|<span data-ttu-id="9ca74-131">FocusStates</span><span class="sxs-lookup"><span data-stu-id="9ca74-131">FocusStates</span></span>|<span data-ttu-id="9ca74-132">Der Fokus liegt auf dem Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9ca74-132">The control has focus.</span></span>|  
|<span data-ttu-id="9ca74-133">Ohne Fokus</span><span class="sxs-lookup"><span data-stu-id="9ca74-133">Unfocused</span></span>|<span data-ttu-id="9ca74-134">FocusStates</span><span class="sxs-lookup"><span data-stu-id="9ca74-134">FocusStates</span></span>|<span data-ttu-id="9ca74-135">Der Fokus liegt nicht auf dem Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="9ca74-135">The control does not have focus.</span></span>|  
|<span data-ttu-id="9ca74-136">Gültig</span><span class="sxs-lookup"><span data-stu-id="9ca74-136">Valid</span></span>|<span data-ttu-id="9ca74-137">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="9ca74-137">ValidationStates</span></span>|<span data-ttu-id="9ca74-138">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="9ca74-138">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="9ca74-139">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="9ca74-139">InvalidFocused</span></span>|<span data-ttu-id="9ca74-140">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="9ca74-140">ValidationStates</span></span>|<span data-ttu-id="9ca74-141">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="9ca74-141">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="9ca74-142">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="9ca74-142">InvalidUnfocused</span></span>|<span data-ttu-id="9ca74-143">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="9ca74-143">ValidationStates</span></span>|<span data-ttu-id="9ca74-144">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="9ca74-144">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="slider-controltemplate-example"></a><span data-ttu-id="9ca74-145">Beispiel für Schieberegler-ControlTemplate</span><span class="sxs-lookup"><span data-stu-id="9ca74-145">Slider ControlTemplate Example</span></span>  
 <span data-ttu-id="9ca74-146">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.Slider> .</span><span class="sxs-lookup"><span data-stu-id="9ca74-146">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Slider> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Slider](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/slider.xaml#slider)]  
  
 <span data-ttu-id="9ca74-147">Im vorhergehenden Beispiel wird mindestens eine der folgenden Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9ca74-147">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="9ca74-148">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="9ca74-148">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9ca74-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ca74-149">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="9ca74-150">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="9ca74-150">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="9ca74-151">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="9ca74-151">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="9ca74-152">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="9ca74-152">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="9ca74-153">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="9ca74-153">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
