---
title: Standardfunktionen im DataGridView-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- data grids [Windows Forms], default functionality in DataGridView control
- DataGridView control [Windows Forms], default functionality
ms.assetid: 4405f697-cad1-4839-9bcd-8ddb09d9f00e
ms.openlocfilehash: b695883ac7ec3fb0c459adb66214b0eceab3a128
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972156"
---
# <a name="default-functionality-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="62bc4-102">Standardfunktionalität des DataGridView-Steuerelements von Windows Forms</span><span class="sxs-lookup"><span data-stu-id="62bc4-102">Default Functionality in the Windows Forms DataGridView Control</span></span>
<span data-ttu-id="62bc4-103">Das Windows Forms- <xref:System.Windows.Forms.DataGridView> Steuerelement bietet Benutzern eine beträchtliche Menge an Standardfunktionen.</span><span class="sxs-lookup"><span data-stu-id="62bc4-103">The Windows Forms <xref:System.Windows.Forms.DataGridView> control provides users with a significant amount of default functionality.</span></span>  
  
## <a name="default-functionality"></a><span data-ttu-id="62bc4-104">Standardfunktionalität</span><span class="sxs-lookup"><span data-stu-id="62bc4-104">Default Functionality</span></span>  
 <span data-ttu-id="62bc4-105">Standardmäßig ist ein- <xref:System.Windows.Forms.DataGridView> Steuerelement:</span><span class="sxs-lookup"><span data-stu-id="62bc4-105">By default, a <xref:System.Windows.Forms.DataGridView> control:</span></span>  
  
- <span data-ttu-id="62bc4-106">Zeigt automatisch Spaltenkopfzeilen und Zeilen Header an, die sichtbar bleiben, wenn die Tabelle vertikal scrollt.</span><span class="sxs-lookup"><span data-stu-id="62bc4-106">Automatically displays column headers and row headers that remain visible as the table scrolls vertically.</span></span>  
  
- <span data-ttu-id="62bc4-107">Verfügt über einen Zeilen Header, der einen Auswahl Indikator für die aktuelle Zeile enthält.</span><span class="sxs-lookup"><span data-stu-id="62bc4-107">Has a row header that contains a selection indicator for the current row.</span></span>  
  
- <span data-ttu-id="62bc4-108">Hat ein Auswahl Rechteck in der ersten Zelle.</span><span class="sxs-lookup"><span data-stu-id="62bc4-108">Has a selection rectangle in the first cell.</span></span>  
  
- <span data-ttu-id="62bc4-109">Enthält Spalten, deren Größe automatisch geändert werden kann, wenn der Benutzer auf die Spalten unter Teiler doppelklickt.</span><span class="sxs-lookup"><span data-stu-id="62bc4-109">Has columns that can be automatically resized when the user double-clicks the column dividers.</span></span>  
  
- <span data-ttu-id="62bc4-110">Unterstützt automatisch visuelle Stile unter Windows XP und der Windows Server 2003-Produktfamilie, wenn die <xref:System.Windows.Forms.Application.EnableVisualStyles%2A> -Methode von der-Methode der Anwendung aufgerufen wird `Main` .</span><span class="sxs-lookup"><span data-stu-id="62bc4-110">Automatically supports visual styles on Windows XP and the Windows Server 2003 family when the <xref:System.Windows.Forms.Application.EnableVisualStyles%2A> method is called from the application's `Main` method.</span></span>  
  
 <span data-ttu-id="62bc4-111">Außerdem kann der Inhalt eines <xref:System.Windows.Forms.DataGridView> Steuer Elements standardmäßig bearbeitet werden:</span><span class="sxs-lookup"><span data-stu-id="62bc4-111">Additionally, the contents of a <xref:System.Windows.Forms.DataGridView> control can be edited by default:</span></span>  
  
- <span data-ttu-id="62bc4-112">Wenn der Benutzer auf F2 in einer Zelle doppelklickt oder diese drückt, versetzt das Steuerelement die Zelle automatisch in den Bearbeitungsmodus und aktualisiert den Inhalt der Zelle als Benutzer.</span><span class="sxs-lookup"><span data-stu-id="62bc4-112">If the user double-clicks or presses F2 in a cell, the control automatically puts the cell into edit mode and updates the contents of the cell as the user types.</span></span>  
  
- <span data-ttu-id="62bc4-113">Wenn der Benutzer einen Bildlauf zum Ende des Rasters durchführt, wird dem Benutzer angezeigt, dass eine Zeile zum Hinzufügen neuer Datensätze vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="62bc4-113">If the user scrolls to the end of the grid, the user will see that a row for adding new records is present.</span></span> <span data-ttu-id="62bc4-114">Wenn der Benutzer auf diese Zeile klickt, wird dem Steuerelement eine neue Zeile <xref:System.Windows.Forms.DataGridView> mit Standardwerten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="62bc4-114">When the user clicks this row, a new row is added to the <xref:System.Windows.Forms.DataGridView> control, with default values.</span></span> <span data-ttu-id="62bc4-115">Wenn der Benutzer ESC drückt, verschwindet diese neue Zeile.</span><span class="sxs-lookup"><span data-stu-id="62bc4-115">When the user presses ESC, this new row disappears.</span></span>  
  
- <span data-ttu-id="62bc4-116">Wenn der Benutzer auf einen Zeilen Header klickt, wird die gesamte Zeile ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="62bc4-116">If the user clicks a row header, the whole row is selected.</span></span>  
  
 <span data-ttu-id="62bc4-117">Wenn Sie ein <xref:System.Windows.Forms.DataGridView> Steuerelement durch Festlegen der-Eigenschaft an eine Datenquelle binden <xref:System.Windows.Forms.DataGridView.DataSource%2A> , wird das-Steuerelement:</span><span class="sxs-lookup"><span data-stu-id="62bc4-117">When you bind a <xref:System.Windows.Forms.DataGridView> control to a data source by setting its <xref:System.Windows.Forms.DataGridView.DataSource%2A> property, the control:</span></span>  
  
- <span data-ttu-id="62bc4-118">Verwendet automatisch die Namen der Datenquellen Spalten als Spaltenheader Text.</span><span class="sxs-lookup"><span data-stu-id="62bc4-118">Automatically uses the names of the data source's columns as the column header text.</span></span>  
  
- <span data-ttu-id="62bc4-119">Wird mit dem Inhalt der Datenquelle aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="62bc4-119">Is populated with the contents of the data source.</span></span> <span data-ttu-id="62bc4-120"><xref:System.Windows.Forms.DataGridView> Spalten werden für jede Spalte in der Datenquelle automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="62bc4-120"><xref:System.Windows.Forms.DataGridView> columns are automatically created for each column in the data source.</span></span>  
  
- <span data-ttu-id="62bc4-121">Erstellt eine Zeile für jede sichtbare Zeile in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="62bc4-121">Creates a row for each visible row in the table.</span></span>  
  
- <span data-ttu-id="62bc4-122">Sortiert die Zeilen automatisch basierend auf den zugrunde liegenden Daten, wenn der Benutzer auf einen Spaltenheader klickt.</span><span class="sxs-lookup"><span data-stu-id="62bc4-122">Automatically sorts the rows based on the underlying data when the user clicks a column header.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="62bc4-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62bc4-123">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- [<span data-ttu-id="62bc4-124">DataGridView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="62bc4-124">DataGridView Control</span></span>](datagridview-control-windows-forms.md)
