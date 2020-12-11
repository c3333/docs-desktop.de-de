---
title: Sicherheit
ms.date: 03/30/2017
helpviewer_keywords:
- designer access security [Windows Forms]
- permissions [Windows Forms], Windows Forms
- Windows Forms, security
- security [Windows Forms]
- access control [Windows Forms], Windows Forms
- security policy [Windows Forms], Windows Forms
ms.assetid: 932d438a-5285-46d8-a958-8c93d0ad6cae
ms.openlocfilehash: 2ead74987769649e8defd69ceb929ca685baa51e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974699"
---
# <a name="windows-forms-security"></a><span data-ttu-id="dc441-102">Sicherheit in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="dc441-102">Windows Forms Security</span></span>

<span data-ttu-id="dc441-103">Windows Forms verfügt über ein Code basiertes Sicherheitsmodell (Sicherheitsstufen werden für Code festgelegt, unabhängig davon, welcher Benutzer den Code ausführen muss).</span><span class="sxs-lookup"><span data-stu-id="dc441-103">Windows Forms features a security model that is code-based (security levels are set for code, regardless of the user running the code).</span></span> <span data-ttu-id="dc441-104">Dies gilt zusätzlich zu allen Sicherheits Schemas, die möglicherweise bereits auf Ihrem Computersystem vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="dc441-104">This is in addition to any security schemas that may be in place already on your computer system.</span></span> <span data-ttu-id="dc441-105">Diese können die im Browser (z. b. die zonenbasierte Sicherheit in Internet Explorer) oder das Betriebssystem (z. b. die auf Anmelde Informationen basierende Sicherheit von Windows NT) enthalten.</span><span class="sxs-lookup"><span data-stu-id="dc441-105">These can include those in the browser (such as the zone-based security available in Internet Explorer) or the operating system (such as the credential-based security of Windows NT).</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="dc441-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="dc441-106">In This Section</span></span>  

 [<span data-ttu-id="dc441-107">Übersicht über die Sicherheit in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="dc441-107">Security in Windows Forms Overview</span></span>](security-in-windows-forms-overview.md)  
 <span data-ttu-id="dc441-108">Erläutert kurz das .NET Framework Sicherheitsmodell und die grundlegenden Schritte, die erforderlich sind, um sicherzustellen, dass die Windows Forms in Ihrer Anwendung sicher sind.</span><span class="sxs-lookup"><span data-stu-id="dc441-108">Briefly explains the .NET Framework security model and the basic steps necessary to ensure the Windows Forms in your application are secure.</span></span>  
  
 [<span data-ttu-id="dc441-109">Mehr Sicherheit beim Datei- und Datenzugriff in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="dc441-109">More Secure File and Data Access in Windows Forms</span></span>](more-secure-file-and-data-access-in-windows-forms.md)  
 <span data-ttu-id="dc441-110">Beschreibt, wie in einer teilweise vertrauenswürdigen Umgebung auf Dateien und Daten zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="dc441-110">Describes how to access files and data in a semi-trusted environment.</span></span>  
  
 [<span data-ttu-id="dc441-111">Mehr Sicherheit beim Drucken in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="dc441-111">More Secure Printing in Windows Forms</span></span>](more-secure-printing-in-windows-forms.md)  
 <span data-ttu-id="dc441-112">Hier wird beschrieben, wie Sie in einer teilweise vertrauenswürdigen Umgebung auf Druck Features zugreifen.</span><span class="sxs-lookup"><span data-stu-id="dc441-112">Describes how to access printing features in a semi-trusted environment.</span></span>  
  
 [<span data-ttu-id="dc441-113">Weitere Überlegungen zur Sicherheit in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="dc441-113">Additional Security Considerations in Windows Forms</span></span>](additional-security-considerations-in-windows-forms.md)  
 <span data-ttu-id="dc441-114">Beschreibt das Ausführen von Fenster Manipulationen, das Verwenden der Zwischenablage und das Aufrufen von nicht verwaltetem Code in einer teilweise vertrauenswürdigen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="dc441-114">Describes performing window manipulation, using the Clipboard, and making calls to unmanaged code in a semi-trusted environment.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="dc441-115">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="dc441-115">Related Sections</span></span>  

 <span data-ttu-id="dc441-116">[Standard Sicherheitsrichtlinie](/previous-versions/dotnet/netframework-4.0/03kwzyfc(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="dc441-116">[Default Security Policy](/previous-versions/dotnet/netframework-4.0/03kwzyfc(v=vs.100))</span></span>  
 <span data-ttu-id="dc441-117">Listet die Standard Berechtigungen auf, die in den Berechtigungs Sätzen Full Trust, local Intranet und Internet erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="dc441-117">Lists the default permissions granted in the Full Trust, Local Intranet, and Internet permission sets.</span></span>  
  
 <span data-ttu-id="dc441-118">[Allgemeine Verwaltung von Sicherheitsrichtlinien](/previous-versions/dotnet/netframework-4.0/ed5htz45(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="dc441-118">[General Security Policy Administration](/previous-versions/dotnet/netframework-4.0/ed5htz45(v=vs.100))</span></span>  
 <span data-ttu-id="dc441-119">Enthält Informationen über die Verwaltung der .NET Framework Sicherheitsrichtlinie und die Erhöhung der Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="dc441-119">Gives information about the administering the .NET Framework security policy and elevating permissions.</span></span>  
  
 [<span data-ttu-id="dc441-120">Problematische Berechtigungen und Richtlinienverwaltung</span><span class="sxs-lookup"><span data-stu-id="dc441-120">Dangerous Permissions and Policy Administration</span></span>](/dotnet/framework/misc/dangerous-permissions-and-policy-administration)  
 <span data-ttu-id="dc441-121">Erläutert einige der The.NET Framework-Berechtigungen, die möglicherweise eine Umgehung des Sicherheitssystems ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="dc441-121">Discusses some of the.NET Framework permissions that can potentially allow the security system to be circumvented.</span></span>  
  
 [<span data-ttu-id="dc441-122">Richtlinien für das Schreiben von sicherem Code</span><span class="sxs-lookup"><span data-stu-id="dc441-122">Secure Coding Guidelines</span></span>](/dotnet/standard/security/secure-coding-guidelines)  
 <span data-ttu-id="dc441-123">Links zu Themen, in denen die bewährten Methoden zum sicheren Schreiben von Code für die .NET Framework erläutert werden.</span><span class="sxs-lookup"><span data-stu-id="dc441-123">Links to topics that explain the best practices for securely writing code against the .NET Framework.</span></span>  
  
 <span data-ttu-id="dc441-124">[Anfordern von Berechtigungen](/previous-versions/dotnet/netframework-4.0/yd267cce(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="dc441-124">[Requesting Permissions](/previous-versions/dotnet/netframework-4.0/yd267cce(v=vs.100))</span></span>  
 <span data-ttu-id="dc441-125">Erläutert die Verwendung von Attributen, um der Laufzeit mitzuteilen, welche Berechtigungen Ihr Code ausführen muss.</span><span class="sxs-lookup"><span data-stu-id="dc441-125">Discusses the use of attributes to let the runtime know what permissions your code needs to run.</span></span>  
  
 [<span data-ttu-id="dc441-126">Schlüsselbegriffe der Sicherheit</span><span class="sxs-lookup"><span data-stu-id="dc441-126">Key Security Concepts</span></span>](/dotnet/standard/security/key-security-concepts)  
 <span data-ttu-id="dc441-127">Links zu Themen, in denen die grundlegenden Aspekte der Code Sicherheit behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="dc441-127">Links to topics that cover the basic aspects of code security.</span></span>  
  
 [<span data-ttu-id="dc441-128">Grundlagen der Codezugriffssicherheit</span><span class="sxs-lookup"><span data-stu-id="dc441-128">Code Access Security Basics</span></span>](/dotnet/framework/misc/code-access-security-basics)  
 <span data-ttu-id="dc441-129">Erläutert die Grundlagen der Arbeit mit der Sicherheitsrichtlinie für die .NET Framework Laufzeit.</span><span class="sxs-lookup"><span data-stu-id="dc441-129">Discusses the basics of working with the .NET Framework run time security policy.</span></span>  
  
 <span data-ttu-id="dc441-130">[Festlegen, wann die Sicherheitsrichtlinie geändert werden soll](/previous-versions/dotnet/netframework-4.0/xky659fc(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="dc441-130">[Determining When to Modify Security Policy](/previous-versions/dotnet/netframework-4.0/xky659fc(v=vs.100))</span></span>  
 <span data-ttu-id="dc441-131">Erläutert, wie Sie ermitteln können, wann Ihre Anwendungen von der Standard Sicherheitsrichtlinie abweichen müssen.</span><span class="sxs-lookup"><span data-stu-id="dc441-131">Explains how to determine when your applications need to diverge from the default security policy.</span></span>  
  
 <span data-ttu-id="dc441-132">[Bereitstellen von Sicherheitsrichtlinien](/previous-versions/dotnet/netframework-4.0/13wcxx6y(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="dc441-132">[Deploying Security Policy](/previous-versions/dotnet/netframework-4.0/13wcxx6y(v=vs.100))</span></span>  
 <span data-ttu-id="dc441-133">Erläutert die beste Vorgehensweise zum Bereitstellen von Sicherheitsrichtlinien Änderungen.</span><span class="sxs-lookup"><span data-stu-id="dc441-133">Discusses the best manner for deploying security policy changes.</span></span>
