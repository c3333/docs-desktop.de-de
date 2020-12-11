---
title: GroupBox-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- ControlTemplate [WPF], GroupBox
- parts [WPF], GroupBox
- GroupBox [WPF], styles and templates
- states [WPF], GroupBox
- styles [WPF], GroupBox
- templates [WPF], GroupBox
ms.assetid: 33df7037-0a1b-476f-b9d0-41566a777699
ms.openlocfilehash: 8648c284a1da3e7d629bec91210c8dd5ecdb8484
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977049"
---
# <a name="groupbox-styles-and-templates"></a><span data-ttu-id="44f83-102">GroupBox-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="44f83-102">GroupBox Styles and Templates</span></span>
<a name="introduction"></a> <span data-ttu-id="44f83-103">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.GroupBox> .</span><span class="sxs-lookup"><span data-stu-id="44f83-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.GroupBox> control.</span></span> <span data-ttu-id="44f83-104">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="44f83-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="44f83-105">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="44f83-105">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>  
  
<a name="groupbox_parts"></a>
## <a name="groupbox-parts"></a><span data-ttu-id="44f83-106">GroupBox-Teile</span><span class="sxs-lookup"><span data-stu-id="44f83-106">GroupBox Parts</span></span>  
 <span data-ttu-id="44f83-107">Das- <xref:System.Windows.Controls.GroupBox> Steuerelement verfügt über keine benannten Teile.</span><span class="sxs-lookup"><span data-stu-id="44f83-107">The <xref:System.Windows.Controls.GroupBox> control does not have any named parts.</span></span>  
  
<a name="groupbox_states"></a>
## <a name="groupbox-states"></a><span data-ttu-id="44f83-108">GroupBox-Zustände</span><span class="sxs-lookup"><span data-stu-id="44f83-108">GroupBox States</span></span>  
 <span data-ttu-id="44f83-109">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.GroupBox> .</span><span class="sxs-lookup"><span data-stu-id="44f83-109">The following table lists the visual states for the <xref:System.Windows.Controls.GroupBox> control.</span></span>  
  
|<span data-ttu-id="44f83-110">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="44f83-110">VisualState Name</span></span>|<span data-ttu-id="44f83-111">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="44f83-111">VisualStateGroup Name</span></span>|<span data-ttu-id="44f83-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="44f83-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="44f83-113">Gültig</span><span class="sxs-lookup"><span data-stu-id="44f83-113">Valid</span></span>|<span data-ttu-id="44f83-114">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="44f83-114">ValidationStates</span></span>|<span data-ttu-id="44f83-115">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="44f83-115">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="44f83-116">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="44f83-116">InvalidFocused</span></span>|<span data-ttu-id="44f83-117">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="44f83-117">ValidationStates</span></span>|<span data-ttu-id="44f83-118">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="44f83-118">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="44f83-119">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="44f83-119">InvalidUnfocused</span></span>|<span data-ttu-id="44f83-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="44f83-120">ValidationStates</span></span>|<span data-ttu-id="44f83-121">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="44f83-121">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
<a name="groupbox_controltemplate_example"></a>
## <a name="groupbox-controltemplate-example"></a><span data-ttu-id="44f83-122">GroupBox ControlTemplate-Beispiel</span><span class="sxs-lookup"><span data-stu-id="44f83-122">GroupBox ControlTemplate Example</span></span>  
 <span data-ttu-id="44f83-123">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.GroupBox> .</span><span class="sxs-lookup"><span data-stu-id="44f83-123">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.GroupBox> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#GroupBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/groupbox.xaml#groupbox)]  
  
 <span data-ttu-id="44f83-124"><xref:System.Windows.Controls.ControlTemplate>Verwendet mindestens eine der folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="44f83-124">The <xref:System.Windows.Controls.ControlTemplate> uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="44f83-125">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="44f83-125">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44f83-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44f83-126">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="44f83-127">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="44f83-127">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="44f83-128">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="44f83-128">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="44f83-129">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="44f83-129">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="44f83-130">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="44f83-130">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
