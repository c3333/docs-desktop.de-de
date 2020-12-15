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
# <a name="whats-new-windows-forms-net"></a><span data-ttu-id="9c8c7-105">Neuerungen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="9c8c7-105">What's new (Windows Forms .NET)</span></span>

<span data-ttu-id="9c8c7-106">Windows Forms für .NET 5.0 enthält nun die folgenden Features und Verbesserungen gegenüber .NET Framework.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-106">Windows Forms for .NET 5.0 adds the following features and enhancements over .NET Framework.</span></span>

<span data-ttu-id="9c8c7-107">Es gibt einige Breaking Changes, die Sie bei der Migration von .NET Framework zu .NET 5.0 beachten sollten.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-107">There are a few breaking changes you should be aware of when migrating from .NET Framework to .NET 5.0.</span></span> <span data-ttu-id="9c8c7-108">Weitere Informationen finden Sie unter [Breaking Changes in Windows Forms](/dotnet/core/compatibility/winforms).</span><span class="sxs-lookup"><span data-stu-id="9c8c7-108">For more information, see [Breaking changes in Windows Forms](/dotnet/core/compatibility/winforms).</span></span>

## <a name="enhanced-features"></a><span data-ttu-id="9c8c7-109">Verbesserte Features</span><span class="sxs-lookup"><span data-stu-id="9c8c7-109">Enhanced features</span></span>

- <span data-ttu-id="9c8c7-110">Muster der Microsoft-Benutzeroberflächenautomatisierung funktionieren mit Tools für Barrierefreiheit wie Narrator und Jaws besser.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-110">Microsoft UI Automation patterns work better with accessibility tools like Narrator and Jaws.</span></span>
- <span data-ttu-id="9c8c7-111">Verbesserte Leistung.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-111">Improved performance.</span></span>
- <span data-ttu-id="9c8c7-112">In der VB.NET-Projektvorlage werden für hohe DPI-Auflösungen wie bei 4K-Bildschirmen standardmäßig die DPI SystemAware-Einstellungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-112">The VB.NET project template defaults to DPI SystemAware settings for high DPI resolutions such as 4k monitors.</span></span>
- <span data-ttu-id="9c8c7-113">Die Standardschriftart entspricht den aktuellen Windows-Entwurfsempfehlungen.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-113">The default font matches the current Windows design recommendations.</span></span>

  > [!CAUTION]
  > <span data-ttu-id="9c8c7-114">Das kann sich auf das Layout von Anwendungen auswirken, die von .NET Framework migriert werden.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-114">This may impact the layout of apps migrated from .NET Framework.</span></span>

## <a name="new-controls"></a><span data-ttu-id="9c8c7-115">Neue Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="9c8c7-115">New controls</span></span>

<span data-ttu-id="9c8c7-116">Die folgenden Steuerelemente sind seit der Portierung von Windows Forms zu .NET Framework verfügbar:</span><span class="sxs-lookup"><span data-stu-id="9c8c7-116">The following controls have been added since Windows Forms was ported to .NET Framework:</span></span>

- <xref:System.Windows.Forms.TaskDialog?displayProperty=fullName>
  
  <span data-ttu-id="9c8c7-117">Bei einem Aufgabendialogfeld handelt es sich um ein Dialogfeld zum Anzeigen von Informationen und zum Entgegennehmen einfacher Eingaben des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-117">A task dialog is a dialog box that can be used to display information and receive simple input from the user.</span></span> <span data-ttu-id="9c8c7-118">Es wird wie ein Meldungsfeld vom Betriebssystem nach Parametern formatiert, die Sie festlegen.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-118">Like a message box, it's formatted by the operating system according to parameters you set.</span></span> <span data-ttu-id="9c8c7-119">Im Vergleich zu einem Meldungsfeld enthält ein Aufgabendialogfeld mehr Features.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-119">Task dialog has more features than a message box.</span></span> <span data-ttu-id="9c8c7-120">Weitere Informationen finden Sie unter [Beispiel für ein Aufgabendialogfeld](https://github.com/dotnet/samples/tree/master/windowsforms/TaskDialogDemo).</span><span class="sxs-lookup"><span data-stu-id="9c8c7-120">For more information, see the [Task dialog sample](https://github.com/dotnet/samples/tree/master/windowsforms/TaskDialogDemo).</span></span>

- <xref:Microsoft.Web.WebView2.WinForms.WebView2?displayProperty=fullName>

  <span data-ttu-id="9c8c7-121">Ein neues Webbrowsersteuerelement mit moderner Webunterstützung.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-121">A new web browser control with modern web support.</span></span> <span data-ttu-id="9c8c7-122">Basierend auf Edge (Chromium).</span><span class="sxs-lookup"><span data-stu-id="9c8c7-122">Based on Edge (Chromium).</span></span> <span data-ttu-id="9c8c7-123">Weitere Informationen finden Sie unter [Erste Schritte mit WebView2 in Windows Forms](/microsoft-edge/webview2/gettingstarted/winforms).</span><span class="sxs-lookup"><span data-stu-id="9c8c7-123">For more information, see [Getting started with WebView2 in Windows Forms](/microsoft-edge/webview2/gettingstarted/winforms).</span></span>

## <a name="enhanced-controls"></a><span data-ttu-id="9c8c7-124">Erweiterte Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="9c8c7-124">Enhanced controls</span></span>

- <xref:System.Windows.Forms.ListView?displayProperty=fullName>

  - <span data-ttu-id="9c8c7-125">Unterstützt reduzierbare Gruppen</span><span class="sxs-lookup"><span data-stu-id="9c8c7-125">Supports collapsible groups</span></span>
  - <span data-ttu-id="9c8c7-126">Fußzeilen</span><span class="sxs-lookup"><span data-stu-id="9c8c7-126">Footers</span></span>
  - <span data-ttu-id="9c8c7-127">Untertitel-, Aufgaben- und Titelbilder einer Gruppe</span><span class="sxs-lookup"><span data-stu-id="9c8c7-127">Group subtitle, task, and title images</span></span>

- <xref:System.Windows.Forms.FolderBrowserDialog?displayProperty=fullName>

  <span data-ttu-id="9c8c7-128">Dieses Dialogfeld wurde aktualisiert, sodass nun anstelle der alten Windows 7-Benutzeroberfläche die moderne Windows-Benutzeroberfläche verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-128">This dialog has been upgraded to use the modern Windows experience instead of the old Windows 7 experience.</span></span>

- <xref:System.Windows.Forms.FileDialog?displayProperty=fullName>

  - <span data-ttu-id="9c8c7-129">Ab der neuen Version wird <xref:System.Windows.Forms.FileDialog.ClientGuid> unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-129">Added support for <xref:System.Windows.Forms.FileDialog.ClientGuid>.</span></span>

    <span data-ttu-id="9c8c7-130">Mit `ClientGuid` kann eine aufrufende Anwendung dem persistenten Zustand eines Dialogfelds eine GUID zuordnen.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-130">`ClientGuid` enables a calling application to associate a GUID with a dialog's persisted state.</span></span> <span data-ttu-id="9c8c7-131">Der Zustand eines Dialogfelds kann Faktoren wie den zuletzt besuchten Ordner und die Position und Größe des Dialogfelds beinhalten.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-131">A dialog's state can include factors such as the last visited folder and the position and size of the dialog.</span></span> <span data-ttu-id="9c8c7-132">Dieser Zustand wird in der Regel basierend auf dem Namen der ausführbaren Datei beibehalten.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-132">Typically, this state is persisted based on the name of the executable file.</span></span> <span data-ttu-id="9c8c7-133">Mit `ClientGuid` kann eine Anwendung innerhalb einer Anwendung unterschiedliche Zustände des Dialogfelds beibehalten.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-133">With `ClientGuid`, an application can persist  different states of the dialog within the same application.</span></span>

- <xref:System.Windows.Forms.TextRenderer?displayProperty=fullName>

  <span data-ttu-id="9c8c7-134">Ab der neuen Version wird zur Verbesserung der Leistung beim Rendern von Text <xref:System.ReadOnlySpan%601> unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9c8c7-134">Support added for <xref:System.ReadOnlySpan%601> to enhance performance of rendering text.</span></span>

## <a name="see-also"></a><span data-ttu-id="9c8c7-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c8c7-135">See also</span></span>

- [<span data-ttu-id="9c8c7-136">Breaking Changes bei Windows Forms</span><span class="sxs-lookup"><span data-stu-id="9c8c7-136">Breaking changes in Windows Forms</span></span>](/dotnet/core/compatibility/winforms)
- [<span data-ttu-id="9c8c7-137">Tutorial: Erstellen einer neuen WinForms-Anwendung (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="9c8c7-137">Tutorial: Create a new WinForms app (Windows Forms .NET)</span></span>](../get-started/create-app-visual-studio.md)
- [<span data-ttu-id="9c8c7-138">Migrieren einer Windows Forms-Desktopanwendung zu .NET 5</span><span class="sxs-lookup"><span data-stu-id="9c8c7-138">How to migrate a Windows Forms desktop app to .NET 5</span></span>](../migration/index.md)
