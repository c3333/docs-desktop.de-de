---
title: Was ist Windows Forms?
description: Dieser Artikel enthält eine Übersicht über Windows Forms mit .NET Core und .NET 5.
ms.date: 10/26/2020
ms.topic: overview
ms.openlocfilehash: a0908891d9391d5820fe75cac69278ddda1b2244
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96992803"
---
# <a name="desktop-guide-windows-forms-net"></a>Desktopleitfaden (Windows Forms .NET)

Willkommen beim Desktopleitfaden zu Windows Forms, einem Benutzeroberflächenframework, mit dem umfangreiche Desktopclientanwendungen für Windows erstellt werden können. Die Entwicklungsplattform Windows Forms unterstützt eine breite Palette an Anwendungsentwicklungsfeatures wie Steuerelemente, Grafiken, Datenbindungen und Benutzereingaben. Windows Forms bietet zum einfachen Erstellen von Windows Forms-Anwendungen einen visuellen Drag & Drop-Designer in Visual Studio.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

Es gibt zwei Implementierungen von Windows Forms:

01. Die Open-Source-Implementierung, die auf [GitHub](https://github.com/dotnet/winforms) gehostet wird.

    Diese Version wird unter .NET 5 und .NET Core 3.1 ausgeführt. Der visuelle Windows Forms-Designer erfordert mindestens [Visual Studio 2019 Version 16.8, Vorschauversion](https://visualstudio.microsoft.com/downloads/?utm_medium=microsoft&utm_source=docs.microsoft.com&utm_campaign=inline+link&utm_content=download+vs2019+desktopguide+winforms).

01. Die Implementierung von .NET Framework 4, die von Visual Studio 2019 und Visual Studio 2017 unterstützt wird.

    .NET Framework 4 ist eine reine Windows-Version von .NET, die nicht als Komponente des Betriebssystems Windows betrachtet wird. Diese Version von Windows Forms ist in .NET Framework enthalten.

Dieser Desktopleitfaden bezieht sich auf Windows Forms unter .NET 5. Weitere Informationen zur .NET Framework-Version von Windows Forms finden Sie unter [Windows Forms für .NET Framework](../../../framework/winforms/index.yml?view=netframeworkdesktop-4.8&preserve-view=true).

## <a name="introduction"></a>Einführung

Windows Forms ist ein Benutzeroberflächenframework zum Erstellen von Windows-Anwendungen. Es bietet eine der produktivsten Möglichkeiten zum Erstellen von Desktopanwendungen mithilfe des in Visual Studio bereitgestellten visuellen Designers. Funktionen wie die Drag & Drop-Platzierung von visuellen Steuerelementen erleichtern das Erstellen von Desktopanwendungen.

Mit Windows Forms können Sie grafisch ansprechende Anwendungen erstellen, die sich ohne großen Aufwand bereitstellen, aktualisieren und verwenden lassen – sowohl offline als auch online. Windows Forms-Anwendungen können auf die lokale Hardware und das lokale Dateisystem des Computers zugreifen, auf dem sie ausgeführt werden.

Informationen zum Erstellen einer Windows Forms-Anwendung finden Sie unter [Tutorial: Erstellen einer neuen WinForms-Anwendung (Windows Forms .NET)](../get-started/create-app-visual-studio.md).

## <a name="why-migrate-from-net-framework"></a>Gründe für die Migration von .NET Framework

Windows Forms für .NET 5.0 enthält neue Features und Verbesserungen gegenüber .NET Framework. Weitere Informationen finden Sie unter [Neues in Windows Forms für .NET 5](../whats-new/index.md). Informationen zum Migrieren einer Anwendung finden Sie unter [Migrieren einer Windows Forms-Desktopanwendung zu .NET 5](../migration/index.md).

## <a name="build-rich-interactive-user-interfaces"></a>Erstellen von interaktiven Benutzeroberflächen mit anspruchsvollen Grafiken

Windows Forms ist die Technologie zur Erstellung von Benutzeroberflächen für .NET. Dabei handelt es sich um verwaltete Bibliotheken, die allgemeine Anwendungsaufgaben wie Lese- und Schreibzugriffe auf das Dateisystem erleichtern. Mit einer Entwicklungsumgebung wie Visual Studio können Sie intelligente Windows Forms-Clientanwendungen erstellen, die Informationen anzeigen, Benutzer zur Eingabe von Daten auffordern oder über ein Netzwerk mit Remotecomputern kommunizieren.

In Windows Forms stellt ein *Formular* eine visuelle Oberfläche dar, auf der Informationen für den Benutzer angezeigt werden. In der Regel erstellen Sie Windows Forms-Anwendungen, indem Sie Steuerelemente in Formulare einfügen und Antworten auf Benutzeraktionen, wie Maus- und Tastatureingaben, entwickeln. Ein *Steuerelement* ist ein diskretes Benutzeroberflächenelement, das Daten anzeigt oder Dateneingaben akzeptiert.

Wenn ein Benutzer Aktionen im Formular oder in enthaltenen Steuerelementen ausführt, wird ein Ereignis generiert. Die Anwendung reagiert auf diese Ereignisse und verarbeitet sie zum Zeitpunkt ihres Auftretens.<!-- TODO  For more information, see [Creating Event Handlers in Windows Forms](creating-event-handlers-in-windows-forms.md).-->

Windows Forms enthält eine Vielzahl von Steuerelementen, die Sie Formularen hinzufügen können: Steuerelemente zur Anzeige von Textfeldern, Schaltflächen, Dropdownfeldern, Optionsfeldern und sogar Webseiten.<!-- TODO For a list of all the controls you can use on a form, see [Controls to Use on Windows Forms](./controls/controls-to-use-on-windows-forms.md).--> Windows Forms unterstützt über die <xref:System.Windows.Forms.UserControl>-Klasse auch das Erstellen benutzerdefinierter Steuerelemente, wenn ein vorhandenes Steuerelement für Ihre Anforderungen nicht geeignet ist.

Windows Forms verfügt über komplexe Steuerelemente für die Benutzeroberfläche, mit denen Features aus High-End-Anwendungen wie Microsoft Office emuliert werden können. Mit dem <xref:System.Windows.Forms.ToolStrip>-Steuerelement und dem <xref:System.Windows.Forms.MenuStrip>-Steuerelement können Sie Symbolleisten und Menüs erstellen, die Texte und Bilder, Untermenüs oder weitere Steuerelemente enthalten, z. B. Textfelder und Kombinationsfelder.

Mit dem **Windows Forms-Designer** in Visual Studio können Sie Windows Forms-Anwendungen direkt im Drag & Drop-Verfahren erstellen. Wählen Sie Steuerelemente einfach mit dem Mauszeiger aus, und fügen Sie sie an der gewünschten Stelle im Formular ein. Der Designer stellt Tools wie Rasterlinien und Ausrichtungslinien bereit, um das Anordnen von Steuerelementen zu erleichtern. Mit den Steuerelementen <xref:System.Windows.Forms.FlowLayoutPanel>, <xref:System.Windows.Forms.TableLayoutPanel> und <xref:System.Windows.Forms.SplitContainer> können Sie mit geringem Zeitaufwand komplexe Formularlayouts erstellen.

Schließlich enthält der <xref:System.Drawing>-Namespace zum Erstellen eigener Benutzeroberflächenelemente eine Vielzahl von Klassen, um Linien, Kreise und andere Formen direkt auf einem Formular zu zeichnen.

### <a name="create-forms-and-controls"></a>Erstellen von Formularen und Steuerelementen

Ausführliche Informationen zur Verwendung dieser Features finden Sie in den folgenden Hilfethemen.

- [Hinzufügen eines Formulars zu einem Projekt](../forms/how-to-add.md)
- [Hinzufügen von Steuerelementen zu einem Formular](../controls/how-to-add-to-a-form.md)

<!-- TODO
| Using the <xref:System.Windows.Forms.ToolStrip> Control | [How to: Create a Basic ToolStrip with Standard Items Using the Designer](./controls/create-a-basic-wf-toolstrip-with-standard-items-using-the-designer.md) |
| Creating graphics with <xref:System.Drawing> | [Getting Started with Graphics Programming](./advanced/getting-started-with-graphics-programming.md)  |
| Creating custom controls                     | [How to: Inherit from the UserControl Class](./controls/how-to-inherit-from-the-usercontrol-class.md) |
-->

## <a name="display-and-manipulate-data"></a>Anzeigen und Ändern von Daten

Viele Anwendungen müssen Daten aus einer Datenbank, einer XML- oder JSON-Datei, einem Webdienst oder einer anderen Datenquelle anzeigen. Mit dem <xref:System.Windows.Forms.DataGridView>-Steuerelement bietet Windows Forms ein flexibles Steuerelement zum Anzeigen von Tabellendaten im herkömmlichen Zeilen- und Spaltenformat, bei dem jedes Datenelement in einer eigenen Zelle enthalten ist. Mit <xref:System.Windows.Forms.DataGridView> können Sie die Darstellung einzelner Zellen anpassen, die Position beliebiger Zeilen oder Spalten fixieren und komplexe Steuerelemente in einer Zelle anzeigen, um nur einige Features zu nennen.

Mit Windows Forms kann problemlos eine Netzwerkverbindung mit Datenquellen hergestellt werden. Die <xref:System.Windows.Forms.BindingSource>-Komponente stellt eine Verbindung mit einer Datenquelle dar und macht Methoden zum Binden von Daten an Steuerelemente, Navigieren zum vorherigen oder nächsten Datensatz, Bearbeiten von Datensätzen und Speichern von Änderungen in der ursprünglichen Quelle verfügbar. Das <xref:System.Windows.Forms.BindingNavigator>-Steuerelement stellt über die <xref:System.Windows.Forms.BindingSource>-Komponente eine einfache Schnittstelle zum Navigieren zwischen Datensätzen bereit.

Mit dem Datenquellenfenster in Visual Studio können datengebundene Steuerelemente problemlos erstellt werden. In diesem Fenster werden die Datenquellen in Ihrem Projekt angezeigt, z. B. Datenbanken, Webdienste oder Objekte. Zum Erstellen datengebundener Steuerelemente können Sie Elemente aus diesem Fenster auf Formulare im Projekt ziehen. Darüber hinaus können Sie auch bestehende Steuerelemente an Daten binden, indem Sie Objekte aus dem Datenquellenfenster auf bestehende Steuerelemente ziehen.

Ein weiterer Datenbindungstyp, der in Windows Forms verwaltet werden kann, lautet *Einstellungen*. Die meisten Anwendungen müssen bestimmte Informationen über ihren Laufzeitzustand, z. B. die zuletzt bekannte Größe des Formulars, sowie Benutzereinstellungen wie Standardspeicherorte von Dateien erhalten. Die Funktion "Anwendungseinstellungen" trägt diesen Anforderungen Rechnung und stellt eine einfache Möglichkeit dar, beide Arten von Einstellungen auf dem Clientcomputer zu speichern. Nachdem Sie die Einstellungen mit Visual Studio oder einem Code-Editor definiert haben, werden diese im XML-Format gespeichert und zur Laufzeit automatisch in den Arbeitsspeicher eingelesen.

<!-- TODO
### Display and manipulate data

For step-by-step information about how to use these features, see the following Help topics.

| Description                                                   | Help topic                                                                                                                                                        |
|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Using the <xref:System.Windows.Forms.BindingSource> component | [How to: Bind Windows Forms Controls with the BindingSource Component Using the Designer](./controls/bind-wf-controls-with-the-bindingsource.md)                  |
| Working with ADO.NET data sources                             | [How to: Sort and Filter ADO.NET Data with the Windows Forms BindingSource Component](./controls/sort-and-filter-ado-net-data-with-wf-bindingsource-component.md) |
| Using the Data Sources window                                 | [Bind Windows Forms controls to data in Visual Studio](/visualstudio/data-tools/bind-windows-forms-controls-to-data-in-visual-studio)                             |
| Using app settings                                            | [How to: Create Application Settings](./advanced/how-to-create-application-settings.md)                                                                           |

-->

## <a name="deploy-apps-to-client-computers"></a>Bereitstellen von Anwendungen auf Clientcomputern

Nach dem Erstellen müssen Sie die Anwendung an Ihre Benutzer senden, damit diese die Anwendung auf dem eigenen Clientcomputer installieren und ausführen können. Mithilfe der ClickOnce-Technologie können Sie Anwendungen in Visual Studio mit wenigen Klicks bereitstellen und Benutzern eine URL zur Verfügung stellen, die auf die Anwendung im Internet verweist. ClickOnce verwaltet alle Elemente und Abhängigkeiten in der Anwendung und stellt sicher, dass die Anwendung auf dem Clientcomputer ordnungsgemäß installiert ist.

ClickOnce-Anwendungen können so konfiguriert werden, dass sie nur ausgeführt werden, wenn der Benutzer mit dem Netzwerk verbunden ist, oder dass sie sowohl online als auch offline ausgeführt werden können. Wenn Sie angeben, dass eine Anwendung den Offlinebetrieb unterstützen soll, fügt ClickOnce im Menü **Start** des Benutzers einen Link zur Anwendung hinzu. Der Benutzer kann die Anwendung dann auch ohne die URL öffnen.

Wenn Sie die Anwendung aktualisieren, veröffentlichen Sie auf dem Webserver ein neues Bereitstellungsmanifest und eine neue Kopie der Anwendung. ClickOnce erkennt, wenn ein Update verfügbar ist, und aktualisiert die Installation des Benutzers. Zum Aktualisieren von alten Anwendungen ist keine benutzerdefinierte Programmierung erforderlich.

<!-- TODO

### Deploy ClickOnce apps

For a full introduction to ClickOnce, see [ClickOnce Security and Deployment](/visualstudio/deployment/clickonce-security-and-deployment). For step-by-step information about how to use these features, see the following Help topics,

|Description|Help topic|
|-----------------|----------------|
|Deploying an app by using ClickOnce|[How to: Publish a ClickOnce Application using the Publish Wizard](/visualstudio/deployment/how-to-publish-a-clickonce-application-using-the-publish-wizard)<br /><br /> [Walkthrough: Manually Deploying a ClickOnce Application](/visualstudio/deployment/walkthrough-manually-deploying-a-clickonce-application)|
|Updating a ClickOnce deployment|[How to: Manage Updates for a ClickOnce Application](/visualstudio/deployment/how-to-manage-updates-for-a-clickonce-application)|
|Managing security with ClickOnce|[How to: Enable ClickOnce Security Settings](/visualstudio/deployment/how-to-enable-clickonce-security-settings)|
-->

<!-- TODO
## Other controls and features

There are many other features in Windows Forms that make implementing common tasks fast and easy, such as support for creating dialog boxes, printing, adding help and documentation, and localizing your app to multiple languages.

### Implement other controls and features

For step-by-step information about how to use these features, see the following Help topics.

| Description | Help topic |
|-------------|------------|
|Printing the contents of a form | [How to: Print Graphics in Windows Forms](./advanced/how-to-print-graphics-in-windows-forms.md)<br /><br /> [How to: Print a Multi-Page Text File in Windows Forms](./advanced/how-to-print-a-multi-page-text-file-in-windows-forms.md) |
|Learn more about Windows Forms security | [Security in Windows Forms Overview](security-in-windows-forms-overview.md) |
-->

## <a name="see-also"></a>Siehe auch

- [Tutorial: Erstellen einer neuen WinForms-Anwendung (Windows Forms .NET)](../get-started/create-app-visual-studio.md)
- [Hinzufügen eines Formulars zu einem Projekt (Windows Forms .NET)](../forms/how-to-add.md)
- [Hinzufügen eines Steuerelements (Windows Forms .NET)](../controls/how-to-add-to-a-form.md)
