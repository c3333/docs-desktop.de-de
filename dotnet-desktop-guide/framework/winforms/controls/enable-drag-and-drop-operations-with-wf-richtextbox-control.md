---
title: Aktivieren von Drag & Drop-Vorgängen mit dem RichTextBox-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- examples [Windows Forms], text boxes
- drag and drop [Windows Forms], richTextBox control
- text boxes [Windows Forms], drag-and-drop operations
- RichTextBox control [Windows Forms], drag-and-drop operations
ms.assetid: ca167d1c-2014-4cf0-96a0-20598470be3b
ms.openlocfilehash: 27e5c18598552c465ef17f5e58069bc10e401c09
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975782"
---
# <a name="how-to-enable-drag-and-drop-operations-with-the-windows-forms-richtextbox-control"></a>Vorgehensweise: Aktivieren von Drag & Drop-Operationen mithilfe des RichTextBox-Steuerelements von Windows Forms
Drag &amp; Drop-Vorgänge mit dem Windows Forms-Steuerelement <xref:System.Windows.Forms.RichTextBox> erfolgen durch Verarbeitung der Ereignisse <xref:System.Windows.Forms.RichTextBox.DragEnter> und <xref:System.Windows.Forms.RichTextBox.DragDrop> . Durch das <xref:System.Windows.Forms.RichTextBox> -Steuerelement werden Drag &amp; Drop-Vorgänge daher sehr einfach.  
  
### <a name="to-enable-drag-operations-in-a-richtextbox-control"></a>Aktivieren von Drag-Vorgängen in einem RichTextBox-Steuerelement  
  
1. Legen Sie die <xref:System.Windows.Forms.RichTextBox.AllowDrop%2A> -Eigenschaft des <xref:System.Windows.Forms.RichTextBox> -Steuerelements auf `true`fest.  
  
2. Erstellen Sie Code für den Ereignishandler des <xref:System.Windows.Forms.RichTextBox.DragEnter> -Ereignisses. Verwenden Sie eine `if` -Anweisung, um sicherzustellen, dass die gezogenen Daten einem passenden Typ angehören (in diesem Fall Text). Die <xref:System.Windows.Forms.DragEventArgs.Effect%2A?displayProperty=nameWithType> -Eigenschaft kann auf jeden beliebigen Wert der <xref:System.Windows.Forms.DragDropEffects> -Enumeration festgelegt werden.  
  
    ```vb  
    Private Sub RichTextBox1_DragEnter(ByVal sender As Object, _
       ByVal e As System.Windows.Forms.DragEventArgs) _
       Handles RichTextBox1.DragEnter  
       If (e.Data.GetDataPresent(DataFormats.Text)) Then  
          e.Effect = DragDropEffects.Copy  
       Else  
          e.Effect = DragDropEffects.None  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void richTextBox1_DragEnter(object sender,
    System.Windows.Forms.DragEventArgs e)  
    {  
       if (e.Data.GetDataPresent(DataFormats.Text))
          e.Effect = DragDropEffects.Copy;  
       else  
          e.Effect = DragDropEffects.None;  
    }  
    ```  
  
    ```cpp  
    private:  
       void richTextBox1_DragEnter(System::Object ^  sender,  
          System::Windows::Forms::DragEventArgs ^  e)  
       {  
          if (e->Data->GetDataPresent(DataFormats::Text))  
             e->Effect = DragDropEffects::Copy;  
          else  
             e->Effect = DragDropEffects::None;  
       }  
    ```  
  
     (Visual c# und Visual C++) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.  
  
    ```csharp  
    this.richTextBox1.DragEnter += new  
        System.Windows.Forms.DragEventHandler  
        (this.richTextBox1_DragEnter);  
    ```  
  
    ```cpp  
    this->richTextBox1->DragEnter += gcnew  
       System::Windows::Forms::DragEventHandler  
       (this, &Form1::richTextBox1_DragEnter);  
    ```  
  
3. Erstellen Sie Code zur Behandlung des <xref:System.Windows.Forms.RichTextBox.DragDrop> -Ereignisses. Verwenden Sie die <xref:System.Windows.Forms.DataObject.GetData%2A?displayProperty=nameWithType> -Methode, um die gezogenen Daten abzurufen.  
  
     Im Beispiel unten legt der Code die <xref:System.Windows.Forms.RichTextBox.Text%2A> -Eigenschaft des <xref:System.Windows.Forms.RichTextBox> -Steuerelements auf die gezogenen Daten fest. Wenn sich bereits Text im <xref:System.Windows.Forms.RichTextBox> -Steuerelement befindet, wird der gezogene Text an der Einfügemarke eingefügt.  
  
    ```vb  
    Private Sub RichTextBox1_DragDrop(ByVal sender As Object, _
       ByVal e As System.Windows.Forms.DragEventArgs) _
       Handles RichTextBox1.DragDrop  
       Dim i As Int16
       Dim s As String  
  
       ' Get start position to drop the text.  
       i = RichTextBox1.SelectionStart  
       s = RichTextBox1.Text.Substring(i)  
       RichTextBox1.Text = RichTextBox1.Text.Substring(0, i)  
  
       ' Drop the text on to the RichTextBox.  
       RichTextBox1.Text = RichTextBox1.Text + _  
          e.Data.GetData(DataFormats.Text).ToString()  
       RichTextBox1.Text = RichTextBox1.Text + s  
    End Sub  
    ```  
  
    ```csharp  
    private void richTextBox1_DragDrop(object sender,
    System.Windows.Forms.DragEventArgs e)  
    {  
       int i;  
       String s;  
  
       // Get start position to drop the text.  
       i = richTextBox1.SelectionStart;  
       s = richTextBox1.Text.Substring(i);  
       richTextBox1.Text = richTextBox1.Text.Substring(0,i);  
  
       // Drop the text on to the RichTextBox.  
       richTextBox1.Text = richTextBox1.Text +
          e.Data.GetData(DataFormats.Text).ToString();  
       richTextBox1.Text = richTextBox1.Text + s;  
    }  
    ```  
  
    ```cpp  
    private:  
       System::Void richTextBox1_DragDrop(System::Object ^  sender,  
          System::Windows::Forms::DragEventArgs ^  e)  
       {  
          int i;  
          String ^s;  
  
       // Get start position to drop the text.  
       i = richTextBox1->SelectionStart;  
       s = richTextBox1->Text->Substring(i);  
       richTextBox1->Text = richTextBox1->Text->Substring(0,i);  
  
       // Drop the text on to the RichTextBox.  
       String ^str = String::Concat(richTextBox1->Text, e->Data  
       ->GetData(DataFormats->Text)->ToString());
       richTextBox1->Text = String::Concat(str, s);  
       }  
    ```  
  
     (Visual c# und Visual C++) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.  
  
    ```csharp  
    this.richTextBox1.DragDrop += new  
        System.Windows.Forms.DragEventHandler  
        (this.richTextBox1_DragDrop);  
    ```  
  
    ```cpp  
    this->richTextBox1->DragDrop += gcnew
       System::Windows::Forms::DragEventHandler  
       (this, &Form1::richTextBox1_DragDrop);  
    ```  
  
### <a name="to-test-the-drag-and-drop-functionality-in-your-application"></a>Testen der Drag & Drop-Funktionalität in der Anwendung  
  
1. Speichern und erstellen Sie Ihre Anwendung. Führen Sie WordPad aus, während die Anwendung ausgeführt wird.  
  
     WordPad ist ein Text-Editor von Windows, der Drag & Drop-Vorgänge ermöglicht. Sie können auf WordPad zugreifen, indem Sie auf die Schaltfläche **Start** klicken, den Befehl **Ausführen** auswählen und anschließend `WordPad` in das Textfeld des Dialogfelds **Ausführen** eingeben. Abschließend klicken Sie auf **OK**.  
  
2. Wenn WordPad geöffnet ist, geben Sie eine Textzeichenfolge ein. Markieren Sie den Text mit der Maus, und ziehen Sie den markierten Text dann auf das <xref:System.Windows.Forms.RichTextBox> -Steuerelement in der Windows-Anwendung.  
  
     Beachten Sie, dass wenn sich die Maus über dem <xref:System.Windows.Forms.RichTextBox> -Steuerelement befindet (und damit folglich das <xref:System.Windows.Forms.RichTextBox.DragEnter> -Ereignis ausgelöst wird), sich der Mauszeiger ändert und Sie den ausgewählten Text auf dem <xref:System.Windows.Forms.RichTextBox> -Steuerelement ablegen können.  
  
     Wenn Sie die Maustaste loslassen, wird der ausgewählte Text abgelegt (das heißt, das <xref:System.Windows.Forms.RichTextBox.DragDrop> -Ereignis wird ausgelöst) und in das <xref:System.Windows.Forms.RichTextBox> -Steuerelement eingefügt.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.RichTextBox>
- [Vorgehensweise: Ausführen von Drag &amp; Drop-Operationen zwischen Anwendungen](../advanced/how-to-perform-drag-and-drop-operations-between-applications.md)
- [RichTextBox-Steuerelement](richtextbox-control-windows-forms.md)
- [Steuerelemente für Windows Forms](controls-to-use-on-windows-forms.md)
