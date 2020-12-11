---
title: Architektur des DataGridView-Steuerelements
ms.date: 03/30/2017
helpviewer_keywords:
- DataGridView control [Windows Forms], architecture
ms.assetid: 1c6cabf0-02ee-4bbc-9574-b54bb7f5b19e
ms.openlocfilehash: 2e1884383cca87f8d4ff84f486e2b29761a0c55d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972175"
---
# <a name="datagridview-control-architecture-windows-forms"></a><span data-ttu-id="e8242-102">Architektur des DataGridView-Steuerelements (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="e8242-102">DataGridView Control Architecture (Windows Forms)</span></span>
<span data-ttu-id="e8242-103">Das <xref:System.Windows.Forms.DataGridView> -Steuerelement und die zugehörigen Klassen sind als flexibles, erweiterbares System zum Anzeigen und Bearbeiten von Tabellendaten konzipiert.</span><span class="sxs-lookup"><span data-stu-id="e8242-103">The <xref:System.Windows.Forms.DataGridView> control and its related classes are designed to be a flexible, extensible system for displaying and editing tabular data.</span></span> <span data-ttu-id="e8242-104">Diese Klassen sind alle im <xref:System.Windows.Forms?displayProperty=nameWithType> -Namespace enthalten, und alle werden mit dem Präfix "DataGridView" benannt.</span><span class="sxs-lookup"><span data-stu-id="e8242-104">These classes are all contained in the <xref:System.Windows.Forms?displayProperty=nameWithType> namespace, and they are all named with the "DataGridView" prefix.</span></span>  
  
## <a name="architecture-elements"></a><span data-ttu-id="e8242-105">Architekturelemente</span><span class="sxs-lookup"><span data-stu-id="e8242-105">Architecture Elements</span></span>  
 <span data-ttu-id="e8242-106">Die primären <xref:System.Windows.Forms.DataGridView> Begleit Klassen werden von abgeleitet <xref:System.Windows.Forms.DataGridViewElement> .</span><span class="sxs-lookup"><span data-stu-id="e8242-106">The primary <xref:System.Windows.Forms.DataGridView> companion classes derive from <xref:System.Windows.Forms.DataGridViewElement>.</span></span> <span data-ttu-id="e8242-107">Das folgende Objektmodell veranschaulicht die <xref:System.Windows.Forms.DataGridViewElement> Vererbungs Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="e8242-107">The following object model illustrates the <xref:System.Windows.Forms.DataGridViewElement> inheritance hierarchy.</span></span>  
  
 ![Diagramm, das die datagridviewelements-Objektmodell Hierarchie anzeigt.](./media/datagridview-control-architecture-windows-forms/datagridviewelement-object-model.gif)  
  
 <span data-ttu-id="e8242-109">Die <xref:System.Windows.Forms.DataGridViewElement> -Klasse stellt einen Verweis auf das übergeordnete Steuerelement bereit <xref:System.Windows.Forms.DataGridView> und verfügt über eine- <xref:System.Windows.Forms.DataGridViewElement.State%2A> Eigenschaft, die einen Wert enthält, der eine Kombination von Werten aus der- <xref:System.Windows.Forms.DataGridViewElementStates> Enumeration darstellt.</span><span class="sxs-lookup"><span data-stu-id="e8242-109">The <xref:System.Windows.Forms.DataGridViewElement> class provides a reference to the parent <xref:System.Windows.Forms.DataGridView> control and has a <xref:System.Windows.Forms.DataGridViewElement.State%2A> property, which holds a value that represents a combination of values from the <xref:System.Windows.Forms.DataGridViewElementStates> enumeration.</span></span>  
  
 <span data-ttu-id="e8242-110">In den folgenden Abschnitten werden die <xref:System.Windows.Forms.DataGridView> Begleit Klassen ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e8242-110">The following sections describe the <xref:System.Windows.Forms.DataGridView> companion classes in more detail.</span></span>  
  
### <a name="datagridviewelementstates"></a><span data-ttu-id="e8242-111">DataGridViewElementStates</span><span class="sxs-lookup"><span data-stu-id="e8242-111">DataGridViewElementStates</span></span>  
 <span data-ttu-id="e8242-112">Die <xref:System.Windows.Forms.DataGridViewElementStates>-Enumeration verfügt über folgende Werte:</span><span class="sxs-lookup"><span data-stu-id="e8242-112">The <xref:System.Windows.Forms.DataGridViewElementStates> enumeration contains the following values:</span></span>  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.None>  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.Frozen>  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.ReadOnly>  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.Resizable>  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.ResizableSet>  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.Selected>  
  
- <xref:System.Windows.Forms.DataGridViewElementStates.Visible>  
  
 <span data-ttu-id="e8242-113">Die Werte dieser Enumeration können mit den bitweisen logischen Operatoren kombiniert werden, sodass die- <xref:System.Windows.Forms.DataGridViewElement.State%2A> Eigenschaft mehr als einen Status gleichzeitig Ausdrücken kann.</span><span class="sxs-lookup"><span data-stu-id="e8242-113">The values of this enumeration can be combined with the bitwise logical operators, so the <xref:System.Windows.Forms.DataGridViewElement.State%2A> property can express more than one state at once.</span></span> <span data-ttu-id="e8242-114">Beispielsweise kann ein <xref:System.Windows.Forms.DataGridViewElement> gleichzeitig <xref:System.Windows.Forms.DataGridViewElementStates.Frozen> , <xref:System.Windows.Forms.DataGridViewElementStates.Selected> und sein <xref:System.Windows.Forms.DataGridViewElementStates.Visible> .</span><span class="sxs-lookup"><span data-stu-id="e8242-114">For example, a <xref:System.Windows.Forms.DataGridViewElement> can be simultaneously <xref:System.Windows.Forms.DataGridViewElementStates.Frozen>, <xref:System.Windows.Forms.DataGridViewElementStates.Selected>, and <xref:System.Windows.Forms.DataGridViewElementStates.Visible>.</span></span>  
  
### <a name="cells-and-bands"></a><span data-ttu-id="e8242-115">Zellen und Bänder</span><span class="sxs-lookup"><span data-stu-id="e8242-115">Cells and Bands</span></span>  
 <span data-ttu-id="e8242-116">Das- <xref:System.Windows.Forms.DataGridView> Steuerelement besteht aus zwei grundlegenden Arten von Objekten: Zellen und Bänder.</span><span class="sxs-lookup"><span data-stu-id="e8242-116">The <xref:System.Windows.Forms.DataGridView> control comprises two fundamental kinds of objects: cells and bands.</span></span> <span data-ttu-id="e8242-117">Alle Zellen werden von der <xref:System.Windows.Forms.DataGridViewCell> Basisklasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e8242-117">All cells derive from the <xref:System.Windows.Forms.DataGridViewCell> base class.</span></span> <span data-ttu-id="e8242-118">Die beiden Arten von Bändern, <xref:System.Windows.Forms.DataGridViewColumn> und <xref:System.Windows.Forms.DataGridViewRow> , werden beide von der- <xref:System.Windows.Forms.DataGridViewBand> Basisklasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e8242-118">The two kinds of bands, <xref:System.Windows.Forms.DataGridViewColumn> and <xref:System.Windows.Forms.DataGridViewRow>, both derive from the <xref:System.Windows.Forms.DataGridViewBand> base class.</span></span>  
  
 <span data-ttu-id="e8242-119">Das- <xref:System.Windows.Forms.DataGridView> Steuerelement interagiert mit mehreren Klassen, aber die am häufigsten gefundenen sind <xref:System.Windows.Forms.DataGridViewCell> , <xref:System.Windows.Forms.DataGridViewColumn> und <xref:System.Windows.Forms.DataGridViewRow> .</span><span class="sxs-lookup"><span data-stu-id="e8242-119">The <xref:System.Windows.Forms.DataGridView> control interoperates with several classes, but the most commonly encountered are <xref:System.Windows.Forms.DataGridViewCell>, <xref:System.Windows.Forms.DataGridViewColumn>, and <xref:System.Windows.Forms.DataGridViewRow>.</span></span>  
  
### <a name="datagridviewcell"></a><span data-ttu-id="e8242-120">DataGridViewCell</span><span class="sxs-lookup"><span data-stu-id="e8242-120">DataGridViewCell</span></span>  
 <span data-ttu-id="e8242-121">Die Zelle ist die grundlegende Einheit der Interaktion für das <xref:System.Windows.Forms.DataGridView> .</span><span class="sxs-lookup"><span data-stu-id="e8242-121">The cell is the fundamental unit of interaction for the <xref:System.Windows.Forms.DataGridView>.</span></span> <span data-ttu-id="e8242-122">Die Anzeige wird auf Zellen zentriert, und der Dateneintrag wird häufig durch Zellen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="e8242-122">Display is centered on cells, and data entry is often performed through cells.</span></span> <span data-ttu-id="e8242-123">Mithilfe der-Auflistung der-Klasse können Sie auf Zellen zugreifen <xref:System.Windows.Forms.DataGridViewRow.Cells%2A> <xref:System.Windows.Forms.DataGridViewRow> , und Sie können mithilfe der-Auflistung des-Steuer Elements auf die ausgewählten Zellen zugreifen <xref:System.Windows.Forms.DataGridView.SelectedCells%2A> <xref:System.Windows.Forms.DataGridView> .</span><span class="sxs-lookup"><span data-stu-id="e8242-123">You can access cells by using the <xref:System.Windows.Forms.DataGridViewRow.Cells%2A> collection of the <xref:System.Windows.Forms.DataGridViewRow> class, and you can access the selected cells by using the <xref:System.Windows.Forms.DataGridView.SelectedCells%2A> collection of the <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="e8242-124">Das folgende Objektmodell veranschaulicht diese Verwendung und zeigt die <xref:System.Windows.Forms.DataGridViewCell> Vererbungs Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="e8242-124">The following object model illustrates this usage and shows the <xref:System.Windows.Forms.DataGridViewCell> inheritance hierarchy.</span></span>  
  
 ![Diagramm, das die DataGridViewCell-Objektmodell Hierarchie anzeigt.](./media/datagridview-control-architecture-windows-forms/datagridviewcell-object-model.gif)  
  
 <span data-ttu-id="e8242-126">Der <xref:System.Windows.Forms.DataGridViewCell> Typ ist eine abstrakte Basisklasse, von der alle Zelltypen abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="e8242-126">The <xref:System.Windows.Forms.DataGridViewCell> type is an abstract base class, from which all cell types derive.</span></span> <span data-ttu-id="e8242-127"><xref:System.Windows.Forms.DataGridViewCell> und die abgeleiteten Typen sind keine Windows Forms Steuerelemente, sondern einige Host Windows Forms-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="e8242-127"><xref:System.Windows.Forms.DataGridViewCell> and its derived types are not Windows Forms controls, but some host Windows Forms controls.</span></span> <span data-ttu-id="e8242-128">Alle von einer Zelle unterstützten Bearbeitungsfunktionen werden in der Regel von einem gehosteten Steuerelement behandelt.</span><span class="sxs-lookup"><span data-stu-id="e8242-128">Any editing functionality supported by a cell is typically handled by a hosted control.</span></span>  
  
 <span data-ttu-id="e8242-129"><xref:System.Windows.Forms.DataGridViewCell> -Objekte steuern ihre eigenen Erscheinungsbild-und Zeichnungsfunktionen nicht auf die gleiche Weise wie Windows Forms-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="e8242-129"><xref:System.Windows.Forms.DataGridViewCell> objects do not control their own appearance and painting features in the same way as Windows Forms controls.</span></span> <span data-ttu-id="e8242-130">Stattdessen ist der <xref:System.Windows.Forms.DataGridView> für das Aussehen seiner <xref:System.Windows.Forms.DataGridViewCell> Objekte verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="e8242-130">Instead, the <xref:System.Windows.Forms.DataGridView> is responsible for the appearance of its <xref:System.Windows.Forms.DataGridViewCell> objects.</span></span> <span data-ttu-id="e8242-131">Sie können die Darstellung und das Verhalten von Zellen durch Interaktion mit den <xref:System.Windows.Forms.DataGridView> Eigenschaften und Ereignissen des-Steuer Elements erheblich beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="e8242-131">You can significantly affect the appearance and behavior of cells by interacting with the <xref:System.Windows.Forms.DataGridView> control's properties and events.</span></span> <span data-ttu-id="e8242-132">Wenn Sie besondere Anforderungen an Anpassungen haben, die über die Funktionen des Steuer Elements hinausgehen <xref:System.Windows.Forms.DataGridView> , können Sie eine eigene Klasse implementieren, die von <xref:System.Windows.Forms.DataGridViewCell> oder einer ihrer untergeordneten Klassen abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="e8242-132">When you have special requirements for customizations that are beyond the capabilities of the <xref:System.Windows.Forms.DataGridView> control, you can implement your own class that derives from <xref:System.Windows.Forms.DataGridViewCell> or one of its child classes.</span></span>  
  
 <span data-ttu-id="e8242-133">Die folgende Liste zeigt die Klassen, die von abgeleitet sind <xref:System.Windows.Forms.DataGridViewCell> :</span><span class="sxs-lookup"><span data-stu-id="e8242-133">The following list shows the classes derived from <xref:System.Windows.Forms.DataGridViewCell>:</span></span>  
  
- <xref:System.Windows.Forms.DataGridViewTextBoxCell>  
  
- <xref:System.Windows.Forms.DataGridViewButtonCell>  
  
- <xref:System.Windows.Forms.DataGridViewLinkCell>  
  
- <xref:System.Windows.Forms.DataGridViewCheckBoxCell>  
  
- <xref:System.Windows.Forms.DataGridViewComboBoxCell>  
  
- <xref:System.Windows.Forms.DataGridViewImageCell>  
  
- <xref:System.Windows.Forms.DataGridViewHeaderCell>  
  
- <xref:System.Windows.Forms.DataGridViewRowHeaderCell>  
  
- <xref:System.Windows.Forms.DataGridViewColumnHeaderCell>  
  
- <xref:System.Windows.Forms.DataGridViewTopLeftHeaderCell>  
  
- <span data-ttu-id="e8242-134">Ihre benutzerdefinierten Zelltypen</span><span class="sxs-lookup"><span data-stu-id="e8242-134">Your custom cell types</span></span>  
  
### <a name="datagridviewcolumn"></a><span data-ttu-id="e8242-135">DataGridViewColumn</span><span class="sxs-lookup"><span data-stu-id="e8242-135">DataGridViewColumn</span></span>  
 <span data-ttu-id="e8242-136">Das Schema des <xref:System.Windows.Forms.DataGridView> angefügten Datenspeicher des Steuer Elements wird in den <xref:System.Windows.Forms.DataGridView> Spalten des Steuer Elements ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="e8242-136">The schema of the <xref:System.Windows.Forms.DataGridView> control's attached data store is expressed in the <xref:System.Windows.Forms.DataGridView> control's columns.</span></span> <span data-ttu-id="e8242-137">Sie können auf die <xref:System.Windows.Forms.DataGridView> Spalten des Steuer Elements mithilfe der-Auflistung zugreifen <xref:System.Windows.Forms.DataGridView.Columns%2A> .</span><span class="sxs-lookup"><span data-stu-id="e8242-137">You can access the <xref:System.Windows.Forms.DataGridView> control's columns by using the <xref:System.Windows.Forms.DataGridView.Columns%2A> collection.</span></span> <span data-ttu-id="e8242-138">Sie können auf die ausgewählten Spalten zugreifen, indem Sie die-Auflistung verwenden <xref:System.Windows.Forms.DataGridView.SelectedColumns%2A> .</span><span class="sxs-lookup"><span data-stu-id="e8242-138">You can access the selected columns by using the <xref:System.Windows.Forms.DataGridView.SelectedColumns%2A> collection.</span></span> <span data-ttu-id="e8242-139">Das folgende Objektmodell veranschaulicht diese Verwendung und zeigt die <xref:System.Windows.Forms.DataGridViewColumn> Vererbungs Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="e8242-139">The following object model illustrates this usage and shows the <xref:System.Windows.Forms.DataGridViewColumn> inheritance hierarchy.</span></span>  
  
 ![Diagramm, das die DataGridViewColumn-Objektmodell Hierarchie anzeigt.](./media/datagridview-control-architecture-windows-forms/datagridviewcolumn-object-model.gif)  
  
 <span data-ttu-id="e8242-141">Einige der Schlüssel Zelltypen weisen entsprechende Spaltentypen auf.</span><span class="sxs-lookup"><span data-stu-id="e8242-141">Some of the key cell types have corresponding column types.</span></span> <span data-ttu-id="e8242-142">Diese werden von der- <xref:System.Windows.Forms.DataGridViewColumn> Basisklasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="e8242-142">These are derived from the <xref:System.Windows.Forms.DataGridViewColumn> base class.</span></span>  
  
 <span data-ttu-id="e8242-143">Die folgende Liste zeigt die Klassen, die von abgeleitet sind <xref:System.Windows.Forms.DataGridViewColumn> :</span><span class="sxs-lookup"><span data-stu-id="e8242-143">The following list shows the classes derived from <xref:System.Windows.Forms.DataGridViewColumn>:</span></span>  
  
- <xref:System.Windows.Forms.DataGridViewButtonColumn>  
  
- <xref:System.Windows.Forms.DataGridViewCheckBoxColumn>  
  
- <xref:System.Windows.Forms.DataGridViewComboBoxColumn>  
  
- <xref:System.Windows.Forms.DataGridViewImageColumn>  
  
- <xref:System.Windows.Forms.DataGridViewTextBoxColumn>  
  
- <xref:System.Windows.Forms.DataGridViewLinkColumn>  
  
- <span data-ttu-id="e8242-144">Ihre benutzerdefinierten Spaltentypen</span><span class="sxs-lookup"><span data-stu-id="e8242-144">Your custom column types</span></span>  
  
### <a name="datagridview-editing-controls"></a><span data-ttu-id="e8242-145">DataGridView-Bearbeitungs Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="e8242-145">DataGridView Editing Controls</span></span>  
 <span data-ttu-id="e8242-146">Zellen, die erweiterte Bearbeitungsfunktionen unterstützen, verwenden normalerweise ein gehosteter Steuerelement, das von einem Windows Forms Steuerelement abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="e8242-146">Cells that support advanced editing functionality typically use a hosted control that is derived from a Windows Forms control.</span></span> <span data-ttu-id="e8242-147">Diese Steuerelemente implementieren auch die- <xref:System.Windows.Forms.IDataGridViewEditingControl> Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e8242-147">These controls also implement the <xref:System.Windows.Forms.IDataGridViewEditingControl> interface.</span></span> <span data-ttu-id="e8242-148">Das folgende Objektmodell veranschaulicht die Verwendung dieser Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="e8242-148">The following object model illustrates the usage of these controls.</span></span>  
  
 ![Diagramm, das die DataGridView-Bearbeitungs Steuerelement-Objektmodell Hierarchie anzeigt.](./media/datagridview-control-architecture-windows-forms/datagridviewediting-object-model.gif)  
  
 <span data-ttu-id="e8242-150">Die folgenden Bearbeitungs Steuerelemente werden mit dem-Steuerelement bereitgestellt <xref:System.Windows.Forms.DataGridView> :</span><span class="sxs-lookup"><span data-stu-id="e8242-150">The following editing controls are provided with the <xref:System.Windows.Forms.DataGridView> control:</span></span>  
  
- <xref:System.Windows.Forms.DataGridViewComboBoxEditingControl>  
  
- <xref:System.Windows.Forms.DataGridViewTextBoxEditingControl>  
  
 <span data-ttu-id="e8242-151">Weitere Informationen zum Erstellen eigener Bearbeitungs Steuerelemente finden Sie unter Gewusst [wie: Hosten von Steuerelementen in Windows Forms DataGridView-Zellen](how-to-host-controls-in-windows-forms-datagridview-cells.md).</span><span class="sxs-lookup"><span data-stu-id="e8242-151">For information about creating your own editing controls, see [How to: Host Controls in Windows Forms DataGridView Cells](how-to-host-controls-in-windows-forms-datagridview-cells.md).</span></span>  
  
 <span data-ttu-id="e8242-152">In der folgenden Tabelle wird die Beziehung zwischen Zellen Typen, Spaltentypen und Bearbeitungs Steuerelementen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e8242-152">The following table illustrates the relationship among cell types, column types, and editing controls.</span></span>  
  
|<span data-ttu-id="e8242-153">Zellentyp</span><span class="sxs-lookup"><span data-stu-id="e8242-153">Cell type</span></span>|<span data-ttu-id="e8242-154">Gehosteter Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e8242-154">Hosted control</span></span>|<span data-ttu-id="e8242-155">Spaltentyp</span><span class="sxs-lookup"><span data-stu-id="e8242-155">Column type</span></span>|  
|---------------|--------------------|-----------------|  
|<xref:System.Windows.Forms.DataGridViewButtonCell>|<span data-ttu-id="e8242-156">–</span><span class="sxs-lookup"><span data-stu-id="e8242-156">n/a</span></span>|<xref:System.Windows.Forms.DataGridViewButtonColumn>|  
|<xref:System.Windows.Forms.DataGridViewCheckBoxCell>|<span data-ttu-id="e8242-157">–</span><span class="sxs-lookup"><span data-stu-id="e8242-157">n/a</span></span>|<xref:System.Windows.Forms.DataGridViewCheckBoxColumn>|  
|<xref:System.Windows.Forms.DataGridViewComboBoxCell>|<xref:System.Windows.Forms.DataGridViewComboBoxEditingControl>|<xref:System.Windows.Forms.DataGridViewComboBoxColumn>|  
|<xref:System.Windows.Forms.DataGridViewImageCell>|<span data-ttu-id="e8242-158">–</span><span class="sxs-lookup"><span data-stu-id="e8242-158">n/a</span></span>|<xref:System.Windows.Forms.DataGridViewImageColumn>|  
|<xref:System.Windows.Forms.DataGridViewLinkCell>|<span data-ttu-id="e8242-159">–</span><span class="sxs-lookup"><span data-stu-id="e8242-159">n/a</span></span>|<xref:System.Windows.Forms.DataGridViewLinkColumn>|  
|<xref:System.Windows.Forms.DataGridViewTextBoxCell>|<xref:System.Windows.Forms.DataGridViewTextBoxEditingControl>|<xref:System.Windows.Forms.DataGridViewTextBoxColumn>|  
  
### <a name="datagridviewrow"></a><span data-ttu-id="e8242-160">DataGridViewRow</span><span class="sxs-lookup"><span data-stu-id="e8242-160">DataGridViewRow</span></span>  
 <span data-ttu-id="e8242-161">Die <xref:System.Windows.Forms.DataGridViewRow> -Klasse zeigt die Datenfelder eines Datensatzes aus dem Datenspeicher an, an den das <xref:System.Windows.Forms.DataGridView> Steuerelement angefügt ist.</span><span class="sxs-lookup"><span data-stu-id="e8242-161">The <xref:System.Windows.Forms.DataGridViewRow> class displays a record's data fields from the data store to which the <xref:System.Windows.Forms.DataGridView> control is attached.</span></span> <span data-ttu-id="e8242-162"><xref:System.Windows.Forms.DataGridView>Mithilfe der-Auflistung können Sie auf die Zeilen des-Steuer Elements zugreifen <xref:System.Windows.Forms.DataGridView.Rows%2A> .</span><span class="sxs-lookup"><span data-stu-id="e8242-162">You can access the <xref:System.Windows.Forms.DataGridView> control's rows by using the <xref:System.Windows.Forms.DataGridView.Rows%2A> collection.</span></span> <span data-ttu-id="e8242-163">Sie können auf die ausgewählten Zeilen zugreifen, indem Sie die-Auflistung verwenden <xref:System.Windows.Forms.DataGridView.SelectedRows%2A> .</span><span class="sxs-lookup"><span data-stu-id="e8242-163">You can access the selected rows by using the <xref:System.Windows.Forms.DataGridView.SelectedRows%2A> collection.</span></span> <span data-ttu-id="e8242-164">Das folgende Objektmodell veranschaulicht diese Verwendung und zeigt die <xref:System.Windows.Forms.DataGridViewRow> Vererbungs Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="e8242-164">The following object model illustrates this usage and shows the <xref:System.Windows.Forms.DataGridViewRow> inheritance hierarchy.</span></span>  
  
 ![Diagramm, das die DataGridViewRow-Objektmodell Hierarchie anzeigt.](./media/datagridview-control-architecture-windows-forms/datagridviewrow-object-model.gif)
  
 <span data-ttu-id="e8242-166">Sie können eigene Typen aus der- <xref:System.Windows.Forms.DataGridViewRow> Klasse ableiten, obwohl dies in der Regel nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e8242-166">You can derive your own types from the <xref:System.Windows.Forms.DataGridViewRow> class, although this will typically not be necessary.</span></span> <span data-ttu-id="e8242-167">Das <xref:System.Windows.Forms.DataGridView> -Steuerelement verfügt über mehrere Zeilen bezogene Ereignisse und Eigenschaften, mit denen das Verhalten seiner Objekte angepasst werden soll <xref:System.Windows.Forms.DataGridViewRow> .</span><span class="sxs-lookup"><span data-stu-id="e8242-167">The <xref:System.Windows.Forms.DataGridView> control has several row-related events and properties for customizing the behavior of its <xref:System.Windows.Forms.DataGridViewRow> objects.</span></span>  
  
 <span data-ttu-id="e8242-168">Wenn Sie die <xref:System.Windows.Forms.DataGridView> -Eigenschaft des Steuer Elements aktivieren <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A> , wird eine spezielle Zeile zum Hinzufügen neuer Zeilen als letzte Zeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e8242-168">If you enable the <xref:System.Windows.Forms.DataGridView> control's <xref:System.Windows.Forms.DataGridView.AllowUserToAddRows%2A> property, a special row for adding new rows appears as the last row.</span></span> <span data-ttu-id="e8242-169">Diese Zeile ist Teil der Auflistung <xref:System.Windows.Forms.DataGridView.Rows%2A> , verfügt jedoch über spezielle Funktionen, die möglicherweise Ihre Aufmerksamkeit erfordern.</span><span class="sxs-lookup"><span data-stu-id="e8242-169">This row is part of the <xref:System.Windows.Forms.DataGridView.Rows%2A> collection, but it has special functionality that may require your attention.</span></span> <span data-ttu-id="e8242-170">Weitere Informationen finden Sie unter [Verwenden der Zeile für neue Datensätze im Windows Forms DataGridView-Steuer](using-the-row-for-new-records-in-the-windows-forms-datagridview-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="e8242-170">For more information, see [Using the Row for New Records in the Windows Forms DataGridView Control](using-the-row-for-new-records-in-the-windows-forms-datagridview-control.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8242-171">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8242-171">See also</span></span>

- [<span data-ttu-id="e8242-172">Übersicht über das DataGridView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e8242-172">DataGridView Control Overview</span></span>](datagridview-control-overview-windows-forms.md)
- [<span data-ttu-id="e8242-173">Anpassen des DataGridView-Steuerelements von Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e8242-173">Customizing the Windows Forms DataGridView Control</span></span>](customizing-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="e8242-174">Verwenden der Zeile für neue Datensätze im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e8242-174">Using the Row for New Records in the Windows Forms DataGridView Control</span></span>](using-the-row-for-new-records-in-the-windows-forms-datagridview-control.md)
