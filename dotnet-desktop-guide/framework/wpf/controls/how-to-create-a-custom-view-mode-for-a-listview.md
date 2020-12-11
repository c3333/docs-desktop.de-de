---
title: 'Gewusst wie: Erstellen eines benutzerdefinierten Ansichtsmodus für eine ListView'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView controls [WPF], creating custom View mode
ms.assetid: 71077349-eeb9-4344-ab29-b5df96df3314
ms.openlocfilehash: 3b9ca17bddcecb1895205fca76f0a489ecf25c4f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978073"
---
# <a name="how-to-create-a-custom-view-mode-for-a-listview"></a>Gewusst wie: Erstellen eines benutzerdefinierten Ansichtsmodus für eine ListView

Dieses Beispiel zeigt, wie ein benutzerdefinierter <xref:System.Windows.Controls.ListView.View%2A> Modus für ein Steuerelement erstellt wird <xref:System.Windows.Controls.ListView> .  
  
## <a name="example"></a>Beispiel  
 Sie müssen die- <xref:System.Windows.Controls.ViewBase> Klasse verwenden, wenn Sie eine benutzerdefinierte Ansicht für das-Steuerelement erstellen <xref:System.Windows.Controls.ListView> . Das folgende Beispiel zeigt einen Ansichtsmodus `PlainView` , der von der- <xref:System.Windows.Controls.ViewBase> Klasse abgeleitet wird.  
  
 [!code-csharp[ListViewCustomView#PlainView](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/PlainView.cs#plainview)]
 [!code-vb[ListViewCustomView#PlainView](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ListViewCustomView/visualbasic/plainview.vb#plainview)]  
  
 Verwenden Sie die-Klasse, um einen Stil auf die benutzerdefinierte Ansicht anzuwenden <xref:System.Windows.Style> . Im folgenden Beispiel wird ein <xref:System.Windows.Style> für den `PlainView` Ansichtsmodus definiert. Im vorherigen Beispiel wird dieser Stil als Wert der-Eigenschaft festgelegt, die <xref:System.Windows.Controls.ViewBase.DefaultStyleKey%2A> für definiert ist `PlainView` .  
  
 [!code-xaml[ListViewCustomView#PlainViewStyle](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/Themes/Generic.xaml#plainviewstyle)]  
  
 Um das Layout der Daten in einem benutzerdefinierten Ansichtsmodus zu definieren, definieren Sie ein- <xref:System.Windows.DataTemplate> Objekt. Im folgenden Beispiel wird ein definiert <xref:System.Windows.DataTemplate> , das zum Anzeigen von Daten im `PlainView` Ansichtsmodus verwendet werden kann.  
  
 [!code-xaml[ListViewCustomView#PlainViewDataTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/Window1.xaml#plainviewdatatemplate)]  
  
 Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.ResourceKey> für den `PlainView` Ansichtsmodus definiert wird, der das verwendet <xref:System.Windows.DataTemplate> , das im vorherigen Beispiel definiert wurde.  
  
 [!code-xaml[ListViewCustomView#PlainViewtileView](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/Window1.xaml#plainviewtileview)]  
  
 Ein <xref:System.Windows.Controls.ListView> Steuerelement kann eine benutzerdefinierte Ansicht verwenden, wenn Sie die- <xref:System.Windows.Controls.ListView.View%2A> Eigenschaft auf den Ressourcen Schlüssel festlegen. Im folgenden Beispiel wird gezeigt, wie `PlainView` als Ansichtsmodus für eine angegeben wird <xref:System.Windows.Controls.ListView> .  
  
 [!code-csharp[ListViewCustomView#ListViewtileViewmode](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/Window1.xaml.cs#listviewtileviewmode)]
 [!code-vb[ListViewCustomView#ListViewtileViewmode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ListViewCustomView/visualbasic/window1.xaml.vb#listviewtileviewmode)]  
  
 Das komplette Beispiel finden Sie unter [ListView mit mehreren Ansichten (c#)](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp) oder [ListView mit mehreren Ansichten (Visual Basic)](https://github.com/dotnet/docs/tree/master/samples/snippets/visualbasic/VS_Snippets_Wpf/ListViewCustomView/visualbasic).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Artikel zu Vorgehensweisen](listview-how-to-topics.md)
- [Übersicht über ListView](listview-overview.md)
- [Übersicht über GridView](gridview-overview.md)
