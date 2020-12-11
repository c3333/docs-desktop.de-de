---
title: Window-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], Window
- templates [WPF], Window
- styles [WPF], Window
- ControlTemplate [WPF], Window
- Window [WPF], styles and templates
- states [WPF], Window
ms.assetid: 2dfdf025-347b-4342-bf28-95206c273f35
ms.openlocfilehash: ed488cf2fb5f4e73da544f8d758950fee318adf1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978018"
---
# <a name="window-styles-and-templates"></a><span data-ttu-id="47fd0-102">Window-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="47fd0-102">Window Styles and Templates</span></span>
<span data-ttu-id="47fd0-103">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Window> .</span><span class="sxs-lookup"><span data-stu-id="47fd0-103">This topic describes the styles and templates for the <xref:System.Windows.Window> control.</span></span> <span data-ttu-id="47fd0-104">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="47fd0-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="47fd0-105">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="47fd0-105">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>  
  
## <a name="window-parts"></a><span data-ttu-id="47fd0-106">Fensterteile</span><span class="sxs-lookup"><span data-stu-id="47fd0-106">Window Parts</span></span>  
 <span data-ttu-id="47fd0-107">Das- <xref:System.Windows.Window> Steuerelement verfügt über keine benannten Teile.</span><span class="sxs-lookup"><span data-stu-id="47fd0-107">The <xref:System.Windows.Window> control does not have any named parts.</span></span>  
  
## <a name="window-states"></a><span data-ttu-id="47fd0-108">Fenster Zustände</span><span class="sxs-lookup"><span data-stu-id="47fd0-108">Window States</span></span>  
 <span data-ttu-id="47fd0-109">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Window> .</span><span class="sxs-lookup"><span data-stu-id="47fd0-109">The following table lists the visual states for the <xref:System.Windows.Window> control.</span></span>  
  
|<span data-ttu-id="47fd0-110">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="47fd0-110">VisualState Name</span></span>|<span data-ttu-id="47fd0-111">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="47fd0-111">VisualStateGroup Name</span></span>|<span data-ttu-id="47fd0-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47fd0-112">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="47fd0-113">Gültig</span><span class="sxs-lookup"><span data-stu-id="47fd0-113">Valid</span></span>|<span data-ttu-id="47fd0-114">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="47fd0-114">ValidationStates</span></span>|<span data-ttu-id="47fd0-115">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="47fd0-115">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="47fd0-116">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="47fd0-116">InvalidFocused</span></span>|<span data-ttu-id="47fd0-117">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="47fd0-117">ValidationStates</span></span>|<span data-ttu-id="47fd0-118">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="47fd0-118">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="47fd0-119">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="47fd0-119">InvalidUnfocused</span></span>|<span data-ttu-id="47fd0-120">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="47fd0-120">ValidationStates</span></span>|<span data-ttu-id="47fd0-121">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="47fd0-121">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="window-controltemplate-example"></a><span data-ttu-id="47fd0-122">Fenster ControlTemplate-Beispiel</span><span class="sxs-lookup"><span data-stu-id="47fd0-122">Window ControlTemplate Example</span></span>  
 <span data-ttu-id="47fd0-123">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Window> .</span><span class="sxs-lookup"><span data-stu-id="47fd0-123">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Window> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Window](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/window.xaml#window)]  
  
 <span data-ttu-id="47fd0-124"><xref:System.Windows.Controls.ControlTemplate>Verwendet mindestens eine der folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="47fd0-124">The <xref:System.Windows.Controls.ControlTemplate> uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ResizeGrip](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/resizegrip.xaml#resizegrip)]  
[!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="47fd0-125">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="47fd0-125">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="47fd0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47fd0-126">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="47fd0-127">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="47fd0-127">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="47fd0-128">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="47fd0-128">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="47fd0-129">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="47fd0-129">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="47fd0-130">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="47fd0-130">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
