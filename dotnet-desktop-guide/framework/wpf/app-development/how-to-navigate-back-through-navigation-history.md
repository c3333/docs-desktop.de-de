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
# <a name="how-to-navigate-back-through-navigation-history"></a>Gewusst wie: Navigieren zurück durch den Navigationsverlauf
In diesem Beispiel wird veranschaulicht, wie Sie zu Einträgen im Navigationsverlauf zurück navigieren.  
  
## <a name="example"></a>Beispiel  
 Code, der von Inhalten ausgeführt wird, die in einem <xref:System.Windows.Navigation.NavigationWindow> , <xref:System.Windows.Controls.Frame> mithilfe <xref:System.Windows.Navigation.NavigationService> von oder Internet Explorer gehostet werden, kann durch den Navigationsverlauf, einen Eintrag gleichzeitig, navigieren.  
  
 Wenn Sie zu einem Eintrag zurück navigieren, müssen Sie zunächst überprüfen, ob Einträge im Navigationsverlauf zurück vorhanden sind, indem Sie die **CanGoBack** -Eigenschaft überprüfen, bevor Sie einen Eintrag durch Aufrufen der **GoBack** -Methode zurück navigieren. Dies wird im folgenden Beispiel veranschaulicht:  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateBackCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/HomePage.xaml.cs#navigatebackcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateBackCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/homepage.xaml.vb#navigatebackcode)]  
  
 **CanGoBack** und **GoBack** werden von <xref:System.Windows.Navigation.NavigationWindow> , <xref:System.Windows.Controls.Frame> und implementiert <xref:System.Windows.Navigation.NavigationService> .  
  
> [!NOTE]
> Wenn Sie " **GoBack**" aufzurufen und keine Einträge im Navigationsverlauf zurück vorhanden sind, <xref:System.InvalidOperationException> wird eine ausgelöst.
