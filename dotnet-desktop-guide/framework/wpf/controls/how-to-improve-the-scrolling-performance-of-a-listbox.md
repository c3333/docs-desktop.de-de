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
# <a name="how-to-improve-the-scrolling-performance-of-a-listbox"></a><span data-ttu-id="5fcb7-102">Gewusst wie: Verbessern der Bildlaufleistung eines Listenfelds</span><span class="sxs-lookup"><span data-stu-id="5fcb7-102">How to: Improve the Scrolling Performance of a ListBox</span></span>
<span data-ttu-id="5fcb7-103">Wenn eine <xref:System.Windows.Controls.ListBox> zahlreiche Elemente enthält, kann die Benutzeroberflächen Antwort langsam sein, wenn ein Benutzer <xref:System.Windows.Controls.ListBox> mit dem Mausrad oder dem Ziehpunkt einer Scrollleiste einen Bildlauf durchführt.</span><span class="sxs-lookup"><span data-stu-id="5fcb7-103">If a <xref:System.Windows.Controls.ListBox> contains many items, the user interface response can be slow when a user scrolls the <xref:System.Windows.Controls.ListBox> by using the mouse wheel or dragging the thumb of a scrollbar.</span></span> <span data-ttu-id="5fcb7-104"><xref:System.Windows.Controls.ListBox>Durch Festlegen der `VirtualizingStackPanel.VirtualizationMode` angefügten-Eigenschaft auf können Sie die Leistung des verbessern, wenn der Benutzer einen Bildlauf durchführt <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="5fcb7-104">You can improve the performance of the <xref:System.Windows.Controls.ListBox> when the user scrolls by setting the `VirtualizingStackPanel.VirtualizationMode` attached property to <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5fcb7-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5fcb7-105">Example</span></span>  
  
## <a name="description"></a><span data-ttu-id="5fcb7-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5fcb7-106">Description</span></span>  
<span data-ttu-id="5fcb7-107">Im folgenden Beispiel wird ein erstellt <xref:System.Windows.Controls.ListBox> und die `VirtualizingStackPanel.VirtualizationMode` angefügte-Eigenschaft auf festgelegt <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> , um die Leistung beim Scrollen zu verbessern</span><span class="sxs-lookup"><span data-stu-id="5fcb7-107">The following example creates a <xref:System.Windows.Controls.ListBox> and sets the `VirtualizingStackPanel.VirtualizationMode` attached property to <xref:System.Windows.Controls.VirtualizationMode.Recycling?displayProperty=nameWithType> to improve performance during scrolling.</span></span>  
  
## <a name="code"></a><span data-ttu-id="5fcb7-108">Code</span><span class="sxs-lookup"><span data-stu-id="5fcb7-108">Code</span></span>  
 [!code-xaml[RecycleItemContainerShippets#VirtualizationMode](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml#virtualizationmode)]  
  
 <span data-ttu-id="5fcb7-109">Das folgende Beispiel zeigt die Daten, die im vorherigen Beispiel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5fcb7-109">The following example shows the data that the previous example uses.</span></span>  
  
 [!code-csharp[RecycleItemContainerShippets#ListBoxData](~/samples/snippets/csharp/VS_Snippets_Wpf/RecycleItemContainerShippets/CSharp/Window1.xaml.cs#listboxdata)]
 [!code-vb[RecycleItemContainerShippets#ListBoxData](~/samples/snippets/visualbasic/VS_Snippets_Wpf/RecycleItemContainerShippets/visualbasic/window1.xaml.vb#listboxdata)]
