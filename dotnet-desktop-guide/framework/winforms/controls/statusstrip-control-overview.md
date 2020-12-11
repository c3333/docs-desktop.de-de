---
title: Übersicht über das StatusStrip-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- StatusStrip
helpviewer_keywords:
- StatusStrip control [Windows Forms], about StatusStrip control
- status bars [Windows Forms], about status bars
ms.assetid: c0d9bcbb-f8b8-46ef-bae2-4146b8c8ce99
ms.openlocfilehash: 9f2426220e8fe0f13d2098de8975be2ad2e43845
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976456"
---
# <a name="statusstrip-control-overview"></a><span data-ttu-id="9e699-102">Übersicht über das StatusStrip-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="9e699-102">StatusStrip Control Overview</span></span>

<span data-ttu-id="9e699-103">Ein <xref:System.Windows.Forms.StatusStrip>-Steuerelement zeigt Informationen zu einem Objekt an, das in einem <xref:System.Windows.Forms.Form> angezeigt wird, zu den Komponenten des Objekts oder Kontextinformationen, die sich auf die Operation dieses Objekts in Ihrer Anwendung beziehen.</span><span class="sxs-lookup"><span data-stu-id="9e699-103">A <xref:System.Windows.Forms.StatusStrip> control displays information about an object being viewed on a <xref:System.Windows.Forms.Form>, the object's components, or contextual information that relates to that object's operation within your application.</span></span> <span data-ttu-id="9e699-104">Ein <xref:System.Windows.Forms.StatusStrip>-Steuerelement besteht normalerweise aus <xref:System.Windows.Forms.ToolStripStatusLabel>-Objekten, von denen jedes Text, ein Symbol oder beides anzeigt.</span><span class="sxs-lookup"><span data-stu-id="9e699-104">Typically, a <xref:System.Windows.Forms.StatusStrip> control consists of <xref:System.Windows.Forms.ToolStripStatusLabel> objects, each of which displays text, an icon, or both.</span></span> <span data-ttu-id="9e699-105">Der <xref:System.Windows.Forms.StatusStrip> kann zudem auch <xref:System.Windows.Forms.ToolStripDropDownButton>-, <xref:System.Windows.Forms.ToolStripSplitButton> und <xref:System.Windows.Forms.ToolStripProgressBar>-Steuerelemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="9e699-105">The <xref:System.Windows.Forms.StatusStrip> can also contain <xref:System.Windows.Forms.ToolStripDropDownButton>, <xref:System.Windows.Forms.ToolStripSplitButton>, and <xref:System.Windows.Forms.ToolStripProgressBar> controls.</span></span>  
  
 <span data-ttu-id="9e699-106">Der standardmäßige <xref:System.Windows.Forms.StatusStrip> weist keine Panels auf.</span><span class="sxs-lookup"><span data-stu-id="9e699-106">The default <xref:System.Windows.Forms.StatusStrip> has no panels.</span></span> <span data-ttu-id="9e699-107">Verwenden Sie die <xref:System.Windows.Forms.ToolStripItemCollection.AddRange%2A?displayProperty=nameWithType>-Methode, um einem <xref:System.Windows.Forms.StatusStrip> Panels hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="9e699-107">To add panels to a <xref:System.Windows.Forms.StatusStrip>, use the <xref:System.Windows.Forms.ToolStripItemCollection.AddRange%2A?displayProperty=nameWithType> method.</span></span>  
  
 <span data-ttu-id="9e699-108">Es gibt umfassende Unterstützung für den Umgang mit <xref:System.Windows.Forms.StatusStrip>-Elementen und häufig verwendeten Befehle in Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9e699-108">There is extensive support for handling <xref:System.Windows.Forms.StatusStrip> items and common commands in Visual Studio.</span></span>  
  
 <span data-ttu-id="9e699-109">Siehe auch Dialog Feld "Status Strip-Elementauflistungs- [Editor](/previous-versions/visualstudio/visual-studio-2010/ms233631(v=vs.100)) " und " [Status Strip-Aufgaben](/previous-versions/visualstudio/visual-studio-2010/ms233642(v=vs.100))".</span><span class="sxs-lookup"><span data-stu-id="9e699-109">Also see [StatusStrip Items Collection Editor](/previous-versions/visualstudio/visual-studio-2010/ms233631(v=vs.100)) and [StatusStrip Tasks Dialog Box](/previous-versions/visualstudio/visual-studio-2010/ms233642(v=vs.100)).</span></span>  
  
 <span data-ttu-id="9e699-110">Obwohl <xref:System.Windows.Forms.StatusStrip> das <xref:System.Windows.Forms.StatusBar>-Steuerelement vorheriger Versionen ersetzt und erweitert, wird das <xref:System.Windows.Forms.StatusBar>-Steuerelement sowohl aus Gründen der Abwärtskompatibilität als auch, falls gewünscht, für die zukünftige Verwendung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="9e699-110">Although <xref:System.Windows.Forms.StatusStrip> replaces and extends the <xref:System.Windows.Forms.StatusBar> control of previous versions, <xref:System.Windows.Forms.StatusBar> is retained for both backward compatibility and future use if you choose.</span></span>  
  
### <a name="important-statusstrip-members"></a><span data-ttu-id="9e699-111">Wichtige StatusStrip-Member</span><span class="sxs-lookup"><span data-stu-id="9e699-111">Important StatusStrip Members</span></span>  
  
|<span data-ttu-id="9e699-112">Name</span><span class="sxs-lookup"><span data-stu-id="9e699-112">Name</span></span>|<span data-ttu-id="9e699-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e699-113">Description</span></span>|  
|----------|-----------------|  
|<xref:System.Windows.Forms.StatusStrip.CanOverflow%2A>|<span data-ttu-id="9e699-114">Ruft einen Wert ab, der angibt, ob <xref:System.Windows.Forms.StatusStrip> Überlauffunktionen unterstützt, bzw. legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="9e699-114">Gets or sets a value indicating whether the <xref:System.Windows.Forms.StatusStrip> supports overflow functionality.</span></span>|  
|<xref:System.Windows.Forms.StatusStrip.Stretch%2A>|<span data-ttu-id="9e699-115">Ruft einen Wert ab, der angibt, ob sich das <xref:System.Windows.Forms.StatusStrip>-Objekt in seinem <xref:System.Windows.Forms.ToolStripContainer>-Objekt von einem Ende zum anderen Ende erstreckt, oder legt diesen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="9e699-115">Gets or sets a value indicating whether the <xref:System.Windows.Forms.StatusStrip> stretches from end to end in its <xref:System.Windows.Forms.ToolStripContainer>.</span></span>|  
  
### <a name="important-statusstrip-companion-classes"></a><span data-ttu-id="9e699-116">Wichtige StatusStrip-Begleitklassen</span><span class="sxs-lookup"><span data-stu-id="9e699-116">Important StatusStrip Companion Classes</span></span>  
  
|<span data-ttu-id="9e699-117">Name</span><span class="sxs-lookup"><span data-stu-id="9e699-117">Name</span></span>|<span data-ttu-id="9e699-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e699-118">Description</span></span>|  
|----------|-----------------|  
|<xref:System.Windows.Forms.ToolStripStatusLabel>|<span data-ttu-id="9e699-119">Stellt ein Panel in einem <xref:System.Windows.Forms.StatusStrip>-Steuerelement dar.</span><span class="sxs-lookup"><span data-stu-id="9e699-119">Represents a panel in a <xref:System.Windows.Forms.StatusStrip> control.</span></span>|  
|<xref:System.Windows.Forms.ToolStripDropDownButton>|<span data-ttu-id="9e699-120">Zeigt eine zugehörige <xref:System.Windows.Forms.ToolStripDropDown> an, aus der der Benutzer ein einzelnes Element auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="9e699-120">Displays an associated <xref:System.Windows.Forms.ToolStripDropDown> from which the user can select a single item.</span></span>|  
|<xref:System.Windows.Forms.ToolStripSplitButton>|<span data-ttu-id="9e699-121">Stellt ein zweiteiliges Steuerelement dar, das aus einer Standardschaltfläche und einem Dropdownmenü besteht.</span><span class="sxs-lookup"><span data-stu-id="9e699-121">Represents a two-part control that is a standard button and a drop-down menu.</span></span>|  
|<xref:System.Windows.Forms.ToolStripProgressBar>|<span data-ttu-id="9e699-122">Zeigt den Fortschrittsstatus eines Prozesses an.</span><span class="sxs-lookup"><span data-stu-id="9e699-122">Displays the completion state of a process.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="9e699-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e699-123">See also</span></span>

- <xref:System.Windows.Forms.StatusStrip>
- <xref:System.Windows.Forms.ToolStripStatusLabel>
- <xref:System.Windows.Forms.ToolStripStatusLabel.Spring%2A>
