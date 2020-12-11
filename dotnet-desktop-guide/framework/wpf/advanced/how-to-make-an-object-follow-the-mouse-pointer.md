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
# <a name="how-to-make-an-object-follow-the-mouse-pointer"></a>Gewusst wie: Konfigurieren eines Objekts zum Folgen des Mauszeigers
In diesem Beispiel wird gezeigt, wie die Dimensionen eines Objekts geändert werden, wenn der Mauszeiger auf dem Bildschirm bewegt wird.  
  
 Das Beispiel enthält eine [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] -Datei, die die [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] -und eine Code-Behind-Datei erstellt, die den-Ereignishandler erstellt.  
  
## <a name="example"></a>Beispiel  
 Mit dem folgenden XAML-Code wird das erstellt [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] , das aus einem <xref:System.Windows.Shapes.Ellipse> in einem besteht <xref:System.Windows.Controls.StackPanel> und den Ereignishandler für das-Ereignis anfügt <xref:System.Windows.UIElement.MouseMove> .  
  
 [!code-xaml[mouseMoveWithPointer#MouseMoveWithPointerXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/mouseMoveWithPointer/CSharp/Window1.xaml#mousemovewithpointerxaml)]  
  
 Der folgende Code Behind erstellt den- <xref:System.Windows.UIElement.MouseMove> Ereignishandler.  Wenn der Mauszeiger bewegt wird, werden die Höhe und die Breite des <xref:System.Windows.Shapes.Ellipse> erhöht und gesenkt.  
  
 [!code-csharp[mouseMoveWithPointer#MouseMovePointerGetPosition](~/samples/snippets/csharp/VS_Snippets_Wpf/mouseMoveWithPointer/CSharp/Window1.xaml.cs#mousemovepointergetposition)]
 [!code-vb[mouseMoveWithPointer#MouseMovePointerGetPosition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/mouseMoveWithPointer/VisualBasic/Window1.xaml.vb#mousemovepointergetposition)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Eingabe](input-overview.md)
