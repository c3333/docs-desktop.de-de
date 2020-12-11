---
title: Übersicht über das ToolStripProgressBar-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- ToolStripProgressBar
helpviewer_keywords:
- toolbars [Windows Forms], progress bars
- progress controls [Windows Forms]
- ToolStripProgressBar control [Windows Forms], about ToolStripProgressBar control
ms.assetid: ec3ab522-5fe4-4b4d-a551-bc19e84f4774
ms.openlocfilehash: 380dabe2468ae3c7d9d7303498823d847a8d119e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977158"
---
# <a name="toolstripprogressbar-control-overview"></a><span data-ttu-id="d073c-102">Übersicht über das ToolStripProgressBar-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d073c-102">ToolStripProgressBar Control Overview</span></span>
<span data-ttu-id="d073c-103">Das <xref:System.Windows.Forms.ToolStripProgressBar> kombiniert die Rafting-und Renderingfunktionalität aller Steuer <xref:System.Windows.Forms.ToolStrip> Elemente mit der typischen Prozess Verfolgungs Funktion.</span><span class="sxs-lookup"><span data-stu-id="d073c-103">The <xref:System.Windows.Forms.ToolStripProgressBar> combines the rafting and rendering functionality of all <xref:System.Windows.Forms.ToolStrip> controls with its typical process-tracking functionality.</span></span> <span data-ttu-id="d073c-104">Eine <xref:System.Windows.Forms.ToolStripProgressBar> wird in der Regel von <xref:System.Windows.Forms.StatusStrip> und weniger häufig von einem gehostet <xref:System.Windows.Forms.ToolStrip> .</span><span class="sxs-lookup"><span data-stu-id="d073c-104">A <xref:System.Windows.Forms.ToolStripProgressBar> is most usually hosted by <xref:System.Windows.Forms.StatusStrip>, and less frequently by a <xref:System.Windows.Forms.ToolStrip>.</span></span>  
  
 <span data-ttu-id="d073c-105">Obwohl <xref:System.Windows.Forms.ToolStripProgressBar> das-Steuerelement in früheren Versionen ersetzt und Funktionen zum-Steuerelement hinzufügt, wird bei Bedarf <xref:System.Windows.Forms.ToolStripProgressBar> sowohl für die Abwärtskompatibilität als auch für die zukünftige Verwendung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="d073c-105">Although <xref:System.Windows.Forms.ToolStripProgressBar> replaces and adds functionality to the control in previous versions, <xref:System.Windows.Forms.ToolStripProgressBar> is retained for both backward compatibility and future use if desired.</span></span>  
  
### <a name="important-toolstripprogressbar-members"></a><span data-ttu-id="d073c-106">Wichtige ToolStripProgressBar-Elemente</span><span class="sxs-lookup"><span data-stu-id="d073c-106">Important ToolStripProgressBar Members</span></span>  
  
|<span data-ttu-id="d073c-107">Name</span><span class="sxs-lookup"><span data-stu-id="d073c-107">Name</span></span>|<span data-ttu-id="d073c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d073c-108">Description</span></span>|  
|----------|-----------------|  
|<xref:System.Windows.Forms.ToolStripProgressBar.MarqueeAnimationSpeed%2A>|<span data-ttu-id="d073c-109">Ruft einen Wert ab, der die Verzögerung zwischen den Aktualisierungen der <xref:System.Windows.Forms.ProgressBarStyle.Marquee>-Anzeige in Millisekunden darstellt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="d073c-109">Gets or sets a value representing the delay between each <xref:System.Windows.Forms.ProgressBarStyle.Marquee> display update, in milliseconds.</span></span>|  
|<xref:System.Windows.Forms.ProgressBar.Maximum%2A>|<span data-ttu-id="d073c-110">Ruft die Obergrenze des für diese <xref:System.Windows.Forms.ToolStripProgressBar> definierten Bereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="d073c-110">Gets or sets the upper bound of the range that is defined for this <xref:System.Windows.Forms.ToolStripProgressBar>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripProgressBar.Minimum%2A>|<span data-ttu-id="d073c-111">Ruft die Untergrenze des für die <xref:System.Windows.Forms.ToolStripProgressBar> definierten Bereichs ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="d073c-111">Gets or sets the lower bound of the range that is defined for this <xref:System.Windows.Forms.ToolStripProgressBar>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripProgressBar.Style%2A>|<span data-ttu-id="d073c-112">Ruft den Stil ab, mit dem der <xref:System.Windows.Forms.ToolStripProgressBar> Fortschritt eines Vorgangs angezeigt wird, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="d073c-112">Gets or sets the style that the <xref:System.Windows.Forms.ToolStripProgressBar> uses to display the progress of an operation.</span></span>|  
|<xref:System.Windows.Forms.ToolStripProgressBar.Value%2A>|<span data-ttu-id="d073c-113">Ruft den aktuellen Wert der <xref:System.Windows.Forms.ToolStripProgressBar> ab oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="d073c-113">Gets or sets the current value of the <xref:System.Windows.Forms.ToolStripProgressBar>.</span></span>|  
|<xref:System.Windows.Forms.ToolStripProgressBar.PerformStep%2A>|<span data-ttu-id="d073c-114">Erhöht die aktuelle Position der Statusanzeige um den Betrag der <xref:System.Windows.Forms.ToolStripProgressBar.Step%2A>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="d073c-114">Advances the current position of the progress bar by the amount of the <xref:System.Windows.Forms.ToolStripProgressBar.Step%2A> property.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="d073c-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d073c-115">See also</span></span>

- <xref:System.Windows.Forms.ToolStripProgressBar>
