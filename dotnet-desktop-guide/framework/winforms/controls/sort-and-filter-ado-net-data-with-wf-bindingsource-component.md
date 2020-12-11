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
# <a name="how-to-sort-and-filter-adonet-data-with-the-windows-forms-bindingsource-component"></a>Vorgehensweise: Sortieren und Filtern von ADO.NET-Daten mit der BindingSource-Komponente in Windows Forms

Mithilfe der-Eigenschaft und der-Eigenschaft können Sie die Sortier-und Filterfunktion des Steuer Elements verfügbar machen <xref:System.Windows.Forms.BindingSource> <xref:System.Windows.Forms.BindingSource.Sort%2A> <xref:System.Windows.Forms.BindingSource.Filter%2A> . Sie können eine einfache Sortierung anwenden, wenn die zugrunde liegende Datenquelle eine ist <xref:System.ComponentModel.IBindingList> , und Sie können Filter und erweiterte Sortierung anwenden, wenn die Datenquelle eine ist <xref:System.ComponentModel.IBindingListView> . Die- <xref:System.Windows.Forms.BindingSource.Sort%2A> Eigenschaft erfordert die ADO.NET-Standard Syntax: eine Zeichenfolge, die den Namen einer Datenspalte in der Datenquelle darstellt, gefolgt von `ASC` oder `DESC` , um anzugeben, ob die Liste in aufsteigender oder absteigender Reihenfolge sortiert werden soll. Sie können eine erweiterte Sortierung oder eine Sortierung mit mehreren Spalten festlegen, indem Sie jede Spalte durch ein Komma Trennzeichen trennen. Die- <xref:System.Windows.Forms.BindingSource.Filter%2A> Eigenschaft nimmt einen Zeichen folgen Ausdruck an.  
  
> [!NOTE]
> Das Speichern vertraulicher Informationen (z. B. eines Kennworts) innerhalb der Verbindungszeichenfolge kann die Sicherheit einer Anwendung beeinträchtigen. Der Zugriff auf eine Datenbank lässt sich mithilfe der Windows-Authentifizierung (wird auch als integrierte Sicherheit bezeichnet) sicherer steuern. Weitere Informationen finden Sie unter [Protecting Connection Information (Schützen von Verbindungsinformationen)](/dotnet/framework/data/adonet/protecting-connection-information).  
  
### <a name="to-filter-data-with-the-bindingsource"></a>So filtern Sie Daten mit der BindingSource  
  
- Legen Sie die- <xref:System.Windows.Forms.BindingSource.Filter%2A> Eigenschaft auf den gewünschten Ausdruck fest.  
  
     Im folgenden Codebeispiel ist der Ausdruck ein Spaltenname, gefolgt von dem Wert, den Sie für die Spalte benötigen.  
  
 [!code-csharp[System.Windows.Forms.DataConnectorFilterAndSort#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/CS/form1.cs#11)]
 [!code-vb[System.Windows.Forms.DataConnectorFilterAndSort#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/VB/form1.vb#11)]  
  
### <a name="to-sort-data-with-the-bindingsource"></a>So sortieren Sie Daten mit der BindingSource  
  
1. Legen Sie die- <xref:System.Windows.Forms.BindingSource.Sort%2A> Eigenschaft auf den Spaltennamen fest, den Sie folgen möchten, `ASC` oder `DESC` , um den aufsteigenden oder absteigenden Auftrag anzugeben.  
  
2. Trennen Sie mehrere Spalten durch ein Komma.  
  
 [!code-csharp[System.Windows.Forms.DataConnectorFilterAndSort#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/CS/form1.cs#12)]
 [!code-vb[System.Windows.Forms.DataConnectorFilterAndSort#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/VB/form1.vb#12)]  
  
## <a name="example"></a>Beispiel  

 Im folgenden Codebeispiel werden Daten aus der Customers-Tabelle der Beispieldatenbank Northwind in ein <xref:System.Windows.Forms.DataGridView> -Steuerelement geladen, und die angezeigten Daten werden gefiltert und sortiert.  
  
 [!code-csharp[System.Windows.Forms.DataConnectorFilterAndSort#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/CS/form1.cs#1)]
 [!code-vb[System.Windows.Forms.DataConnectorFilterAndSort#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataConnectorFilterAndSort/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  

 Um dieses Beispiel auszuführen, fügen Sie den Code in ein Formular ein, das ein mit dem Namen <xref:System.Windows.Forms.BindingSource> `BindingSource1` und ein mit dem <xref:System.Windows.Forms.DataGridView> Namen enthält `dataGridView1` . Behandeln Sie das <xref:System.Windows.Forms.Form.Load> -Ereignis für das Formular, und nennen Sie es `InitializeSortedFilteredBindingSource` in der Load-Ereignishandlermethode  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.BindingSource.Sort%2A>
- <xref:System.Windows.Forms.BindingSource.Filter%2A>
- [Gewusst wie: Installieren von Beispieldatenbanken](/previous-versions/visualstudio/visual-studio-2013/8b6y4c7s(v=vs.120))
- [BindingSource-Komponente](bindingsource-component.md)
