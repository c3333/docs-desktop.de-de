---
title: Frame-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], Frame
- templates [WPF], Frame
- ControlTemplate [WPF], Frame
- Frame [WPF], styles and templates
- states [WPF], Frame
- styles [WPF], Frame
ms.assetid: a01c32e2-c951-46a0-a82f-2614ca241f0b
ms.openlocfilehash: 106a7a2a0138250261ce31b0cbd98173b14e749a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974943"
---
# <a name="frame-styles-and-templates"></a><span data-ttu-id="09a88-102">Frame-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="09a88-102">Frame Styles and Templates</span></span>
<span data-ttu-id="09a88-103">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.Frame> .</span><span class="sxs-lookup"><span data-stu-id="09a88-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Frame> control.</span></span> <span data-ttu-id="09a88-104">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="09a88-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="09a88-105">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="09a88-105">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>  
  
## <a name="frame-parts"></a><span data-ttu-id="09a88-106">Frame Teile</span><span class="sxs-lookup"><span data-stu-id="09a88-106">Frame Parts</span></span>  
 <span data-ttu-id="09a88-107">In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.Frame> .</span><span class="sxs-lookup"><span data-stu-id="09a88-107">The following table lists the named parts for the <xref:System.Windows.Controls.Frame> control.</span></span>  
  
|<span data-ttu-id="09a88-108">Teil</span><span class="sxs-lookup"><span data-stu-id="09a88-108">Part</span></span>|<span data-ttu-id="09a88-109">type</span><span class="sxs-lookup"><span data-stu-id="09a88-109">Type</span></span>|<span data-ttu-id="09a88-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="09a88-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="09a88-111">PART_FrameCP</span><span class="sxs-lookup"><span data-stu-id="09a88-111">PART_FrameCP</span></span>|<xref:System.Windows.Controls.ContentPresenter>|<span data-ttu-id="09a88-112">Der Inhalts Bereich.</span><span class="sxs-lookup"><span data-stu-id="09a88-112">The content area.</span></span>|  
  
## <a name="frame-states"></a><span data-ttu-id="09a88-113">Frame Zustände</span><span class="sxs-lookup"><span data-stu-id="09a88-113">Frame States</span></span>  
 <span data-ttu-id="09a88-114">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.Frame> .</span><span class="sxs-lookup"><span data-stu-id="09a88-114">The following table lists the visual states for the <xref:System.Windows.Controls.Frame> control.</span></span>  
  
|<span data-ttu-id="09a88-115">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="09a88-115">VisualState Name</span></span>|<span data-ttu-id="09a88-116">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="09a88-116">VisualStateGroup Name</span></span>|<span data-ttu-id="09a88-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09a88-117">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="09a88-118">Gültig</span><span class="sxs-lookup"><span data-stu-id="09a88-118">Valid</span></span>|<span data-ttu-id="09a88-119">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="09a88-119">ValidationStates</span></span>|<span data-ttu-id="09a88-120">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="09a88-120">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="09a88-121">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="09a88-121">InvalidFocused</span></span>|<span data-ttu-id="09a88-122">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="09a88-122">ValidationStates</span></span>|<span data-ttu-id="09a88-123">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="09a88-123">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="09a88-124">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="09a88-124">InvalidUnfocused</span></span>|<span data-ttu-id="09a88-125">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="09a88-125">ValidationStates</span></span>|<span data-ttu-id="09a88-126">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="09a88-126">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="frame-controltemplate-example"></a><span data-ttu-id="09a88-127">Frame ControlTemplate-Beispiel</span><span class="sxs-lookup"><span data-stu-id="09a88-127">Frame ControlTemplate Example</span></span>  
 <span data-ttu-id="09a88-128">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.Frame> .</span><span class="sxs-lookup"><span data-stu-id="09a88-128">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Frame> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Frame](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/frame.xaml#frame)]  
  
 <span data-ttu-id="09a88-129">Im vorhergehenden Beispiel wird mindestens eine der folgenden Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="09a88-129">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="09a88-130">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="09a88-130">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="09a88-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09a88-131">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="09a88-132">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="09a88-132">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="09a88-133">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="09a88-133">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="09a88-134">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="09a88-134">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="09a88-135">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="09a88-135">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
