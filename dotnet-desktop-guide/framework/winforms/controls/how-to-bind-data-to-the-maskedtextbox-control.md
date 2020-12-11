---
title: 'Vorgehensweise: Binden von Daten an das MaskedTextBox-Steuerelement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- MaskedTextBox control [Windows Forms]
- data binding [Windows Forms], MaskedTextBox control [Windows Forms]
- MaskedTextBox control [Windows Forms], binding data
ms.assetid: 34b29f07-e8df-48d4-b08b-53fcca524708
ms.openlocfilehash: 0cbb239e24b254c37c453486590185e934adf482
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975715"
---
# <a name="how-to-bind-data-to-the-maskedtextbox-control"></a>Vorgehensweise: Binden von Daten an das MaskedTextBox-Steuerelement
Sie können Daten <xref:System.Windows.Forms.MaskedTextBox> wie jedes andere Windows Forms Steuerelement an ein Steuerelement binden. Wenn das Format der Daten in der Datenbank jedoch nicht mit dem Format identisch ist, das von ihrer Masken Definition erwartet wird, müssen Sie die Daten neu formatieren. Im folgenden Verfahren wird veranschaulicht, wie dies mithilfe der <xref:System.Windows.Forms.Binding.Format> -und- <xref:System.Windows.Forms.Binding.Parse> Ereignisse der- <xref:System.Windows.Forms.Binding> Klasse durchzuführen ist, um separate Felder für Telefonnummern und Telefon Erweiterungs Datenbanken als einzelnes bearbeitbares Feld anzuzeigen.  
  
 Das folgende Verfahren erfordert, dass Sie Zugriff auf eine SQL Server Datenbank haben, auf der die Beispieldatenbank "Northwind" installiert ist.  
  
### <a name="to-bind-data-to-a-maskedtextbox-control"></a>So binden Sie Daten an ein MaskedTextBox-Steuerelement  
  
1. Erstellen Sie ein neues Windows Forms-Projekt.  
  
2. Ziehen <xref:System.Windows.Forms.TextBox> Sie zwei-Steuerelemente auf das Formular, benennen Sie Sie `FirstName` und `LastName` .  
  
3. Ziehen Sie ein- <xref:System.Windows.Forms.MaskedTextBox> Steuerelement auf das Formular, benennen Sie es `PhoneMask` .  
  
4. Legen Sie die- <xref:System.Windows.Forms.MaskedTextBox.Mask%2A> Eigenschaft von `PhoneMask` auf fest `(000) 000-0000 x9999` .  
  
5. Fügen Sie dem Formular die folgenden Namespace Importe hinzu.  
  
    ```csharp  
    using System.Data.SqlClient;  
    ```  
  
    ```vb  
    Imports System.Data.SqlClient  
    ```  
  
6. Klicken Sie mit der rechten Maustaste, und wählen Sie **Code anzeigen** aus. Platzieren Sie diesen Code an einer beliebigen Stelle in der Formular Klasse.  
  
    ```csharp  
    Binding currentBinding, phoneBinding;  
    DataSet employeesTable = new DataSet();  
    SqlConnection sc;  
    SqlDataAdapter dataConnect;  
  
    private void Form1_Load(object sender, EventArgs e)  
    {  
        DoMaskBinding();  
    }  
  
    private void DoMaskBinding()  
    {  
        try  
        {  
            sc = new SqlConnection("Data Source=CLIENTUE;Initial Catalog=NORTHWIND;Integrated Security=SSPI");  
            sc.Open();  
        }  
        catch (Exception ex)  
        {  
            MessageBox.Show(ex.Message);  
            return;  
        }  
  
        dataConnect = new SqlDataAdapter("SELECT * FROM Employees", sc);  
        dataConnect.Fill(employeesTable, "Employees");  
  
        // Now bind MaskedTextBox to appropriate field. Note that we must create the Binding objects  
        // before adding them to the control - otherwise, we won't get a Format event on the
        // initial load.
        try  
        {  
            currentBinding = new Binding("Text", employeesTable, "Employees.FirstName");  
            firstName.DataBindings.Add(currentBinding);  
  
            currentBinding = new Binding("Text", employeesTable, "Employees.LastName");  
            lastName.DataBindings.Add(currentBinding);  
  
            phoneBinding =new Binding("Text", employeesTable, "Employees.HomePhone");  
            // We must add the event handlers before we bind, or the Format event will not get called  
            // for the first record.  
            phoneBinding.Format += new ConvertEventHandler(phoneBinding_Format);  
            phoneBinding.Parse += new ConvertEventHandler(phoneBinding_Parse);  
            phoneMask.DataBindings.Add(phoneBinding);  
        }  
        catch (Exception ex)  
        {  
            MessageBox.Show(ex.Message);  
            return;  
        }  
    }  
    ```  
  
    ```vb  
    Dim WithEvents CurrentBinding, PhoneBinding As Binding  
    Dim EmployeesTable As New DataSet()  
    Dim sc As SqlConnection  
    Dim DataConnect As SqlDataAdapter  
  
    Private Sub Form1_Load(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles MyBase.Load  
        DoMaskedBinding()  
    End Sub  
  
    Private Sub DoMaskedBinding()  
        Try  
            sc = New SqlConnection("Data Source=SERVERNAME;Initial Catalog=NORTHWIND;Integrated Security=SSPI")  
            sc.Open()  
        Catch ex As Exception  
            MessageBox.Show(ex.Message)  
            Exit Sub  
        End Try  
  
        DataConnect = New SqlDataAdapter("SELECT * FROM Employees", sc)  
        DataConnect.Fill(EmployeesTable, "Employees")  
  
        ' Now bind MaskedTextBox to appropriate field. Note that we must create the Binding objects  
        ' before adding them to the control - otherwise, we won't get a Format event on the
        ' initial load.  
        Try  
            CurrentBinding = New Binding("Text", EmployeesTable, "Employees.FirstName")  
            firstName.DataBindings.Add(CurrentBinding)  
            CurrentBinding = New Binding("Text", EmployeesTable, "Employees.LastName")  
            lastName.DataBindings.Add(CurrentBinding)  
            PhoneBinding = New Binding("Text", EmployeesTable, "Employees.HomePhone")  
            PhoneMask.DataBindings.Add(PhoneBinding)  
        Catch ex As Exception  
            MessageBox.Show(ex.Message)  
            Application.Exit()  
        End Try  
    End Sub  
    ```  
  
7. Fügen Sie Ereignishandler für das-Ereignis und das-Ereignis hinzu <xref:System.Windows.Forms.Binding.Format> <xref:System.Windows.Forms.Binding.Parse> , um die `PhoneNumber` Felder und vom gebundenen zu kombinieren und zu trennen `Extension` <xref:System.Data.DataSet> .  
  
    ```csharp  
    private void phoneBinding_Format(Object sender, ConvertEventArgs e)  
    {  
        String ext;  
  
        DataRowView currentRow = (DataRowView)BindingContext[employeesTable, "Employees"].Current;  
        if (currentRow["Extension"] == null)
        {  
            ext = "";  
        } else
        {  
            ext = currentRow["Extension"].ToString();  
        }  
  
        e.Value = e.Value.ToString().Trim() + " x" + ext;  
    }  
  
    private void phoneBinding_Parse(Object sender, ConvertEventArgs e)  
    {  
        String phoneNumberAndExt = e.Value.ToString();  
  
        int extIndex = phoneNumberAndExt.IndexOf("x");  
        String ext = phoneNumberAndExt.Substring(extIndex).Trim();  
        String phoneNumber = phoneNumberAndExt.Substring(0, extIndex).Trim();  
  
        //Get the current binding object, and set the new extension manually.
        DataRowView currentRow = (DataRowView)BindingContext[employeesTable, "Employees"].Current;  
        // Remove the "x" from the extension.  
        currentRow["Extension"] = ext.Substring(1);  
  
        //Return the phone number.  
        e.Value = phoneNumber;  
    }  
    ```  
  
    ```vb  
    Private Sub PhoneBinding_Format(ByVal sender As Object, ByVal e As ConvertEventArgs) Handles PhoneBinding.Format  
        Dim Ext As String  
  
        Dim CurrentRow As DataRowView = CType(Me.BindingContext(EmployeesTable, "Employees").Current, DataRowView)  
        If (CurrentRow("Extension") Is Nothing) Then  
            Ext = ""  
        Else  
            Ext = CurrentRow("Extension").ToString()  
        End If  
  
        e.Value = e.Value.ToString().Trim() & " x" & Ext  
    End Sub  
  
    Private Sub PhoneBinding_Parse(ByVal sender As Object, ByVal e As ConvertEventArgs) Handles PhoneBinding.Parse  
        Dim PhoneNumberAndExt As String = e.Value.ToString()  
  
        Dim ExtIndex As Integer = PhoneNumberAndExt.IndexOf("x")  
        Dim Ext As String = PhoneNumberAndExt.Substring(ExtIndex).Trim()  
        Dim PhoneNumber As String = PhoneNumberAndExt.Substring(0, ExtIndex).Trim()  
  
        ' Get the current binding object, and set the new extension manually.
        Dim CurrentRow As DataRowView = CType(Me.BindingContext(EmployeesTable, "Employees").Current, DataRowView)  
        ' Remove the "x" from the extension.  
        CurrentRow("Extension") = CObj(Ext.Substring(1))  
  
        ' Return the phone number.  
        e.Value = PhoneNumber  
    End Sub  
    ```  
  
8. Fügen Sie <xref:System.Windows.Forms.Button> dem Formular zwei-Steuerelemente hinzu. Benennen Sie Sie `previousButton` und `nextButton` . Doppelklicken Sie auf jede Schaltfläche, um einen <xref:System.Windows.Forms.Control.Click> -Ereignishandler hinzuzufügen, und füllen Sie die Ereignishandler aus, wie im folgenden Codebeispiel gezeigt.  
  
    ```csharp  
    private void previousButton_Click(object sender, EventArgs e)  
    {  
        BindingContext[employeesTable, "Employees"].Position = BindingContext[employeesTable, "Employees"].Position - 1;  
    }  
  
    private void nextButton_Click(object sender, EventArgs e)  
    {  
        BindingContext[employeesTable, "Employees"].Position = BindingContext[employeesTable, "Employees"].Position + 1;  
    }  
    ```  
  
    ```vb  
    Private Sub PreviousButton_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles PreviousButton.Click  
        Me.BindingContext(EmployeesTable, "Employees").Position = Me.BindingContext(EmployeesTable, "Employees").Position - 1  
    End Sub  
  
    Private Sub NextButton_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles NextButton.Click  
        Me.BindingContext(EmployeesTable, "Employees").Position = Me.BindingContext(EmployeesTable, "Employees").Position + 1  
    End Sub  
    ```  
  
9. Führen Sie das Beispiel aus. Bearbeiten Sie die Daten, und verwenden **Sie die Schalt** Flächen zurück und **weiter** , um festzustellen, ob die Daten ordnungsgemäß in der gespeichert werden <xref:System.Data.DataSet> .  
  
## <a name="example"></a>Beispiel  
 Das folgende Codebeispiel ist das vollständige Codelisting, das sich aus der Ausführung des vorherigen Verfahrens ergibt.  
  
 [!code-cpp[MaskedTextBoxData#1](~/samples/snippets/cpp/VS_Snippets_Winforms/MaskedTextBoxData/cpp/form1.cpp#1)]
 [!code-csharp[MaskedTextBoxData#1](~/samples/snippets/csharp/VS_Snippets_Winforms/MaskedTextBoxData/CS/form1.cs#1)]
 [!code-vb[MaskedTextBoxData#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/MaskedTextBoxData/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
  
- Erstellen Sie ein Visual c#-oder Visual Basic-Projekt.  
  
- Fügen Sie dem Formular die Steuer <xref:System.Windows.Forms.TextBox> Elemente und hinzu <xref:System.Windows.Forms.MaskedTextBox> , wie im vorherigen Verfahren beschrieben.  
  
- Öffnen Sie die Quell Code Datei für das Standardformular des Projekts.  
  
- Ersetzen Sie den Quellcode in dieser Datei durch den Code, der im vorherigen Abschnitt "Code" aufgeführt ist.  
  
- Kompilieren Sie die Anwendung.  
  
## <a name="see-also"></a>Siehe auch

- [Exemplarische Vorgehensweise: Arbeiten mit dem MaskedTextBox-Steuerelement](walkthrough-working-with-the-maskedtextbox-control.md)
