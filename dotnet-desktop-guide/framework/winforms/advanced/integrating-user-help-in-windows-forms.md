---
title: Integrieren der Benutzerhilfe
ms.date: 03/30/2017
helpviewer_keywords:
- Help [Windows Forms], Windows Forms (using designer)
- Windows Forms, Help (using designer)
- HTML Help [Windows Forms], Windows Forms (using designer)
- Help [Windows Forms], Windows applications (using designer)
- forms. Help (using designer)
- Windows applications [Windows Forms], Help (using designer)
ms.assetid: a8563d25-8a75-4bc7-a024-f1870591b50f
ms.openlocfilehash: e1d9921b01c1fafe690a2727f2a45443d6f42728
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976089"
---
# <a name="integrating-user-help-in-windows-forms"></a><span data-ttu-id="4a186-102">Integrieren von Benutzerhilfe in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4a186-102">Integrating User Help in Windows Forms</span></span>
<span data-ttu-id="4a186-103">Ein wichtiger, aber oft übersehen Aspekt der Bildung von Windows-basierten Anwendungen ist das Hilfesystem, da Benutzer in Zeiten von Verwirrung auf Unterstützung setzen.</span><span class="sxs-lookup"><span data-stu-id="4a186-103">An essential, but often overlooked, aspect of building Windows-based applications is the Help system, as this is where users turn for assistance in times of confusion.</span></span> <span data-ttu-id="4a186-104">Windows Forms unterstützen zwei verschiedene Arten von Hilfe, die jeweils von der [HelpProvider-Komponente](../controls/helpprovider-component-windows-forms.md)bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4a186-104">Windows Forms support two different types of Help, each provided by the [HelpProvider Component](../controls/helpprovider-component-windows-forms.md).</span></span> <span data-ttu-id="4a186-105">Der erste Punkt besteht darin, den Benutzer auf eine Hilfedatei der HTML-oder HTML-Hilfe 1 zu verweisen. das Format *x* oder höher.</span><span class="sxs-lookup"><span data-stu-id="4a186-105">The first involves pointing the user to a Help file of either HTML or HTML Help 1.*x* or greater format.</span></span> <span data-ttu-id="4a186-106">Die zweite kann eine kurze "What es this"-typhilfe zu einzelnen Steuerelementen anzeigen. Dies ist besonders nützlich in Dialogfeldern.</span><span class="sxs-lookup"><span data-stu-id="4a186-106">The second can display brief "What's This"-type Help on individual controls; this is especially useful on dialog boxes.</span></span> <span data-ttu-id="4a186-107">Beide Arten von Hilfe können im gleichen Formular verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a186-107">Both types of Help can be used on the same form.</span></span>  
  
 <span data-ttu-id="4a186-108">Außerdem kann die QuickInfo- [Komponente](../controls/tooltip-component-windows-forms.md) verwendet werden, um einzelne Hilfe für Steuerelemente auf Windows Forms bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="4a186-108">Additionally, the [ToolTip Component](../controls/tooltip-component-windows-forms.md) can be used to provide individual Help for controls on Windows Forms.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="4a186-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4a186-109">In This Section</span></span>  
 [<span data-ttu-id="4a186-110">Vorgehensweise: Bereitstellen von Hilfe in einer Windows-Anwendung</span><span class="sxs-lookup"><span data-stu-id="4a186-110">How to: Provide Help in a Windows Application</span></span>](how-to-provide-help-in-a-windows-application.md)  
 <span data-ttu-id="4a186-111">Erläutert, wie die- `HelpProvider` Komponente verwendet wird, um Steuerelemente mit Dateien in einem Hilfesystem zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="4a186-111">Explains how to use the `HelpProvider` component to link controls to files in a Help system.</span></span>  
  
 [<span data-ttu-id="4a186-112">Vorgehensweise: Anzeigen der kontextbezogenen Hilfe</span><span class="sxs-lookup"><span data-stu-id="4a186-112">How to: Display Pop-up Help</span></span>](how-to-display-pop-up-help.md)  
 <span data-ttu-id="4a186-113">Erläutert die Verwendung der- `HelpProvider` Komponente zum Anzeigen der Popup Hilfe auf Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="4a186-113">Explains how to use the `HelpProvider` component to show pop-up Help on Windows Forms.</span></span>  
  
 [<span data-ttu-id="4a186-114">Benutzerführung mithilfe von QuickInfos</span><span class="sxs-lookup"><span data-stu-id="4a186-114">Control Help Using ToolTips</span></span>](control-help-using-tooltips.md)  
 <span data-ttu-id="4a186-115">Beschreibt die Verwendung der `ToolTip` -Komponente, um die Steuerelement spezifische Hilfe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4a186-115">Describes using the `ToolTip` component to show control-specific Help.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="4a186-116">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="4a186-116">Related Sections</span></span>  
 [<span data-ttu-id="4a186-117">HelpProvider-Komponente</span><span class="sxs-lookup"><span data-stu-id="4a186-117">HelpProvider Component</span></span>](../controls/helpprovider-component-windows-forms.md)  
 <span data-ttu-id="4a186-118">Erläutert die Grundlagen der `HelpProvider` Komponente.</span><span class="sxs-lookup"><span data-stu-id="4a186-118">Explains the basics of the `HelpProvider` component.</span></span>  
  
 [<span data-ttu-id="4a186-119">ToolTip-Komponente</span><span class="sxs-lookup"><span data-stu-id="4a186-119">ToolTip Component</span></span>](../controls/tooltip-component-windows-forms.md)  
 <span data-ttu-id="4a186-120">Erläutert die Grundlagen der `ToolTip` Komponente.</span><span class="sxs-lookup"><span data-stu-id="4a186-120">Explains the basics of the `ToolTip` component.</span></span>  
  
 [<span data-ttu-id="4a186-121">Übersicht über Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4a186-121">Windows Forms Overview</span></span>](../windows-forms-overview.md)  
 <span data-ttu-id="4a186-122">Erläutert die Grundlagen von Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="4a186-122">Explains the basics of Windows Forms.</span></span>  
  
 [<span data-ttu-id="4a186-123">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="4a186-123">Windows Forms</span></span>](../index.yml)  
 <span data-ttu-id="4a186-124">Bietet einen Überblick über Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="4a186-124">Provides an overview of Windows Forms.</span></span>
