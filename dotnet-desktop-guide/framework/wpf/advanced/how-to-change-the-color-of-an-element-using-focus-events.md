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
# <a name="how-to-change-the-color-of-an-element-using-focus-events"></a>Gewusst wie: Ändern der Farbe eines Elements mithilfe von Fokusereignissen
Dieses Beispiel zeigt, wie Sie die Farbe eines Elements ändern können, wenn es mit dem <xref:System.Windows.UIElement.GotFocus> -Ereignis und dem-Ereignis den Fokus verliert <xref:System.Windows.UIElement.LostFocus> .  
  
 Dieses Beispiel besteht aus einer [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Datei und einer Code Behind-Datei.  
  
## <a name="example"></a>Beispiel  
 Der folgende XAML-Code erstellt die Benutzeroberfläche, die aus zwei <xref:System.Windows.Controls.Button> -Objekten besteht, und fügt Ereignishandler für die <xref:System.Windows.UIElement.GotFocus> -und- <xref:System.Windows.UIElement.LostFocus> Ereignisse an die- <xref:System.Windows.Controls.Button> Objekte an.  
  
 [!code-xaml[gotfocusLostfocusEffectUsingEvent#GotLostFocusSampleXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/gotfocusLostfocusEffectUsingEvent/CSharp/Window1.xaml#gotlostfocussamplexaml)]  
  
 Der folgende Code Behind erstellt die <xref:System.Windows.UIElement.GotFocus> <xref:System.Windows.UIElement.LostFocus> Ereignishandler und.  Wenn der <xref:System.Windows.Controls.Button> Tastaturfokus erhält, <xref:System.Windows.Controls.Control.Background%2A> wird der von <xref:System.Windows.Controls.Button> in rot geändert.  Wenn das den <xref:System.Windows.Controls.Button> Tastaturfokus verliert, <xref:System.Windows.Controls.Control.Background%2A> wird der von <xref:System.Windows.Controls.Button> wieder in weiß geändert.  
  
 [!code-csharp[gotfocusLostfocusEffectUsingEvent#GotLostFocusSampleEventHandlers](~/samples/snippets/csharp/VS_Snippets_Wpf/gotfocusLostfocusEffectUsingEvent/CSharp/Window1.xaml.cs#gotlostfocussampleeventhandlers)]
 [!code-vb[gotfocusLostfocusEffectUsingEvent#GotLostFocusSampleEventHandlers](~/samples/snippets/visualbasic/VS_Snippets_Wpf/gotfocusLostfocusEffectUsingEvent/VisualBasic/Window1.xaml.vb#gotlostfocussampleeventhandlers)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Eingabe](input-overview.md)
