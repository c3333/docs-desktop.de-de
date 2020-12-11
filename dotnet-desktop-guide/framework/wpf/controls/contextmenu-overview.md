---
title: Übersicht über ContextMenu
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], ContextMenu
- ContextMenu controls [WPF], about ContextMenu controls
ms.assetid: 16909c42-799a-4561-91e0-7d69dcfeea91
ms.openlocfilehash: c9e63efb37c8847f27ca4b3616f6f1b5323ac3e5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977341"
---
# <a name="contextmenu-overview"></a><span data-ttu-id="91618-102">Übersicht über ContextMenu</span><span class="sxs-lookup"><span data-stu-id="91618-102">ContextMenu Overview</span></span>
<span data-ttu-id="91618-103">Die- <xref:System.Windows.Controls.ContextMenu> Klasse stellt das-Element dar, das Funktionen mithilfe eines kontextspezifischen verfügbar macht <xref:System.Windows.Controls.Menu> .</span><span class="sxs-lookup"><span data-stu-id="91618-103">The <xref:System.Windows.Controls.ContextMenu> class represents the element that exposes functionality by using a context-specific <xref:System.Windows.Controls.Menu>.</span></span> <span data-ttu-id="91618-104">Normalerweise macht ein Benutzer das <xref:System.Windows.Controls.ContextMenu> in der verfügbar, [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] indem er mit der rechten Maustaste auf die Maustaste klickt.</span><span class="sxs-lookup"><span data-stu-id="91618-104">Typically, a user exposes the <xref:System.Windows.Controls.ContextMenu> in the [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] by right-clicking the mouse button.</span></span> <span data-ttu-id="91618-105">In diesem Thema wird das <xref:System.Windows.Controls.ContextMenu> -Element vorgestellt, und es werden Beispiele für die Verwendung in [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] und Code bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="91618-105">This topic introduces the <xref:System.Windows.Controls.ContextMenu> element and provides examples of how to use it in [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] and code.</span></span>  

<a name="contextmenu_control"></a>
## <a name="contextmenu-control"></a><span data-ttu-id="91618-106">ContextMenu-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="91618-106">ContextMenu Control</span></span>  
 <span data-ttu-id="91618-107">Ein <xref:System.Windows.Controls.ContextMenu> wird an ein bestimmtes Steuerelement angefügt.</span><span class="sxs-lookup"><span data-stu-id="91618-107">A <xref:System.Windows.Controls.ContextMenu> is attached to a specific control.</span></span> <span data-ttu-id="91618-108">Mit dem- <xref:System.Windows.Controls.ContextMenu> Element können Sie Benutzern eine Liste von Elementen präsentieren, mit denen Befehle oder Optionen angegeben werden, die einem bestimmten Steuerelement zugeordnet sind, z <xref:System.Windows.Controls.Button> . b. ein.</span><span class="sxs-lookup"><span data-stu-id="91618-108">The <xref:System.Windows.Controls.ContextMenu> element enables you to present users with a list of items that specify commands or options that are associated with a particular control, for example, a <xref:System.Windows.Controls.Button>.</span></span> <span data-ttu-id="91618-109">Das Menü wird mit einem Rechtsklick mit der Maus aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="91618-109">Users right-click the control to make the menu appear.</span></span> <span data-ttu-id="91618-110">Wenn Sie auf einen klicken, wird in der Regel ein <xref:System.Windows.Controls.MenuItem> Untermenü geöffnet, oder eine Anwendung führt einen Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="91618-110">Typically, clicking a <xref:System.Windows.Controls.MenuItem> opens a submenu or causes an application to carry out a command.</span></span>  
  
<a name="creating_contextmenus"></a>
## <a name="creating-contextmenus"></a><span data-ttu-id="91618-111">Erstellen von ContextMenus</span><span class="sxs-lookup"><span data-stu-id="91618-111">Creating ContextMenus</span></span>  
 <span data-ttu-id="91618-112">In den folgenden Beispielen wird veranschaulicht, wie ein <xref:System.Windows.Controls.ContextMenu> mit Untermenüs erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="91618-112">The following examples show how to create a <xref:System.Windows.Controls.ContextMenu> with submenus.</span></span> <span data-ttu-id="91618-113">Die Steuer <xref:System.Windows.Controls.ContextMenu> Elemente werden an Schaltflächen Steuerelemente angefügt.</span><span class="sxs-lookup"><span data-stu-id="91618-113">The <xref:System.Windows.Controls.ContextMenu> controls are attached to button controls.</span></span>  
  
 [!code-xaml[ContextMenu#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenu/CSharp/Pane1.xaml#1)]  
  
 [!code-csharp[ContextMenu#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenu/CSharp/Pane1.xaml.cs#2)]
 [!code-vb[ContextMenu#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ContextMenu/VisualBasic/Pane1.xaml.vb#2)]  
  
<a name="applying_styles_to_contextmenu"></a>
## <a name="applying-styles-to-a-contextmenu"></a><span data-ttu-id="91618-114">Anwenden von Stilen auf ein ContextMenu</span><span class="sxs-lookup"><span data-stu-id="91618-114">Applying Styles to a ContextMenu</span></span>  
 <span data-ttu-id="91618-115">Mithilfe eines-Steuer Elements <xref:System.Windows.Style> können Sie die Darstellung und das Verhalten eines drastisch ändern, <xref:System.Windows.Controls.ContextMenu> ohne ein benutzerdefiniertes Steuerelement schreiben zu müssen.</span><span class="sxs-lookup"><span data-stu-id="91618-115">By using a control <xref:System.Windows.Style>, you can dramatically change the appearance and behavior of a <xref:System.Windows.Controls.ContextMenu> without writing a custom control.</span></span> <span data-ttu-id="91618-116">Zusätzlich zur Festlegung von visuellen Eigenschaften können Sie auch Stile auf Teilelemente eines Steuerelements anwenden.</span><span class="sxs-lookup"><span data-stu-id="91618-116">In addition to setting visual properties, you can also apply styles to parts of a control.</span></span> <span data-ttu-id="91618-117">Beispielsweise können Sie das Verhalten der Teile des Steuer Elements ändern, indem Sie Eigenschaften verwenden, oder Sie können Teile hinzufügen oder das Layout von ändern <xref:System.Windows.Controls.ContextMenu> .</span><span class="sxs-lookup"><span data-stu-id="91618-117">For example, you can change the behavior of parts of the control by using properties, or you can add parts to, or change the layout of, a <xref:System.Windows.Controls.ContextMenu>.</span></span> <span data-ttu-id="91618-118">In den folgenden Beispielen werden verschiedene Möglichkeiten zum Hinzufügen von Stilen zu-Steuer <xref:System.Windows.Controls.ContextMenu> Elementen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="91618-118">The following examples show several ways to add styles to <xref:System.Windows.Controls.ContextMenu> controls.</span></span>  
  
 <span data-ttu-id="91618-119">Im ersten Beispiel wird ein Stil mit der Bezeichnung `SimpleSysResources` definiert. An diesem Beispiel können Sie sehen, wie die aktuellen Systemeinstellungen in Ihrem Stil verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="91618-119">The first example defines a style called `SimpleSysResources`, which shows how to use the current system settings in your style.</span></span> <span data-ttu-id="91618-120">Im Beispiel wird <xref:System.Windows.SystemColors.MenuHighlightBrushKey%2A> als <xref:System.Windows.Controls.Control.Background%2A> Farbe und <xref:System.Windows.SystemColors.MenuTextBrushKey%2A> als <xref:System.Windows.Controls.Control.Foreground%2A> Farbe des zugewiesen <xref:System.Windows.Controls.ContextMenu> .</span><span class="sxs-lookup"><span data-stu-id="91618-120">The example assigns <xref:System.Windows.SystemColors.MenuHighlightBrushKey%2A> as the <xref:System.Windows.Controls.Control.Background%2A> color and <xref:System.Windows.SystemColors.MenuTextBrushKey%2A> as the <xref:System.Windows.Controls.Control.Foreground%2A> color of the <xref:System.Windows.Controls.ContextMenu>.</span></span>  
  
```xaml  
<Style x:Key="SimpleSysResources" TargetType="{x:Type MenuItem}">  
  <Setter Property = "Background" Value=
    "{DynamicResource {x:Static SystemColors.MenuHighlightBrushKey}}"/>  
  <Setter Property = "Foreground" Value=
    "{DynamicResource {x:Static SystemColors.MenuTextBrushKey}}"/>  
</Style>  
```  
  
 <span data-ttu-id="91618-121">Im folgenden Beispiel wird das- <xref:System.Windows.Trigger> Element verwendet, um die Darstellung eines als <xref:System.Windows.Controls.Menu> Reaktion auf Ereignisse zu ändern, die für ausgelöst werden <xref:System.Windows.Controls.ContextMenu> .</span><span class="sxs-lookup"><span data-stu-id="91618-121">The following example uses the <xref:System.Windows.Trigger> element to change the appearance of a <xref:System.Windows.Controls.Menu> in response to events that are raised on the <xref:System.Windows.Controls.ContextMenu>.</span></span> <span data-ttu-id="91618-122">Wenn ein Benutzer die Maus über das Menü bewegt, ändert sich die Darstellung der <xref:System.Windows.Controls.ContextMenu> Elemente.</span><span class="sxs-lookup"><span data-stu-id="91618-122">When a user moves the mouse over the menu, the appearance of the <xref:System.Windows.Controls.ContextMenu> items changes.</span></span>  
  
```xaml  
<Style x:Key="Triggers" TargetType="{x:Type MenuItem}">  
  <Style.Triggers>  
    <Trigger Property="MenuItem.IsMouseOver" Value="true">  
      <Setter Property = "FontSize" Value="16"/>  
      <Setter Property = "FontStyle" Value="Italic"/>  
      <Setter Property = "Foreground" Value="Red"/>  
    </Trigger>  
  </Style.Triggers>  
</Style>  
```  
  
## <a name="see-also"></a><span data-ttu-id="91618-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91618-123">See also</span></span>

- <xref:System.Windows.Controls.ContextMenu>
- <xref:System.Windows.Style>
- <xref:System.Windows.Controls.Menu>
- <xref:System.Windows.Controls.MenuItem>
- [<span data-ttu-id="91618-124">ContextMenu</span><span class="sxs-lookup"><span data-stu-id="91618-124">ContextMenu</span></span>](contextmenu.md)
- [<span data-ttu-id="91618-125">ContextMenu-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="91618-125">ContextMenu Styles and Templates</span></span>](contextmenu-styles-and-templates.md)
- [<span data-ttu-id="91618-126">Beispiel für WPF-Steuerelementsammlungen</span><span class="sxs-lookup"><span data-stu-id="91618-126">WPF Controls Gallery Sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Getting%20Started/ControlsAndLayout)
