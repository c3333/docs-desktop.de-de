---
title: 'Gewusst wie: Erstellen und Verwenden eines Canvas'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], Canvas
- Canvas control [WPF], creating
- Canvas control [WPF], using
ms.assetid: 420b9487-9a15-477c-9489-a22a4dec7779
ms.openlocfilehash: c9ee49327b6490df094e84b4227ea0fb2e757c4d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976997"
---
# <a name="how-to-create-and-use-a-canvas"></a>Gewusst wie: Erstellen und Verwenden eines Canvas
In diesem Beispiel wird gezeigt, wie eine Instanz von erstellt und verwendet wird <xref:System.Windows.Controls.Canvas> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel <xref:System.Windows.Controls.TextBlock> werden zwei-Elemente explizit mithilfe der <xref:System.Windows.Controls.Canvas.SetTop%2A> - <xref:System.Windows.Controls.Canvas.SetLeft%2A> Methode und der-Methode von positioniert <xref:System.Windows.Controls.Canvas> . Im Beispiel wird auch eine <xref:System.Windows.Controls.Control.Background%2A> Farbe von zugewiesen `LightSteelBlue` <xref:System.Windows.Controls.Canvas> .  
  
> [!NOTE]
> Wenn Sie [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] zum Positionieren von <xref:System.Windows.Controls.TextBlock> Elementen verwenden, verwenden Sie die <xref:System.Windows.Controls.Canvas.Top%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Controls.Canvas.Left%2A> .  
  
 [!code-csharp[CanvasCode#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasCode/CSharp/Canvas_Code.cs#1)]
 [!code-vb[CanvasCode#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasCode/VisualBasic/canvas_vb.vb#1)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.TextBlock>
- <xref:System.Windows.Controls.Canvas.SetTop%2A>
- <xref:System.Windows.Controls.Canvas.SetLeft%2A>
- <xref:System.Windows.Controls.Canvas.Top%2A>
- <xref:System.Windows.Controls.Canvas.Left%2A>
- [Übersicht über Panel-Elemente](panels-overview.md)
- [Artikel zu Vorgehensweisen](canvas-how-to-topics.md)
