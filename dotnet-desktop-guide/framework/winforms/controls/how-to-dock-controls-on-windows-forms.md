---
title: Andocken von Steuerelementen
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], docking
- Explorer-style applications [Windows Forms], creating
- Windows Forms controls, filling client area
ms.assetid: bc11f2e4-e90a-4830-b0e2-f43b6e2b8bec
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: 02f1c26dcb322a39c41781c83d8c820bd2fd27e0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976503"
---
# <a name="how-to-dock-controls-on-windows-forms"></a><span data-ttu-id="56c82-102">Gewusst wie: Andocken von Steuerelementen auf Windows Forms</span><span class="sxs-lookup"><span data-stu-id="56c82-102">How to: Dock controls on Windows Forms</span></span>

<span data-ttu-id="56c82-103">Sie können Steuerelemente an die Ränder Ihres Formulars andocken, oder Sie können den Container des Steuer Elements ausfüllen (entweder ein Formular oder ein Container Steuerelement).</span><span class="sxs-lookup"><span data-stu-id="56c82-103">You can dock controls to the edges of your form or have them fill the control's container (either a form or a container control).</span></span> <span data-ttu-id="56c82-104">Windows-Explorer Dockt das Steuerelement beispielsweise <xref:System.Windows.Forms.TreeView> an die linke Seite des Fensters und dessen <xref:System.Windows.Forms.ListView> Steuerelement auf der rechten Seite des Fensters an.</span><span class="sxs-lookup"><span data-stu-id="56c82-104">For example, Windows Explorer docks its <xref:System.Windows.Forms.TreeView> control to the left side of the window and its <xref:System.Windows.Forms.ListView> control to the right side of the window.</span></span> <span data-ttu-id="56c82-105">Verwenden Sie die- <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft für alle sichtbaren Windows Forms Steuerelemente, um den Docking Modus zu definieren.</span><span class="sxs-lookup"><span data-stu-id="56c82-105">Use the <xref:System.Windows.Forms.Control.Dock%2A> property for all visible Windows Forms controls to define the docking mode.</span></span>

> [!NOTE]
> <span data-ttu-id="56c82-106">Steuerelemente werden in umgekehrter z-Reihenfolge angedockt.</span><span class="sxs-lookup"><span data-stu-id="56c82-106">Controls are docked in reverse z-order.</span></span>

<span data-ttu-id="56c82-107">Die- <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft interagiert mit der- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="56c82-107">The <xref:System.Windows.Forms.Control.Dock%2A> property interacts with the <xref:System.Windows.Forms.Control.AutoSize%2A> property.</span></span> <span data-ttu-id="56c82-108">Weitere Informationen finden Sie unter [Übersicht über die AutoSize-Eigenschaft](autosize-property-overview.md).</span><span class="sxs-lookup"><span data-stu-id="56c82-108">For more information, see [AutoSize Property Overview](autosize-property-overview.md).</span></span>

## <a name="to-dock-a-control"></a><span data-ttu-id="56c82-109">Zum Andocken eines Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="56c82-109">To dock a control</span></span>

1. <span data-ttu-id="56c82-110">Wählen Sie in Visual Studio das Steuerelement aus, das Sie andocken möchten.</span><span class="sxs-lookup"><span data-stu-id="56c82-110">In Visual Studio, select the control that you want to dock.</span></span>

2. <span data-ttu-id="56c82-111">Klicken Sie im **Eigenschaften** Fenster auf den Pfeil rechts neben der- <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="56c82-111">In the **Properties** window, click the arrow to the right of the <xref:System.Windows.Forms.Control.Dock%2A> property.</span></span>

   <span data-ttu-id="56c82-112">Es wird ein Editor angezeigt, der eine Reihe von Feldern anzeigt, die die Ränder und den Mittelpunkt des Formulars darstellen.</span><span class="sxs-lookup"><span data-stu-id="56c82-112">An editor is displayed that shows a series of boxes representing the edges and the center of the form.</span></span>

3. <span data-ttu-id="56c82-113">Klicken Sie auf die Schaltfläche, die den Rand des Formulars darstellt, in dem Sie das Steuerelement andocken möchten.</span><span class="sxs-lookup"><span data-stu-id="56c82-113">Click the button that represents the edge of the form where you want to dock the control.</span></span> <span data-ttu-id="56c82-114">Um den Inhalt des Formular-oder Container Steuer Elements des Steuer Elements auszufüllen, klicken Sie auf das Feld Center.</span><span class="sxs-lookup"><span data-stu-id="56c82-114">To fill the contents of the control's form or container control, click the center box.</span></span> <span data-ttu-id="56c82-115">Klicken Sie zum Deaktivieren des Andock auf **(keine)** .</span><span class="sxs-lookup"><span data-stu-id="56c82-115">Click **(none)** to disable docking.</span></span>

   <span data-ttu-id="56c82-116">Die Größe des Steuer Elements wird automatisch an die Grenzen des angedockten Rands angepasst.</span><span class="sxs-lookup"><span data-stu-id="56c82-116">The control is automatically resized to fit the boundaries of the docked edge.</span></span>

   > [!NOTE]
   > <span data-ttu-id="56c82-117">Geerbte Steuerelemente müssen in der Lage sein, `Protected` angedockt zu werden.</span><span class="sxs-lookup"><span data-stu-id="56c82-117">Inherited controls must be `Protected` to be able to be docked.</span></span> <span data-ttu-id="56c82-118">Um die Zugriffsebene eines Steuer Elements zu ändern, legen Sie seine **modifizierereigenschaft** im Fenster **Eigenschaften** fest.</span><span class="sxs-lookup"><span data-stu-id="56c82-118">To change the access level of a control, set its **Modifier** property in the **Properties** window.</span></span>

## <a name="see-also"></a><span data-ttu-id="56c82-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56c82-119">See also</span></span>

- [<span data-ttu-id="56c82-120">Windows Forms Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="56c82-120">Windows Forms Controls</span></span>](index.md)
- [<span data-ttu-id="56c82-121">Beschriften einzelner Steuerelemente für Windows Forms und Konfigurieren von Shortcuts für diese Elemente</span><span class="sxs-lookup"><span data-stu-id="56c82-121">Labeling Individual Windows Forms Controls and Providing Shortcuts to Them</span></span>](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [<span data-ttu-id="56c82-122">Steuerelemente für Windows Forms</span><span class="sxs-lookup"><span data-stu-id="56c82-122">Controls to Use on Windows Forms</span></span>](controls-to-use-on-windows-forms.md)
- [<span data-ttu-id="56c82-123">Windows Forms-Steuerelemente nach Funktion</span><span class="sxs-lookup"><span data-stu-id="56c82-123">Windows Forms Controls by Function</span></span>](windows-forms-controls-by-function.md)
- [<span data-ttu-id="56c82-124">Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem FlowLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="56c82-124">How to: Anchor and Dock Child Controls in a FlowLayoutPanel Control</span></span>](how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [<span data-ttu-id="56c82-125">Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem TableLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="56c82-125">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [<span data-ttu-id="56c82-126">Übersicht über die AutoSize-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="56c82-126">AutoSize Property Overview</span></span>](autosize-property-overview.md)
- [<span data-ttu-id="56c82-127">Gewusst wie: Verankern von Steuerelementen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="56c82-127">How to: Anchor Controls on Windows Forms</span></span>](how-to-anchor-controls-on-windows-forms.md)
