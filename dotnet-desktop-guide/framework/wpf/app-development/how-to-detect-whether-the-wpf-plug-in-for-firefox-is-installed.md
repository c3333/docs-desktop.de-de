---
title: Erkennen, ob WPF-Plug-In für Firefox installiert ist
titleSuffix: ''
ms.date: 03/30/2017
helpviewer_keywords:
- plug-in for Firefox [WPF]
- detecting Firefox installation [WPF]
- checking for the Firefox plug-in [WPF]
- Firefox [WPF], detecting installation
- detecting whether the WPF plug-in for Firefox is installed [WPF]
ms.assetid: 5f839373-e3fb-44f1-88ad-4a0761f02189
ms.openlocfilehash: ed16f98b992f4c1a0cea3e13a0ab29d630789a67
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976800"
---
# <a name="how-to-detect-whether-the-wpf-plug-in-for-firefox-is-installed"></a><span data-ttu-id="bb37d-102">Gewusst wie: Erkennen einer Installation des WPF-Plug-Ins für Firefox</span><span class="sxs-lookup"><span data-stu-id="bb37d-102">How to: Detect Whether the WPF Plug-In for Firefox Is Installed</span></span>

<span data-ttu-id="bb37d-103">Das Windows Presentation Foundation (WPF)-Plug-in für Firefox ermöglicht, dass XAML-Browser Anwendungen (XBAPs) und lose XAML-Dateien im Mozilla Firefox-Browser ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bb37d-103">The Windows Presentation Foundation (WPF) plug-in for Firefox enables XAML browser applications (XBAPs) and loose XAML files to run in the Mozilla Firefox browser.</span></span> <span data-ttu-id="bb37d-104">Dieses Thema enthält ein in HTML und JavaScript geschriebenes Skript, mit dem Administratoren ermitteln können, ob das WPF-Plug-in für Firefox installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bb37d-104">This topic provides a script written in HTML and JavaScript that administrators can use to determine whether the WPF plug-in for Firefox is installed.</span></span>

> [!NOTE]
> <span data-ttu-id="bb37d-105">Weitere Informationen zum Installieren, bereitstellen und ermitteln der .NET Framework finden Sie unter [Installieren des .NET Framework für Entwickler](/dotnet/framework/install/guide-for-developers).</span><span class="sxs-lookup"><span data-stu-id="bb37d-105">For more information about installing, deploying, and detecting the .NET Framework, see [Install the .NET Framework for developers](/dotnet/framework/install/guide-for-developers).</span></span>

## <a name="example"></a><span data-ttu-id="bb37d-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bb37d-106">Example</span></span>

<span data-ttu-id="bb37d-107">Wenn die .NET Framework 3,5 installiert ist, wird der Client Computer mit einem WPF-Plug-in für Firefox konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="bb37d-107">When the .NET Framework 3.5 is installed, the client computer is configured with a WPF plug-in for Firefox.</span></span> <span data-ttu-id="bb37d-108">Das folgende Beispielskript überprüft das WPF-Plug-in für Firefox und zeigt dann eine entsprechende Statusmeldung an.</span><span class="sxs-lookup"><span data-stu-id="bb37d-108">The following example script checks for the WPF plug-in for Firefox and then displays an appropriate status message.</span></span>

```html
<HTML>

  <HEAD>
    <TITLE>Test for the WPF plug-in for Firefox</TITLE>
    <META HTTP-EQUIV="Content-Type" CONTENT="text/html; charset=utf-8" />
    <SCRIPT type="text/javascript">
    <!--
    function OnLoad()
    {

       // Check for the WPF plug-in for Firefox and report
       var msg = "The WPF plug-in for Firefox is ";
       var wpfPlugin = navigator.plugins["Windows Presentation Foundation"];
       if( wpfPlugin != null ) {
          document.writeln(msg + " installed.");
       }
       else {
          document.writeln(msg + " not installed. Please install or reinstall the .NET Framework 3.5.");
       }
    }
    -->
    </SCRIPT>
  </HEAD>

  <BODY onload="OnLoad()" />

</HTML>
```

<span data-ttu-id="bb37d-109">Wenn die Überprüfung auf das WPF-Plug-in für Firefox erfolgreich ist, wird die folgende Statusmeldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="bb37d-109">If the check for the WPF plug-in for Firefox is successful, the following status message is displayed:</span></span>

`The WPF plug-in for Firefox is installed.`

<span data-ttu-id="bb37d-110">Andernfalls wird die folgende Statusmeldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="bb37d-110">Otherwise, the following status message is displayed:</span></span>

`The WPF plug-in for Firefox is not installed. Please install or reinstall the .NET Framework 3.5.`

## <a name="see-also"></a><span data-ttu-id="bb37d-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb37d-111">See also</span></span>

- [<span data-ttu-id="bb37d-112">Erkennen einer .NET Framework 3.0-Installation</span><span class="sxs-lookup"><span data-stu-id="bb37d-112">Detect Whether the .NET Framework 3.0 Is Installed</span></span>](how-to-detect-whether-the-net-framework-3-0-is-installed.md)
- [<span data-ttu-id="bb37d-113">Erkennen einer .NET Framework 3.5-Installation</span><span class="sxs-lookup"><span data-stu-id="bb37d-113">Detect Whether the .NET Framework 3.5 Is Installed</span></span>](how-to-detect-whether-the-net-framework-3-5-is-installed.md)
- [<span data-ttu-id="bb37d-114">Übersicht über WPF-XAML-Browser Anwendungen</span><span class="sxs-lookup"><span data-stu-id="bb37d-114">WPF XAML Browser Applications Overview</span></span>](wpf-xaml-browser-applications-overview.md)
