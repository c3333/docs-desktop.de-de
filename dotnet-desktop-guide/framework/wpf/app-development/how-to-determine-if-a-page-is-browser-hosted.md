---
title: 'Gewusst wie: bestimmen, ob eine Seite Browser gehostet ist'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hosted pages in browser [WPF]
- pages [WPF], hosted in browser
ms.assetid: 737e0f26-8371-49b4-9579-70879e51e1aa
ms.openlocfilehash: c4cb1065807d16c1d1f5a95c8ac9c9cbe5a0fdab
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976801"
---
# <a name="how-to-determine-if-a-page-is-browser-hosted"></a><span data-ttu-id="91fee-102">Gewusst wie: bestimmen, ob eine Seite Browser gehostet ist</span><span class="sxs-lookup"><span data-stu-id="91fee-102">How to: Determine If a Page is Browser Hosted</span></span>
<span data-ttu-id="91fee-103">In diesem Beispiel wird veranschaulicht, wie ermittelt wird, ob ein <xref:System.Windows.Controls.Page> in einem Browser gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="91fee-103">This example demonstrates how to determine if a <xref:System.Windows.Controls.Page> is hosted in a browser.</span></span>  
  
## <a name="example"></a><span data-ttu-id="91fee-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="91fee-104">Example</span></span>  
 <span data-ttu-id="91fee-105">Ein <xref:System.Windows.Controls.Page> kann Host agnostisch sein und kann daher in verschiedene Arten von Hosts geladen werden, einschließlich,, oder eines <xref:System.Windows.Controls.Frame> <xref:System.Windows.Navigation.NavigationWindow> Browsers.</span><span class="sxs-lookup"><span data-stu-id="91fee-105">A <xref:System.Windows.Controls.Page> can be host agnostic and, consequently, can be loaded into several different types of hosts, including a <xref:System.Windows.Controls.Frame>, a <xref:System.Windows.Navigation.NavigationWindow>, or a browser.</span></span> <span data-ttu-id="91fee-106">Dies kann vorkommen, wenn eine Bibliotheksassembly vorhanden ist, die eine oder mehrere Seiten enthält und auf die von mehreren eigenständigen und durch suchbaren (XBAP) Host Anwendungen verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="91fee-106">This can happen when you have a library assembly that contains one or more pages, and which is referenced by multiple standalone and browsable (XAML browser application (XBAP)) host applications.</span></span>  
  
 <span data-ttu-id="91fee-107">Im folgenden Beispiel wird veranschaulicht, wie verwendet <xref:System.Windows.Interop.BrowserInteropHelper.IsBrowserHosted%2A?displayProperty=nameWithType> wird, um zu bestimmen, ob ein <xref:System.Windows.Controls.Page> in einem Browser gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="91fee-107">The following example demonstrates how to use <xref:System.Windows.Interop.BrowserInteropHelper.IsBrowserHosted%2A?displayProperty=nameWithType> to determine if a <xref:System.Windows.Controls.Page> is hosted in a browser.</span></span>  
  
 [!code-csharp[HOWTOBrowserInteropHelperSnippets#IsBrowserHostedCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOBrowserInteropHelperSnippets/CSharp/Page1.xaml.cs#isbrowserhostedcode)]
 [!code-vb[HOWTOBrowserInteropHelperSnippets#IsBrowserHostedCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOBrowserInteropHelperSnippets/visualbasic/page1.xaml.vb#isbrowserhostedcode)]  
  
## <a name="see-also"></a><span data-ttu-id="91fee-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91fee-108">See also</span></span>

- <xref:System.Windows.Controls.Frame>
- <xref:System.Windows.Controls.Page>
