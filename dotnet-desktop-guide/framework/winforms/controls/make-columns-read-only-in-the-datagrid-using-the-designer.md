---
title: Erstellen von Spalten Read-Only im DataGridView-Steuerelement mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, columns
- DataGridView control [Windows Forms], read-only columns
- data [Windows Forms], displaying
- columns [Windows Forms], read-only
ms.assetid: b4ef7a75-ab33-4ee3-b2cf-201530e454e9
ms.openlocfilehash: 2dd3f8bfcad39ca3d530c79a6e6a8170585f7adf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975548"
---
# <a name="how-to-make-columns-read-only-in-the-windows-forms-datagridview-control-using-the-designer"></a><span data-ttu-id="ca242-102">Vorgehensweise: Festlegen von schreibgeschützten Spalten im DataGridView-Steuerelement in Windows Forms mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="ca242-102">How to: Make Columns Read-Only in the Windows Forms DataGridView Control Using the Designer</span></span>
<span data-ttu-id="ca242-103">Standardmäßig können Benutzer im Windows Forms Steuerelement angezeigte Text-und numerische Daten ändern <xref:System.Windows.Forms.DataGridView> .</span><span class="sxs-lookup"><span data-stu-id="ca242-103">By default, users can modify text and numerical data displayed in the Windows Forms <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="ca242-104">Wenn Sie Daten anzeigen möchten, die nicht für Änderungen vorgesehen sind, müssen Sie die Spalten, die die Daten enthalten, als schreibgeschützt festlegen.</span><span class="sxs-lookup"><span data-stu-id="ca242-104">If you want to display data that is not meant for modification, you must make the columns that contain the data read-only.</span></span> <span data-ttu-id="ca242-105">Informationen dazu, wie das Steuerelement vollständig schreibgeschützt wird, finden Sie unter Gewusst [wie: verhindern des Hinzufügens und Löschens von Zeilen im Windows Forms DataGridView-Steuerelement mithilfe des Designers](prevent-row-addition-and-deletion-in-the-datagrid-using-the-designer.md).</span><span class="sxs-lookup"><span data-stu-id="ca242-105">For information about how to make the control entirely read-only, see [How to: Prevent Row Addition and Deletion in the Windows Forms DataGridView Control Using the Designer](prevent-row-addition-and-deletion-in-the-datagrid-using-the-designer.md).</span></span>

 <span data-ttu-id="ca242-106">Das folgende Verfahren erfordert ein **Windows-Anwendungs** Projekt mit einem Formular, das ein-Steuerelement enthält <xref:System.Windows.Forms.DataGridView> .</span><span class="sxs-lookup"><span data-stu-id="ca242-106">The following procedure requires a **Windows Application** project with a form containing a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="ca242-107">Weitere Informationen zum Einrichten eines solchen Projekts finden Sie unter Gewusst [wie: Erstellen eines Windows Forms-Anwendungs Projekts](/visualstudio/ide/step-1-create-a-windows-forms-application-project) und Gewusst [wie: Hinzufügen von Steuerelementen zu Windows Forms](how-to-add-controls-to-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="ca242-107">For information about setting up such a project, see [How to: Create a Windows Forms application project](/visualstudio/ide/step-1-create-a-windows-forms-application-project) and [How to: Add Controls to Windows Forms](how-to-add-controls-to-windows-forms.md).</span></span>

## <a name="to-make-a-column-read-only-by-using-the-designer"></a><span data-ttu-id="ca242-108">So machen Sie eine Spalte mithilfe des Designers als schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="ca242-108">To make a column read-only by using the designer</span></span>

1. <span data-ttu-id="ca242-109">Klicken Sie ![ in der oberen rechten Ecke des Steuer Elements auf das Symbol Designer Aktionen (kleiner schwarzer Pfeil ](./media/designer-actions-glyph.gif) ) <xref:System.Windows.Forms.DataGridView> , und wählen Sie dann **Spalten bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="ca242-109">Click the designer actions glyph (![Small black arrow](./media/designer-actions-glyph.gif)) on the upper-right corner of the <xref:System.Windows.Forms.DataGridView> control, and then select **Edit Columns**.</span></span>

2. <span data-ttu-id="ca242-110">Wählen Sie in der Liste **Ausgewählte Spalten** eine Spalte aus.</span><span class="sxs-lookup"><span data-stu-id="ca242-110">Select a column from the **Selected Columns** list.</span></span>

3. <span data-ttu-id="ca242-111">Legen Sie im Raster **Spalten Eigenschaften** die- <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A> Eigenschaft auf fest `true` .</span><span class="sxs-lookup"><span data-stu-id="ca242-111">In the **Column Properties** grid, set the <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A> property to `true`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ca242-112">Sie können eine Spalte auch als schreibgeschützt festlegen, wenn Sie Sie hinzufügen, **indem Sie im** Dialogfeld **Spalte hinzufügen** das Kontrollkästchen Schreibgeschützt aktivieren.</span><span class="sxs-lookup"><span data-stu-id="ca242-112">You can also make a column read-only when you add it by selecting the **Read Only** check box in the **Add Column** dialog box.</span></span>

## <a name="see-also"></a><span data-ttu-id="ca242-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca242-113">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn.ReadOnly%2A?displayProperty=nameWithType>
- [<span data-ttu-id="ca242-114">Vorgehensweise: Hinzufügen und Entfernen von Spalten im DataGridView-Steuerelement in Windows Forms mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="ca242-114">How to: Add and Remove Columns in the Windows Forms DataGridView Control Using the Designer</span></span>](add-and-remove-columns-in-the-datagrid-using-the-designer.md)
- [<span data-ttu-id="ca242-115">Vorgehensweise: Verhindern des Hinzufügens und Löschens von Zeilen im DataGridView-Steuerelement in Windows Forms mithilfe des Designers</span><span class="sxs-lookup"><span data-stu-id="ca242-115">How to: Prevent Row Addition and Deletion in the Windows Forms DataGridView Control Using the Designer</span></span>](prevent-row-addition-and-deletion-in-the-datagrid-using-the-designer.md)
- [<span data-ttu-id="ca242-116">Vorgehensweise: Erstellen eines Windows Forms-Anwendungs Projekts</span><span class="sxs-lookup"><span data-stu-id="ca242-116">How to: Create a Windows Forms application project</span></span>](/visualstudio/ide/step-1-create-a-windows-forms-application-project)
- [<span data-ttu-id="ca242-117">How to: Hinzufügen von Steuerelementen zu Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ca242-117">How to: Add Controls to Windows Forms</span></span>](how-to-add-controls-to-windows-forms.md)
