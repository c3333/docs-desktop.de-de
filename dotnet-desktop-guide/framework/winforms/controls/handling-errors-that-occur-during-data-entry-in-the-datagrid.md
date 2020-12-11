---
title: 'Exemplarische Vorgehensweise: Behandeln von Fehlern, die während der Dateneingabe im DataGridView-Steuerelement auftreten'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- error handling [Windows Forms], dataGridView control
- data grids [Windows Forms], error handling
- DataGridView control [Windows Forms], error handling
- data entry [Windows Forms], error handling
- error handling [Windows Forms], data entry
- walkthroughs [Windows Forms], DataGridView control
ms.assetid: 30a68b85-d3af-4946-83c1-1e2d010d0511
ms.openlocfilehash: d65dd038ddc276ec09a1db3af4f14fc87fec56f2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975984"
---
# <a name="walkthrough-handling-errors-that-occur-during-data-entry-in-the-windows-forms-datagridview-control"></a><span data-ttu-id="d0218-102">Exemplarische Vorgehensweise: Behandeln von Fehlern, die während der Dateneingabe im DataGridView-Steuerelement in Windows Forms auftreten</span><span class="sxs-lookup"><span data-stu-id="d0218-102">Walkthrough: Handling Errors that Occur During Data Entry in the Windows Forms DataGridView Control</span></span>

<span data-ttu-id="d0218-103">Das Behandeln von Fehlern aus dem zugrunde liegenden Datenspeicher ist ein erforderliches Feature für eine Dateneingabe Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d0218-103">Handling errors from the underlying data store is a required feature for a data-entry application.</span></span> <span data-ttu-id="d0218-104">Das Windows Forms-Steuerelement vereinfacht <xref:System.Windows.Forms.DataGridView> dies durch das verfügbar machen des- <xref:System.Windows.Forms.DataGridView.DataError> Ereignisses, das ausgelöst wird, wenn der Datenspeicher eine Einschränkungs Verletzung oder eine unterbrochene Geschäftsregel erkennt.</span><span class="sxs-lookup"><span data-stu-id="d0218-104">The Windows Forms <xref:System.Windows.Forms.DataGridView> control makes this easy by exposing the <xref:System.Windows.Forms.DataGridView.DataError> event, which is raised when the data store detects a constraint violation or a broken business rule.</span></span>

<span data-ttu-id="d0218-105">In dieser exemplarischen Vorgehensweise rufen Sie Zeilen aus der `Customers` -Tabelle in der Northwind-Beispieldatenbank ab und zeigen Sie in einem-Steuerelement an <xref:System.Windows.Forms.DataGridView> .</span><span class="sxs-lookup"><span data-stu-id="d0218-105">In this walkthrough, you will retrieve rows from the `Customers` table in the Northwind sample database and display them in a <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="d0218-106">Wenn ein doppelter `CustomerID` Wert in einer neuen Zeile oder einer bearbeiteten vorhandenen Zeile erkannt wird, tritt das- <xref:System.Windows.Forms.DataGridView.DataError> Ereignis auf, das durch Anzeigen einer behandelt wird, die <xref:System.Windows.Forms.MessageBox> die Ausnahme beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d0218-106">When a duplicate `CustomerID` value is detected in a new row or an edited existing row, the <xref:System.Windows.Forms.DataGridView.DataError> event will occur, which will be handled by displaying a <xref:System.Windows.Forms.MessageBox> that describes the exception.</span></span>

<span data-ttu-id="d0218-107">Informationen zum Kopieren des Codes in diesem Thema als einzelne Auflistung finden Sie unter Gewusst [wie: Behandeln von Fehlern, die während der Dateneingabe im Windows Forms DataGridView-Steuerelement auftreten](handle-errors-that-occur-during-data-entry-in-the-datagrid.md).</span><span class="sxs-lookup"><span data-stu-id="d0218-107">To copy the code in this topic as a single listing, see [How to: Handle Errors That Occur During Data Entry in the Windows Forms DataGridView Control](handle-errors-that-occur-during-data-entry-in-the-datagrid.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d0218-108">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="d0218-108">Prerequisites</span></span>

<span data-ttu-id="d0218-109">Für die Durchführung dieser exemplarischen Vorgehensweise benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d0218-109">In order to complete this walkthrough, you will need:</span></span>

- <span data-ttu-id="d0218-110">Zugriff auf einen Server mit der Beispieldatenbank Northwind SQL Server.</span><span class="sxs-lookup"><span data-stu-id="d0218-110">Access to a server that has the Northwind SQL Server sample database.</span></span>

## <a name="creating-the-form"></a><span data-ttu-id="d0218-111">Erstellen des Formulars</span><span class="sxs-lookup"><span data-stu-id="d0218-111">Creating the Form</span></span>

#### <a name="to-handle-data-entry-errors-in-the-datagridview-control"></a><span data-ttu-id="d0218-112">So verarbeiten Sie Dateneingabe Fehler im DataGridView-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="d0218-112">To handle data-entry errors in the DataGridView control</span></span>

1. <span data-ttu-id="d0218-113">Erstellen Sie eine Klasse, die von abgeleitet ist <xref:System.Windows.Forms.Form> und ein <xref:System.Windows.Forms.DataGridView> -Steuerelement und eine- <xref:System.Windows.Forms.BindingSource> Komponente enthält.</span><span class="sxs-lookup"><span data-stu-id="d0218-113">Create a class that derives from <xref:System.Windows.Forms.Form> and contains a <xref:System.Windows.Forms.DataGridView> control and a <xref:System.Windows.Forms.BindingSource> component.</span></span>

    <span data-ttu-id="d0218-114">Im folgenden Codebeispiel wird die grundlegende Initialisierung und eine-Methode bereitstellt `Main` .</span><span class="sxs-lookup"><span data-stu-id="d0218-114">The following code example provides basic initialization and includes a `Main` method.</span></span>

    [!code-csharp[System.Windows.Forms.DataGridView.DataError#01](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#01)]
    [!code-vb[System.Windows.Forms.DataGridView.DataError#01](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#01)]
    [!code-csharp[System.Windows.Forms.DataGridView.DataError#02](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#02)]
    [!code-vb[System.Windows.Forms.DataGridView.DataError#02](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#02)]

2. <span data-ttu-id="d0218-115">Implementieren Sie eine Methode in der Klassendefinition Ihres Formulars, um die Details der Verbindungs Herstellung mit der Datenbank zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d0218-115">Implement a method in your form's class definition for handling the details of connecting to the database.</span></span>

    <span data-ttu-id="d0218-116">Dieses Codebeispiel verwendet eine- `GetData` Methode, die ein aufgefülltes Objekt zurückgibt <xref:System.Data.DataTable> .</span><span class="sxs-lookup"><span data-stu-id="d0218-116">This code example uses a `GetData` method that returns a populated <xref:System.Data.DataTable> object.</span></span> <span data-ttu-id="d0218-117">Stellen Sie sicher, dass Sie die `connectionString` Variable auf einen Wert festlegen, der für Ihre Datenbank geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="d0218-117">Be sure that you set the `connectionString` variable to a value that is appropriate for your database.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="d0218-118">Das Speichern vertraulicher Informationen (z. B. eines Kennworts) innerhalb der Verbindungszeichenfolge kann die Sicherheit einer Anwendung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="d0218-118">Storing sensitive information, such as a password, within the connection string can affect the security of your application.</span></span> <span data-ttu-id="d0218-119">Der Zugriff auf eine Datenbank lässt sich mithilfe der Windows-Authentifizierung (wird auch als integrierte Sicherheit bezeichnet) sicherer steuern.</span><span class="sxs-lookup"><span data-stu-id="d0218-119">Using Windows Authentication (also known as integrated security) is a more secure way to control access to a database.</span></span> <span data-ttu-id="d0218-120">Weitere Informationen finden Sie unter [Protecting Connection Information (Schützen von Verbindungsinformationen)](/dotnet/framework/data/adonet/protecting-connection-information).</span><span class="sxs-lookup"><span data-stu-id="d0218-120">For more information, see [Protecting Connection Information](/dotnet/framework/data/adonet/protecting-connection-information).</span></span>

    [!code-csharp[System.Windows.Forms.DataGridView.DataError#30](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#30)]
    [!code-vb[System.Windows.Forms.DataGridView.DataError#30](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#30)]

3. <span data-ttu-id="d0218-121">Implementieren Sie einen Handler für das- <xref:System.Windows.Forms.Form.Load> Ereignis des Formulars, das und initialisiert, <xref:System.Windows.Forms.DataGridView> <xref:System.Windows.Forms.BindingSource> und richtet die Datenbindung ein.</span><span class="sxs-lookup"><span data-stu-id="d0218-121">Implement a handler for your form's <xref:System.Windows.Forms.Form.Load> event that initializes the <xref:System.Windows.Forms.DataGridView> and <xref:System.Windows.Forms.BindingSource> and sets up the data binding.</span></span>

    [!code-csharp[System.Windows.Forms.DataGridView.DataError#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#10)]
    [!code-vb[System.Windows.Forms.DataGridView.DataError#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#10)]

4. <span data-ttu-id="d0218-122">Behandeln Sie das- <xref:System.Windows.Forms.DataGridView.DataError> Ereignis auf dem <xref:System.Windows.Forms.DataGridView> .</span><span class="sxs-lookup"><span data-stu-id="d0218-122">Handle the <xref:System.Windows.Forms.DataGridView.DataError> event on the <xref:System.Windows.Forms.DataGridView>.</span></span>

    <span data-ttu-id="d0218-123">Wenn der Kontext für den Fehler ein Commitvorgang ist, wird der Fehler in einem angezeigt <xref:System.Windows.Forms.MessageBox> .</span><span class="sxs-lookup"><span data-stu-id="d0218-123">If the context for the error is a commit operation, display the error in a <xref:System.Windows.Forms.MessageBox>.</span></span>

    [!code-csharp[System.Windows.Forms.DataGridView.DataError#20](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/CS/errorhandling.cs#20)]
    [!code-vb[System.Windows.Forms.DataGridView.DataError#20](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridView.DataError/VB/errorhandling.vb#20)]

## <a name="testing-the-application"></a><span data-ttu-id="d0218-124">Testen der Anwendung</span><span class="sxs-lookup"><span data-stu-id="d0218-124">Testing the Application</span></span>

<span data-ttu-id="d0218-125">Sie können das Formular jetzt testen, um sicherzustellen, dass das Verhalten wie erwartet ausfällt.</span><span class="sxs-lookup"><span data-stu-id="d0218-125">You can now test the form to make sure it behaves as expected.</span></span>

#### <a name="to-test-the-form"></a><span data-ttu-id="d0218-126">So testen Sie das Formular</span><span class="sxs-lookup"><span data-stu-id="d0218-126">To test the form</span></span>

- <span data-ttu-id="d0218-127">Drücken Sie F5, um die Anwendung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d0218-127">Press F5 to run the application.</span></span>

  <span data-ttu-id="d0218-128">Sie sehen ein Steuerelement, <xref:System.Windows.Forms.DataGridView> das mit Daten aus der Customers-Tabelle gefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="d0218-128">You will see a <xref:System.Windows.Forms.DataGridView> control filled with data from the Customers table.</span></span> <span data-ttu-id="d0218-129">Wenn Sie einen doppelten Wert für eingeben `CustomerID` und den Bearbeitungs Commit durchführen, wird der Zellwert automatisch wieder hergestellt, und es wird ein <xref:System.Windows.Forms.MessageBox> angezeigt, in dem der Dateneingabe Fehler angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="d0218-129">If you enter a duplicate value for `CustomerID` and commit the edit, the cell value will revert automatically and you will see a <xref:System.Windows.Forms.MessageBox> that displays the data entry error.</span></span>

## <a name="next-steps"></a><span data-ttu-id="d0218-130">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="d0218-130">Next Steps</span></span>

<span data-ttu-id="d0218-131">Diese Anwendung enthält grundlegende Kenntnisse über die <xref:System.Windows.Forms.DataGridView> Funktionen des-Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="d0218-131">This application gives you a basic understanding of the <xref:System.Windows.Forms.DataGridView> control's capabilities.</span></span> <span data-ttu-id="d0218-132">Sie können die Darstellung und das Verhalten des <xref:System.Windows.Forms.DataGridView> Steuer Elements auf verschiedene Weise anpassen:</span><span class="sxs-lookup"><span data-stu-id="d0218-132">You can customize the appearance and behavior of the <xref:System.Windows.Forms.DataGridView> control in several ways:</span></span>

- <span data-ttu-id="d0218-133">Ändern von Rahmen-und Header Stilen.</span><span class="sxs-lookup"><span data-stu-id="d0218-133">Change border and header styles.</span></span> <span data-ttu-id="d0218-134">Weitere Informationen finden Sie unter Gewusst [wie: Ändern der Rahmen-und Rasterlinien Stile im Windows Forms DataGridView-Steuer](change-the-border-and-gridline-styles-in-the-datagrid.md)Element.</span><span class="sxs-lookup"><span data-stu-id="d0218-134">For more information, see [How to: Change the Border and Gridline Styles in the Windows Forms DataGridView Control](change-the-border-and-gridline-styles-in-the-datagrid.md).</span></span>

- <span data-ttu-id="d0218-135">Aktivieren oder Einschränken der Benutzereingaben für das <xref:System.Windows.Forms.DataGridView> Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d0218-135">Enable or restrict user input to the <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="d0218-136">Weitere Informationen finden Sie unter Gewusst [wie: verhindern des Hinzufügens und Löschens von Zeilen im Windows Forms DataGridView-Steuer](prevent-row-addition-and-deletion-datagridview.md)Element und Gewusst [wie: Erstellen von Spalten Read-Only im Windows Forms DataGridView-Steuer](how-to-make-columns-read-only-in-the-windows-forms-datagridview-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="d0218-136">For more information, see [How to: Prevent Row Addition and Deletion in the Windows Forms DataGridView Control](prevent-row-addition-and-deletion-datagridview.md), and [How to: Make Columns Read-Only in the Windows Forms DataGridView Control](how-to-make-columns-read-only-in-the-windows-forms-datagridview-control.md).</span></span>

- <span data-ttu-id="d0218-137">Überprüfen Sie die Benutzereingaben für das <xref:System.Windows.Forms.DataGridView> Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="d0218-137">Validate user input to the <xref:System.Windows.Forms.DataGridView> control.</span></span> <span data-ttu-id="d0218-138">Weitere Informationen finden Sie unter Exemplarische Vorgehensweise [: Validieren von Daten im Windows Forms DataGridView-Steuer](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="d0218-138">For more information, see [Walkthrough: Validating Data in the Windows Forms DataGridView Control](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md).</span></span>

- <span data-ttu-id="d0218-139">Verarbeiten Sie sehr große Datasets im virtuellen Modus.</span><span class="sxs-lookup"><span data-stu-id="d0218-139">Handle very large data sets using virtual mode.</span></span> <span data-ttu-id="d0218-140">Weitere Informationen finden Sie unter Exemplarische [Vorgehensweise: Implementieren des virtuellen Modus im Windows Forms DataGridView-Steuer](implementing-virtual-mode-wf-datagridview-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="d0218-140">For more information, see [Walkthrough: Implementing Virtual Mode in the Windows Forms DataGridView Control](implementing-virtual-mode-wf-datagridview-control.md).</span></span>

- <span data-ttu-id="d0218-141">Passen Sie die Darstellung von Zellen an.</span><span class="sxs-lookup"><span data-stu-id="d0218-141">Customize the appearance of cells.</span></span> <span data-ttu-id="d0218-142">Weitere Informationen finden Sie unter Gewusst [wie: Anpassen der Darstellung von Zellen im Windows Forms DataGridView-Steuer](customize-the-appearance-of-cells-in-the-datagrid.md) Element und Gewusst [wie: Festlegen von Standardzellen Formaten für das Windows Forms DataGridView-Steuer](how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control.md)Element.</span><span class="sxs-lookup"><span data-stu-id="d0218-142">For more information, see [How to: Customize the Appearance of Cells in the Windows Forms DataGridView Control](customize-the-appearance-of-cells-in-the-datagrid.md) and [How to: Set Default Cell Styles for the Windows Forms DataGridView Control](how-to-set-default-cell-styles-for-the-windows-forms-datagridview-control.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="d0218-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0218-143">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.BindingSource>
- [<span data-ttu-id="d0218-144">Dateneingabe im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d0218-144">Data Entry in the Windows Forms DataGridView Control</span></span>](data-entry-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="d0218-145">Vorgehensweise: Behandeln von Fehlern, die während der Dateneingabe im DataGridView-Steuerelement in Windows Forms auftreten</span><span class="sxs-lookup"><span data-stu-id="d0218-145">How to: Handle Errors That Occur During Data Entry in the Windows Forms DataGridView Control</span></span>](handle-errors-that-occur-during-data-entry-in-the-datagrid.md)
- [<span data-ttu-id="d0218-146">Exemplarische Vorgehensweise: Validieren von Daten im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d0218-146">Walkthrough: Validating Data in the Windows Forms DataGridView Control</span></span>](walkthrough-validating-data-in-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="d0218-147">Schützen von Verbindungsinformationen</span><span class="sxs-lookup"><span data-stu-id="d0218-147">Protecting Connection Information</span></span>](/dotnet/framework/data/adonet/protecting-connection-information)
