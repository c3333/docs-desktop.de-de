---
title: 'Gewusst wie: Suchen des Quellelements in einem Ereignishandler'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- source element in event handlers [WPF]
- event handlers [WPF], finding source element in
ms.assetid: 85f71c5a-b714-4c65-9711-7d905c2bbe98
ms.openlocfilehash: 9a49878c9ad8313903df4506796998fd43e2e749
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977574"
---
# <a name="how-to-find-the-source-element-in-an-event-handler"></a>Gewusst wie: Suchen des Quellelements in einem Ereignishandler
Dieses Beispiel zeigt, wie Sie das Quell Element in einem Ereignishandler suchen.  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt einen- <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Ereignishandler, der in einer Code Behind-Datei deklariert ist. Wenn ein Benutzer auf die Schaltfläche klickt, an die der Handler angefügt ist, ändert der Handler einen Eigenschafts Wert. Der Handlercode verwendet die- <xref:System.Windows.RoutedEventArgs.Source%2A> Eigenschaft der Routing Ereignisdaten, die in den Ereignis Argumenten gemeldet werden, um den- <xref:System.Windows.FrameworkElement.Width%2A> Eigenschafts Wert für das-Element zu ändern <xref:System.Windows.RoutedEventArgs.Source%2A> .  
  
 [!code-xaml[RoutedEventSource#XAMLHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventSource/CSharp/default.xaml#xamlhandler)]  
  
 [!code-csharp[RoutedEventSource#Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/RoutedEventSource/CSharp/default.xaml.cs#handler)]
 [!code-vb[RoutedEventSource#Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RoutedEventSource/VisualBasic/default.xaml.vb#handler)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.RoutedEventArgs>
- [Übersicht über Routingereignisse](routed-events-overview.md)
- [Artikel zu Vorgehensweisen](events-how-to-topics.md)
