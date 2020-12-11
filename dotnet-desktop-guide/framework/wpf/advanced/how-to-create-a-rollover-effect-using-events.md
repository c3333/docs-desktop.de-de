---
title: 'Gewusst wie: Erstellen eines Rollovereffekts mit Ereignissen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- colors of elements [WPF], changing
- rollover effect [WPF]
- element colors [WPF], changing
ms.assetid: 3b20d028-6f1c-4b25-95d2-fa68cefbdb4c
ms.openlocfilehash: d4587b7b116045af11702a99c841956434f96404
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977555"
---
# <a name="how-to-create-a-rollover-effect-using-events"></a>Gewusst wie: Erstellen eines Rollovereffekts mit Ereignissen
Dieses Beispiel zeigt, wie Sie die Farbe eines Elements ändern können, wenn der Mauszeiger in den Bereich wechselt, der vom-Element belegt wird.  
  
 Dieses Beispiel besteht aus einer [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Datei und einer Code Behind-Datei.  
  
> [!NOTE]
> In diesem Beispiel wird veranschaulicht, wie Ereignisse verwendet werden, aber die empfohlene Vorgehensweise zum Erreichen desselben Effekts ist die Verwendung von <xref:System.Windows.Trigger> in einem Stil. Weitere Informationen finden Sie unter [Erstellen von Formaten und Vorlagen](/dotnet/desktop-wpf/fundamentals/styles-templates-overview).  
  
## <a name="example"></a>Beispiel  
 Der folgende XAML-Code erstellt die Benutzeroberfläche, die aus <xref:System.Windows.Controls.Border> einem besteht <xref:System.Windows.Controls.TextBlock> , und fügt die <xref:System.Windows.Input.Mouse.MouseEnter> -Ereignishandler und die- <xref:System.Windows.UIElement.MouseLeave> Ereignishandler an die an <xref:System.Windows.Controls.Border> .  
  
 [!code-xaml[mouseenterMouseleave#MouseEnterLeaveSampleXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/mouseenterMouseleave/CSharp/Window1.xaml#mouseenterleavesamplexaml)]  
  
 Der folgende Code Behind erstellt die <xref:System.Windows.UIElement.MouseEnter> <xref:System.Windows.UIElement.MouseLeave> Ereignishandler und.  Wenn der Mauszeiger in den Eintritt <xref:System.Windows.Controls.Border> , wird der Hintergrund der <xref:System.Windows.Controls.Border> in rot geändert.  Wenn der Mauszeiger das-Zeichen verlässt <xref:System.Windows.Controls.Border> , wird der Hintergrund von <xref:System.Windows.Controls.Border> wieder in weiß geändert.  
  
 [!code-csharp[mouseenterMouseleave#MouseEnterLeaveSampleEventHandlers](~/samples/snippets/csharp/VS_Snippets_Wpf/mouseenterMouseleave/CSharp/Window1.xaml.cs#mouseenterleavesampleeventhandlers)]
 [!code-vb[mouseenterMouseleave#MouseEnterLeaveSampleEventHandlers](~/samples/snippets/visualbasic/VS_Snippets_Wpf/mouseenterMouseleave/VisualBasic/Window1.xaml.vb#mouseenterleavesampleeventhandlers)]
