---
title: DocumentViewer-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- templates [WPF], DocumentViewer
- DocumentViewer [WPF], styles and templates
- states [WPF], DocumentViewer
- ControlTemplate [WPF], DocumentViewer
- parts [WPF], DocumentViewer
- styles [WPF], DocumentViewer
ms.assetid: 6bd4ff8f-ea6a-4084-ac58-e7a67446ce1c
ms.openlocfilehash: 8a5d000dd67c1f5699c411db6ad1d7244ef0ad03
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977783"
---
# <a name="documentviewer-styles-and-templates"></a><span data-ttu-id="4eb14-102">DocumentViewer-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="4eb14-102">DocumentViewer Styles and Templates</span></span>
<span data-ttu-id="4eb14-103">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.DocumentViewer> .</span><span class="sxs-lookup"><span data-stu-id="4eb14-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.DocumentViewer> control.</span></span> <span data-ttu-id="4eb14-104">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="4eb14-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="4eb14-105">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="4eb14-105">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>  
  
## <a name="documentviewer-parts"></a><span data-ttu-id="4eb14-106">DocumentViewer-Teile</span><span class="sxs-lookup"><span data-stu-id="4eb14-106">DocumentViewer Parts</span></span>  
 <span data-ttu-id="4eb14-107">In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.DocumentViewer> .</span><span class="sxs-lookup"><span data-stu-id="4eb14-107">The following table lists the named parts for the <xref:System.Windows.Controls.DocumentViewer> control.</span></span>  
  
|<span data-ttu-id="4eb14-108">Teil</span><span class="sxs-lookup"><span data-stu-id="4eb14-108">Part</span></span>|<span data-ttu-id="4eb14-109">type</span><span class="sxs-lookup"><span data-stu-id="4eb14-109">Type</span></span>|<span data-ttu-id="4eb14-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4eb14-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="4eb14-111">PART_ContentHost</span><span class="sxs-lookup"><span data-stu-id="4eb14-111">PART_ContentHost</span></span>|<xref:System.Windows.Controls.ScrollViewer>|<span data-ttu-id="4eb14-112">Der Inhalt und der scrollbereich.</span><span class="sxs-lookup"><span data-stu-id="4eb14-112">The content and scrolling area.</span></span>|  
|<span data-ttu-id="4eb14-113">PART_FindToolBarHost</span><span class="sxs-lookup"><span data-stu-id="4eb14-113">PART_FindToolBarHost</span></span>|<xref:System.Windows.Controls.ContentControl>|<span data-ttu-id="4eb14-114">Das Suchfeld, das standardmäßig unten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4eb14-114">The search box, at the bottom by default.</span></span>|  
  
## <a name="documentviewer-states"></a><span data-ttu-id="4eb14-115">DocumentViewer-Zustände</span><span class="sxs-lookup"><span data-stu-id="4eb14-115">DocumentViewer States</span></span>  
 <span data-ttu-id="4eb14-116">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.DocumentViewer> .</span><span class="sxs-lookup"><span data-stu-id="4eb14-116">The following table lists the visual states for the <xref:System.Windows.Controls.DocumentViewer> control.</span></span>  
  
|<span data-ttu-id="4eb14-117">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="4eb14-117">VisualState Name</span></span>|<span data-ttu-id="4eb14-118">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="4eb14-118">VisualStateGroup Name</span></span>|<span data-ttu-id="4eb14-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4eb14-119">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="4eb14-120">Gültig</span><span class="sxs-lookup"><span data-stu-id="4eb14-120">Valid</span></span>|<span data-ttu-id="4eb14-121">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="4eb14-121">ValidationStates</span></span>|<span data-ttu-id="4eb14-122">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="4eb14-122">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="4eb14-123">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="4eb14-123">InvalidFocused</span></span>|<span data-ttu-id="4eb14-124">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="4eb14-124">ValidationStates</span></span>|<span data-ttu-id="4eb14-125">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="4eb14-125">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="4eb14-126">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="4eb14-126">InvalidUnfocused</span></span>|<span data-ttu-id="4eb14-127">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="4eb14-127">ValidationStates</span></span>|<span data-ttu-id="4eb14-128">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="4eb14-128">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="documentviewer-controltemplate-example"></a><span data-ttu-id="4eb14-129">DocumentViewer ControlTemplate-Beispiel</span><span class="sxs-lookup"><span data-stu-id="4eb14-129">DocumentViewer ControlTemplate Example</span></span>  
 <span data-ttu-id="4eb14-130">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.DocumentViewer> .</span><span class="sxs-lookup"><span data-stu-id="4eb14-130">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.DocumentViewer> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#DocumentViewer](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/documentviewer.xaml#documentviewer)]  
  
 <span data-ttu-id="4eb14-131">Im vorhergehenden Beispiel wird mindestens eine der folgenden Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="4eb14-131">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="4eb14-132">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="4eb14-132">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4eb14-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4eb14-133">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="4eb14-134">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="4eb14-134">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="4eb14-135">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="4eb14-135">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="4eb14-136">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="4eb14-136">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="4eb14-137">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="4eb14-137">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
