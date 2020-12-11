---
title: 'Vorgehensweise: Auswählen der Drucker, die an den Computer eines Benutzers angeschlossen sind'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- printing [Windows Forms], choosing printers
- printers [Windows Forms], choosing
ms.assetid: 63c1172b-2931-4ac0-953f-37f629494bbf
ms.openlocfilehash: 2afbccd02ef42a78d5eac1a01841516fca27c92e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972381"
---
# <a name="how-to-choose-the-printers-attached-to-a-users-computer-in-windows-forms"></a>Vorgehensweise: Auswählen der einem Benutzercomputer zugewiesenen Drucker in Windows Forms
Häufig möchten Benutzer einen anderen Drucker als den Standarddrucker zum Drucken auswählen. Sie können es Benutzern ermöglichen, mithilfe der <xref:System.Windows.Forms.PrintDialog> -Komponente einen Drucker unter den Druckern auszuwählen, die derzeit installiert sind. Über die Komponente <xref:System.Windows.Forms.PrintDialog> wird das <xref:System.Windows.Forms.DialogResult> der Komponente <xref:System.Windows.Forms.PrintDialog> aufgezeichnet und für die Auswahl des Druckers verwendet.  
  
 In der folgenden Prozedur wird eine Textdatei ausgewählt, die auf dem Standarddrucker gedruckt werden soll. Die <xref:System.Windows.Forms.PrintDialog> -Klasse wird dann instanziiert.  
  
### <a name="to-choose-a-printer-and-then-print-a-file"></a>So wählen Sie einen Drucker aus und drucken eine Datei  
  
1. Wählen Sie den Drucker aus, der mit der Komponente verwendet werden soll <xref:System.Windows.Forms.PrintDialog> .  
  
     Im folgenden Codebeispiel werden zwei Ereignisse behandelt. Im ersten, dem <xref:System.Windows.Forms.Button> -Ereignis eines-Steuer Elements <xref:System.Windows.Forms.Control.Click> , <xref:System.Windows.Forms.PrintDialog> wird die-Klasse instanziiert, und der vom Benutzer ausgewählte Drucker wird in der- <xref:System.Windows.Forms.DialogResult> Eigenschaft aufgezeichnet.  
  
     Im zweiten Ereignis, dem- <xref:System.Drawing.Printing.PrintDocument.PrintPage> Ereignis der- <xref:System.Drawing.Printing.PrintDocument> Komponente, wird ein Beispiel Dokument an den angegebenen Drucker ausgegeben.  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles Button1.Click  
       Dim PrintDialog1 As New PrintDialog()  
       PrintDialog1.Document = PrintDocument1  
       Dim result As DialogResult = PrintDialog1.ShowDialog()  
  
       If (result = DialogResult.OK) Then  
         PrintDocument1.Print()  
       End If
  
    End Sub  
  
    Private Sub PrintDocument1_PrintPage(ByVal sender As Object, ByVal e As System.Drawing.Printing.PrintPageEventArgs) Handles PrintDocument1.PrintPage  
       e.Graphics.FillRectangle(Brushes.Red, New Rectangle(500, 500, 500, 500))
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)  
    {  
       PrintDialog printDialog1 = new PrintDialog();  
       printDialog1.Document = printDocument1;  
       DialogResult result = printDialog1.ShowDialog();  
       if (result == DialogResult.OK)  
       {  
          printDocument1.Print();  
       }  
    }  
  
    private void printDocument1_PrintPage(object sender,
    System.Drawing.Printing.PrintPageEventArgs e)  
    {  
       e.Graphics.FillRectangle(Brushes.Red,
         new Rectangle(500, 500, 500, 500));  
    }  
    ```  
  
    ```cpp  
    private:  
       void button1_Click(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          PrintDialog ^ printDialog1 = gcnew PrintDialog();  
          printDialog1->Document = printDocument1;  
          System::Windows::Forms::DialogResult result =
             printDialog1->ShowDialog();  
          if (result == DialogResult::OK)  
          {  
             printDocument1->Print();  
          }  
       }  
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
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
    ```cpp  
    this->printDocument1->PrintPage += gcnew  
       System::Drawing::Printing::PrintPageEventHandler  
       (this, &Form1::printDocument1_PrintPage);  
    this->button1->Click += gcnew  
       System::EventHandler(this, &Form1::button1_Click);  
    ```  
  
## <a name="see-also"></a>Siehe auch

- [Druckunterstützung in Windows Forms](windows-forms-print-support.md)
