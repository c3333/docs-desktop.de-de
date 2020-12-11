---
title: Vollständige Druckaufträge
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- print jobs [Windows Forms], completing in Windows Forms
- printing [Windows Forms], print jobs
ms.assetid: 23ec74f7-34c5-4710-82a0-ee2914518548
ms.openlocfilehash: 62f67002bfbaf46e73bae06fdaff26efde865c06
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975012"
---
# <a name="how-to-complete-windows-forms-print-jobs"></a>Vorgehensweise: Fertigstellen von Druckaufträgen in Windows Forms
Häufig bieten Word-Prozessoren und andere Anwendungen, die das Drucken einschließen, die Möglichkeit, Benutzern eine Meldung anzuzeigen, dass ein Druckauftrag vollständig ist. Sie können diese Funktionalität in Ihrem Windows Forms bereitstellen, indem Sie das- <xref:System.Drawing.Printing.PrintDocument.EndPrint> Ereignis der- <xref:System.Drawing.Printing.PrintDocument> Komponente behandeln.  
  
 Das folgende Verfahren erfordert, dass Sie eine Windows-basierte Anwendung mit einer- <xref:System.Drawing.Printing.PrintDocument> Komponente erstellt haben. Dies ist die Standardmethode zum Aktivieren von Drucken aus einer Windows-basierten Anwendung. Weitere Informationen zum Drucken aus Windows Forms mithilfe der- <xref:System.Drawing.Printing.PrintDocument> Komponente finden Sie unter [How to: Create Standard Windows Forms Print Jobs](how-to-create-standard-windows-forms-print-jobs.md).  
  
### <a name="to-complete-a-print-job"></a>So vervollständigen Sie einen Druckauftrag  
  
1. Legen Sie die- <xref:System.Drawing.Printing.PrintDocument.DocumentName%2A> Eigenschaft der <xref:System.Drawing.Printing.PrintDocument> Komponente fest.  
  
    ```vb  
    PrintDocument1.DocumentName = "MyTextFile"  
    ```  
  
    ```csharp  
    printDocument1.DocumentName = "MyTextFile";  
    ```  
  
    ```cpp  
    printDocument1->DocumentName = "MyTextFile";  
    ```  
  
2. Erstellen Sie Code zur Behandlung des <xref:System.Drawing.Printing.PrintDocument.EndPrint> -Ereignisses.  
  
     Im folgenden Codebeispiel wird ein Meldungs Feld angezeigt, das angibt, dass das Dokument den Druckvorgang abgeschlossen hat.  
  
    ```vb  
    Private Sub PrintDocument1_EndPrint(ByVal sender As Object, ByVal e As System.Drawing.Printing.PrintEventArgs) Handles PrintDocument1.EndPrint  
       MessageBox.Show(PrintDocument1.DocumentName + " has finished printing.")  
    End Sub  
    ```  
  
    ```csharp  
    private void printDocument1_EndPrint(object sender,
    System.Drawing.Printing.PrintEventArgs e)  
    {  
       MessageBox.Show(printDocument1.DocumentName +
          " has finished printing.");  
    }  
    ```  
  
    ```cpp  
    private:  
       void printDocument1_EndPrint(System::Object ^ sender,  
          System::Drawing::Printing::PrintEventArgs ^ e)  
       {  
          MessageBox::Show(String::Concat(printDocument1->DocumentName,  
             " has finished printing."));  
       }  
    ```  
  
     (Visual c# und Visual C++) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.  
  
    ```csharp  
    this.printDocument1.EndPrint += new  
       System.Drawing.Printing.PrintEventHandler  
       (this.printDocument1_EndPrint);  
    ```  
  
    ```cpp  
    this->printDocument1->EndPrint += gcnew  
       System::Drawing::Printing::PrintEventHandler  
       (this, &Form1::printDocument1_EndPrint);  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Printing.PrintDocument>
- [Druckunterstützung in Windows Forms](windows-forms-print-support.md)
