---
title: Erstellen einer Nachschlage Tabelle für das ComboBox-, ListBox-oder CheckedListBox-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- CheckedListBox control [Windows Forms], creating lookup tables
- lookup tables
- list boxes [Windows Forms], lookup tables
- ListBox control [Windows Forms], lookup tables
- ComboBox control [Windows Forms], lookup table
- lookup tables [Windows Forms], creating for controls
- combo boxes [Windows Forms], lookup tables
- ListBox control [Windows Forms], creating lookup tables
ms.assetid: 4ce35f12-1f4e-4317-92d1-af8686a8cfaa
ms.openlocfilehash: 57dc95fc16d77ee1492f53bf57eac001a343ca8f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972216"
---
# <a name="how-to-create-a-lookup-table-for-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a><span data-ttu-id="ad652-102">Vorgehensweise: Erstellen einer Suchtabelle für ComboBox-, ListBox- oder CheckedListBox-Steuerelemente in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ad652-102">How to: Create a Lookup Table for a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>

<span data-ttu-id="ad652-103">Manchmal ist es sinnvoll, Daten in einem benutzerfreundlichen Format in einem Windows Form anzuzeigen, aber Sie sollten die Daten in einem Format speichern, das vor allem für Ihr Programm sinnvoll ist.</span><span class="sxs-lookup"><span data-stu-id="ad652-103">Sometimes it is useful to display data in a user-friendly format on a Windows Form, but store the data in a format that is more meaningful to your program.</span></span> <span data-ttu-id="ad652-104">Beispielsweise können in einem Bestellformular für Nahrungsmittel die Menüelemente nach Namen in einem Listenfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ad652-104">For example, an order form for food might display the menu items by name in a list box.</span></span> <span data-ttu-id="ad652-105">Die zur Erfassung der Bestellung verwendete Datentabelle enthält hingegen die eindeutigen ID-Nummern der Nahrungsmittel.</span><span class="sxs-lookup"><span data-stu-id="ad652-105">However, the data table recording the order would contain the unique ID numbers representing the food.</span></span> <span data-ttu-id="ad652-106">Die folgende Tabelle enthält ein Beispiel zum Speichern und Anzeigen von Bestellformulardaten für Nahrungsmittel.</span><span class="sxs-lookup"><span data-stu-id="ad652-106">The following tables show an example of how to store and display order-form data for food.</span></span>  
  
### <a name="orderdetailstable"></a><span data-ttu-id="ad652-107">OrderDetailsTable</span><span class="sxs-lookup"><span data-stu-id="ad652-107">OrderDetailsTable</span></span>  
  
|<span data-ttu-id="ad652-108">OrderID</span><span class="sxs-lookup"><span data-stu-id="ad652-108">OrderID</span></span>|<span data-ttu-id="ad652-109">Artikel-ID</span><span class="sxs-lookup"><span data-stu-id="ad652-109">ItemID</span></span>|<span data-ttu-id="ad652-110">Menge</span><span class="sxs-lookup"><span data-stu-id="ad652-110">Quantity</span></span>|  
|-------------|------------|--------------|  
|<span data-ttu-id="ad652-111">4085</span><span class="sxs-lookup"><span data-stu-id="ad652-111">4085</span></span>|<span data-ttu-id="ad652-112">12</span><span class="sxs-lookup"><span data-stu-id="ad652-112">12</span></span>|<span data-ttu-id="ad652-113">1</span><span class="sxs-lookup"><span data-stu-id="ad652-113">1</span></span>|  
|<span data-ttu-id="ad652-114">4086</span><span class="sxs-lookup"><span data-stu-id="ad652-114">4086</span></span>|<span data-ttu-id="ad652-115">13</span><span class="sxs-lookup"><span data-stu-id="ad652-115">13</span></span>|<span data-ttu-id="ad652-116">3</span><span class="sxs-lookup"><span data-stu-id="ad652-116">3</span></span>|  
  
### <a name="itemtable"></a><span data-ttu-id="ad652-117">ItemTable</span><span class="sxs-lookup"><span data-stu-id="ad652-117">ItemTable</span></span>  
  
|<span data-ttu-id="ad652-118">id</span><span class="sxs-lookup"><span data-stu-id="ad652-118">ID</span></span>|<span data-ttu-id="ad652-119">Name</span><span class="sxs-lookup"><span data-stu-id="ad652-119">Name</span></span>|  
|--------|----------|  
|<span data-ttu-id="ad652-120">12</span><span class="sxs-lookup"><span data-stu-id="ad652-120">12</span></span>|<span data-ttu-id="ad652-121">Kartoffel</span><span class="sxs-lookup"><span data-stu-id="ad652-121">Potato</span></span>|  
|<span data-ttu-id="ad652-122">13</span><span class="sxs-lookup"><span data-stu-id="ad652-122">13</span></span>|<span data-ttu-id="ad652-123">Huhn</span><span class="sxs-lookup"><span data-stu-id="ad652-123">Chicken</span></span>|  
  
 <span data-ttu-id="ad652-124">In diesem Szenario speichert eine Tabelle, **OrderDetailsTable**, die tatsächlichen Informationen, die Sie beim Anzeigen und speichern berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="ad652-124">In this scenario, one table, **OrderDetailsTable**, stores the actual information you are concerned with displaying and saving.</span></span> <span data-ttu-id="ad652-125">Allerdings geschieht dies aus Platzgründen auf eine ziemlich kryptische Art und Weise.</span><span class="sxs-lookup"><span data-stu-id="ad652-125">But to save space, it does so in a fairly cryptic fashion.</span></span> <span data-ttu-id="ad652-126">Die andere Tabelle, **ItemTable**, enthält nur Darstellungs bezogene Informationen darüber, welche ID-Nummer mit welchem Nahrungsmittel Namen übereinstimmt, und nichts über die tatsächlichen Nahrungsmittel Bestellungen.</span><span class="sxs-lookup"><span data-stu-id="ad652-126">The other table, **ItemTable**, contains only appearance-related information about which ID number is equivalent to which food name, and nothing about the actual food orders.</span></span>  
  
 <span data-ttu-id="ad652-127">Das **ItemTable** -Steuerelement ist mit dem <xref:System.Windows.Forms.ComboBox> Steuerelement, <xref:System.Windows.Forms.ListBox> oder <xref:System.Windows.Forms.CheckedListBox> über drei Eigenschaften verbunden.</span><span class="sxs-lookup"><span data-stu-id="ad652-127">The **ItemTable** is connected to the <xref:System.Windows.Forms.ComboBox>, <xref:System.Windows.Forms.ListBox>, or <xref:System.Windows.Forms.CheckedListBox> control through three properties.</span></span> <span data-ttu-id="ad652-128">Die- `DataSource` Eigenschaft enthält den Namen dieser Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ad652-128">The `DataSource` property contains the name of this table.</span></span> <span data-ttu-id="ad652-129">Die- `DisplayMember` Eigenschaft enthält die Datenspalte der Tabelle, die im-Steuerelement (dem Nahrungsmittel Namen) angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad652-129">The `DisplayMember` property contains the data column of that table that you want to display in the control (the food name).</span></span> <span data-ttu-id="ad652-130">Die- `ValueMember` Eigenschaft enthält die Datenspalte der Tabelle mit den gespeicherten Informationen (ID-Nummer).</span><span class="sxs-lookup"><span data-stu-id="ad652-130">The `ValueMember` property contains the data column of that table with the stored information (the ID number).</span></span>  
  
 <span data-ttu-id="ad652-131">" **OrderDetailsTable** " ist über seine Bindungs Auflistung mit dem Steuerelement verbunden, und der Zugriff erfolgt über die- <xref:System.Windows.Forms.Control.DataBindings%2A> Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ad652-131">The **OrderDetailsTable** is connected to the control by its bindings collection, accessed through the <xref:System.Windows.Forms.Control.DataBindings%2A> property.</span></span> <span data-ttu-id="ad652-132">Wenn Sie der Auflistung ein Bindungs Objekt hinzufügen, verbinden Sie eine Steuerelement Eigenschaft mit einem bestimmten Datenmember (der Spalte mit ID-Nummern) in einer Datenquelle ( **OrderDetailsTable**).</span><span class="sxs-lookup"><span data-stu-id="ad652-132">When you add a binding object to the collection, you connect a control property to a specific data member (the column of ID numbers) in a data source (the **OrderDetailsTable**).</span></span> <span data-ttu-id="ad652-133">Wenn im Steuerelement eine Auswahl getroffen wird, wird die Formulareingabe in dieser Tabelle gespeichert.</span><span class="sxs-lookup"><span data-stu-id="ad652-133">When a selection is made in the control, this table is where the form input is saved.</span></span>  
  
### <a name="to-create-a-lookup-table"></a><span data-ttu-id="ad652-134">So erstellen Sie eine Suchtabelle</span><span class="sxs-lookup"><span data-stu-id="ad652-134">To create a lookup table</span></span>  
  
1. <span data-ttu-id="ad652-135">Fügen Sie dem Formular ein Steuerelement "<xref:System.Windows.Forms.ComboBox>", "<xref:System.Windows.Forms.ListBox>", oder "<xref:System.Windows.Forms.CheckedListBox>" hinzu.</span><span class="sxs-lookup"><span data-stu-id="ad652-135">Add a <xref:System.Windows.Forms.ComboBox>, <xref:System.Windows.Forms.ListBox>, or <xref:System.Windows.Forms.CheckedListBox> control to the form.</span></span>  
  
2. <span data-ttu-id="ad652-136">Stellen Sie eine Verbindung zur Datenquelle her.</span><span class="sxs-lookup"><span data-stu-id="ad652-136">Connect to your data source.</span></span>  
  
3. <span data-ttu-id="ad652-137">Richten Sie eine Datenbeziehung zwischen den beiden Tabellen ein.</span><span class="sxs-lookup"><span data-stu-id="ad652-137">Establish a data relation between the two tables.</span></span> <span data-ttu-id="ad652-138">Weitere [Informationen finden Sie unter Einführung in DataRelations-Objekte](/previous-versions/visualstudio/visual-studio-2013/0k21zcyx(v=vs.120)).</span><span class="sxs-lookup"><span data-stu-id="ad652-138">See [Introduction to DataRelation Objects](/previous-versions/visualstudio/visual-studio-2013/0k21zcyx(v=vs.120)).</span></span>  
  
4. <span data-ttu-id="ad652-139">Legen Sie die folgenden Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="ad652-139">Set the following properties.</span></span> <span data-ttu-id="ad652-140">Sie können im Code oder im Designer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ad652-140">They can be set in code or in the designer.</span></span>  
  
    |<span data-ttu-id="ad652-141">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ad652-141">Property</span></span>|<span data-ttu-id="ad652-142">Einstellung</span><span class="sxs-lookup"><span data-stu-id="ad652-142">Setting</span></span>|  
    |--------------|-------------|  
    |<xref:System.Windows.Forms.ListControl.DataSource%2A>|<span data-ttu-id="ad652-143">Die Tabelle, die Informationen darüber enthält, welche ID-Nummer welchem Element entspricht.</span><span class="sxs-lookup"><span data-stu-id="ad652-143">The table that contains information about which ID number is equivalent to which item.</span></span> <span data-ttu-id="ad652-144">Im vorherigen Szenario ist dies `ItemTable` .</span><span class="sxs-lookup"><span data-stu-id="ad652-144">In the previous scenario, this is `ItemTable`.</span></span>|  
    |<xref:System.Windows.Forms.ListControl.DisplayMember%2A>|<span data-ttu-id="ad652-145">Die Spalte der Datenquellentabelle, die im Steuerelement angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad652-145">The column of the data source table that you want to display in the control.</span></span> <span data-ttu-id="ad652-146">Im vorherigen Szenario ist dies `"Name"` (um im Code festzulegen, die Verwendung von Anführungszeichen).</span><span class="sxs-lookup"><span data-stu-id="ad652-146">In the previous scenario, this is `"Name"` (to set in code, use quotation marks).</span></span>|  
    |<xref:System.Windows.Forms.ListControl.ValueMember%2A>|<span data-ttu-id="ad652-147">Die Spalte der Datenquellentabelle, die die gespeicherten Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="ad652-147">The column of the data source table that contains the stored information.</span></span> <span data-ttu-id="ad652-148">Im vorherigen Szenario ist dies `"ID"` (um im Code festzulegen, die Verwendung von Anführungszeichen).</span><span class="sxs-lookup"><span data-stu-id="ad652-148">In the previous scenario, this is `"ID"` (to set in code, use quotation marks).</span></span>|  
  
5. <span data-ttu-id="ad652-149">Rufen Sie in einer Prozedur die Methode "<xref:System.Windows.Forms.ControlBindingsCollection.Add%2A>" der Klasse "<xref:System.Windows.Forms.ControlBindingsCollection>" auf, um die Eigenschaft "<xref:System.Windows.Forms.ListControl.SelectedValue%2A>" des Steuerelements an die Tabelle zu binden, die die Formulareingabe erfasst.</span><span class="sxs-lookup"><span data-stu-id="ad652-149">In a procedure, call the <xref:System.Windows.Forms.ControlBindingsCollection.Add%2A> method of the <xref:System.Windows.Forms.ControlBindingsCollection> class to bind the control's <xref:System.Windows.Forms.ListControl.SelectedValue%2A> property to the table recording the form input.</span></span> <span data-ttu-id="ad652-150">Sie können dies auch im Designer anstelle von im Code durchführen, indem Sie <xref:System.Windows.Forms.Control.DataBindings%2A> im **Eigenschaften** Fenster auf die-Eigenschaft des Steuer Elements zugreifen.</span><span class="sxs-lookup"><span data-stu-id="ad652-150">You can also do this in the Designer instead of in code, by accessing the control's <xref:System.Windows.Forms.Control.DataBindings%2A> property in the **Properties** window.</span></span> <span data-ttu-id="ad652-151">Im vorherigen Szenario ist dies `OrderDetailsTable` , und die-Spalte ist `"ItemID"` .</span><span class="sxs-lookup"><span data-stu-id="ad652-151">In the previous scenario, this is `OrderDetailsTable`, and the column is `"ItemID"`.</span></span>  
  
    ```vb  
    ListBox1.DataBindings.Add("SelectedValue", OrderDetailsTable, "ItemID")  
    ```  
  
    ```csharp  
    listBox1.DataBindings.Add("SelectedValue", OrderDetailsTable, "ItemID");  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="ad652-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad652-152">See also</span></span>

- [<span data-ttu-id="ad652-153">Datenbindung und Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ad652-153">Data Binding and Windows Forms</span></span>](../data-binding-and-windows-forms.md)
- [<span data-ttu-id="ad652-154">Übersicht über das ListBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ad652-154">ListBox Control Overview</span></span>](listbox-control-overview-windows-forms.md)
- [<span data-ttu-id="ad652-155">Übersicht über das ComboBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ad652-155">ComboBox Control Overview</span></span>](combobox-control-overview-windows-forms.md)
- [<span data-ttu-id="ad652-156">Übersicht über das CheckedListBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ad652-156">CheckedListBox Control Overview</span></span>](checkedlistbox-control-overview-windows-forms.md)
- [<span data-ttu-id="ad652-157">Steuerelemente in Windows Forms zum Auflisten von Optionen</span><span class="sxs-lookup"><span data-stu-id="ad652-157">Windows Forms Controls Used to List Options</span></span>](windows-forms-controls-used-to-list-options.md)
