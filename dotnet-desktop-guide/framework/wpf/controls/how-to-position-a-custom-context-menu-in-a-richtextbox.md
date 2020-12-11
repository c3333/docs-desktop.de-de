---
title: 'Gewusst wie: Positionieren eines benutzerdefinierten Kontextmenüs in einem "RichTextBox"-Element'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom context menus [WPF], positioning
- positioning custom context menus [WPF]
- RichTextBox control [WPF], positioning custom context menus
- context menus [WPF], positioning
ms.assetid: bf77c930-a546-4573-9a56-9af345ba189a
ms.openlocfilehash: f9407f59c3daafd09fa5b84006f33ef2f3ebd31f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978158"
---
# <a name="how-to-position-a-custom-context-menu-in-a-richtextbox"></a>Gewusst wie: Positionieren eines benutzerdefinierten Kontextmenüs in einem "RichTextBox"-Element
In diesem Beispiel wird gezeigt, wie ein benutzerdefiniertes Kontextmenü für eine positioniert wird <xref:System.Windows.Controls.RichTextBox> .  
  
 Bei der Implementierung eines benutzerdefinierten Kontextmenüs für ein **RichTextBox**-Element sind Sie verantwortlich für die Positionierung des Kontextmenüs.  Standardmäßig wird ein benutzerdefiniertes Kontextmenü in der Mitte des **RichTextBox**-Elements geöffnet.  
  
## <a name="example"></a>Beispiel  
 Um das Standard Platzierungs Verhalten zu überschreiben, fügen Sie einen Listener für das- <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> Ereignis hinzu.  Im folgenden Beispiel wird veranschaulicht, wie dies programmgesteuert erfolgt.  
  
 [!code-csharp[RichTextBox_ContextMenu#_AddListener](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBox_ContextMenu/CSharp/app.xaml.cs#_addlistener)]
 [!code-vb[RichTextBox_ContextMenu#_AddListener](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBox_ContextMenu/VisualBasic/app.xaml.vb#_addlistener)]  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt eine Implementierung des entsprechenden <xref:System.Windows.FrameworkContentElement.ContextMenuOpening> Ereignislistener.  
  
 [!code-csharp[RichTextBox_ContextMenu#_ListenerBody](~/samples/snippets/csharp/VS_Snippets_Wpf/RichTextBox_ContextMenu/CSharp/app.xaml.cs#_listenerbody)]
 [!code-vb[RichTextBox_ContextMenu#_ListenerBody](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RichTextBox_ContextMenu/VisualBasic/app.xaml.vb#_listenerbody)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über RichTextBox](richtextbox-overview.md)
- [Übersicht über TextBox](textbox-overview.md)
