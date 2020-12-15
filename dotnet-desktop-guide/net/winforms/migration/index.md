---
title: Migrieren einer Windows Forms-Anwendung zu .NET 5
description: Hier erfahren Sie, wie Sie eine .NET Framework Windows Forms-Anwendung zu .NET 5 portieren.
ms.date: 11/02/2020
ms.topic: how-to
ms.openlocfilehash: 105c209fc567d2cce70b01267f793152d8140cb8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96992804"
---
# <a name="how-to-migrate-a-windows-forms-desktop-app-to-net-5"></a><span data-ttu-id="bcfc2-103">Migrieren einer Windows Forms-Desktopanwendung zu .NET 5</span><span class="sxs-lookup"><span data-stu-id="bcfc2-103">How to migrate a Windows Forms desktop app to .NET 5</span></span>

<span data-ttu-id="bcfc2-104">In diesem Artikel wird beschrieben, wie eine Windows Forms-Desktopanwendung von .NET Framework zu .NET 5 oder höher migriert wird.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-104">This article describes how to migrate a Windows Forms desktop app from .NET Framework to .NET 5 or later.</span></span> <span data-ttu-id="bcfc2-105">Das .NET SDK bietet Unterstützung für Windows Forms-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-105">The .NET SDK includes support for Windows Forms applications.</span></span> <span data-ttu-id="bcfc2-106">Windows Forms ist immer noch ein ausschließlich für Windows bestimmtes Framework und kann nur unter Windows ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-106">Windows Forms is still a Windows-only framework and only runs on Windows.</span></span>

<span data-ttu-id="bcfc2-107">Für die Migration einer Anwendung von .NET Framework zu .NET 5 ist im Allgemeinen eine neue Projektdatei erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-107">Migrating your app from .NET Framework to .NET 5 generally requires a new project file.</span></span> <span data-ttu-id="bcfc2-108">Bei .NET 5 werden Projektdateien im SDK-Format verwendet, während bei .NET Framework in der Regel ältere Visual Studio-Projektdateien zum Einsatz kommen.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-108">.NET 5 uses SDK-style project files while .NET Framework typically uses the older Visual Studio project file.</span></span> <span data-ttu-id="bcfc2-109">Wenn Sie jemals eine Visual Studio-Projektdatei in einem Text-Editor geöffnet haben, wissen Sie, wie detailliert diese ist.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-109">If you've ever opened a Visual Studio project file in a text editor, you know how verbose it is.</span></span> <span data-ttu-id="bcfc2-110">Projekte im SDK-Format sind kleiner und erfordern weniger Einträge als Projekte im älteren Dateiformat.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-110">SDK-style projects are smaller and don't require as many entries as the older project file format does.</span></span>

<span data-ttu-id="bcfc2-111">Weitere Informationen zu .NET 5 finden Sie unter [Einführung in .NET](/dotnet/core/introduction).</span><span class="sxs-lookup"><span data-stu-id="bcfc2-111">To learn more about .NET 5, see [Introduction to .NET](/dotnet/core/introduction).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="bcfc2-112">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="bcfc2-112">Prerequisites</span></span>

- [<span data-ttu-id="bcfc2-113">Visual Studio 2019, Version 16.8, Vorschauversion</span><span class="sxs-lookup"><span data-stu-id="bcfc2-113">Visual Studio 2019 version 16.8 Preview</span></span>](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019+desktopguide+winforms)

  - <span data-ttu-id="bcfc2-114">Wählen Sie die [Visual Studio-Desktop-Workload](/visualstudio/install/modify-visual-studio?view=vs-2019&preserve-view=true#modify-workloads) aus.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-114">Select the [Visual Studio Desktop workload](/visualstudio/install/modify-visual-studio?view=vs-2019&preserve-view=true#modify-workloads).</span></span>

  - <span data-ttu-id="bcfc2-115">Wählen Sie die [jeweilige .NET 5-Komponente](/visualstudio/install/modify-visual-studio?view=vs-2019&preserve-view=true#modify-individual-components) aus.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-115">Select the [.NET 5 individual component](/visualstudio/install/modify-visual-studio?view=vs-2019&preserve-view=true#modify-individual-components).</span></span>

- <span data-ttu-id="bcfc2-116">Vorschauversion des WinForms-Designers in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-116">Preview WinForms designer in Visual Studio.</span></span>

  <span data-ttu-id="bcfc2-117">Um den Designer zu aktivieren, wechseln Sie zu **Extras** > **Optionen** > **Umgebung** > **Vorschaufeatures**, und wählen Sie Option **Use the preview Windows Forms designer for .NET Core apps** (Vorschauversion des Windows Forms-Designers für .NET Core-Apps verwenden) aus.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-117">To enable the designer, go to **Tools** > **Options** > **Environment** > **Preview Features** and select the **Use the preview Windows Forms designer for .NET Core apps** option.</span></span>

- <span data-ttu-id="bcfc2-118">In diesem Artikel wird die Beispielanwendung [Vergleichsspiel](https://github.com/dotnet/samples/tree/master/windowsforms/matching-game/net45/) verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-118">This article uses the [Matching game](https://github.com/dotnet/samples/tree/master/windowsforms/matching-game/net45/) sample app.</span></span> <span data-ttu-id="bcfc2-119">Wenn Sie diese Anwendung verwenden möchten, laden Sie sie herunter, und öffnen Sie sie in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-119">If you want to follow along, download and open the application in Visual Studio.</span></span> <span data-ttu-id="bcfc2-120">Andernfalls verwenden Sie Ihre eigene Anwendung.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-120">Otherwise, use your own app.</span></span>

### <a name="consider"></a><span data-ttu-id="bcfc2-121">Consider</span><span class="sxs-lookup"><span data-stu-id="bcfc2-121">Consider</span></span>

<span data-ttu-id="bcfc2-122">Wenn Sie eine .NET Framework Windows Forms-Anwendung migrieren, müssen Sie ein paar Dinge berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-122">When migrating a .NET Framework Windows Forms application, there are a few things you must consider.</span></span>

01. <span data-ttu-id="bcfc2-123">Überprüfen Sie, ob Ihre Anwendung ein guter Kandidat für die Migration ist.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-123">Check that your application is a good candidate for migration.</span></span>

    <span data-ttu-id="bcfc2-124">Verwenden Sie [.NET Portability Analyzer](/dotnet/standard/analyzers/portability-analyzer), um zu bestimmen, ob Ihr Projekt zu .NET 5 migriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-124">Use the [.NET Portability Analyzer](/dotnet/standard/analyzers/portability-analyzer) to determine if your project will migrate to .NET 5.</span></span> <span data-ttu-id="bcfc2-125">Wenn bei Ihrem Projekt Probleme mit .NET 5 vorliegen, können Sie diese Probleme mit dem Analyzer identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-125">If your project has issues with .NET 5, the analyzer helps you identify those problems.</span></span> <span data-ttu-id="bcfc2-126">Das Tool .NET Portability Analyzer kann als Visual Studio-Erweiterung installiert oder über die Befehlszeile verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-126">The .NET Portability Analyzer tool can be installed as a Visual Studio extension or used from the command line.</span></span> <span data-ttu-id="bcfc2-127">Weitere Informationen finden Sie unter [.NET Portability Analyzer](/dotnet/standard/analyzers/portability-analyzer).</span><span class="sxs-lookup"><span data-stu-id="bcfc2-127">For more information, see [.NET Portability Analyzer](/dotnet/standard/analyzers/portability-analyzer).</span></span>

01. <span data-ttu-id="bcfc2-128">Sie verwenden eine andere Version von Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-128">You're using a different version of Windows Forms.</span></span>

    <span data-ttu-id="bcfc2-129">Als .NET Core 3.0 veröffentlicht wurde, wurde Windows Forms als [Open-Source-Version auf GitHub](https://github.com/dotnet/winforms) zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-129">When .NET Core 3.0 was released, Windows Forms went [open source on GitHub](https://github.com/dotnet/winforms).</span></span> <span data-ttu-id="bcfc2-130">Der Code für Windows Forms für .NET 5 ist ein Fork der .NET Framework-Windows Forms-Codebasis.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-130">The code for Windows Forms for .NET 5 is a fork of the .NET Framework Windows Forms codebase.</span></span> <span data-ttu-id="bcfc2-131">Es ist möglich, dass einige Unterschiede bestehen, und Ihre Anwendung schwierig zu migrieren ist.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-131">It's possible some differences exist and your app will be difficult to migrate.</span></span>

01. <span data-ttu-id="bcfc2-132">Das [Windows Compatibility Pack][compat-pack] könnte Ihnen bei der Migration helfen.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-132">The [Windows Compatibility Pack][compat-pack] may help you migrate.</span></span>

    <span data-ttu-id="bcfc2-133">Einige APIs, die in .NET Framework verfügbar sind, sind nicht in .NET 5 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-133">Some APIs that are available in .NET Framework aren't available in .NET 5.</span></span> <span data-ttu-id="bcfc2-134">Das [Windows Compatibility Pack][compat-pack] fügt viele dieser APIs hinzu und könnte zur Kompatibilität Ihrer Windows Forms-App mit .NET 5 beitragen.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-134">The [Windows Compatibility Pack][compat-pack] adds many of these APIs and may help your Windows Forms app become compatible with .NET 5.</span></span>

01. <span data-ttu-id="bcfc2-135">Aktualisieren Sie die NuGet-Pakete, die von Ihrem Projekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-135">Update the NuGet packages used by your project.</span></span>

    <span data-ttu-id="bcfc2-136">Es hat sich bewährt, vor jeder Migration die neuesten Versionen der NuGet-Pakete zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-136">It's always a good practice to use the latest versions of NuGet packages before any migration.</span></span> <span data-ttu-id="bcfc2-137">Wenn Ihre Anwendung auf NuGet-Pakete verweist, aktualisieren Sie sie auf die neueste Version.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-137">If your application is referencing any NuGet packages, update them to the latest version.</span></span> <span data-ttu-id="bcfc2-138">Stellen Sie sicher, dass die Anwendung erfolgreich erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-138">Ensure your application builds successfully.</span></span> <span data-ttu-id="bcfc2-139">Wenn nach dem Upgrade Paketfehler auftreten, stufen Sie das Paket auf die neueste Version herab, die Ihren Code nicht beschädigt.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-139">After upgrading, if there are any package errors, downgrade the package to the latest version that doesn't break your code.</span></span>

## <a name="back-up-your-projects"></a><span data-ttu-id="bcfc2-140">Sichern von Projekten</span><span class="sxs-lookup"><span data-stu-id="bcfc2-140">Back up your projects</span></span>

<span data-ttu-id="bcfc2-141">Beim Migrieren eines Projekts müssen Sie das Projekt zunächst einmal sichern.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-141">The first step to migrating a project is to back up your project!</span></span> <span data-ttu-id="bcfc2-142">Wenn etwas schief geht, können Sie Ihren Code in den ursprünglichen Zustand zurückversetzen, indem Sie die Sicherung wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-142">If something goes wrong, you can restore your code to its original state by restoring your backup.</span></span> <span data-ttu-id="bcfc2-143">Verlassen Sie sich beim Sichern eines Projekts nicht auf Tools wie .NET Portability Analyzer.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-143">Don't rely on tools such as the .NET Portability Analyzer to back up your project, even if they seem to.</span></span> <span data-ttu-id="bcfc2-144">Am besten erstellen Sie selbst eine Kopie des ursprünglichen Projekts.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-144">It's best to personally create a copy of the original project.</span></span>

## <a name="nuget-packages"></a><span data-ttu-id="bcfc2-145">NuGet-Pakete</span><span class="sxs-lookup"><span data-stu-id="bcfc2-145">NuGet packages</span></span>

<span data-ttu-id="bcfc2-146">Wenn Ihr Projekt auf NuGet-Pakete verweist, befindet sich in Ihrem Projektordner vermutlich eine **packages.config**-Datei.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-146">If your project is referencing NuGet packages, you probably have a **packages.config** file in your project folder.</span></span> <span data-ttu-id="bcfc2-147">Bei Projekten im SDK-Format werden NuGet-Paketverweise in der Projektdatei konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-147">With SDK-style projects, NuGet package references are configured in the project file.</span></span> <span data-ttu-id="bcfc2-148">In Visual Studio-Projektdateien können optional ebenfalls NuGet-Pakete definiert werden.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-148">Visual Studio project files can optionally define NuGet packages in the project file too.</span></span> <span data-ttu-id="bcfc2-149">Bei .NET 5 werden für NuGet-Pakete keine **packages.config**-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-149">.NET 5 doesn't use **packages.config** for NuGet packages.</span></span> <span data-ttu-id="bcfc2-150">NuGet-Paketverweise müssen vor der Migration in die Projektdatei migriert werden.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-150">NuGet package references must be migrated into the project file before migration.</span></span>

<span data-ttu-id="bcfc2-151">Gehen Sie wie folgt vor, um die **packages.config**-Datei zu migrieren:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-151">To migrate the **packages.config** file, do the following steps:</span></span>

01. <span data-ttu-id="bcfc2-152">Suchen Sie in **Projektmappen-Explorer** nach dem Projekt, das migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-152">In **Solution explorer**, find the project you're migrating.</span></span>
02. <span data-ttu-id="bcfc2-153">Klicken Sie mit der rechten Maustaste auf **packages.config** >  **„packages.config“ zu PackageReference migrieren**.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-153">Right-click on **packages.config** > **Migrate packages.config to PackageReference**.</span></span>
03. <span data-ttu-id="bcfc2-154">Wählen Sie alle Pakete auf oberster Ebene aus.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-154">Select all of the top-level packages.</span></span>

<span data-ttu-id="bcfc2-155">Es wird ein Buildbericht erstellt, um Sie über mögliche Probleme bei der Migration der NuGet-Pakete zu informieren.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-155">A build report is generated to let you know of any issues migrating the NuGet packages.</span></span>

## <a name="project-file"></a><span data-ttu-id="bcfc2-156">Projektdatei</span><span class="sxs-lookup"><span data-stu-id="bcfc2-156">Project file</span></span>

<span data-ttu-id="bcfc2-157">Als Nächstes müssen Sie bei der Migration einer Anwendung die Projektdatei konvertieren.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-157">The next step in migrating your app is converting the project file.</span></span> <span data-ttu-id="bcfc2-158">Wie bereits erwähnt, werden bei .NET 5 Projektdateien im SDK-Format verwendet. Visual Studio-Projektdateien, die bei .NET Framework verwendet werden, werden nicht geladen.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-158">As previously stated, .NET 5 uses SDK-style project files and won't load the Visual Studio project files that .NET Framework uses.</span></span> <span data-ttu-id="bcfc2-159">Es kann jedoch sein, das Sie bereits Projekte im SDK-Format verwenden.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-159">However, there's the possibility that you're already using SDK-style projects.</span></span> <span data-ttu-id="bcfc2-160">Den Unterschied können Sie in Visual Studio leicht erkennen.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-160">You can easily spot the difference in Visual Studio.</span></span> <span data-ttu-id="bcfc2-161">Klicken Sie mit der rechten Maustaste in **Projektmappen-Explorer**, und suchen Sie nach der Menüoption **Projektdatei bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-161">Right-click on the project file in **Solution explorer** and look for the **Edit Project File** menu option.</span></span> <span data-ttu-id="bcfc2-162">Wenn dieses Menüelement nicht angezeigt wird, verwenden Sie das alte Visual Studio-Projektformat und müssen ein Upgrade ausführen.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-162">If this menu item is missing, you're using the old Visual Studio project format and need to upgrade.</span></span>

<span data-ttu-id="bcfc2-163">Konvertieren alle Projekte in Ihrer Projektmappe.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-163">Convert each project in your solution.</span></span> <span data-ttu-id="bcfc2-164">Wenn Sie die bereits erwähnte Beispielanwendung verwenden, werden die beiden Projekte **MatchingGame** und **MatchingGame.Logic** konvertiert.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-164">If you're using the sample app previously referenced, both the **MatchingGame** and **MatchingGame.Logic** projects would be converted.</span></span>

<span data-ttu-id="bcfc2-165">Gehen Sie wie folgt vor, um ein Projekt zu konvertieren:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-165">To convert a project, do the following steps:</span></span>

01. <span data-ttu-id="bcfc2-166">Suchen Sie in **Projektmappen-Explorer** nach dem Projekt, das migriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-166">In **Solution explorer**, find the project you're migrating.</span></span>
01. <span data-ttu-id="bcfc2-167">Klicken Sie mit der rechten Maustaste auf das Projekt, und wählen Sie **Projekt entladen** aus.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-167">Right-click on the project and select **Unload Project**.</span></span>
01. <span data-ttu-id="bcfc2-168">Klicken Sie mit der rechten Maustaste auf das Projekt, und wählen Sie **Projektdatei bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-168">Right-click on the project and select **Edit Project File**.</span></span>
01. <span data-ttu-id="bcfc2-169">Kopieren Sie den XML-Code des Projekt, und fügen Sie ihn in einen Text-Editor ein.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-169">Copy-and-paste the project XML into a text editor.</span></span> <span data-ttu-id="bcfc2-170">Sie sollten eine Kopie verwenden, sodass Sie ohne großen Aufwand Inhalte in das neue Projekt verschieben können.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-170">You'll want a copy so that it's easy to move content into the new project.</span></span>
01. <span data-ttu-id="bcfc2-171">Löschen Sie den Inhalt der Datei, und fügen Sie den folgenden XML-Code ein:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-171">Erase the content of the file and paste the following XML:</span></span>

    ```xml
    <Project Sdk="Microsoft.NET.Sdk">

      <PropertyGroup>
        <OutputType>WinExe</OutputType>
        <TargetFramework>net5.0-windows</TargetFramework>
        <UseWindowsForms>true</UseWindowsForms>
        <GenerateAssemblyInfo>false</GenerateAssemblyInfo>
      </PropertyGroup>

    </Project>
    ```

    > [!IMPORTANT]
    > <span data-ttu-id="bcfc2-172">Mit Bibliotheken muss keine `<OutputType>`-Einstellung definiert werden.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-172">Libraries don't need to define an `<OutputType>` setting.</span></span> <span data-ttu-id="bcfc2-173">Entfernen Sie diesen Eintrag, wenn Sie ein Bibliotheksprojekt aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-173">Remove that entry if you're upgrading a library project.</span></span>

<span data-ttu-id="bcfc2-174">Dieser XML-Code stellt die grundlegende Struktur des Projekts dar.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-174">This XML gives you the basic structure of the project.</span></span> <span data-ttu-id="bcfc2-175">Er enthält jedoch keine Einstellung aus der alten Projektdatei.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-175">However, it doesn't contain any of the settings from the old project file.</span></span> <span data-ttu-id="bcfc2-176">Führen Sie die folgenden Schritte aus, und verwenden Sie dabei die zuvor in einen Text-Editor kopierten alten Projektinformationen:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-176">Using the old project information you previously copied to a text editor, do the following steps:</span></span>

01. <span data-ttu-id="bcfc2-177">Kopieren Sie die folgenden Elemente aus der alten Projektdatei in das `<PropertyGroup>`-Element in der neuen Projektdatei:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-177">Copy the following elements from the old project file into the `<PropertyGroup>` element in the new project file:</span></span>

    - `<RootNamespace>`
    - `<AssemblyName>`

    <span data-ttu-id="bcfc2-178">Die Projektdatei sollte in etwa wie der folgende XML-Code aussehen:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-178">Your project file should look similar to the following XML:</span></span>

    ```xml
    <Project Sdk="Microsoft.NET.Sdk">

      <PropertyGroup>
        <OutputType>WinExe</OutputType>
        <TargetFramework>net5.0-windows</TargetFramework>
        <UseWindowsForms>true</UseWindowsForms>
        <GenerateAssemblyInfo>false</GenerateAssemblyInfo>

        <RootNamespace>MatchingGame</RootNamespace>
        <AssemblyName>MatchingGame</AssemblyName>
      </PropertyGroup>

    </Project>
    ```

01. <span data-ttu-id="bcfc2-179">Kopieren Sie die `<ItemGroup>`-Elemente aus der alten Projektdatei, zu denen `<ProjectReference>` oder `<PackageReference>` gehört, in der neuen Datei an eine Stelle nach dem schließenden Tag `</PropertyGroup>`.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-179">Copy the `<ItemGroup>` elements from the old project file that contain `<ProjectReference>` or `<PackageReference>` into the new file after the `</PropertyGroup>` closing tag.</span></span>

    <span data-ttu-id="bcfc2-180">Die Projektdatei sollte in etwa wie der folgende XML-Code aussehen:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-180">Your project file should look similar to the following XML:</span></span>

    ```xml
    <Project Sdk="Microsoft.NET.Sdk">

      <PropertyGroup>
        (contains settings previously described)
      </PropertyGroup>

      <ItemGroup>
        <ProjectReference Include="..\MatchingGame.Logic\MatchingGame.Logic.csproj">
          <Project>{36b3e6e2-a9ae-4924-89ae-7f0120ce08bd}</Project>
          <Name>MatchingGame.Logic</Name>
        </ProjectReference>
      </ItemGroup>
      <ItemGroup>
        <PackageReference Include="MetroFramework">
          <Version>1.2.0.3</Version>
        </PackageReference>
      </ItemGroup>

    </Project>
    ```

    <span data-ttu-id="bcfc2-181">Da die `<ProjectReference>`-Elemente keine untergeordneten `<Project>`- und `<Name>`-Elemente benötigen, können Sie diese Einstellungen entfernen:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-181">The `<ProjectReference>` elements don't need the `<Project>` and `<Name>` children, so you can remove those settings:</span></span>

    ```xml
    <ItemGroup>
      <ProjectReference Include="..\MatchingGame.Logic\MatchingGame.Logic.csproj" />
    </ItemGroup>
    ```

### <a name="resources-and-settings"></a><span data-ttu-id="bcfc2-182">Ressourcen und Einstellungen</span><span class="sxs-lookup"><span data-stu-id="bcfc2-182">Resources and settings</span></span>

<span data-ttu-id="bcfc2-183">Windows Forms-Projekte für .NET Framework enthalten in der Regel andere Dateien, z. B. *Properties/Settings.settings* und *Properties/Resources.resx*.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-183">Windows Forms projects for .NET Framework typically include other files such as *Properties/Settings.settings* and *Properties/Resources.resx*.</span></span> <span data-ttu-id="bcfc2-184">Diese Dateien und alle *resx*-Dateien für Ihre Anwendung (außer *resx*-Formulardateien) müssen migriert werden.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-184">These files, and any *resx* file created for your app besides form *resx* files, would need to be migrated.</span></span>

<span data-ttu-id="bcfc2-185">Kopieren Sie diese Einträge aus der alten Projektdatei in ein `<ItemGroup>`-Element im neuen Projekt.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-185">Copy those entries from the old project file into an `<ItemGroup>` element in the new project.</span></span> <span data-ttu-id="bcfc2-186">Ändern Sie nach dem Kopieren der Einträge alle `<Compile Include="value">`- bzw. `<EmbeddedResource Include="value">`-Elemente so, dass `Update` anstelle von `Include` verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-186">After you copy the entries, change any `<Compile Include="value">` or `<EmbeddedResource Include="value">` elements to instead use `Update` instead of `Include`.</span></span>

- <span data-ttu-id="bcfc2-187">Importieren Sie die Konfiguration für die *Settings.settings*-Datei.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-187">Import the configuration for the *Settings.settings* file.</span></span> <span data-ttu-id="bcfc2-188">Im `<Compile>`-Element wurde `Include` in `Update` geändert:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-188">Notice that the `Include` was changed to `Update` on the `<Compile>` element:</span></span>

  ```xml
  <ItemGroup>
    <None Include="Properties\Settings.settings">
      <Generator>SettingsSingleFileGenerator</Generator>
      <LastGenOutput>Settings.Designer.cs</LastGenOutput>
    </None>
    <Compile Update="Properties\Settings.Designer.cs">
      <AutoGen>True</AutoGen>
      <DependentUpon>Settings.settings</DependentUpon>
      <DesignTimeSharedInput>True</DesignTimeSharedInput>
    </Compile>
  </ItemGroup>
  ```

  > [!IMPORTANT]
  > <span data-ttu-id="bcfc2-189">Bei **Visual Basic**-Projekten wird als Standarddatei für Projekteinstellungen der Ordner *My Project*, bei C#-Projekten dagegen der Ordner *Properties* verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-189">**Visual Basic** projects typically use the folder *My Project* while C# projects typically use the folder *Properties* for the default project settings file.</span></span>
  
- <span data-ttu-id="bcfc2-190">Importieren Sie die Konfiguration für alle *resx*-Dateien, z. B. für die Datei *properties/Resources.resx*.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-190">Import the configuration for any *resx* file, such as the *properties/Resources.resx* file.</span></span> <span data-ttu-id="bcfc2-191">Sowohl im `<Compile>`- als auch im `<EmbeddedResource>`-Element wurde `Include` in `Update` geändert und `<SubType>` wurde aus `<EmbeddedResource>` entfernt:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-191">Notice that the `Include` was changed to `Update` on both the `<Compile>` and `<EmbeddedResource>` elements, and `<SubType>` was removed from `<EmbeddedResource>`:</span></span>

  ```xml
  <ItemGroup>
    <EmbeddedResource Update="Properties\Resources.resx">
      <Generator>ResXFileCodeGenerator</Generator>
      <LastGenOutput>Resources.Designer.cs</LastGenOutput>
    </EmbeddedResource>
    <Compile Update="Properties\Resources.Designer.cs">
      <AutoGen>True</AutoGen>
      <DependentUpon>Resources.resx</DependentUpon>
      <DesignTime>True</DesignTime>
    </Compile>
  </ItemGroup>
  ```

  > [!IMPORTANT]
  > <span data-ttu-id="bcfc2-192">Bei **Visual Basic**-Projekten wird als Standarddatei für die Projektressource der Ordner *My Project*, bei C#-Projekten dagegen der Ordner *Properties* verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-192">**Visual Basic** projects typically use the folder *My Project* while C# projects typically use the folder *Properties* for the default project resource file.</span></span>

### <a name="visual-basic"></a><span data-ttu-id="bcfc2-193">Visual Basic</span><span class="sxs-lookup"><span data-stu-id="bcfc2-193">Visual Basic</span></span>

<span data-ttu-id="bcfc2-194">Bei Projekten in der Sprache Visual Basic müssen zusätzliche Konfigurationsschritte durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-194">Visual Basic language projects require extra configuration.</span></span>

01. <span data-ttu-id="bcfc2-195">Importieren Sie die Einstellung *My Project\Application.myapp* der Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-195">Import the configuration file *My Project\Application.myapp* setting.</span></span> <span data-ttu-id="bcfc2-196">Für die Elemente `<None>` und `<Compile>` wird das `Update`-Attribut anstelle des `Include`-Attributs verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-196">Notice that the `<None>` and `<Compile>` elements use the `Update` attribute instead of the `Include` attribute.</span></span>

    ```xml
    <ItemGroup>
      <None Update="My Project\Application.myapp">
        <Generator>MyApplicationCodeGenerator</Generator>
        <LastGenOutput>Application.Designer.vb</LastGenOutput>
      </None>
      <Compile Update="My Project\Application.Designer.vb">
        <AutoGen>True</AutoGen>
        <DependentUpon>Application.myapp</DependentUpon>
        <DesignTime>True</DesignTime>
      </Compile>
    </ItemGroup>
    ```

01. <span data-ttu-id="bcfc2-197">Fügen Sie dem `<PropertyGroup>`-Element die `<MyType>WindowsForms</MyType>`-Einstellung hinzu:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-197">Add the `<MyType>WindowsForms</MyType>` setting to the `<PropertyGroup>` element:</span></span>

    ```xml
    <PropertyGroup>
      (contains settings previously described)

      <MyType>WindowsForms</MyType>
    </PropertyGroup>
    ```

    <span data-ttu-id="bcfc2-198">Mit dieser Einstellung werden die `My`-Namespacemember importiert, mit denen Visual Basic-Programmierer vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-198">This setting imports the `My` namespace members Visual Basic programmers are familiar with.</span></span>

01. <span data-ttu-id="bcfc2-199">Importieren Sie die vom Projekt definierten Namespaces.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-199">Import the namespaces defined by your project.</span></span>

    <span data-ttu-id="bcfc2-200">Mit Visual Basic-Projekten können Namespaces automatisch in jede Codedatei importiert werden.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-200">Visual Basic projects can automatically import namespaces into every code file.</span></span> <span data-ttu-id="bcfc2-201">Kopieren Sie die `<ItemGroup>`-Elemente aus der alten Projektdatei, zu denen `<Import>` gehört, in der neuen Datei an eine Stelle nach dem schließenden Tag `</PropertyGroup>`.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-201">Copy the `<ItemGroup>` elements from the old project file that contain `<Import>` into the new file after the `</PropertyGroup>` closing tag.</span></span>

    ```xml
    <ItemGroup>
      <Import Include="Microsoft.VisualBasic" />
      <Import Include="System" />
      <Import Include="System.Collections" />
      <Import Include="System.Collections.Generic" />
      <Import Include="System.Data" />
      <Import Include="System.Drawing" />
      <Import Include="System.Diagnostics" />
      <Import Include="System.Windows.Forms" />
      <Import Include="System.Linq" />
      <Import Include="System.Xml.Linq" />
      <Import Include="System.Threading.Tasks" />
    </ItemGroup>
    ```

    <span data-ttu-id="bcfc2-202">Wenn keine `<Import>`-Anweisungen vorhanden sind oder beim Kompilieren des Projekts Fehler auftreten, überprüfen Sie, ob im Projekt zumindest die folgenden `<Import>`-Anweisungen definiert sind:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-202">If you can't find any `<Import>` statements, or your project fails to compile, make sure you at least have the following `<Import>` statements defined in your project:</span></span>

    ```xml
    <ItemGroup>
      <Import Include="System.Data" />
      <Import Include="System.Drawing" />
      <Import Include="System.Windows.Forms" />
    </ItemGroup>
    ```

01. <span data-ttu-id="bcfc2-203">Kopieren Sie die Einstellungen `<Option*>` und `<StartupObject>` aus dem ursprünglichen Projekt in das `<PropertyGroup>`-Element:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-203">From the original project, copy the `<Option*>` and `<StartupObject>` settings to the `<PropertyGroup>` element:</span></span>

    ```xml
    <PropertyGroup>
      (contains settings previously described)

      <OptionExplicit>On</OptionExplicit>
      <OptionCompare>Binary</OptionCompare>
      <OptionStrict>Off</OptionStrict>
      <OptionInfer>On</OptionInfer>
      <StartupObject>MatchingGame.My.MyApplication</StartupObject>
    </PropertyGroup>
    ```

### <a name="reload-the-project"></a><span data-ttu-id="bcfc2-204">Erneutes Laden des Projekts</span><span class="sxs-lookup"><span data-stu-id="bcfc2-204">Reload the project</span></span>

<span data-ttu-id="bcfc2-205">Nachdem Sie ein Projekt in das neue SDK-Format konvertiert haben, laden Sie das Projekt erneut in Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-205">After you convert a project to the new SDK-style format, reload the project in Visual Studio:</span></span>

01. <span data-ttu-id="bcfc2-206">Suchen Sie in **Projektmappen-Explorer** nach dem Projekt, das konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-206">In **Solution Explorer**, find the project you converted.</span></span>
01. <span data-ttu-id="bcfc2-207">Klicken Sie mit der rechten Maustaste auf das Projekt, und wählen Sie **Projekt erneut laden** aus.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-207">Right-click on the project and select **Reload Project**.</span></span>

    <span data-ttu-id="bcfc2-208">Wenn beim Laden des Projekts ein Fehler auftritt, enthält der XML-Code des Projekts möglicherweise einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-208">If the project fails to load, you may have introduced a mistake in the XML of the project.</span></span> <span data-ttu-id="bcfc2-209">Öffnen Sie die Projektdatei zur Bearbeitung, suchen Sie nach dem Fehler, und beheben Sie ihn.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-209">Open the project file for editing and try to identify and fix the mistake.</span></span> <span data-ttu-id="bcfc2-210">Wenn Sie keinen Fehler finden, versuchen Sie es noch mal.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-210">If you can't find a mistake, try starting over.</span></span>

## <a name="edit-appconfig"></a><span data-ttu-id="bcfc2-211">Bearbeiten der Datei „App.config“</span><span class="sxs-lookup"><span data-stu-id="bcfc2-211">Edit App.config</span></span>

<span data-ttu-id="bcfc2-212">Wenn Ihre Anwendung eine *App.config*-Datei enthält, entfernen Sie das `<supportedRuntime>`-Element:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-212">If your app has an *App.config* file, remove the `<supportedRuntime>` element:</span></span>

```xml
<supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5" />
```

<span data-ttu-id="bcfc2-213">Im Zusammenhang mit der Datei *App.config* müssen einige Dinge berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-213">There are some things you should consider with the *App.config* file.</span></span> <span data-ttu-id="bcfc2-214">Die Datei *App.config* in .NET Framework wurde nicht nur zum Konfigurieren der Anwendung, sondern auch zum Konfigurieren von Laufzeiteinstellungen und Verhaltensweisen wie die Protokollierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-214">The *App.config* file in .NET Framework was used not only to configure the app, but to configure runtime settings and behavior, such as logging.</span></span> <span data-ttu-id="bcfc2-215">Ab .NET 5 (und in .NET Core) wird die Datei *App.config* nicht mehr für die Laufzeitkonfiguration verwendet.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-215">The *App.config* file in .NET 5+ (and .NET Core) is no longer used for runtime configuration.</span></span> <span data-ttu-id="bcfc2-216">Wenn Ihre *App.config*-Datei diese Abschnitte enthält, werden diese nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-216">If your *App.config* file has these sections, they won't be respected.</span></span>

## <a name="add-the-compatibility-package"></a><span data-ttu-id="bcfc2-217">Hinzufügen des Kompatibilitätspakets</span><span class="sxs-lookup"><span data-stu-id="bcfc2-217">Add the compatibility package</span></span>

<span data-ttu-id="bcfc2-218">Wenn Ihre Projektdatei ordnungsgemäß geladen wird, bei der Kompilierung für Ihr Projekt jedoch ein Fehler auftritt und Fehlermeldungen wie die folgende angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-218">If your project file is loading correctly, but compilation fails for your project and you receive errors similar to the following:</span></span>

- <span data-ttu-id="bcfc2-219">**Der Typ oder Namespace \<some name> wurde nicht gefunden**</span><span class="sxs-lookup"><span data-stu-id="bcfc2-219">**The type or namespace \<some name> could not be found**</span></span>
- <span data-ttu-id="bcfc2-220">**Der Name \<some name> ist im aktuellen Kontext nicht vorhanden**</span><span class="sxs-lookup"><span data-stu-id="bcfc2-220">**The name \<some name> does not exist in the current context**</span></span>

<span data-ttu-id="bcfc2-221">Müssen Sie Ihrer Anwendung möglicherweise das [`Microsoft.Windows.Compatibility`](https://www.nuget.org/packages/Microsoft.Windows.Compatibility/)-Paket hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-221">You may need to add the [`Microsoft.Windows.Compatibility`](https://www.nuget.org/packages/Microsoft.Windows.Compatibility/) package to your app.</span></span> <span data-ttu-id="bcfc2-222">Mit diesem Paket werden etwa 21.000 .NET-APIs aus .NET Framework wie die `System.Configuration.ConfigurationManager`-Klasse und APIs für die Interaktion mit der Windows-Registrierung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-222">This package adds ~21,000 .NET APIs from .NET Framework, such as the `System.Configuration.ConfigurationManager` class and APIs for interacting with the Windows Registry.</span></span> <span data-ttu-id="bcfc2-223">Fügen Sie das Paket `Microsoft.Windows.Compatibility` hinzu.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-223">Add the `Microsoft.Windows.Compatibility` package.</span></span>

<span data-ttu-id="bcfc2-224">Bearbeiten Sie die Projektdatei, und fügen Sie das folgende `<ItemGroup>`-Element hinzu:</span><span class="sxs-lookup"><span data-stu-id="bcfc2-224">Edit your project file and add the following `<ItemGroup>` element:</span></span>

```xml
<ItemGroup>
  <PackageReference Include="Microsoft.Windows.Compatibility" Version="5.0.0" />
</ItemGroup>
```

## <a name="test-your-app"></a><span data-ttu-id="bcfc2-225">Testen Ihrer App</span><span class="sxs-lookup"><span data-stu-id="bcfc2-225">Test your app</span></span>

<span data-ttu-id="bcfc2-226">Testen Sie Ihre Anwendung, nachdem Sie sie migriert haben.</span><span class="sxs-lookup"><span data-stu-id="bcfc2-226">After you've finished migrating your app, test it!</span></span>

## <a name="next-steps"></a><span data-ttu-id="bcfc2-227">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="bcfc2-227">Next steps</span></span>

- <span data-ttu-id="bcfc2-228">Informieren Sie sich über [Breaking Changes in Windows Forms](/dotnet/core/compatibility/winforms).</span><span class="sxs-lookup"><span data-stu-id="bcfc2-228">Learn about [breaking changes in Windows Forms](/dotnet/core/compatibility/winforms).</span></span>
- <span data-ttu-id="bcfc2-229">Lesen Sie mehr über das [Windows Compatibility Pack][compat-pack].</span><span class="sxs-lookup"><span data-stu-id="bcfc2-229">Read more about the [Windows Compatibility Pack][compat-pack].</span></span>

[compat-pack]: /dotnet/core/porting/windows-compat-pack
