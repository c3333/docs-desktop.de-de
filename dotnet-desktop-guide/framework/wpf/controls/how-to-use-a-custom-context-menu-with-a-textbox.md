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
# <a name="how-to-use-a-custom-context-menu-with-a-textbox"></a>Gewusst wie: Verwenden eines benutzerdefinierten Kontextmenüs mit "TextBox"
In diesem Beispiel wird gezeigt, wie ein einfaches benutzerdefiniertes Kontextmenü für ein definiert und implementiert wird <xref:System.Windows.Controls.TextBox> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beispiel wird ein-Steuerelement definiert <xref:System.Windows.Controls.TextBox> , das ein benutzerdefiniertes Kontextmenü enthält.  
  
 Das Kontextmenü wird mithilfe eines- <xref:System.Windows.Controls.ContextMenu> Elements definiert.  Das Kontextmenü selbst besteht aus einer Reihe von <xref:System.Windows.Controls.MenuItem> Elementen und <xref:System.Windows.Controls.Separator> Elementen.  Jedes- <xref:System.Windows.Controls.MenuItem> Element definiert einen Befehl im Kontextmenü. das <xref:System.Windows.Controls.HeaderedItemsControl.Header%2A> -Attribut definiert den Anzeige Text für den Menübefehl, und das- <xref:System.Windows.Controls.MenuItem.Click> Attribut gibt eine Handlermethode für jedes Menü Element an.  Das <xref:System.Windows.Controls.Separator> -Element bewirkt lediglich, dass eine Trennlinie zwischen den vorherigen und nachfolgenden Menü Elementen gerendert wird.  
  
 [!code-xaml[TextBox_ContextMenu#_TextBox_ContextMenuXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_ContextMenu/CSharp/Window1.xaml#_textbox_contextmenuxaml)]  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt den Implementierungs Code für die vorherige Kontextmenü Definition sowie den Code, der das Kontextmenü aktiviert und deaktiviert.  Das- <xref:System.Windows.Controls.ContextMenu.Opened> Ereignis wird verwendet, um bestimmte Befehle basierend auf dem aktuellen Zustand von dynamisch zu aktivieren oder zu deaktivieren <xref:System.Windows.Controls.TextBox> .  
  
 Um das Standardkontext Menü wiederherzustellen, verwenden <xref:System.Windows.DependencyObject.ClearValue%2A> Sie die-Methode, um den Wert der-Eigenschaft zu löschen <xref:System.Windows.FrameworkElement.ContextMenu%2A> .  Um das Kontextmenü vollständig zu deaktivieren, legen Sie die- <xref:System.Windows.FrameworkElement.ContextMenu%2A> Eigenschaft auf einen NULL-Verweis ( `Nothing` in Visual Basic) fest.  
  
 [!code-csharp[TextBox_ContextMenu#_TextBox_ContextMenu](~/samples/snippets/csharp/VS_Snippets_Wpf/TextBox_ContextMenu/CSharp/Window1.xaml.cs#_textbox_contextmenu)]
 [!code-vb[TextBox_ContextMenu#_TextBox_ContextMenu](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextBox_ContextMenu/VisualBasic/Window1.xaml.vb#_textbox_contextmenu)]  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden der Rechtschreibprüfung mit einem Kontextmenü](how-to-use-spell-checking-with-a-context-menu.md)
- [Übersicht über TextBox](textbox-overview.md)
- [Übersicht über RichTextBox](richtextbox-overview.md)
