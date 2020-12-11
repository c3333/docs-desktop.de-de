---
title: 'Gewusst wie: Verbessern der Bildlaufleistung eines Listenfelds'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListBox control [WPF], reusing item containers
- ListBox control [WPF], improving scrolling performance
ms.assetid: 1e2bf8f3-c8ce-47f7-a400-a7fe11d1a848
ms.openlocfilehash: a9d1ca1d8ac2ef830984408f3052eb0ed0987c5d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977189"
---
# <a name="how-to-improve-the-scrolling-performance-of-a-listbox"></a>Gewusst wie: Verbessern der Bildlaufleistung eines Listenfelds
Wenn eine <xref:System.Windows.Controls.ListBox> zahlreiche Elemente enthält, kann die Benutzeroberflächen Antwort langsam sein, wenn ein Benutzer <xref:System.Windows.Controls.ListBox> mit dem Mausrad oder dem Ziehpunkt einer Scrollleiste einen Bildlauf durchführt. <xref:System.Windows.Controls.ListBox>Durch Festlegen der `VirtualizingStackPanel.VirtualizationMode` angefügten-Eigenschaft auf können Sie die Leistung des verbessern, wenn der Benutzer einen Bildlauf durchführt <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> .  
  
## <a name="example"></a>Beispiel  
  
## <a name="description"></a>BESCHREIBUNG  
Im folgenden Beispiel wird ein erstellt <xref:System.Windows.Controls.ListBox> und die `VirtualizingStackPanel.VirtualizationMode` angefügte-Eigenschaft auf festgelegt <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> , um die Leistung beim Scrollen zu verbessern  
  
## <a name="code"></a>Code  
 [!code-xaml[RecycleItemContainerShippets#VirtualizationMode](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml#virtualizationmode)]  
  
 Das folgende Beispiel zeigt die Daten, die im vorherigen Beispiel verwendet werden.  
  
 [!code-csharp[RecycleItemContainerShippets#ListBoxData](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml.cs#listboxdata)]
 [!code-vb[RecycleItemContainerShippets#ListBoxData](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RecycleItemContainerShippets/visualbasic/window1.xaml.vb#listboxdata)]
