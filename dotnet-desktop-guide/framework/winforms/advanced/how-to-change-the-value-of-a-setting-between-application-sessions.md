---
title: 'Vorgehensweise: Ändern des Werts einer Einstellung zwischen Anwendungssitzungen'
ms.date: 03/30/2017
helpviewer_keywords:
- application settings [Windows Forms], changing
- application settings [Windows Forms], between application sessions
ms.assetid: 1a85911f-97b2-476c-930b-83379edd890c
ms.openlocfilehash: 95e613cb280813cd75d887d3cf147d7c897bc2e6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975015"
---
# <a name="how-to-change-the-value-of-a-setting-between-application-sessions"></a>Vorgehensweise: Ändern des Werts einer Einstellung zwischen Anwendungssitzungen
Manchmal können Sie den Wert einer Einstellung zwischen Anwendungs Sitzungen ändern, nachdem die Anwendung kompiliert und bereitgestellt wurde. Beispielsweise können Sie eine Verbindungs Zeichenfolge so ändern, dass Sie auf den richtigen Speicherort der Datenbank verweist. Da Entwurfszeit Tools nach der Kompilierung und Bereitstellung der Anwendung nicht verfügbar sind, müssen Sie den Einstellungs Wert in der Datei manuell ändern.  
  
### <a name="to-change-the-value-of-a-setting-between-application-sessions"></a>So ändern Sie den Wert einer Einstellung zwischen Anwendungs Sitzungen  
  
1. Öffnen Sie mit Microsoft Notepad oder einem anderen Text-oder XML-Editor die config-Datei, die Ihrer Anwendung zugeordnet ist.  
  
2. Suchen Sie den Eintrag für die Einstellung, die Sie ändern möchten. Es sollte in etwa wie im folgenden Beispiel aussehen.  
  
    ```xml  
    <setting name="Setting1" serializeAs="String" >  
       <value>My Setting Value</value>  
    </setting>  
    ```  
  
3. Geben Sie einen neuen Wert für Ihre Einstellung ein, und speichern Sie die Datei.  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden von Anwendungseinstellungen und Benutzereinstellungen](using-application-settings-and-user-settings.md)
- [Übersicht über Anwendungseinstellungen](application-settings-overview.md)
