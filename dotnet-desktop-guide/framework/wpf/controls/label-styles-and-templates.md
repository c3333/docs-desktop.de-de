---
title: Bezeichnungsformate und -vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- templates [WPF], Label
- parts [WPF], Label
- ControlTemplate [WPF], Label
- styles [WPF], Label
- Label [WPF], styles and templates
- states [WPF], Label
ms.assetid: c1d5359a-8e4a-4925-ab3e-e92bf6694859
ms.openlocfilehash: 476f10a11c497633e2650403068576633d517937
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977335"
---
# <a name="label-styles-and-templates"></a><span data-ttu-id="2e01e-102">Bezeichnungsformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="2e01e-102">Label Styles and Templates</span></span>
<span data-ttu-id="2e01e-103">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.Label> .</span><span class="sxs-lookup"><span data-stu-id="2e01e-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.Label> control.</span></span> <span data-ttu-id="2e01e-104">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="2e01e-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="2e01e-105">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="2e01e-105">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>  
  
## <a name="label-parts"></a><span data-ttu-id="2e01e-106">Bezeichnungs Teile</span><span class="sxs-lookup"><span data-stu-id="2e01e-106">Label Parts</span></span>  
 <span data-ttu-id="2e01e-107">Das- <xref:System.Windows.Controls.Label> Steuerelement verfügt über keine benannten Teile.</span><span class="sxs-lookup"><span data-stu-id="2e01e-107">The <xref:System.Windows.Controls.Label> control does not have any named parts.</span></span>  
  
## <a name="label-states"></a><span data-ttu-id="2e01e-108">Bezeichnungs Zustände</span><span class="sxs-lookup"><span data-stu-id="2e01e-108">Label States</span></span>  
 <span data-ttu-id="2e01e-109">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.Label> .</span><span class="sxs-lookup"><span data-stu-id="2e01e-109">The following table lists the visual states for the <xref:System.Windows.Controls.Label> control.</span></span>  
  
|<span data-ttu-id="2e01e-110">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="2e01e-110">VisualState Name</span></span>|<span data-ttu-id="2e01e-111">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="2e01e-111">VisualStateGroup Name</span></span>|<span data-ttu-id="2e01e-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2e01e-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="2e01e-113">Gültig</span><span class="sxs-lookup"><span data-stu-id="2e01e-113">Valid</span></span>|<span data-ttu-id="2e01e-114">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="2e01e-114">ValidationStates</span></span>|<span data-ttu-id="2e01e-115">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="2e01e-115">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="2e01e-116">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="2e01e-116">InvalidFocused</span></span>|<span data-ttu-id="2e01e-117">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="2e01e-117">ValidationStates</span></span>|<span data-ttu-id="2e01e-118">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="2e01e-118">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="2e01e-119">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="2e01e-119">InvalidUnfocused</span></span>|<span data-ttu-id="2e01e-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="2e01e-120">ValidationStates</span></span>|<span data-ttu-id="2e01e-121">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="2e01e-121">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="label-controltemplate-example"></a><span data-ttu-id="2e01e-122">Beispiel für Bezeichnung "ControlTemplate"</span><span class="sxs-lookup"><span data-stu-id="2e01e-122">Label ControlTemplate Example</span></span>  
 <span data-ttu-id="2e01e-123">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.Label> .</span><span class="sxs-lookup"><span data-stu-id="2e01e-123">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.Label> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Label](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/label.xaml#label)]  
  
 <span data-ttu-id="2e01e-124"><xref:System.Windows.Controls.ControlTemplate>Verwendet mindestens eine der folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="2e01e-124">The <xref:System.Windows.Controls.ControlTemplate> uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="2e01e-125">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="2e01e-125">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="2e01e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e01e-126">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="2e01e-127">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="2e01e-127">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="2e01e-128">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="2e01e-128">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="2e01e-129">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="2e01e-129">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="2e01e-130">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="2e01e-130">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
