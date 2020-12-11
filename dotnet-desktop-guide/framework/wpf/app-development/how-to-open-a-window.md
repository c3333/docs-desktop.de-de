---
title: 'Gewusst wie: Öffnen eines Fensters'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- windows [WPF], opening
- opening windows [WPF]
ms.assetid: 6b91b2bb-fda7-491d-a72e-139dd630a5b0
ms.openlocfilehash: 9ce7ffb3f46dd869fda7893745b531bd02d18ee1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977960"
---
# <a name="how-to-open-a-window"></a>Gewusst wie: Öffnen eines Fensters
In diesem Beispiel wird gezeigt, wie ein Fenster geöffnet wird.  
  
## <a name="example"></a>Beispiel  
 Ein Fenster wird geöffnet, indem <xref:System.Windows.Window> die-Methode instanziiert und aufgerufen wird <xref:System.Windows.Window.Show%2A> . <xref:System.Windows.Window.Show%2A> Öffnet ein Fenster und wird sofort zurückgegeben, ohne darauf zu warten, dass das neue Fenster geschlossen wird. Diese Art von Fenster wird auch als nicht modalem Fenster bezeichnet und schränkt Benutzereingaben *nicht ein.*  
  
 [!code-csharp[HOWTOWindowManagementSnippets#OpenNewWindowCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/MainWindow.xaml.cs#opennewwindowcode)]
 [!code-vb[HOWTOWindowManagementSnippets#OpenNewWindowCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/mainwindow.xaml.vb#opennewwindowcode)]  
  
## <a name="net-framework-security"></a>.NET Framework-Sicherheit  
 Die Instanziierung <xref:System.Windows.Window> erfordert die Berechtigung zum Abrufen unsicherer System eigener Methoden (siehe <xref:System.Windows.Window.%23ctor%2A> ).
