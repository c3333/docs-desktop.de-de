---
title: 'Vorgehensweise: Unterstützen von COM-Interop durch Anzeigen eines Windows Forms mit der ShowDialog-Methode'
ms.date: 03/30/2017
helpviewer_keywords:
- COM [Windows Forms]
- Windows Forms, unmanaged
- COM interop [Windows Forms], calling methods
- ActiveX controls [Windows Forms], COM interop
- Windows Forms, interop
ms.assetid: 87aac8ad-3c04-43b3-9b0c-d0b00df9ee74
ms.openlocfilehash: a4b86616fab5603e08fe9efa1213edaa633deeb9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972400"
---
# <a name="how-to-support-com-interop-by-displaying-a-windows-form-with-the-showdialog-method"></a>Vorgehensweise: Unterstützen von COM-Interop durch Anzeigen eines Windows Forms mit der ShowDialog-Methode

Sie können Component Object Model (com)-Interoperabilitätsprobleme lösen, indem Sie Ihr Windows Form in einer .NET Framework Message-Schleife anzeigen, die mit der-Methode erstellt wird <xref:System.Windows.Forms.Application.Run%2A?displayProperty=nameWithType> .  
  
 Damit ein Formular aus einer COM-Clientanwendung heraus ordnungsgemäß funktioniert, müssen Sie es in einer Windows Forms-Nachrichtenschleife ausführen. Hierzu können Sie einen der folgenden Ansätze verwenden:  
  
- Verwenden Sie die <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> -Methode, um die Windows Form anzuzeigen.  
  
- Zeigen Sie jedes Windows Form in einem separaten Thread an. Weitere Informationen finden Sie unter [Vorgehensweise: Unterstützen von COM-Interop durch Anzeigen jedes Windows Forms in einem eigenen Thread](how-to-support-com-interop-by-displaying-each-windows-form-on-its-own-thread.md).  
  
## <a name="procedure"></a>Prozedur  

 Die Verwendung der- <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> Methode ist die einfachste Möglichkeit, ein Formular in einer .NET Framework-Nachrichten Schleife anzuzeigen, da es für alle Ansätze den geringsten Code erfordert, der implementiert werden muss.  
  
 Die <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> -Methode unterbricht die Nachrichtenschleife der nicht verwalteten Anwendung und zeigt die Form als Dialogfeld an. Da die Nachrichten Schleife der Host Anwendung angehalten wurde, erstellt die- <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> Methode eine neue .NET Framework-Nachrichten Schleife, um die Nachrichten des Formulars zu verarbeiten.  
  
 Der Nachteil der <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> -Methode ist, dass die Form als modales Dialogfeld geöffnet wird. Dieses Verhalten blockiert solange jede Benutzeroberfläche (UI) in der aufrufenden Anwendung, wie die Windows Form geöffnet ist. Wenn der Benutzer das Formular verlässt, wird die .NET Framework Nachrichten Schleife geschlossen, und die Nachrichten Schleife der früheren Anwendung wird erneut ausgeführt.  
  
 Sie können eine Klassenbibliothek in Windows Forms erstellen, die über eine Methode zum Anzeigen der Form verfügt, und die Klassenbibliothek anschließend für COM-Interop bauen. Sie können diese DLL-Datei aus Visual Basic 6.0 oder Microsoft Foundation Classes (MFC) verwenden, und Sie können in jeder dieser Umgebungen die <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> -Methode aufrufen, um die Form anzuzeigen.  
  
#### <a name="to-support-com-interop-by-displaying-a-windows-form-with-the-showdialog-method"></a>So unterstützen Sie COM-Interop durch Anzeigen einer Windows Form mit der ShowDialog-Methode  
  
- Ersetzen Sie alle Aufrufe der- <xref:System.Windows.Forms.Form.Show%2A?displayProperty=nameWithType> Methode durch Aufrufe der- <xref:System.Windows.Forms.Form.ShowDialog%2A?displayProperty=nameWithType> Methode in der .NET Framework Komponente.  
  
## <a name="see-also"></a>Siehe auch

- [Verfügbarmachen von .NET Framework-Komponenten in COM](/dotnet/framework/interop/exposing-dotnet-components-to-co)
- [Vorgehensweise: Unterstützen von COM-Interop durch das Anzeigen einzelner Windows Forms in einem eigenen Thread](how-to-support-com-interop-by-displaying-each-windows-form-on-its-own-thread.md)
- [Windows Forms und nicht verwaltete Anwendungen](windows-forms-and-unmanaged-applications.md)
