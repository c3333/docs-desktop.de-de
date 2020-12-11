---
title: Leistungsoptimierung im DataGridView-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], performance tuning
- performance [Windows Forms], DataGridView control
- performance tuning [Windows Forms], data grids
ms.assetid: 6ccbff28-a0ff-41e4-b601-61b31b61851d
ms.openlocfilehash: 77ad86c4cd606bcf074473c97371ec27bcc5605b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976228"
---
# <a name="performance-tuning-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="7d950-102">Leistungsoptimierung im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7d950-102">Performance Tuning in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="7d950-103">Beim Arbeiten mit großen Datenmengen `DataGridView` kann das Steuerelement eine große Menge an Arbeitsspeicher beanspruchen, es sei denn, Sie verwenden es sorgfältig.</span><span class="sxs-lookup"><span data-stu-id="7d950-103">When working with large amounts of data, the `DataGridView` control can consume a large amount of memory in overhead, unless you use it carefully.</span></span> <span data-ttu-id="7d950-104">Auf Clients mit eingeschränktem Arbeitsspeicher können Sie einen Teil dieses Aufwands vermeiden, indem Sie Features vermeiden, die hohe Arbeitsspeicher Kosten haben.</span><span class="sxs-lookup"><span data-stu-id="7d950-104">On clients with limited memory, you can avoid some of this overhead by avoiding features that have a high memory cost.</span></span> <span data-ttu-id="7d950-105">Sie können auch einige oder alle Aufgaben zur Daten Wartung und-Abruf selbst verwalten, indem Sie den virtuellen Modus verwenden, um die Speicherauslastung für Ihr Szenario anzupassen.</span><span class="sxs-lookup"><span data-stu-id="7d950-105">You can also manage some or all of the data maintenance and retrieval tasks yourself using virtual mode in order to customize the memory usage for your scenario.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="7d950-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7d950-106">In This Section</span></span>  
 [<span data-ttu-id="7d950-107">Empfohlene Vorgehensweisen für das Skalieren des DataGridView-Steuerelements in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7d950-107">Best Practices for Scaling the Windows Forms DataGridView Control</span></span>](best-practices-for-scaling-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="7d950-108">Beschreibt, wie das `DataGridView` -Steuerelement so verwendet wird, dass unnötige Speicherauslastung und Leistungseinbußen bei der Arbeit mit großen Datenmengen vermieden werden.</span><span class="sxs-lookup"><span data-stu-id="7d950-108">Describes how to use the `DataGridView` control in a way that avoids unnecessary memory usage and performance penalties when working with large amounts of data.</span></span>  
  
 [<span data-ttu-id="7d950-109">Virtueller Modus im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7d950-109">Virtual Mode in the Windows Forms DataGridView Control</span></span>](virtual-mode-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="7d950-110">Beschreibt, wie Sie den virtuellen Modus verwenden, um den standardmäßigen Daten Bindungs Mechanismus zu ergänzen oder zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7d950-110">Describes how to use virtual mode to supplement or replace the standard data-binding mechanism.</span></span>  
  
 [<span data-ttu-id="7d950-111">Exemplarische Vorgehensweise: Implementieren des virtuellen Modus im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7d950-111">Walkthrough: Implementing Virtual Mode in the Windows Forms DataGridView Control</span></span>](implementing-virtual-mode-wf-datagridview-control.md)  
 <span data-ttu-id="7d950-112">Beschreibt das Implementieren von Handlern für mehrere Ereignisse im virtuellen Modus.</span><span class="sxs-lookup"><span data-stu-id="7d950-112">Describes how to implement handlers for several virtual-mode events.</span></span> <span data-ttu-id="7d950-113">Außerdem wird veranschaulicht, wie ein Rollback auf Zeilenebene implementiert und ein Commit für Benutzer bearbeitvorgänge ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7d950-113">Also demonstrates how to implement row-level rollback and commit for user edits.</span></span>  
  
 [<span data-ttu-id="7d950-114">Implementieren des virtuellen Modus mit Just-In-Time-Laden von Daten in das DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7d950-114">Implementing Virtual Mode with Just-In-Time Data Loading in the Windows Forms DataGridView Control</span></span>](implementing-virtual-mode-jit-data-loading-in-the-datagrid.md)  
 <span data-ttu-id="7d950-115">Beschreibt, wie Daten bei Bedarf geladen werden. Dies ist nützlich, wenn Sie mehr Daten anzeigen müssen, als der verfügbare Client Speicher speichern kann.</span><span class="sxs-lookup"><span data-stu-id="7d950-115">Describes how to load data on demand, which is useful when you have more data to display than the available client memory can store.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="7d950-116">Verweis</span><span class="sxs-lookup"><span data-stu-id="7d950-116">Reference</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <span data-ttu-id="7d950-117">Enthält die Referenzdokumentation für das <xref:System.Windows.Forms.DataGridView>-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="7d950-117">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.VirtualMode%2A>  
 <span data-ttu-id="7d950-118">Enthält die Referenz Dokumentation für die- <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7d950-118">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.VirtualMode%2A> property.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="7d950-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d950-119">See also</span></span>

- [<span data-ttu-id="7d950-120">DataGridView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="7d950-120">DataGridView Control</span></span>](datagridview-control-windows-forms.md)
- [<span data-ttu-id="7d950-121">Datenanzeigemodi im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7d950-121">Data Display Modes in the Windows Forms DataGridView Control</span></span>](data-display-modes-in-the-windows-forms-datagridview-control.md)
