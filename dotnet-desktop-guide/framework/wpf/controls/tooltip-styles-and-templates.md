---
title: ToolTip-Formate und Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], ToolTip
- styles [WPF], ToolTip
- states [WPF], ToolTip
- ToolTip [WPF], styles and templates
- ControlTemplate [WPF], ToolTip
- templates [WPF], ToolTip
ms.assetid: 405fe385-4de9-49ee-a448-d8f4d1f740dd
ms.openlocfilehash: bc77555a7663bf1e4cd8cea82d43bf3bd2c33b53
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978227"
---
# <a name="tooltip-styles-and-templates"></a><span data-ttu-id="28a5f-102">ToolTip-Formate und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="28a5f-102">ToolTip Styles and Templates</span></span>
<span data-ttu-id="28a5f-103">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.ToolTip> .</span><span class="sxs-lookup"><span data-stu-id="28a5f-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.ToolTip> control.</span></span> <span data-ttu-id="28a5f-104">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="28a5f-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="28a5f-105">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="28a5f-105">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>  
  
## <a name="tooltip-parts"></a><span data-ttu-id="28a5f-106">QuickInfo-Teile</span><span class="sxs-lookup"><span data-stu-id="28a5f-106">ToolTip Parts</span></span>  
 <span data-ttu-id="28a5f-107">Das- <xref:System.Windows.Controls.ToolTip> Steuerelement verfügt über keine benannten Teile.</span><span class="sxs-lookup"><span data-stu-id="28a5f-107">The <xref:System.Windows.Controls.ToolTip> control does not have any named parts.</span></span>  
  
## <a name="tooltip-states"></a><span data-ttu-id="28a5f-108">QuickInfo-Zustände</span><span class="sxs-lookup"><span data-stu-id="28a5f-108">ToolTip States</span></span>  
 <span data-ttu-id="28a5f-109">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.ToolTip> .</span><span class="sxs-lookup"><span data-stu-id="28a5f-109">The following table lists the visual states for the <xref:System.Windows.Controls.ToolTip> control.</span></span>  
  
|<span data-ttu-id="28a5f-110">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="28a5f-110">VisualState Name</span></span>|<span data-ttu-id="28a5f-111">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="28a5f-111">VisualStateGroup Name</span></span>|<span data-ttu-id="28a5f-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28a5f-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="28a5f-113">Geschlossen</span><span class="sxs-lookup"><span data-stu-id="28a5f-113">Closed</span></span>|<span data-ttu-id="28a5f-114">Openstates</span><span class="sxs-lookup"><span data-stu-id="28a5f-114">OpenStates</span></span>|<span data-ttu-id="28a5f-115">Der Standardzustand</span><span class="sxs-lookup"><span data-stu-id="28a5f-115">The default state.</span></span>|  
|<span data-ttu-id="28a5f-116">Öffnen Sie den</span><span class="sxs-lookup"><span data-stu-id="28a5f-116">Open</span></span>|<span data-ttu-id="28a5f-117">Openstates</span><span class="sxs-lookup"><span data-stu-id="28a5f-117">OpenStates</span></span>|<span data-ttu-id="28a5f-118">Der <xref:System.Windows.Controls.ToolTip> ist sichtbar.</span><span class="sxs-lookup"><span data-stu-id="28a5f-118">The <xref:System.Windows.Controls.ToolTip> is visible.</span></span>|  
|<span data-ttu-id="28a5f-119">Gültig</span><span class="sxs-lookup"><span data-stu-id="28a5f-119">Valid</span></span>|<span data-ttu-id="28a5f-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="28a5f-120">ValidationStates</span></span>|<span data-ttu-id="28a5f-121">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="28a5f-121">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="28a5f-122">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="28a5f-122">InvalidFocused</span></span>|<span data-ttu-id="28a5f-123">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="28a5f-123">ValidationStates</span></span>|<span data-ttu-id="28a5f-124">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="28a5f-124">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="28a5f-125">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="28a5f-125">InvalidUnfocused</span></span>|<span data-ttu-id="28a5f-126">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="28a5f-126">ValidationStates</span></span>|<span data-ttu-id="28a5f-127">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="28a5f-127">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="tooltip-controltemplate-example"></a><span data-ttu-id="28a5f-128">QuickInfo-ControlTemplate-Beispiel</span><span class="sxs-lookup"><span data-stu-id="28a5f-128">ToolTip ControlTemplate Example</span></span>  
 <span data-ttu-id="28a5f-129">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.ToolTip> .</span><span class="sxs-lookup"><span data-stu-id="28a5f-129">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.ToolTip> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/tooltip.xaml#tooltip)]  
  
 <span data-ttu-id="28a5f-130">Im vorhergehenden Beispiel wird mindestens eine der folgenden Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="28a5f-130">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="28a5f-131">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="28a5f-131">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="28a5f-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28a5f-132">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="28a5f-133">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="28a5f-133">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="28a5f-134">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="28a5f-134">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="28a5f-135">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="28a5f-135">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="28a5f-136">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="28a5f-136">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
