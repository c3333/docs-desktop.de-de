---
title: 'Gewusst wie: Sicherstellen, dass ein GridSplitter sichtbar ist'
ms.date: 03/30/2017
helpviewer_keywords:
- GridSplitter control [WPF], ensuring visibility of
ms.assetid: 0a62a964-89c8-48f0-9023-5df721a8cf47
ms.openlocfilehash: 2085ac5cec206d8692a1267acf132688f0aa9082
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978165"
---
# <a name="how-to-make-sure-that-a-gridsplitter-is-visible"></a>Gewusst wie: Sicherstellen, dass ein GridSplitter sichtbar ist
In diesem Beispiel wird gezeigt, wie sichergestellt wird, dass ein <xref:System.Windows.Controls.GridSplitter> Steuerelement nicht von den anderen Steuerelementen in einer ausgeblendet wird <xref:System.Windows.Controls.Grid> .  
  
## <a name="example"></a>Beispiel  
 Der <xref:System.Windows.Controls.Panel.Children%2A> eines <xref:System.Windows.Controls.Grid> Steuer Elements wird in der Reihenfolge gerendert, in der Sie in Markup oder Code definiert sind. <xref:System.Windows.Controls.GridSplitter> Steuerelemente können von anderen Steuerelementen ausgeblendet werden, wenn Sie Sie nicht als die letzten Elemente in der Auflistung definieren, <xref:System.Windows.Controls.Panel.Children%2A> oder wenn Sie andere Steuerelemente eine höhere Version angeben <xref:System.Windows.Controls.Panel.ZIndexProperty> .  
  
 <xref:System.Windows.Controls.GridSplitter>Führen Sie einen der folgenden Schritte aus, um verborgene Steuerelemente zu verhindern.  
  
- Stellen Sie sicher, dass die-Steuer <xref:System.Windows.Controls.GridSplitter> Elemente der zuletzt <xref:System.Windows.Controls.Panel.Children%2A> hinzugefügt wurden <xref:System.Windows.Controls.Grid> . Das folgende Beispiel zeigt <xref:System.Windows.Controls.GridSplitter> als letztes Element in der-Auflistung <xref:System.Windows.Controls.Panel.Children%2A> von <xref:System.Windows.Controls.Grid> .  
  
 [!code-xaml[GridSplitterSnips#GridSplitterLastChild](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplitterlastchild)]  
  
- Legen <xref:System.Windows.Controls.Panel.ZIndexProperty> Sie auf fest <xref:System.Windows.Controls.GridSplitter> , damit es höher ist als ein Steuerelement, das es andernfalls ausblenden würde. Im folgenden Beispiel wird das- <xref:System.Windows.Controls.GridSplitter> Steuerelement höher <xref:System.Windows.Controls.Panel.ZIndexProperty> als das-Steuerelement <xref:System.Windows.Controls.Button> .  
  
 [!code-xaml[GridSplitterSnips#GridSplitterZIndex](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplitterzindex)]  
  
- Legen Sie Ränder für das-Steuerelement fest, die andernfalls ausblenden, <xref:System.Windows.Controls.GridSplitter> sodass der verfügbar gemacht <xref:System.Windows.Controls.GridSplitter> wird. Im folgenden Beispiel werden die Ränder eines-Steuer Elements festgelegt, das andernfalls überlagern und ausblenden würde <xref:System.Windows.Controls.GridSplitter> .  
  
 [!code-xaml[GridSplitterSnips#GridSplitterMargin](~/samples/snippets/csharp/VS_Snippets_Wpf/GridSplitterSnips/CSharp/Window1.xaml#gridsplittermargin)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.GridSplitter>
- [Artikel zu Vorgehensweisen](gridsplitter-how-to-topics.md)
