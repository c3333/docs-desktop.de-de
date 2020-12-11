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
# <a name="how-to-open-a-dialog-box"></a>Vorgehensweise: Öffnen eines Dialog Felds
In diesem Beispiel wird gezeigt, wie ein Dialogfeld geöffnet wird.  
  
## <a name="example"></a>Beispiel  
 Ein Dialogfeld ist ein Fenster, das durch Instanziieren <xref:System.Windows.Window> und Aufrufen der- <xref:System.Windows.Window.ShowDialog%2A> Methode geöffnet wird. <xref:System.Windows.Window.ShowDialog%2A> Öffnet ein Fenster und gibt erst dann zurück, wenn das neue Dialogfeld geschlossen wurde. Diese Art von Fenster wird auch als *modales* Fenster bezeichnet und schränkt die Benutzereingabe ein.  
  
 [!code-csharp[HOWTOWindowManagementSnippets#OpenNewDialogBoxCODE](~/samples/snippets/csharp/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/CSharp/MainWindow.xaml.cs#opennewdialogboxcode)]
 [!code-vb[HOWTOWindowManagementSnippets#OpenNewDialogBoxCODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HOWTOWindowManagementSnippets/visualbasic/mainwindow.xaml.vb#opennewdialogboxcode)]  
  
## <a name="net-framework-security"></a>.NET Framework-Sicherheit  
 Der Aufruf <xref:System.Windows.Window.ShowDialog%2A> von erfordert die Berechtigung, alle Windows-und Benutzereingabe Ereignisse ohne Einschränkung zu verwenden.  
  
## <a name="see-also"></a>Siehe auch

- [Zurückgeben eines Dialogfeldergebnisses](how-to-return-a-dialog-box-result.md)
