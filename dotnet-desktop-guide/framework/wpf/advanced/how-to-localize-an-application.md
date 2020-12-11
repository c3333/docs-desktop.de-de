---
title: Lokalisieren einer App
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- localization [WPF], applications
- LocBaml tool [WPF]
- applications [WPF], localizing
ms.assetid: 5001227e-9326-48a4-9dcd-ba1b89ee6653
ms.openlocfilehash: dc7d8f4f56b26fffbd883e1e1d6e420026e1f94f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976881"
---
# <a name="how-to-localize-an-application"></a><span data-ttu-id="0fbc9-102">Vorgehensweise: Lokalisieren einer Anwendung</span><span class="sxs-lookup"><span data-stu-id="0fbc9-102">How to: Localize an application</span></span>

<span data-ttu-id="0fbc9-103">In diesem Lernprogramm wird erläutert, wie eine lokalisierte Anwendung mit dem LocBaml-Tool erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-103">This tutorial explains how to create a localized application by using the LocBaml tool.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="0fbc9-104">Das LocBaml-Tool ist keine einsatzfertige Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-104">The LocBaml tool is not a production-ready application.</span></span> <span data-ttu-id="0fbc9-105">Es wird als Beispiel präsentiert, das einen Teil der Lokalisierungs-APIs verwendet und veranschaulicht, wie Sie ein Lokalisierungstool schreiben können.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-105">It is presented as a sample that uses some of the localization APIs and illustrates how you might write a localization tool.</span></span>  
  
## <a name="overview"></a><span data-ttu-id="0fbc9-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="0fbc9-106">Overview</span></span>

<span data-ttu-id="0fbc9-107">In diesem Artikel erhalten Sie einen Schritt-für-Schritt-Ansatz zum Lokalisieren einer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-107">This article gives you a step-by-step approach to localizing an application.</span></span> <span data-ttu-id="0fbc9-108">Zuerst bereiten Sie Ihre Anwendung so vor, dass der zu über setzende Text extrahiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-108">First, you prepare your application so that the text that will be translated can be extracted.</span></span> <span data-ttu-id="0fbc9-109">Nachdem der Text übersetzt wurde, führen Sie den übersetzten Text mit einer neuen Kopie der ursprünglichen Anwendung zusammen.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-109">After the text is translated, you merge the translated text into a new copy of the original application.</span></span>
  
## <a name="create-a-sample-application"></a><span data-ttu-id="0fbc9-110">Erstellen einer Beispielanwendung</span><span class="sxs-lookup"><span data-stu-id="0fbc9-110">Create a sample application</span></span>

<span data-ttu-id="0fbc9-111">In diesem Schritt bereiten Sie Ihre APP auf die Lokalisierung vor.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-111">In this step, you prepare your app for localization.</span></span> <span data-ttu-id="0fbc9-112">In den Windows Presentation Foundation-Beispielen (WPF) wird ein HelloApp-Beispiel bereitgestellt, das für die Codebeispiele in dieser Diskussion verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-112">In the Windows Presentation Foundation (WPF) samples, a HelloApp sample is supplied that will be used for the code examples in this discussion.</span></span> <span data-ttu-id="0fbc9-113">Wenn Sie dieses Beispiel verwenden möchten, laden Sie die Extensible Application Markup Language Dateien (XAML) vom [LocBaml-Tool Beispiel](https://github.com/microsoft/WPF-Samples/tree/master/Tools/LocBaml)herunter.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-113">If you would like to use this sample, download the Extensible Application Markup Language (XAML) files from the [LocBaml Tool Sample](https://github.com/microsoft/WPF-Samples/tree/master/Tools/LocBaml).</span></span>  
  
1. <span data-ttu-id="0fbc9-114">Entwickeln Sie Ihre Anwendung bis zu dem Punkt, an dem Sie die Lokalisierung starten möchten.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-114">Develop your application to the point where you want to start localization.</span></span>  
  
2. <span data-ttu-id="0fbc9-115">Geben Sie die Entwicklungssprache in der Projektdatei an, damit MSBuild eine Hauptassembly und eine Satellitenassembly (eine Datei mit der .resources.dll Erweiterung) generiert, die die neutralen Sprachressourcen enthält.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-115">Specify the development language in the project file so that MSBuild generates a main assembly and a satellite assembly (a file with the .resources.dll extension) to contain the neutral language resources.</span></span> <span data-ttu-id="0fbc9-116">Die Projektdatei im HelloApp-Beispiel ist "HelloApp.csproj".</span><span class="sxs-lookup"><span data-stu-id="0fbc9-116">The project file in the HelloApp sample is HelloApp.csproj.</span></span> <span data-ttu-id="0fbc9-117">In dieser Datei finden Sie die Entwicklungssprache wie folgt gekennzeichnet:</span><span class="sxs-lookup"><span data-stu-id="0fbc9-117">In that file, you will find the development language identified as follows:</span></span>  
  
   `<UICulture>en-US</UICulture>`  
  
3. <span data-ttu-id="0fbc9-118">Fügen Sie den XAML-Dateien UIDs hinzu.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-118">Add Uids to your XAML files.</span></span> <span data-ttu-id="0fbc9-119">UIDs werden verwendet, um Änderungen an Dateien nachzuverfolgen und die Elemente zu identifizieren, die übersetzt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-119">Uids are used to keep track of changes to files and to identify items that must be translated.</span></span> <span data-ttu-id="0fbc9-120">Um den Dateien UIDs hinzuzufügen, führen Sie `updateuid` in der Projektdatei aus:</span><span class="sxs-lookup"><span data-stu-id="0fbc9-120">To add Uids to your files, run `updateuid` on your project file:</span></span>  

   `msbuild -t:updateuid helloapp.csproj`

   <span data-ttu-id="0fbc9-121">Führen Sie Folgendes aus, um zu überprüfen, ob Sie über fehlende oder doppelte UIDs verfügen `checkuid` :</span><span class="sxs-lookup"><span data-stu-id="0fbc9-121">To verify that you have no missing or duplicate Uids, run `checkuid`:</span></span>  

   `msbuild -t:checkuid helloapp.csproj`

   <span data-ttu-id="0fbc9-122">Nach dem Ausführen von `updateuid` sollten Ihre Dateien UIDs enthalten.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-122">After running `updateuid`, your files should contain Uids.</span></span> <span data-ttu-id="0fbc9-123">In der *"Pane1. XAML* -Datei von HelloApp sollten Sie z. b. Folgendes finden:</span><span class="sxs-lookup"><span data-stu-id="0fbc9-123">For example, in the *Pane1.xaml* file of HelloApp, you should find the following:</span></span>  

   ```xaml
   <StackPanel x:Uid="StackPanel_1">
     <TextBlock x:Uid="TextBlock_1">Hello World</TextBlock>
     <TextBlock x:Uid="TextBlock_2">Goodbye World</TextBlock>
   </StackPanel>
   ```

## <a name="create-the-neutral-language-resources-satellite-assembly"></a><span data-ttu-id="0fbc9-124">Erstellen der Satellitenassembly für neutrale Sprachressourcen</span><span class="sxs-lookup"><span data-stu-id="0fbc9-124">Create the neutral-language resources satellite assembly</span></span>

<span data-ttu-id="0fbc9-125">Nachdem die Anwendung so konfiguriert wurde, dass Sie eine Satellitenassembly mit neutralen Sprachressourcen generiert, erstellen Sie die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-125">After the application is configured to generate a neutral-language resources satellite assembly, you build the application.</span></span> <span data-ttu-id="0fbc9-126">Dadurch wird die Hauptanwendungsassembly und die Satellitenassembly für die neutrale Sprache generiert, die von LocBaml für die Lokalisierung benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-126">This generates the main application assembly as well as the neutral-language resources satellite assembly that's required by LocBaml for localization.</span></span>

<span data-ttu-id="0fbc9-127">So erstellen Sie die Anwendung:</span><span class="sxs-lookup"><span data-stu-id="0fbc9-127">To build the application:</span></span>  
  
1. <span data-ttu-id="0fbc9-128">Kompilieren Sie HelloApp, um eine Dynamic Link Library (dll) zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="0fbc9-128">Compile HelloApp to create a dynamic-link library (DLL):</span></span>  
  
   `msbuild helloapp.csproj`
  
2. <span data-ttu-id="0fbc9-129">Die neu erstellte Hauptanwendungsassembly, HelloApp.exe, wird im folgenden Ordner erstellt: *c:\helloapp\bin\debug*</span><span class="sxs-lookup"><span data-stu-id="0fbc9-129">The newly created main application assembly, HelloApp.exe, is created in the following folder: *C:\HelloApp\Bin\Debug*</span></span>
  
3. <span data-ttu-id="0fbc9-130">Die neu erstellte Satellitenassembly für neutrale Sprachressourcen, HelloApp.resources.dll, wird im folgenden Ordner erstellt: *c:\helloapp\bin\debug\de-US*</span><span class="sxs-lookup"><span data-stu-id="0fbc9-130">The newly created neutral-language resources satellite assembly, HelloApp.resources.dll, is created in the following folder: *C:\HelloApp\Bin\Debug\en-US*</span></span>
  
## <a name="build-the-locbaml-tool"></a><span data-ttu-id="0fbc9-131">Erstellen des LocBaml-Tools</span><span class="sxs-lookup"><span data-stu-id="0fbc9-131">Build the LocBaml tool</span></span>  
  
1. <span data-ttu-id="0fbc9-132">Alle Dateien, die zum Erstellen von LocBaml erforderlich sind, befinden sich in den WPF-Beispielen.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-132">All the files necessary to build LocBaml are located in the WPF samples.</span></span> <span data-ttu-id="0fbc9-133">Laden Sie die c#-Dateien aus dem [LocBaml-Tool Beispiel](https://github.com/microsoft/WPF-Samples/tree/master/Tools/LocBaml)herunter.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-133">Download the C# files from the [LocBaml Tool Sample](https://github.com/microsoft/WPF-Samples/tree/master/Tools/LocBaml).</span></span>  
  
2. <span data-ttu-id="0fbc9-134">Führen Sie über die Befehlszeile die Projektdatei (locbaml.csproj) aus, um das Tool zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="0fbc9-134">From the command line, run the project file (locbaml.csproj) to build the tool:</span></span>  

   `msbuild locbaml.csproj`
  
3. <span data-ttu-id="0fbc9-135">Wechseln Sie zum Verzeichnis " *bin\Release* ", um die neu erstellte ausführbare Datei (locbaml.exe) zu suchen.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-135">Go to the *Bin\Release* directory to find the newly created executable file (locbaml.exe).</span></span> <span data-ttu-id="0fbc9-136">Beispiel: *C:\LocBaml\Bin\Release\locbaml.exe*</span><span class="sxs-lookup"><span data-stu-id="0fbc9-136">Example: *C:\LocBaml\Bin\Release\locbaml.exe*</span></span>
  
4. <span data-ttu-id="0fbc9-137">Die Optionen, die Sie beim Ausführen von LocBaml angeben können, sind wie folgt.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-137">The options that you can specify when you run LocBaml are as follows.</span></span>

   | <span data-ttu-id="0fbc9-138">Option</span><span class="sxs-lookup"><span data-stu-id="0fbc9-138">Option</span></span> | <span data-ttu-id="0fbc9-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fbc9-139">Description</span></span>|
   | - | - |
   | <span data-ttu-id="0fbc9-140">`parse` oder `-p`</span><span class="sxs-lookup"><span data-stu-id="0fbc9-140">`parse` or `-p`</span></span> | <span data-ttu-id="0fbc9-141">Analysiert BAML-, Ressourcen-oder DLL-Dateien, um eine CSV-oder txt-Datei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-141">Parses Baml, resources, or DLL files to generate a .csv or .txt file.</span></span> |
   | <span data-ttu-id="0fbc9-142">`generate` oder `-g`</span><span class="sxs-lookup"><span data-stu-id="0fbc9-142">`generate` or `-g`</span></span> | <span data-ttu-id="0fbc9-143">Generiert eine lokalisierte Binärdatei, indem eine übersetzte Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-143">Generates a localized binary file by using a translated file.</span></span> |
   | <span data-ttu-id="0fbc9-144">`out` oder `-o` {*File Directory*]</span><span class="sxs-lookup"><span data-stu-id="0fbc9-144">`out` or `-o` {*filedirectory*]</span></span> | <span data-ttu-id="0fbc9-145">Der Name der Ausgabedatei.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-145">Output file name.</span></span> |
   | <span data-ttu-id="0fbc9-146">`culture` oder `-cul` {*Culture*]</span><span class="sxs-lookup"><span data-stu-id="0fbc9-146">`culture` or `-cul` {*culture*]</span></span> | <span data-ttu-id="0fbc9-147">Locale der Ausgabeassemblys</span><span class="sxs-lookup"><span data-stu-id="0fbc9-147">Locale of output assemblies.</span></span> |
   | <span data-ttu-id="0fbc9-148">`translation` oder `-trans` {*translation.csv*]</span><span class="sxs-lookup"><span data-stu-id="0fbc9-148">`translation` or `-trans` {*translation.csv*]</span></span> | <span data-ttu-id="0fbc9-149">Übersetzte oder lokalisierte Datei.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-149">Translated or localized file.</span></span> |
   | <span data-ttu-id="0fbc9-150">`asmpath` oder `-asmpath` {*File Directory*]</span><span class="sxs-lookup"><span data-stu-id="0fbc9-150">`asmpath` or `-asmpath` {*filedirectory*]</span></span> | <span data-ttu-id="0fbc9-151">Wenn Ihr XAML-Code benutzerdefinierte Steuerelemente enthält, müssen Sie `asmpath` für die benutzerdefinierte Steuerelement-Assembly bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-151">If your XAML code contains custom controls, you must supply the `asmpath` to the custom control assembly.</span></span> |
   | `nologo` | <span data-ttu-id="0fbc9-152"> Bewirkt, dass weder ein Logo noch Copyrightinformationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-152">Displays no logo or copyright information.</span></span> |
   | `verbose` | <span data-ttu-id="0fbc9-153"> Bewirkt, dass Informationen im ausführlichen Modus angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-153">Displays verbose mode information.</span></span> |
  
   > [!NOTE]
   > <span data-ttu-id="0fbc9-154">Wenn Sie beim Ausführen des Tools eine Liste der Optionen benötigen, geben Sie ein, `LocBaml.exe` und drücken Sie dann die **Eingabe** Taste.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-154">If you need a list of the options when you are running the tool, enter `LocBaml.exe` and then press **Enter**.</span></span>
  
## <a name="use-locbaml-to-parse-a-file"></a><span data-ttu-id="0fbc9-155">Verwenden von LocBaml zum Analysieren einer Datei</span><span class="sxs-lookup"><span data-stu-id="0fbc9-155">Use LocBaml to parse a file</span></span>

<span data-ttu-id="0fbc9-156">Nachdem Sie das LocBaml-Tool erstellt haben, können Sie es verwenden, um "HelloApp.resources.dll" zu analysieren, um den Textinhalt zu extrahieren, der lokalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-156">Now that you have created the LocBaml tool, you are ready to use it to parse HelloApp.resources.dll to extract the text content that will be localized.</span></span>  
  
1. <span data-ttu-id="0fbc9-157">Kopieren Sie "LocBaml.exe" in den "bin\debug"-Ordner Ihrer Anwendung, in dem die Hauptanwendungsassembly erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-157">Copy LocBaml.exe to your application's bin\debug folder, where the main application assembly was created.</span></span>  
  
2. <span data-ttu-id="0fbc9-158">Um die Satellitenassemblydatei zu analysieren und die Ausgabe als CSV-Datei zu speichern, verwenden Sie den folgenden Befehl ein:</span><span class="sxs-lookup"><span data-stu-id="0fbc9-158">To parse the satellite assembly file and store the output as a .csv file, use the following command:</span></span>  
  
   `LocBaml.exe /parse HelloApp.resources.dll /out:Hello.csv`
  
   > [!NOTE]
   > <span data-ttu-id="0fbc9-159">Wenn sich die Eingabedatei "HelloApp.resources.dll" nicht im selben Ordner wie "LocBaml.exe" befindet, verschieben Sie eine der Dateien, damit sich beide Dateien im selben Verzeichnis befinden.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-159">If the input file, HelloApp.resources.dll, is not in the same directory as LocBaml.exe move one of the files so that both files are in the same directory.</span></span>  
  
3. <span data-ttu-id="0fbc9-160">Wenn Sie LocBaml ausführen, um Dateien zu analysieren, besteht die Ausgabe aus sieben Feldern, die jeweils durch Kommas (CSV-Dateien) oder Tabulatoren (TXT-Dateien) getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-160">When you run LocBaml to parse files, the output consists of seven fields delimited by commas (.csv files) or tabs (.txt files).</span></span> <span data-ttu-id="0fbc9-161">Nachstehend ist die bei der Analyse erstellte CSV-Datei für "HelloApp.Resources.dll" gezeigt:</span><span class="sxs-lookup"><span data-stu-id="0fbc9-161">The following shows the parsed .csv file for the HelloApp.resources.dll:</span></span>

   | |
   |-|
   |<span data-ttu-id="0fbc9-162">HelloApp.g.en-US.resources:window1.baml,Stack1:System.Windows.Controls.StackPanel.$Content,Ignore,FALSE, FALSE,,#Text1;#Text2;</span><span class="sxs-lookup"><span data-stu-id="0fbc9-162">HelloApp.g.en-US.resources:window1.baml,Stack1:System.Windows.Controls.StackPanel.$Content,Ignore,FALSE, FALSE,,#Text1;#Text2;</span></span>|
   |<span data-ttu-id="0fbc9-163">HelloApp.g.en-US.resources:window1.baml,Text1:System.Windows.Controls.TextBlock.$Content,None,TRUE, TRUE,,Hello World</span><span class="sxs-lookup"><span data-stu-id="0fbc9-163">HelloApp.g.en-US.resources:window1.baml,Text1:System.Windows.Controls.TextBlock.$Content,None,TRUE, TRUE,,Hello World</span></span>|
   |<span data-ttu-id="0fbc9-164">HelloApp.g.en-US.resources:window1.baml,Text2:System.Windows.Controls.TextBlock.$Content,None,TRUE, TRUE,,Goodbye World</span><span class="sxs-lookup"><span data-stu-id="0fbc9-164">HelloApp.g.en-US.resources:window1.baml,Text2:System.Windows.Controls.TextBlock.$Content,None,TRUE, TRUE,,Goodbye World</span></span>|

   <span data-ttu-id="0fbc9-165">Die sieben Felder sind:</span><span class="sxs-lookup"><span data-stu-id="0fbc9-165">The seven fields are:</span></span>  
  
   - <span data-ttu-id="0fbc9-166">**BAML-Name**.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-166">**BAML Name**.</span></span> <span data-ttu-id="0fbc9-167">Der Name der BAML-Ressource bezogen auf die Satellitenassembly für die Ausgangssprache.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-167">The name of the BAML resource with respect to the source language satellite assembly.</span></span>  
  
   - <span data-ttu-id="0fbc9-168">**Ressourcen Schlüssel**.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-168">**Resource Key**.</span></span> <span data-ttu-id="0fbc9-169">Der lokalisierte Ressourcenbezeichner.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-169">The localized resource identifier.</span></span>  
  
   - <span data-ttu-id="0fbc9-170">**Kategorie**</span><span class="sxs-lookup"><span data-stu-id="0fbc9-170">**Category**.</span></span> <span data-ttu-id="0fbc9-171">Der Werttyp.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-171">The value type.</span></span> <span data-ttu-id="0fbc9-172">Siehe [Lokalisierungs Attribute und-Kommentare](localization-attributes-and-comments.md).</span><span class="sxs-lookup"><span data-stu-id="0fbc9-172">See [Localization Attributes and Comments](localization-attributes-and-comments.md).</span></span>  
  
   - <span data-ttu-id="0fbc9-173">**Lesbarkeit**.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-173">**Readability**.</span></span> <span data-ttu-id="0fbc9-174">Gibt an, ob der Wert von einem Lokalisierungstool gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-174">Whether the value can be read by a localizer.</span></span> <span data-ttu-id="0fbc9-175">Siehe [Lokalisierungs Attribute und-Kommentare](localization-attributes-and-comments.md).</span><span class="sxs-lookup"><span data-stu-id="0fbc9-175">See [Localization Attributes and Comments](localization-attributes-and-comments.md).</span></span>  
  
   - <span data-ttu-id="0fbc9-176">**Änderbarkeit**.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-176">**Modifiability**.</span></span> <span data-ttu-id="0fbc9-177">Gibt an, ob der Wert von einem Lokalisierungstool geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-177">Whether the value can be modified by a localizer.</span></span> <span data-ttu-id="0fbc9-178">Siehe [Lokalisierungs Attribute und-Kommentare](localization-attributes-and-comments.md).</span><span class="sxs-lookup"><span data-stu-id="0fbc9-178">See [Localization Attributes and Comments](localization-attributes-and-comments.md).</span></span>  
  
   - <span data-ttu-id="0fbc9-179">**Kommentare**.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-179">**Comments**.</span></span> <span data-ttu-id="0fbc9-180">Zusätzliche Beschreibung des Werts, um zu ermitteln, wie ein Wert lokalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-180">Additional description of the value to help determine how a value is localized.</span></span> <span data-ttu-id="0fbc9-181">Siehe [Lokalisierungs Attribute und-Kommentare](localization-attributes-and-comments.md).</span><span class="sxs-lookup"><span data-stu-id="0fbc9-181">See [Localization Attributes and Comments](localization-attributes-and-comments.md).</span></span>  
  
   - <span data-ttu-id="0fbc9-182">**Wert**.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-182">**Value**.</span></span> <span data-ttu-id="0fbc9-183">Der Textwert, der in die gewünschte Sprache übersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-183">The text value to translate to the desired culture.</span></span>  
  
   <span data-ttu-id="0fbc9-184">Die folgende Tabelle zeigt, wie diese Felder den durch Trennzeichen getrennten Werten der CSV-Datei zugeordnet sind:</span><span class="sxs-lookup"><span data-stu-id="0fbc9-184">The following table shows how these fields map to the delimited values of the .csv file:</span></span>  
  
   |<span data-ttu-id="0fbc9-185">BAML-Name</span><span class="sxs-lookup"><span data-stu-id="0fbc9-185">BAML name</span></span>|<span data-ttu-id="0fbc9-186">Ressourcenschlüssel</span><span class="sxs-lookup"><span data-stu-id="0fbc9-186">Resource key</span></span>|<span data-ttu-id="0fbc9-187">Category</span><span class="sxs-lookup"><span data-stu-id="0fbc9-187">Category</span></span>|<span data-ttu-id="0fbc9-188">Lesbarkeit</span><span class="sxs-lookup"><span data-stu-id="0fbc9-188">Readability</span></span>|<span data-ttu-id="0fbc9-189">Änderbarkeit</span><span class="sxs-lookup"><span data-stu-id="0fbc9-189">Modifiability</span></span>|<span data-ttu-id="0fbc9-190">Kommentare</span><span class="sxs-lookup"><span data-stu-id="0fbc9-190">Comments</span></span>|<span data-ttu-id="0fbc9-191">Wert</span><span class="sxs-lookup"><span data-stu-id="0fbc9-191">Value</span></span>|  
   |---------------|------------------|--------------|-----------------|-------------------|--------------|-----------|
   |<span data-ttu-id="0fbc9-192">HelloApp.g.en-US.resources:window1.baml</span><span class="sxs-lookup"><span data-stu-id="0fbc9-192">HelloApp.g.en-US.resources:window1.baml</span></span>|<span data-ttu-id="0fbc9-193">Stack1:System.Windows.Controls.StackPanel.$Content</span><span class="sxs-lookup"><span data-stu-id="0fbc9-193">Stack1:System.Windows.Controls.StackPanel.$Content</span></span>|<span data-ttu-id="0fbc9-194">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="0fbc9-194">Ignore</span></span>|<span data-ttu-id="0fbc9-195">FALSE</span><span class="sxs-lookup"><span data-stu-id="0fbc9-195">FALSE</span></span>|<span data-ttu-id="0fbc9-196">FALSE</span><span class="sxs-lookup"><span data-stu-id="0fbc9-196">FALSE</span></span>||<span data-ttu-id="0fbc9-197">#Text1;#Text2</span><span class="sxs-lookup"><span data-stu-id="0fbc9-197">#Text1;#Text2</span></span>|
   |<span data-ttu-id="0fbc9-198">HelloApp.g.en-US.resources:window1.baml</span><span class="sxs-lookup"><span data-stu-id="0fbc9-198">HelloApp.g.en-US.resources:window1.baml</span></span>|<span data-ttu-id="0fbc9-199">Text1:System.Windows.Controls.TextBlock.$Content</span><span class="sxs-lookup"><span data-stu-id="0fbc9-199">Text1:System.Windows.Controls.TextBlock.$Content</span></span>|<span data-ttu-id="0fbc9-200">Keine</span><span class="sxs-lookup"><span data-stu-id="0fbc9-200">None</span></span>|<span data-ttu-id="0fbc9-201">TRUE</span><span class="sxs-lookup"><span data-stu-id="0fbc9-201">TRUE</span></span>|<span data-ttu-id="0fbc9-202">TRUE</span><span class="sxs-lookup"><span data-stu-id="0fbc9-202">TRUE</span></span>||<span data-ttu-id="0fbc9-203">Hello World</span><span class="sxs-lookup"><span data-stu-id="0fbc9-203">Hello World</span></span>|
   |<span data-ttu-id="0fbc9-204">HelloApp.g.en-US.resources:window1.baml</span><span class="sxs-lookup"><span data-stu-id="0fbc9-204">HelloApp.g.en-US.resources:window1.baml</span></span>|<span data-ttu-id="0fbc9-205">Text2:System.Windows.Controls.TextBlock.$Content</span><span class="sxs-lookup"><span data-stu-id="0fbc9-205">Text2:System.Windows.Controls.TextBlock.$Content</span></span>|<span data-ttu-id="0fbc9-206">Keine</span><span class="sxs-lookup"><span data-stu-id="0fbc9-206">None</span></span>|<span data-ttu-id="0fbc9-207">TRUE</span><span class="sxs-lookup"><span data-stu-id="0fbc9-207">TRUE</span></span>|<span data-ttu-id="0fbc9-208">TRUE</span><span class="sxs-lookup"><span data-stu-id="0fbc9-208">TRUE</span></span>||<span data-ttu-id="0fbc9-209">Goodbye World</span><span class="sxs-lookup"><span data-stu-id="0fbc9-209">Goodbye World</span></span>|
  
   <span data-ttu-id="0fbc9-210">Beachten Sie, dass alle Werte für das Feld **Kommentare** keine Werte enthalten. Wenn ein Feld keinen Wert hat, ist es leer.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-210">Notice that all the values for the **Comments** field contain no values; if a field doesn't have a value, it is empty.</span></span> <span data-ttu-id="0fbc9-211">Beachten Sie auch, dass das Element in der ersten Zeile weder lesbar noch änderbar ist und "Ignore" als **Kategoriewert** aufweist. Dies bedeutet, dass der Wert nicht lokalisierbar ist.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-211">Also notice that the item in the first row is neither readable nor modifiable, and has "Ignore" as its **Category** value, all of which indicates that the value is not localizable.</span></span>  
  
4. <span data-ttu-id="0fbc9-212">Um die Ermittlung Lokalisier barer Elemente in analysierten Dateien, insbesondere in großen Dateien, zu vereinfachen, können Sie die Elemente nach **Kategorie**, **Lesbarkeit** und **Änderbarkeit** sortieren oder filtern.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-212">To facilitate discovery of localizable items in parsed files, particularly in large files, you can sort or filter the items by **Category**, **Readability**, and **Modifiability**.</span></span> <span data-ttu-id="0fbc9-213">Beispielsweise können Sie nicht lesbare und nicht änderbare Werte herausfiltern.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-213">For example, you can filter out unreadable and unmodifiable values.</span></span>  
  
## <a name="translate-the-localizable-content"></a><span data-ttu-id="0fbc9-214">Übersetzen des lokalisierbaren Inhalts</span><span class="sxs-lookup"><span data-stu-id="0fbc9-214">Translate the localizable content</span></span>

<span data-ttu-id="0fbc9-215">Verwenden Sie ein beliebiges Tool, das Ihnen zur Verfügung steht, um den extrahierten Inhalt zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-215">Use any tool that you have available to translate the extracted content.</span></span> <span data-ttu-id="0fbc9-216">Eine gute Möglichkeit hierfür besteht darin, die Ressourcen in eine CSV-Datei zu schreiben und Sie in Microsoft Excel anzuzeigen, sodass Übersetzungsänderungen an der letzten Spalte (Wert) vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-216">A good way to do this is to write the resources to a .csv file and view them in Microsoft Excel, making translation changes to the last column (value).</span></span>  
  
## <a name="use-locbaml-to-generate-a-new-resourcesdll-file"></a><span data-ttu-id="0fbc9-217">Verwenden von LocBaml zum Generieren einer neuen .resources.dll Datei</span><span class="sxs-lookup"><span data-stu-id="0fbc9-217">Use LocBaml to generate a new .resources.dll file</span></span>

<span data-ttu-id="0fbc9-218">Die Inhalte, die durch das Analysieren von "HelloApp.resources.dll" mit LocBaml erkannt wurden, sind nun übersetzt und müssen wieder mit der ursprünglichen Anwendung zusammengeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-218">The content that was identified by parsing HelloApp.resources.dll with LocBaml has been translated and must be merged back into the original application.</span></span> <span data-ttu-id="0fbc9-219">Verwenden `generate` Sie die `-g` Option oder, um eine neue .resources.dll Datei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-219">Use the `generate` or `-g` option to generate a new .resources.dll file.</span></span>  
  
1. <span data-ttu-id="0fbc9-220">Verwenden Sie die folgende Syntax, um eine neue "HelloApp.resources.dll"-Datei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-220">Use the following syntax to generate a new HelloApp.resources.dll file.</span></span> <span data-ttu-id="0fbc9-221">Kennzeichnen Sie die Kultur als "en-US" (/cul:en-US).</span><span class="sxs-lookup"><span data-stu-id="0fbc9-221">Mark the culture as en-US (/cul:en-US).</span></span>  
  
   `LocBaml.exe /generate HelloApp.resources.dll /trans:Hello.csv /out:c:\ /cul:en-US`  

   > [!NOTE]
   > <span data-ttu-id="0fbc9-222">Wenn sich die Eingabedatei, "HelloApp.resources.dll", nicht im selben Ordner wie die ausführbare Datei, "LocBaml.exe", befindet, verschieben Sie eine der Dateien, damit sich beide Dateien im selben Verzeichnis befinden.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-222">If the input file, Hello.csv, is not in the same directory as the executable, LocBaml.exe, move one of the files so that both files are in the same directory.</span></span>  
  
2. <span data-ttu-id="0fbc9-223">Ersetzen Sie die alte *HelloApp.resources.dll* Datei im *C:\HelloApp\Bin\Debug\en-US\HelloApp.resources.dll* Verzeichnis durch die neu erstellte *HelloApp.resources.dll* Datei.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-223">Replace the old *HelloApp.resources.dll* file in the *C:\HelloApp\Bin\Debug\en-US\HelloApp.resources.dll* directory with your newly created *HelloApp.resources.dll* file.</span></span>  
  
3. <span data-ttu-id="0fbc9-224">"Hello World" und "Goodbye World" sollten jetzt in Ihrer Anwendung übersetzt sein.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-224">"Hello World" and "Goodbye World" should now be translated in your application.</span></span>  
  
4. <span data-ttu-id="0fbc9-225">Um in eine andere Kultur zu übersetzen, verwenden Sie die Kultur der Sprache, in die Sie übersetzen.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-225">To translate to a different culture, use the culture of the language that you are translating to.</span></span> <span data-ttu-id="0fbc9-226">Das folgende Beispiel zeigt, wie in kanadisches Französisch übersetzt wird:</span><span class="sxs-lookup"><span data-stu-id="0fbc9-226">The following example shows how to translate to French-Canadian:</span></span>  
  
   `LocBaml.exe /generate HelloApp.resources.dll /trans:Hellofr-CA.csv /out:c:\ /cul:fr-CA`  
  
5. <span data-ttu-id="0fbc9-227">Erstellen Sie in dem Ordner, in dem sich die Hauptanwendungsassembly befindet, einen neuen kulturspezifischen Ordner, der die neue Satellitenassembly aufnehmen soll.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-227">In the same assembly as the main application assembly, create a new culture-specific folder to house the new satellite assembly.</span></span> <span data-ttu-id="0fbc9-228">Für kanadisches Französisch ist dies der Ordner "fr-CA".</span><span class="sxs-lookup"><span data-stu-id="0fbc9-228">For French-Canadian, the folder would be fr-CA.</span></span>  
  
6. <span data-ttu-id="0fbc9-229">Kopieren Sie die generierte Satellitenassembly in den neuen Ordner.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-229">Copy the generated satellite assembly to the new folder.</span></span>  
  
7. <span data-ttu-id="0fbc9-230">Um die neue Satellitenassembly zu testen, müssen Sie die Kultur ändern, unter der Ihre Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-230">To test the new satellite assembly, you need to change the culture under which your application will run.</span></span> <span data-ttu-id="0fbc9-231">Dazu haben Sie zwei Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="0fbc9-231">You can do this in one of two ways:</span></span>  
  
   - <span data-ttu-id="0fbc9-232">Ändern Sie die regionalen Einstellungen des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-232">Change your operating system's regional settings.</span></span>
  
   - <span data-ttu-id="0fbc9-233">Fügen Sie in Ihrer Anwendung den folgenden Code in "App.xaml.cs" hinzu:</span><span class="sxs-lookup"><span data-stu-id="0fbc9-233">In your application, add the following code to App.xaml.cs:</span></span>  
  
     [!code-xaml[LocBamlChangeCultureSnippets#LocBamlChangeCultureMARKUP](~/samples/snippets/csharp/VS_Snippets_Wpf/LocBamlChangeCultureSnippets/CSharp/App.xaml#locbamlchangeculturemarkup)]
     [!code-csharp[LocBamlChangeCultureSnippets#LocBamlChangeCultureCODEBEHIND](~/samples/snippets/csharp/VS_Snippets_Wpf/LocBamlChangeCultureSnippets/CSharp/App.xaml.cs#locbamlchangeculturecodebehind)]
     [!code-vb[LocBamlChangeCultureSnippets#LocBamlChangeCultureCODEBEHIND](~/samples/snippets/visualbasic/VS_Snippets_Wpf/LocBamlChangeCultureSnippets/VisualBasic/Application.xaml.vb#locbamlchangeculturecodebehind)]  
  
## <a name="tips-for-using-locbaml"></a><span data-ttu-id="0fbc9-234">Tipps für die Verwendung von LocBaml</span><span class="sxs-lookup"><span data-stu-id="0fbc9-234">Tips for Using LocBaml</span></span>  
  
- <span data-ttu-id="0fbc9-235">Alle abhängigen Assemblys, die benutzerdefinierte Steuerelemente definieren, müssen in das lokale Verzeichnis von LocBaml kopiert oder im globalen Assemblycache (GAC) installiert werden.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-235">All dependent assemblies that define custom controls must be copied into the local directory of LocBaml or installed into the GAC.</span></span> <span data-ttu-id="0fbc9-236">Dies ist erforderlich, da die Lokalisierungs-API Zugriff auf die abhängigen Assemblys haben muss, wenn Sie das binäre XAML (BAML) liest.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-236">This is necessary because the localization API must have access to the dependent assemblies when it reads the binary XAML (BAML).</span></span>  
  
- <span data-ttu-id="0fbc9-237">Wenn die Hauptassembly signiert ist, muss auch die generierte Ressourcen-DLL signiert sein, damit sie geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-237">If the main assembly is signed, the generated resource DLL must also be signed in order for it to be loaded.</span></span>  
  
- <span data-ttu-id="0fbc9-238">Die Version der lokalisierten Ressourcen-DLL muss mit der Hauptassembly synchronisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0fbc9-238">The version of the localized resource DLL needs to be synchronized with the main assembly.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0fbc9-239">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fbc9-239">See also</span></span>

- [<span data-ttu-id="0fbc9-240">Globalisierung für WPF</span><span class="sxs-lookup"><span data-stu-id="0fbc9-240">Globalization for WPF</span></span>](globalization-for-wpf.md)
- [<span data-ttu-id="0fbc9-241">Übersicht über die Verwendung eines automatischen Layouts</span><span class="sxs-lookup"><span data-stu-id="0fbc9-241">Use Automatic Layout Overview</span></span>](use-automatic-layout-overview.md)
