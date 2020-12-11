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
# <a name="accessing-unexposed-members-on-the-managed-html-document-object-model"></a><span data-ttu-id="f0200-102">Zugreifen auf nicht verfügbar gemachte Member des verwalteten HTML-Dokumentobjektmodells</span><span class="sxs-lookup"><span data-stu-id="f0200-102">Accessing Unexposed Members on the Managed HTML Document Object Model</span></span>
<span data-ttu-id="f0200-103">Der verwaltete HTML-Dokumentobjektmodell (DOM) enthält eine Klasse <xref:System.Windows.Forms.HtmlElement> mit dem Namen, die die Eigenschaften, Methoden und Ereignisse verfügbar macht, die alle HTML-Elemente gemeinsam haben.</span><span class="sxs-lookup"><span data-stu-id="f0200-103">The managed HTML Document Object Model (DOM) contains a class called <xref:System.Windows.Forms.HtmlElement> that exposes the properties, methods, and events that all HTML elements have in common.</span></span> <span data-ttu-id="f0200-104">Manchmal müssen Sie jedoch auf Member zugreifen, die von der verwalteten Schnittstelle nicht direkt verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="f0200-104">Sometimes, however, you will need to access members that the managed interface does not directly expose.</span></span> <span data-ttu-id="f0200-105">In diesem Thema werden zwei Möglichkeiten für den Zugriff auf nicht verfügbar gemachte Member untersucht, einschließlich JScript-und VBScript-Funktionen, die in einer Webseite definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f0200-105">This topic examines two ways for accessing unexposed members, including JScript and VBScript functions defined inside of a Web page.</span></span>  
  
## <a name="accessing-unexposed-members-through-managed-interfaces"></a><span data-ttu-id="f0200-106">Zugreifen auf nicht verfügbar gemachte Member über verwaltete Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f0200-106">Accessing Unexposed Members through Managed Interfaces</span></span>  
 <span data-ttu-id="f0200-107"><xref:System.Windows.Forms.HtmlDocument> und <xref:System.Windows.Forms.HtmlElement> stellen vier Methoden bereit, die den Zugriff auf nicht verfügbar gemachte Member ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f0200-107"><xref:System.Windows.Forms.HtmlDocument> and <xref:System.Windows.Forms.HtmlElement> provide four methods that enable access to unexposed members.</span></span> <span data-ttu-id="f0200-108">In der folgenden Tabelle werden die Typen und die zugehörigen Methoden aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f0200-108">The following table shows the types and their corresponding methods.</span></span>  
  
|<span data-ttu-id="f0200-109">Memberart</span><span class="sxs-lookup"><span data-stu-id="f0200-109">Member Type</span></span>|<span data-ttu-id="f0200-110">Methode(n)</span><span class="sxs-lookup"><span data-stu-id="f0200-110">Method(s)</span></span>|  
|-----------------|-----------------|  
|<span data-ttu-id="f0200-111">Eigenschaften ( <xref:System.Windows.Forms.HtmlElement> )</span><span class="sxs-lookup"><span data-stu-id="f0200-111">Properties (<xref:System.Windows.Forms.HtmlElement>)</span></span>|<xref:System.Windows.Forms.HtmlElement.GetAttribute%2A><br /><br /> <xref:System.Windows.Forms.HtmlElement.SetAttribute%2A>|  
|<span data-ttu-id="f0200-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="f0200-112">Methods</span></span>|<xref:System.Windows.Forms.HtmlElement.InvokeMember%2A>|  
|<span data-ttu-id="f0200-113">Ereignisse ( <xref:System.Windows.Forms.HtmlDocument> )</span><span class="sxs-lookup"><span data-stu-id="f0200-113">Events (<xref:System.Windows.Forms.HtmlDocument>)</span></span>|<xref:System.Windows.Forms.HtmlDocument.AttachEventHandler%2A><br /><br /> <xref:System.Windows.Forms.HtmlDocument.DetachEventHandler%2A>|  
|<span data-ttu-id="f0200-114">Ereignisse ( <xref:System.Windows.Forms.HtmlElement> )</span><span class="sxs-lookup"><span data-stu-id="f0200-114">Events (<xref:System.Windows.Forms.HtmlElement>)</span></span>|<xref:System.Windows.Forms.HtmlElement.AttachEventHandler%2A><br /><br /> <xref:System.Windows.Forms.HtmlElement.DetachEventHandler%2A>|  
|<span data-ttu-id="f0200-115">Ereignisse ( <xref:System.Windows.Forms.HtmlWindow> )</span><span class="sxs-lookup"><span data-stu-id="f0200-115">Events (<xref:System.Windows.Forms.HtmlWindow>)</span></span>|<xref:System.Windows.Forms.HtmlWindow.AttachEventHandler%2A><br /><br /> <xref:System.Windows.Forms.HtmlWindow.DetachEventHandler%2A>|  
  
 <span data-ttu-id="f0200-116">Wenn Sie diese Methoden verwenden, wird davon ausgegangen, dass Sie über ein Element des richtigen zugrunde liegenden Typs verfügen.</span><span class="sxs-lookup"><span data-stu-id="f0200-116">When you use these methods, it is assumed that you have an element of the correct underlying type.</span></span> <span data-ttu-id="f0200-117">Angenommen, Sie möchten das `Submit` -Ereignis eines `FORM` -Elements auf einer HTML-Seite überwachen, damit Sie eine Vorverarbeitung der Werte durchführen können, `FORM` bevor der Benutzer Sie an den Server übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f0200-117">Suppose that you want to listen to the `Submit` event of a `FORM` element on an HTML page, so that you can perform some pre-processing on the `FORM`'s values before the user submits them to the server.</span></span> <span data-ttu-id="f0200-118">Wenn Sie die Kontrolle über den HTML-Code haben, würden Sie im Idealfall definieren, `FORM` um ein eindeutiges Attribut zu erhalten `ID` .</span><span class="sxs-lookup"><span data-stu-id="f0200-118">Ideally, if you have control over the HTML, you would define the `FORM` to have a unique `ID` attribute.</span></span>  
  
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
  
 <span data-ttu-id="f0200-119">Nachdem Sie diese Seite in das- <xref:System.Windows.Forms.WebBrowser> Steuerelement geladen haben, können Sie die-Methode verwenden, <xref:System.Windows.Forms.HtmlDocument.GetElementById%2A> um zur `FORM` Laufzeit mithilfe von `form1` als-Argument abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f0200-119">After you load this page into the <xref:System.Windows.Forms.WebBrowser> control, you can use the <xref:System.Windows.Forms.HtmlDocument.GetElementById%2A> method to retrieve the `FORM` at run time using `form1` as the argument.</span></span>  
  
 [!code-csharp[System.Windows.Forms.HtmlElement#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.HtmlElement/CS/Form1.cs#10)]
 [!code-vb[System.Windows.Forms.HtmlElement#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.HtmlElement/VB/Form1.vb#10)]  
  
## <a name="accessing-unmanaged-interfaces"></a><span data-ttu-id="f0200-120">Zugreifen auf nicht verwaltete Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f0200-120">Accessing Unmanaged Interfaces</span></span>  
 <span data-ttu-id="f0200-121">Sie können auch auf nicht verfügbar gemachte Member im verwalteten HTML-DOM zugreifen, indem Sie die von den einzelnen DOM-Klassen verfügbar gemachten nicht verwalteten Component Object Model (com)-Schnittstellen verwenden.</span><span class="sxs-lookup"><span data-stu-id="f0200-121">You can also access unexposed members on the managed HTML DOM by using the unmanaged Component Object Model (COM) interfaces exposed by each DOM class.</span></span> <span data-ttu-id="f0200-122">Dies wird empfohlen, wenn Sie mehrere Aufrufe für nicht verfügbar gemachte Member durchführen müssen, oder wenn die nicht verfügbar gemachten Member andere nicht verwaltete Schnittstellen zurückgeben, die nicht vom verwalteten HTML-DOM umschließt werden.</span><span class="sxs-lookup"><span data-stu-id="f0200-122">This is recommended if you have to make several calls against unexposed members, or if the unexposed members return other unmanaged interfaces not wrapped by the managed HTML DOM.</span></span>  
  
 <span data-ttu-id="f0200-123">Die folgende Tabelle zeigt alle nicht verwalteten Schnittstellen, die über das verwaltete HTML-DOM verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="f0200-123">The following table shows all of the unmanaged interfaces exposed through the managed HTML DOM.</span></span> <span data-ttu-id="f0200-124">Klicken Sie auf die einzelnen Links, um eine Erläuterung der Verwendung und beispielsweise Code zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="f0200-124">Click on each link for an explanation of its usage and for example code.</span></span>  
  
|<span data-ttu-id="f0200-125">type</span><span class="sxs-lookup"><span data-stu-id="f0200-125">Type</span></span>|<span data-ttu-id="f0200-126">Nicht verwaltete Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f0200-126">Unmanaged Interface</span></span>|  
|----------|-------------------------|  
|<xref:System.Windows.Forms.HtmlDocument>|<xref:System.Windows.Forms.HtmlDocument.DomDocument%2A>|  
|<xref:System.Windows.Forms.HtmlElement>|<xref:System.Windows.Forms.HtmlElement.DomElement%2A>|  
|<xref:System.Windows.Forms.HtmlWindow>|<xref:System.Windows.Forms.HtmlWindow.DomWindow%2A>|  
|<xref:System.Windows.Forms.HtmlHistory>|<xref:System.Windows.Forms.HtmlHistory.DomHistory%2A>|  
  
 <span data-ttu-id="f0200-127">Die einfachste Möglichkeit, die COM-Schnittstellen zu verwenden, besteht darin, einen Verweis auf die nicht verwaltete HTML-DOM-Bibliothek (MSHTML.dll) von der Anwendung hinzuzufügen, obwohl dies nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="f0200-127">The easiest way to use the COM interfaces is to add a reference to the unmanaged HTML DOM library (MSHTML.dll) from your application, although this is unsupported.</span></span> <span data-ttu-id="f0200-128">Weitere Informationen finden Sie im [Knowledge Base-Artikel 934368](https://support.microsoft.com/kb/934368).</span><span class="sxs-lookup"><span data-stu-id="f0200-128">For more information, see [Knowledge Base Article 934368](https://support.microsoft.com/kb/934368).</span></span>  
  
## <a name="accessing-script-functions"></a><span data-ttu-id="f0200-129">Zugreifen auf Skriptfunktionen</span><span class="sxs-lookup"><span data-stu-id="f0200-129">Accessing Script Functions</span></span>  
 <span data-ttu-id="f0200-130">Eine HTML-Seite kann eine oder mehrere Funktionen mithilfe einer Skriptsprache wie z. b. JScript oder VBScript definieren.</span><span class="sxs-lookup"><span data-stu-id="f0200-130">An HTML page can define one or more functions by using a scripting language such as JScript or VBScript.</span></span> <span data-ttu-id="f0200-131">Diese Funktionen werden in einer Seite auf `SCRIPT` der Seite platziert und können Bedarfs gesteuert oder als Reaktion auf ein Ereignis im Dom ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f0200-131">These functions are placed inside of a `SCRIPT` page in the page, and can be run on demand or in response to an event on the DOM.</span></span>  
  
 <span data-ttu-id="f0200-132">Sie können alle Skriptfunktionen, die Sie in einer HTML-Seite definieren, mithilfe der- <xref:System.Windows.Forms.HtmlDocument.InvokeScript%2A> Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="f0200-132">You can call any script functions you define in an HTML page using the <xref:System.Windows.Forms.HtmlDocument.InvokeScript%2A> method.</span></span> <span data-ttu-id="f0200-133">Wenn die Skript Methode ein HTML-Element zurückgibt, können Sie eine Umwandlung verwenden, um dieses Rückgabe Ergebnis in eine zu konvertieren <xref:System.Windows.Forms.HtmlElement> .</span><span class="sxs-lookup"><span data-stu-id="f0200-133">If the script method returns an HTML element, you can use a cast to convert this return result to an <xref:System.Windows.Forms.HtmlElement>.</span></span> <span data-ttu-id="f0200-134">Weitere Informationen und Beispielcode finden Sie unter <xref:System.Windows.Forms.HtmlDocument.InvokeScript%2A> .</span><span class="sxs-lookup"><span data-stu-id="f0200-134">For details and example code, see <xref:System.Windows.Forms.HtmlDocument.InvokeScript%2A>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f0200-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f0200-135">See also</span></span>

- [<span data-ttu-id="f0200-136">Verwenden des verwalteten HTML-Dokumentobjektmodells</span><span class="sxs-lookup"><span data-stu-id="f0200-136">Using the Managed HTML Document Object Model</span></span>](using-the-managed-html-document-object-model.md)
