---
title: Ändern der Reihenfolge von Spalten im DataGridView-Steuerelement mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- columns [Windows Forms], order of
- DataGridView control [Windows Forms], column order
- Windows Forms, columns
- data [Windows Forms], displaying
ms.assetid: 7fe52a98-75d6-448c-97a5-65ca2c568c1a
ms.openlocfilehash: 7540203fb1c0465caeb045275734d1a7c6f25ee8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975108"
---
# <a name="how-to-change-the-order-of-columns-in-the-windows-forms-datagridview-control-using-the-designer"></a><span data-ttu-id="99d2d-102">Vorgehensweise: Ändern der Reihenfolge von Spalten des DataGridView-Steuerelements in Windows Forms mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="99d2d-102">How to: Change the Order of Columns in the Windows Forms DataGridView Control Using the Designer</span></span>

<span data-ttu-id="99d2d-103">Wenn Sie ein Windows Forms- <xref:System.Windows.Forms.DataGridView> Steuerelement an eine Datenquelle binden, wird die Anzeigereihenfolge der automatisch generierten Spalten von der Datenquelle vorgegeben.</span><span class="sxs-lookup"><span data-stu-id="99d2d-103">When you bind a Windows Forms <xref:System.Windows.Forms.DataGridView> control to a data source, the display order of the automatically generated columns is dictated by the data source.</span></span> <span data-ttu-id="99d2d-104">Wenn Sie diese Reihenfolge nicht bevorzugen, können Sie die Reihenfolge der Spalten mithilfe des Designers ändern.</span><span class="sxs-lookup"><span data-stu-id="99d2d-104">If this order is not what you prefer, you can change the order of the columns using the designer.</span></span> <span data-ttu-id="99d2d-105">Möglicherweise möchten Sie auch ungebundene Spalten zum Steuerelement hinzufügen und die Anzeigereihenfolge ändern.</span><span class="sxs-lookup"><span data-stu-id="99d2d-105">You may also want to add unbound columns to the control and change their display order.</span></span> <span data-ttu-id="99d2d-106">Informationen zum programmgesteuerten Ändern der Spaltenreihenfolge finden Sie unter Gewusst [wie: Ändern der Reihenfolge von Spalten im Windows Forms DataGridView-Steuer](how-to-change-the-order-of-columns-in-the-windows-forms-datagridview-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="99d2d-106">For information about how to change the column order programmatically, see [How to: Change the Order of Columns in the Windows Forms DataGridView Control](how-to-change-the-order-of-columns-in-the-windows-forms-datagridview-control.md).</span></span>

<span data-ttu-id="99d2d-107">Das folgende Verfahren erfordert ein **Windows-Anwendungs** Projekt mit einem Formular, das ein-Steuerelement enthält <xref:System.Windows.Forms.DataGridView> .</span><span class="sxs-lookup"><span data-stu-id="99d2d-107">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="99d2d-108">Weitere Informationen zum Einrichten eines solchen Projekts finden Sie unter Gewusst [wie: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project) und Gewusst [wie: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="99d2d-108">For information about setting up such a project, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>

## <a name="to-change-the-column-order-using-the-designer"></a><span data-ttu-id="99d2d-109">So ändern Sie die Spaltenreihenfolge mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="99d2d-109">To change the column order using the designer</span></span>

1. <span data-ttu-id="99d2d-110">Klicken Sie ![ in der oberen rechten Ecke des Steuer Elements auf das Symbol Designer Aktionen (kleiner schwarzer Pfeil ](./media/designer-actions-glyph.gif) ) <xref:System.Windows.Forms.DataGridView> , und wählen Sie dann **Spalten bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="99d2d-110">Click the designer actions glyph (![Small black arrow](./media/designer-actions-glyph.gif)) on the upper-right corner of the <xref:System.Windows.Forms.DataGridView> control, and then select **Edit Columns**.</span></span>

2. <span data-ttu-id="99d2d-111">Wählen Sie in der Liste **Ausgewählte Spalten** eine Spalte aus.</span><span class="sxs-lookup"><span data-stu-id="99d2d-111">Select a column from the **Selected Columns** list.</span></span>

3. <span data-ttu-id="99d2d-112">Klicken Sie auf den nach-oben-oder nach-unten-Pfeil rechts neben der Liste **Ausgewählte Spalten** , bis sich die ausgewählte Spalte an der gewünschten Position befindet.</span><span class="sxs-lookup"><span data-stu-id="99d2d-112">Click the up or down arrow to the right of the **Selected Columns** list until the selected column is in the position you want.</span></span>

## <a name="see-also"></a><span data-ttu-id="99d2d-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99d2d-113">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- [<span data-ttu-id="99d2d-114">Vorgehensweise: Hinzufügen und Entfernen von Spalten im DataGridView-Steuerelement in Windows Forms mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="99d2d-114">How to: Add and Remove Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](add-and-remove-columns-in-the-datagrid-using-the-designer.md)
- [<span data-ttu-id="99d2d-115">Vorgehensweise: Erstellen eines Windows Forms-Anwendungs Projekts</span><span class="sxs-lookup"><span data-stu-id="99d2d-115">How to: Create a Windows Forms application project</span></span>](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [<span data-ttu-id="99d2d-116">How to: Hinzufügen von Steuerelementen zu Windows Forms</span><span class="sxs-lookup"><span data-stu-id="99d2d-116">How to: Add Controls to Windows Forms</span></span>](how-to-add-controls-to-windows-forms.md)
