---
title: ProgressBar-Formate und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], ProgressBar
- ProgressBar [WPF], styles and templates
- styles [WPF], ProgressBar
- ControlTemplate [WPF], ProgressBar
- templates [WPF], ProgressBar
- states [WPF], ProgressBar
ms.assetid: 935aa600-16e6-4947-a905-37a189a583dd
ms.openlocfilehash: 781c185e01621767a82ebee054c578ed291c9b79
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977027"
---
# <a name="progressbar-styles-and-templates"></a><span data-ttu-id="83b81-102">ProgressBar-Formate und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="83b81-102">ProgressBar Styles and Templates</span></span>
<span data-ttu-id="83b81-103">In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.ProgressBar> .</span><span class="sxs-lookup"><span data-stu-id="83b81-103">This topic describes the styles and templates for the <xref:System.Windows.Controls.ProgressBar> control.</span></span> <span data-ttu-id="83b81-104">Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen.</span><span class="sxs-lookup"><span data-stu-id="83b81-104">You can modify the default <xref:System.Windows.Controls.ControlTemplate> to give the control a unique appearance.</span></span> <span data-ttu-id="83b81-105">Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.</span><span class="sxs-lookup"><span data-stu-id="83b81-105">For more information, see [Create a template for a control](/dotnet/desktop-wpf/themes/how-to-create-apply-template).</span></span>  
  
## <a name="progressbar-parts"></a><span data-ttu-id="83b81-106">ProgressBar-Teile</span><span class="sxs-lookup"><span data-stu-id="83b81-106">ProgressBar Parts</span></span>  
 <span data-ttu-id="83b81-107">In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.ProgressBar> .</span><span class="sxs-lookup"><span data-stu-id="83b81-107">The following table lists the named parts for the <xref:System.Windows.Controls.ProgressBar> control.</span></span>  
  
|<span data-ttu-id="83b81-108">Teil</span><span class="sxs-lookup"><span data-stu-id="83b81-108">Part</span></span>|<span data-ttu-id="83b81-109">type</span><span class="sxs-lookup"><span data-stu-id="83b81-109">Type</span></span>|<span data-ttu-id="83b81-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83b81-110">Description</span></span>|  
|-|-|-|  
|<span data-ttu-id="83b81-111">PART_Indicator</span><span class="sxs-lookup"><span data-stu-id="83b81-111">PART_Indicator</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="83b81-112">Das Objekt, das den Fortschritt angibt.</span><span class="sxs-lookup"><span data-stu-id="83b81-112">The object that indicates progress.</span></span>|  
|<span data-ttu-id="83b81-113">PART_Track</span><span class="sxs-lookup"><span data-stu-id="83b81-113">PART_Track</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="83b81-114">Das-Objekt, das den Pfad der Statusanzeige definiert.</span><span class="sxs-lookup"><span data-stu-id="83b81-114">The object that defines the path of the progress indicator.</span></span>|  
|<span data-ttu-id="83b81-115">PART_GlowRect</span><span class="sxs-lookup"><span data-stu-id="83b81-115">PART_GlowRect</span></span>|<xref:System.Windows.FrameworkElement>|<span data-ttu-id="83b81-116">Ein-Objekt, das die Statusanzeige verschönert.</span><span class="sxs-lookup"><span data-stu-id="83b81-116">An object that embellishes the progress bar.</span></span>|  
  
## <a name="progressbar-states"></a><span data-ttu-id="83b81-117">ProgressBar-Zustände</span><span class="sxs-lookup"><span data-stu-id="83b81-117">ProgressBar States</span></span>  
 <span data-ttu-id="83b81-118">In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.ProgressBar> .</span><span class="sxs-lookup"><span data-stu-id="83b81-118">The following table lists the visual states for the <xref:System.Windows.Controls.ProgressBar> control.</span></span>  
  
|<span data-ttu-id="83b81-119">VisualState-Name</span><span class="sxs-lookup"><span data-stu-id="83b81-119">VisualState Name</span></span>|<span data-ttu-id="83b81-120">VisualStateGroup-Name</span><span class="sxs-lookup"><span data-stu-id="83b81-120">VisualStateGroup Name</span></span>|<span data-ttu-id="83b81-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="83b81-121">Description</span></span>|  
|----------------------|---------------------------|-----------------|  
|<span data-ttu-id="83b81-122">Bestimmte</span><span class="sxs-lookup"><span data-stu-id="83b81-122">Determinate</span></span>|<span data-ttu-id="83b81-123">CommonStates</span><span class="sxs-lookup"><span data-stu-id="83b81-123">CommonStates</span></span>|<span data-ttu-id="83b81-124"><xref:System.Windows.Controls.ProgressBar> meldet den Fortschritt basierend auf der- <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="83b81-124"><xref:System.Windows.Controls.ProgressBar> reports progress based on the <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> property.</span></span>|  
|<span data-ttu-id="83b81-125">Unbestimmten</span><span class="sxs-lookup"><span data-stu-id="83b81-125">Indeterminate</span></span>|<span data-ttu-id="83b81-126">CommonStates</span><span class="sxs-lookup"><span data-stu-id="83b81-126">CommonStates</span></span>|<span data-ttu-id="83b81-127"><xref:System.Windows.Controls.ProgressBar> meldet den generischen Fortschritt mit einem Wiederholungsmuster.</span><span class="sxs-lookup"><span data-stu-id="83b81-127"><xref:System.Windows.Controls.ProgressBar> reports generic progress with a repeating pattern.</span></span>|  
|<span data-ttu-id="83b81-128">Gültig</span><span class="sxs-lookup"><span data-stu-id="83b81-128">Valid</span></span>|<span data-ttu-id="83b81-129">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="83b81-129">ValidationStates</span></span>|<span data-ttu-id="83b81-130">Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .</span><span class="sxs-lookup"><span data-stu-id="83b81-130">The control uses the <xref:System.Windows.Controls.Validation> class and the <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `false`.</span></span>|  
|<span data-ttu-id="83b81-131">InvalidFocused</span><span class="sxs-lookup"><span data-stu-id="83b81-131">InvalidFocused</span></span>|<span data-ttu-id="83b81-132">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="83b81-132">ValidationStates</span></span>|<span data-ttu-id="83b81-133">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="83b81-133">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control has focus.</span></span>|  
|<span data-ttu-id="83b81-134">InvalidUnfocused</span><span class="sxs-lookup"><span data-stu-id="83b81-134">InvalidUnfocused</span></span>|<span data-ttu-id="83b81-135">ValidationStates</span><span class="sxs-lookup"><span data-stu-id="83b81-135">ValidationStates</span></span>|<span data-ttu-id="83b81-136">Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.</span><span class="sxs-lookup"><span data-stu-id="83b81-136">The <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> attached property is `true` has the control does not have focus.</span></span>|  
  
## <a name="progressbar-controltemplate-example"></a><span data-ttu-id="83b81-137">ProgressBar ControlTemplate-Beispiel</span><span class="sxs-lookup"><span data-stu-id="83b81-137">ProgressBar ControlTemplate Example</span></span>  
 <span data-ttu-id="83b81-138">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.ProgressBar> .</span><span class="sxs-lookup"><span data-stu-id="83b81-138">The following example shows how to define a <xref:System.Windows.Controls.ControlTemplate> for the <xref:System.Windows.Controls.ProgressBar> control.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#ProgressBar](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/progressbar.xaml#progressbar)]  
  
 <span data-ttu-id="83b81-139">Im vorhergehenden Beispiel wird mindestens eine der folgenden Ressourcen verwendet.</span><span class="sxs-lookup"><span data-stu-id="83b81-139">The preceding example uses one or more of the following resources.</span></span>  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 <span data-ttu-id="83b81-140">Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span><span class="sxs-lookup"><span data-stu-id="83b81-140">For the complete sample, see [Styling with ControlTemplates Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="83b81-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83b81-141">See also</span></span>

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [<span data-ttu-id="83b81-142">Steuerelementformate und -vorlagen</span><span class="sxs-lookup"><span data-stu-id="83b81-142">Control Styles and Templates</span></span>](control-styles-and-templates.md)
- [<span data-ttu-id="83b81-143">Anpassung von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="83b81-143">Control Customization</span></span>](control-customization.md)
- [<span data-ttu-id="83b81-144">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="83b81-144">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="83b81-145">Erstellen einer Vorlage für ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="83b81-145">Create a template for a control</span></span>](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
