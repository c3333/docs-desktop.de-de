---
title: 'Gewusst wie: Angeben einer benutzerdefinierten Popup-Position'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Popup control [WPF], specifying custom position
ms.assetid: 28c24f39-d3aa-4ee2-b950-384b4a5dab92
ms.openlocfilehash: b48dedc044b418062642af5c5bb40afab78a3c97
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977526"
---
# <a name="how-to-specify-a-custom-popup-position"></a>Gewusst wie: Angeben einer benutzerdefinierten Popup-Position
In diesem Beispiel wird gezeigt, wie eine benutzerdefinierte Position für ein Steuerelement angegeben <xref:System.Windows.Controls.Primitives.Popup> wird, wenn die- <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> Eigenschaft auf festgelegt ist <xref:System.Windows.Controls.Primitives.PlacementMode.Custom> .  
  
## <a name="example"></a>Beispiel  
 Wenn die- <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> Eigenschaft auf festgelegt ist <xref:System.Windows.Controls.Primitives.PlacementMode.Custom> , <xref:System.Windows.Controls.Primitives.Popup> Ruft die eine definierte Instanz des Delegaten auf <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> . Dieser Delegat gibt eine Reihe möglicher Punkte zurück, die relativ zur linken oberen Ecke des Zielbereichs und der linken oberen Ecke von sind <xref:System.Windows.Controls.Primitives.Popup> . Die <xref:System.Windows.Controls.Primitives.Popup> Platzierung erfolgt an dem Punkt, an dem die beste Sichtbarkeit bereit steht.  
  
 Im folgenden Beispiel wird gezeigt, wie die Position eines definiert <xref:System.Windows.Controls.Primitives.Popup> wird, indem die-Eigenschaft auf festgelegt wird <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> <xref:System.Windows.Controls.Primitives.PlacementMode.Custom> . Außerdem wird gezeigt, wie ein Delegat erstellt und zugewiesen wird <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> , um die zu positionieren <xref:System.Windows.Controls.Primitives.Popup> .  Der Rückruf Delegat gibt zwei- <xref:System.Windows.Controls.Primitives.CustomPopupPlacement> Objekte zurück.  Wenn die <xref:System.Windows.Controls.Primitives.Popup> von einem Bildschirmrand an der ersten Position ausgeblendet wird, <xref:System.Windows.Controls.Primitives.Popup> wird der an der zweiten Position platziert.  
  
 [!code-xaml[PopupCustomPlacement#CustomPlacement](~/samples/snippets/csharp/VS_Snippets_Wpf/PopupCustomPlacement/CSharp/Window1.xaml#customplacement)]  
  
 [!code-csharp[PopupCustomPlacement#DelegateInstance](~/samples/snippets/csharp/VS_Snippets_Wpf/PopupCustomPlacement/CSharp/Window1.xaml.cs#delegateinstance)]
 [!code-vb[PopupCustomPlacement#DelegateInstance](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PopupCustomPlacement/visualbasic/window1.xaml.vb#delegateinstance)]  
  
 [!code-csharp[PopupCustomPlacement#DelegateDefinition](~/samples/snippets/csharp/VS_Snippets_Wpf/PopupCustomPlacement/CSharp/Window1.xaml.cs#delegatedefinition)]
 [!code-vb[PopupCustomPlacement#DelegateDefinition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PopupCustomPlacement/visualbasic/window1.xaml.vb#delegatedefinition)]  
  
 Das komplette Beispiel finden Sie unter [Beispiel für eine Popup Platzierung](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/VS_Snippets_Wpf/PopupPositionSnippet/CS).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Primitives.Popup>
- [Übersicht über Popup](popup-overview.md)
- [Gewusst-wie-Artikel](popup-how-to-topics.md)
