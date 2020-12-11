---
title: Erstellen eines HTML-Dokument-Viewers in einer Windows Forms-App
titleSuffix: ''
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- WebBrowser control [Windows Forms], creating an HTML document viewer
- document viewers
- Windows Forms, creating document viewers
ms.assetid: 6a6338fe-f7ee-4f5e-9d8f-0465c57e9039
ms.openlocfilehash: 913bc86af034645b4b8cf3d69da4c9def58fc19c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976334"
---
# <a name="how-to-create-an-html-document-viewer-in-a-windows-forms-application"></a>Vorgehensweise: Erstellen eines HTML-Dokumentviewers in einer Windows Forms-Anwendung
Sie können das <xref:System.Windows.Forms.WebBrowser> -Steuerelement verwenden, um HTML-Dokumente anzuzeigen und zu drucken, ohne die vollständige Funktionalität eines Internet-Webbrowsers bereitzustellen. Dies ist hilfreich, wenn Sie die Formatierungsfunktionen von HTML nutzen möchten, aber nicht möchten, dass Benutzer beliebige Webseiten laden, die möglicherweise nicht vertrauenswürdige websteuer Elemente oder potenziell bösartigen Skriptcode enthalten. Möglicherweise möchten Sie die Funktionalität des Steuer Elements <xref:System.Windows.Forms.WebBrowser> auf diese Weise einschränken, um es z. b. als HTML-e-Mail-Viewer zu verwenden oder um HTML-formatierte Hilfe in der Anwendung bereitzustellen.  
  
### <a name="to-create-an-html-document-viewer"></a>So erstellen Sie einen HTML-Dokument-Viewer  
  
1. Legen Sie die- <xref:System.Windows.Forms.WebBrowser.AllowWebBrowserDrop%2A> Eigenschaft auf fest `false` , um zu verhindern, dass das <xref:System.Windows.Forms.WebBrowser> Steuerelement Dateien öffnet, die auf diesem  
  
     [!code-csharp[WebBrowserMisc#20](~/samples/snippets/csharp/VS_Snippets_Winforms/WebBrowserMisc/CS/WebBrowserMisc.cs#20)]
     [!code-vb[WebBrowserMisc#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/WebBrowserMisc/vb/WebBrowserMisc.vb#20)]  
  
2. Legen Sie die- <xref:System.Windows.Forms.WebBrowser.Url%2A> Eigenschaft auf den Speicherort der anzuzeigenden anfangs Datei fest.  
  
     [!code-csharp[WebBrowserMisc#21](~/samples/snippets/csharp/VS_Snippets_Winforms/WebBrowserMisc/CS/WebBrowserMisc.cs#21)]
     [!code-vb[WebBrowserMisc#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/WebBrowserMisc/vb/WebBrowserMisc.vb#21)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Ein <xref:System.Windows.Forms.WebBrowser>-Steuerelement namens `webBrowser1`.  
  
- Verweise auf die Assemblys `System` und `System.Windows.Forms`.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.WebBrowser>
- <xref:System.Windows.Forms.WebBrowser.AllowWebBrowserDrop%2A>
- <xref:System.Windows.Forms.WebBrowser.Url%2A>
- [Übersicht über das WebBrowser-Steuerelement](webbrowser-control-overview.md)
- [WebBrowser-Sicherheit](webbrowser-security.md)
- [Vorgehensweise: Navigieren zu einem URL mit dem WebBrowser-Steuerelement](how-to-navigate-to-a-url-with-the-webbrowser-control.md)
- [Vorgehensweise: Drucken mit einem WebBrowser-Steuerelement](how-to-print-with-a-webbrowser-control.md)
