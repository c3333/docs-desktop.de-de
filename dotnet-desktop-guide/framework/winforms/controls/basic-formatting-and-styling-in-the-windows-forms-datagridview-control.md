---
title: Grundlegende Formatierung und Formatierung im DataGridView-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], formatting and styling
- data grids [Windows Forms], formatting
ms.assetid: b9b90836-1f56-4aa9-8db8-edc78fe830e8
ms.openlocfilehash: d295718b7bd4f3bc4c5f63b6e6cb911f733525fe
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975144"
---
# <a name="basic-formatting-and-styling-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="cb824-102">Grundlegende Formatierungen und Formate im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cb824-102">Basic Formatting and Styling in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="cb824-103">Das `DataGridView` -Steuerelement erleichtert das Definieren der grundlegenden Darstellung von Zellen und die Anzeige Formatierung von Zellwerten.</span><span class="sxs-lookup"><span data-stu-id="cb824-103">The `DataGridView` control makes it easy to define the basic appearance of cells and the display formatting of cell values.</span></span> <span data-ttu-id="cb824-104">Sie können Darstellung und Formatierungs Stile für einzelne Zellen, für Zellen in bestimmten Spalten und Zeilen oder für alle Zellen im Steuerelement definieren, indem Sie die Eigenschaften der Objekte festlegen, auf die `DataGridViewCellStyle` über verschiedene Steuerelement Eigenschaften zugegriffen wird `DataGridView` .</span><span class="sxs-lookup"><span data-stu-id="cb824-104">You can define appearance and formatting styles for individual cells, for cells in specific columns and rows, or for all cells in the control by setting the properties of the `DataGridViewCellStyle` objects accessed through various `DataGridView` control properties.</span></span> <span data-ttu-id="cb824-105">Außerdem können Sie diese Stile dynamisch auf Grundlage von Faktoren wie dem Zellwert ändern, indem Sie das- `CellFormatting` Ereignis behandeln.</span><span class="sxs-lookup"><span data-stu-id="cb824-105">Additionally, you can modify these styles dynamically based on factors such as the cell value by handling the `CellFormatting` event.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="cb824-106">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cb824-106">In This Section</span></span>  
 [<span data-ttu-id="cb824-107">Vorgehensweise: Ändern des Rahmen- und Rasterlinienstils im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cb824-107">How to: Change the Border and Gridline Styles in the Windows Forms DataGridView Control</span></span>](change-the-border-and-gridline-styles-in-the-datagrid.md)  
 <span data-ttu-id="cb824-108">Beschreibt, wie Eigenschaften festgelegt werden `DataGridView` , die die Darstellung des Steuerelement Rahmens und der Begrenzungs Linien zwischen Zellen definieren.</span><span class="sxs-lookup"><span data-stu-id="cb824-108">Describes how to set `DataGridView` properties that define the appearance of the control border and the boundary lines between cells.</span></span>  
  
 [<span data-ttu-id="cb824-109">Zellstile im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cb824-109">Cell Styles in the Windows Forms DataGridView Control</span></span>](cell-styles-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="cb824-110">Beschreibt die `DataGridViewCellStyle` -Klasse und wie Eigenschaften dieses Typs interagieren, um zu definieren, wie Zellen im-Steuerelement angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cb824-110">Describes the `DataGridViewCellStyle` class and how properties of that type interact to define how cells are displayed in the control.</span></span>  
  
 [<span data-ttu-id="cb824-111">Vorgehensweise: Festlegen von Standardzellenformaten für das DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cb824-111">How to: Set Default Cell Styles for the Windows Forms DataGridView Control</span></span>](how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="cb824-112">Beschreibt, wie Eigenschaften verwendet werden `DataGridViewCellStyle` , um die Standarddarstellung von Zellen in bestimmten Zeilen und Spalten und im gesamten Steuerelement zu definieren.</span><span class="sxs-lookup"><span data-stu-id="cb824-112">Describes how to use `DataGridViewCellStyle` properties to define the default appearance of cells in specific rows and columns and in the entire control.</span></span>  
  
 [<span data-ttu-id="cb824-113">Vorgehensweise: Formatieren von Daten im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cb824-113">How to: Format Data in the Windows Forms DataGridView Control</span></span>](how-to-format-data-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="cb824-114">Beschreibt, wie Zellen Anzeigewerte mithilfe von Eigenschaften formatiert werden `DataGridViewCellStyle` .</span><span class="sxs-lookup"><span data-stu-id="cb824-114">Describes how to format cell display values using `DataGridViewCellStyle` properties.</span></span>  
  
 [<span data-ttu-id="cb824-115">Gewusst wie: Festlegen von Schriftart- und Farbstilen im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cb824-115">How to: Set Font and Color Styles in the Windows Forms DataGridView Control</span></span>](how-to-set-font-and-color-styles-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="cb824-116">Beschreibt, wie die- `DefaultCellStyle` Eigenschaft verwendet wird, um grundlegende Anzeigeeigenschaften für alle Zellen im-Steuerelement festzulegen.</span><span class="sxs-lookup"><span data-stu-id="cb824-116">Describes how to use the `DefaultCellStyle` property to set basic display characteristics for all cells in the control.</span></span>  
  
 [<span data-ttu-id="cb824-117">Vorgehensweise: Festlegen von abwechselnden Zeilenstilen für das DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cb824-117">How to: Set Alternating Row Styles for the Windows Forms DataGridView Control</span></span>](how-to-set-alternating-row-styles-for-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="cb824-118">Beschreibt, wie ein Ledger-ähnlicher Effekt im-Steuerelement mit abwechselnden Zeilen erstellt wird, die anders angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cb824-118">Describes how to create a ledger-like effect in the control using alternating rows that are displayed differently.</span></span>  
  
 [<span data-ttu-id="cb824-119">Vorgehensweise: Verwenden der Zeilenvorlage zum Anpassen von Zeilen im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cb824-119">How to: Use the Row Template to Customize Rows in the Windows Forms DataGridView Control</span></span>](use-the-row-template-to-customize-rows-in-the-datagrid.md)  
 <span data-ttu-id="cb824-120">Beschreibt, wie die- `RowTemplate` Eigenschaft verwendet wird, um Zeilen Eigenschaften festzulegen, die für alle Zeilen im-Steuerelement verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb824-120">Describes how to use the `RowTemplate` property to set row properties that will be used for all rows in the control.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="cb824-121">Verweis</span><span class="sxs-lookup"><span data-stu-id="cb824-121">Reference</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <span data-ttu-id="cb824-122">Enthält die Referenzdokumentation für das <xref:System.Windows.Forms.DataGridView>-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="cb824-122">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 <xref:System.Windows.Forms.DataGridViewCellStyle>  
 <span data-ttu-id="cb824-123">Enthält die Referenz Dokumentation für die- <xref:System.Windows.Forms.DataGridViewCellStyle> Klasse.</span><span class="sxs-lookup"><span data-stu-id="cb824-123">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewCellStyle> class.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.CellFormatting>  
 <span data-ttu-id="cb824-124">Enthält die Referenz Dokumentation für das- <xref:System.Windows.Forms.DataGridView.CellFormatting> Ereignis.</span><span class="sxs-lookup"><span data-stu-id="cb824-124">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.CellFormatting> event.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.RowTemplate%2A>  
 <span data-ttu-id="cb824-125">Enthält die Referenz Dokumentation für die- <xref:System.Windows.Forms.DataGridView.RowTemplate%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="cb824-125">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.RowTemplate%2A> property.</span></span>  
  
## <a name="related-sections"></a><span data-ttu-id="cb824-126">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="cb824-126">Related Sections</span></span>  
 [<span data-ttu-id="cb824-127">Anpassen des DataGridView-Steuerelements von Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cb824-127">Customizing the Windows Forms DataGridView Control</span></span>](customizing-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="cb824-128">Enthält Themen, in denen das benutzerdefinierte Zeichnen von <xref:System.Windows.Forms.DataGridView>-Zellen und Zeilen und das Erstellen von abgeleiteten Zell-, Spalten- und Zeilentypen beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="cb824-128">Provides topics that describe custom painting <xref:System.Windows.Forms.DataGridView> cells and rows, and creating derived cell, column, and row types.</span></span>  
  
 [<span data-ttu-id="cb824-129">Grundlegende Spalten-, Zeilen- und Zellfunktionen im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="cb824-129">Basic Column, Row, and Cell Features in the Windows Forms DataGridView Control</span></span>](basic-column-row-and-cell-features-wf-datagridview-control.md)  
 <span data-ttu-id="cb824-130">Stellt Themen bereit, in denen häufig verwendete Zellen-, Zeilen-und Spalten Eigenschaften beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cb824-130">Provides topics that describe commonly used cell, row, and column properties.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb824-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb824-131">See also</span></span>

- [<span data-ttu-id="cb824-132">DataGridView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="cb824-132">DataGridView Control</span></span>](datagridview-control-windows-forms.md)
