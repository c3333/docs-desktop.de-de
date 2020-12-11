---
title: Ausblenden von Spalten im DataGridView-Steuerelement mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, columns
- columns [Windows Forms], hiding
- DataGridView control [Windows Forms], column hiding
- data [Windows Forms], displaying
ms.assetid: a81c38e6-2527-426a-bcb1-be691403be04
ms.openlocfilehash: c5344e10a69d86b1733f5462f9c2df0f0e71b8d5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975981"
---
# <a name="how-to-hide-columns-in-the-windows-forms-datagridview-control-using-the-designer"></a><span data-ttu-id="73e8f-102">Vorgehensweise: Ausblenden von Spalten im DataGridView-Steuerelement in Windows Forms mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="73e8f-102">How to: Hide Columns in the Windows Forms DataGridView Control Using the Designer</span></span>
<span data-ttu-id="73e8f-103">Manchmal möchten Sie nur einige der Spalten anzeigen, die in einem <xref:System.Windows.Forms.DataGridView>-Steuerelement in Windows Forms verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="73e8f-103">Sometimes you will want to display only some of the columns that are available in a Windows Forms <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="73e8f-104">Beispielsweise können Sie Benutzern mit Verwaltungs Anmelde Informationen eine Employee-Gehalts Spalte anzeigen, während Sie Sie von anderen Benutzern ausblenden.</span><span class="sxs-lookup"><span data-stu-id="73e8f-104">For example, you may want to show an employee salary column to users with management credentials while hiding it from other users.</span></span> <span data-ttu-id="73e8f-105">Alternativ können Sie das Steuerelement an eine Datenquelle binden, die viele Spalten enthält, von denen Sie nur einige Spalten anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="73e8f-105">Alternately, you may want to bind the control to a data source that contains many columns, only some of which you want to display.</span></span> <span data-ttu-id="73e8f-106">In diesem Fall werden Sie in der Regel die Spalten entfernen, die Sie nicht anzeigen möchten, anstatt Sie zu verbergen.</span><span class="sxs-lookup"><span data-stu-id="73e8f-106">In this case, you will typically remove the columns you are not interested in displaying rather than hiding them.</span></span> <span data-ttu-id="73e8f-107">Weitere Informationen finden Sie unter Gewusst [wie: Hinzufügen und Entfernen von Spalten im Windows Forms DataGridView-Steuerelement mithilfe des Designers](add-and-remove-columns-in-the-datagrid-using-the-designer.md).</span><span class="sxs-lookup"><span data-stu-id="73e8f-107">For more information, see [How to: Add and Remove Columns in the Windows Forms DataGridView Control Using the Designer](add-and-remove-columns-in-the-datagrid-using-the-designer.md).</span></span>

 <span data-ttu-id="73e8f-108">Das folgende Verfahren erfordert ein **Windows-Anwendungs** Projekt mit einem Formular, das ein-Steuerelement enthält <xref:System.Windows.Forms.DataGridView> .</span><span class="sxs-lookup"><span data-stu-id="73e8f-108">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="73e8f-109">Weitere Informationen zum Einrichten eines solchen Projekts finden Sie unter Gewusst [wie: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project) und Gewusst [wie: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="73e8f-109">For information about setting up such a project, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>

## <a name="to-hide-a-column-using-the-designer"></a><span data-ttu-id="73e8f-110">So blenden Sie eine Spalte mithilfe des Designers aus</span><span class="sxs-lookup"><span data-stu-id="73e8f-110">To hide a column using the designer</span></span>

1. <span data-ttu-id="73e8f-111">Klicken Sie ![ in der oberen rechten Ecke des Steuer Elements auf das Symbol Designer Aktionen (kleiner schwarzer Pfeil ](./media/designer-actions-glyph.gif) ) <xref:System.Windows.Forms.DataGridView> , und wählen Sie dann **Spalten bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="73e8f-111">Click the designer actions glyph (![Small black arrow](./media/designer-actions-glyph.gif)) on the upper-right corner of the <xref:System.Windows.Forms.DataGridView> control, and then select **Edit Columns**.</span></span>

2. <span data-ttu-id="73e8f-112">Wählen Sie in der Liste **Ausgewählte Spalten** eine Spalte aus.</span><span class="sxs-lookup"><span data-stu-id="73e8f-112">Select a column from the **Selected Columns** list.</span></span>

3. <span data-ttu-id="73e8f-113">Legen Sie im Raster **Spalten Eigenschaften** die- <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A> Eigenschaft auf fest `false` .</span><span class="sxs-lookup"><span data-stu-id="73e8f-113">In the **Column Properties** grid, set the <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A> property to `false`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="73e8f-114">Sie können eine Spalte auch beim Hinzufügen ausblenden, indem Sie im Dialogfeld **Spalte hinzufügen** das Kontrollkästchen **sichtbar** deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="73e8f-114">You can also hide a column when adding it by clearing the **Visible** check box in the **Add Column** dialog box.</span></span>

## <a name="see-also"></a><span data-ttu-id="73e8f-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73e8f-115">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn.Visible%2A?displayProperty=nameWithType>
- [<span data-ttu-id="73e8f-116">Vorgehensweise: Hinzufügen und Entfernen von Spalten im DataGridView-Steuerelement in Windows Forms mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="73e8f-116">How to: Add and Remove Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](add-and-remove-columns-in-the-datagrid-using-the-designer.md)
- [<span data-ttu-id="73e8f-117">Vorgehensweise: Erstellen eines Windows Forms-Anwendungs Projekts</span><span class="sxs-lookup"><span data-stu-id="73e8f-117">How to: Create a Windows Forms application project</span></span>](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [<span data-ttu-id="73e8f-118">How to: Hinzufügen von Steuerelementen zu Windows Forms</span><span class="sxs-lookup"><span data-stu-id="73e8f-118">How to: Add Controls to Windows Forms</span></span>](how-to-add-controls-to-windows-forms.md)
