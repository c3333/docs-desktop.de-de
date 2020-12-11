---
title: 'Vorgehensweise: Öffnen eines Dialog Felds'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- opening dialog boxes [WPF]
- dialog boxes [WPF], opening
ms.assetid: 6b1557d2-da98-4ef4-9f68-4089f04ab9ea
ms.openlocfilehash: 70ac31285dd22244b4bd6ad0d188d182eb6e6264
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976961"
---
# <a name="how-to-open-a-dialog-box"></a><span data-ttu-id="bbea5-102">Vorgehensweise: Öffnen eines Dialog Felds</span><span class="sxs-lookup"><span data-stu-id="bbea5-102">How to: Open a Dialog Box</span></span>
<span data-ttu-id="bbea5-103">In diesem Beispiel wird gezeigt, wie ein Dialogfeld geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="bbea5-103">This example shows how to open a dialog box.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bbea5-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bbea5-104">Example</span></span>  
 <span data-ttu-id="bbea5-105">Ein Dialogfeld ist ein Fenster, das durch Instanziieren <xref:System.Windows.Window> und Aufrufen der- <xref:System.Windows.Window.ShowDialog%2A> Methode geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="bbea5-105">A dialog box is a window that is opened by instantiating <xref:System.Windows.Window> and calling the <xref:System.Windows.Window.ShowDialog%2A> method.</span></span> <span data-ttu-id="bbea5-106"><xref:System.Windows.Window.ShowDialog%2A> Öffnet ein Fenster und gibt erst dann zurück, wenn das neue Dialogfeld geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="bbea5-106"><xref:System.Windows.Window.ShowDialog%2A> opens a window and doesn't return until the new dialog box has been closed.</span></span> <span data-ttu-id="bbea5-107">Diese Art von Fenster wird auch als *modales* Fenster bezeichnet und schränkt die Benutzereingabe ein.</span><span class="sxs-lookup"><span data-stu-id="bbea5-107">This type of window is also known as a *modal* window, and restricts user input.</span></span>  
  
 [!code-csharp[HOWTOWindowManagementSnippets#OpenNewDialogBoxCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/MainWindow.xaml.cs#opennewdialogboxcode)]
 [!code-vb[HOWTOWindowManagementSnippets#OpenNewDialogBoxCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/mainwindow.xaml.vb#opennewdialogboxcode)]  
  
## <a name="net-framework-security"></a><span data-ttu-id="bbea5-108">.NET Framework-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="bbea5-108">.NET Framework Security</span></span>  
 <span data-ttu-id="bbea5-109">Der Aufruf <xref:System.Windows.Window.ShowDialog%2A> von erfordert die Berechtigung, alle Windows-und Benutzereingabe Ereignisse ohne Einschränkung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bbea5-109">Calling <xref:System.Windows.Window.ShowDialog%2A> requires permission to use all windows and user input events without restriction.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bbea5-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbea5-110">See also</span></span>

- [<span data-ttu-id="bbea5-111">Zurückgeben eines Dialogfeldergebnisses</span><span class="sxs-lookup"><span data-stu-id="bbea5-111">Return a Dialog Box Result</span></span>](how-to-return-a-dialog-box-result.md)
