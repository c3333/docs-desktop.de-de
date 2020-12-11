---
title: 'Vorgehensweise: Zugreifen auf den HTML-Quellcode im verwalteten HTML-Dokumentobjektmodell'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- managed HTML DOM
- HTML [Windows Forms], accessing in Windows Forms
ms.assetid: 53db79fa-8a5e-448e-88c2-f54ace3860b6
ms.openlocfilehash: 2db3e5a16268d71d972a84d65b3f0aa37771923c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975982"
---
# <a name="how-to-access-the-html-source-in-the-managed-html-document-object-model"></a>Vorgehensweise: Zugreifen auf den HTML-Quellcode im verwalteten HTML-Dokumentobjektmodell

Die <xref:System.Windows.Forms.WebBrowser.DocumentStream%2A>-Eigenschaft und die <xref:System.Windows.Forms.WebBrowser.DocumentText%2A>-Eigenschaft des <xref:System.Windows.Forms.WebBrowser>-Steuerelements geben den HTML-Code des aktuellen Dokuments zurück, der bei der ersten Anzeige verwendet wurde. Wenn Sie jedoch die Seite mithilfe von Methoden- und Eigenschaftenaufrufen wie <xref:System.Windows.Forms.HtmlElement.AppendChild%2A> und <xref:System.Windows.Forms.HtmlElement.InnerHtml%2A> ändern, werden diese Änderungen nicht angezeigt, wenn Sie <xref:System.Windows.Forms.WebBrowser.DocumentStream%2A> und <xref:System.Windows.Forms.WebBrowser.DocumentText%2A> aufrufen. Um die aktuelle HTML-Quelle für das DOM zu erhalten, müssen Sie die <xref:System.Windows.Forms.HtmlElement.OuterHtml%2A>-Eigenschaft des HTML-Elements aufrufen.  
  
 Im folgenden Verfahren wird gezeigt, wie die dynamische Quelle abgerufen und in einem separaten Kontextmenü angezeigt wird.  
  
### <a name="retrieving-the-dynamic-source-with-the-outerhtml-property"></a>Abrufen der dynamischen Quelle mit der OuterHtml-Eigenschaft  
  
1. Erstellen Sie eine neue Windows Forms-Anwendung. Beginnen Sie mit einem einzelnen <xref:System.Windows.Forms.Form> , und nennen Sie es `Form1` .  
  
2. Hosten <xref:System.Windows.Forms.WebBrowser> Sie das Steuerelement in Ihrer Windows Forms Anwendung, und nennen Sie es `WebBrowser1` . Weitere Informationen finden Sie unter Gewusst [wie: Hinzufügen von Webbrowser Funktionen zu einer Windows Forms Anwendung](how-to-add-web-browser-capabilities-to-a-windows-forms-application.md).  
  
3. Erstellen Sie eine zweite <xref:System.Windows.Forms.Form> in der Anwendung mit dem Namen `CodeForm` .  
  
4. Fügen Sie ein <xref:System.Windows.Forms.RichTextBox> -Steuerelement hinzu, `CodeForm` und legen Sie dessen- <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft auf `Fill`  
  
5. Erstellen Sie eine öffentliche Eigenschaft für den `CodeForm` Namen `Code` .  
  
     [!code-csharp[DisplayWebBrowserCode#1](~/samples/snippets/csharp/VS_Snippets_Winforms/DisplayWebBrowserCode/CS/CodeForm.cs#1)]
     [!code-vb[DisplayWebBrowserCode#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/DisplayWebBrowserCode/VB/CodeForm.vb#1)]  
  
6. Fügen Sie ein <xref:System.Windows.Forms.Button> -Steuerelement `Button1` mit dem Namen zu hinzu <xref:System.Windows.Forms.Form> , und überwachen Sie das- <xref:System.Windows.Forms.Control.Click> Ereignis Ausführliche Informationen zu Überwachungs Ereignissen finden Sie unter [Events (Ereignisse](/dotnet/standard/events/index)).  
  
7. Fügen Sie dem <xref:System.Windows.Forms.Control.Click>-Ereignishandler den folgenden Code hinzu.  
  
     [!code-csharp[DisplayWebBrowserCode#2](~/samples/snippets/csharp/VS_Snippets_Winforms/DisplayWebBrowserCode/CS/Form1.cs#2)]
     [!code-vb[DisplayWebBrowserCode#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/DisplayWebBrowserCode/VB/Form1.vb#2)]  
  
## <a name="robust-programming"></a>Stabile Programmierung  

 Testen Sie immer zuerst den Wert von <xref:System.Windows.Forms.WebBrowser.Document%2A>, bevor Sie einen Abruf versuchen. Wenn die aktuelle Seite noch nicht vollständig geladen wurde, kann <xref:System.Windows.Forms.WebBrowser.Document%2A> oder ein bzw. mehrere untergeordnete Objekte möglicherweise nicht initialisiert werden.  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden des verwalteten HTML-Dokumentobjektmodells](using-the-managed-html-document-object-model.md)
- [Übersicht über das WebBrowser-Steuerelement](webbrowser-control-overview.md)
