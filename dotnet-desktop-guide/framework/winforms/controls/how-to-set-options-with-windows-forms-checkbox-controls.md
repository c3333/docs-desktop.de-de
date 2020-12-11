---
title: Festlegen von Optionen mit CheckBox-Steuerelementen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- checked
helpviewer_keywords:
- CheckBox control [Windows Forms], checked state
- check boxes [Windows Forms], using to set options
- CheckBox control [Windows Forms], using to set options
ms.assetid: 2ac70498-7e3e-4e07-8901-ccabaeb5fd3e
ms.openlocfilehash: 00b467836d8e60aeee51a010a6384abf7dd73c56
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975585"
---
# <a name="how-to-set-options-with-windows-forms-checkbox-controls"></a>Gewusst wie: Festlegen von Optionen mit CheckBox-Steuerelementen in Windows Forms
Ein Windows Forms <xref:System.Windows.Forms.CheckBox> -Steuerelement wird verwendet, um Benutzern die Optionen true/false oder yes/no zu übergeben. Das-Steuerelement zeigt ein Häkchen an, wenn es ausgewählt wird.  
  
### <a name="to-set-options-with-checkbox-controls"></a>So legen Sie Optionen mit CheckBox-Steuerelementen fest  
  
1. Überprüfen Sie den Wert der- <xref:System.Windows.Forms.CheckBox.Checked%2A> Eigenschaft, um den Status zu bestimmen, und verwenden Sie diesen Wert, um eine Option festzulegen.  
  
     Wenn im folgenden Codebeispiel das <xref:System.Windows.Forms.CheckBox> -Ereignis des-Steuer Elements <xref:System.Windows.Forms.CheckBox.CheckedChanged> ausgelöst wird, wird die-Eigenschaft des Formulars <xref:System.Windows.Forms.Control.AllowDrop%2A> auf festgelegt, `false` Wenn das Kontrollkästchen aktiviert ist. Dies ist nützlich für Situationen, in denen die Benutzerinteraktion eingeschränkt werden soll.  
  
    ```vb  
    Private Sub CheckBox1_CheckedChanged(ByVal sender As System.Object, _  
       ByVal e As System.EventArgs) Handles CheckBox1.CheckedChanged  
       ' Determine the CheckState of the check box.  
       If CheckBox1.CheckState = CheckState.Checked Then  
          ' If checked, do not allow items to be dragged onto the form.  
          Me.AllowDrop = False  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void checkBox1_CheckedChanged(object sender, System.EventArgs e)  
    {  
       // Determine the CheckState of the check box.  
       if (checkBox1.CheckState == CheckState.Checked)
       {  
          // If checked, do not allow items to be dragged onto the form.  
          this.AllowDrop = false;  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void checkBox1_CheckedChanged(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          // Determine the CheckState of the check box.  
          if (checkBox1->CheckState == CheckState::Checked)
          {  
             // If checked, do not allow items to be dragged onto the form.  
             this->AllowDrop = false;  
          }  
       }  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.CheckBox>
- [Übersicht über das CheckBox-Steuerelement](checkbox-control-overview-windows-forms.md)
- [Gewusst wie: Reagieren auf das Klicken auf Kontrollkästchen in Windows Forms](how-to-respond-to-windows-forms-checkbox-clicks.md)
- [CheckBox-Steuerelement](checkbox-control-windows-forms.md)
