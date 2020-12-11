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
# <a name="how-to-view-errors-within-a-dataset-with-the-windows-forms-errorprovider-component"></a>Vorgehensweise: Anzeigen von Fehlern innerhalb eines Datasets mit der ErrorProvider-Komponente in Windows Forms
Sie können die Windows Forms <xref:System.Windows.Forms.ErrorProvider> Komponente verwenden, um Spalten Fehler in einem DataSet oder einer anderen Datenquelle anzuzeigen. Damit eine- <xref:System.Windows.Forms.ErrorProvider> Komponente Datenfehler in einem Formular anzeigt, muss Sie nicht direkt einem-Steuerelement zugeordnet werden. Nachdem Sie an eine Datenquelle gebunden wurde, kann Sie ein Fehler Symbol neben jedem Steuerelement anzeigen, das an dieselbe Datenquelle gebunden ist.  
  
> [!NOTE]
> Wenn Sie die-und-Eigenschaften des Fehler Anbieters <xref:System.Windows.Forms.ErrorProvider.DataSource%2A> <xref:System.Windows.Forms.ErrorProvider.DataMember%2A> zur Laufzeit ändern, sollten Sie die-Methode verwenden, <xref:System.Windows.Forms.ErrorProvider.BindToDataAndErrors%2A> um Konflikte zu vermeiden.  
  
### <a name="to-display-data-errors"></a>So zeigen Sie Datenfehler an  
  
1. Binden Sie die Komponente an eine bestimmte Spalte innerhalb einer Datentabelle.  
  
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
  
2. Legen Sie die- <xref:System.Windows.Forms.ErrorProvider.ContainerControl%2A> Eigenschaft auf das Formular fest.  
  
    ```vb  
    ErrorProvider1.ContainerControl = Me  
    ```  
  
    ```csharp  
    errorProvider1.ContainerControl = this;  
    ```  
  
3. Legen Sie die Position des aktuellen Datensatzes auf eine Zeile fest, die einen Spalten Fehler enthält.  
  
    ```vb  
    DataTable1.Rows(5).SetColumnError("Name", "Bad data in this row.")  
    Me.BindingContext(DataTable1).Position = 5  
    ```  
  
    ```csharp  
    DataTable1.Rows[5].SetColumnError("Name", "Bad data in this row.");  
    this.BindingContext [DataTable1].Position = 5;  
    ```  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die ErrorProvider-Komponente](errorprovider-component-overview-windows-forms.md)
- [Vorgehensweise: Anzeigen von Fehlersymbolen für die Formularvalidierung mit der ErrorProvider-Komponente in Windows Forms](display-error-icons-for-form-validation-with-wf-errorprovider.md)
