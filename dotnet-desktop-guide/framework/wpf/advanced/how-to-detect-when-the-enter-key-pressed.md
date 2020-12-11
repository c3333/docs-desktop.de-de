---
title: 'Gewusst wie: Erkennen, wenn die EINGABETASTE gedrückt wird'
description: Erkennen, wenn die Eingabetaste auf der Tastatur in Windows Presentation Foundation ausgewählt ist. Dieses Beispiel besteht aus XAML und einer Code Behind-Datei.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Enter key [WPF], detecting
- keys [WPF], Enter
ms.assetid: a66f39d2-ef4a-43a5-b454-a4ea0fe88655
ms.openlocfilehash: 1e74113f22e03f41da2e51178179aa52f6bfcd2c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977000"
---
# <a name="how-to-detect-when-the-enter-key-pressed"></a>Gewusst wie: Erkennen, wenn die EINGABETASTE gedrückt wird
Dieses Beispiel zeigt, wie Sie erkennen können, wann der <xref:System.Windows.Input.Key.Enter> Schlüssel auf der Tastatur gedrückt wird.  
  
 Dieses Beispiel besteht aus einer [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Datei und einer Code Behind-Datei.  
  
## <a name="example"></a>Beispiel  
 Wenn der Benutzer die <xref:System.Windows.Input.Key.Enter> Taste in drückt <xref:System.Windows.Controls.TextBox> , wird die Eingabe im Textfeld in einem anderen Bereich des angezeigt [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] .  
  
 Der folgende XAML-Code erstellt die Benutzeroberfläche, die aus <xref:System.Windows.Controls.StackPanel> , <xref:System.Windows.Controls.TextBlock> und besteht <xref:System.Windows.Controls.TextBox> .  
  
 [!code-xaml[keydown#KeyDownUI](~/samples/snippets/csharp/VS_Snippets_Wpf/KeyDown/CSharp/Window1.xaml#keydownui)]  
  
 Der folgende Code Behind erstellt den- <xref:System.Windows.UIElement.KeyDown> Ereignishandler.  Wenn die gedrückte Taste der Schlüssel ist <xref:System.Windows.Input.Key.Enter> , wird eine Meldung in der angezeigt <xref:System.Windows.Controls.TextBlock> .  
  
 [!code-csharp[keydown#KeyDownSample](~/samples/snippets/csharp/VS_Snippets_Wpf/KeyDown/CSharp/Window1.xaml.cs#keydownsample)]
 [!code-vb[keydown#KeyDownSample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/KeyDown/VisualBasic/Window1.xaml.vb#keydownsample)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Eingabe](input-overview.md)
- [Übersicht über Routingereignisse](routed-events-overview.md)
