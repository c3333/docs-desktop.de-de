---
title: Neuerungen in Windows Forms
description: Hier erfahren Sie, welche Neuerungen in Windows Forms für .NET enthalten sind. Windows Forms. .NET enthält neue Features und Verbesserungen gegenüber .NET Framework.
ms.date: 11/05/2020
ms.topic: conceptual
ms.openlocfilehash: 5c22fdd2df68cd59b7bc0b93c6aa7223bdf06ec0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96992802"
---
# <a name="whats-new-windows-forms-net"></a>Neuerungen (Windows Forms .NET)

Windows Forms für .NET 5.0 enthält nun die folgenden Features und Verbesserungen gegenüber .NET Framework.

Es gibt einige Breaking Changes, die Sie bei der Migration von .NET Framework zu .NET 5.0 beachten sollten. Weitere Informationen finden Sie unter [Breaking Changes in Windows Forms](/dotnet/core/compatibility/winforms).

## <a name="enhanced-features"></a>Verbesserte Features

- Muster der Microsoft-Benutzeroberflächenautomatisierung funktionieren mit Tools für Barrierefreiheit wie Narrator und Jaws besser.
- Verbesserte Leistung.
- In der VB.NET-Projektvorlage werden für hohe DPI-Auflösungen wie bei 4K-Bildschirmen standardmäßig die DPI SystemAware-Einstellungen verwendet.
- Die Standardschriftart entspricht den aktuellen Windows-Entwurfsempfehlungen.

  > [!CAUTION]
  > Das kann sich auf das Layout von Anwendungen auswirken, die von .NET Framework migriert werden.

## <a name="new-controls"></a>Neue Steuerelemente

Die folgenden Steuerelemente sind seit der Portierung von Windows Forms zu .NET Framework verfügbar:

- <xref:System.Windows.Forms.TaskDialog?displayProperty=fullName>
  
  Bei einem Aufgabendialogfeld handelt es sich um ein Dialogfeld zum Anzeigen von Informationen und zum Entgegennehmen einfacher Eingaben des Benutzers. Es wird wie ein Meldungsfeld vom Betriebssystem nach Parametern formatiert, die Sie festlegen. Im Vergleich zu einem Meldungsfeld enthält ein Aufgabendialogfeld mehr Features. Weitere Informationen finden Sie unter [Beispiel für ein Aufgabendialogfeld](https://github.com/dotnet/samples/tree/master/windowsforms/TaskDialogDemo).

- <xref:Microsoft.Web.WebView2.WinForms.WebView2?displayProperty=fullName>

  Ein neues Webbrowsersteuerelement mit moderner Webunterstützung. Basierend auf Edge (Chromium). Weitere Informationen finden Sie unter [Erste Schritte mit WebView2 in Windows Forms](/microsoft-edge/webview2/gettingstarted/winforms).

## <a name="enhanced-controls"></a>Erweiterte Steuerelemente

- <xref:System.Windows.Forms.ListView?displayProperty=fullName>

  - Unterstützt reduzierbare Gruppen
  - Fußzeilen
  - Untertitel-, Aufgaben- und Titelbilder einer Gruppe

- <xref:System.Windows.Forms.FolderBrowserDialog?displayProperty=fullName>

  Dieses Dialogfeld wurde aktualisiert, sodass nun anstelle der alten Windows 7-Benutzeroberfläche die moderne Windows-Benutzeroberfläche verwendet wird.

- <xref:System.Windows.Forms.FileDialog?displayProperty=fullName>

  - Ab der neuen Version wird <xref:System.Windows.Forms.FileDialog.ClientGuid> unterstützt.

    Mit `ClientGuid` kann eine aufrufende Anwendung dem persistenten Zustand eines Dialogfelds eine GUID zuordnen. Der Zustand eines Dialogfelds kann Faktoren wie den zuletzt besuchten Ordner und die Position und Größe des Dialogfelds beinhalten. Dieser Zustand wird in der Regel basierend auf dem Namen der ausführbaren Datei beibehalten. Mit `ClientGuid` kann eine Anwendung innerhalb einer Anwendung unterschiedliche Zustände des Dialogfelds beibehalten.

- <xref:System.Windows.Forms.TextRenderer?displayProperty=fullName>

  Ab der neuen Version wird zur Verbesserung der Leistung beim Rendern von Text <xref:System.ReadOnlySpan%601> unterstützt.

## <a name="see-also"></a>Siehe auch

- [Breaking Changes bei Windows Forms](/dotnet/core/compatibility/winforms)
- [Tutorial: Erstellen einer neuen WinForms-Anwendung (Windows Forms .NET)](../get-started/create-app-visual-studio.md)
- [Migrieren einer Windows Forms-Desktopanwendung zu .NET 5](../migration/index.md)
