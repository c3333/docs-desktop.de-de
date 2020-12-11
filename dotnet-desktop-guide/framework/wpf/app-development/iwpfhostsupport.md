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
# <a name="iwpfhostsupport"></a><span data-ttu-id="cda5c-102">IWpfHostSupport</span><span class="sxs-lookup"><span data-stu-id="cda5c-102">IWpfHostSupport</span></span>

<span data-ttu-id="cda5c-103">Anwendungen, die [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Inhalte über PresentationHost.exe hosten, implementieren diese Schnittstelle, um einen Punkt der Integration zwischen dem Host und PresentationHost.exe bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="cda5c-103">Applications that host [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] content via PresentationHost.exe implement this interface to provide a point of integration between the host and PresentationHost.exe.</span></span>  
  
## <a name="remarks"></a><span data-ttu-id="cda5c-104">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cda5c-104">Remarks</span></span>  

 <span data-ttu-id="cda5c-105">Win32-Anwendungen (z. b. Webbrowser) können WPF-Inhalte hosten, einschließlich XAML-Browser Anwendungen (XBAPs) und losem XAML-Code.</span><span class="sxs-lookup"><span data-stu-id="cda5c-105">Win32 applications such as Web browsers can host WPF content, including XAML browser applications (XBAPs) and loose XAML.</span></span> <span data-ttu-id="cda5c-106">Zum Hosten von WPF-Inhalt erstellen Win32-Anwendungen eine Instanz des [Webbrowser-Steuer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85))Elements.</span><span class="sxs-lookup"><span data-stu-id="cda5c-106">To host WPF content, Win32 applications create an instance of the [WebBrowser control](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85)).</span></span> <span data-ttu-id="cda5c-107">Um gehostet zu werden, erstellt WPF eine Instanz von PresentationHost.exe, die den gehosteten WPF-Inhalt für den Host zur Anzeige im [Webbrowser-Steuer](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85))Element bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cda5c-107">To be hosted, WPF creates an instance of PresentationHost.exe, which provides the hosted WPF content to the host for display in the [WebBrowser control](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752040(v=vs.85)).</span></span>  
  
 <span data-ttu-id="cda5c-108">Die von aktivierte Integration `IWpfHostSupport` ermöglicht PresentationHost.exe folgende Aktionen:</span><span class="sxs-lookup"><span data-stu-id="cda5c-108">The integration enabled by `IWpfHostSupport` allows PresentationHost.exe to:</span></span>  
  
- <span data-ttu-id="cda5c-109">Ermitteln und registrieren Sie sich bei den roheingabe Geräten (Human Interface Devices), an denen die Host Anwendung interessiert ist.</span><span class="sxs-lookup"><span data-stu-id="cda5c-109">Discover and register with the raw input devices (Human Interface Devices) that the host application is interested in.</span></span>  
  
- <span data-ttu-id="cda5c-110">Empfangen von Eingabe Nachrichten von den registrierten roheingabe-Geräten und weiterleiten entsprechender Nachrichten an die Host Anwendung.</span><span class="sxs-lookup"><span data-stu-id="cda5c-110">Receive input messages from the registered raw input devices and forward appropriate messages to the host application.</span></span>  
  
- <span data-ttu-id="cda5c-111">Fragen Sie die Host Anwendung nach Benutzeroberflächen für benutzerdefinierte Fortschritte und Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="cda5c-111">Query the host application for custom progress and error user interfaces.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="cda5c-112">Diese API ist nur für die Verwendung auf dem lokalen Clientcomputer vorgesehen und wird nur zu diesem Zweck unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cda5c-112">This API is only intended and supported for use on the local client machine</span></span>  
  
## <a name="members"></a><span data-ttu-id="cda5c-113">Member</span><span class="sxs-lookup"><span data-stu-id="cda5c-113">Members</span></span>  
  
|<span data-ttu-id="cda5c-114">Member</span><span class="sxs-lookup"><span data-stu-id="cda5c-114">Member</span></span>|<span data-ttu-id="cda5c-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cda5c-115">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="cda5c-116">GetRawInputDevices</span><span class="sxs-lookup"><span data-stu-id="cda5c-116">GetRawInputDevices</span></span>](getrawinputdevices.md)|<span data-ttu-id="cda5c-117">Ermöglicht es der Datei "PresentationHost.exe", Geräte für die Eingabe von Rohdaten (Eingabegeräte, Human Interface Devices) zu erkennen, die für die Hostanwendung interessant sind.</span><span class="sxs-lookup"><span data-stu-id="cda5c-117">Allows PresentationHost.exe to discover the raw input devices (Human Interface Devices) that the host application is interested in.</span></span>|  
|[<span data-ttu-id="cda5c-118">FilterInputMessage</span><span class="sxs-lookup"><span data-stu-id="cda5c-118">FilterInputMessage</span></span>](filterinputmessage.md)|<span data-ttu-id="cda5c-119">Wird immer dann von "PresentationHost.exe" aufgerufen, wenn eine Meldung empfangen wurde, es sei denn, E_NOTIMPL wurde zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cda5c-119">Called by PresentationHost.exe whenever a message is received unless E_NOTIMPL is returned.</span></span>|  
|[<span data-ttu-id="cda5c-120">GetCustomUI</span><span class="sxs-lookup"><span data-stu-id="cda5c-120">GetCustomUI</span></span>](getcustomui.md)|<span data-ttu-id="cda5c-121">Standardmäßig stellt PresentationHost.exe einen eigenen Bereitstellungs Fortschritt und Bereitstellungs Fehler-Benutzeroberflächen bereit, die beim Bereitstellen von WPF-Inhalt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cda5c-121">By default, PresentationHost.exe provides its own deployment progress and deployment error user interfaces that are displayed when WPF content is deployed.</span></span>|
