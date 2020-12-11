---
title: 'Gewusst wie: Vorwärts- oder Rückwärtsnavigation mit dem Navigationsverlauf'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- history [WPF], navigating forward
- navigation [WPF], through navigation history (forward)
ms.assetid: 5939d574-5f53-469e-85f5-1f2b13607caa
ms.openlocfilehash: 76a78debdce14123cc465ac9abf4db906fe0a2df
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977390"
---
# <a name="how-to-navigate-forward-or-back-through-navigation-history"></a><span data-ttu-id="60d65-102">Gewusst wie: Vorwärts- oder Rückwärtsnavigation mit dem Navigationsverlauf</span><span class="sxs-lookup"><span data-stu-id="60d65-102">How to: Navigate Forward or Back Through Navigation History</span></span>
<span data-ttu-id="60d65-103">In diesem Beispiel wird veranschaulicht, wie vorwärts oder zurück zu Einträgen im Navigationsverlauf navigiert wird.</span><span class="sxs-lookup"><span data-stu-id="60d65-103">This example illustrates how to navigate forward or back to entries in navigation history.</span></span>  
  
## <a name="example"></a><span data-ttu-id="60d65-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="60d65-104">Example</span></span>  
 <span data-ttu-id="60d65-105">Code, der aus dem Inhalt der folgenden Hosts ausgeführt wird, kann vorwärts oder rückwärts durch den Navigationsverlauf navigieren, jeweils ein Eintrag.</span><span class="sxs-lookup"><span data-stu-id="60d65-105">Code that runs from content in the following hosts can navigate forward or back through navigation history, one entry at a time.</span></span>  
  
- <span data-ttu-id="60d65-106"><xref:System.Windows.Navigation.NavigationWindow> genutzt <xref:System.Windows.Navigation.NavigationService></span><span class="sxs-lookup"><span data-stu-id="60d65-106"><xref:System.Windows.Navigation.NavigationWindow> using <xref:System.Windows.Navigation.NavigationService></span></span>  
  
- <span data-ttu-id="60d65-107"><xref:System.Windows.Controls.Frame> genutzt <xref:System.Windows.Navigation.NavigationService></span><span class="sxs-lookup"><span data-stu-id="60d65-107"><xref:System.Windows.Controls.Frame> using <xref:System.Windows.Navigation.NavigationService></span></span>  
  
- <span data-ttu-id="60d65-108">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="60d65-108">Internet Explorer</span></span>  
  
 <span data-ttu-id="60d65-109">Bevor Sie einen Eintrag vorwärts navigieren können, müssen Sie zunächst überprüfen, ob im vorwärts Navigationsverlauf Einträge vorhanden sind, indem Sie die **CanGoForward** -Eigenschaft überprüfen.</span><span class="sxs-lookup"><span data-stu-id="60d65-109">Before you can navigate forward one entry, you must first check that there are entries in forward navigation history by inspecting the **CanGoForward** property.</span></span> <span data-ttu-id="60d65-110">Um einen Eintrag vorwärts zu navigieren, rufen Sie die **GoForward** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="60d65-110">To navigate forward one entry, you call the **GoForward** method.</span></span> <span data-ttu-id="60d65-111">Dies wird im folgenden Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="60d65-111">This is illustrated in the following example:</span></span>  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateForwardCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigateforwardcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateForwardCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigateforwardcode)]  
  
 <span data-ttu-id="60d65-112">Bevor Sie zu einem Eintrag zurück navigieren können, müssen Sie zunächst überprüfen, ob im Navigationsverlauf zurück Einträge vorhanden sind, indem Sie die Eigenschaft **CanGoBack** überprüfen.</span><span class="sxs-lookup"><span data-stu-id="60d65-112">Before you can navigate back one entry, you must first check that there are entries in back navigation history by inspecting the **CanGoBack** property.</span></span> <span data-ttu-id="60d65-113">Um zurück zu einem Eintrag zu navigieren, rufen Sie die **GoBack** -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="60d65-113">To navigate back one entry, you call the **GoBack** method.</span></span> <span data-ttu-id="60d65-114">Dies wird im folgenden Beispiel veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="60d65-114">This is illustrated in the following example:</span></span>  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateBackCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigatebackcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateBackCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigatebackcode)]  
  
 <span data-ttu-id="60d65-115">" **CanGoForward**", " **GoForward**", " **CanGoBack**" und " **GoBack** " werden von <xref:System.Windows.Navigation.NavigationWindow> , <xref:System.Windows.Controls.Frame> und implementiert <xref:System.Windows.Navigation.NavigationService> .</span><span class="sxs-lookup"><span data-stu-id="60d65-115">**CanGoForward**, **GoForward**, **CanGoBack**, and **GoBack** are implemented by <xref:System.Windows.Navigation.NavigationWindow>, <xref:System.Windows.Controls.Frame>, and <xref:System.Windows.Navigation.NavigationService>.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="60d65-116">Wenn Sie " **GoForward**" und im Navigationsverlauf "Vorwärts" keine Einträge vorhanden sind oder wenn Sie " **GoBack**" aufgerufen haben und keine Einträge im Navigationsverlauf zurück vorhanden sind, wird eine ausgelöst <xref:System.InvalidOperationException> .</span><span class="sxs-lookup"><span data-stu-id="60d65-116">If you call **GoForward**, and there are no entries in forward navigation history, or if you call **GoBack**, and there are no entries in back navigation history, an <xref:System.InvalidOperationException> is thrown.</span></span>
