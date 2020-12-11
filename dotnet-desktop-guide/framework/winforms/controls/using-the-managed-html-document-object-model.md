---
title: Verwenden des verwalteten HTML-Dokumentobjektmodells
ms.date: 03/30/2017
helpviewer_keywords:
- managed HTML DOM
ms.assetid: a017dd5c-cd7b-47e4-952c-f4f54cb48409
ms.openlocfilehash: fe84cabfaabdc14c7dec6cb69653d41b4c6f6416
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977206"
---
# <a name="using-the-managed-html-document-object-model"></a><span data-ttu-id="d1c5e-102">Verwenden des verwalteten HTML-Dokumentobjektmodells</span><span class="sxs-lookup"><span data-stu-id="d1c5e-102">Using the Managed HTML Document Object Model</span></span>
<span data-ttu-id="d1c5e-103">Das verwaltete HTML-Dokument Objektmodell (DOM) stellt einen Wrapper bereit, der auf der .NET Framework für die von Internet Explorer verfügbar gemachten HTML-klassenbasiert.</span><span class="sxs-lookup"><span data-stu-id="d1c5e-103">The managed HTML document object model (DOM) provides a wrapper based on the .NET Framework for the HTML classes exposed by Internet Explorer.</span></span> <span data-ttu-id="d1c5e-104">Verwenden Sie diese Klassen, um im Steuerelement gehostete HTML-Seiten zu bearbeiten <xref:System.Windows.Forms.WebBrowser> oder um neue Seiten von Anfang an zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1c5e-104">Use these classes to manipulate HTML pages hosted in the <xref:System.Windows.Forms.WebBrowser> control, or to build new pages from the beginning.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="d1c5e-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d1c5e-105">In This Section</span></span>  
 [<span data-ttu-id="d1c5e-106">Vorgehensweise: Zugreifen auf das verwaltete HTML-Dokumentobjektmodell</span><span class="sxs-lookup"><span data-stu-id="d1c5e-106">How to: Access the Managed HTML Document Object Model</span></span>](how-to-access-the-managed-html-document-object-model.md)  
 <span data-ttu-id="d1c5e-107">Hier wird beschrieben, wie Sie eine gültige Instanz von <xref:System.Windows.Forms.HtmlDocument> entweder aus einer Windows Forms Anwendung oder einem <xref:System.Windows.Forms.UserControl> in Internet Explorer gehosteten abrufen.</span><span class="sxs-lookup"><span data-stu-id="d1c5e-107">Describes how to obtain a valid instance of <xref:System.Windows.Forms.HtmlDocument> from either a Windows Forms application or a <xref:System.Windows.Forms.UserControl> hosted in Internet Explorer.</span></span>  
  
 [<span data-ttu-id="d1c5e-108">Vorgehensweise: Zugreifen auf den HTML-Quellcode im verwalteten HTML-Dokumentobjektmodell</span><span class="sxs-lookup"><span data-stu-id="d1c5e-108">How to: Access the HTML Source in the Managed HTML Document Object Model</span></span>](how-to-access-the-html-source-in-the-managed-html-document-object-model.md)  
 <span data-ttu-id="d1c5e-109">Beschreibt, wie Sie die ursprüngliche, nicht geänderte HTML-Quelle abrufen und wie Sie die "Live"-Quelle abrufen, die den aktuellen Status des DOM widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="d1c5e-109">Describes how to obtain the original, unmodified HTML source, and how to obtain the "live" source that reflects the current state of the DOM.</span></span>  
  
 [<span data-ttu-id="d1c5e-110">Vorgehensweise: Ändern von Formaten eines Elements im verwalteten HTML-Dokumentobjektmodell</span><span class="sxs-lookup"><span data-stu-id="d1c5e-110">How to: Change Styles on an Element in the Managed HTML Document Object Model</span></span>](how-to-change-styles-on-an-element-in-the-managed-html-document-object-model.md)  
 <span data-ttu-id="d1c5e-111">Beschreibt, wie Stile bearbeitet werden, die zur Steuerung der visuellen Darstellung von Elementen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1c5e-111">Describes how to manipulate styles, which are used to control the visual display of elements.</span></span>  
  
 [<span data-ttu-id="d1c5e-112">Zugreifen auf Frames im verwalteten HTML-Dokumentobjektmodell</span><span class="sxs-lookup"><span data-stu-id="d1c5e-112">Accessing Frames in the Managed HTML Document Object Model</span></span>](accessing-frames-in-the-managed-html-document-object-model.md)  
 <span data-ttu-id="d1c5e-113">Beschreibt, was Frames und Framesets sind und wie Sie auf das DOM eines Frames zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d1c5e-113">Describes what frames and framesets are, and how to access the DOM of a frame.</span></span>  
  
 [<span data-ttu-id="d1c5e-114">Zugreifen auf nicht verfügbar gemachte Member des verwalteten HTML-Dokumentobjektmodells</span><span class="sxs-lookup"><span data-stu-id="d1c5e-114">Accessing Unexposed Members on the Managed HTML Document Object Model</span></span>](accessing-unexposed-members-on-the-managed-html-document-object-model.md)  
 <span data-ttu-id="d1c5e-115">Beschreibt, wie auf Member des zugrunde liegenden DOM zugegriffen wird, die nicht über eine verwaltete Entsprechung verfügen.</span><span class="sxs-lookup"><span data-stu-id="d1c5e-115">Describes how to access members of the underlying DOM that do not have a managed equivalent.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="d1c5e-116">Referenz</span><span class="sxs-lookup"><span data-stu-id="d1c5e-116">Reference</span></span>  
 <xref:System.Windows.Forms.HtmlDocument>  
  
 <xref:System.Windows.Forms.HtmlElement>  
  
 <xref:System.Windows.Forms.HtmlWindow>  
  
## <a name="related-sections"></a><span data-ttu-id="d1c5e-117">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="d1c5e-117">Related Sections</span></span>  
 [<span data-ttu-id="d1c5e-118">WebBrowser-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d1c5e-118">WebBrowser Control</span></span>](webbrowser-control-windows-forms.md)  
