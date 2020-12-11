---
title: 'Gewusst wie: Suchen von Elementen, die mit einer DataTemplate generiert wurden'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- finding DataTemplate elements [WPF]
- DataTemplate [WPF]
ms.assetid: bfcd564e-5e9e-451e-8641-a9b5c3cfac90
ms.openlocfilehash: a0cb3c6f4431e16425d8aae305a917d87a3d7f96
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978145"
---
# <a name="how-to-find-datatemplate-generated-elements"></a>Gewusst wie: Suchen von Elementen, die mit einer DataTemplate generiert wurden
Dieses Beispiel zeigt, wie Sie Elemente finden, die von einem generiert werden <xref:System.Windows.DataTemplate> .  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel gibt es eine <xref:System.Windows.Controls.ListBox> , die an einige XML-Daten gebunden ist:  
  
 [!code-xaml[FindGeneratedItems#LB](~/samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml#lb)]  
  
 Der <xref:System.Windows.Controls.ListBox> verwendet Folgendes <xref:System.Windows.DataTemplate> :  
  
 [!code-xaml[FindGeneratedItems#DT](~/samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml#dt)]  
  
 Wenn Sie das Element abrufen möchten <xref:System.Windows.Controls.TextBlock> , das von <xref:System.Windows.DataTemplate> einem bestimmten generiert <xref:System.Windows.Controls.ListBoxItem> wurde, müssen Sie das Abrufen <xref:System.Windows.Controls.ListBoxItem> , das <xref:System.Windows.Controls.ContentPresenter> in diesem suchen <xref:System.Windows.Controls.ListBoxItem> und dann für den aufrufen, der <xref:System.Windows.FrameworkTemplate.FindName%2A> <xref:System.Windows.DataTemplate> auf festgelegt ist <xref:System.Windows.Controls.ContentPresenter> . Im folgenden Beispiel wird gezeigt, wie diese Schritte ausgeführt werden. Zu Demonstrationszwecken wird in diesem Beispiel ein Meldungs Feld erstellt, in dem der Text Inhalt des <xref:System.Windows.DataTemplate> -generierten Textblocks angezeigt wird.  
  
 [!code-csharp[FindGeneratedItems#DTFindElement](~/samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml.cs#dtfindelement)]
 [!code-vb[FindGeneratedItems#DTFindElement](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FindGeneratedItems/VisualBasic/Window1.xaml.vb#dtfindelement)]  
  
 Im folgenden finden Sie die Implementierung von `FindVisualChild` , die die- <xref:System.Windows.Media.VisualTreeHelper> Methoden verwendet:  
  
 [!code-csharp[FindGeneratedItems#FVC](~/samples/snippets/csharp/VS_Snippets_Wpf/FindGeneratedItems/CSharp/Window1.xaml.cs#fvc)]
 [!code-vb[FindGeneratedItems#FVC](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FindGeneratedItems/VisualBasic/Window1.xaml.vb#fvc)]  
  
## <a name="see-also"></a>Siehe auch

- [How to: Suchen von Elementen, die mit einer ControlTemplate generiert wurden](../controls/how-to-find-controltemplate-generated-elements.md)
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
- [Erstellen von Formaten und Vorlagen](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [WPF-XAML-Namescopes](../advanced/wpf-xaml-namescopes.md)
- [Strukturen in WPF](../advanced/trees-in-wpf.md)
