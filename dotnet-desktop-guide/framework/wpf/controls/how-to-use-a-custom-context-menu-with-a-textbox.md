---
title: 'Gewusst wie: Verwenden eines benutzerdefinierten Kontextmenüs mit "TextBox"'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- context menus [WPF], custom
- menus [WPF], custom
- custom context menus [WPF]
- TextBox control [WPF], custom content menus
ms.assetid: 842d3cd5-6fa0-4be4-8d90-6c7466213b1c
ms.openlocfilehash: 93ee6d44e9e5703d70d0583b759330a9e52f60b9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976625"
---
# <a name="how-to-use-a-custom-context-menu-with-a-textbox"></a><span data-ttu-id="b9fa9-102">Gewusst wie: Verwenden eines benutzerdefinierten Kontextmenüs mit "TextBox"</span><span class="sxs-lookup"><span data-stu-id="b9fa9-102">How to: Use a Custom Context Menu with a TextBox</span></span>
<span data-ttu-id="b9fa9-103">In diesem Beispiel wird gezeigt, wie ein einfaches benutzerdefiniertes Kontextmenü für ein definiert und implementiert wird <xref:System.Windows.Controls.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="b9fa9-103">This example shows how to define and implement a simple custom context menu for a <xref:System.Windows.Controls.TextBox>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b9fa9-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b9fa9-104">Example</span></span>  
 <span data-ttu-id="b9fa9-105">Im folgenden [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beispiel wird ein-Steuerelement definiert <xref:System.Windows.Controls.TextBox> , das ein benutzerdefiniertes Kontextmenü enthält.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-105">The following [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] example defines a <xref:System.Windows.Controls.TextBox> control that includes a custom context menu.</span></span>  
  
 <span data-ttu-id="b9fa9-106">Das Kontextmenü wird mithilfe eines- <xref:System.Windows.Controls.ContextMenu> Elements definiert.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-106">The context menu is defined using a <xref:System.Windows.Controls.ContextMenu> element.</span></span>  <span data-ttu-id="b9fa9-107">Das Kontextmenü selbst besteht aus einer Reihe von <xref:System.Windows.Controls.MenuItem> Elementen und <xref:System.Windows.Controls.Separator> Elementen.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-107">The context menu itself consists of a series of <xref:System.Windows.Controls.MenuItem> elements and <xref:System.Windows.Controls.Separator> elements.</span></span>  <span data-ttu-id="b9fa9-108">Jedes- <xref:System.Windows.Controls.MenuItem> Element definiert einen Befehl im Kontextmenü. das <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> -Attribut definiert den Anzeige Text für den Menübefehl, und das- <xref:System.Windows.Controls.MenuItem.Click> Attribut gibt eine Handlermethode für jedes Menü Element an.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-108">Each <xref:System.Windows.Controls.MenuItem> element defines a command in the context menu; the <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> attribute defines the display text for the menu command, and the <xref:System.Windows.Controls.MenuItem.Click> attribute specifies a handler method for each menu item.</span></span>  <span data-ttu-id="b9fa9-109">Das <xref:System.Windows.Controls.Separator> -Element bewirkt lediglich, dass eine Trennlinie zwischen den vorherigen und nachfolgenden Menü Elementen gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-109">The <xref:System.Windows.Controls.Separator> element simply causes a separating line to be rendered between the previous and subsequent menu items.</span></span>  
  
 [!code-xaml[TextBox_ContextMenu#_TextBox_ContextMenuXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_ContextMenu/CSharp/Window1.xaml#_textbox_contextmenuxaml)]  
  
## <a name="example"></a><span data-ttu-id="b9fa9-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b9fa9-110">Example</span></span>  
 <span data-ttu-id="b9fa9-111">Das folgende Beispiel zeigt den Implementierungs Code für die vorherige Kontextmenü Definition sowie den Code, der das Kontextmenü aktiviert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-111">The following example shows the implementation code for the preceding context menu definition, as well as the code that enables and disables the context menu.</span></span>  <span data-ttu-id="b9fa9-112">Das- <xref:System.Windows.Controls.ContextMenu.Opened> Ereignis wird verwendet, um bestimmte Befehle basierend auf dem aktuellen Zustand von dynamisch zu aktivieren oder zu deaktivieren <xref:System.Windows.Controls.TextBox> .</span><span class="sxs-lookup"><span data-stu-id="b9fa9-112">The <xref:System.Windows.Controls.ContextMenu.Opened> event is used to dynamically enable or disable certain commands depending on the current state of the <xref:System.Windows.Controls.TextBox>.</span></span>  
  
 <span data-ttu-id="b9fa9-113">Um das Standardkontext Menü wiederherzustellen, verwenden <xref:System.Windows.DependencyObject.ClearValue%2A> Sie die-Methode, um den Wert der-Eigenschaft zu löschen <xref:System.Windows.FrameworkElement.ContextMenu%2A> .</span><span class="sxs-lookup"><span data-stu-id="b9fa9-113">To restore the default context menu, use the <xref:System.Windows.DependencyObject.ClearValue%2A> method to clear the value of the <xref:System.Windows.FrameworkElement.ContextMenu%2A> property.</span></span>  <span data-ttu-id="b9fa9-114">Um das Kontextmenü vollständig zu deaktivieren, legen Sie die- <xref:System.Windows.FrameworkElement.ContextMenu%2A> Eigenschaft auf einen NULL-Verweis ( `Nothing` in Visual Basic) fest.</span><span class="sxs-lookup"><span data-stu-id="b9fa9-114">To disable the context menu altogether, set the <xref:System.Windows.FrameworkElement.ContextMenu%2A> property to a null reference (`Nothing` in Visual Basic).</span></span>  
  
 [!code-csharp[TextBox_ContextMenu#_TextBox_ContextMenu](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_ContextMenu/CSharp/Window1.xaml.cs#_textbox_contextmenu)]
 [!code-vb[TextBox_ContextMenu#_TextBox_ContextMenu](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_ContextMenu/VisualBasic/Window1.xaml.vb#_textbox_contextmenu)]  
  
## <a name="see-also"></a><span data-ttu-id="b9fa9-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9fa9-115">See also</span></span>

- [<span data-ttu-id="b9fa9-116">Verwenden der Rechtschreibprüfung mit einem Kontextmenü</span><span class="sxs-lookup"><span data-stu-id="b9fa9-116">Use Spell Checking with a Context Menu</span></span>](how-to-use-spell-checking-with-a-context-menu.md)
- [<span data-ttu-id="b9fa9-117">Übersicht über TextBox</span><span class="sxs-lookup"><span data-stu-id="b9fa9-117">TextBox Overview</span></span>](textbox-overview.md)
- [<span data-ttu-id="b9fa9-118">Übersicht über RichTextBox</span><span class="sxs-lookup"><span data-stu-id="b9fa9-118">RichTextBox Overview</span></span>](richtextbox-overview.md)
