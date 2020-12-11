---
title: 'Gewusst wie: Abrufen des Rückgabewerts einer Seitenfunktion'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- functions [WPF], getting return values of
- page functions [WPF], getting return values of
- return values of page functions [WPF]
- getting [WPF], return values of page functions
ms.assetid: 75470af6-256c-4c46-87e7-705080723a1c
ms.openlocfilehash: 054ffe16690425e118fcac481b2a5ff63f9450f2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972288"
---
# <a name="how-to-get-the-return-value-of-a-page-function"></a><span data-ttu-id="3c0b3-102">Gewusst wie: Abrufen des Rückgabewerts einer Seitenfunktion</span><span class="sxs-lookup"><span data-stu-id="3c0b3-102">How to: Get the Return Value of a Page Function</span></span>
<span data-ttu-id="3c0b3-103">In diesem Beispiel wird gezeigt, wie das Ergebnis, das von einer Seitenfunktion zurückgegeben wird, abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3c0b3-103">This example shows how to get the result that is returned by a page function.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3c0b3-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3c0b3-104">Example</span></span>  
 <span data-ttu-id="3c0b3-105">Um das Ergebnis zu erhalten, das von einer Seiten Funktion zurückgegeben wird, müssen Sie <xref:System.Windows.Navigation.PageFunction%601.Return> die Seiten Funktion verarbeiten, die Sie aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3c0b3-105">To get the result that is returned from a page function, you need to handle <xref:System.Windows.Navigation.PageFunction%601.Return> of the page function you are calling.</span></span>  
  
 [!code-xaml[HOWTOPageFunctionSnippets#CallAPageFunctionXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/CSharp/CallingPage.xaml#callapagefunctionxaml)]  
  
 [!code-csharp[HOWTOPageFunctionSnippets#GetPageFunctionResultCODEBEHIND](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/CSharp/CallingPage.xaml.cs#getpagefunctionresultcodebehind)]
 [!code-vb[HOWTOPageFunctionSnippets#GetPageFunctionResultCODEBEHIND](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOPageFunctionSnippets/VisualBasic/CallingPage.xaml.vb#getpagefunctionresultcodebehind)]  
  
## <a name="see-also"></a><span data-ttu-id="3c0b3-106">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c0b3-106">See also</span></span>

- <xref:System.Windows.Navigation.PageFunction%601>
