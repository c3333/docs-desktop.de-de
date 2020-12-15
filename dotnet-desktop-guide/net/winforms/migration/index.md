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
# <a name="how-to-migrate-a-windows-forms-desktop-app-to-net-5"></a>Migrieren einer Windows Forms-Desktopanwendung zu .NET 5

In diesem Artikel wird beschrieben, wie eine Windows Forms-Desktopanwendung von .NET Framework zu .NET 5 oder höher migriert wird. Das .NET SDK bietet Unterstützung für Windows Forms-Anwendungen. Windows Forms ist immer noch ein ausschließlich für Windows bestimmtes Framework und kann nur unter Windows ausgeführt.

Für die Migration einer Anwendung von .NET Framework zu .NET 5 ist im Allgemeinen eine neue Projektdatei erforderlich. Bei .NET 5 werden Projektdateien im SDK-Format verwendet, während bei .NET Framework in der Regel ältere Visual Studio-Projektdateien zum Einsatz kommen. Wenn Sie jemals eine Visual Studio-Projektdatei in einem Text-Editor geöffnet haben, wissen Sie, wie detailliert diese ist. Projekte im SDK-Format sind kleiner und erfordern weniger Einträge als Projekte im älteren Dateiformat.

Weitere Informationen zu .NET 5 finden Sie unter [Einführung in .NET](/dotnet/core/introduction).

## <a name="prerequisites"></a>Voraussetzungen

- [Visual Studio 2019, Version 16.8, Vorschauversion](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019+desktopguide+winforms)

  - Wählen Sie die [Visual Studio-Desktop-Workload](/visualstudio/install/modify-visual-studio?view=vs-2019&preserve-view=true#modify-workloads) aus.

  - Wählen Sie die [jeweilige .NET 5-Komponente](/visualstudio/install/modify-visual-studio?view=vs-2019&preserve-view=true#modify-individual-components) aus.

- Vorschauversion des WinForms-Designers in Visual Studio.

  Um den Designer zu aktivieren, wechseln Sie zu **Extras** > **Optionen** > **Umgebung** > **Vorschaufeatures**, und wählen Sie Option **Use the preview Windows Forms designer for .NET Core apps** (Vorschauversion des Windows Forms-Designers für .NET Core-Apps verwenden) aus.

- In diesem Artikel wird die Beispielanwendung [Vergleichsspiel](https://github.com/dotnet/samples/tree/master/windowsforms/matching-game/net45/) verwendet. Wenn Sie diese Anwendung verwenden möchten, laden Sie sie herunter, und öffnen Sie sie in Visual Studio. Andernfalls verwenden Sie Ihre eigene Anwendung.

### <a name="consider"></a>Consider

Wenn Sie eine .NET Framework Windows Forms-Anwendung migrieren, müssen Sie ein paar Dinge berücksichtigen.

01. Überprüfen Sie, ob Ihre Anwendung ein guter Kandidat für die Migration ist.

    Verwenden Sie [.NET Portability Analyzer](/dotnet/standard/analyzers/portability-analyzer), um zu bestimmen, ob Ihr Projekt zu .NET 5 migriert werden kann. Wenn bei Ihrem Projekt Probleme mit .NET 5 vorliegen, können Sie diese Probleme mit dem Analyzer identifizieren. Das Tool .NET Portability Analyzer kann als Visual Studio-Erweiterung installiert oder über die Befehlszeile verwendet werden. Weitere Informationen finden Sie unter [.NET Portability Analyzer](/dotnet/standard/analyzers/portability-analyzer).

01. Sie verwenden eine andere Version von Windows Forms.

    Als .NET Core 3.0 veröffentlicht wurde, wurde Windows Forms als [Open-Source-Version auf GitHub](https://github.com/dotnet/winforms) zur Verfügung gestellt. Der Code für Windows Forms für .NET 5 ist ein Fork der .NET Framework-Windows Forms-Codebasis. Es ist möglich, dass einige Unterschiede bestehen, und Ihre Anwendung schwierig zu migrieren ist.

01. Das [Windows Compatibility Pack][compat-pack] könnte Ihnen bei der Migration helfen.

    Einige APIs, die in .NET Framework verfügbar sind, sind nicht in .NET 5 verfügbar. Das [Windows Compatibility Pack][compat-pack] fügt viele dieser APIs hinzu und könnte zur Kompatibilität Ihrer Windows Forms-App mit .NET 5 beitragen.

01. Aktualisieren Sie die NuGet-Pakete, die von Ihrem Projekt verwendet werden.

    Es hat sich bewährt, vor jeder Migration die neuesten Versionen der NuGet-Pakete zu verwenden. Wenn Ihre Anwendung auf NuGet-Pakete verweist, aktualisieren Sie sie auf die neueste Version. Stellen Sie sicher, dass die Anwendung erfolgreich erstellt wird. Wenn nach dem Upgrade Paketfehler auftreten, stufen Sie das Paket auf die neueste Version herab, die Ihren Code nicht beschädigt.

## <a name="back-up-your-projects"></a>Sichern von Projekten

Beim Migrieren eines Projekts müssen Sie das Projekt zunächst einmal sichern. Wenn etwas schief geht, können Sie Ihren Code in den ursprünglichen Zustand zurückversetzen, indem Sie die Sicherung wiederherstellen. Verlassen Sie sich beim Sichern eines Projekts nicht auf Tools wie .NET Portability Analyzer. Am besten erstellen Sie selbst eine Kopie des ursprünglichen Projekts.

## <a name="nuget-packages"></a>NuGet-Pakete

Wenn Ihr Projekt auf NuGet-Pakete verweist, befindet sich in Ihrem Projektordner vermutlich eine **packages.config**-Datei. Bei Projekten im SDK-Format werden NuGet-Paketverweise in der Projektdatei konfiguriert. In Visual Studio-Projektdateien können optional ebenfalls NuGet-Pakete definiert werden. Bei .NET 5 werden für NuGet-Pakete keine **packages.config**-Dateien verwendet. NuGet-Paketverweise müssen vor der Migration in die Projektdatei migriert werden.

Gehen Sie wie folgt vor, um die **packages.config**-Datei zu migrieren:

01. Suchen Sie in **Projektmappen-Explorer** nach dem Projekt, das migriert werden soll.
02. Klicken Sie mit der rechten Maustaste auf **packages.config** >  **„packages.config“ zu PackageReference migrieren**.
03. Wählen Sie alle Pakete auf oberster Ebene aus.

Es wird ein Buildbericht erstellt, um Sie über mögliche Probleme bei der Migration der NuGet-Pakete zu informieren.

## <a name="project-file"></a>Projektdatei

Als Nächstes müssen Sie bei der Migration einer Anwendung die Projektdatei konvertieren. Wie bereits erwähnt, werden bei .NET 5 Projektdateien im SDK-Format verwendet. Visual Studio-Projektdateien, die bei .NET Framework verwendet werden, werden nicht geladen. Es kann jedoch sein, das Sie bereits Projekte im SDK-Format verwenden. Den Unterschied können Sie in Visual Studio leicht erkennen. Klicken Sie mit der rechten Maustaste in **Projektmappen-Explorer**, und suchen Sie nach der Menüoption **Projektdatei bearbeiten**. Wenn dieses Menüelement nicht angezeigt wird, verwenden Sie das alte Visual Studio-Projektformat und müssen ein Upgrade ausführen.

Konvertieren alle Projekte in Ihrer Projektmappe. Wenn Sie die bereits erwähnte Beispielanwendung verwenden, werden die beiden Projekte **MatchingGame** und **MatchingGame.Logic** konvertiert.

Gehen Sie wie folgt vor, um ein Projekt zu konvertieren:

01. Suchen Sie in **Projektmappen-Explorer** nach dem Projekt, das migriert werden soll.
01. Klicken Sie mit der rechten Maustaste auf das Projekt, und wählen Sie **Projekt entladen** aus.
01. Klicken Sie mit der rechten Maustaste auf das Projekt, und wählen Sie **Projektdatei bearbeiten** aus.
01. Kopieren Sie den XML-Code des Projekt, und fügen Sie ihn in einen Text-Editor ein. Sie sollten eine Kopie verwenden, sodass Sie ohne großen Aufwand Inhalte in das neue Projekt verschieben können.
01. Löschen Sie den Inhalt der Datei, und fügen Sie den folgenden XML-Code ein:

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
    > Mit Bibliotheken muss keine `<OutputType>`-Einstellung definiert werden. Entfernen Sie diesen Eintrag, wenn Sie ein Bibliotheksprojekt aktualisieren.

Dieser XML-Code stellt die grundlegende Struktur des Projekts dar. Er enthält jedoch keine Einstellung aus der alten Projektdatei. Führen Sie die folgenden Schritte aus, und verwenden Sie dabei die zuvor in einen Text-Editor kopierten alten Projektinformationen:

01. Kopieren Sie die folgenden Elemente aus der alten Projektdatei in das `<PropertyGroup>`-Element in der neuen Projektdatei:

    - `<RootNamespace>`
    - `<AssemblyName>`

    Die Projektdatei sollte in etwa wie der folgende XML-Code aussehen:

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

01. Kopieren Sie die `<ItemGroup>`-Elemente aus der alten Projektdatei, zu denen `<ProjectReference>` oder `<PackageReference>` gehört, in der neuen Datei an eine Stelle nach dem schließenden Tag `</PropertyGroup>`.

    Die Projektdatei sollte in etwa wie der folgende XML-Code aussehen:

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

    Da die `<ProjectReference>`-Elemente keine untergeordneten `<Project>`- und `<Name>`-Elemente benötigen, können Sie diese Einstellungen entfernen:

    ```xml
    <ItemGroup>
      <ProjectReference Include="..\MatchingGame.Logic\MatchingGame.Logic.csproj" />
    </ItemGroup>
    ```

### <a name="resources-and-settings"></a>Ressourcen und Einstellungen

Windows Forms-Projekte für .NET Framework enthalten in der Regel andere Dateien, z. B. *Properties/Settings.settings* und *Properties/Resources.resx*. Diese Dateien und alle *resx*-Dateien für Ihre Anwendung (außer *resx*-Formulardateien) müssen migriert werden.

Kopieren Sie diese Einträge aus der alten Projektdatei in ein `<ItemGroup>`-Element im neuen Projekt. Ändern Sie nach dem Kopieren der Einträge alle `<Compile Include="value">`- bzw. `<EmbeddedResource Include="value">`-Elemente so, dass `Update` anstelle von `Include` verwendet wird.

- Importieren Sie die Konfiguration für die *Settings.settings*-Datei. Im `<Compile>`-Element wurde `Include` in `Update` geändert:

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
  > Bei **Visual Basic**-Projekten wird als Standarddatei für Projekteinstellungen der Ordner *My Project*, bei C#-Projekten dagegen der Ordner *Properties* verwendet.
  
- Importieren Sie die Konfiguration für alle *resx*-Dateien, z. B. für die Datei *properties/Resources.resx*. Sowohl im `<Compile>`- als auch im `<EmbeddedResource>`-Element wurde `Include` in `Update` geändert und `<SubType>` wurde aus `<EmbeddedResource>` entfernt:

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
  > Bei **Visual Basic**-Projekten wird als Standarddatei für die Projektressource der Ordner *My Project*, bei C#-Projekten dagegen der Ordner *Properties* verwendet.

### <a name="visual-basic"></a>Visual Basic

Bei Projekten in der Sprache Visual Basic müssen zusätzliche Konfigurationsschritte durchgeführt werden.

01. Importieren Sie die Einstellung *My Project\Application.myapp* der Konfigurationsdatei. Für die Elemente `<None>` und `<Compile>` wird das `Update`-Attribut anstelle des `Include`-Attributs verwendet.

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

01. Fügen Sie dem `<PropertyGroup>`-Element die `<MyType>WindowsForms</MyType>`-Einstellung hinzu:

    ```xml
    <PropertyGroup>
      (contains settings previously described)

      <MyType>WindowsForms</MyType>
    </PropertyGroup>
    ```

    Mit dieser Einstellung werden die `My`-Namespacemember importiert, mit denen Visual Basic-Programmierer vertraut sind.

01. Importieren Sie die vom Projekt definierten Namespaces.

    Mit Visual Basic-Projekten können Namespaces automatisch in jede Codedatei importiert werden. Kopieren Sie die `<ItemGroup>`-Elemente aus der alten Projektdatei, zu denen `<Import>` gehört, in der neuen Datei an eine Stelle nach dem schließenden Tag `</PropertyGroup>`.

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

    Wenn keine `<Import>`-Anweisungen vorhanden sind oder beim Kompilieren des Projekts Fehler auftreten, überprüfen Sie, ob im Projekt zumindest die folgenden `<Import>`-Anweisungen definiert sind:

    ```xml
    <ItemGroup>
      <Import Include="System.Data" />
      <Import Include="System.Drawing" />
      <Import Include="System.Windows.Forms" />
    </ItemGroup>
    ```

01. Kopieren Sie die Einstellungen `<Option*>` und `<StartupObject>` aus dem ursprünglichen Projekt in das `<PropertyGroup>`-Element:

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

### <a name="reload-the-project"></a>Erneutes Laden des Projekts

Nachdem Sie ein Projekt in das neue SDK-Format konvertiert haben, laden Sie das Projekt erneut in Visual Studio:

01. Suchen Sie in **Projektmappen-Explorer** nach dem Projekt, das konvertiert werden soll.
01. Klicken Sie mit der rechten Maustaste auf das Projekt, und wählen Sie **Projekt erneut laden** aus.

    Wenn beim Laden des Projekts ein Fehler auftritt, enthält der XML-Code des Projekts möglicherweise einen Fehler. Öffnen Sie die Projektdatei zur Bearbeitung, suchen Sie nach dem Fehler, und beheben Sie ihn. Wenn Sie keinen Fehler finden, versuchen Sie es noch mal.

## <a name="edit-appconfig"></a>Bearbeiten der Datei „App.config“

Wenn Ihre Anwendung eine *App.config*-Datei enthält, entfernen Sie das `<supportedRuntime>`-Element:

```xml
<supportedRuntime version="v4.0" sku=".NETFramework,Version=v4.5" />
```

Im Zusammenhang mit der Datei *App.config* müssen einige Dinge berücksichtigt werden. Die Datei *App.config* in .NET Framework wurde nicht nur zum Konfigurieren der Anwendung, sondern auch zum Konfigurieren von Laufzeiteinstellungen und Verhaltensweisen wie die Protokollierung verwendet. Ab .NET 5 (und in .NET Core) wird die Datei *App.config* nicht mehr für die Laufzeitkonfiguration verwendet. Wenn Ihre *App.config*-Datei diese Abschnitte enthält, werden diese nicht berücksichtigt.

## <a name="add-the-compatibility-package"></a>Hinzufügen des Kompatibilitätspakets

Wenn Ihre Projektdatei ordnungsgemäß geladen wird, bei der Kompilierung für Ihr Projekt jedoch ein Fehler auftritt und Fehlermeldungen wie die folgende angezeigt werden:

- **Der Typ oder Namespace \<some name> wurde nicht gefunden**
- **Der Name \<some name> ist im aktuellen Kontext nicht vorhanden**

Müssen Sie Ihrer Anwendung möglicherweise das [`Microsoft.Windows.Compatibility`](https://www.nuget.org/packages/Microsoft.Windows.Compatibility/)-Paket hinzufügen. Mit diesem Paket werden etwa 21.000 .NET-APIs aus .NET Framework wie die `System.Configuration.ConfigurationManager`-Klasse und APIs für die Interaktion mit der Windows-Registrierung hinzugefügt. Fügen Sie das Paket `Microsoft.Windows.Compatibility` hinzu.

Bearbeiten Sie die Projektdatei, und fügen Sie das folgende `<ItemGroup>`-Element hinzu:

```xml
<ItemGroup>
  <PackageReference Include="Microsoft.Windows.Compatibility" Version="5.0.0" />
</ItemGroup>
```

## <a name="test-your-app"></a>Testen Ihrer App

Testen Sie Ihre Anwendung, nachdem Sie sie migriert haben.

## <a name="next-steps"></a>Nächste Schritte

- Informieren Sie sich über [Breaking Changes in Windows Forms](/dotnet/core/compatibility/winforms).
- Lesen Sie mehr über das [Windows Compatibility Pack][compat-pack].

[compat-pack]: /dotnet/core/porting/windows-compat-pack
