---
title: 'Vorgehensweise: Lesen von Einstellungen zur Laufzeit mit C#'
description: Erfahren Sie, wie Sie anwendungsspezifische und benutzerspezifische Einstellungen zur Laufzeit mit c# über das Properties-Objekt lesen.
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], reading
- application settings [Windows Forms], run time
- application settings [Windows Forms], C#
ms.assetid: dbe8bf09-5e1c-49da-9192-154033d7240b
ms.openlocfilehash: d784544e018bb693c501e35ea36fcae1946ef5eb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976133"
---
# <a name="how-to-read-settings-at-run-time-with-c"></a>Gewusst wie: Lesen von Einstellungen zur Laufzeit mit C\#

Über das Properties-Objekt können Sie zur Laufzeit anwendungsspezifische und benutzerspezifische Einstellungen auslesen. Das Properties-Objekt macht alle Standardeinstellungen für das Projekt über den Properties. Settings. Default-Member im Standard Namespace des Projekts verfügbar, in dem Sie definiert sind.  
  
## <a name="to-read-settings-at-run-time-with-c"></a>So lesen Sie Einstellungen zur Laufzeit mit C\#
  
Greifen Sie über den Properties.Settings.Default-Member auf die geeignete Einstellung zu. Im folgenden Beispiel wird gezeigt, wie Sie einer BackColor-Eigenschaft eine Einstellung mit Namen `myColor` zuweisen. Dies setzt voraus, dass Sie zuvor eine Einstellungsdatei erstellt haben, die eine Einstellung mit Namen `myColor` vom Typ `System.Drawing.Color` enthält. Weitere Informationen zum Erstellen einer Einstellungsdatei finden [Sie unter Gewusst wie: Erstellen einer neuen Einstellung zur Entwurfszeit](how-to-create-a-new-setting-at-design-time.md).  
  
```csharp
this.BackColor = Properties.Settings.Default.myColor;  
```  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden von Anwendungseinstellungen und Benutzereinstellungen](using-application-settings-and-user-settings.md)
- [Vorgehensweise: Schreiben von Benutzereinstellungen zur Laufzeit mit C#](how-to-write-user-settings-at-run-time-with-csharp.md)
- [Übersicht über Anwendungseinstellungen](application-settings-overview.md)
