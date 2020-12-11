---
title: Standard Druckaufträge erstellen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- printing [Windows Forms]
- printing [Windows Forms], creating print jobs
- printing [Visual Basic], in Windows applications
ms.assetid: 03342b90-9cfe-40b2-838b-b479a13c5dea
ms.openlocfilehash: d9607de7c74132e0d7dce605b16d62c79b7dbccb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975265"
---
# <a name="how-to-create-standard-windows-forms-print-jobs"></a>Vorgehensweise: Erstellen von standardmäßigen Druckaufträgen in Windows Forms
Die Grundlage für das Drucken in Windows Forms ist die <xref:System.Drawing.Printing.PrintDocument> Komponente – genauer gesagt das <xref:System.Drawing.Printing.PrintDocument.PrintPage> Ereignis. Wenn Sie Code schreiben, um das Ereignis zu behandeln <xref:System.Drawing.Printing.PrintDocument.PrintPage> , können Sie angeben, was gedruckt und gedruckt werden soll.  
  
### <a name="to-create-a-print-job"></a>So erstellen Sie einen Druckauftrag  
  
1. Fügen Sie dem <xref:System.Drawing.Printing.PrintDocument> Formular eine Komponente hinzu.  
  
2. Erstellen Sie Code zur Behandlung des <xref:System.Drawing.Printing.PrintDocument.PrintPage> -Ereignisses.  
  
     Sie müssen ihre eigene Druck Logik programmieren. Außerdem müssen Sie das Material angeben, das gedruckt werden soll.  
  
     Im folgenden Codebeispiel wird eine Beispiel Grafik in der Form eines roten Rechtecks im-Ereignishandler erstellt, der <xref:System.Drawing.Printing.PrintDocument.PrintPage> als Material zum Drucken fungiert.  
  
    ```vb  
    Private Sub PrintDocument1_PrintPage(ByVal sender As Object, ByVal e As System.Drawing.Printing.PrintPageEventArgs) Handles PrintDocument1.PrintPage  
       e.Graphics.FillRectangle(Brushes.Red, New Rectangle(500, 500, 500, 500))  
    End Sub  
    ```  
  
    ```csharp  
    private void printDocument1_PrintPage(object sender,
    System.Drawing.Printing.PrintPageEventArgs e)  
    {  
       e.Graphics.FillRectangle(Brushes.Red,
         new Rectangle(500, 500, 500, 500));  
    }  
    ```  
  
    ```cpp  
    private:  
       void printDocument1_PrintPage(System::Object ^ sender,  
          System::Drawing::Printing::PrintPageEventArgs ^ e)  
       {  
          e->Graphics->FillRectangle(Brushes::Red,  
             Rectangle(500, 500, 500, 500));  
       }  
    ```  
  
     (Visual c# und Visual C++) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.  
  
    ```csharp  
    this.printDocument1.PrintPage += new  
       System.Drawing.Printing.PrintPageEventHandler  
       (this.printDocument1_PrintPage);  
    ```  
  
    ```cpp  
    printDocument1->PrintPage += gcnew  
       System::Drawing::Printing::PrintPageEventHandler  
       (this, &Form1::printDocument1_PrintPage);  
    ```  
  
     Möglicherweise möchten Sie auch Code für das <xref:System.Drawing.Printing.PrintDocument.BeginPrint> -Ereignis und das-Ereignis schreiben, z. b. <xref:System.Drawing.Printing.PrintDocument.EndPrint> eine ganze Zahl, die die Gesamtzahl der zu druckenden Seiten darstellt, die bei jeder Seite gedruckt wird.  
  
    > [!NOTE]
    > Sie können dem Formular eine Komponente hinzufügen <xref:System.Windows.Forms.PrintDialog> , um Benutzern eine saubere und effiziente Benutzeroberfläche zur Verfügung zu stellen. Durch Festlegen der- <xref:System.Windows.Forms.PrintDialog.Document%2A> Eigenschaft der- <xref:System.Windows.Forms.PrintDialog> Komponente können Sie Eigenschaften festlegen, die sich auf das Druck Dokument beziehen, mit dem Sie in Ihrem Formular arbeiten. Weitere Informationen zur- <xref:System.Windows.Forms.PrintDialog> Komponente finden Sie unter [PrintDialog-Komponente](../controls/printdialog-component-windows-forms.md).  
  
     Weitere Informationen zu den Besonderheiten Windows Forms Druckaufträgen, einschließlich der programmgesteuerten Erstellung eines Druckauftrags, finden Sie unter <xref:System.Drawing.Printing.PrintPageEventArgs> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Printing.PrintDocument>
- [Druckunterstützung in Windows Forms](windows-forms-print-support.md)
