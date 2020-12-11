---
title: 'Gewusst wie: Ausrichten eines Steuerelements an den Rändern eines Formulars zur Entwurfszeit'
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], docking using designer
- Dock property [Windows Forms], aligning controls (using designer)
ms.assetid: 51f08998-5e3b-4330-be58-a4edd0eb60f4
ms.openlocfilehash: b08e01eb9adb984a32a8fc435cf1f3b93b159a14
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976368"
---
# <a name="how-to-align-a-control-to-the-edges-of-forms-at-design-time"></a><span data-ttu-id="3b7c6-102">Gewusst wie: Ausrichten eines Steuerelements an den Rändern eines Formulars zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="3b7c6-102">How to: Align a Control to the Edges of Forms at Design Time</span></span>

<span data-ttu-id="3b7c6-103">Sie können das Steuerelement am Rand Ihrer Formulare ausrichten, indem Sie den Wert der- <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-103">You can make your control align to the edge of your forms by setting the value of the <xref:System.Windows.Forms.Control.Dock%2A> property.</span></span> <span data-ttu-id="3b7c6-104">Diese Eigenschaft legt fest, wo auf dem Formular das Steuerelement sich befindet.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-104">This property designates where your control resides in the form.</span></span> <span data-ttu-id="3b7c6-105">Die <xref:System.Windows.Forms.Control.Dock%2A>-Eigenschaft kann auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="3b7c6-105">The <xref:System.Windows.Forms.Control.Dock%2A> property can be set to the following values:</span></span>

|<span data-ttu-id="3b7c6-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="3b7c6-106">Setting</span></span>|<span data-ttu-id="3b7c6-107">Auswirkung auf das Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3b7c6-107">Effect on your control</span></span>|
|-------------|----------------------------|
|<xref:System.Windows.Forms.DockStyle.Bottom>|<span data-ttu-id="3b7c6-108">Wird im unteren Bereich des Formulars angedockt.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-108">Docks to the bottom of the form.</span></span>|
|<xref:System.Windows.Forms.DockStyle.Fill>|<span data-ttu-id="3b7c6-109">Füllt den gesamten verbleibenden Platz im Formular aus.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-109">Fills all remaining space in the form.</span></span>|
|<xref:System.Windows.Forms.DockStyle.Left>|<span data-ttu-id="3b7c6-110">Wird an der linken Seite des Formulars angedockt.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-110">Docks to the left side of the form.</span></span>|
|<xref:System.Windows.Forms.DockStyle.None>|<span data-ttu-id="3b7c6-111">Wird nicht an einer beliebigen Stelle andocken und wird an dem Speicherort angezeigt, der durch angegeben ist <xref:System.Windows.Forms.Control.Location%2A> .</span><span class="sxs-lookup"><span data-stu-id="3b7c6-111">Does not dock anywhere, and it appears at the location specified by its <xref:System.Windows.Forms.Control.Location%2A>.</span></span>|
|<xref:System.Windows.Forms.DockStyle.Right>|<span data-ttu-id="3b7c6-112">Wird an der rechten Seite des Formulars angedockt.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-112">Docks to the right side of the form.</span></span>|
|<xref:System.Windows.Forms.DockStyle.Top>|<span data-ttu-id="3b7c6-113">Wird im oberen Bereich des Formulars angedockt.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-113">Docks to the top of the form.</span></span>|

<span data-ttu-id="3b7c6-114">Diese Werte können auch im Code festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-114">These values can also be set in code.</span></span> <span data-ttu-id="3b7c6-115">Weitere Informationen finden Sie unter Gewusst [wie: Ausrichten eines Steuer Elements an den Kanten von Formularen](how-to-align-a-control-to-the-edges-of-forms.md).</span><span class="sxs-lookup"><span data-stu-id="3b7c6-115">For more information, see [How to: Align a Control to the Edges of Forms](how-to-align-a-control-to-the-edges-of-forms.md).</span></span>

## <a name="set-the-dock-property-for-your-control-at-design-time"></a><span data-ttu-id="3b7c6-116">Festlegen der Dock-Eigenschaft für das Steuerelement zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="3b7c6-116">Set the Dock property for your control at design time</span></span>

1. <span data-ttu-id="3b7c6-117">Wählen Sie in der Windows Forms-Designer in Visual Studio das Steuerelement aus.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-117">In the Windows Forms Designer in Visual Studio, select your control.</span></span>

2. <span data-ttu-id="3b7c6-118">Klicken Sie im Fenster **Eigenschaften** auf das Dropdown Feld neben der- <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-118">In the **Properties** window, click the drop-down box next to the <xref:System.Windows.Forms.Control.Dock%2A> property.</span></span>

     <span data-ttu-id="3b7c6-119">Eine grafische Benutzeroberfläche, die die sechs möglichen Einstellungen darstellt, <xref:System.Windows.Forms.Control.Dock%2A> wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-119">A graphical interface representing the six possible <xref:System.Windows.Forms.Control.Dock%2A> settings is displayed.</span></span>

3. <span data-ttu-id="3b7c6-120">Wählen Sie die entsprechende Einstellung aus.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-120">Choose the appropriate setting.</span></span>

4. <span data-ttu-id="3b7c6-121">Das Steuerelement wird nun in der durch die-Einstellung angegebenen Weise andocken.</span><span class="sxs-lookup"><span data-stu-id="3b7c6-121">Your control will now dock in the manner specified by the setting.</span></span>

## <a name="see-also"></a><span data-ttu-id="3b7c6-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b7c6-122">See also</span></span>

- <xref:System.Windows.Forms.Control.Dock%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.Anchor%2A?displayProperty=nameWithType>
- [<span data-ttu-id="3b7c6-123">Vorgehensweise: Ausrichten eines Steuerelements an Formularrändern</span><span class="sxs-lookup"><span data-stu-id="3b7c6-123">How to: Align a Control to the Edges of Forms</span></span>](how-to-align-a-control-to-the-edges-of-forms.md)
- [<span data-ttu-id="3b7c6-124">Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von Ausrichtungslinien</span><span class="sxs-lookup"><span data-stu-id="3b7c6-124">Walkthrough: Arranging Controls on Windows Forms Using Snaplines</span></span>](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
- [<span data-ttu-id="3b7c6-125">Gewusst wie: Verankern von Steuerelementen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="3b7c6-125">How to: Anchor Controls on Windows Forms</span></span>](how-to-anchor-controls-on-windows-forms.md)
- [<span data-ttu-id="3b7c6-126">Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem TableLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3b7c6-126">How to: Anchor and Dock Child Controls in a TableLayoutPanel Control</span></span>](how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [<span data-ttu-id="3b7c6-127">Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem FlowLayoutPanel-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="3b7c6-127">How to: Anchor and Dock Child Controls in a FlowLayoutPanel Control</span></span>](how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [<span data-ttu-id="3b7c6-128">Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von TableLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="3b7c6-128">Walkthrough: Arranging Controls on Windows Forms Using a TableLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [<span data-ttu-id="3b7c6-129">Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von FlowLayoutPanel</span><span class="sxs-lookup"><span data-stu-id="3b7c6-129">Walkthrough: Arranging Controls on Windows Forms Using a FlowLayoutPanel</span></span>](walkthrough-arranging-controls-on-windows-forms-using-a-flowlayoutpanel.md)
- [<span data-ttu-id="3b7c6-130">Entwickeln von Windows Forms-Steuerelementen zur Entwurfszeit</span><span class="sxs-lookup"><span data-stu-id="3b7c6-130">Developing Windows Forms Controls at Design Time</span></span>](developing-windows-forms-controls-at-design-time.md)
