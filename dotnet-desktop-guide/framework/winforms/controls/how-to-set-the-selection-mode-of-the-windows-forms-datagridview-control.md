---
title: Festlegen des Auswahlmodus des DataGridView-Steuer Elements
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- selection [Windows Forms], modes in DataGridView control
- DataGridView control [Windows Forms], selection mode
- data grids [Windows Forms], selection mode
ms.assetid: 2f241643-7f82-4583-8757-03494f63b465
ms.openlocfilehash: da866aac3ac5b08a06ec71744aadb4260bd0cfc4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976762"
---
# <a name="how-to-set-the-selection-mode-of-the-windows-forms-datagridview-control"></a><span data-ttu-id="039fd-102">Vorgehensweise: Festlegen des Auswahlmodus des DataGridView-Steuerelements in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="039fd-102">How to: Set the Selection Mode of the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="039fd-103">Im folgenden Codebeispiel wird veranschaulicht, wie ein-Steuerelement so konfiguriert wird, dass durch Klicken auf eine beliebige Stelle <xref:System.Windows.Forms.DataGridView> in einer Zeile automatisch die gesamte Zeile ausgewählt wird, sodass jeweils nur eine Zeile ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="039fd-103">The following code example demonstrates how to configure a <xref:System.Windows.Forms.DataGridView> control so that clicking anywhere within a row automatically selects the entire row, and so that only one row at a time can be selected.</span></span>  
  
## <a name="example"></a><span data-ttu-id="039fd-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="039fd-104">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewMisc#065](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/CS/datagridviewmisc.cs#065)]
 [!code-vb[System.Windows.Forms.DataGridViewMisc#065](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewMisc/VB/datagridviewmisc.vb#065)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="039fd-105">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="039fd-105">Compiling the Code</span></span>  
 <span data-ttu-id="039fd-106">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="039fd-106">This example requires:</span></span>  
  
- <span data-ttu-id="039fd-107">Ein <xref:System.Windows.Forms.DataGridView>-Steuerelement namens `dataGridView1`.</span><span class="sxs-lookup"><span data-stu-id="039fd-107">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
- <span data-ttu-id="039fd-108">Verweise auf die Assemblys <xref:System?displayProperty=nameWithType> und <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="039fd-108">References to the <xref:System?displayProperty=nameWithType> and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="039fd-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="039fd-109">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridView.MultiSelect%2A>
- <xref:System.Windows.Forms.DataGridView.SelectionMode%2A>
- <xref:System.Windows.Forms.DataGridViewSelectionMode>
- [<span data-ttu-id="039fd-110">Verwendung von Auswahl und Zwischenablage mit dem DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="039fd-110">Selection and Clipboard Use with the Windows Forms DataGridView Control</span></span>](selection-and-clipboard-use-with-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="039fd-111">Auswahlmodi im DataGridView-Steuerelement von Windows Forms</span><span class="sxs-lookup"><span data-stu-id="039fd-111">Selection Modes in the Windows Forms DataGridView Control</span></span>](selection-modes-in-the-windows-forms-datagridview-control.md)
