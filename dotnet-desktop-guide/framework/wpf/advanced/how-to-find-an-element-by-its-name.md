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
# <a name="how-to-find-an-element-by-its-name"></a><span data-ttu-id="941a0-102">Gewusst wie: Suchen nach einem Element anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="941a0-102">How to: Find an Element by Its Name</span></span>
<span data-ttu-id="941a0-103">In diesem Beispiel wird beschrieben, wie die- <xref:System.Windows.FrameworkElement.FindName%2A> Methode verwendet wird, um nach einem Element anhand seines Werts zu suchen <xref:System.Windows.FrameworkElement.Name%2A> .</span><span class="sxs-lookup"><span data-stu-id="941a0-103">This example describes how to use the <xref:System.Windows.FrameworkElement.FindName%2A> method to find an element by its <xref:System.Windows.FrameworkElement.Name%2A> value.</span></span>  
  
## <a name="example"></a><span data-ttu-id="941a0-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="941a0-104">Example</span></span>  
 <span data-ttu-id="941a0-105">In diesem Beispiel wird die-Methode, um ein bestimmtes Element anhand seines Namens zu suchen, als Ereignishandler einer Schaltfläche geschrieben.</span><span class="sxs-lookup"><span data-stu-id="941a0-105">In this example, the method to find a particular element by its name is written as the event handler of a button.</span></span> <span data-ttu-id="941a0-106">`stackPanel` ist der <xref:System.Windows.FrameworkElement.Name%2A> des Stamms <xref:System.Windows.FrameworkElement> , der durchsucht wird, und die Beispiel Methode gibt dann visuell das gefundene Element durch umwandeln als <xref:System.Windows.Controls.TextBlock> und Ändern einer der <xref:System.Windows.Controls.TextBlock> sichtbaren [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="941a0-106">`stackPanel` is the <xref:System.Windows.FrameworkElement.Name%2A> of the root <xref:System.Windows.FrameworkElement> being searched, and the example method then visually indicates the found element by casting it as <xref:System.Windows.Controls.TextBlock> and changing one of the <xref:System.Windows.Controls.TextBlock> visible [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] properties.</span></span>  
  
 [!code-csharp[FEFindName#Find](~/samples/snippets/csharp/VS_Snippets_Wpf/FEFindName/CSharp/default.xaml.cs#find)]
 [!code-vb[FEFindName#Find](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FEFindName/VisualBasic/default.xaml.vb#find)]
