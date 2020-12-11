---
title: 'Vorgehensweise: Erstellen von Anwendungseinstellungen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- application settings [Windows Forms], Windows Forms
- application settings [Windows Forms], creating
ms.assetid: 1e7aa347-af75-41e5-89ca-f53cab704f72
ms.openlocfilehash: 1c7bcb5b9166cf8fcb01f11d701ea4ebca713ee7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974832"
---
# <a name="how-to-create-application-settings"></a><span data-ttu-id="12f69-102">Vorgehensweise: Erstellen von Anwendungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="12f69-102">How to: Create Application Settings</span></span>

<span data-ttu-id="12f69-103">Mithilfe von verwaltetem Code können Sie neue Anwendungseinstellungen erstellen und diese an Eigenschaften für Ihr Formular oder die Steuerelemente Ihres Formulars binden, damit diese Einstellungen zur Laufzeit automatisch geladen und gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="12f69-103">Using managed code, you can create new application settings and bind them to properties on your form or your form's controls, so that these settings are loaded and saved automatically at run time.</span></span>  
  
 <span data-ttu-id="12f69-104">Im folgenden Verfahren erstellen Sie manuell eine Wrapperklasse, die von <xref:System.Configuration.ApplicationSettingsBase> abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="12f69-104">In the following procedure, you manually create a wrapper class that derives from <xref:System.Configuration.ApplicationSettingsBase>.</span></span> <span data-ttu-id="12f69-105">Dieser Klasse fügen Sie für jede Anwendungseinstellung, die Sie verfügbar machen möchten, eine Eigenschaft hinzu, auf die öffentlich zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="12f69-105">To this class you add a publicly accessible property for each application setting that you want to expose.</span></span>  
  
 <span data-ttu-id="12f69-106">Sie können dieses Verfahren auch mit minimalem Programmieraufwand in Visual Studio-Designer ausführen.</span><span class="sxs-lookup"><span data-stu-id="12f69-106">You can also perform this procedure using minimal code in the Visual Studio designer.</span></span>  <span data-ttu-id="12f69-107">Siehe auch Gewusst [wie: Erstellen von Anwendungseinstellungen mithilfe des Designers](/previous-versions/visualstudio/visual-studio-2010/wabtadw6(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="12f69-107">Also see [How to: Create Application Settings Using the Designer](/previous-versions/visualstudio/visual-studio-2010/wabtadw6(v=vs.100)).</span></span>  
  
### <a name="to-create-new-application-settings-programmatically"></a><span data-ttu-id="12f69-108">So erstellen Sie programmgesteuert neue Anwendungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="12f69-108">To create new Application Settings programmatically</span></span>  
  
1. <span data-ttu-id="12f69-109">Fügen Sie dem Projekt eine neue Klasse hinzu, und benennen Sie diese um.</span><span class="sxs-lookup"><span data-stu-id="12f69-109">Add a new class to your project, and rename it.</span></span> <span data-ttu-id="12f69-110">Für dieses Verfahren wird diese Klasse aufgerufen `MyUserSettings` .</span><span class="sxs-lookup"><span data-stu-id="12f69-110">For this procedure, we will call this class `MyUserSettings`.</span></span> <span data-ttu-id="12f69-111">Ändern Sie die Klassendefinition so, dass die Klasse von <xref:System.Configuration.ApplicationSettingsBase> abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="12f69-111">Change the class definition so that the class derives from <xref:System.Configuration.ApplicationSettingsBase>.</span></span>  
  
2. <span data-ttu-id="12f69-112">Definieren Sie eine Eigenschaft für diese Wrapperklasse für jede benötigte Anwendungseinstellung, und wenden Sie diese Eigenschaft mit <xref:System.Configuration.ApplicationScopedSettingAttribute> oder mit <xref:System.Configuration.UserScopedSettingAttribute>, abhängig vom Bereich der Einstellung an.</span><span class="sxs-lookup"><span data-stu-id="12f69-112">Define a property on this wrapper class for each application setting you require, and apply that property with either the <xref:System.Configuration.ApplicationScopedSettingAttribute> or <xref:System.Configuration.UserScopedSettingAttribute>, depending on the scope of the setting.</span></span> <span data-ttu-id="12f69-113">Weitere Informationen zum Einstellungsbereich finden Sie unter [Übersicht über Anwendungseinstellungen](application-settings-overview.md).</span><span class="sxs-lookup"><span data-stu-id="12f69-113">For more information about settings scope, see [Application Settings Overview](application-settings-overview.md).</span></span> <span data-ttu-id="12f69-114">Ihr Code sollte jetzt wie folgt aussehen.</span><span class="sxs-lookup"><span data-stu-id="12f69-114">By now, your code should look like this:</span></span>  
  
     [!code-csharp[ApplicationSettings.Create#1](~/samples/snippets/csharp/VS_Snippets_Winforms/ApplicationSettings.Create/CS/MyAppSettings.cs#1)]
     [!code-vb[ApplicationSettings.Create#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ApplicationSettings.Create/VB/MyAppSettings.vb#1)]  
  
3. <span data-ttu-id="12f69-115">Erstellen Sie eine Instanz dieser Wrapperklasse in Ihrer Anwendung.</span><span class="sxs-lookup"><span data-stu-id="12f69-115">Create an instance of this wrapper class in your application.</span></span> <span data-ttu-id="12f69-116">Sie wird in der Regel ein privates Element des Hauptformulars sein.</span><span class="sxs-lookup"><span data-stu-id="12f69-116">It will commonly be a private member of the main form.</span></span> <span data-ttu-id="12f69-117">Nachdem Sie nun Ihre Klasse definiert haben, müssen Sie sie an eine Eigenschaft binden. In diesem Fall ist dies die Eigenschaft <xref:System.Windows.Forms.Form.BackColor%2A> des Formulars.</span><span class="sxs-lookup"><span data-stu-id="12f69-117">Now that you have defined your class, you need to bind it to a property; in this case, the <xref:System.Windows.Forms.Form.BackColor%2A> property of your form.</span></span> <span data-ttu-id="12f69-118">Dies können Sie im-Ereignishandler Ihres Formulars erreichen `Load` .</span><span class="sxs-lookup"><span data-stu-id="12f69-118">You can accomplish this in your form's `Load` event handler.</span></span>  
  
     [!code-csharp[ApplicationSettings.Create#2](~/samples/snippets/csharp/VS_Snippets_Winforms/ApplicationSettings.Create/CS/Form1.cs#2)]
     [!code-vb[ApplicationSettings.Create#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ApplicationSettings.Create/VB/Form1.vb#2)]  
  
4. <span data-ttu-id="12f69-119">Wenn Sie eine Möglichkeit zum Ändern von Einstellungen zur Laufzeit bereitstellen, müssen Sie die aktuellen Einstellungen des Benutzers auf dem Datenträger speichern, wenn das Formular geschlossen wird. Andernfalls gehen diese Änderungen verloren.</span><span class="sxs-lookup"><span data-stu-id="12f69-119">If you provide a way to change settings at run time, you will need to save the user's current settings to disk when your form closes, or else these changes will be lost.</span></span>  
  
     [!code-csharp[ApplicationSettings.Create#3](~/samples/snippets/csharp/VS_Snippets_Winforms/ApplicationSettings.Create/CS/Form1.cs#3)]
     [!code-vb[ApplicationSettings.Create#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ApplicationSettings.Create/VB/Form1.vb#3)]  
  
     <span data-ttu-id="12f69-120">Sie haben nun erfolgreich eine neue Anwendungseinstellung erstellt und diese an die angegebene Eigenschaft gebunden.</span><span class="sxs-lookup"><span data-stu-id="12f69-120">You have now successfully created a new application setting and bound it to the specified property.</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="12f69-121">.NET Framework-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="12f69-121">.NET Framework Security</span></span>  

 <span data-ttu-id="12f69-122">Der Standardeinstellungsanbieter (<xref:System.Configuration.LocalFileSettingsProvider>) speichert Informationen in Konfigurationsdateien als Nur-Text persistent.</span><span class="sxs-lookup"><span data-stu-id="12f69-122">The default settings provider, <xref:System.Configuration.LocalFileSettingsProvider>, persists information to configuration files as plain text.</span></span> <span data-ttu-id="12f69-123">Auf diese Weise wird die Sicherheit für die Dateizugriffssicherheit eingeschränkt, die vom Betriebssystem für den aktuellen Benutzer bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="12f69-123">This limits security to the file access security provided by the operating system for the current user.</span></span> <span data-ttu-id="12f69-124">Aus diesem Grund müssen die Informationen, die in Konfigurationsdateien gespeichert werden, sorgfältig ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="12f69-124">Because of this, care must be taken with the information stored in configuration files.</span></span> <span data-ttu-id="12f69-125">Häufig werden z. B. Anwendungseinstellungen zum Speichern von Verbindungszeichenfolgen verwendet, die auf den Datenspeicher der Anwendung zeigen.</span><span class="sxs-lookup"><span data-stu-id="12f69-125">For example, one common use for application settings is to store connection strings that point to the application's data store.</span></span> <span data-ttu-id="12f69-126">Allerdings sollten diese Zeichenfolgen aus Sicherheitsgründen keine Kennwörter enthalten.</span><span class="sxs-lookup"><span data-stu-id="12f69-126">However, because of security concerns, such strings should not include passwords.</span></span> <span data-ttu-id="12f69-127">Weitere Informationen zu Verbindungszeichenfolgen finden Sie unter <xref:System.Configuration.SpecialSetting>.</span><span class="sxs-lookup"><span data-stu-id="12f69-127">For more information about connection strings, see <xref:System.Configuration.SpecialSetting>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="12f69-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12f69-128">See also</span></span>

- <xref:System.Configuration.SpecialSettingAttribute>
- <xref:System.Configuration.LocalFileSettingsProvider>
- [<span data-ttu-id="12f69-129">Übersicht über Anwendungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="12f69-129">Application Settings Overview</span></span>](application-settings-overview.md)
- [<span data-ttu-id="12f69-130">Vorgehensweise: Überprüfen von Anwendungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="12f69-130">How to: Validate Application Settings</span></span>](how-to-validate-application-settings.md)
