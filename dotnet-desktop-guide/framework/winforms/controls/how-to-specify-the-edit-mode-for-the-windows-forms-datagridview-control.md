---
title: Festlegen des Bearbeitungsmodus für das DataGridView-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- DataGridView control [Windows Forms], edit mode
- data grids [Windows Forms], edit mode
ms.assetid: 93e117e8-94c4-411b-ba31-645e475ed85c
ms.openlocfilehash: c0318202a80f9a43f1b656201732ef032f430b5b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976642"
---
# <a name="how-to-specify-the-edit-mode-for-the-windows-forms-datagridview-control"></a><span data-ttu-id="1488a-102">Vorgehensweise: Festlegen des Bearbeitungsmodus für das DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="1488a-102">How to: Specify the Edit Mode for the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="1488a-103">Standardmäßig können Benutzer den Inhalt der aktuellen <xref:System.Windows.Forms.DataGridView> Textfeld Zelle bearbeiten, indem Sie Sie eingeben oder F2 drücken.</span><span class="sxs-lookup"><span data-stu-id="1488a-103">By default, users can edit the contents of the current <xref:System.Windows.Forms.DataGridView> text box cell by typing in it or pressing F2.</span></span> <span data-ttu-id="1488a-104">Dadurch wird die Zelle in den Bearbeitungsmodus versetzt, wenn alle der folgenden Bedingungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="1488a-104">This puts the cell in edit mode if all of the following conditions are met:</span></span>  
  
- <span data-ttu-id="1488a-105">Die zugrunde liegende Datenquelle unterstützt die Bearbeitung.</span><span class="sxs-lookup"><span data-stu-id="1488a-105">The underlying data source supports editing.</span></span>  
  
- <span data-ttu-id="1488a-106">Das- <xref:System.Windows.Forms.DataGridView> Steuerelement ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1488a-106">The <xref:System.Windows.Forms.DataGridView> control is enabled.</span></span>  
  
- <span data-ttu-id="1488a-107">Der <xref:System.Windows.Forms.DataGridView.EditMode%2A>-Eigenschaftswert lautet nicht <xref:System.Windows.Forms.DataGridViewEditMode.EditProgrammatically>.</span><span class="sxs-lookup"><span data-stu-id="1488a-107">The <xref:System.Windows.Forms.DataGridView.EditMode%2A> property value is not <xref:System.Windows.Forms.DataGridViewEditMode.EditProgrammatically>.</span></span>  
  
- <span data-ttu-id="1488a-108">Die `ReadOnly` Eigenschaften von Zelle, Zeile, Spalte und Steuerelement sind auf festgelegt `false` .</span><span class="sxs-lookup"><span data-stu-id="1488a-108">The `ReadOnly` properties of the cell, row, column, and control are all set to `false`.</span></span>  
  
 <span data-ttu-id="1488a-109">Im Bearbeitungsmodus kann der Benutzer den Zellwert ändern und die EINGABETASTE drücken, um die Änderung zu übernehmen, oder ESC, um die Zelle auf den ursprünglichen Wert zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="1488a-109">In edit mode, the user can change the cell value and press ENTER to commit the change or ESC to revert the cell to its original value.</span></span>  
  
 <span data-ttu-id="1488a-110">Sie können ein <xref:System.Windows.Forms.DataGridView> Steuerelement so konfigurieren, dass eine Zelle in den Bearbeitungsmodus wechselt, sobald Sie zur aktuellen Zelle wird.</span><span class="sxs-lookup"><span data-stu-id="1488a-110">You can configure a <xref:System.Windows.Forms.DataGridView> control so that a cell enters edit mode as soon as it becomes the current cell.</span></span> <span data-ttu-id="1488a-111">Das Verhalten der Enter-Taste und der ESC-Taste ist in diesem Fall unverändert, aber die Zelle bleibt im Bearbeitungsmodus, nachdem ein Commit oder ein Commit für den Wert ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="1488a-111">The behavior of the ENTER and ESC keys is unchanged in this case, but the cell remains in edit mode after the value is committed or reverted.</span></span> <span data-ttu-id="1488a-112">Sie können das Steuerelement auch so konfigurieren, dass die Zellen in den Bearbeitungsmodus wechseln, wenn Benutzer in der Zelle eingeben oder nur dann, wenn Benutzer die Taste F2 drücken.</span><span class="sxs-lookup"><span data-stu-id="1488a-112">You can also configure the control so that cells enter edit mode only when users type in the cell or only when users press F2.</span></span> <span data-ttu-id="1488a-113">Schließlich können Sie verhindern, dass Zellen in den Bearbeitungsmodus wechseln, außer wenn Sie die- <xref:System.Windows.Forms.DataGridView.BeginEdit%2A> Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1488a-113">Finally, you can prevent cells from entering edit mode except when you call the <xref:System.Windows.Forms.DataGridView.BeginEdit%2A> method.</span></span>  
  
### <a name="to-change-the-edit-mode-of-a-datagridview-control"></a><span data-ttu-id="1488a-114">So ändern Sie den Bearbeitungsmodus eines DataGridView-Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="1488a-114">To change the edit mode of a DataGridView control</span></span>  
  
- <span data-ttu-id="1488a-115">Legen Sie die- <xref:System.Windows.Forms.DataGridView.EditMode%2A?displayProperty=nameWithType> Eigenschaft auf die entsprechende- <xref:System.Windows.Forms.DataGridViewEditMode> Enumeration fest.</span><span class="sxs-lookup"><span data-stu-id="1488a-115">Set the <xref:System.Windows.Forms.DataGridView.EditMode%2A?displayProperty=nameWithType> property to the appropriate <xref:System.Windows.Forms.DataGridViewEditMode> enumeration.</span></span>  
  
     [!code-csharp[System.Windows.Forms.DataGridViewMisc#067](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#067)]
     [!code-vb[System.Windows.Forms.DataGridViewMisc#067](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#067)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="1488a-116">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="1488a-116">Compiling the Code</span></span>  
 <span data-ttu-id="1488a-117">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1488a-117">This example requires:</span></span>  
  
- <span data-ttu-id="1488a-118">Ein <xref:System.Windows.Forms.DataGridView>-Steuerelement namens `dataGridView1`.</span><span class="sxs-lookup"><span data-stu-id="1488a-118">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
- <span data-ttu-id="1488a-119">Verweise auf die Assemblys <xref:System> und <xref:System.Windows.Forms>.</span><span class="sxs-lookup"><span data-stu-id="1488a-119">References to the <xref:System> and <xref:System.Windows.Forms> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1488a-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1488a-120">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.EditMode%2A?displayProperty=nameWithType>
- [<span data-ttu-id="1488a-121">Dateneingabe im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="1488a-121">Data Entry in the Windows Forms DataGridView Control</span></span>](data-entry-in-the-windows-forms-datagridview-control.md)
