---
title: 'Gewusst wie: Festlegen der Höhe eines Fensters auf einer Seite'
ms.date: 03/30/2017
helpviewer_keywords:
- windows [WPF], setting height from a page
- pages [WPF], setting window height from
- height of window [WPF], setting from a page
ms.assetid: 4e4488ff-ab5c-4ee9-81a4-e1addb55c5cc
ms.openlocfilehash: c1041af88241011b51c96d7b61423344a32b25ca
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972287"
---
# <a name="how-to-set-the-height-of-a-window-from-a-page"></a><span data-ttu-id="6d6e2-102">Gewusst wie: Festlegen der Höhe eines Fensters auf einer Seite</span><span class="sxs-lookup"><span data-stu-id="6d6e2-102">How to: Set the Height of a Window from a Page</span></span>
<span data-ttu-id="6d6e2-103">In diesem Beispiel wird veranschaulicht, wie die Höhe des Fensters von einem festgelegt wird <xref:System.Windows.Controls.Page> .</span><span class="sxs-lookup"><span data-stu-id="6d6e2-103">This example illustrates how to set the height of the window from a <xref:System.Windows.Controls.Page>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="6d6e2-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6d6e2-104">Example</span></span>  
 <span data-ttu-id="6d6e2-105">Ein <xref:System.Windows.Controls.Page> kann die Höhe des Host Fensters durch Festlegen von festlegen <xref:System.Windows.Controls.Page.WindowHeight%2A> .</span><span class="sxs-lookup"><span data-stu-id="6d6e2-105">A <xref:System.Windows.Controls.Page> can set the height of its host window by setting <xref:System.Windows.Controls.Page.WindowHeight%2A>.</span></span> <span data-ttu-id="6d6e2-106">Diese Eigenschaft ermöglicht es dem <xref:System.Windows.Controls.Page> nicht, explizite Informationen über den Typ des Fensters zu haben, in dem es gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-106">This property allows the <xref:System.Windows.Controls.Page> to not have explicit knowledge of the type of window that hosts it.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="6d6e2-107">Um die Höhe eines Fensters mit festzulegen <xref:System.Windows.Controls.Page.WindowHeight%2A> , muss ein untergeordnetes Element eines <xref:System.Windows.Controls.Page> Fensters sein.</span><span class="sxs-lookup"><span data-stu-id="6d6e2-107">To set the height of a window using <xref:System.Windows.Controls.Page.WindowHeight%2A>, a <xref:System.Windows.Controls.Page> must be the child of a window.</span></span>  
  
 [!code-xaml[HOWTONavigationSnippets#SetPageWindowHeightXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/SetWindowHeightPage.xaml#setpagewindowheightxaml)]
