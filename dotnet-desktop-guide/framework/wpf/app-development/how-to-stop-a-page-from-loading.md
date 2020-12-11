---
title: 'Gewusst wie: verhindern des Ladens einer Seite'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- pages [WPF], stopping from loading
- methods [WPF], Stoploading
- events [WPF], NavigationStopped
- NavigationStopped properties [WPF]
- stopping pages from loading [WPF]
- loading [WPF], stopping
ms.assetid: e2b695b0-517e-462c-8ccf-90cc8d6ba864
ms.openlocfilehash: c5694bb2cb6c618cd84bad3dc893ae3855e44892
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972280"
---
# <a name="how-to-stop-a-page-from-loading"></a><span data-ttu-id="e5e94-102">Gewusst wie: verhindern des Ladens einer Seite</span><span class="sxs-lookup"><span data-stu-id="e5e94-102">How to: Stop a Page from Loading</span></span>
<span data-ttu-id="e5e94-103">In diesem Beispiel wird gezeigt, wie die- <xref:System.Windows.Navigation.NavigationWindow.StopLoading%2A> Methode aufgerufen wird, um die Navigation zu Inhalten zu beenden, bevor Sie heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="e5e94-103">This example shows how to call the <xref:System.Windows.Navigation.NavigationWindow.StopLoading%2A> method to stop navigation to content before it has finished being downloaded.</span></span>  
  
## <a name="example"></a><span data-ttu-id="e5e94-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e5e94-104">Example</span></span>  
 <span data-ttu-id="e5e94-105"><xref:System.Windows.Navigation.NavigationWindow.StopLoading%2A> beendet den Download des angeforderten Inhalts und bewirkt, dass das <xref:System.Windows.Navigation.NavigationWindow.NavigationStopped> Ereignis ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="e5e94-105"><xref:System.Windows.Navigation.NavigationWindow.StopLoading%2A> stops the download of the requested content, and causes the <xref:System.Windows.Navigation.NavigationWindow.NavigationStopped> event to be raised.</span></span>  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateStopLoadingCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/MainWindow.xaml.cs#navigatestoploadingcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateStopLoadingCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/mainwindow.xaml.vb#navigatestoploadingcode)]
