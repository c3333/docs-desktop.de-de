---
title: Erstellen einer Nachschlage Tabelle mit der BindingSource-Komponente
ms.date: 03/30/2017
helpviewer_keywords:
- lookup tables
- tables [Windows Forms], creating lookup tables
- BindingSource component [Windows Forms], creating a lookup table
- BindingSource component [Windows Forms], examples
ms.assetid: 622fce80-879d-44be-abbf-8350ec22ca2b
ms.openlocfilehash: ccf2bfa6cf3f56a38b55f8c87004c42a46172891
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975699"
---
# <a name="how-to-create-a-lookup-table-with-the-windows-forms-bindingsource-component"></a><span data-ttu-id="d3648-102">Vorgehensweise: Erstellen einer Suchtabelle mit der BindingSource-Komponente in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d3648-102">How to: Create a Lookup Table with the Windows Forms BindingSource Component</span></span>
<span data-ttu-id="d3648-103">Eine Nachschlagetabelle ist eine Tabelle mit Daten, in der die Daten aus Datensätzen einer verknüpften Tabelle in einer Spalte dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d3648-103">A lookup table is a table of data that has a column that displays data from records in a related table.</span></span> <span data-ttu-id="d3648-104">In den folgenden Verfahren wird ein <xref:System.Windows.Forms.ComboBox>-Steuerelement für die Anzeige des Felds mit der Fremdschlüsselbeziehung von der übergeordneten zur untergeordneten Tabelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3648-104">In the following procedures, a <xref:System.Windows.Forms.ComboBox> control is used to display the field with the foreign-key relationship from the parent to the child table.</span></span>  
  
 <span data-ttu-id="d3648-105">Zur Visualisierung dieser beiden Tabellen und dieser Beziehung finden Sie hier ein Beispiel einer über- und untergeordneten Tabelle:</span><span class="sxs-lookup"><span data-stu-id="d3648-105">To help visualize these two tables and this relationship, here is an example of a parent and child table:</span></span>  
  
 <span data-ttu-id="d3648-106">KundenTabelle (übergeordnete Tabelle)</span><span class="sxs-lookup"><span data-stu-id="d3648-106">CustomersTable (parent table)</span></span>  
  
|<span data-ttu-id="d3648-107">CustomerID</span><span class="sxs-lookup"><span data-stu-id="d3648-107">CustomerID</span></span>|<span data-ttu-id="d3648-108">CustomerName</span><span class="sxs-lookup"><span data-stu-id="d3648-108">CustomerName</span></span>|  
|----------------|------------------|  
|<span data-ttu-id="d3648-109">712</span><span class="sxs-lookup"><span data-stu-id="d3648-109">712</span></span>|<span data-ttu-id="d3648-110">Paul Koch</span><span class="sxs-lookup"><span data-stu-id="d3648-110">Paul Koch</span></span>|  
|<span data-ttu-id="d3648-111">713</span><span class="sxs-lookup"><span data-stu-id="d3648-111">713</span></span>|<span data-ttu-id="d3648-112">Tamara Johnston</span><span class="sxs-lookup"><span data-stu-id="d3648-112">Tamara Johnston</span></span>|  
  
 <span data-ttu-id="d3648-113">OrdersTable (untergeordnete Tabelle)</span><span class="sxs-lookup"><span data-stu-id="d3648-113">OrdersTable (child table)</span></span>  
  
|<span data-ttu-id="d3648-114">OrderID</span><span class="sxs-lookup"><span data-stu-id="d3648-114">OrderID</span></span>|<span data-ttu-id="d3648-115">OrderDate</span><span class="sxs-lookup"><span data-stu-id="d3648-115">OrderDate</span></span>|<span data-ttu-id="d3648-116">CustomerID</span><span class="sxs-lookup"><span data-stu-id="d3648-116">CustomerID</span></span>|  
|-------------|---------------|----------------|  
|<span data-ttu-id="d3648-117">903</span><span class="sxs-lookup"><span data-stu-id="d3648-117">903</span></span>|<span data-ttu-id="d3648-118">Donnerstag, 12. Februar 2004</span><span class="sxs-lookup"><span data-stu-id="d3648-118">February 12, 2004</span></span>|<span data-ttu-id="d3648-119">712</span><span class="sxs-lookup"><span data-stu-id="d3648-119">712</span></span>|  
|<span data-ttu-id="d3648-120">904</span><span class="sxs-lookup"><span data-stu-id="d3648-120">904</span></span>|<span data-ttu-id="d3648-121">13. Februar 2004</span><span class="sxs-lookup"><span data-stu-id="d3648-121">February 13, 2004</span></span>|<span data-ttu-id="d3648-122">713</span><span class="sxs-lookup"><span data-stu-id="d3648-122">713</span></span>|  
  
 <span data-ttu-id="d3648-123">In diesem Szenario speichert eine Tabelle, nämlich KundenTabelle, die tatsächlichen Daten, die Sie anzeigen und speichern möchten.</span><span class="sxs-lookup"><span data-stu-id="d3648-123">In this scenario, one table, CustomersTable, stores the actual information you want to display and save.</span></span> <span data-ttu-id="d3648-124">Um aber Platz zu sparen, lässt die Tabelle Daten weg, was für Klarheit sorgt.</span><span class="sxs-lookup"><span data-stu-id="d3648-124">But to save space, the table leaves out data that adds clarity.</span></span> <span data-ttu-id="d3648-125">Die andere Tabelle, BestellungenTabelle, enthält nur erscheinungsbezogene Daten darüber, welche Kunden-ID-Nummer welchem Bestelldatum und welcher Bestell-ID entspricht.</span><span class="sxs-lookup"><span data-stu-id="d3648-125">The other table, OrdersTable, contains only appearance-related information about which customer ID number is equivalent to which order date and order ID.</span></span> <span data-ttu-id="d3648-126">Die Kundennamen werden nicht erwähnt.</span><span class="sxs-lookup"><span data-stu-id="d3648-126">There is no mention of the customers' names.</span></span>  
  
 <span data-ttu-id="d3648-127">Es sind vier wichtige Eigenschaften im [ComboBox-Steuerelement](combobox-control-windows-forms.md) für das Erstellen der Nachschlagetabelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3648-127">Four important properties are set on the [ComboBox Control](combobox-control-windows-forms.md) control to create the lookup table.</span></span>  
  
- <span data-ttu-id="d3648-128">Die Eigenschaft <xref:System.Windows.Forms.ComboBox.DataSource%2A> enthält den Namen der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d3648-128">The <xref:System.Windows.Forms.ComboBox.DataSource%2A> property contains the name of the table.</span></span>  
  
- <span data-ttu-id="d3648-129">Die Eigenschaft <xref:System.Windows.Forms.ListControl.DisplayMember%2A> enthält die Datenspalte dieser Tabelle, die für die Anzeige des Text-Steuerelements (der Name des Kunden) anzeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3648-129">The <xref:System.Windows.Forms.ListControl.DisplayMember%2A> property contains the data column of that table that you want to display for the control text (the customer's name).</span></span>  
  
- <span data-ttu-id="d3648-130">Die Eigenschaft <xref:System.Windows.Forms.ListControl.ValueMember%2A> enthält die Datenspalte der Tabelle mit den gespeicherten Informationen (der ID-Nummer und der übergeordneten Tabelle).</span><span class="sxs-lookup"><span data-stu-id="d3648-130">The <xref:System.Windows.Forms.ListControl.ValueMember%2A> property contains the data column of that table with the stored information (the ID number in the parent table).</span></span>  
  
- <span data-ttu-id="d3648-131">Die Eigenschaft <xref:System.Windows.Forms.ListControl.SelectedValue%2A> liefert den Nachschlagewert für die untergeordnete Tabelle auf Grundlage von <xref:System.Windows.Forms.ListControl.ValueMember%2A>.</span><span class="sxs-lookup"><span data-stu-id="d3648-131">The <xref:System.Windows.Forms.ListControl.SelectedValue%2A> property provides the lookup value for the child table, based on the <xref:System.Windows.Forms.ListControl.ValueMember%2A>.</span></span>  
  
 <span data-ttu-id="d3648-132">Die Verfahren unten zeigen, wie Sie das Formular als Nachschlagetabelle gestalten und Daten mit den Steuerelementen darauf binden.</span><span class="sxs-lookup"><span data-stu-id="d3648-132">The procedures below show you how to lay out your form as a lookup table and bind data to the controls on it.</span></span> <span data-ttu-id="d3648-133">Um die Verfahren erfolgreich durchführen zu können, benötigen Sie eine Datenquelle mit über- und untergeordneten Tabellen, die – wie bereits erwähnt – eine Fremdschlüsselbeziehung haben.</span><span class="sxs-lookup"><span data-stu-id="d3648-133">To successfully complete the procedures, you must have a data source with parent and child tables that have a foreign-key relationship, as mentioned previously.</span></span>  
  
### <a name="to-create-the-user-interface"></a><span data-ttu-id="d3648-134">So erstellen Sie die Benutzeroberfläche</span><span class="sxs-lookup"><span data-stu-id="d3648-134">To create the user interface</span></span>  
  
1. <span data-ttu-id="d3648-135">Ziehen Sie ein-Steuerelement aus der **Toolbox** <xref:System.Windows.Forms.ComboBox> auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="d3648-135">From the **ToolBox**, drag a <xref:System.Windows.Forms.ComboBox> control onto the form.</span></span>  
  
     <span data-ttu-id="d3648-136">Dieses Steuerelement zeigt die Spalte aus der übergeordneten Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="d3648-136">This control will display the column from parent table.</span></span>  
  
2. <span data-ttu-id="d3648-137">Ziehen Sie andere Steuerelemente zur Anzeige von Details aus der untergeordneten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d3648-137">Drag other controls to display details from the child table.</span></span> <span data-ttu-id="d3648-138">Das Format der Daten in der Tabelle bestimmt die Auswahl der Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="d3648-138">The format of the data in the table should determine which controls you choose.</span></span> <span data-ttu-id="d3648-139">Weitere Informationen finden Sie unter [Windows Forms-Steuerelemente nach Funktion](windows-forms-controls-by-function.md).</span><span class="sxs-lookup"><span data-stu-id="d3648-139">For more information, see [Windows Forms Controls by Function](windows-forms-controls-by-function.md).</span></span>  
  
3. <span data-ttu-id="d3648-140">Ziehen Sie ein <xref:System.Windows.Forms.BindingNavigator>-Steuerelement auf das Formular; damit können Sie die Daten in die untergeordnete Tabelle navigieren.</span><span class="sxs-lookup"><span data-stu-id="d3648-140">Drag a <xref:System.Windows.Forms.BindingNavigator> control onto the form; this will allow you to navigate the data in the child table.</span></span>  
  
### <a name="to-connect-to-the-data-and-bind-it-to-controls"></a><span data-ttu-id="d3648-141">So verbinden Sie die Daten und binden diese an die Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="d3648-141">To connect to the data and bind it to controls</span></span>  
  
1. <span data-ttu-id="d3648-142">Wählen Sie die <xref:System.Windows.Forms.ComboBox> und klicken Sie das Symbol Smarttask, sodass das Dialogfeld Smarttask angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d3648-142">Select the <xref:System.Windows.Forms.ComboBox> and click the Smart Task glyph to display the Smart Task dialog box.</span></span>  
  
2. <span data-ttu-id="d3648-143">Wählen Sie **An Daten gebundene Elemente verwenden** aus.</span><span class="sxs-lookup"><span data-stu-id="d3648-143">Select **Use data bound items**.</span></span>  
  
3. <span data-ttu-id="d3648-144">Klicken Sie auf den Pfeil neben dem Dropdownfeld **Datenquelle**.</span><span class="sxs-lookup"><span data-stu-id="d3648-144">Click the arrow next to the **Data Source** drop-down box.</span></span> <span data-ttu-id="d3648-145">Wenn eine Datenquelle bereits für das Projekt oder Formular konfiguriert wurde, wird sie angezeigt; ansonsten führen Sie bitte die folgenden Schritte durch (In diesem Beispiel werden die Kunden- und Bestellungentabellen der Northwind-Beispieldatenbank verwendet, auf die in Klammern verwiesen wird).</span><span class="sxs-lookup"><span data-stu-id="d3648-145">If a data source has previously been configured for the project or form, it will appear; otherwise, complete the following steps (This example uses the Customers and Orders tables of the Northwind sample database and refers to them in parentheses).</span></span>  
  
    1. <span data-ttu-id="d3648-146">Klicken Sie auf **Projektdatenquelle hinzufügen**, um die Daten zu verbinden und die Datenquelle zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="d3648-146">Click **Add Project Data Source** to connect to data and create a data source.</span></span>  
  
    2. <span data-ttu-id="d3648-147">Klicken Sie auf der Startseite des **Assistenten zum Konfigurieren von Datenquellen** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="d3648-147">On the **Data Source Configuration Wizard** welcome page, click **Next**.</span></span>  
  
    3. <span data-ttu-id="d3648-148">Wählen Sie auf der Seite **Datenquellentyp auswählen** die Option **Datenbank** aus.</span><span class="sxs-lookup"><span data-stu-id="d3648-148">Select **Database** on the **Choose a Data Source Type** page.</span></span>  
  
    4. <span data-ttu-id="d3648-149">Wählen Sie auf der Seite **Wählen Sie Ihre Datenverbindung aus** eine Datenverbindung aus der Liste verfügbar Verbindungen aus.</span><span class="sxs-lookup"><span data-stu-id="d3648-149">Select a data connection from the list of available connections on the **Choose Your Data Connection** page.</span></span> <span data-ttu-id="d3648-150">Wenn die gewünschte Datenverbindung nicht verfügbar ist, wählen Sie **Neue Verbindung** aus, und legen Sie eine neue Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="d3648-150">If your desired data connection is not available, select **New Connection** to create a new data connection.</span></span>  
  
    5. <span data-ttu-id="d3648-151">Klicken Sie auf **Ja, Verbindung speichern unter**, um die Verbindungszeichenfolge in der Anwendungskonfigurationsdatei zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d3648-151">Click **Yes, save the connection** to save the connection string in the application configuration file.</span></span>  
  
    6. <span data-ttu-id="d3648-152">Wählen Sie die Datenbankobjekte, die in die Anwendung gebracht werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d3648-152">Select the database objects to bring into your application.</span></span> <span data-ttu-id="d3648-153">In diesem Fall wählen Sie eine übergeordnete und eine untergeordnete Tabelle (z. B. Kunden und Bestellungen) mit einer Fremdschlüsselbeziehung.</span><span class="sxs-lookup"><span data-stu-id="d3648-153">In this case, select a parent table and child table (for example, Customers and Orders) with a foreign key relationship.</span></span>  
  
    7. <span data-ttu-id="d3648-154">Ersetzen Sie den Standardnamen des Datasets falls gewünscht.</span><span class="sxs-lookup"><span data-stu-id="d3648-154">Replace the default dataset name if you want.</span></span>  
  
    8. <span data-ttu-id="d3648-155">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="d3648-155">Click **Finish**.</span></span>  
  
4. <span data-ttu-id="d3648-156">Wählen Sie im Dropdownfeld **Member anzeigen** den Spaltennamen aus (z.B. ContactName), der im Kombinationsfeld angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3648-156">In the **Display Member** drop-down box, select the column name (for example, ContactName) to be displayed in the combo box.</span></span>  
  
5. <span data-ttu-id="d3648-157">Wählen Sie im Dropdownfeld **Wertemember** die Spalte (z.B. CustomerID) für das Durchführen des Nachschlagevorgangs in der untergeordneten Tabelle aus.</span><span class="sxs-lookup"><span data-stu-id="d3648-157">In the **Value Member** drop-down box, select the column (for example, CustomerID) to perform the lookup operation in the child table.</span></span>  
  
6. <span data-ttu-id="d3648-158">Navigieren Sie im Dropdownfeld **Ausgewählter Wert** zu **Projektdatenquellen** und dem eben erstellten Dataset mit den über- und untergeordneten Tabellen.</span><span class="sxs-lookup"><span data-stu-id="d3648-158">In the **Selected Value** drop-down box, navigate to **Project Data Sources** and the dataset you just created that contains the parent and child tables.</span></span> <span data-ttu-id="d3648-159">Wählen Sie dieselbe Eigenschaft der untergeordneten Tabelle, die ein Wertemember der übergeordneten Tabelle ist (z. B. Orders.CustomerID).</span><span class="sxs-lookup"><span data-stu-id="d3648-159">Select the same property of the child table that is the Value Member of the parent table (for example, Orders.CustomerID).</span></span> <span data-ttu-id="d3648-160">Das entsprechende Datenset <xref:System.Windows.Forms.BindingSource> und die Tabelleadapterkomponenten werden erstellt und dem Formular hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d3648-160">The appropriate <xref:System.Windows.Forms.BindingSource> , data set, and table adapter components will be created and added to the form.</span></span>  
  
7. <span data-ttu-id="d3648-161">Binden Sie das Steuerelement <xref:System.Windows.Forms.BindingNavigator> an die untergeordnete Tabelle <xref:System.Windows.Forms.BindingSource> (z. B. `OrdersBindingSource`).</span><span class="sxs-lookup"><span data-stu-id="d3648-161">Bind the <xref:System.Windows.Forms.BindingNavigator> control to the <xref:System.Windows.Forms.BindingSource> of the child table (for example, `OrdersBindingSource`).</span></span>  
  
8. <span data-ttu-id="d3648-162">Binden Sie die Steuerelement außer <xref:System.Windows.Forms.ComboBox> und <xref:System.Windows.Forms.BindingNavigator> an das Feld "Details" aus der <xref:System.Windows.Forms.BindingSource> der untergeordneten Tabelle (z. B. `OrdersBindingSource`), die Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="d3648-162">Bind the controls other than the <xref:System.Windows.Forms.ComboBox> and <xref:System.Windows.Forms.BindingNavigator> control to the details fields from the child table's <xref:System.Windows.Forms.BindingSource> (for example, `OrdersBindingSource`) that you want to display.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d3648-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3648-163">See also</span></span>

- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="d3648-164">BindingSource-Komponente</span><span class="sxs-lookup"><span data-stu-id="d3648-164">BindingSource Component</span></span>](bindingsource-component.md)
- [<span data-ttu-id="d3648-165">ComboBox-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d3648-165">ComboBox Control</span></span>](combobox-control-windows-forms.md)
- [<span data-ttu-id="d3648-166">Binden von Steuerelementen an Daten in Visual Studio</span><span class="sxs-lookup"><span data-stu-id="d3648-166">Bind controls to data in Visual Studio</span></span>](/visualstudio/data-tools/bind-controls-to-data-in-visual-studio)
