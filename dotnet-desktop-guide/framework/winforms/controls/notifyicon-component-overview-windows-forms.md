---
title: Übersicht über die NotifyIcon-Komponente
ms.date: 03/30/2017
f1_keywords:
- NotifyIcon
helpviewer_keywords:
- NotifyIcon component [Windows Forms], about NotifyIcon component
- system tray icons [Windows Forms], about system tray icons
- system tray icons [Windows Forms], using in Windows Forms
ms.assetid: 5b9189fa-d4ae-41a6-9b97-eb1f44bb1a69
ms.openlocfilehash: 587bf514db853f1122ed16abc05a195985c5ce8d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976701"
---
# <a name="notifyicon-component-overview-windows-forms"></a><span data-ttu-id="e425c-102">Übersicht über die NotifyIcon-Komponente (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="e425c-102">NotifyIcon Component Overview (Windows Forms)</span></span>

<span data-ttu-id="e425c-103">Die <xref:System.Windows.Forms.NotifyIcon>-Komponente von Windows Forms wird in der Regel verwendet, um Symbole für Prozesse anzuzeigen, die im Hintergrund ausgeführt werden und für die nur selten eine Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e425c-103">The Windows Forms <xref:System.Windows.Forms.NotifyIcon> component is typically used to display icons for processes that run in the background and do not show a user interface much of the time.</span></span> <span data-ttu-id="e425c-104">Ein Beispiel ist ein Virenschutzprogramm, auf das durch Klicken auf ein Symbol im Statusbereich der Taskleiste zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e425c-104">An example would be a virus protection program that can be accessed by clicking an icon in the status notification area of the taskbar.</span></span>

## <a name="key-properties-of-notifyicons"></a><span data-ttu-id="e425c-105">Haupteigenschaften von NotifyIcons</span><span class="sxs-lookup"><span data-stu-id="e425c-105">Key Properties of NotifyIcons</span></span>

<span data-ttu-id="e425c-106">Jede <xref:System.Windows.Forms.NotifyIcon>-Komponente zeigt ein einzelnes Symbol im Statusbereich an.</span><span class="sxs-lookup"><span data-stu-id="e425c-106">Each <xref:System.Windows.Forms.NotifyIcon> component displays a single icon in the status area.</span></span> <span data-ttu-id="e425c-107">Wenn drei Hintergrundprozesse ausgeführt werden, für die jeweils ein Symbol angezeigt werden soll, müssen Sie dem Formular drei <xref:System.Windows.Forms.NotifyIcon>-Komponenten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e425c-107">If you have three background processes and wish to display an icon for each, you must add three <xref:System.Windows.Forms.NotifyIcon> components to the form.</span></span> <span data-ttu-id="e425c-108">Die wichtigsten Eigenschaften der <xref:System.Windows.Forms.NotifyIcon>-Komponente sind <xref:System.Windows.Forms.NotifyIcon.Icon%2A> und <xref:System.Windows.Forms.NotifyIcon.Visible%2A>.</span><span class="sxs-lookup"><span data-stu-id="e425c-108">The key properties of the <xref:System.Windows.Forms.NotifyIcon> component are <xref:System.Windows.Forms.NotifyIcon.Icon%2A> and <xref:System.Windows.Forms.NotifyIcon.Visible%2A>.</span></span> <span data-ttu-id="e425c-109">Mit der <xref:System.Windows.Forms.NotifyIcon.Icon%2A>-Eigenschaft wird das Symbol festgelegt, das im Statusbereich angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="e425c-109">The <xref:System.Windows.Forms.NotifyIcon.Icon%2A> property sets the icon that appears in the status area.</span></span> <span data-ttu-id="e425c-110">Damit das Symbol angezeigt wird, muss die <xref:System.Windows.Forms.NotifyIcon.Visible%2A>-Eigenschaft auf `true` festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="e425c-110">In order for the icon to appear, the <xref:System.Windows.Forms.NotifyIcon.Visible%2A> property must be set to `true`.</span></span>

## <a name="notifyicons-options"></a><span data-ttu-id="e425c-111">Optionen für NotifyIcons</span><span class="sxs-lookup"><span data-stu-id="e425c-111">NotifyIcons Options</span></span>

<span data-ttu-id="e425c-112">Sie können SprechblasenInfos, Kontextmenüs und QuickInfos mit einem <xref:System.Windows.Forms.NotifyIcon> verknüpfen, um den Benutzer zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e425c-112">You can associate balloon tips, shortcut menus, and ToolTips with a <xref:System.Windows.Forms.NotifyIcon> to assist the user.</span></span>

<span data-ttu-id="e425c-113">Sie können eine SprechblasenInfo für ein <xref:System.Windows.Forms.NotifyIcon> anzeigen, indem Sie die <xref:System.Windows.Forms.NotifyIcon.ShowBalloonTip%2A>-Methode aufrufen und die Zeitspanne angeben, für die die SprechblasenInfo angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e425c-113">You can display balloon tips for a <xref:System.Windows.Forms.NotifyIcon> by calling the <xref:System.Windows.Forms.NotifyIcon.ShowBalloonTip%2A> method specifying the time span you wish the balloon tip to display.</span></span> <span data-ttu-id="e425c-114">Über <xref:System.Windows.Forms.NotifyIcon.BalloonTipText%2A>, <xref:System.Windows.Forms.NotifyIcon.BalloonTipIcon%2A> bzw. <xref:System.Windows.Forms.NotifyIcon.BalloonTipTitle%2A> können Sie auch den Text, das Symbol bzw. den Titel der SprechblasenInfo angeben.</span><span class="sxs-lookup"><span data-stu-id="e425c-114">You can also specify the text, icon and title of the balloon tip with the <xref:System.Windows.Forms.NotifyIcon.BalloonTipText%2A>, <xref:System.Windows.Forms.NotifyIcon.BalloonTipIcon%2A> and <xref:System.Windows.Forms.NotifyIcon.BalloonTipTitle%2A>, respectively.</span></span> <span data-ttu-id="e425c-115"><xref:System.Windows.Forms.NotifyIcon>-Komponenten können auch zugeordnete QuickInfos und Kontextmenüs haben.</span><span class="sxs-lookup"><span data-stu-id="e425c-115"><xref:System.Windows.Forms.NotifyIcon> components can also have associated ToolTips and shortcut menus.</span></span> <span data-ttu-id="e425c-116">Weitere Informationen finden Sie unter Übersicht über die [ToolTip-Komponente](tooltip-component-overview-windows-forms.md) und [Übersicht über die ContextMenu-Komponente](contextmenu-component-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="e425c-116">For more information, see [ToolTip Component Overview](tooltip-component-overview-windows-forms.md) and [ContextMenu Component Overview](contextmenu-component-overview-windows-forms.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="e425c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e425c-117">See also</span></span>

- <xref:System.Windows.Forms.NotifyIcon>
- [<span data-ttu-id="e425c-118">NotifyIcon-Komponente</span><span class="sxs-lookup"><span data-stu-id="e425c-118">NotifyIcon Component</span></span>](notifyicon-component-windows-forms.md)
