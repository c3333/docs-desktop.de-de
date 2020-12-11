---
title: Verwendung von Auswahl und Zwischenablage mit dem DataGridView-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], Clipboard use
- cells [Windows Forms], selecting in grids
- Clipboard [Windows Forms], in DataGridView control
- selection [Windows Forms], in DataGridView control
- data grids [Windows Forms], selecting cells
- DataGridView control [Windows Forms], selecting cells
ms.assetid: 82cffcad-8b30-4897-bddb-c3a79d751b83
ms.openlocfilehash: 6993f77e8ce532d8df1bdc7e6b6abc1cc3268e49
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972333"
---
# <a name="selection-and-clipboard-use-with-the-windows-forms-datagridview-control"></a><span data-ttu-id="6d0c6-102">Verwendung von Auswahl und Zwischenablage mit dem DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6d0c6-102">Selection and Clipboard Use with the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="6d0c6-103">Das- `DataGridView` Steuerelement bietet Ihnen eine Vielzahl von Optionen, um zu konfigurieren, wie Benutzer Zellen, Zeilen und Spalten auswählen können.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-103">The `DataGridView` control provides you with a variety of options for configuring how users can select cells, rows, and columns.</span></span> <span data-ttu-id="6d0c6-104">Sie können z. b. eine einzelne oder mehrere Auswahl, die Auswahl ganzer Zeilen oder Spalten aktivieren, wenn Benutzer auf Zellen klicken, oder die Auswahl ganzer Zeilen oder Spalten nur dann, wenn Benutzer auf Ihre Header klicken, wodurch auch die Zellen Auswahl aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-104">For example, you can enable single or multiple selection, selection of whole rows or columns when users click cells, or selection of whole rows or columns only when users click their headers, which enables cell selection as well.</span></span> <span data-ttu-id="6d0c6-105">Wenn Sie eine eigene Benutzeroberfläche für die Auswahl bereitstellen möchten, können Sie die normale Auswahl deaktivieren und die gesamte Auswahlprogramm gesteuert verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-105">If you want to provide your own user interface for selection, you can disable ordinary selection and handle all selection programmatically.</span></span> <span data-ttu-id="6d0c6-106">Außerdem können Sie es Benutzern ermöglichen, die ausgewählten Werte in die Zwischenablage zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-106">Additionally, you can enable users to copy the selected values to the Clipboard.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="6d0c6-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6d0c6-107">In This Section</span></span>  
 [<span data-ttu-id="6d0c6-108">Auswahlmodi im DataGridView-Steuerelement von Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6d0c6-108">Selection Modes in the Windows Forms DataGridView Control</span></span>](selection-modes-in-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="6d0c6-109">Beschreibt die Optionen für Benutzer-und programmgesteuerte Auswahl im-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-109">Describes the options for user and programmatic selection in the control.</span></span>  
  
 [<span data-ttu-id="6d0c6-110">Vorgehensweise: Festlegen des Auswahlmodus des DataGridView-Steuerelements in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6d0c6-110">How to: Set the Selection Mode of the Windows Forms DataGridView Control</span></span>](how-to-set-the-selection-mode-of-the-windows-forms-datagridview-control.md)  
 <span data-ttu-id="6d0c6-111">Beschreibt, wie das Steuerelement für eine einzeilige Auswahl konfiguriert wird, wenn ein Benutzer auf eine Zelle klickt.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-111">Describes how to configure the control for single-row selection when a user clicks a cell.</span></span>  
  
 [<span data-ttu-id="6d0c6-112">Vorgehensweise: Abrufen der ausgewählten Zellen, Zeilen und Spalten im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6d0c6-112">How to: Get the Selected Cells, Rows, and Columns in the Windows Forms DataGridView Control</span></span>](selected-cells-rows-and-columns-datagridview.md)  
 <span data-ttu-id="6d0c6-113">Beschreibt das Arbeiten mit den ausgewählten Zellen-, Zeilen-und Spalten Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-113">Describes how to work with the selected cell, row, and column collections.</span></span>  
  
 [<span data-ttu-id="6d0c6-114">Vorgehensweise: Festlegen, dass mehrere Zellen aus dem DataGridView-Steuerelement in Windows Forms in die Zwischenablage kopiert werden können</span><span class="sxs-lookup"><span data-stu-id="6d0c6-114">How to: Enable Users to Copy Multiple Cells to the Clipboard from the Windows Forms DataGridView Control</span></span>](enable-users-to-copy-multiple-cells-to-the-clipboard-datagridview.md)  
 <span data-ttu-id="6d0c6-115">Beschreibt, wie die Zwischenablage Unterstützung im-Steuerelement aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-115">Describes how to enable Clipboard support in the control.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="6d0c6-116">Verweis</span><span class="sxs-lookup"><span data-stu-id="6d0c6-116">Reference</span></span>  
 <xref:System.Windows.Forms.DataGridView>  
 <span data-ttu-id="6d0c6-117">Enthält die Referenzdokumentation für das <xref:System.Windows.Forms.DataGridView>-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-117">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView> control.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.SelectionMode%2A?displayProperty=nameWithType>  
 <span data-ttu-id="6d0c6-118">Enthält die Referenz Dokumentation für die- <xref:System.Windows.Forms.DataGridView.SelectionMode%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-118">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.SelectionMode%2A> property.</span></span>  
  
 <xref:System.Windows.Forms.DataGridView.ClipboardCopyMode%2A>  
 <span data-ttu-id="6d0c6-119">Enthält die Referenz Dokumentation für die- <xref:System.Windows.Forms.DataGridView.ClipboardCopyMode%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-119">Provides reference documentation for the <xref:System.Windows.Forms.DataGridView.ClipboardCopyMode%2A> property.</span></span>  
  
 <xref:System.Windows.Forms.DataGridViewSelectedCellCollection>  
 <span data-ttu-id="6d0c6-120">Enthält die Referenz Dokumentation für die- <xref:System.Windows.Forms.DataGridViewSelectedCellCollection> Klasse.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-120">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewSelectedCellCollection> class.</span></span>  
  
 <xref:System.Windows.Forms.DataGridViewSelectedRowCollection>  
 <span data-ttu-id="6d0c6-121">Enthält die Referenz Dokumentation für die- <xref:System.Windows.Forms.DataGridViewSelectedRowCollection> Klasse.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-121">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewSelectedRowCollection> class.</span></span>  
  
 <xref:System.Windows.Forms.DataGridViewSelectedColumnCollection>  
 <span data-ttu-id="6d0c6-122">Enthält die Referenz Dokumentation für die- <xref:System.Windows.Forms.DataGridViewSelectedColumnCollection> Klasse.</span><span class="sxs-lookup"><span data-stu-id="6d0c6-122">Provides reference documentation for the <xref:System.Windows.Forms.DataGridViewSelectedColumnCollection> class.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="6d0c6-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6d0c6-123">See also</span></span>

- [<span data-ttu-id="6d0c6-124">DataGridView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="6d0c6-124">DataGridView Control</span></span>](datagridview-control-windows-forms.md)
- [<span data-ttu-id="6d0c6-125">Standardbehandlung von Tastatur und Maus im DataGridView-Steuerelement von Windows Forms</span><span class="sxs-lookup"><span data-stu-id="6d0c6-125">Default Keyboard and Mouse Handling in the Windows Forms DataGridView Control</span></span>](default-keyboard-and-mouse-handling-in-the-windows-forms-datagridview-control.md)
