---
title: Fixieren von Spalten im DataGridView-Steuerelement mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, columns
- columns [Windows Forms], freezing
- DataGridView control [Windows Forms], column freezing
- data [Windows Forms], displaying
ms.assetid: 87412dd2-478f-4751-af87-dafc591fc215
ms.openlocfilehash: 554d5eaa55401bdafc455c2dfb20d7c5d214a9be
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975767"
---
# <a name="how-to-freeze-columns-in-the-windows-forms-datagridview-control-using-the-designer"></a><span data-ttu-id="c990f-102">Vorgehensweise: Fixieren von Spalten im DataGridView-Steuerelement in Windows Forms mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="c990f-102">How to: Freeze Columns in the Windows Forms DataGridView Control Using the Designer</span></span>

<span data-ttu-id="c990f-103">Wenn Benutzer Daten anzeigen, die in einem <xref:System.Windows.Forms.DataGridView>-Steuerelement in Windows Forms angezeigt werden, müssen sie mitunter häufig auf eine bestimmte Spalte oder Gruppe von Spalten zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c990f-103">When users view data displayed in a Windows Forms <xref:System.Windows.Forms.DataGridView> control, they sometimes need to refer to a single column or set of columns frequently.</span></span> <span data-ttu-id="c990f-104">Wenn Sie z. b. eine Tabelle mit Kundeninformationen anzeigen, die viele Spalten enthält, ist es hilfreich, den Kundennamen jederzeit anzuzeigen, während andere Spalten einen Bildlauf außerhalb des sichtbaren Bereichs ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="c990f-104">For example, when you display a table of customer information that contains many columns, it is useful for you to display the customer name at all times while enabling other columns to scroll outside the visible region.</span></span>

 <span data-ttu-id="c990f-105">Zu diesem Zweck können Sie Spalten im Steuerelement fixieren.</span><span class="sxs-lookup"><span data-stu-id="c990f-105">To achieve this behavior, you can freeze columns in the control.</span></span> <span data-ttu-id="c990f-106">Wenn Sie eine Spalte fixieren, werden automatisch auch alle Spalten links daneben (bzw. rechts daneben in von rechts nach links geschriebenen Sprachen) fixiert.</span><span class="sxs-lookup"><span data-stu-id="c990f-106">When you freeze a column, all the columns to its left (or to its right in right-to-left language scripts) are frozen as well.</span></span> <span data-ttu-id="c990f-107">Fixierte Spalten behalten ihre Position bei, während alle anderen Spalten bei einem Bildlauf mitwandern.</span><span class="sxs-lookup"><span data-stu-id="c990f-107">Frozen columns remain in place while all other columns can scroll.</span></span> <span data-ttu-id="c990f-108">Wenn die Neuanordnung von Spalten aktiviert ist, werden die fixierten Spalten als eine Gruppe im Unterschied zu den nicht fixierten Spalten behandelt.</span><span class="sxs-lookup"><span data-stu-id="c990f-108">If column reordering is enabled, the frozen columns are treated as a group distinct from the unfrozen columns.</span></span> <span data-ttu-id="c990f-109">Benutzer können Spalten in beiden Gruppen neu positionieren, jedoch keine Spalte aus einer Gruppe in die andere verschieben.</span><span class="sxs-lookup"><span data-stu-id="c990f-109">Users can reposition columns in either group, but they cannot move a column from one group to the other.</span></span>

 <span data-ttu-id="c990f-110">Das folgende Verfahren erfordert ein **Windows-Anwendungs** Projekt mit einem Formular, das ein-Steuerelement enthält <xref:System.Windows.Forms.DataGridView> .</span><span class="sxs-lookup"><span data-stu-id="c990f-110">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="c990f-111">Weitere Informationen zum Einrichten eines solchen Projekts finden Sie unter Gewusst [wie: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project) und Gewusst [wie: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="c990f-111">For information about setting up such a project, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>

## <a name="to-freeze-a-column-using-the-designer"></a><span data-ttu-id="c990f-112">So fixieren Sie eine Spalte mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="c990f-112">To freeze a column using the designer</span></span>

1. <span data-ttu-id="c990f-113">Klicken Sie ![ in der oberen rechten Ecke des Steuer Elements auf das Symbol Designer Aktionen (kleiner schwarzer Pfeil ](./media/designer-actions-glyph.gif) ) <xref:System.Windows.Forms.DataGridView> , und wählen Sie dann **Spalten bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="c990f-113">Click the designer actions glyph (![Small black arrow](./media/designer-actions-glyph.gif)) on the upper-right corner of the <xref:System.Windows.Forms.DataGridView> control, and then select **Edit Columns**.</span></span>

2. <span data-ttu-id="c990f-114">Wählen Sie in der Liste **Ausgewählte Spalten** eine Spalte aus.</span><span class="sxs-lookup"><span data-stu-id="c990f-114">Select a column from the **Selected Columns** list.</span></span>

3. <span data-ttu-id="c990f-115">Legen Sie im Raster **Spalten Eigenschaften** die- <xref:System.Windows.Forms.DataGridViewColumn.Frozen%2A> Eigenschaft auf fest `true` .</span><span class="sxs-lookup"><span data-stu-id="c990f-115">In the **Column Properties** grid, set the <xref:System.Windows.Forms.DataGridViewColumn.Frozen%2A> property to `true`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c990f-116">Sie können eine Spalte auch beim Hinzufügen fixieren, indem Sie **im Dialog** Feld **Spalte hinzufügen** das Feld fixiert auswählen.</span><span class="sxs-lookup"><span data-stu-id="c990f-116">You can also freeze a column when adding it by selecting the **Frozen** box in the **Add Column** dialog box.</span></span>

## <a name="see-also"></a><span data-ttu-id="c990f-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c990f-117">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn.Frozen%2A?displayProperty=nameWithType>
- [<span data-ttu-id="c990f-118">Vorgehensweise: Hinzufügen und Entfernen von Spalten im DataGridView-Steuerelement in Windows Forms mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="c990f-118">How to: Add and Remove Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](add-and-remove-columns-in-the-datagrid-using-the-designer.md)
- [<span data-ttu-id="c990f-119">Vorgehensweise: Aktivieren der Neuanordnung von Spalten im DataGridView-Steuerelement in Windows Forms mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="c990f-119">How to: Enable Column Reordering in the Windows Forms DataGridView Control Using the Designer</span></span>](enable-column-reordering-in-the-datagrid-using-the-designer.md)
- <span data-ttu-id="c990f-120">[Gewusst wie: Anzeigen von Text mit der Schreibrichtung von rechts nach links in Windows Forms für die Globalisierung](/previous-versions/visualstudio/visual-studio-2010/7d3337xw(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="c990f-120">[How to: Display Right-to-Left Text in Windows Forms for Globalization](/previous-versions/visualstudio/visual-studio-2010/7d3337xw(v=vs.100))</span></span>
- [<span data-ttu-id="c990f-121">Vorgehensweise: Erstellen eines Windows Forms-Anwendungs Projekts</span><span class="sxs-lookup"><span data-stu-id="c990f-121">How to: Create a Windows Forms application project</span></span>](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [<span data-ttu-id="c990f-122">How to: Hinzufügen von Steuerelementen zu Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c990f-122">How to: Add Controls to Windows Forms</span></span>](how-to-add-controls-to-windows-forms.md)
