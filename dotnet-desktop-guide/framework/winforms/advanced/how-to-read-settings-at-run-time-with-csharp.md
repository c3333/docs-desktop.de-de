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
# <a name="how-to-read-settings-at-run-time-with-c"></a><span data-ttu-id="89ddb-103">Gewusst wie: Lesen von Einstellungen zur Laufzeit mit C\#</span><span class="sxs-lookup"><span data-stu-id="89ddb-103">How To: Read Settings at Run Time With C\#</span></span>

<span data-ttu-id="89ddb-104">Über das Properties-Objekt können Sie zur Laufzeit anwendungsspezifische und benutzerspezifische Einstellungen auslesen.</span><span class="sxs-lookup"><span data-stu-id="89ddb-104">You can read both Application-scoped and User-scoped settings at run time via the Properties object.</span></span> <span data-ttu-id="89ddb-105">Das Properties-Objekt macht alle Standardeinstellungen für das Projekt über den Properties. Settings. Default-Member im Standard Namespace des Projekts verfügbar, in dem Sie definiert sind.</span><span class="sxs-lookup"><span data-stu-id="89ddb-105">The Properties object exposes all of the default settings for the project via the Properties.Settings.Default member in the default namespace of the project they are defined in.</span></span>  
  
## <a name="to-read-settings-at-run-time-with-c"></a><span data-ttu-id="89ddb-106">So lesen Sie Einstellungen zur Laufzeit mit C\#</span><span class="sxs-lookup"><span data-stu-id="89ddb-106">To Read Settings at Run Time with C\#</span></span>
  
<span data-ttu-id="89ddb-107">Greifen Sie über den Properties.Settings.Default-Member auf die geeignete Einstellung zu.</span><span class="sxs-lookup"><span data-stu-id="89ddb-107">Access the appropriate setting via the Properties.Settings.Default member.</span></span> <span data-ttu-id="89ddb-108">Im folgenden Beispiel wird gezeigt, wie Sie einer BackColor-Eigenschaft eine Einstellung mit Namen `myColor` zuweisen.</span><span class="sxs-lookup"><span data-stu-id="89ddb-108">The following example shows how to assign a setting named `myColor` to a BackColor property.</span></span> <span data-ttu-id="89ddb-109">Dies setzt voraus, dass Sie zuvor eine Einstellungsdatei erstellt haben, die eine Einstellung mit Namen `myColor` vom Typ `System.Drawing.Color` enthält.</span><span class="sxs-lookup"><span data-stu-id="89ddb-109">It requires you to have previously created a Settings file containing a setting named `myColor` of type `System.Drawing.Color`.</span></span> <span data-ttu-id="89ddb-110">Weitere Informationen zum Erstellen einer Einstellungsdatei finden [Sie unter Gewusst wie: Erstellen einer neuen Einstellung zur Entwurfszeit](how-to-create-a-new-setting-at-design-time.md).</span><span class="sxs-lookup"><span data-stu-id="89ddb-110">For information about creating a Settings file, see [How To: Create a New Setting at Design Time](how-to-create-a-new-setting-at-design-time.md).</span></span>  
  
```csharp
this.BackColor = Properties.Settings.Default.myColor;  
```  
  
## <a name="see-also"></a><span data-ttu-id="89ddb-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89ddb-111">See also</span></span>

- [<span data-ttu-id="89ddb-112">Verwenden von Anwendungseinstellungen und Benutzereinstellungen</span><span class="sxs-lookup"><span data-stu-id="89ddb-112">Using Application Settings and User Settings</span></span>](using-application-settings-and-user-settings.md)
- [<span data-ttu-id="89ddb-113">Vorgehensweise: Schreiben von Benutzereinstellungen zur Laufzeit mit C#</span><span class="sxs-lookup"><span data-stu-id="89ddb-113">How To: Write User Settings at Run Time with C#</span></span>](how-to-write-user-settings-at-run-time-with-csharp.md)
- [<span data-ttu-id="89ddb-114">Übersicht über Anwendungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="89ddb-114">Application Settings Overview</span></span>](application-settings-overview.md)
