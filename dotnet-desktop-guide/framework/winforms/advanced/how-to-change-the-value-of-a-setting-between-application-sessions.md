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
# <a name="how-to-change-the-value-of-a-setting-between-application-sessions"></a><span data-ttu-id="67319-102">Vorgehensweise: Ändern des Werts einer Einstellung zwischen Anwendungssitzungen</span><span class="sxs-lookup"><span data-stu-id="67319-102">How To: Change the Value of a Setting Between Application Sessions</span></span>
<span data-ttu-id="67319-103">Manchmal können Sie den Wert einer Einstellung zwischen Anwendungs Sitzungen ändern, nachdem die Anwendung kompiliert und bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="67319-103">At times, you might want to change the value of a setting between application sessions after the application has been compiled and deployed.</span></span> <span data-ttu-id="67319-104">Beispielsweise können Sie eine Verbindungs Zeichenfolge so ändern, dass Sie auf den richtigen Speicherort der Datenbank verweist.</span><span class="sxs-lookup"><span data-stu-id="67319-104">For example, you might want to change a connection string to point to the correct database location.</span></span> <span data-ttu-id="67319-105">Da Entwurfszeit Tools nach der Kompilierung und Bereitstellung der Anwendung nicht verfügbar sind, müssen Sie den Einstellungs Wert in der Datei manuell ändern.</span><span class="sxs-lookup"><span data-stu-id="67319-105">Since design-time tools are not available after the application has been compiled and deployed, you must change the setting value manually in the file.</span></span>  
  
### <a name="to-change-the-value-of-a-setting-between-application-sessions"></a><span data-ttu-id="67319-106">So ändern Sie den Wert einer Einstellung zwischen Anwendungs Sitzungen</span><span class="sxs-lookup"><span data-stu-id="67319-106">To Change the Value of a Setting Between Application Sessions</span></span>  
  
1. <span data-ttu-id="67319-107">Öffnen Sie mit Microsoft Notepad oder einem anderen Text-oder XML-Editor die config-Datei, die Ihrer Anwendung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="67319-107">Using Microsoft Notepad or some other text or XML editor, open the .config file associated with your application.</span></span>  
  
2. <span data-ttu-id="67319-108">Suchen Sie den Eintrag für die Einstellung, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="67319-108">Locate the entry for the setting you want to change.</span></span> <span data-ttu-id="67319-109">Es sollte in etwa wie im folgenden Beispiel aussehen.</span><span class="sxs-lookup"><span data-stu-id="67319-109">It should look similar to the example presented below.</span></span>  
  
    ```xml  
    <setting name="Setting1" serializeAs="String" >  
       <value>My Setting Value</value>  
    </setting>  
    ```  
  
3. <span data-ttu-id="67319-110">Geben Sie einen neuen Wert für Ihre Einstellung ein, und speichern Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="67319-110">Type a new value for your setting and save the file.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="67319-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67319-111">See also</span></span>

- [<span data-ttu-id="67319-112">Verwenden von Anwendungseinstellungen und Benutzereinstellungen</span><span class="sxs-lookup"><span data-stu-id="67319-112">Using Application Settings and User Settings</span></span>](using-application-settings-and-user-settings.md)
- [<span data-ttu-id="67319-113">Übersicht über Anwendungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="67319-113">Application Settings Overview</span></span>](application-settings-overview.md)
