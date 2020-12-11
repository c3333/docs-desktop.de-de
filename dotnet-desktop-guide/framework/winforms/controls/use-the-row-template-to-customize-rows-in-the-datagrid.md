---
title: Verwenden der Zeilen Vorlage zum Anpassen von Zeilen im DataGridView-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- data grids [Windows Forms], customizing rows
- DataGridView control [Windows Forms], customizing rows
ms.assetid: 6db61607-7e57-4a84-8d63-9d6a7ed7f9ff
ms.openlocfilehash: 35cb95f22c0caa654bf149b5fc4fd0395696a411
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976629"
---
# <a name="how-to-use-the-row-template-to-customize-rows-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="19f4e-102">Vorgehensweise: Verwenden der Zeilenvorlage zum Anpassen von Zeilen im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="19f4e-102">How to: Use the Row Template to Customize Rows in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="19f4e-103">Das- <xref:System.Windows.Forms.DataGridView> Steuerelement verwendet die Zeilen Vorlage als Grundlage für alle Zeilen, die dem Steuerelement entweder über die Datenbindung hinzugefügt werden, oder wenn die-Methode aufgerufen wird, <xref:System.Windows.Forms.DataGridViewRowCollection.Add%2A?displayProperty=nameWithType> ohne eine vorhandene zu verwendende Zeile anzugeben.</span><span class="sxs-lookup"><span data-stu-id="19f4e-103">The <xref:System.Windows.Forms.DataGridView> control uses the row template as a basis for all rows that it adds to the control either through data binding or when you call the <xref:System.Windows.Forms.DataGridViewRowCollection.Add%2A?displayProperty=nameWithType> method without specifying an existing row to use.</span></span>  
  
 <span data-ttu-id="19f4e-104">Mit der Zeilen Vorlage können Sie die Darstellung und das Verhalten von Zeilen besser steuern, als die- <xref:System.Windows.Forms.DataGridView.RowsDefaultCellStyle%2A> Eigenschaft bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="19f4e-104">The row template gives you greater control over the appearance and behavior of rows than the <xref:System.Windows.Forms.DataGridView.RowsDefaultCellStyle%2A> property provides.</span></span> <span data-ttu-id="19f4e-105">Mit der Zeilen Vorlage können Sie alle Eigenschaften festlegen <xref:System.Windows.Forms.DataGridViewRow> , einschließlich <xref:System.Windows.Forms.DataGridViewRow.DefaultCellStyle%2A> .</span><span class="sxs-lookup"><span data-stu-id="19f4e-105">With the row template, you can set any <xref:System.Windows.Forms.DataGridViewRow> properties, including <xref:System.Windows.Forms.DataGridViewRow.DefaultCellStyle%2A>.</span></span>  
  
 <span data-ttu-id="19f4e-106">Es gibt einige Situationen, in denen Sie die Zeilen Vorlage verwenden müssen, um einen bestimmten Effekt zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="19f4e-106">There are some situations where you must use the row template to achieve a particular effect.</span></span> <span data-ttu-id="19f4e-107">Beispielsweise können Informationen zur Zeilenhöhe nicht in einem gespeichert werden <xref:System.Windows.Forms.DataGridViewCellStyle> . Daher müssen Sie eine Zeilen Vorlage verwenden, um die von allen Zeilen verwendete Standardhöhe zu ändern.</span><span class="sxs-lookup"><span data-stu-id="19f4e-107">For example, row height information cannot be stored in a <xref:System.Windows.Forms.DataGridViewCellStyle>, so you must use a row template to change the default height used by all rows.</span></span> <span data-ttu-id="19f4e-108">Die Zeilen Vorlage ist auch nützlich, wenn Sie Ihre eigenen Klassen erstellen, die von abgeleitet <xref:System.Windows.Forms.DataGridViewRow> sind, und Sie möchten, dass der benutzerdefinierte Typ verwendet wird, wenn dem Steuerelement neue Zeilen hinzugefügt werden</span><span class="sxs-lookup"><span data-stu-id="19f4e-108">The row template is also useful when you create your own classes derived from <xref:System.Windows.Forms.DataGridViewRow> and you want your custom type used when new rows are added to the control.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="19f4e-109">Die Zeilen Vorlage wird nur verwendet, wenn Zeilen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="19f4e-109">The row template is used only when rows are added.</span></span> <span data-ttu-id="19f4e-110">Vorhandene Zeilen können nicht durch Ändern der Zeilen Vorlage geändert werden.</span><span class="sxs-lookup"><span data-stu-id="19f4e-110">You cannot change existing rows by changing the row template.</span></span>  
  
### <a name="to-use-the-row-template"></a><span data-ttu-id="19f4e-111">So verwenden Sie die Zeilen Vorlage</span><span class="sxs-lookup"><span data-stu-id="19f4e-111">To use the row template</span></span>  
  
- <span data-ttu-id="19f4e-112">Legen Sie Eigenschaften für das von der-Eigenschaft abgerufene Objekt fest <xref:System.Windows.Forms.DataGridView.RowTemplate%2A?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="19f4e-112">Set properties on the object retrieved from the <xref:System.Windows.Forms.DataGridView.RowTemplate%2A?displayProperty=nameWithType> property.</span></span>  
  
     [!code-cpp[System.Windows.Forms.DataGridView.RowTemplate#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.RowTemplate/CPP/datagridviewrowtemplate.cpp#1)]
     [!code-csharp[System.Windows.Forms.DataGridView.RowTemplate#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.RowTemplate/CS/datagridviewrowtemplate.cs#1)]
     [!code-vb[System.Windows.Forms.DataGridView.RowTemplate#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.RowTemplate/VB/datagridviewrowtemplate.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="19f4e-113">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="19f4e-113">Compiling the Code</span></span>  
 <span data-ttu-id="19f4e-114">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="19f4e-114">This example requires:</span></span>  
  
- <span data-ttu-id="19f4e-115">Ein <xref:System.Windows.Forms.DataGridView>-Steuerelement namens `dataGridView1`.</span><span class="sxs-lookup"><span data-stu-id="19f4e-115">A <xref:System.Windows.Forms.DataGridView> control named `dataGridView1`.</span></span>  
  
- <span data-ttu-id="19f4e-116">Verweise auf die Assemblys <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType> und <xref:System.Windows.Forms?displayProperty=nameWithType>.</span><span class="sxs-lookup"><span data-stu-id="19f4e-116">References to the <xref:System?displayProperty=nameWithType>, <xref:System.Drawing?displayProperty=nameWithType>, and <xref:System.Windows.Forms?displayProperty=nameWithType> assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="19f4e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19f4e-117">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewCellStyle>
- <xref:System.Windows.Forms.DataGridViewRow>
- <xref:System.Windows.Forms.DataGridView.RowTemplate%2A?displayProperty=nameWithType>
- [<span data-ttu-id="19f4e-118">Grundlegende Formatierungen und Formate im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="19f4e-118">Basic Formatting and Styling in the Windows Forms DataGridView Control</span></span>](basic-formatting-and-styling-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="19f4e-119">Zellstile im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="19f4e-119">Cell Styles in the Windows Forms DataGridView Control</span></span>](cell-styles-in-the-windows-forms-datagridview-control.md)
