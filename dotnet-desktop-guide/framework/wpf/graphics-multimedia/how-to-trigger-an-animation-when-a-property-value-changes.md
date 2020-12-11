---
title: 'Gewusst wie: Auslösen einer Animation bei Änderung eines Eigenschaftswerts'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], starting when property values change
- triggering animation [WPF]
- Storyboards [WPF], starting when property values change
ms.assetid: 12399c21-0300-4f4f-9e3a-d92d9907e5f5
ms.openlocfilehash: 7e3eecedf7d464eeb8e4f60f2f05fa06d2e23e09
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977604"
---
# <a name="how-to-trigger-an-animation-when-a-property-value-changes"></a><span data-ttu-id="fd2c3-102">Gewusst wie: Auslösen einer Animation bei Änderung eines Eigenschaftswerts</span><span class="sxs-lookup"><span data-stu-id="fd2c3-102">How to: Trigger an Animation When a Property Value Changes</span></span>
<span data-ttu-id="fd2c3-103">Dieses Beispiel zeigt, wie ein verwendet wird <xref:System.Windows.Trigger> , um eine zu starten, <xref:System.Windows.Media.Animation.Storyboard> Wenn sich ein Eigenschafts Wert ändert.</span><span class="sxs-lookup"><span data-stu-id="fd2c3-103">This example shows how to use a <xref:System.Windows.Trigger> to start a <xref:System.Windows.Media.Animation.Storyboard> when a property value changes.</span></span> <span data-ttu-id="fd2c3-104">Sie können eine <xref:System.Windows.Trigger> innerhalb von <xref:System.Windows.Style> , oder verwenden <xref:System.Windows.Controls.ControlTemplate> <xref:System.Windows.DataTemplate> .</span><span class="sxs-lookup"><span data-stu-id="fd2c3-104">You can use a <xref:System.Windows.Trigger> inside a <xref:System.Windows.Style>, <xref:System.Windows.Controls.ControlTemplate>, or <xref:System.Windows.DataTemplate>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="fd2c3-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fd2c3-105">Example</span></span>  
 <span data-ttu-id="fd2c3-106">Im folgenden Beispiel wird ein- <xref:System.Windows.Trigger> Objekt verwendet, um den eines zu animieren, <xref:System.Windows.UIElement.Opacity%2A> <xref:System.Windows.Controls.Button> wenn seine- <xref:System.Windows.UIElement.IsMouseOver%2A> Eigenschaft zu wird `true` .</span><span class="sxs-lookup"><span data-stu-id="fd2c3-106">The following example uses a <xref:System.Windows.Trigger> to animate the <xref:System.Windows.UIElement.Opacity%2A> of a <xref:System.Windows.Controls.Button> when its <xref:System.Windows.UIElement.IsMouseOver%2A> property becomes `true`.</span></span>  
  
 [!code-xaml[AnimatePropertyStoryboards#PropertyTriggerExample](~/samples/snippets/xaml/VS_Snippets_Wpf/AnimatePropertyStoryboards/XAML/PropertyTriggerExample.xaml#propertytriggerexample)]  
  
 <span data-ttu-id="fd2c3-107">Durch Eigenschafts Objekte angewendete Animationen <xref:System.Windows.Trigger> Verhalten sich komplexer als <xref:System.Windows.EventTrigger> Animationen oder Animationen, die mithilfe von Methoden gestartet wurden <xref:System.Windows.Media.Animation.Storyboard> .</span><span class="sxs-lookup"><span data-stu-id="fd2c3-107">Animations applied by property <xref:System.Windows.Trigger> objects behave in a more complex fashion than <xref:System.Windows.EventTrigger> animations or animations started using <xref:System.Windows.Media.Animation.Storyboard> methods.</span></span>  <span data-ttu-id="fd2c3-108">Sie "Handoff" mit Animationen, die von anderen <xref:System.Windows.Trigger> Objekten definiert werden, verfassen jedoch mit <xref:System.Windows.EventTrigger> und durch Methoden ausgelöste Animationen.</span><span class="sxs-lookup"><span data-stu-id="fd2c3-108">They "handoff" with animations defined by other <xref:System.Windows.Trigger> objects, but compose with <xref:System.Windows.EventTrigger> and method-triggered animations.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="fd2c3-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd2c3-109">See also</span></span>

- <xref:System.Windows.Trigger>
- [<span data-ttu-id="fd2c3-110">Übersicht über die Verfahren zur Animation von Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fd2c3-110">Property Animation Techniques Overview</span></span>](property-animation-techniques-overview.md)
- [<span data-ttu-id="fd2c3-111">Übersicht über Storyboards</span><span class="sxs-lookup"><span data-stu-id="fd2c3-111">Storyboards Overview</span></span>](storyboards-overview.md)
