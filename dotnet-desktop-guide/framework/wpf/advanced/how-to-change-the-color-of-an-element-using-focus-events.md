---
title: 'Gewusst wie: Ändern der Farbe eines Elements mithilfe von Fokusereignissen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- focus events [WPF], changing element color for
- colors of elements [WPF], changing
- elements [WPF], changing color of
ms.assetid: 7e246802-3625-47a7-ae9d-c8a2a40fd040
ms.openlocfilehash: c5c0520aa60f1906f2fb3f545c795ba0034a09bd
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976683"
---
# <a name="how-to-change-the-color-of-an-element-using-focus-events"></a><span data-ttu-id="4f262-102">Gewusst wie: Ändern der Farbe eines Elements mithilfe von Fokusereignissen</span><span class="sxs-lookup"><span data-stu-id="4f262-102">How to: Change the Color of an Element Using Focus Events</span></span>
<span data-ttu-id="4f262-103">Dieses Beispiel zeigt, wie Sie die Farbe eines Elements ändern können, wenn es mit dem <xref:System.Windows.UIElement.GotFocus> -Ereignis und dem-Ereignis den Fokus verliert <xref:System.Windows.UIElement.LostFocus> .</span><span class="sxs-lookup"><span data-stu-id="4f262-103">This example shows how to change the color of an element when it gains and loses focus by using the <xref:System.Windows.UIElement.GotFocus> and <xref:System.Windows.UIElement.LostFocus> events.</span></span>  
  
 <span data-ttu-id="4f262-104">Dieses Beispiel besteht aus einer [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Datei und einer Code Behind-Datei.</span><span class="sxs-lookup"><span data-stu-id="4f262-104">This example consists of a [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] file and a code-behind file.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4f262-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4f262-105">Example</span></span>  
 <span data-ttu-id="4f262-106">Der folgende XAML-Code erstellt die Benutzeroberfläche, die aus zwei <xref:System.Windows.Controls.Button> -Objekten besteht, und fügt Ereignishandler für die <xref:System.Windows.UIElement.GotFocus> -und- <xref:System.Windows.UIElement.LostFocus> Ereignisse an die- <xref:System.Windows.Controls.Button> Objekte an.</span><span class="sxs-lookup"><span data-stu-id="4f262-106">The following XAML creates the user interface, which consists of two <xref:System.Windows.Controls.Button> objects, and attaches event handlers for the <xref:System.Windows.UIElement.GotFocus> and <xref:System.Windows.UIElement.LostFocus> events to the <xref:System.Windows.Controls.Button> objects.</span></span>  
  
 [!code-xaml[gotfocusLostfocusEffectUsingEvent#GotLostFocusSampleXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/gotfocusLostfocusEffectUsingEvent/CSharp/Window1.xaml#gotlostfocussamplexaml)]  
  
 <span data-ttu-id="4f262-107">Der folgende Code Behind erstellt die <xref:System.Windows.UIElement.GotFocus> <xref:System.Windows.UIElement.LostFocus> Ereignishandler und.</span><span class="sxs-lookup"><span data-stu-id="4f262-107">The following code behind creates the <xref:System.Windows.UIElement.GotFocus> and <xref:System.Windows.UIElement.LostFocus> event handlers.</span></span>  <span data-ttu-id="4f262-108">Wenn der <xref:System.Windows.Controls.Button> Tastaturfokus erhält, <xref:System.Windows.Controls.Control.Background%2A> wird der von <xref:System.Windows.Controls.Button> in rot geändert.</span><span class="sxs-lookup"><span data-stu-id="4f262-108">When the <xref:System.Windows.Controls.Button> gains keyboard focus, the <xref:System.Windows.Controls.Control.Background%2A> of the <xref:System.Windows.Controls.Button> is changed to red.</span></span>  <span data-ttu-id="4f262-109">Wenn das den <xref:System.Windows.Controls.Button> Tastaturfokus verliert, <xref:System.Windows.Controls.Control.Background%2A> wird der von <xref:System.Windows.Controls.Button> wieder in weiß geändert.</span><span class="sxs-lookup"><span data-stu-id="4f262-109">When the <xref:System.Windows.Controls.Button> loses keyboard focus, the <xref:System.Windows.Controls.Control.Background%2A> of the <xref:System.Windows.Controls.Button> is changed back to white.</span></span>  
  
 [!code-csharp[gotfocusLostfocusEffectUsingEvent#GotLostFocusSampleEventHandlers](~/samples/snippets/csharp/VS_Snippets_Wpf/gotfocusLostfocusEffectUsingEvent/CSharp/Window1.xaml.cs#gotlostfocussampleeventhandlers)]
 [!code-vb[gotfocusLostfocusEffectUsingEvent#GotLostFocusSampleEventHandlers](~/samples/snippets/visualbasic/VS_Snippets_Wpf/gotfocusLostfocusEffectUsingEvent/VisualBasic/Window1.xaml.vb#gotlostfocussampleeventhandlers)]  
  
## <a name="see-also"></a><span data-ttu-id="4f262-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f262-110">See also</span></span>

- [<span data-ttu-id="4f262-111">Übersicht über die Eingabe</span><span class="sxs-lookup"><span data-stu-id="4f262-111">Input Overview</span></span>](input-overview.md)
