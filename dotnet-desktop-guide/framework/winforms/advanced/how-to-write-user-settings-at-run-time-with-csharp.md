---
title: 'Vorgehensweise: Schreiben von Benutzereinstellungen zur Laufzeit mit C#'
description: Erfahren Sie, wie Sie Einstellungen zur Laufzeit mit c# schreiben, indem Sie die Änderungen an den Einstellungen zwischen Anwendungs Sitzungen beibehalten, indem Sie die Save-Methode aufrufen.
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], run time
- application settings [Windows Forms], writing user settings
- application settings [Windows Forms], C#
ms.assetid: 9d061c7d-b33b-470f-a36d-edccb1d6f9a3
ms.openlocfilehash: 6154ff1b92d6c2d4c788299e59eb8f73e6b69c4b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975852"
---
# <a name="how-to-write-user-settings-at-run-time-with-c"></a>Gewusst wie: Schreiben von Benutzereinstellungen zur Laufzeit mit C\#

Einstellungen im Gültigkeitsbereich der Anwendung sind schreibgeschützt und können nur zur Entwurfszeit oder durch Ändern der CONFIG-Datei zwischen Anwendungssitzungen geändert werden. Einstellungen im Gültigkeitsbereich des Benutzers können jedoch zur Laufzeit geschrieben werden, so als würden Sie einen beliebigen Eigenschaftswert ändern. Der neue Wert wird für die Dauer der Anwendungssitzung beibehalten. Sie können die Änderungen an den Einstellungen zwischen Anwendungssitzungen beibehalten, indem Sie die Save-Methode aufrufen.  
  
## <a name="how-to-write-and-persist-user-settings-at-run-time-with-c"></a>Gewusst wie: schreiben und beibehalten von Benutzereinstellungen zur Laufzeit mit C\#
  
1. Greifen Sie auf die Einstellung zu, und weisen Sie ihr einen neuen Wert zu, wie im folgenden Beispiel gezeigt:  
  
   ```csharp
   Properties.Settings.Default.myColor = Color.AliceBlue;  
   ```  
  
2. Wenn Sie die Änderungen an den Einstellungen zwischen Anwendungssitzungen beibehalten möchten, rufen Sie die Save-Methode auf, wie im folgenden Beispiel gezeigt:  
  
    ```csharp
    Properties.Settings.Default.Save();  
    ```  
  
Benutzereinstellungen werden in einer Datei in einem Unterordner des lokalen ausgeblendeten Ordners für Anwendungsdaten des Benutzers gespeichert.  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden von Anwendungseinstellungen und Benutzereinstellungen](using-application-settings-and-user-settings.md)
- [Vorgehensweise: Lesen von Einstellungen zur Laufzeit mit C#](how-to-read-settings-at-run-time-with-csharp.md)
- [Übersicht über Anwendungseinstellungen](application-settings-overview.md)
