---
title: Verwenden von Anwendungseinstellungen und Benutzereinstellungen
ms.date: 03/30/2017
description: Erfahren Sie, wie Sie mithilfe von Anwendungseinstellungen und Benutzereinstellungen Werte erstellen und darauf zugreifen, die zwischen Anwendungs Ausführungs Sitzungen beibehalten werden.
helpviewer_keywords:
- user settings [Windows Forms]
- application settings [Windows Forms], how-to topics
ms.assetid: 54682d3b-1cbf-4683-9351-012b8b4286b5
ms.openlocfilehash: a30fd354986265eca002fce57bccf5b3bb2adc15
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976047"
---
# <a name="using-application-settings-and-user-settings"></a><span data-ttu-id="c406d-103">Verwenden von Anwendungseinstellungen und Benutzereinstellungen</span><span class="sxs-lookup"><span data-stu-id="c406d-103">Using Application Settings and User Settings</span></span>
<span data-ttu-id="c406d-104">Beginnend mit dem .NET Framework 2,0 können Sie Werte erstellen und darauf zugreifen, die zwischen Anwendungs Ausführungs Sitzungen beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="c406d-104">Starting with the .NET Framework 2.0, you can create and access values that are persisted between application execution sessions.</span></span> <span data-ttu-id="c406d-105">Diese Werte werden als *Einstellungen* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c406d-105">These values are called *settings*.</span></span> <span data-ttu-id="c406d-106">Einstellungen können Benutzereinstellungen oder wertvolle Informationen darstellen, die von der Anwendung verwendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="c406d-106">Settings can represent user preferences, or valuable information the application needs to use.</span></span> <span data-ttu-id="c406d-107">Beispielsweise können Sie eine Reihe von Einstellungen erstellen, die Benutzereinstellungen für das Farbschema einer Anwendung speichern.</span><span class="sxs-lookup"><span data-stu-id="c406d-107">For example, you might create a series of settings that store user preferences for the color scheme of an application.</span></span> <span data-ttu-id="c406d-108">Oder Sie speichern die Verbindungs Zeichenfolge, die eine Datenbank angibt, die von der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c406d-108">Or you might store the connection string that specifies a database that your application uses.</span></span> <span data-ttu-id="c406d-109">Mit Einstellungen können Sie Informationen, die für die Anwendung außerhalb des Codes wichtig sind, beibehalten und Profile erstellen, die die Einstellungen einzelner Benutzer speichern.</span><span class="sxs-lookup"><span data-stu-id="c406d-109">Settings allow you to both persist information that is critical to the application outside the code, and to create profiles that store the preferences of individual users.</span></span>  
  
 <span data-ttu-id="c406d-110">In den Themen in diesem Abschnitt wird beschrieben, wie Einstellungen zur Entwurfszeit und zur Laufzeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c406d-110">The topics in this section describe how to use settings at design time and run time.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="c406d-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c406d-111">In This Section</span></span>  
 [<span data-ttu-id="c406d-112">Vorgehensweise: Erstellen einer neuen Einstellung zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="c406d-112">How To: Create a New Setting at Design Time</span></span>](how-to-create-a-new-setting-at-design-time.md)  
  
 <span data-ttu-id="c406d-113">Erläutert, wie Visual Studio verwendet wird, um eine neue Einstellung für eine Anwendung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c406d-113">Explains how to use Visual Studio to create a new setting for an application.</span></span>  
  
 [<span data-ttu-id="c406d-114">Vorgehensweise: Ändern des Werts einer vorhandenen Einstellung zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="c406d-114">How To: Change the Value of an Existing Setting at Design Time</span></span>](how-to-change-the-value-of-an-existing-setting-at-design-time.md)  
  
 <span data-ttu-id="c406d-115">Beschreibt, wie Visual Studio verwendet wird, um den Wert einer vorhandenen Einstellung zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c406d-115">Describes how to use Visual Studio to change the value of an existing setting.</span></span>  
  
 [<span data-ttu-id="c406d-116">Vorgehensweise: Ändern des Werts einer Einstellung zwischen Anwendungssitzungen</span><span class="sxs-lookup"><span data-stu-id="c406d-116">How To: Change the Value of a Setting Between Application Sessions</span></span>](how-to-change-the-value-of-a-setting-between-application-sessions.md)  
  
 <span data-ttu-id="c406d-117">Erläutert, wie der Wert einer Einstellung in einer kompilierten Anwendung zwischen Anwendungs Sitzungen geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c406d-117">Details how to change the value of a setting in a compiled application between application sessions.</span></span>  
  
 [<span data-ttu-id="c406d-118">Vorgehensweise: Lesen von Einstellungen zur Laufzeit mit C#</span><span class="sxs-lookup"><span data-stu-id="c406d-118">How To: Read Settings at Run Time With C#</span></span>](how-to-read-settings-at-run-time-with-csharp.md)  
  
 <span data-ttu-id="c406d-119">Beschreibt die Verwendung von Code zum Lesen von Einstellungen mit c#.</span><span class="sxs-lookup"><span data-stu-id="c406d-119">Describes how to use code to read settings with C#.</span></span>  
  
 [<span data-ttu-id="c406d-120">Vorgehensweise: Schreiben von Benutzereinstellungen zur Laufzeit mit C#</span><span class="sxs-lookup"><span data-stu-id="c406d-120">How To: Write User Settings at Run Time with C#</span></span>](how-to-write-user-settings-at-run-time-with-csharp.md)  
  
 <span data-ttu-id="c406d-121">Erläutert die Verwendung von Code zum Schreiben und Speichern der Werte von Benutzereinstellungen mit c#.</span><span class="sxs-lookup"><span data-stu-id="c406d-121">Explains how to use code to write and save the values of user settings with C#.</span></span>  
  
 [<span data-ttu-id="c406d-122">Vorgehensweise: Hinzufügen mehrerer Gruppen von Einstellungen zur Anwendung in C#</span><span class="sxs-lookup"><span data-stu-id="c406d-122">How To: Add Multiple Sets of Settings To Your Application in C#</span></span>](how-to-add-multiple-sets-of-settings-to-your-application-in-csharp.md)  
  
 <span data-ttu-id="c406d-123">Erläutert das Hinzufügen mehrerer Einstellungs Sätze zu einer Anwendung mit c#.</span><span class="sxs-lookup"><span data-stu-id="c406d-123">Details how to add multiple sets of settings to an application with C#.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c406d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c406d-124">See also</span></span>

- [<span data-ttu-id="c406d-125">Anwendungseinstellungen für Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c406d-125">Application Settings for Windows Forms</span></span>](application-settings-for-windows-forms.md)
