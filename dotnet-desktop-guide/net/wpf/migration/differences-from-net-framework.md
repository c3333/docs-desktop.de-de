---
title: Unterschiede zwischen dem .NET Framework und .NET
description: In diesem Artikel werden die Unterschiede zwischen der .NET Framework-Implementierung von Windows Presentation Foundation (WPF) und .NET WPF beschrieben. Beim Migrieren einer App sollten Sie diese Inkompatibilitäten berücksichtigen.
author: adegeo
ms.date: 09/21/2019
ms.author: adegeo
ms.topic: conceptual
ms.openlocfilehash: e722faf2adb15966d62cb4a31efd60cf0d26b2a6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942140"
---
# <a name="differences-in-wpf-net"></a><span data-ttu-id="99e8e-104">Unterschiede zu WPF .NET</span><span class="sxs-lookup"><span data-stu-id="99e8e-104">Differences in WPF .NET</span></span>

<span data-ttu-id="99e8e-105">In diesem Artikel werden die Unterschiede in .NET Core und dem .NET Framework bezüglich Windows Presentation Foundation (WPF) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="99e8e-105">This article describes the differences between Windows Presentation Foundation (WPF) on .NET Core and .NET Framework.</span></span> <span data-ttu-id="99e8e-106">WPF für .NET Core ist ein [Open-Source-Framework](https://github.com/dotnet/wpf), das aus dem Quellcode des ursprünglichen WPF-Systems für das .NET Framework geforkt wurde.</span><span class="sxs-lookup"><span data-stu-id="99e8e-106">WPF for .NET Core is an [open-source framework](https://github.com/dotnet/wpf) forked from the original WPF for .NET Framework source code.</span></span>

<span data-ttu-id="99e8e-107">Einige Features des .NET Framework werden jedoch von .NET Core nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="99e8e-107">There are a few features of .NET Framework that .NET Core doesn't support.</span></span> <span data-ttu-id="99e8e-108">Weitere Informationen zu nicht unterstützten Technologien finden Sie unter [.NET Framework-Technologien, die auf .NET Core nicht verfügbar sind](/dotnet/core/porting/net-framework-tech-unavailable).</span><span class="sxs-lookup"><span data-stu-id="99e8e-108">For more information on unsupported technologies, see [.NET Framework technologies unavailable on .NET Core](/dotnet/core/porting/net-framework-tech-unavailable).</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="sdk-style-projects"></a><span data-ttu-id="99e8e-109">Projekte im SDK-Format</span><span class="sxs-lookup"><span data-stu-id="99e8e-109">SDK-style projects</span></span>

<span data-ttu-id="99e8e-110">.Net Core verwendet Projektdateien im SDK-Stil.</span><span class="sxs-lookup"><span data-stu-id="99e8e-110">.NET Core uses SDK-style project files.</span></span> <span data-ttu-id="99e8e-111">Diese Projektdateien unterscheiden sich von herkömmlichen .NET Framework-Projektdateien, die von Visual Studio verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="99e8e-111">These project files are different from the traditional .NET Framework project files managed by Visual Studio.</span></span> <span data-ttu-id="99e8e-112">Sie müssen Ihre Projekte konvertieren, wenn Sie Ihre .NET Framework-WPF-Apps zu .NET Core migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="99e8e-112">To migrate your .NET Framework WPF apps to .NET Core, you must convert your projects.</span></span> <span data-ttu-id="99e8e-113">Weitere Informationen finden Sie unter [Migrieren von WPF-Apps zu .NET Core](convert-project-from-net-framework.md).</span><span class="sxs-lookup"><span data-stu-id="99e8e-113">For more information, see [Migrate WPF apps to .NET Core 3.0](convert-project-from-net-framework.md).</span></span>

## <a name="nuget-package-references"></a><span data-ttu-id="99e8e-114">NuGet-Paketverweise</span><span class="sxs-lookup"><span data-stu-id="99e8e-114">NuGet package references</span></span>

<span data-ttu-id="99e8e-115">Wenn Ihre .NET Framework-App ihre NuGet-Abhängigkeiten in einer *packages.config*-Datei auflistet, migrieren Sie zum Format [`<PackageReference>`](/nuget/consume-packages/package-references-in-project-files):</span><span class="sxs-lookup"><span data-stu-id="99e8e-115">If your .NET Framework app lists its NuGet dependencies in a *packages.config* file, migrate to the [`<PackageReference>`](/nuget/consume-packages/package-references-in-project-files) format:</span></span>

1. <span data-ttu-id="99e8e-116">Öffnen Sie in Visual Studio den Bereich **Projektmappen-Explorer**.</span><span class="sxs-lookup"><span data-stu-id="99e8e-116">In Visual Studio, open the **Solution Explorer** pane.</span></span>
1. <span data-ttu-id="99e8e-117">Klicken Sie in Ihrem WPF-Projekt mit der rechten Maustaste auf **packages.config** >  **"packages.config" zu PackageReference migrieren**.</span><span class="sxs-lookup"><span data-stu-id="99e8e-117">In your WPF project, right-click **packages.config** > **Migrate packages.config to PackageReference**.</span></span>

![Aktualisieren auf PackageReference](media/differences-from-net-framework/package-reference-migration.png)

<span data-ttu-id="99e8e-119">Es wird ein Dialogfeld mit berechneten NuGet-Abhängigkeiten auf oberster Ebene angezeigt, und Sie werden gefragt, welche anderen NuGet-Pakete auf die oberste Ebene höher gestuft werden sollen.</span><span class="sxs-lookup"><span data-stu-id="99e8e-119">A dialog will appear showing calculated top-level NuGet dependencies and asking which other NuGet packages should be promoted to top level.</span></span> <span data-ttu-id="99e8e-120">Klicken Sie auf **OK**. Die *packages.config*-Datei wird daraufhin aus dem Projekt entfernt, und der Projektdatei werden `<PackageReference>`-Elemente hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="99e8e-120">Select **OK** and the *packages.config* file will be removed from the project and `<PackageReference>` elements will be added to the project file.</span></span>

<span data-ttu-id="99e8e-121">Wenn Ihr Projekt `<PackageReference>` verwendet, werden Pakete nicht lokal in einem *Packages*-Ordner gespeichert, sondern global.</span><span class="sxs-lookup"><span data-stu-id="99e8e-121">When your project uses `<PackageReference>`, packages aren't stored locally in a *Packages* folder, they're stored globally.</span></span> <span data-ttu-id="99e8e-122">Öffnen Sie die Projektdatei, und entfernen Sie alle `<Analyzer>`-Elemente, die auf den *Packages*-Ordner verweisen.</span><span class="sxs-lookup"><span data-stu-id="99e8e-122">Open the project file and remove any `<Analyzer>` elements that referred to the *Packages* folder.</span></span> <span data-ttu-id="99e8e-123">Diese Analysetools sind automatisch in den NuGet-Paketverweisen enthalten.</span><span class="sxs-lookup"><span data-stu-id="99e8e-123">These analyzers are automatically included with the NuGet package references.</span></span>

## <a name="code-access-security"></a><span data-ttu-id="99e8e-124">Codezugriffssicherheit</span><span class="sxs-lookup"><span data-stu-id="99e8e-124">Code Access Security</span></span>

<span data-ttu-id="99e8e-125">Die Codezugriffssicherheit (Code Access Security, CAS) wird weder von .NET Core noch von WPF für .NET Core unterstützt.</span><span class="sxs-lookup"><span data-stu-id="99e8e-125">Code Access Security (CAS) is not supported by .NET Core or WPF for .NET Core.</span></span> <span data-ttu-id="99e8e-126">Alle CAS-bezogenen Funktionen gelten als vollständig vertrauenswürdig.</span><span class="sxs-lookup"><span data-stu-id="99e8e-126">All CAS-related functionality is treated under the assumption of full-trust.</span></span> <span data-ttu-id="99e8e-127">In WPF für .NET Core wird CAS-bezogener Code entfernt.</span><span class="sxs-lookup"><span data-stu-id="99e8e-127">WPF for .NET Core removes CAS-related code.</span></span> <span data-ttu-id="99e8e-128">Die öffentliche API-Oberfläche dieser Typen ist weiterhin vorhanden. Damit wird sichergestellt, dass die Aufrufe dieser Typen erfolgreich sind.</span><span class="sxs-lookup"><span data-stu-id="99e8e-128">The public API surface of these types still exists to ensure that calls into these types succeed.</span></span>

<span data-ttu-id="99e8e-129">Öffentlich definierte CAS-bezogene Typen wurden aus den WPF-Assemblys und in die wichtigsten .NET-Bibliotheksassemblys verschoben.</span><span class="sxs-lookup"><span data-stu-id="99e8e-129">Publicly defined CAS-related types were moved out of the WPF assemblies and into the Core .NET library assemblies.</span></span> <span data-ttu-id="99e8e-130">Für die WPF-Assemblys ist die Typweiterleitung an den neuen Speicherort der verschobenen Typen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="99e8e-130">The WPF assemblies have type-forwarding set to the new location of the moved types.</span></span>

| <span data-ttu-id="99e8e-131">Quellassembly</span><span class="sxs-lookup"><span data-stu-id="99e8e-131">Source assembly</span></span> | <span data-ttu-id="99e8e-132">Zielassembly</span><span class="sxs-lookup"><span data-stu-id="99e8e-132">Target assembly</span></span> | <span data-ttu-id="99e8e-133">Typ</span><span class="sxs-lookup"><span data-stu-id="99e8e-133">Type</span></span>                |
| --------------- | --------------- | ------------------- |
| <span data-ttu-id="99e8e-134">*WindowsBase.dll*</span><span class="sxs-lookup"><span data-stu-id="99e8e-134">*WindowsBase.dll*</span></span> | <span data-ttu-id="99e8e-135">*System.Security.Permissions.dll*</span><span class="sxs-lookup"><span data-stu-id="99e8e-135">*System.Security.Permissions.dll*</span></span> | <xref:System.Security.Permissions.MediaPermission> <br /> <xref:System.Security.Permissions.MediaPermissionAttribute> <br /> <xref:System.Security.Permissions.MediaPermissionAudio> <br /> <xref:System.Security.Permissions.MediaPermissionImage> <br /> <xref:System.Security.Permissions.MediaPermissionVideo> <br /> <xref:System.Security.Permissions.WebBrowserPermission> <br /> <xref:System.Security.Permissions.WebBrowserPermissionAttribute> <br /> <xref:System.Security.Permissions.WebBrowserPermissionLevel> |
| <span data-ttu-id="99e8e-136">*System.Xaml.dll*</span><span class="sxs-lookup"><span data-stu-id="99e8e-136">*System.Xaml.dll*</span></span> | <span data-ttu-id="99e8e-137">*System.Security.Permissions.dll*</span><span class="sxs-lookup"><span data-stu-id="99e8e-137">*System.Security.Permissions.dll*</span></span> | <xref:System.Xaml.Permissions.XamlLoadPermission> |
| <span data-ttu-id="99e8e-138">*System.Xaml.dll*</span><span class="sxs-lookup"><span data-stu-id="99e8e-138">*System.Xaml.dll*</span></span> | <span data-ttu-id="99e8e-139">*System.Windows.Extension.dll*</span><span class="sxs-lookup"><span data-stu-id="99e8e-139">*System.Windows.Extension.dll*</span></span>    | <xref:System.Xaml.Permissions.XamlAccessLevel><br/> |

> [!NOTE]
> <span data-ttu-id="99e8e-140">Die Funktionalität für das Speichern und Abrufen von Informationen über die folgenden Eigenschaften wurde im `XamlAccessLevel`-Typ beibehalten, um die Probleme bei der Portierung so gering wie möglich zu halten.</span><span class="sxs-lookup"><span data-stu-id="99e8e-140">In order to minimize porting friction, the functionality for storing and retrieving information related to the following properties was retained in the `XamlAccessLevel` type.</span></span>
>
> - `PrivateAccessToTypeName`
> - `AssemblyNameString`

## <a name="next-steps"></a><span data-ttu-id="99e8e-141">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="99e8e-141">Next steps</span></span>

- [<span data-ttu-id="99e8e-142">Migrieren von WPF-Apps zu .NET Core</span><span class="sxs-lookup"><span data-stu-id="99e8e-142">Learn how to port a .NET Framework WPF app to .NET Core.</span></span>](convert-project-from-net-framework.md)
