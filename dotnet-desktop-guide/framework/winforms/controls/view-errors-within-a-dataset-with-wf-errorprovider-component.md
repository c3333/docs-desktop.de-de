---
title: Anzeigen von Fehlern innerhalb eines Datasets mit der ErrorProvider-Komponente
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- errors [Windows Forms], dataset errors
- error messages [Windows Forms], viewing in datasets
- ErrorProvider component [Windows Forms], dataset errors
ms.assetid: cbae023f-d651-4210-bdea-bcc5f037e321
ms.openlocfilehash: 8c2155bf288db89b5d53567738fd399b915d50b6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977203"
---
# <a name="how-to-view-errors-within-a-dataset-with-the-windows-forms-errorprovider-component"></a><span data-ttu-id="be7ca-102">Vorgehensweise: Anzeigen von Fehlern innerhalb eines Datasets mit der ErrorProvider-Komponente in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="be7ca-102">How to: View Errors Within a DataSet with the Windows Forms ErrorProvider Component</span></span>
<span data-ttu-id="be7ca-103">Sie können die Windows Forms <xref:System.Windows.Forms.ErrorProvider> Komponente verwenden, um Spalten Fehler in einem DataSet oder einer anderen Datenquelle anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="be7ca-103">You can use the Windows Forms <xref:System.Windows.Forms.ErrorProvider> component to view column errors within a dataset or other data source.</span></span> <span data-ttu-id="be7ca-104">Damit eine- <xref:System.Windows.Forms.ErrorProvider> Komponente Datenfehler in einem Formular anzeigt, muss Sie nicht direkt einem-Steuerelement zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="be7ca-104">For an <xref:System.Windows.Forms.ErrorProvider> component to display data errors on a form, it does not have to be directly associated with a control.</span></span> <span data-ttu-id="be7ca-105">Nachdem Sie an eine Datenquelle gebunden wurde, kann Sie ein Fehler Symbol neben jedem Steuerelement anzeigen, das an dieselbe Datenquelle gebunden ist.</span><span class="sxs-lookup"><span data-stu-id="be7ca-105">Once it is bound to a data source, it can display an error icon next to any control that is bound to the same data source.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="be7ca-106">Wenn Sie die-und-Eigenschaften des Fehler Anbieters <xref:System.Windows.Forms.ErrorProvider.DataSource%2A> <xref:System.Windows.Forms.ErrorProvider.DataMember%2A> zur Laufzeit ändern, sollten Sie die-Methode verwenden, <xref:System.Windows.Forms.ErrorProvider.BindToDataAndErrors%2A> um Konflikte zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="be7ca-106">If you change the error provider's <xref:System.Windows.Forms.ErrorProvider.DataSource%2A> and <xref:System.Windows.Forms.ErrorProvider.DataMember%2A> properties at run time, you should use the <xref:System.Windows.Forms.ErrorProvider.BindToDataAndErrors%2A> method to avoid conflicts.</span></span>  
  
### <a name="to-display-data-errors"></a><span data-ttu-id="be7ca-107">So zeigen Sie Datenfehler an</span><span class="sxs-lookup"><span data-stu-id="be7ca-107">To display data errors</span></span>  
  
1. <span data-ttu-id="be7ca-108">Binden Sie die Komponente an eine bestimmte Spalte innerhalb einer Datentabelle.</span><span class="sxs-lookup"><span data-stu-id="be7ca-108">Bind the component to a specific column within a data table.</span></span>  
  
    ```vb  
    ' Assumes existence of DataSet1, DataTable1  
    TextBox1.DataBindings.Add("Text", DataSet1, "Customers.Name")  
    ErrorProvider1.DataSource = DataSet1  
    ErrorProvider1.DataMember = "Customers"  
    ```  
  
    ```csharp  
    // Assumes existence of DataSet1, DataTable1  
    textBox1.DataBindings.Add("Text", DataSet1, "Customers.Name");  
    errorProvider1.DataSource = DataSet1;  
    errorProvider1.DataMember = "Customers";  
    ```  
  
2. <span data-ttu-id="be7ca-109">Legen Sie die- <xref:System.Windows.Forms.ErrorProvider.ContainerControl%2A> Eigenschaft auf das Formular fest.</span><span class="sxs-lookup"><span data-stu-id="be7ca-109">Set the <xref:System.Windows.Forms.ErrorProvider.ContainerControl%2A> property to the form.</span></span>  
  
    ```vb  
    ErrorProvider1.ContainerControl = Me  
    ```  
  
    ```csharp  
    errorProvider1.ContainerControl = this;  
    ```  
  
3. <span data-ttu-id="be7ca-110">Legen Sie die Position des aktuellen Datensatzes auf eine Zeile fest, die einen Spalten Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="be7ca-110">Set the position of the current record to a row that contains a column error.</span></span>  
  
    ```vb  
    DataTable1.Rows(5).SetColumnError("Name", "Bad data in this row.")  
    Me.BindingContext(DataTable1).Position = 5  
    ```  
  
    ```csharp  
    DataTable1.Rows[5].SetColumnError("Name", "Bad data in this row.");  
    this.BindingContext [DataTable1].Position = 5;  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="be7ca-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be7ca-111">See also</span></span>

- [<span data-ttu-id="be7ca-112">Übersicht über die ErrorProvider-Komponente</span><span class="sxs-lookup"><span data-stu-id="be7ca-112">ErrorProvider Component Overview</span></span>](errorprovider-component-overview-windows-forms.md)
- [<span data-ttu-id="be7ca-113">Vorgehensweise: Anzeigen von Fehlersymbolen für die Formularvalidierung mit der ErrorProvider-Komponente in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="be7ca-113">How to: Display Error Icons for Form Validation with the Windows Forms ErrorProvider Component</span></span>](display-error-icons-for-form-validation-with-wf-errorprovider.md)
