---
title: Antworten auf Klicks im DataGrid-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Click event [Windows Forms], monitoring in DataGrid controls
- DataGrid control [Windows Forms], examples
- DataGrid control [Windows Forms], returning clicked cell value
- cells [Windows Forms], location in DataGrid
- examples [Windows Forms], DataGrid control
- DataGrid control [Windows Forms], click events
ms.assetid: a0aa204b-8351-4d82-9933-ee21a5c9e409
ms.openlocfilehash: e72d117b12d43ece8c4d05ed29ab45693418eede
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975601"
---
# <a name="how-to-respond-to-clicks-in-the-windows-forms-datagrid-control"></a><span data-ttu-id="0a73e-102">Vorgehensweise: Reagieren auf das Klicken in das DataGrid-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="0a73e-102">How to: Respond to Clicks in the Windows Forms DataGrid Control</span></span>
> [!NOTE]
> <span data-ttu-id="0a73e-103">Obwohl das <xref:System.Windows.Forms.DataGridView>-Steuerelement das <xref:System.Windows.Forms.DataGrid>-Steuerelement ersetzt und funktionell erweitert, wird das <xref:System.Windows.Forms.DataGrid>-Steuerelement sowohl aus Gründen der Abwärtskompatibilität als auch, falls gewünscht, für die zukünftige Verwendung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="0a73e-103">The <xref:System.Windows.Forms.DataGridView> control replaces and adds functionality to the <xref:System.Windows.Forms.DataGrid> control; however, the <xref:System.Windows.Forms.DataGrid> control is retained for both backward compatibility and future use, if you choose.</span></span> <span data-ttu-id="0a73e-104">Weitere Informationen finden Sie unter [Unterschiede zwischen dem DataGridView-Steuerelement und dem DataGrid-Steuerelement in Windows Forms](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).</span><span class="sxs-lookup"><span data-stu-id="0a73e-104">For more information, see [Differences Between the Windows Forms DataGridView and DataGrid Controls](differences-between-the-windows-forms-datagridview-and-datagrid-controls.md).</span></span>  
  
 <span data-ttu-id="0a73e-105">Nachdem die Windows Forms mit <xref:System.Windows.Forms.DataGrid> einer Datenbank verbunden ist, können Sie überwachen, auf welche Zelle der Benutzer geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="0a73e-105">After the Windows Forms <xref:System.Windows.Forms.DataGrid> is connected to a database, you can monitor which cell the user clicked.</span></span>  
  
### <a name="to-detect-when-the-user-of-the-datagrid-selects-a-different-cell"></a><span data-ttu-id="0a73e-106">So erkennen Sie, wenn der Benutzer des DataGrid eine andere Zelle auswählt</span><span class="sxs-lookup"><span data-stu-id="0a73e-106">To detect when the user of the DataGrid selects a different cell</span></span>  
  
- <span data-ttu-id="0a73e-107"><xref:System.Windows.Forms.DataGrid.CurrentCellChanged>Schreiben Sie im-Ereignishandler Code, um entsprechend zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="0a73e-107">In the <xref:System.Windows.Forms.DataGrid.CurrentCellChanged> event handler, write code to respond appropriately.</span></span>  
  
    ```vb  
    Private Sub myDataGrid_CurrentCellChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles myDataGrid.CurrentCellChanged  
       MessageBox.Show("Col is " & myDataGrid.CurrentCell.ColumnNumber _  
          & ", Row is " & myDataGrid.CurrentCell.RowNumber _  
          & ", Value is " & myDataGrid.Item(myDataGrid.CurrentCell))  
    End Sub  
    ```  
  
    ```csharp  
    private void myDataGrid_CurrentCellChanged(object sender,
    System.EventArgs e)  
    {  
       MessageBox.Show ("Col is " + myDataGrid.CurrentCell.ColumnNumber  
          + ", Row is " + myDataGrid.CurrentCell.RowNumber
          + ", Value is " + myDataGrid[myDataGrid.CurrentCell] );  
    }  
    ```  
  
     <span data-ttu-id="0a73e-108">(Visual c#) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="0a73e-108">(Visual C#) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.myDataGrid.CurrentCellChanged += new  
       System.EventHandler(this.myDataGrid_CurrentCellChanged);  
    ```  
  
### <a name="to-determine-which-part-of-the-datagrid-the-user-clicked"></a><span data-ttu-id="0a73e-109">So bestimmen Sie den Teil des DataGrids, auf den der Benutzer geklickt hat</span><span class="sxs-lookup"><span data-stu-id="0a73e-109">To determine which part of the DataGrid the user clicked</span></span>  
  
- <span data-ttu-id="0a73e-110">Ruft die- <xref:System.Windows.Forms.DataGrid.HitTest%2A> Methode in einem geeigneten Ereignishandler auf, z. b. für das- <xref:System.Windows.Forms.Control.MouseDown> Ereignis oder das- <xref:System.Windows.Forms.Control.Click> Ereignis</span><span class="sxs-lookup"><span data-stu-id="0a73e-110">Call the <xref:System.Windows.Forms.DataGrid.HitTest%2A> method in an appropriate event handler, such as for the <xref:System.Windows.Forms.Control.MouseDown> or <xref:System.Windows.Forms.Control.Click> event.</span></span>  
  
     <span data-ttu-id="0a73e-111">Die- <xref:System.Windows.Forms.DataGrid.HitTest%2A> Methode gibt ein- <xref:System.Windows.Forms.DataGrid.HitTestInfo> Objekt zurück, das die Zeile und die Spalte eines angeklickten Bereichs enthält.</span><span class="sxs-lookup"><span data-stu-id="0a73e-111">The <xref:System.Windows.Forms.DataGrid.HitTest%2A> method returns a <xref:System.Windows.Forms.DataGrid.HitTestInfo> object that contains the row and column of a clicked area.</span></span>  
  
    ```vb  
    Private Sub myDataGrid_MouseDown(ByVal sender As Object, _  
    ByVal e As MouseEventArgs) Handles myDataGrid.MouseDown  
       Dim myGrid As DataGrid = CType(sender, DataGrid)  
       Dim hti As System.Windows.Forms.DataGrid.HitTestInfo  
       hti = myGrid.HitTest(e.X, e.Y)  
       Dim message As String = "You clicked "  
  
       Select Case hti.Type  
          Case System.Windows.Forms.DataGrid.HitTestType.None  
             message &= "the background."  
          Case System.Windows.Forms.DataGrid.HitTestType.Cell  
             message &= "cell at row " & hti.Row & ", col " & hti.Column  
          Case System.Windows.Forms.DataGrid.HitTestType.ColumnHeader  
             message &= "the column header for column " & hti.Column  
          Case System.Windows.Forms.DataGrid.HitTestType.RowHeader  
             message &= "the row header for row " & hti.Row  
          Case System.Windows.Forms.DataGrid.HitTestType.ColumnResize  
             message &= "the column resizer for column " & hti.Column  
          Case System.Windows.Forms.DataGrid.HitTestType.RowResize  
             message &= "the row resizer for row " & hti.Row  
          Case System.Windows.Forms.DataGrid.HitTestType.Caption  
             message &= "the caption"  
          Case System.Windows.Forms.DataGrid.HitTestType.ParentRows  
             message &= "the parent row"  
       End Select  
  
       Console.WriteLine(message)  
    End Sub  
    ```  
  
    ```csharp  
    private void myDataGrid_MouseDown(object sender,
    System.Windows.Forms.MouseEventArgs e)  
    {  
       DataGrid myGrid = (DataGrid) sender;  
       System.Windows.Forms.DataGrid.HitTestInfo hti;  
       hti = myGrid.HitTest(e.X, e.Y);  
       string message = "You clicked ";  
  
       switch (hti.Type)
       {  
          case System.Windows.Forms.DataGrid.HitTestType.None :  
             message += "the background.";  
             break;  
          case System.Windows.Forms.DataGrid.HitTestType.Cell :  
             message += "cell at row " + hti.Row + ", col " + hti.Column;  
             break;  
          case System.Windows.Forms.DataGrid.HitTestType.ColumnHeader :  
             message += "the column header for column " + hti.Column;  
             break;  
          case System.Windows.Forms.DataGrid.HitTestType.RowHeader :  
             message += "the row header for row " + hti.Row;  
             break;  
          case System.Windows.Forms.DataGrid.HitTestType.ColumnResize :  
             message += "the column resizer for column " + hti.Column;  
             break;  
          case System.Windows.Forms.DataGrid.HitTestType.RowResize :  
             message += "the row resizer for row " + hti.Row;  
             break;  
          case System.Windows.Forms.DataGrid.HitTestType.Caption :  
             message += "the caption";  
             break;  
          case System.Windows.Forms.DataGrid.HitTestType.ParentRows :  
             message += "the parent row";  
             break;  
          }  
  
          Console.WriteLine(message);  
    }  
    ```  
  
     <span data-ttu-id="0a73e-112">(Visual c#) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="0a73e-112">(Visual C#) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.myDataGrid.MouseDown += new  
       System.Windows.Forms.MouseEventHandler  
       (this.myDataGrid_MouseDown);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="0a73e-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a73e-113">See also</span></span>

- [<span data-ttu-id="0a73e-114">DataGrid-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="0a73e-114">DataGrid Control</span></span>](datagrid-control-windows-forms.md)
- [<span data-ttu-id="0a73e-115">Vorgehensweise: Ändern der angezeigten Daten im DataGrid-Steuerelement in Windows Forms zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="0a73e-115">How to: Change Displayed Data at Run Time in the Windows Forms DataGrid Control</span></span>](change-displayed-data-at-run-time-wf-datagrid-control.md)
