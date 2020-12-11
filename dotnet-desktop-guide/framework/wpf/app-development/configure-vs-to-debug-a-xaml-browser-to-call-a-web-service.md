---
title: 'Gewusst wie: Konfigurieren von Visual Studio 2005 zum Debuggen einer XAML-Browseranwendung, um einen Webdienst aufzurufen'
ms.date: 03/30/2017
helpviewer_keywords:
- debugging XBAPs that call a Web service [WPF]
- debugging security exceptions for XBAPs [WPF]
- security exception for XBAPs [WPF], debugging
- configuring Visual Studio to debug XAML browser applications [WPF]
- configuring Visual Studio to debug XBAPs [WPF]
ms.assetid: fd1db082-a7bb-4c4b-9331-6ad74a0682d0
ms.openlocfilehash: d8cfae2fb47876d578c51e5f4acdfe0c31e752fe
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977720"
---
# <a name="how-to-configure-visual-studio-to-debug-a-xaml-browser-application-to-call-a-web-service"></a><span data-ttu-id="0a17d-102">Gewusst wie: Konfigurieren von Visual Studio 2005 zum Debuggen einer XAML-Browseranwendung, um einen Webdienst aufzurufen</span><span class="sxs-lookup"><span data-stu-id="0a17d-102">How to: Configure Visual Studio to Debug a XAML Browser Application to Call a Web Service</span></span>
<span data-ttu-id="0a17d-103">XAML-Browser Anwendungen (XBAPs) werden in einer teilweise vertrauenswürdigen Sicherheits Sandbox ausgeführt, die auf den Berechtigungs Satz für die Internet Zone beschränkt ist.</span><span class="sxs-lookup"><span data-stu-id="0a17d-103">XAML browser applications (XBAPs) run within a partial-trust security sandbox that is restricted to the Internet zone set of permissions.</span></span> <span data-ttu-id="0a17d-104">Dieser Berechtigungs Satz schränkt Webdienst Aufrufe nur auf Webdienste ein, die sich auf der Ursprungs Site der XBAP-Anwendung befinden.</span><span class="sxs-lookup"><span data-stu-id="0a17d-104">This permission set restricts Web service calls to only Web services that are located at the XBAP application's site of origin.</span></span> <span data-ttu-id="0a17d-105">Wenn eine XBAP aus Visual Studio 2005 deentschlbelt wird, wird Sie jedoch nicht als dieselbe Ursprungs Site wie der Webdienst betrachtet, auf den Sie verweist.</span><span class="sxs-lookup"><span data-stu-id="0a17d-105">When an XBAP is debugged from Visual Studio 2005, though, it is not considered to have the same site of origin as the Web service it references.</span></span> <span data-ttu-id="0a17d-106">Dies bewirkt, dass Sicherheits Ausnahmen ausgelöst werden, wenn die XBAP versucht, den Webdienst aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="0a17d-106">This causes security exceptions to be raised when the XBAP attempts to call the Web service.</span></span> <span data-ttu-id="0a17d-107">Ein Projekt mit einer Visual Studio 2005 XAML-Browser Anwendung (WPF) kann jedoch so konfiguriert werden, dass es dieselbe Ursprungs Site wie der Webdienst simuliert, der während des Debuggens aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0a17d-107">However, a Visual Studio 2005 XAML Browser Application (WPF) project can be configured to simulate having the same site of origin as the Web service it calls while debugging.</span></span> <span data-ttu-id="0a17d-108">Dies ermöglicht es der XBAP, den Webdienst sicher aufzurufen, ohne Sicherheits Ausnahmen zu verursachen.</span><span class="sxs-lookup"><span data-stu-id="0a17d-108">This allows the XBAP to safely call the Web service without causing security exceptions.</span></span>

## <a name="configuring-visual-studio"></a><span data-ttu-id="0a17d-109">Konfigurieren von Visual Studio 2017</span><span class="sxs-lookup"><span data-stu-id="0a17d-109">Configuring Visual Studio</span></span>
 <span data-ttu-id="0a17d-110">So konfigurieren Sie Visual Studio 2005 zum Debuggen einer XBAP, die einen Webdienst aufruft:</span><span class="sxs-lookup"><span data-stu-id="0a17d-110">To configure Visual Studio 2005 to debug an XBAP that calls a Web service:</span></span>

1. <span data-ttu-id="0a17d-111">Klicken Sie bei ausgewähltem Projekt im **Projektmappen-Explorer** im Menü **Projekt** auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="0a17d-111">With a project selected in **Solution Explorer**, on the **Project** menu, click **Properties**.</span></span>

2. <span data-ttu-id="0a17d-112">Klicken Sie im **Projekt-Designer** auf die Registerkarte **Debuggen** .</span><span class="sxs-lookup"><span data-stu-id="0a17d-112">In the **Project Designer**, click the **Debug** tab.</span></span>

3. <span data-ttu-id="0a17d-113">Wählen Sie im Abschnitt **Start Aktion** die Option **externes Programm starten** aus, und geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="0a17d-113">In the **Start Action** section, select **Start external program** and enter the following:</span></span>

     `C:\WINDOWS\System32\PresentationHost.exe`

4. <span data-ttu-id="0a17d-114">Geben Sie im Abschnitt **Start Optionen** Folgendes in das Textfeld **Befehlszeilenargumente** ein:</span><span class="sxs-lookup"><span data-stu-id="0a17d-114">In the **Start Options** section, enter the following into the **Command line arguments** text box:</span></span>

     <span data-ttu-id="0a17d-115">`-debug`  *filename*</span><span class="sxs-lookup"><span data-stu-id="0a17d-115">`-debug`  *filename*</span></span>

     <span data-ttu-id="0a17d-116">Der *Dateiname* des Parameters "-Debug" ist der **Dateiname** ". XBAP". Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="0a17d-116">The *filename* value for the **-debug** parameter is the .xbap filename; for example:</span></span>

     `-debug c:\example.xbap`

> [!NOTE]
> <span data-ttu-id="0a17d-117">Dies ist die Standardkonfiguration für Projektmappen, die mit der Projektvorlage "Visual Studio 2005 XAML-Browser Anwendung (WPF)" erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="0a17d-117">This is the default configuration for solutions that are created with the Visual Studio 2005 XAML Browser Application (WPF) project template.</span></span>

1. <span data-ttu-id="0a17d-118">Klicken Sie bei ausgewähltem Projekt im **Projektmappen-Explorer** im Menü **Projekt** auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="0a17d-118">With a project selected in **Solution Explorer**, on the **Project** menu, click **Properties**.</span></span>

2. <span data-ttu-id="0a17d-119">Klicken Sie im **Projekt-Designer** auf die Registerkarte **Debuggen** .</span><span class="sxs-lookup"><span data-stu-id="0a17d-119">In the **Project Designer**, click the **Debug** tab.</span></span>

3. <span data-ttu-id="0a17d-120">Fügen Sie im Abschnitt **Start Optionen** den folgenden Befehlszeilenparameter in das Textfeld **Befehlszeilenargumente** ein:</span><span class="sxs-lookup"><span data-stu-id="0a17d-120">In the **Start Options** section, add the following command-line parameter to the **Command line arguments** text box:</span></span>

     <span data-ttu-id="0a17d-121">`-debugSecurityZoneURL`  *URL*</span><span class="sxs-lookup"><span data-stu-id="0a17d-121">`-debugSecurityZoneURL`  *URL*</span></span>

     <span data-ttu-id="0a17d-122">Der *URL* -Wert für den **-DebugSecurityZoneURL-** Parameter ist die URL für den Speicherort, den Sie als Ursprungs Site der Anwendung simulieren möchten.</span><span class="sxs-lookup"><span data-stu-id="0a17d-122">The *URL* value for the **-debugSecurityZoneURL** parameter is the URL for the location that you want to simulate as being the site of origin of your application.</span></span>

 <span data-ttu-id="0a17d-123">Stellen Sie sich als Beispiel eine XAML-Browser Anwendung (XBAP) vor, die einen Webdienst mit der folgenden URL verwendet:</span><span class="sxs-lookup"><span data-stu-id="0a17d-123">As an example, consider a XAML browser application (XBAP) that uses a Web service with the following URL:</span></span>

 `http://services.msdn.microsoft.com/ContentServices/ContentService.asmx`

 <span data-ttu-id="0a17d-124">Die URL für den Ursprungs Standort für diesen Webdienst lautet:</span><span class="sxs-lookup"><span data-stu-id="0a17d-124">The site of origin URL for this Web service is:</span></span>

 `http://services.msdn.microsoft.com`

 <span data-ttu-id="0a17d-125">Folglich lautet der Befehlszeilenparameter Complete **-Debug securityzoneurl** und der Wert:</span><span class="sxs-lookup"><span data-stu-id="0a17d-125">Consequently, the complete **-debugSecurityZoneURL** command-line parameter and value is:</span></span>

 `-debugSecurityZoneURL http://services.msdn.microsoft.com`

## <a name="see-also"></a><span data-ttu-id="0a17d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a17d-126">See also</span></span>

- [<span data-ttu-id="0a17d-127">WPF-Host (PresentationHost.exe)</span><span class="sxs-lookup"><span data-stu-id="0a17d-127">WPF Host (PresentationHost.exe)</span></span>](wpf-host-presentationhost-exe.md)
