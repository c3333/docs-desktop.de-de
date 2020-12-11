---
title: Sortieren und Filtern von ADO.NET-Daten mit der BindingSource-Komponente
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sorting data
- data sorting [Windows Forms], ADO.NET
- data [Windows Forms], filtering
- BindingSource component [Windows Forms], sorting and filtering data
- filtering [Windows Forms], ADO.NET
- data [Windows Forms], sorting
- ADO.NET [Windows Forms]
ms.assetid: 6c206daf-d706-4602-9dbe-435343052063
ms.openlocfilehash: 404e67f1eeed240a171cb1cfef9094a746c3cecb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972328"
---
# <a name="how-to-sort-and-filter-adonet-data-with-the-windows-forms-bindingsource-component"></a><span data-ttu-id="c5f67-102">Vorgehensweise: Sortieren und Filtern von ADO.NET-Daten mit der BindingSource-Komponente in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c5f67-102">How to: Sort and Filter ADO.NET Data with the Windows Forms BindingSource Component</span></span>

<span data-ttu-id="c5f67-103">Mithilfe der-Eigenschaft und der-Eigenschaft können Sie die Sortier-und Filterfunktion des Steuer Elements verfügbar machen <xref:System.Windows.Forms.BindingSource> <xref:System.Windows.Forms.BindingSource.Sort%2A> <xref:System.Windows.Forms.BindingSource.Filter%2A> .</span><span class="sxs-lookup"><span data-stu-id="c5f67-103">You can expose the sorting and filtering capability of <xref:System.Windows.Forms.BindingSource> control through the <xref:System.Windows.Forms.BindingSource.Sort%2A> and <xref:System.Windows.Forms.BindingSource.Filter%2A> properties.</span></span> <span data-ttu-id="c5f67-104">Sie können eine einfache Sortierung anwenden, wenn die zugrunde liegende Datenquelle eine ist <xref:System.ComponentModel.IBindingList> , und Sie können Filter und erweiterte Sortierung anwenden, wenn die Datenquelle eine ist <xref:System.ComponentModel.IBindingListView> .</span><span class="sxs-lookup"><span data-stu-id="c5f67-104">You can apply simple sorting when the underlying data source is an <xref:System.ComponentModel.IBindingList>, and you can apply filtering and advanced sorting when the data source is an <xref:System.ComponentModel.IBindingListView>.</span></span> <span data-ttu-id="c5f67-105">Die- <xref:System.Windows.Forms.BindingSource.Sort%2A> Eigenschaft erfordert die ADO.NET-Standard Syntax: eine Zeichenfolge, die den Namen einer Datenspalte in der Datenquelle darstellt, gefolgt von `ASC` oder `DESC` , um anzugeben, ob die Liste in aufsteigender oder absteigender Reihenfolge sortiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5f67-105">The <xref:System.Windows.Forms.BindingSource.Sort%2A> property requires standard ADO.NET syntax: a string representing the name of a column of data in the data source followed by `ASC` or `DESC` to indicate whether the list should be sorted in ascending or descending order.</span></span> <span data-ttu-id="c5f67-106">Sie können eine erweiterte Sortierung oder eine Sortierung mit mehreren Spalten festlegen, indem Sie jede Spalte durch ein Komma Trennzeichen trennen.</span><span class="sxs-lookup"><span data-stu-id="c5f67-106">You can set advanced sorting or multiple-column sorting by separating each column with a comma separator.</span></span> <span data-ttu-id="c5f67-107">Die- <xref:System.Windows.Forms.BindingSource.Filter%2A> Eigenschaft nimmt einen Zeichen folgen Ausdruck an.</span><span class="sxs-lookup"><span data-stu-id="c5f67-107">The <xref:System.Windows.Forms.BindingSource.Filter%2A> property takes a string expression.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="c5f67-108">Das Speichern vertraulicher Informationen (z. B. eines Kennworts) innerhalb der Verbindungszeichenfolge kann die Sicherheit einer Anwendung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="c5f67-108">Storing sensitive information, such as a password, within the connection string can affect the security of your application.</span></span> <span data-ttu-id="c5f67-109">Der Zugriff auf eine Datenbank lässt sich mithilfe der Windows-Authentifizierung (wird auch als integrierte Sicherheit bezeichnet) sicherer steuern.</span><span class="sxs-lookup"><span data-stu-id="c5f67-109">Using Windows Authentication (also known as integrated security) is a more secure way to control access to a database.</span></span> <span data-ttu-id="c5f67-110">Weitere Informationen finden Sie unter [Protecting Connection Information (Schützen von Verbindungsinformationen)](/dotnet/framework/data/adonet/protecting-connection-information).</span><span class="sxs-lookup"><span data-stu-id="c5f67-110">For more information, see [Protecting Connection Information](/dotnet/framework/data/adonet/protecting-connection-information).</span></span>  
  
### <a name="to-filter-data-with-the-bindingsource"></a><span data-ttu-id="c5f67-111">So filtern Sie Daten mit der BindingSource</span><span class="sxs-lookup"><span data-stu-id="c5f67-111">To filter data with the BindingSource</span></span>  
  
- <span data-ttu-id="c5f67-112">Legen Sie die- <xref:System.Windows.Forms.BindingSource.Filter%2A> Eigenschaft auf den gewünschten Ausdruck fest.</span><span class="sxs-lookup"><span data-stu-id="c5f67-112">Set the <xref:System.Windows.Forms.BindingSource.Filter%2A> property to expression that you want.</span></span>  
  
     <span data-ttu-id="c5f67-113">Im folgenden Codebeispiel ist der Ausdruck ein Spaltenname, gefolgt von dem Wert, den Sie für die Spalte benötigen.</span><span class="sxs-lookup"><span data-stu-id="c5f67-113">In the following code example, the expression is a column name followed by value that you want for the column.</span></span>  
  
 [!code-csharp[System.Windows.Forms.DataConnectorFilterAndSort#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/CS/form1.cs#11)]
 [!code-vb[System.Windows.Forms.DataConnectorFilterAndSort#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/VB/form1.vb#11)]  
  
### <a name="to-sort-data-with-the-bindingsource"></a><span data-ttu-id="c5f67-114">So sortieren Sie Daten mit der BindingSource</span><span class="sxs-lookup"><span data-stu-id="c5f67-114">To sort data with the BindingSource</span></span>  
  
1. <span data-ttu-id="c5f67-115">Legen Sie die- <xref:System.Windows.Forms.BindingSource.Sort%2A> Eigenschaft auf den Spaltennamen fest, den Sie folgen möchten, `ASC` oder `DESC` , um den aufsteigenden oder absteigenden Auftrag anzugeben.</span><span class="sxs-lookup"><span data-stu-id="c5f67-115">Set the <xref:System.Windows.Forms.BindingSource.Sort%2A> property to the column name that you want followed by `ASC` or `DESC` to indicate the ascending or descending order.</span></span>  
  
2. <span data-ttu-id="c5f67-116">Trennen Sie mehrere Spalten durch ein Komma.</span><span class="sxs-lookup"><span data-stu-id="c5f67-116">Separate multiple columns with a comma.</span></span>  
  
 [!code-csharp[System.Windows.Forms.DataConnectorFilterAndSort#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/CS/form1.cs#12)]
 [!code-vb[System.Windows.Forms.DataConnectorFilterAndSort#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/VB/form1.vb#12)]  
  
## <a name="example"></a><span data-ttu-id="c5f67-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c5f67-117">Example</span></span>  

 <span data-ttu-id="c5f67-118">Im folgenden Codebeispiel werden Daten aus der Customers-Tabelle der Beispieldatenbank Northwind in ein <xref:System.Windows.Forms.DataGridView> -Steuerelement geladen, und die angezeigten Daten werden gefiltert und sortiert.</span><span class="sxs-lookup"><span data-stu-id="c5f67-118">The following code example loads data from the Customers table of the Northwind sample database into a <xref:System.Windows.Forms.DataGridView> control, and filters and sorts the displayed data.</span></span>  
  
 [!code-csharp[System.Windows.Forms.DataConnectorFilterAndSort#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataConnectorFilterAndSort#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c5f67-119">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="c5f67-119">Compiling the Code</span></span>  

 <span data-ttu-id="c5f67-120">Um dieses Beispiel auszuführen, fügen Sie den Code in ein Formular ein, das ein mit dem Namen <xref:System.Windows.Forms.BindingSource> `BindingSource1` und ein mit dem <xref:System.Windows.Forms.DataGridView> Namen enthält `dataGridView1` .</span><span class="sxs-lookup"><span data-stu-id="c5f67-120">To run this example, paste the code into a form that contains a <xref:System.Windows.Forms.BindingSource> named `BindingSource1` and a <xref:System.Windows.Forms.DataGridView> named `dataGridView1`.</span></span> <span data-ttu-id="c5f67-121">Behandeln Sie das <xref:System.Windows.Forms.Form.Load> -Ereignis für das Formular, und nennen Sie es `InitializeSortedFilteredBindingSource` in der Load-Ereignishandlermethode</span><span class="sxs-lookup"><span data-stu-id="c5f67-121">Handle the <xref:System.Windows.Forms.Form.Load> event for the form and call `InitializeSortedFilteredBindingSource` in the load event handler method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c5f67-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5f67-122">See also</span></span>

- <xref:System.Windows.Forms.BindingSource.Sort%2A>
- <xref:System.Windows.Forms.BindingSource.Filter%2A>
- <span data-ttu-id="c5f67-123">[Gewusst wie: Installieren von Beispieldatenbanken](/previous-versions/visualstudio/visual-studio-2013/8b6y4c7s(v=vs.120))</span><span class="sxs-lookup"><span data-stu-id="c5f67-123">[How to: Install Sample Databases](/previous-versions/visualstudio/visual-studio-2013/8b6y4c7s(v=vs.120))</span></span>
- [<span data-ttu-id="c5f67-124">BindingSource-Komponente</span><span class="sxs-lookup"><span data-stu-id="c5f67-124">BindingSource Component</span></span>](bindingsource-component.md)
