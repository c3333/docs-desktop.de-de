---
title: ToolBar-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- states [WPF], ToolBar
- styles [WPF], ToolBar
- ControlTemplate [WPF], ToolBar
- parts [WPF], ToolBar
- ToolBar [WPF], styles and templates
- templates [WPF], ToolBar
ms.assetid: bd875f46-4690-46f5-81e0-f11a9822484f
ms.openlocfilehash: 1ece74e1c4aa1be9845bd812b29f2ad7f580d4e2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977024"
---
# <a name="toolbar-styles-and-templates"></a><span data-ttu-id="ee530-102">ToolBar-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="ee530-102">ToolBar Styles and Templates</span></span>
<span data-ttu-id="ee530-103">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.ToolBar> .</span><span class="sxs-lookup"><span data-stu-id="ee530-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.ToolBar> control.</span></span> <span data-ttu-id="ee530-104">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="ee530-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="ee530-105">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="ee530-105">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>  
  
## <a name="toolbar-parts"></a><span data-ttu-id="ee530-106">Symbolleisten Teile</span><span class="sxs-lookup"><span data-stu-id="ee530-106">ToolBar Parts</span></span>  
 <span data-ttu-id="ee530-107">In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.ToolBar> .</span><span class="sxs-lookup"><span data-stu-id="ee530-107">The following table lists the named parts for the <xref:System.Windows.Controls.ToolBar> control.</span></span>  
  
|<span data-ttu-id="ee530-108">Teil</span><span class="sxs-lookup"><span data-stu-id="ee530-108">Part</span></span>|<span data-ttu-id="ee530-109">type</span><span class="sxs-lookup"><span data-stu-id="ee530-109">Type</span></span>|<span data-ttu-id="ee530-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ee530-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="ee530-111">PART_ToolBarPanel</span><span class="sxs-lookup"><span data-stu-id="ee530-111">PART_ToolBarPanel</span></span>|<xref:System.Windows.Controls.Primitives.ToolBarPanel>|<span data-ttu-id="ee530-112">Das-Objekt, das die Steuerelemente auf dem enthält <xref:System.Windows.Controls.ToolBar> .</span><span class="sxs-lookup"><span data-stu-id="ee530-112">The object that contains the controls on the <xref:System.Windows.Controls.ToolBar>.</span></span>|  
|<span data-ttu-id="ee530-113">PART_ToolBarOverflowPanel</span><span class="sxs-lookup"><span data-stu-id="ee530-113">PART_ToolBarOverflowPanel</span></span>|<xref:System.Windows.Controls.Primitives.ToolBarOverflowPanel>|<span data-ttu-id="ee530-114">Das-Objekt, das die Steuerelemente enthält, die sich im Überlauf Bereich von befinden <xref:System.Windows.Controls.ToolBar> .</span><span class="sxs-lookup"><span data-stu-id="ee530-114">The object that contains the controls that are in the overflow area of the <xref:System.Windows.Controls.ToolBar>.</span></span>|  
  
 <span data-ttu-id="ee530-115">Wenn Sie einen <xref:System.Windows.Controls.ControlTemplate> für eine erstellen <xref:System.Windows.Controls.ToolBar> , enthält die Vorlage möglicherweise eine <xref:System.Windows.Controls.ItemsPresenter> innerhalb eines <xref:System.Windows.Controls.ScrollViewer> .</span><span class="sxs-lookup"><span data-stu-id="ee530-115">When you create a <xref:System.Windows.Controls.ControlTemplate> for a <xref:System.Windows.Controls.ToolBar>, your template might contain an <xref:System.Windows.Controls.ItemsPresenter> within a <xref:System.Windows.Controls.ScrollViewer>.</span></span> <span data-ttu-id="ee530-116">(Die <xref:System.Windows.Controls.ItemsPresenter> zeigt jedes Element in der an <xref:System.Windows.Controls.ToolBar> ; das <xref:System.Windows.Controls.ScrollViewer> ermöglicht das Scrollen im-Steuerelement).</span><span class="sxs-lookup"><span data-stu-id="ee530-116">(The <xref:System.Windows.Controls.ItemsPresenter> displays each item in the <xref:System.Windows.Controls.ToolBar>; the <xref:System.Windows.Controls.ScrollViewer> enables scrolling within the control).</span></span>  <span data-ttu-id="ee530-117">Wenn das <xref:System.Windows.Controls.ItemsPresenter> nicht das direkt untergeordnete Element von ist <xref:System.Windows.Controls.ScrollViewer> , müssen Sie den <xref:System.Windows.Controls.ItemsPresenter> Namen, `ItemsPresenter` .</span><span class="sxs-lookup"><span data-stu-id="ee530-117">If the <xref:System.Windows.Controls.ItemsPresenter> is not the direct child of the <xref:System.Windows.Controls.ScrollViewer>, you must give the <xref:System.Windows.Controls.ItemsPresenter> the name, `ItemsPresenter`.</span></span>  
  
## <a name="toolbar-states"></a><span data-ttu-id="ee530-118">Symbolleisten Zustände</span><span class="sxs-lookup"><span data-stu-id="ee530-118">ToolBar States</span></span>  
 <span data-ttu-id="ee530-119">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.ToolBar> .</span><span class="sxs-lookup"><span data-stu-id="ee530-119">The following table lists the visual states for the <xref:System.Windows.Controls.ToolBar> control.</span></span>  
  
|<span data-ttu-id="ee530-120">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="ee530-120">VisualState Name</span></span>|<span data-ttu-id="ee530-121">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="ee530-121">VisualStateGroup Name</span></span>|<span data-ttu-id="ee530-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee530-122">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="ee530-123">Gültig</span><span class="sxs-lookup"><span data-stu-id="ee530-123">Valid</span></span>|<span data-ttu-id="ee530-124">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="ee530-124">ValidationStates</span></span>|<span data-ttu-id="ee530-125">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="ee530-125">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="ee530-126">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="ee530-126">InvalidFocused</span></span>|<span data-ttu-id="ee530-127">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="ee530-127">ValidationStates</span></span>|<span data-ttu-id="ee530-128">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="ee530-128">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="ee530-129">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="ee530-129">InvalidUnfocused</span></span>|<span data-ttu-id="ee530-130">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="ee530-130">ValidationStates</span></span>|<span data-ttu-id="ee530-131">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="ee530-131">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="toolbar-controltemplate-example"></a><span data-ttu-id="ee530-132">Symbolleisten-ControlTemplate-Beispiel</span><span class="sxs-lookup"><span data-stu-id="ee530-132">ToolBar ControlTemplate Example</span></span>  
 <span data-ttu-id="ee530-133">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.ToolBar> .</span><span class="sxs-lookup"><span data-stu-id="ee530-133">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.ToolBar> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ToolBar](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/toolbar.xaml#toolbar)]  
  
 <span data-ttu-id="ee530-134">Im vorhergehenden Beispiel wird mindestens eine der folgenden Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ee530-134">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="ee530-135">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="ee530-135">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ee530-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee530-136">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="ee530-137">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="ee530-137">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="ee530-138">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="ee530-138">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="ee530-139">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="ee530-139">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="ee530-140">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ee530-140">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
