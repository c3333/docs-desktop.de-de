---
title: Reagieren auf CheckBox-Klicks
description: Erfahren Sie, wie Sie Ihre Windows Forms Anwendung programmieren, um je nach Zustand des Kontrollkästchens Aktionen auszuführen.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Click event [Windows Forms], CheckBox control
- CheckBox control [Windows Forms], Click events
- events [Windows Forms], Click events
- double-clicks
- check boxes [Windows Forms], responding to events
ms.assetid: c39f901e-8899-43b6-aa31-939cbf7089fb
ms.openlocfilehash: 58944bc421f990343b6c58484aaab3d79c8bda5e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975600"
---
# <a name="how-to-respond-to-windows-forms-checkbox-clicks"></a>Gewusst wie: Reagieren auf das Klicken auf Kontrollkästchen in Windows Forms
Wenn ein Benutzer auf ein Windows Forms-Steuerelement klickt <xref:System.Windows.Forms.CheckBox> , tritt das- <xref:System.Windows.Forms.Control.Click> Ereignis auf. Sie können Ihre Anwendung so programmieren, dass je nach Zustand des Kontrollkästchens Aktionen ausgeführt werden.  
  
### <a name="to-respond-to-checkbox-clicks"></a>So reagieren Sie auf CheckBox-Klicks  
  
1. <xref:System.Windows.Forms.Control.Click>Verwenden Sie im-Ereignishandler die <xref:System.Windows.Forms.CheckBox.Checked%2A> -Eigenschaft, um den Zustand des Steuer Elements zu bestimmen und alle notwendigen Aktionen auszuführen.  
  
    ```vb  
    Private Sub CheckBox1_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles CheckBox1.Click  
       ' The CheckBox control's Text property is changed each time the
       ' control is clicked, indicating a checked or unchecked state.  
       If CheckBox1.Checked = True Then  
          CheckBox1.Text = "Checked"  
       Else  
          CheckBox1.Text = "Unchecked"  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void checkBox1_Click(object sender, System.EventArgs e)  
    {  
       // The CheckBox control's Text property is changed each time the
       // control is clicked, indicating a checked or unchecked state.  
       if (checkBox1.Checked)  
       {  
          checkBox1.Text = "Checked";  
       }  
       else  
       {  
          checkBox1.Text = "Unchecked";  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void checkBox1_CheckedChanged(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          if (checkBox1->Checked)  
          {  
             checkBox1->Text = "Checked";  
          }  
          else  
          {  
             checkBox1->Text = "Unchecked";  
          }  
       }  
    ```  
  
    > [!NOTE]
    > Wenn der Benutzer versucht, auf das Steuerelement zu doppelklicken <xref:System.Windows.Forms.CheckBox> , wird jeder Klick separat verarbeitet, d. h <xref:System.Windows.Forms.CheckBox> ., das Steuerelement unterstützt das Doppelklick Ereignis nicht.  
  
    > [!NOTE]
    > Wenn die- <xref:System.Windows.Forms.CheckBox.AutoCheck%2A> Eigenschaft ist `true` (Standardeinstellung), <xref:System.Windows.Forms.CheckBox> wird automatisch ausgewählt oder gelöscht, wenn darauf geklickt wird. Andernfalls müssen Sie die-Eigenschaft manuell festlegen, <xref:System.Windows.Forms.CheckBox.Checked%2A> Wenn das- <xref:System.Windows.Forms.Control.Click> Ereignis auftritt.  
  
     Sie können auch das- <xref:System.Windows.Forms.CheckBox> Steuerelement verwenden, um eine Vorgehensweise zu bestimmen.  
  
### <a name="to-determine-a-course-of-action-when-a-check-box-is-clicked"></a>So bestimmen Sie eine Vorgehensweise, wenn auf ein Kontrollkästchen geklickt wird  
  
1. Verwenden Sie eine Case-Anweisung, um den Wert der-Eigenschaft abzufragen <xref:System.Windows.Forms.CheckBox.CheckState%2A> , um eine Vorgehensweise zu bestimmen. Wenn die- <xref:System.Windows.Forms.CheckBox.ThreeState%2A> Eigenschaft auf festgelegt ist `true` , gibt die- <xref:System.Windows.Forms.CheckBox.CheckState%2A> Eigenschaft möglicherweise drei mögliche Werte zurück, die das Kontrollkästchen darstellen, das Kontrollkästchen deaktiviert ist, oder einen dritten unbestimmten Zustand, in dem das Feld mit einer Abbild Darstellung angezeigt wird, um anzugeben, dass die Option nicht verfügbar ist.  
  
    ```vb  
    Private Sub CheckBox1_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles CheckBox1.Click  
       Select Case CheckBox1.CheckState  
          Case CheckState.Checked  
             ' Code for checked state.  
          Case CheckState.Unchecked  
             ' Code for unchecked state.  
          Case CheckState.Indeterminate  
             ' Code for indeterminate state.  
       End Select
    End Sub  
    ```  
  
    ```csharp  
    private void checkBox1_Click(object sender, System.EventArgs e)  
    {  
       switch(checkBox1.CheckState)  
       {  
          case CheckState.Checked:  
             // Code for checked state.  
             break;  
          case CheckState.Unchecked:  
             // Code for unchecked state.  
             break;  
          case CheckState.Indeterminate:  
             // Code for indeterminate state.  
             break;  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void checkBox1_CheckedChanged(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          switch(checkBox1->CheckState) {  
             case CheckState::Checked:  
                // Code for checked state.  
                break;  
             case CheckState::Unchecked:  
                // Code for unchecked state.  
                break;  
             case CheckState::Indeterminate:  
                // Code for indeterminate state.  
                break;  
          }  
       }  
    ```  
  
    > [!NOTE]
    > Wenn die <xref:System.Windows.Forms.CheckBox.ThreeState%2A> -Eigenschaft auf festgelegt ist `true` , <xref:System.Windows.Forms.CheckBox.Checked%2A> gibt die `true` -Eigenschaft sowohl für <xref:System.Windows.Forms.CheckState.Checked> als auch für zurück <xref:System.Windows.Forms.CheckState.Indeterminate> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.CheckBox>
- [Übersicht über das CheckBox-Steuerelement](checkbox-control-overview-windows-forms.md)
- [Gewusst wie: Festlegen von Optionen mit CheckBox-Steuerelementen in Windows Forms](how-to-set-options-with-windows-forms-checkbox-controls.md)
- [CheckBox-Steuerelement](checkbox-control-windows-forms.md)
