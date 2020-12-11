---
title: 'Gewusst wie: Anwenden eines FocusVisualStyle auf ein Steuerelement'
ms.date: 03/30/2017
helpviewer_keywords:
- properties [WPF], FocusVisualStyle
- FocusVisualStyle property [WPF]
ms.assetid: 363de99e-8ecc-438c-ac4a-f9147432ebd6
ms.openlocfilehash: c27994bfbc77f7cbe360ad3aab94827900e52232
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976390"
---
# <a name="how-to-apply-a-focusvisualstyle-to-a-control"></a><span data-ttu-id="38388-102">Gewusst wie: Anwenden eines FocusVisualStyle auf ein Steuerelement</span><span class="sxs-lookup"><span data-stu-id="38388-102">How to: Apply a FocusVisualStyle to a Control</span></span>
<span data-ttu-id="38388-103">In diesem Beispiel wird gezeigt, wie Sie einen visuellen Fokus Stil in Ressourcen erstellen und den Stil mithilfe der-Eigenschaft auf ein Steuerelement anwenden <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> .</span><span class="sxs-lookup"><span data-stu-id="38388-103">This example shows you how to create a focus visual style in resources and apply the style to a control, using the <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> property.</span></span>  
  
## <a name="example"></a><span data-ttu-id="38388-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="38388-104">Example</span></span>  
 <span data-ttu-id="38388-105">Im folgenden Beispiel wird ein Stil definiert, mit dem zusätzliche Steuerelement Zusammensetzung erstellt werden, die nur angewendet wird, wenn sich das Steuerelement im Fokus befindet [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="38388-105">The following example defines a style that creates additional control compositing that only applies when that control is keyboard focused in the [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)].</span></span> <span data-ttu-id="38388-106">Dies wird erreicht, indem ein Stil mit einem definiert <xref:System.Windows.Controls.ControlTemplate> und dann beim Festlegen der-Eigenschaft auf diesen Stil als Ressource verwiesen wird <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> .</span><span class="sxs-lookup"><span data-stu-id="38388-106">This is accomplished by defining a style with a <xref:System.Windows.Controls.ControlTemplate>, then referencing that style as a resource when setting the <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> property.</span></span>  
  
 <span data-ttu-id="38388-107">Ein externes Rechteck, das einem Rahmen ähnelt, wird außerhalb des rechteckigen Bereichs platziert.</span><span class="sxs-lookup"><span data-stu-id="38388-107">An external rectangle resembling a border is placed outside of the rectangular area.</span></span> <span data-ttu-id="38388-108">Sofern nicht anders geändert, verwendet die Größe des Stils den <xref:System.Windows.FrameworkElement.ActualHeight%2A> und <xref:System.Windows.FrameworkElement.ActualWidth%2A> des rechteckigen Steuer Elements, bei dem der visuelle Fokus Stil angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="38388-108">Unless otherwise modified, the sizing of the style uses the <xref:System.Windows.FrameworkElement.ActualHeight%2A> and <xref:System.Windows.FrameworkElement.ActualWidth%2A> of the rectangular control where the focus visual style is applied.</span></span> <span data-ttu-id="38388-109">In diesem Beispiel werden negative Werte für das festgelegt <xref:System.Windows.FrameworkElement.Margin%2A> , damit der Rahmen etwas außerhalb des Steuer Elements angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="38388-109">This example sets negative values for the <xref:System.Windows.FrameworkElement.Margin%2A> to make the border appear slightly outside the focused control.</span></span>  
  
 [!code-xaml[FEFocusVisualStyle#XAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FEFocusVisualStyle/CS/page1.xaml#xaml)]  
  
 <span data-ttu-id="38388-110">Ein <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> ist ein Additiv zu einem Steuerelement Vorlagen Stil, der entweder von einem expliziten Stil oder einem Design Stil stammt. der primäre Stil für ein Steuerelement kann weiterhin mithilfe von erstellt werden, <xref:System.Windows.Controls.ControlTemplate> und dieser Stil wird auf die-Eigenschaft festgelegt <xref:System.Windows.FrameworkElement.Style%2A> .</span><span class="sxs-lookup"><span data-stu-id="38388-110">A <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> is additive to any control template style that comes either from an explicit style or a theme style; the primary style for a control can still be created by using a <xref:System.Windows.Controls.ControlTemplate> and setting that style to the <xref:System.Windows.FrameworkElement.Style%2A> property.</span></span>  
  
 <span data-ttu-id="38388-111">Visuelle Fokus Stile sollten konsistent für ein Design oder eine Benutzeroberfläche verwendet werden, anstatt für jedes Fokussier Bare Element einen anderen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="38388-111">Focus visual styles should be used consistently across a theme or a UI, rather than using a different one for each focusable element.</span></span> <span data-ttu-id="38388-112">Weitere Informationen finden Sie unter Formatieren [für den Fokus in Steuerelementen und Focus VisualStyle](styling-for-focus-in-controls-and-focusvisualstyle.md).</span><span class="sxs-lookup"><span data-stu-id="38388-112">For details, see [Styling for Focus in Controls, and FocusVisualStyle](styling-for-focus-in-controls-and-focusvisualstyle.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="38388-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38388-113">See also</span></span>

- <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A>
- [<span data-ttu-id="38388-114">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="38388-114">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [<span data-ttu-id="38388-115">Fokusstile in Steuerelementen und FocusVisualStyle</span><span class="sxs-lookup"><span data-stu-id="38388-115">Styling for Focus in Controls, and FocusVisualStyle</span></span>](styling-for-focus-in-controls-and-focusvisualstyle.md)
