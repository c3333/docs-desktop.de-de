---
title: 'Exemplarische Vorgehensweise: Arbeiten mit dem MaskedTextBox-Steuerelement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- input [Windows Forms], controlling to ensure validity
- MaskedTextBox control [Windows Forms], walkthroughs
- MaskedTextBox control [Windows Forms], validation
- user input [Windows Forms], controlling
- text [Windows Forms], controls for input
ms.assetid: df60565e-5447-4110-92a6-be1f6ff5faa3
ms.openlocfilehash: db32b3ec88a07747ea3e286af9f04edce3f1ba3b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976585"
---
# <a name="walkthrough-working-with-the-maskedtextbox-control"></a>Exemplarische Vorgehensweise: Arbeiten mit dem MaskedTextBox-Steuerelement
In dieser exemplarischen Vorgehensweise werden u. a. folgende Aufgaben veranschaulicht:  
  
- Initialisieren des <xref:System.Windows.Forms.MaskedTextBox> Steuer Elements  
  
- Verwenden des <xref:System.Windows.Forms.MaskedTextBox.MaskInputRejected> Ereignis Handlers, um den Benutzer zu benachrichtigen, wenn ein Zeichen nicht der Maske entspricht  
  
- Weisen Sie der Eigenschaft einen Typ zu, <xref:System.Windows.Forms.MaskedTextBox.ValidatingType%2A> und verwenden <xref:System.Windows.Forms.MaskedTextBox.TypeValidationCompleted> Sie den Ereignishandler, um den Benutzer zu benachrichtigen, wenn der Wert, für den Sie einen Commit durchsetzen möchten, nicht gültig ist.  
  
## <a name="creating-the-project-and-adding-a-control"></a>Erstellen des Projekts und Hinzufügen eines Steuer Elements  
  
#### <a name="to-add-a-maskedtextbox-control-to-your-form"></a>So fügen Sie dem Formular ein MaskedTextBox-Steuerelement hinzu  
  
1. Öffnen Sie das Formular, in dem Sie das Steuerelement platzieren möchten <xref:System.Windows.Forms.MaskedTextBox> .  
  
2. Ziehen Sie ein- <xref:System.Windows.Forms.MaskedTextBox> Steuerelement aus der **Toolbox** auf das Formular.  
  
3. Klicken Sie mit der rechten Maustaste, und wählen Sie **Eigenschaften** aus. Wählen Sie im Fenster **Eigenschaften** die Eigenschaft **Maske** aus, und klicken Sie auf die Schaltfläche mit den Auslassungs Punkten ( **...** ) neben dem Eigenschaftsnamen.  
  
4. Wählen Sie im Dialogfeld **Eingabemaske** die **kurze Datums** Maske aus, und klicken Sie auf **OK**.  
  
5. Legen Sie im Fenster **Eigenschaften** die- <xref:System.Windows.Forms.MaskedTextBox.BeepOnError%2A> Eigenschaft auf fest `true` . Diese Eigenschaft bewirkt, dass ein kurzes Signal jedes Mal einen Sound auslöst, wenn der Benutzer versucht, ein Zeichen einzugeben, das die Masken Definition verletzt.  
  
 Eine Zusammenfassung der Zeichen, die von der Mask-Eigenschaft unterstützt werden, finden Sie im Abschnitt "Hinweise" der- <xref:System.Windows.Forms.MaskedTextBox.Mask%2A> Eigenschaft.  
  
## <a name="alert-the-user-to-input-errors"></a>Warnung für den Benutzer zur Eingabe von Fehlern  
  
#### <a name="add-a-balloon-tip-for-rejected-mask-input"></a>Sprechblasen Info für abgelehnte Masken Eingabe hinzufügen  
  
1. Kehren Sie zur **Toolbox** zurück, und fügen Sie dem Formular einen hinzu <xref:System.Windows.Forms.ToolTip> .  
  
2. Erstellen Sie einen Ereignishandler für das- <xref:System.Windows.Forms.MaskedTextBox.MaskInputRejected> Ereignis, das auslöst, <xref:System.Windows.Forms.ToolTip> Wenn ein Eingabefehler auftritt. Die Sprechblasen Info bleibt für fünf Sekunden oder bis zur Anzeige durch den Benutzer sichtbar.  
  
    ```csharp  
    public void Form1_Load(Object sender, EventArgs e)
    {  
        ... // Other initialization code  
        maskedTextBox1.Mask = "00/00/0000";  
        maskedTextBox1.MaskInputRejected += new MaskInputRejectedEventHandler(maskedTextBox1_MaskInputRejected)  
    }  
  
    void maskedTextBox1_MaskInputRejected(object sender, MaskInputRejectedEventArgs e)  
    {  
        toolTip1.ToolTipTitle = "Invalid Input";  
        toolTip1.Show("We're sorry, but only digits (0-9) are allowed in dates.", maskedTextBox1, maskedTextBox1.Location, 5000);  
    }  
    ```  
  
    ```vb  
    Private Sub Form1_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load  
        Me.ToolTip1.IsBalloon = True  
        Me.MaskedTextBox1.Mask = "00/00/0000"  
    End Sub  
  
    Private Sub MaskedTextBox1_MaskInputRejected(sender as Object, e as MaskInputRejectedEventArgs) Handles MaskedTextBox1.MaskInputRejected  
        ToolTip1.ToolTipTitle = "Invalid Input"  
        ToolTip1.Show("We're sorry, but only digits (0-9) are allowed in dates.", MaskedTextBox1, 5000)  
    End Sub  
    ```  
  
## <a name="alert-the-user-to-a-type-that-is-not-valid"></a>Warnung an den Benutzer, der ungültig ist  
  
#### <a name="add-a-balloon-tip-for-invalid-data-types"></a>Sprechblasen Tipp für ungültige Datentypen hinzufügen  
  
1. Weisen Sie im- <xref:System.Windows.Forms.Form.Load> Ereignishandler des Formulars ein- <xref:System.Type> Objekt zu, das den <xref:System.DateTime> Typ der-Eigenschaft des-Steuer Elements darstellt <xref:System.Windows.Forms.MaskedTextBox> <xref:System.Windows.Forms.MaskedTextBox.ValidatingType%2A> :  
  
    ```csharp  
    private void Form1_Load(Object sender, EventArgs e)  
    {  
        // Other code  
        maskedTextBox1.ValidatingType = typeof(System.DateTime);  
        maskedTextBox1.TypeValidationCompleted += new TypeValidationEventHandler(maskedTextBox1_TypeValidationCompleted);  
    }  
    ```  
  
    ```vb  
    Private Sub Form1_Load(sender as Object, e as EventArgs)  
        // Other code  
        MaskedTextBox1.ValidatingType = GetType(System.DateTime)  
    End Sub  
    ```  
  
2. Fügen Sie einen Ereignishandler für das <xref:System.Windows.Forms.MaskedTextBox.TypeValidationCompleted>-Ereignis hinzu:  
  
    ```csharp  
    public void maskedTextBox1_TypeValidationCompleted(object sender, TypeValidationEventArgs e)  
    {  
        if (!e.IsValidInput)  
        {  
           toolTip1.ToolTipTitle = "Invalid Date Value";  
           toolTip1.Show("We're sorry, but the value you entered is not a valid date. Please change the value.", maskedTextBox1, 5000);  
           e.Cancel = true;  
        }  
    }  
    ```  
  
    ```vb  
    Public Sub MaskedTextBox1_TypeValidationCompleted(sender as Object, e as TypeValidationEventArgs)  
        If Not e.IsValidInput Then  
           ToolTip1.ToolTipTitle = "Invalid Date Value"  
           ToolTip1.Show("We're sorry, but the value you entered is not a valid date. Please change the value.", maskedTextBox1, 5000)  
           e.Cancel = True  
        End If  
    End Sub  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.MaskedTextBox>
- [MaskedTextBox-Steuerelement](maskedtextbox-control-windows-forms.md)
