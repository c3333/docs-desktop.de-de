---
title: 'Vorgehensweise: Aktualisieren einer Seite'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- pages [WPF], refreshing
- refreshing pages [WPF]
ms.assetid: 06dd1bbd-81c4-40ad-ac0d-7a5b326b1465
ms.openlocfilehash: 71a71c91384a8905413358d023531afec23f2d41
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977918"
---
# <a name="how-to-refresh-a-page"></a>Vorgehensweise: Aktualisieren einer Seite
In diesem Beispiel wird gezeigt, wie die-Methode aufgerufen wird <xref:System.Windows.Navigation.NavigationWindow.Refresh%2A> , um den aktuellen Inhalt in einem zu aktualisieren <xref:System.Windows.Navigation.NavigationWindow> .  
  
## <a name="example"></a>Beispiel  
 <xref:System.Windows.Navigation.NavigationWindow.Refresh%2A> Aktualisiert den aktuellen Inhalt in einer <xref:System.Windows.Navigation.NavigationWindow> , die aus der Quelle erneut geladen werden soll.  
  
 [!code-csharp[HOWTONavigationSnippets#NavigateRefreshCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTONavigationSnippets/CSharp/MainWindow.xaml.cs#navigaterefreshcode)]
 [!code-vb[HOWTONavigationSnippets#NavigateRefreshCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTONavigationSnippets/visualbasic/mainwindow.xaml.vb#navigaterefreshcode)]
