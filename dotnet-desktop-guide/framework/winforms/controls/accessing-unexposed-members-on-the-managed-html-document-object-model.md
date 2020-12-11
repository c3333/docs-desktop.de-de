---
title: Zugreifen auf nicht verfügbar gemachte Member des verwalteten HTML-Dokumentobjektmodells
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- unexposed members
- managed HTML DOM [Windows Forms], accessing unexposed members
ms.assetid: 762295bd-2355-4aa7-b43c-5bff997a33e6
ms.openlocfilehash: 525ef52ecbbc61fba787fa8286c56c638d837faf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975804"
---
# <a name="accessing-unexposed-members-on-the-managed-html-document-object-model"></a>Zugreifen auf nicht verfügbar gemachte Member des verwalteten HTML-Dokumentobjektmodells
Der verwaltete HTML-Dokumentobjektmodell (DOM) enthält eine Klasse <xref:System.Windows.Forms.HtmlElement> mit dem Namen, die die Eigenschaften, Methoden und Ereignisse verfügbar macht, die alle HTML-Elemente gemeinsam haben. Manchmal müssen Sie jedoch auf Member zugreifen, die von der verwalteten Schnittstelle nicht direkt verfügbar gemacht werden. In diesem Thema werden zwei Möglichkeiten für den Zugriff auf nicht verfügbar gemachte Member untersucht, einschließlich JScript-und VBScript-Funktionen, die in einer Webseite definiert sind.  
  
## <a name="accessing-unexposed-members-through-managed-interfaces"></a>Zugreifen auf nicht verfügbar gemachte Member über verwaltete Schnittstellen  
 <xref:System.Windows.Forms.HtmlDocument> und <xref:System.Windows.Forms.HtmlElement> stellen vier Methoden bereit, die den Zugriff auf nicht verfügbar gemachte Member ermöglichen. In der folgenden Tabelle werden die Typen und die zugehörigen Methoden aufgeführt.  
  
|Memberart|Methode(n)|  
|-----------------|-----------------|  
|Eigenschaften ( <xref:System.Windows.Forms.HtmlElement> )|<xref:System.Windows.Forms.HtmlElement.GetAttribute%2A><br /><br /> <xref:System.Windows.Forms.HtmlElement.SetAttribute%2A>|  
|Methoden|<xref:System.Windows.Forms.HtmlElement.InvokeMember%2A>|  
|Ereignisse ( <xref:System.Windows.Forms.HtmlDocument> )|<xref:System.Windows.Forms.HtmlDocument.AttachEventHandler%2A><br /><br /> <xref:System.Windows.Forms.HtmlDocument.DetachEventHandler%2A>|  
|Ereignisse ( <xref:System.Windows.Forms.HtmlElement> )|<xref:System.Windows.Forms.HtmlElement.AttachEventHandler%2A><br /><br /> <xref:System.Windows.Forms.HtmlElement.DetachEventHandler%2A>|  
|Ereignisse ( <xref:System.Windows.Forms.HtmlWindow> )|<xref:System.Windows.Forms.HtmlWindow.AttachEventHandler%2A><br /><br /> <xref:System.Windows.Forms.HtmlWindow.DetachEventHandler%2A>|  
  
 Wenn Sie diese Methoden verwenden, wird davon ausgegangen, dass Sie über ein Element des richtigen zugrunde liegenden Typs verfügen. Angenommen, Sie möchten das `Submit` -Ereignis eines `FORM` -Elements auf einer HTML-Seite überwachen, damit Sie eine Vorverarbeitung der Werte durchführen können, `FORM` bevor der Benutzer Sie an den Server übermittelt. Wenn Sie die Kontrolle über den HTML-Code haben, würden Sie im Idealfall definieren, `FORM` um ein eindeutiges Attribut zu erhalten `ID` .  
  
```html  
<HTML>  
  
    <HEAD>  
        <TITLE>Form Page</TITLE>  
    </HEAD>  
  
    <BODY>  
        <FORM ID="form1">  
             ... form fields defined here ...  
        </FORM>  
    </BODY>  
  
</HTML>  
```  
  
 Nachdem Sie diese Seite in das- <xref:System.Windows.Forms.WebBrowser> Steuerelement geladen haben, können Sie die-Methode verwenden, <xref:System.Windows.Forms.HtmlDocument.GetElementById%2A> um zur `FORM` Laufzeit mithilfe von `form1` als-Argument abzurufen.  
  
 [!code-csharp[System.Windows.Forms.HtmlElement#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.HtmlElement/CS/Form1.cs#10)]
 [!code-vb[System.Windows.Forms.HtmlElement#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.HtmlElement/VB/Form1.vb#10)]  
  
## <a name="accessing-unmanaged-interfaces"></a>Zugreifen auf nicht verwaltete Schnittstellen  
 Sie können auch auf nicht verfügbar gemachte Member im verwalteten HTML-DOM zugreifen, indem Sie die von den einzelnen DOM-Klassen verfügbar gemachten nicht verwalteten Component Object Model (com)-Schnittstellen verwenden. Dies wird empfohlen, wenn Sie mehrere Aufrufe für nicht verfügbar gemachte Member durchführen müssen, oder wenn die nicht verfügbar gemachten Member andere nicht verwaltete Schnittstellen zurückgeben, die nicht vom verwalteten HTML-DOM umschließt werden.  
  
 Die folgende Tabelle zeigt alle nicht verwalteten Schnittstellen, die über das verwaltete HTML-DOM verfügbar gemacht werden. Klicken Sie auf die einzelnen Links, um eine Erläuterung der Verwendung und beispielsweise Code zu erhalten.  
  
|type|Nicht verwaltete Schnittstelle|  
|----------|-------------------------|  
|<xref:System.Windows.Forms.HtmlDocument>|<xref:System.Windows.Forms.HtmlDocument.DomDocument%2A>|  
|<xref:System.Windows.Forms.HtmlElement>|<xref:System.Windows.Forms.HtmlElement.DomElement%2A>|  
|<xref:System.Windows.Forms.HtmlWindow>|<xref:System.Windows.Forms.HtmlWindow.DomWindow%2A>|  
|<xref:System.Windows.Forms.HtmlHistory>|<xref:System.Windows.Forms.HtmlHistory.DomHistory%2A>|  
  
 Die einfachste Möglichkeit, die COM-Schnittstellen zu verwenden, besteht darin, einen Verweis auf die nicht verwaltete HTML-DOM-Bibliothek (MSHTML.dll) von der Anwendung hinzuzufügen, obwohl dies nicht unterstützt wird. Weitere Informationen finden Sie im [Knowledge Base-Artikel 934368](https://support.microsoft.com/kb/934368).  
  
## <a name="accessing-script-functions"></a>Zugreifen auf Skriptfunktionen  
 Eine HTML-Seite kann eine oder mehrere Funktionen mithilfe einer Skriptsprache wie z. b. JScript oder VBScript definieren. Diese Funktionen werden in einer Seite auf `SCRIPT` der Seite platziert und können Bedarfs gesteuert oder als Reaktion auf ein Ereignis im Dom ausgeführt werden.  
  
 Sie können alle Skriptfunktionen, die Sie in einer HTML-Seite definieren, mithilfe der- <xref:System.Windows.Forms.HtmlDocument.InvokeScript%2A> Methode abrufen. Wenn die Skript Methode ein HTML-Element zurückgibt, können Sie eine Umwandlung verwenden, um dieses Rückgabe Ergebnis in eine zu konvertieren <xref:System.Windows.Forms.HtmlElement> . Weitere Informationen und Beispielcode finden Sie unter <xref:System.Windows.Forms.HtmlDocument.InvokeScript%2A> .  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden des verwalteten HTML-Dokumentobjektmodells](using-the-managed-html-document-object-model.md)
