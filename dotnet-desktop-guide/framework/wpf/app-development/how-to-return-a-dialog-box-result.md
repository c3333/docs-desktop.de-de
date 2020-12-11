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
# <a name="how-to-return-a-dialog-box-result"></a>Gewusst wie: Zurückgeben eines Dialog Feld Ergebnisses
Dieses Beispiel zeigt, wie das Dialogfeld Ergebnis für ein Fenster abgerufen wird, das durch Aufrufen von geöffnet wird <xref:System.Windows.Window.ShowDialog%2A> .  
  
## <a name="example"></a>Beispiel  
 Bevor ein Dialogfeld geschlossen wird, <xref:System.Windows.Window.DialogResult%2A> sollte seine-Eigenschaft mit einem festgelegt werden, <xref:System.Nullable%601> <xref:System.Boolean> das angibt, wie der Benutzer das Dialogfeld geschlossen hat. Dieser Wert wird von zurückgegeben <xref:System.Windows.Window.ShowDialog%2A> , damit Client Code bestimmen kann, wie das Dialogfeld geschlossen wurde, und damit das Ergebnis verarbeitet wird.  
  
> [!NOTE]
> <xref:System.Windows.Window.DialogResult%2A> kann nur festgelegt werden, wenn ein Fenster durch Aufrufen von geöffnet wurde <xref:System.Windows.Window.ShowDialog%2A> .  
  
 [!code-csharp[HOWTOWindowManagementSnippets#GetDialogResultCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/MainWindow.xaml.cs#getdialogresultcode)]
 [!code-vb[HOWTOWindowManagementSnippets#GetDialogResultCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/mainwindow.xaml.vb#getdialogresultcode)]  
  
## <a name="net-framework-security"></a>.NET Framework-Sicherheit  
 Der Aufruf <xref:System.Windows.Window.ShowDialog%2A> von erfordert die Berechtigung, alle Windows-und Benutzereingabe Ereignisse ohne Einschränkung zu verwenden.
