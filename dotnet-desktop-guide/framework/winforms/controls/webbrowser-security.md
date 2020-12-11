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
# <a name="webbrowser-security"></a>WebBrowser-Sicherheit

Das- <xref:System.Windows.Forms.WebBrowser> Steuerelement ist nur für vollständige Vertrauenswürdigkeit konzipiert. Der im-Steuerelement angezeigte HTML-Inhalt kann von externen Webservern stammen und kann nicht verwalteten Code in Form von Skripts oder websteuer Elementen enthalten. Wenn Sie das <xref:System.Windows.Forms.WebBrowser> Steuerelement in dieser Situation verwenden, ist das Steuerelement nicht weniger sicher als Internet Explorer, aber das verwaltete <xref:System.Windows.Forms.WebBrowser> Steuerelement verhindert nicht, dass dieser nicht verwaltete Code ausgeführt wird.  
  
 Weitere Informationen zu Sicherheitsproblemen im Zusammenhang mit dem zugrunde liegenden ActiveX-Steuerelement finden Sie unter `WebBrowser` Webbrowser- [Steuer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85))Element.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.WebBrowser>
- [Übersicht über das WebBrowser-Steuerelement](webbrowser-control-overview.md)
- [WebBrowser-Steuerelement](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85))
