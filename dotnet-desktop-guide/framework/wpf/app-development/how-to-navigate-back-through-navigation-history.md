---
title: 'Gewusst wie: Navigieren zurück durch den Navigationsverlauf'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- history [WPF], navigating back
- navigation [WPF], through navigation history (back)
ms.assetid: 9343234b-d864-441d-b8a7-d895cba80a87
ms.openlocfilehash: 53b32e145390d7052262042c7a793699c163b373
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977391"
---
# <a name="how-to-navigate-back-through-navigation-history"></a><span data-ttu-id="9f7b1-102">Gewusst wie: Navigieren zurück durch den Navigationsverlauf</span><span class="sxs-lookup"><span data-stu-id="9f7b1-102">How to: Navigate Back Through Navigation History</span></span>
<span data-ttu-id="9f7b1-103">In diesem Beispiel wird veranschaulicht, wie Sie zu Einträgen im Navigationsverlauf zurück navigieren.</span><span class="sxs-lookup"><span data-stu-id="9f7b1-103">This example illustrates how to navigate to entries in back navigation history.</span></span>  
  
## <a name="example"></a><span data-ttu-id="9f7b1-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9f7b1-104">Example</span></span>  
 <span data-ttu-id="9f7b1-105">Code, der von Inhalten ausgeführt wird, die in einem <xref:System.Windows.Navigation.NavigationWindow> , <xref:System.Windows.Controls.Frame> mithilfe <xref:System.Windows.Navigation.NavigationService> von oder Internet Explorer gehostet werden, kann durch den Navigationsverlauf, einen Eintrag gleichzeitig, navigieren.</span><span class="sxs-lookup"><span data-stu-id="9f7b1-105">Code that is running from content that is hosted in a <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame> using <xref:System.Windows.Navigation.NavigationService>, or Internet Explorer can navigate back through navigation history, one entry at a time.</span></span>  
  
 <span data-ttu-id="9f7b1-106">Wenn Sie zu einem Eintrag zurück navigieren, müssen Sie zunächst überprüfen, ob Einträge im Navigationsverlauf zurück vorhanden sind, indem Sie die **CanGoBack** -Eigenschaft überprüfen, bevor Sie einen Eintrag durch Aufrufen der **GoBack** -Methode zurück navigieren.</span><span class="sxs-lookup"><span data-stu-id="9f7b1-106">Navigating back one entry requires first checking that there are entries in back navigation history, by inspecting the **CanGoBack** property, before navigating back one entry, by calling the **GoBack** method.</span></span> <span data-ttu-id="9f7b1-107">Dies wird im folgenden Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="9f7b1-107">This is illustrated in the following example:</span></span>  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateBackCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigatebackcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateBackCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigatebackcode)]  
  
 <span data-ttu-id="9f7b1-108">**CanGoBack** und **GoBack** werden von <xref:System.Windows.Navigation.NavigationWindow> , <xref:System.Windows.Controls.Frame> und implementiert <xref:System.Windows.Navigation.NavigationService> .</span><span class="sxs-lookup"><span data-stu-id="9f7b1-108">**CanGoBack** and **GoBack** are implemented by <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame>, and <xref:System.Windows.Navigation.NavigationService>.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="9f7b1-109">Wenn Sie " **GoBack**" aufzurufen und keine Einträge im Navigationsverlauf zurück vorhanden sind, <xref:System.InvalidOperationException> wird eine ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="9f7b1-109">If you call **GoBack**, and there are no entries in back navigation history, an <xref:System.InvalidOperationException> is raised.</span></span>
