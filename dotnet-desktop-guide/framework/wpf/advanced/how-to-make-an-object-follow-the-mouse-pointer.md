---
title: 'Gewusst wie: Konfigurieren eines Objekts zum Folgen des Mauszeigers'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- following the mouse pointer (cursor)
- mouse pointer (cursor), making objects follow
- cursor (mouse pointer), making objects follow
ms.assetid: 50b20415-14bc-405c-baf3-2fb254fffde3
ms.openlocfilehash: f348586341d0fa5b6e1a5fe15ab8c3a75e369e64
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976877"
---
# <a name="how-to-make-an-object-follow-the-mouse-pointer"></a><span data-ttu-id="7fb05-102">Gewusst wie: Konfigurieren eines Objekts zum Folgen des Mauszeigers</span><span class="sxs-lookup"><span data-stu-id="7fb05-102">How to: Make an Object Follow the Mouse Pointer</span></span>
<span data-ttu-id="7fb05-103">In diesem Beispiel wird gezeigt, wie die Dimensionen eines Objekts geändert werden, wenn der Mauszeiger auf dem Bildschirm bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="7fb05-103">This example shows how to change the dimensions of an object when the mouse pointer moves on the screen.</span></span>  
  
 <span data-ttu-id="7fb05-104">Das Beispiel enthält eine [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] -Datei, die die [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] -und eine Code-Behind-Datei erstellt, die den-Ereignishandler erstellt.</span><span class="sxs-lookup"><span data-stu-id="7fb05-104">The example includes an [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] file that creates the [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] and a code-behind file that creates the event handler.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7fb05-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7fb05-105">Example</span></span>  
 <span data-ttu-id="7fb05-106">Mit dem folgenden XAML-Code wird das erstellt [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] , das aus einem <xref:System.Windows.Shapes.Ellipse> in einem besteht <xref:System.Windows.Controls.StackPanel> und den Ereignishandler für das-Ereignis anfügt <xref:System.Windows.UIElement.MouseMove> .</span><span class="sxs-lookup"><span data-stu-id="7fb05-106">The following XAML creates the [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)], which consists of an <xref:System.Windows.Shapes.Ellipse> inside of a <xref:System.Windows.Controls.StackPanel>, and attaches the event handler for the <xref:System.Windows.UIElement.MouseMove> event.</span></span>  
  
 [!code-xaml[mouseMoveWithPointer#MouseMoveWithPointerXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/mouseMoveWithPointer/CSharp/Window1.xaml#mousemovewithpointerxaml)]  
  
 <span data-ttu-id="7fb05-107">Der folgende Code Behind erstellt den- <xref:System.Windows.UIElement.MouseMove> Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="7fb05-107">The following code behind creates the <xref:System.Windows.UIElement.MouseMove> event handler.</span></span>  <span data-ttu-id="7fb05-108">Wenn der Mauszeiger bewegt wird, werden die Höhe und die Breite des <xref:System.Windows.Shapes.Ellipse> erhöht und gesenkt.</span><span class="sxs-lookup"><span data-stu-id="7fb05-108">When the mouse pointer moves, the height and the width of the <xref:System.Windows.Shapes.Ellipse> are increased and decreased.</span></span>  
  
 [!code-csharp[mouseMoveWithPointer#MouseMovePointerGetPosition](~/samples/snippets/csharp/VS_Snippets_Wpf/mouseMoveWithPointer/CSharp/Window1.xaml.cs#mousemovepointergetposition)]
 [!code-vb[mouseMoveWithPointer#MouseMovePointerGetPosition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/mouseMoveWithPointer/VisualBasic/Window1.xaml.vb#mousemovepointergetposition)]  
  
## <a name="see-also"></a><span data-ttu-id="7fb05-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fb05-109">See also</span></span>

- [<span data-ttu-id="7fb05-110">Übersicht über die Eingabe</span><span class="sxs-lookup"><span data-stu-id="7fb05-110">Input Overview</span></span>](input-overview.md)
