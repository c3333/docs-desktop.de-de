---
title: IWpfHostSupport
ms.date: 03/30/2017
helpviewer_keywords:
- IWpfHostSupport interface [WPF]
ms.assetid: cc5a0281-de81-4cc1-87e4-0e46b1a811e9
ms.openlocfilehash: eb4b6a22a6f2f5de138ff3795dd32058f87cdb7a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972268"
---
# <a name="iwpfhostsupport"></a>IWpfHostSupport

Anwendungen, die [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Inhalte über PresentationHost.exe hosten, implementieren diese Schnittstelle, um einen Punkt der Integration zwischen dem Host und PresentationHost.exe bereitzustellen.  
  
## <a name="remarks"></a>Bemerkungen  

 Win32-Anwendungen (z. b. Webbrowser) können WPF-Inhalte hosten, einschließlich XAML-Browser Anwendungen (XBAPs) und losem XAML-Code. Zum Hosten von WPF-Inhalt erstellen Win32-Anwendungen eine Instanz des [Webbrowser-Steuer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85))Elements. Um gehostet zu werden, erstellt WPF eine Instanz von PresentationHost.exe, die den gehosteten WPF-Inhalt für den Host zur Anzeige im [Webbrowser-Steuer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85))Element bereitstellt.  
  
 Die von aktivierte Integration `IWpfHostSupport` ermöglicht PresentationHost.exe folgende Aktionen:  
  
- Ermitteln und registrieren Sie sich bei den roheingabe Geräten (Human Interface Devices), an denen die Host Anwendung interessiert ist.  
  
- Empfangen von Eingabe Nachrichten von den registrierten roheingabe-Geräten und weiterleiten entsprechender Nachrichten an die Host Anwendung.  
  
- Fragen Sie die Host Anwendung nach Benutzeroberflächen für benutzerdefinierte Fortschritte und Fehler ab.  
  
> [!NOTE]
> Diese API ist nur für die Verwendung auf dem lokalen Clientcomputer vorgesehen und wird nur zu diesem Zweck unterstützt.  
  
## <a name="members"></a>Member  
  
|Member|BESCHREIBUNG|  
|------------|-----------------|  
|[GetRawInputDevices](getrawinputdevices.md)|Ermöglicht es der Datei "PresentationHost.exe", Geräte für die Eingabe von Rohdaten (Eingabegeräte, Human Interface Devices) zu erkennen, die für die Hostanwendung interessant sind.|  
|[FilterInputMessage](filterinputmessage.md)|Wird immer dann von "PresentationHost.exe" aufgerufen, wenn eine Meldung empfangen wurde, es sei denn, E_NOTIMPL wurde zurückgegeben.|  
|[GetCustomUI](getcustomui.md)|Standardmäßig stellt PresentationHost.exe einen eigenen Bereitstellungs Fortschritt und Bereitstellungs Fehler-Benutzeroberflächen bereit, die beim Bereitstellen von WPF-Inhalt angezeigt werden.|
