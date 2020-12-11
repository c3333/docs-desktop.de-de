---
title: 'Gewusst wie: Suchen nach einem Element anhand des Namens'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- elements [WPF], finding by name
ms.assetid: cfa7cf35-8aa2-4060-9454-872ed4af3f0e
ms.openlocfilehash: d8f5e9077400d460e2e42638a534bacc656db22f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977575"
---
# <a name="how-to-find-an-element-by-its-name"></a>Gewusst wie: Suchen nach einem Element anhand des Namens
In diesem Beispiel wird beschrieben, wie die- <xref:System.Windows.FrameworkElement.FindName%2A> Methode verwendet wird, um nach einem Element anhand seines Werts zu suchen <xref:System.Windows.FrameworkElement.Name%2A> .  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel wird die-Methode, um ein bestimmtes Element anhand seines Namens zu suchen, als Ereignishandler einer Schaltfläche geschrieben. `stackPanel` ist der <xref:System.Windows.FrameworkElement.Name%2A> des Stamms <xref:System.Windows.FrameworkElement> , der durchsucht wird, und die Beispiel Methode gibt dann visuell das gefundene Element durch umwandeln als <xref:System.Windows.Controls.TextBlock> und Ändern einer der <xref:System.Windows.Controls.TextBlock> sichtbaren [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] Eigenschaften an.  
  
 [!code-csharp[FEFindName#Find](~/samples/snippets/csharp/VS_Snippets_Wpf/FEFindName/CSharp/default.xaml.cs#find)]
 [!code-vb[FEFindName#Find](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FEFindName/VisualBasic/default.xaml.vb#find)]
