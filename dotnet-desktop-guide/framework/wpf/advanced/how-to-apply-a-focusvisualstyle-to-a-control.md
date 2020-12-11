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
# <a name="how-to-apply-a-focusvisualstyle-to-a-control"></a>Gewusst wie: Anwenden eines FocusVisualStyle auf ein Steuerelement
In diesem Beispiel wird gezeigt, wie Sie einen visuellen Fokus Stil in Ressourcen erstellen und den Stil mithilfe der-Eigenschaft auf ein Steuerelement anwenden <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein Stil definiert, mit dem zusätzliche Steuerelement Zusammensetzung erstellt werden, die nur angewendet wird, wenn sich das Steuerelement im Fokus befindet [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] . Dies wird erreicht, indem ein Stil mit einem definiert <xref:System.Windows.Controls.ControlTemplate> und dann beim Festlegen der-Eigenschaft auf diesen Stil als Ressource verwiesen wird <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> .  
  
 Ein externes Rechteck, das einem Rahmen ähnelt, wird außerhalb des rechteckigen Bereichs platziert. Sofern nicht anders geändert, verwendet die Größe des Stils den <xref:System.Windows.FrameworkElement.ActualHeight%2A> und <xref:System.Windows.FrameworkElement.ActualWidth%2A> des rechteckigen Steuer Elements, bei dem der visuelle Fokus Stil angewendet wird. In diesem Beispiel werden negative Werte für das festgelegt <xref:System.Windows.FrameworkElement.Margin%2A> , damit der Rahmen etwas außerhalb des Steuer Elements angezeigt wird.  
  
 [!code-xaml[FEFocusVisualStyle#XAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FEFocusVisualStyle/CS/page1.xaml#xaml)]  
  
 Ein <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A> ist ein Additiv zu einem Steuerelement Vorlagen Stil, der entweder von einem expliziten Stil oder einem Design Stil stammt. der primäre Stil für ein Steuerelement kann weiterhin mithilfe von erstellt werden, <xref:System.Windows.Controls.ControlTemplate> und dieser Stil wird auf die-Eigenschaft festgelegt <xref:System.Windows.FrameworkElement.Style%2A> .  
  
 Visuelle Fokus Stile sollten konsistent für ein Design oder eine Benutzeroberfläche verwendet werden, anstatt für jedes Fokussier Bare Element einen anderen zu verwenden. Weitere Informationen finden Sie unter Formatieren [für den Fokus in Steuerelementen und Focus VisualStyle](styling-for-focus-in-controls-and-focusvisualstyle.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A>
- [Erstellen von Formaten und Vorlagen](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [Fokusstile in Steuerelementen und FocusVisualStyle](styling-for-focus-in-controls-and-focusvisualstyle.md)
