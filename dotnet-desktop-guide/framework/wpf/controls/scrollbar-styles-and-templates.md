---
title: ScrollBar-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- styles [WPF], ScrollBar
- ControlTemplate [WPF], ScrollBar
- states [WPF], ScrollBar
- ScrollBar [WPF], styles and templates
- templates [WPF], ScrollBar
- parts [WPF], ScrollBar
ms.assetid: 066ea45a-e27d-43b0-adfe-cce6934c22f5
ms.openlocfilehash: 4c4a0e4eeb6d9d58470973dc8ae1877b8fef9bde
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977079"
---
# <a name="scrollbar-styles-and-templates"></a><span data-ttu-id="7bf22-102">ScrollBar-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="7bf22-102">ScrollBar Styles and Templates</span></span>
<span data-ttu-id="7bf22-103">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.Primitives.ScrollBar> .</span><span class="sxs-lookup"><span data-stu-id="7bf22-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Primitives.ScrollBar> control.</span></span> <span data-ttu-id="7bf22-104">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="7bf22-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="7bf22-105">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="7bf22-105">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>  
  
## <a name="scrollbar-parts"></a><span data-ttu-id="7bf22-106">ScrollBar-Teile</span><span class="sxs-lookup"><span data-stu-id="7bf22-106">ScrollBar Parts</span></span>  
 <span data-ttu-id="7bf22-107">In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.Primitives.ScrollBar> .</span><span class="sxs-lookup"><span data-stu-id="7bf22-107">The following table lists the named parts for the <xref:System.Windows.Controls.Primitives.ScrollBar> control.</span></span>  
  
|<span data-ttu-id="7bf22-108">Teil</span><span class="sxs-lookup"><span data-stu-id="7bf22-108">Part</span></span>|<span data-ttu-id="7bf22-109">type</span><span class="sxs-lookup"><span data-stu-id="7bf22-109">Type</span></span>|<span data-ttu-id="7bf22-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bf22-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="7bf22-111">PART_Track</span><span class="sxs-lookup"><span data-stu-id="7bf22-111">PART_Track</span></span>|<xref:System.Windows.Controls.Primitives.Track>|<span data-ttu-id="7bf22-112">Der Container für das Element, das die Position der angibt <xref:System.Windows.Controls.Primitives.ScrollBar> .</span><span class="sxs-lookup"><span data-stu-id="7bf22-112">The container for the element that indicates the position of the <xref:System.Windows.Controls.Primitives.ScrollBar>.</span></span>|  
  
## <a name="scrollbar-states"></a><span data-ttu-id="7bf22-113">ScrollBar-Zustände</span><span class="sxs-lookup"><span data-stu-id="7bf22-113">ScrollBar States</span></span>  
 <span data-ttu-id="7bf22-114">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.Primitives.ScrollBar> .</span><span class="sxs-lookup"><span data-stu-id="7bf22-114">The following table lists the visual states for the <xref:System.Windows.Controls.Primitives.ScrollBar> control.</span></span>  
  
|<span data-ttu-id="7bf22-115">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="7bf22-115">VisualState Name</span></span>|<span data-ttu-id="7bf22-116">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="7bf22-116">VisualStateGroup Name</span></span>|<span data-ttu-id="7bf22-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7bf22-117">Description</span></span>|  
|----------------------|---------------------------|-----------------|  
|<span data-ttu-id="7bf22-118">Normal</span><span class="sxs-lookup"><span data-stu-id="7bf22-118">Normal</span></span>|<span data-ttu-id="7bf22-119">CommonStates</span><span class="sxs-lookup"><span data-stu-id="7bf22-119">CommonStates</span></span>|<span data-ttu-id="7bf22-120">Der Standardzustand</span><span class="sxs-lookup"><span data-stu-id="7bf22-120">The default state.</span></span>|  
|<span data-ttu-id="7bf22-121">MouseOver</span><span class="sxs-lookup"><span data-stu-id="7bf22-121">MouseOver</span></span>|<span data-ttu-id="7bf22-122">CommonStates</span><span class="sxs-lookup"><span data-stu-id="7bf22-122">CommonStates</span></span>|<span data-ttu-id="7bf22-123">Der Mauszeiger ist über dem Steuerelement positioniert.</span><span class="sxs-lookup"><span data-stu-id="7bf22-123">The mouse pointer is positioned over the control.</span></span>|  
|<span data-ttu-id="7bf22-124">Deaktiviert</span><span class="sxs-lookup"><span data-stu-id="7bf22-124">Disabled</span></span>|<span data-ttu-id="7bf22-125">CommonStates</span><span class="sxs-lookup"><span data-stu-id="7bf22-125">CommonStates</span></span>|<span data-ttu-id="7bf22-126">Das Steuerelement ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7bf22-126">The control is disabled.</span></span>|  
|<span data-ttu-id="7bf22-127">Gültig</span><span class="sxs-lookup"><span data-stu-id="7bf22-127">Valid</span></span>|<span data-ttu-id="7bf22-128">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="7bf22-128">ValidationStates</span></span>|<span data-ttu-id="7bf22-129">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="7bf22-129">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="7bf22-130">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="7bf22-130">InvalidFocused</span></span>|<span data-ttu-id="7bf22-131">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="7bf22-131">ValidationStates</span></span>|<span data-ttu-id="7bf22-132">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, `true` und das Steuerelement besitzt den Fokus.</span><span class="sxs-lookup"><span data-stu-id="7bf22-132">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` and the control has focus.</span></span>|  
|<span data-ttu-id="7bf22-133">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="7bf22-133">InvalidUnfocused</span></span>|<span data-ttu-id="7bf22-134">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="7bf22-134">ValidationStates</span></span>|<span data-ttu-id="7bf22-135">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, `true` und das Steuerelement besitzt keinen Fokus.</span><span class="sxs-lookup"><span data-stu-id="7bf22-135">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` and the control does not have focus.</span></span>|  
  
## <a name="scrollbar-controltemplate-example"></a><span data-ttu-id="7bf22-136">ScrollBar ControlTemplate-Beispiel</span><span class="sxs-lookup"><span data-stu-id="7bf22-136">ScrollBar ControlTemplate Example</span></span>  
 <span data-ttu-id="7bf22-137">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.Primitives.ScrollBar> .</span><span class="sxs-lookup"><span data-stu-id="7bf22-137">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Primitives.ScrollBar> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ScrollBar](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/scrollbar.xaml#scrollbar)]  
  
 <span data-ttu-id="7bf22-138">Im vorhergehenden Beispiel wird mindestens eine der folgenden Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7bf22-138">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="7bf22-139">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="7bf22-139">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7bf22-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bf22-140">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="7bf22-141">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="7bf22-141">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="7bf22-142">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="7bf22-142">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="7bf22-143">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="7bf22-143">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="7bf22-144">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="7bf22-144">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
