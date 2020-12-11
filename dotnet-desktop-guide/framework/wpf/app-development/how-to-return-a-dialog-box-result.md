---
title: 'Gewusst wie: Zurückgeben eines Dialog Feld Ergebnisses'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- dialog boxes [WPF], returning results
ms.assetid: 4c5cf286-746b-4052-934d-d80cbf8acba3
ms.openlocfilehash: 5e3670006762bcd09634b29314ecf2d05b1a44da
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977962"
---
# <a name="how-to-return-a-dialog-box-result"></a><span data-ttu-id="f0fc8-102">Gewusst wie: Zurückgeben eines Dialog Feld Ergebnisses</span><span class="sxs-lookup"><span data-stu-id="f0fc8-102">How to: Return a Dialog Box Result</span></span>
<span data-ttu-id="f0fc8-103">Dieses Beispiel zeigt, wie das Dialogfeld Ergebnis für ein Fenster abgerufen wird, das durch Aufrufen von geöffnet wird <xref:System.Windows.Window.ShowDialog%2A> .</span><span class="sxs-lookup"><span data-stu-id="f0fc8-103">This example shows how to retrieve the dialog result for a window that is opened by calling <xref:System.Windows.Window.ShowDialog%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f0fc8-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f0fc8-104">Example</span></span>  
 <span data-ttu-id="f0fc8-105">Bevor ein Dialogfeld geschlossen wird, <xref:System.Windows.Window.DialogResult%2A> sollte seine-Eigenschaft mit einem festgelegt werden, <xref:System.Nullable%601> <xref:System.Boolean> das angibt, wie der Benutzer das Dialogfeld geschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="f0fc8-105">Before a dialog box closes, its <xref:System.Windows.Window.DialogResult%2A> property should be set with a <xref:System.Nullable%601><xref:System.Boolean> that indicates how the user closed the dialog box.</span></span> <span data-ttu-id="f0fc8-106">Dieser Wert wird von zurückgegeben <xref:System.Windows.Window.ShowDialog%2A> , damit Client Code bestimmen kann, wie das Dialogfeld geschlossen wurde, und damit das Ergebnis verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="f0fc8-106">This value is returned by <xref:System.Windows.Window.ShowDialog%2A> to allow client code to determine how the dialog box was closed and, consequently, how to process the result.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f0fc8-107"><xref:System.Windows.Window.DialogResult%2A> kann nur festgelegt werden, wenn ein Fenster durch Aufrufen von geöffnet wurde <xref:System.Windows.Window.ShowDialog%2A> .</span><span class="sxs-lookup"><span data-stu-id="f0fc8-107"><xref:System.Windows.Window.DialogResult%2A> can only be set if a window was opened by calling <xref:System.Windows.Window.ShowDialog%2A>.</span></span>  
  
 [!code-csharp[HOWTOWindowManagementSnippets#GetDialogResultCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/MainWindow.xaml.cs#getdialogresultcode)]
 [!code-vb[HOWTOWindowManagementSnippets#GetDialogResultCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/mainwindow.xaml.vb#getdialogresultcode)]  
  
## <a name="net-framework-security"></a><span data-ttu-id="f0fc8-108">.NET Framework-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="f0fc8-108">.NET Framework Security</span></span>  
 <span data-ttu-id="f0fc8-109">Der Aufruf <xref:System.Windows.Window.ShowDialog%2A> von erfordert die Berechtigung, alle Windows-und Benutzereingabe Ereignisse ohne Einschränkung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0fc8-109">Calling <xref:System.Windows.Window.ShowDialog%2A> requires permission to use all windows and user input events without restriction.</span></span>
