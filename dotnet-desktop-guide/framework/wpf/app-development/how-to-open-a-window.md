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
# <a name="how-to-open-a-window"></a><span data-ttu-id="c1077-102">Gewusst wie: Öffnen eines Fensters</span><span class="sxs-lookup"><span data-stu-id="c1077-102">How to: Open a Window</span></span>
<span data-ttu-id="c1077-103">In diesem Beispiel wird gezeigt, wie ein Fenster geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="c1077-103">This example shows how to open a window.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c1077-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c1077-104">Example</span></span>  
 <span data-ttu-id="c1077-105">Ein Fenster wird geöffnet, indem <xref:System.Windows.Window> die-Methode instanziiert und aufgerufen wird <xref:System.Windows.Window.Show%2A> .</span><span class="sxs-lookup"><span data-stu-id="c1077-105">A window is opened by instantiating <xref:System.Windows.Window> and calling the <xref:System.Windows.Window.Show%2A> method.</span></span> <span data-ttu-id="c1077-106"><xref:System.Windows.Window.Show%2A> Öffnet ein Fenster und wird sofort zurückgegeben, ohne darauf zu warten, dass das neue Fenster geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="c1077-106"><xref:System.Windows.Window.Show%2A> opens a window and returns immediately without waiting for the new window to close.</span></span> <span data-ttu-id="c1077-107">Diese Art von Fenster wird auch als nicht modalem Fenster bezeichnet und schränkt Benutzereingaben *nicht ein.*</span><span class="sxs-lookup"><span data-stu-id="c1077-107">This type of window is also known as a *modeless* window, and doesn't restrict user input.</span></span>  
  
 [!code-csharp[HOWTOWindowManagementSnippets#OpenNewWindowCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/MainWindow.xaml.cs#opennewwindowcode)]
 [!code-vb[HOWTOWindowManagementSnippets#OpenNewWindowCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/mainwindow.xaml.vb#opennewwindowcode)]  
  
## <a name="net-framework-security"></a><span data-ttu-id="c1077-108">.NET Framework-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="c1077-108">.NET Framework Security</span></span>  
 <span data-ttu-id="c1077-109">Die Instanziierung <xref:System.Windows.Window> erfordert die Berechtigung zum Abrufen unsicherer System eigener Methoden (siehe <xref:System.Windows.Window.%23ctor%2A> ).</span><span class="sxs-lookup"><span data-stu-id="c1077-109">Instantiating <xref:System.Windows.Window> requires permission to call unsafe native methods (see <xref:System.Windows.Window.%23ctor%2A>).</span></span>
