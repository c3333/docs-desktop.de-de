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
# <a name="contextmenu-overview"></a>Übersicht über ContextMenu
Die- <xref:System.Windows.Controls.ContextMenu> Klasse stellt das-Element dar, das Funktionen mithilfe eines kontextspezifischen verfügbar macht <xref:System.Windows.Controls.Menu> . Normalerweise macht ein Benutzer das <xref:System.Windows.Controls.ContextMenu> in der verfügbar, [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] indem er mit der rechten Maustaste auf die Maustaste klickt. In diesem Thema wird das <xref:System.Windows.Controls.ContextMenu> -Element vorgestellt, und es werden Beispiele für die Verwendung in [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] und Code bereitstellt.  

<a name="contextmenu_control"></a>
## <a name="contextmenu-control"></a>ContextMenu-Steuerelement  
 Ein <xref:System.Windows.Controls.ContextMenu> wird an ein bestimmtes Steuerelement angefügt. Mit dem- <xref:System.Windows.Controls.ContextMenu> Element können Sie Benutzern eine Liste von Elementen präsentieren, mit denen Befehle oder Optionen angegeben werden, die einem bestimmten Steuerelement zugeordnet sind, z <xref:System.Windows.Controls.Button> . b. ein. Das Menü wird mit einem Rechtsklick mit der Maus aufgerufen. Wenn Sie auf einen klicken, wird in der Regel ein <xref:System.Windows.Controls.MenuItem> Untermenü geöffnet, oder eine Anwendung führt einen Befehl aus.  
  
<a name="creating_contextmenus"></a>
## <a name="creating-contextmenus"></a>Erstellen von ContextMenus  
 In den folgenden Beispielen wird veranschaulicht, wie ein <xref:System.Windows.Controls.ContextMenu> mit Untermenüs erstellt wird. Die Steuer <xref:System.Windows.Controls.ContextMenu> Elemente werden an Schaltflächen Steuerelemente angefügt.  
  
 [!code-xaml[ContextMenu#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenu/CSharp/Pane1.xaml#1)]  
  
 [!code-csharp[ContextMenu#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ContextMenu/CSharp/Pane1.xaml.cs#2)]
 [!code-vb[ContextMenu#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ContextMenu/VisualBasic/Pane1.xaml.vb#2)]  
  
<a name="applying_styles_to_contextmenu"></a>
## <a name="applying-styles-to-a-contextmenu"></a>Anwenden von Stilen auf ein ContextMenu  
 Mithilfe eines-Steuer Elements <xref:System.Windows.Style> können Sie die Darstellung und das Verhalten eines drastisch ändern, <xref:System.Windows.Controls.ContextMenu> ohne ein benutzerdefiniertes Steuerelement schreiben zu müssen. Zusätzlich zur Festlegung von visuellen Eigenschaften können Sie auch Stile auf Teilelemente eines Steuerelements anwenden. Beispielsweise können Sie das Verhalten der Teile des Steuer Elements ändern, indem Sie Eigenschaften verwenden, oder Sie können Teile hinzufügen oder das Layout von ändern <xref:System.Windows.Controls.ContextMenu> . In den folgenden Beispielen werden verschiedene Möglichkeiten zum Hinzufügen von Stilen zu-Steuer <xref:System.Windows.Controls.ContextMenu> Elementen veranschaulicht.  
  
 Im ersten Beispiel wird ein Stil mit der Bezeichnung `SimpleSysResources` definiert. An diesem Beispiel können Sie sehen, wie die aktuellen Systemeinstellungen in Ihrem Stil verwendet werden können. Im Beispiel wird <xref:System.Windows.SystemColors.MenuHighlightBrushKey%2A> als <xref:System.Windows.Controls.Control.Background%2A> Farbe und <xref:System.Windows.SystemColors.MenuTextBrushKey%2A> als <xref:System.Windows.Controls.Control.Foreground%2A> Farbe des zugewiesen <xref:System.Windows.Controls.ContextMenu> .  
  
```xaml  
<Style x:Key="SimpleSysResources" TargetType="{x:Type MenuItem}">  
  <Setter Property = "Background" Value=
    "{DynamicResource {x:Static SystemColors.MenuHighlightBrushKey}}"/>  
  <Setter Property = "Foreground" Value=
    "{DynamicResource {x:Static SystemColors.MenuTextBrushKey}}"/>  
</Style>  
```  
  
 Im folgenden Beispiel wird das- <xref:System.Windows.Trigger> Element verwendet, um die Darstellung eines als <xref:System.Windows.Controls.Menu> Reaktion auf Ereignisse zu ändern, die für ausgelöst werden <xref:System.Windows.Controls.ContextMenu> . Wenn ein Benutzer die Maus über das Menü bewegt, ändert sich die Darstellung der <xref:System.Windows.Controls.ContextMenu> Elemente.  
  
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
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.ContextMenu>
- <xref:System.Windows.Style>
- <xref:System.Windows.Controls.Menu>
- <xref:System.Windows.Controls.MenuItem>
- [ContextMenu](contextmenu.md)
- [ContextMenu-Stile und -Vorlagen](contextmenu-styles-and-templates.md)
- [Beispiel für WPF-Steuerelementsammlungen](https://github.com/Microsoft/WPF-Samples/tree/master/Getting%20Started/ControlsAndLayout)
