---
title: WebBrowser-Sicherheit
ms.date: 03/30/2017
helpviewer_keywords:
- WebBrowser control [Windows Forms], security
- security [Windows Forms], WebBrowser control
ms.assetid: 0968846e-48ee-485a-9797-65b5b9a622f8
ms.openlocfilehash: 3412a775cd62723bb1d7ab8548b8a89ea05ad7f6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976581"
---
# <a name="webbrowser-security"></a><span data-ttu-id="01bc4-102">WebBrowser-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="01bc4-102">WebBrowser Security</span></span>

<span data-ttu-id="01bc4-103">Das- <xref:System.Windows.Forms.WebBrowser> Steuerelement ist nur für vollständige Vertrauenswürdigkeit konzipiert.</span><span class="sxs-lookup"><span data-stu-id="01bc4-103">The <xref:System.Windows.Forms.WebBrowser> control is designed to work in full trust only.</span></span> <span data-ttu-id="01bc4-104">Der im-Steuerelement angezeigte HTML-Inhalt kann von externen Webservern stammen und kann nicht verwalteten Code in Form von Skripts oder websteuer Elementen enthalten.</span><span class="sxs-lookup"><span data-stu-id="01bc4-104">The HTML content displayed in the control can come from external Web servers and may contain unmanaged code in the form of scripts or Web controls.</span></span> <span data-ttu-id="01bc4-105">Wenn Sie das <xref:System.Windows.Forms.WebBrowser> Steuerelement in dieser Situation verwenden, ist das Steuerelement nicht weniger sicher als Internet Explorer, aber das verwaltete <xref:System.Windows.Forms.WebBrowser> Steuerelement verhindert nicht, dass dieser nicht verwaltete Code ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01bc4-105">If you use the <xref:System.Windows.Forms.WebBrowser> control in this situation, the control is no less secure than Internet Explorer would be, but the managed <xref:System.Windows.Forms.WebBrowser> control does not prevent such unmanaged code from running.</span></span>  
  
 <span data-ttu-id="01bc4-106">Weitere Informationen zu Sicherheitsproblemen im Zusammenhang mit dem zugrunde liegenden ActiveX-Steuerelement finden Sie unter `WebBrowser` Webbrowser- [Steuer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85))Element.</span><span class="sxs-lookup"><span data-stu-id="01bc4-106">For more information about security issues relating to the underlying ActiveX `WebBrowser` control, see [WebBrowser Control](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85)).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="01bc4-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01bc4-107">See also</span></span>

- <xref:System.Windows.Forms.WebBrowser>
- [<span data-ttu-id="01bc4-108">Übersicht über das WebBrowser-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="01bc4-108">WebBrowser Control Overview</span></span>](webbrowser-control-overview.md)
- <span data-ttu-id="01bc4-109">[WebBrowser-Steuerelement](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="01bc4-109">[WebBrowser Control](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85))</span></span>
