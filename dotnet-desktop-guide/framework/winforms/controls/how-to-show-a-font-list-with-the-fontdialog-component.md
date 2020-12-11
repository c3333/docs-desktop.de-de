---
title: 'Vorgehensweise: Anzeigen einer Schriftartenliste mit der FontDialog-Komponente'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- fonts [Windows Forms], showing list
- FontDialog component [Windows Forms]
- fonts [Windows Forms], attributes
- Font property [Windows Forms], setting with FontDialog component
- Font dialog box [Windows Forms], displaying
- fonts [Windows Forms], selecting
ms.assetid: 35692c1b-0937-4b7a-9207-1ae6bdc244a0
ms.openlocfilehash: 05e9b5e1280d0318354b0d47f4d78f7ec1c5f4e7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976746"
---
# <a name="how-to-show-a-font-list-with-the-fontdialog-component"></a>Vorgehensweise: Anzeigen einer Schriftartenliste mit der FontDialog-Komponente
Mit der [FontDialog](fontdialog-component-windows-forms.md) -Komponente können Benutzer eine Schriftart auswählen und deren Anzeige Aspekte ändern, wie z. b. die Gewichtung und die Größe.  
  
 Die im Dialogfeld ausgewählte Schriftart wird in der-Eigenschaft zurückgegeben <xref:System.Windows.Forms.FontDialog.Font%2A> . Daher ist die Nutzung der vom Benutzer ausgewählten Schriftart genauso einfach wie das Lesen einer Eigenschaft.  
  
### <a name="to-select-font-properties-using-the-fontdialog-component"></a>So wählen Sie Schriftart Eigenschaften mit der FontDialog-Komponente aus  
  
1. Zeigen Sie das Dialogfeld mit der- <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode an.  
  
2. Verwenden Sie die- <xref:System.Windows.Forms.DialogResult> Eigenschaft, um zu bestimmen, wie das Dialogfeld geschlossen wurde.  
  
3. Verwenden Sie die- <xref:System.Windows.Forms.FontDialog.Font%2A> Eigenschaft, um die gewünschte Schriftart festzulegen.  
  
     Im folgenden Beispiel <xref:System.Windows.Forms.Button> öffnet der-Ereignishandler des-Steuer Elements <xref:System.Windows.Forms.Control.Click> eine- <xref:System.Windows.Forms.FontDialog> Komponente. Wenn eine Schriftart ausgewählt wird und der Benutzer auf **OK** klickt, <xref:System.Windows.Forms.FontDialog.Font%2A> wird die-Eigenschaft eines <xref:System.Windows.Forms.TextBox> Steuer Elements auf dem Formular auf die gewählte Schriftart festgelegt. Das Beispiel setzt voraus, dass das Formular über ein <xref:System.Windows.Forms.Button> Steuerelement, ein  <xref:System.Windows.Forms.TextBox> -Steuerelement und eine- <xref:System.Windows.Forms.FontDialog> Komponente verfügt.  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, _  
       ByVal e As System.EventArgs) Handles Button1.Click  
       If FontDialog1.ShowDialog() = DialogResult.OK Then  
          TextBox1.Font = FontDialog1.Font  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)  
    {  
       if(fontDialog1.ShowDialog() == DialogResult.OK)  
       {  
          textBox1.Font = fontDialog1.Font;  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void button1_Click(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          if(fontDialog1->ShowDialog() == DialogResult::OK)  
          {  
             textBox1->Font = fontDialog1->Font;  
          }  
       }  
    ```  
  
     (Visual c# und Visual C++) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.  
  
    ```csharp  
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
    ```cpp  
    button1->Click += gcnew System::EventHandler(this, &Form1::button1_Click);  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.FontDialog>
- [FontDialog-Komponente](fontdialog-component-windows-forms.md)
