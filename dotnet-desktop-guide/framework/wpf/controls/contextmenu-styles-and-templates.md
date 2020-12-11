---
title: ContextMenu-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- templates [WPF], ContextMenu
- parts [WPF], ContextMenu
- ContextMenu [WPF], styles and templates
- styles [WPF], ContextMenu
- ControlTemplate [WPF], ContextMenu
- states [WPF], ContextMenu
ms.assetid: 342d1f17-c406-4f94-8f55-867c5f3ea511
ms.openlocfilehash: 0f168c440c804c543ee9923d0021677ac529d5e1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977338"
---
# <a name="contextmenu-styles-and-templates"></a><span data-ttu-id="059fe-102">ContextMenu-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="059fe-102">ContextMenu Styles and Templates</span></span>
<span data-ttu-id="059fe-103">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.ContextMenu> .</span><span class="sxs-lookup"><span data-stu-id="059fe-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.ContextMenu> control.</span></span> <span data-ttu-id="059fe-104">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="059fe-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="059fe-105">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="059fe-105">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>  
  
## <a name="contextmenu-parts"></a><span data-ttu-id="059fe-106">ContextMenu-Teile</span><span class="sxs-lookup"><span data-stu-id="059fe-106">ContextMenu Parts</span></span>  
 <span data-ttu-id="059fe-107">Das- <xref:System.Windows.Controls.ContextMenu> Steuerelement verfügt über keine benannten Teile.</span><span class="sxs-lookup"><span data-stu-id="059fe-107">The <xref:System.Windows.Controls.ContextMenu> control does not have any named parts.</span></span>  
  
 <span data-ttu-id="059fe-108">Wenn Sie einen <xref:System.Windows.Controls.ControlTemplate> für eine erstellen <xref:System.Windows.Controls.ContextMenu> , enthält die Vorlage möglicherweise eine <xref:System.Windows.Controls.ItemsPresenter> innerhalb eines <xref:System.Windows.Controls.ScrollViewer> .</span><span class="sxs-lookup"><span data-stu-id="059fe-108">When you create a <xref:System.Windows.Controls.ControlTemplate> for a <xref:System.Windows.Controls.ContextMenu>, your template might contain an <xref:System.Windows.Controls.ItemsPresenter> within a <xref:System.Windows.Controls.ScrollViewer>.</span></span> <span data-ttu-id="059fe-109">(Die <xref:System.Windows.Controls.ItemsPresenter> zeigt jedes Element in der an <xref:System.Windows.Controls.ContextMenu> ; das <xref:System.Windows.Controls.ScrollViewer> ermöglicht das Scrollen im-Steuerelement).</span><span class="sxs-lookup"><span data-stu-id="059fe-109">(The <xref:System.Windows.Controls.ItemsPresenter> displays each item in the <xref:System.Windows.Controls.ContextMenu>; the <xref:System.Windows.Controls.ScrollViewer> enables scrolling within the control).</span></span>  <span data-ttu-id="059fe-110">Wenn das <xref:System.Windows.Controls.ItemsPresenter> nicht das direkt untergeordnete Element von ist <xref:System.Windows.Controls.ScrollViewer> , müssen Sie den <xref:System.Windows.Controls.ItemsPresenter> Namen, `ItemsPresenter` .</span><span class="sxs-lookup"><span data-stu-id="059fe-110">If the <xref:System.Windows.Controls.ItemsPresenter> is not the direct child of the <xref:System.Windows.Controls.ScrollViewer>, you must give the <xref:System.Windows.Controls.ItemsPresenter> the name, `ItemsPresenter`.</span></span>  
  
## <a name="contextmenu-states"></a><span data-ttu-id="059fe-111">ContextMenu-Zustände</span><span class="sxs-lookup"><span data-stu-id="059fe-111">ContextMenu States</span></span>  
 <span data-ttu-id="059fe-112">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.ContextMenu> .</span><span class="sxs-lookup"><span data-stu-id="059fe-112">The following table lists the visual states for the <xref:System.Windows.Controls.ContextMenu> control.</span></span>  
  
|<span data-ttu-id="059fe-113">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="059fe-113">VisualState Name</span></span>|<span data-ttu-id="059fe-114">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="059fe-114">VisualStateGroup Name</span></span>|<span data-ttu-id="059fe-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="059fe-115">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="059fe-116">Gültig</span><span class="sxs-lookup"><span data-stu-id="059fe-116">Valid</span></span>|<span data-ttu-id="059fe-117">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="059fe-117">ValidationStates</span></span>|<span data-ttu-id="059fe-118">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="059fe-118">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="059fe-119">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="059fe-119">InvalidFocused</span></span>|<span data-ttu-id="059fe-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="059fe-120">ValidationStates</span></span>|<span data-ttu-id="059fe-121">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="059fe-121">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="059fe-122">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="059fe-122">InvalidUnfocused</span></span>|<span data-ttu-id="059fe-123">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="059fe-123">ValidationStates</span></span>|<span data-ttu-id="059fe-124">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="059fe-124">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="contextmenu-controltemplate-example"></a><span data-ttu-id="059fe-125">ContextMenu ControlTemplate-Beispiel</span><span class="sxs-lookup"><span data-stu-id="059fe-125">ContextMenu ControlTemplate Example</span></span>  
 <span data-ttu-id="059fe-126">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.ContextMenu> .</span><span class="sxs-lookup"><span data-stu-id="059fe-126">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.ContextMenu> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ContextMenu](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/menu.xaml#contextmenu)]  
  
 <span data-ttu-id="059fe-127"><xref:System.Windows.Controls.ControlTemplate>Verwendet die folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="059fe-127">The <xref:System.Windows.Controls.ControlTemplate> uses the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="059fe-128">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="059fe-128">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="059fe-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="059fe-129">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="059fe-130">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="059fe-130">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="059fe-131">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="059fe-131">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="059fe-132">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="059fe-132">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="059fe-133">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="059fe-133">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
