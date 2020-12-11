---
title: Anwendungseinstellungen für benutzerdefinierte Steuerelemente
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], application settings
- application settings [Windows Forms], custom controls
ms.assetid: f44afb74-76cc-44f2-890a-44b7cdc211a1
ms.openlocfilehash: a4e477ce1c171b514482623595b2c5565564a2cb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975067"
---
# <a name="application-settings-for-custom-controls"></a>Anwendungseinstellungen für benutzerdefinierte Steuerelemente
Sie müssen bestimmte Aufgaben durchführen, um Ihren benutzerdefinierten Steuerelementen zu ermöglichen, Anwendungseinstellungen beizubehalten, wenn die Steuerelemente in Anwendungen von Drittanbietern gehostet werden.

 Der größte Teil der Dokumentation über das Feature "Anwendungseinstellungen" wird unter der Annahme geschrieben, dass Sie eine eigenständige Anwendung erstellen. Wenn Sie jedoch ein Steuerelement erstellen, das andere Entwickler in Ihren Anwendungen hosten, müssen Sie einige zusätzliche Schritte ausführen, damit das Steuerelement seine Einstellungen ordnungsgemäß persistent speichert.

## <a name="application-settings-and-custom-controls"></a>Anwendungseinstellungen und benutzerdefinierte Steuerelemente
 Damit das Steuerelement seine Einstellungen ordnungsgemäß persistent speichert, muss es den Prozess einschließen, indem er seine eigene Wrapper Klasse für dedizierte Anwendungseinstellungen erstellt, die von abgeleitet ist <xref:System.Configuration.ApplicationSettingsBase> . Außerdem muss die Hauptsteuer Element Klasse implementieren <xref:System.Configuration.IPersistComponentSettings> . Die-Schnittstelle enthält mehrere Eigenschaften sowie zwei Methoden, <xref:System.Configuration.IPersistComponentSettings.LoadComponentSettings%2A> und <xref:System.Configuration.IPersistComponentSettings.SaveComponentSettings%2A> . Wenn Sie das Steuerelement einem Formular mithilfe der **Windows Forms-Designer** in Visual Studio hinzufügen, wird Windows Forms <xref:System.Configuration.IPersistComponentSettings.LoadComponentSettings%2A> automatisch aufgerufen, wenn das Steuerelement initialisiert wird. Sie müssen <xref:System.Configuration.IPersistComponentSettings.SaveComponentSettings%2A> sich selbst in der- `Dispose` Methode des Steuer Elements anrufen.

 Außerdem sollten Sie Folgendes implementieren, damit Anwendungseinstellungen für benutzerdefinierte Steuerelemente in Entwurfszeit Umgebungen wie Visual Studio ordnungsgemäß funktionieren:

1. Eine benutzerdefinierte Anwendungs Einstellungs Klasse mit einem Konstruktor, der eine <xref:System.ComponentModel.IComponent> als einen einzelnen Parameter annimmt. Verwenden Sie diese Klasse, um alle Anwendungseinstellungen zu speichern und zu laden. Wenn Sie eine neue Instanz dieser Klasse erstellen, übergeben Sie das benutzerdefinierte Steuerelement mithilfe des Konstruktors.

2. Erstellen Sie diese benutzerdefinierte Einstellungs Klasse, nachdem das Steuerelement erstellt und in einem Formular abgelegt wurde, z. b <xref:System.Windows.Forms.Form.Load> . im-Ereignishandler des Formulars.

 Anweisungen zum Erstellen einer benutzerdefinierten Einstellungs Klasse finden Sie unter Gewusst [wie: Erstellen von Anwendungseinstellungen](how-to-create-application-settings.md).

## <a name="settings-keys-and-shared-settings"></a>Einstellungs Schlüssel und freigegebene Einstellungen
 Einige Steuerelemente können mehrmals innerhalb desselben Formulars verwendet werden. In den meisten Fällen möchten Sie, dass diese Steuerelemente ihre eigenen individuellen Einstellungen beibehalten. Mit der- <xref:System.Configuration.IPersistComponentSettings.SettingsKey%2A> Eigenschaft für <xref:System.Configuration.IPersistComponentSettings> können Sie eine eindeutige Zeichenfolge bereitstellen, mit der mehrere Versionen eines Steuer Elements in einem Formular eindeutig unterschieden werden können.

 Die einfachste Methode zur Implementierung <xref:System.Configuration.IPersistComponentSettings.SettingsKey%2A> von ist die Verwendung der- <xref:System.Windows.Forms.Control.Name%2A> Eigenschaft des-Steuer Elements für den <xref:System.Configuration.IPersistComponentSettings.SettingsKey%2A> . Wenn Sie die Einstellungen des Steuer Elements laden oder speichern, übergeben Sie den Wert von für <xref:System.Configuration.IPersistComponentSettings.SettingsKey%2A> an die- <xref:System.Configuration.ApplicationSettingsBase.SettingsKey%2A> Eigenschaft der- <xref:System.Configuration.ApplicationSettingsBase> Klasse. Anwendungseinstellungen verwenden diesen eindeutigen Schlüssel, wenn die Benutzereinstellungen in XML beibehalten werden. Im folgenden Codebeispiel wird gezeigt, wie ein `<userSettings>` Abschnitt nach einer Instanz eines benutzerdefinierten Steuer Elements namens suchen kann `CustomControl1` , das eine Einstellung für seine- `Text` Eigenschaft speichert.

```xml
<userSettings>
    <CustomControl1>
        <setting name="Text" serializedAs="string">
            <value>Hello, World</value>
        </setting>
    </CustomControl1>
</userSettings>
```

 Alle Instanzen eines Steuer Elements, die keinen Wert für angeben, <xref:System.Configuration.ApplicationSettingsBase.SettingsKey%2A> haben dieselben Einstellungen.

## <a name="see-also"></a>Siehe auch

- <xref:System.Configuration.ApplicationSettingsBase>
- <xref:System.Configuration.IPersistComponentSettings>
- [Architektur der Anwendungseinstellungen](application-settings-architecture.md)
