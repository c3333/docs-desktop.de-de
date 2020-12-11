---
title: 'Gewusst wie: Navigieren zu einer Seite'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- pages [WPF], navigating to
- navigation [WPF], to page
ms.assetid: 2a556fc0-748b-417f-a58a-0d05a7afb66f
ms.openlocfilehash: 25a0dbbc609c7b6f8f2878d2068e61e492a59c7e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978167"
---
# <a name="how-to-navigate-to-a-page"></a><span data-ttu-id="44ef9-102">Gewusst wie: Navigieren zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="44ef9-102">How to: Navigate to a Page</span></span>
<span data-ttu-id="44ef9-103">In diesem Beispiel werden verschiedene Möglichkeiten veranschaulicht, mit denen eine Seite von einem aus navigiert werden kann <xref:System.Windows.Navigation.NavigationWindow> .</span><span class="sxs-lookup"><span data-stu-id="44ef9-103">This example illustrates several ways in which a page can be navigated to from a <xref:System.Windows.Navigation.NavigationWindow>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="44ef9-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="44ef9-104">Example</span></span>  
 <span data-ttu-id="44ef9-105">Eine kann <xref:System.Windows.Navigation.NavigationWindow> mit einer der folgenden Aktionen zu einer Seite navigieren:</span><span class="sxs-lookup"><span data-stu-id="44ef9-105">It is possible for a <xref:System.Windows.Navigation.NavigationWindow> to navigate to a page using one of the following:</span></span>  
  
- <span data-ttu-id="44ef9-106">Die <xref:System.Windows.Navigation.NavigationWindow.Source%2A>-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="44ef9-106">The <xref:System.Windows.Navigation.NavigationWindow.Source%2A> property.</span></span>  
  
- <span data-ttu-id="44ef9-107">Die <xref:System.Windows.Navigation.NavigationWindow.Navigate%2A> -Methode.</span><span class="sxs-lookup"><span data-stu-id="44ef9-107">The <xref:System.Windows.Navigation.NavigationWindow.Navigate%2A> method.</span></span>  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateToPageCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/MainWindow.xaml.cs#navigatetopagecode)]
 [!code-vb[HOWTONavigationSnippets#NavigateToPageCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/mainwindow.xaml.vb#navigatetopagecode)]  
  
> [!NOTE]
> <span data-ttu-id="44ef9-108">Uniform Resource Identifier (URIs) kann entweder relativ oder absolut sein.</span><span class="sxs-lookup"><span data-stu-id="44ef9-108">Uniform resource identifiers (URIs) can be either relative or absolute.</span></span> <span data-ttu-id="44ef9-109">Weitere Informationen finden Sie unter [Paket-URIs in WPF](pack-uris-in-wpf.md).</span><span class="sxs-lookup"><span data-stu-id="44ef9-109">For more information, see [Pack URIs in WPF](pack-uris-in-wpf.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="44ef9-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="44ef9-110">See also</span></span>

- <xref:System.Windows.Controls.Frame>
- <xref:System.Windows.Controls.Page>
- <xref:System.Windows.Navigation.NavigationService>
