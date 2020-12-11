---
title: 'Gewusst wie: Abrufen eines ListBoxItem'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListBox controls [WPF], getting a ListBoxItem
- ListBoxItem [WPF]
ms.assetid: da877c6f-5fd8-40cb-8909-225cbfd99aa5
ms.openlocfilehash: 27a435feb4a941c77af221ab25bd63ea98b16e92
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975501"
---
# <a name="how-to-get-a-listboxitem"></a>Gewusst wie: Abrufen eines ListBoxItem
Wenn Sie ein bestimmtes <xref:System.Windows.Controls.ListBoxItem> an einem bestimmten Index in einem-Wert erhalten müssen <xref:System.Windows.Controls.ListBox> , können Sie einen verwenden <xref:System.Windows.Controls.ItemContainerGenerator> .  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel zeigt einen <xref:System.Windows.Controls.ListBox> und seine Elemente.  
  
 [!code-xaml[ListBoxItems#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ListBoxItems/CSharp/Window1.xaml#1)]  
  
 Im folgenden Beispiel wird gezeigt, wie das-Element abgerufen wird, indem der Index des Elements in der- <xref:System.Windows.Controls.ItemContainerGenerator.ContainerFromIndex%2A> Eigenschaft von angegeben wird <xref:System.Windows.Controls.ItemContainerGenerator> .  
  
 [!code-csharp[ListBoxItems#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ListBoxItems/CSharp/Window1.xaml.cs#2)]
 [!code-vb[ListBoxItems#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ListBoxItems/VisualBasic/Window1.xaml.vb#2)]  
  
 Nachdem Sie das Listenfeld Element abgerufen haben, können Sie den Inhalt des Elements anzeigen, wie im folgenden Beispiel gezeigt.  
  
 [!code-csharp[ListBoxItems#3](~/samples/snippets/csharp/VS_Snippets_Wpf/ListBoxItems/CSharp/Window1.xaml.cs#3)]
 [!code-vb[ListBoxItems#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ListBoxItems/VisualBasic/Window1.xaml.vb#3)]
