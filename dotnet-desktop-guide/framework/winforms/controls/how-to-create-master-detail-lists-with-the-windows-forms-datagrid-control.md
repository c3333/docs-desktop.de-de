---
title: Erstellen von Master-Detail Listen mit dem DataGrid-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- master-details lists
- DataGrid control [Windows Forms], master-details lists
- related tables [Windows Forms], displaying in DataGrid control
ms.assetid: 20388c6a-94f9-4d96-be18-8c200491247f
ms.openlocfilehash: e8ab63d52d97a8a6e6f60da741186e3937350e1e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975683"
---
# <a name="how-to-create-masterdetail-lists-with-the-windows-forms-datagrid-control"></a>Vorgehensweise: Erstellen von Master/Detail-Listen mit dem DataGrid-Steuerelement in Windows Forms
> [!NOTE]
> Obwohl das <xref:System.Windows.Forms.DataGridView>-Steuerelement das <xref:System.Windows.Forms.DataGrid>-Steuerelement ersetzt und funktionell erweitert, wird das <xref:System.Windows.Forms.DataGrid>-Steuerelement sowohl aus Gründen der Abwärtskompatibilität als auch, falls gewünscht, für die zukünftige Verwendung beibehalten. Weitere Informationen finden Sie unter [Unterschiede zwischen dem DataGridView-Steuerelement und dem DataGrid-Steuerelement in Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).  
  
 Wenn Ihr <xref:System.Data.DataSet> eine Reihe verwandter Tabellen enthält, können Sie zwei-Steuer <xref:System.Windows.Forms.DataGrid> Elemente verwenden, um die Daten im Master-/Detail-Format anzuzeigen. Eine <xref:System.Windows.Forms.DataGrid> ist als Haupt Raster festgelegt, und die zweite ist als das Detail Raster festgelegt. Wenn Sie in der Liste Master einen Eintrag auswählen, werden alle zugehörigen untergeordneten Einträge in der Detail Liste angezeigt. Wenn Ihr z. b. <xref:System.Data.DataSet> eine Customers-Tabelle und eine zugehörige Orders-Tabelle enthält, geben Sie die Customers-Tabelle als Haupt Raster und die Orders-Tabelle als Detail Raster an. Wenn ein Kunde aus dem Haupt Raster ausgewählt wird, werden alle Bestellungen, die diesem Kunden in der Tabelle Orders zugeordnet sind, im Detail Raster angezeigt.  
  
### <a name="to-set-a-masterdetail-relationship-programmatically"></a>So legen Sie eine Master/Detail-Beziehung Programm gesteuert fest  
  
1. Erstellen Sie zwei neue Steuer <xref:System.Windows.Forms.DataGrid> Elemente, und legen Sie deren Eigenschaften fest.  
  
2. Fügen Sie dem Dataset Tabellen hinzu.  
  
3. Deklarieren Sie eine Variable vom Typ <xref:System.Data.DataRelation> zur Darstellung der Beziehung, die Sie erstellen möchten.  
  
4. Instanziieren Sie die Beziehung, indem Sie einen Namen für die Beziehung angeben und die Tabelle, die Spalte und das Element angeben, mit denen die beiden Tabellen verknüpft werden.  
  
5. Fügen Sie die Beziehung der <xref:System.Data.DataSet> -Auflistung des-Objekts hinzu <xref:System.Data.DataSet.Relations%2A> .  
  
6. Verwenden Sie die- <xref:System.Windows.Forms.DataGrid.SetDataBinding%2A> Methode des <xref:System.Windows.Forms.DataGrid> , um die einzelnen Raster an die zu binden <xref:System.Data.DataSet> .  
  
     Im folgenden Beispiel wird gezeigt, wie eine Master/Detail-Beziehung zwischen den Tabellen Customers und Orders in einem zuvor generierten () festgelegt wird <xref:System.Data.DataSet> `ds` .  
  
    ```vb  
    Dim myDataRelation As DataRelation  
    myDataRelation = New DataRelation _  
       ("CustOrd", ds.Tables("Customers").Columns("CustomerID"), _  
       ds.Tables("Orders").Columns("CustomerID"))  
    ' Add the relation to the DataSet.  
    ds.Relations.Add(myDataRelation)  
    GridOrders.SetDataBinding(ds, "Customers")  
    GridDetails.SetDataBinding(ds, "Customers.CustOrd")  
    ```  
  
    ```csharp  
    DataRelation myDataRelation;  
    myDataRelation = new DataRelation("CustOrd", ds.Tables["Customers"].Columns["CustomerID"], ds.Tables["Orders"].Columns["CustomerID"]);  
    // Add the relation to the DataSet.  
    ds.Relations.Add(myDataRelation);  
    GridOrders.SetDataBinding(ds,"Customers");  
    GridDetails.SetDataBinding(ds,"Customers.CustOrd");  
    ```  
  
    ```cpp  
    DataRelation^ myDataRelation;  
    myDataRelation = gcnew DataRelation("CustOrd",  
       ds->Tables["Customers"]->Columns["CustomerID"],  
       ds->Tables["Orders"]->Columns["CustomerID"]);  
    // Add the relation to the DataSet.  
    ds->Relations->Add(myDataRelation);  
    GridOrders->SetDataBinding(ds, "Customers");  
    GridDetails->SetDataBinding(ds, "Customers.CustOrd");  
    ```  
  
## <a name="see-also"></a>Siehe auch

- [DataGrid-Steuerelement](datagrid-control-windows-forms.md)
- [Übersicht über das DataGrid-Steuerelement](datagrid-control-overview-windows-forms.md)
- [Vorgehensweise: Binden des DataGrid-Steuerelements in Windows Forms an eine Datenquelle](how-to-bind-the-windows-forms-datagrid-control-to-a-data-source.md)
