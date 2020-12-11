---
title: 'Vorgehensweise: Anzeigen einer Farbpalette mit der ColorDialog-Komponente'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- palettes [Windows Forms], showing color
- color dialog box [Windows Forms], showing color palettes
- colors [Windows Forms], allowing users to select
- color palettes [Windows Forms], dialog box
- ColorDialog component [Windows Forms], showing color palettes
- color palettes [Windows Forms], showing in ColorDialog component
- colors [Windows Forms], showing palettes
ms.assetid: ee050f61-dbc8-4436-ba22-51360981ab48
ms.openlocfilehash: 0406ef7a32678bd149c0024348a7adf1f0b72926
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976645"
---
# <a name="how-to-show-a-color-palette-with-the-colordialog-component"></a>Vorgehensweise: Anzeigen einer Farbpalette mit der ColorDialog-Komponente
Die [Color Dialog](colordialog-component-windows-forms.md) -Komponente zeigt eine Palette von Farben an und gibt eine Eigenschaft mit der vom Benutzer ausgewählten Farbe zurück.  
  
### <a name="to-choose-a-color-using-the-colordialog-component"></a>So wählen Sie mithilfe der Color Dialog-Komponente eine Farbe aus  
  
1. Zeigen Sie das Dialogfeld mit der- <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode an.  
  
2. Verwenden Sie die- <xref:System.Windows.Forms.DialogResult> Eigenschaft, um zu bestimmen, wie das Dialogfeld geschlossen wurde.  
  
3. Verwenden Sie die- <xref:System.Windows.Forms.ColorDialog.Color%2A> Eigenschaft der- <xref:System.Windows.Forms.ColorDialog> Komponente, um die ausgewählte Farbe festzulegen.  
  
     Im folgenden Beispiel <xref:System.Windows.Forms.Button> öffnet der-Ereignishandler des-Steuer Elements <xref:System.Windows.Forms.Control.Click> eine- <xref:System.Windows.Forms.ColorDialog> Komponente. Wenn eine Farbe ausgewählt wird und der Benutzer auf **OK** klickt, <xref:System.Windows.Forms.Button> wird die Hintergrundfarbe des Steuer Elements auf die ausgewählte Farbe festgelegt. Im Beispiel wird davon ausgegangen, dass das Formular über ein <xref:System.Windows.Forms.Button> Steuerelement und eine <xref:System.Windows.Forms.ColorDialog> Komponente verfügt.  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, _  
    ByVal e As System.EventArgs) Handles Button1.Click  
       If ColorDialog1.ShowDialog() = DialogResult.OK Then  
          Button1.BackColor = ColorDialog1.Color  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)  
    {  
       if(colorDialog1.ShowDialog() == DialogResult.OK)  
       {  
          button1.BackColor = colorDialog1.Color;  
       }  
    }  
    ```  
  
    ```cpp  
    private:  
       void button1_Click(System::Object ^ sender,
          System::EventArgs ^ e)  
       {  
          if(colorDialog1->ShowDialog() == DialogResult::OK)  
          {  
             button1->BackColor = colorDialog1->Color;  
          }  
       }  
    ```  
  
     (Visual c#, Visual C++) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.  
  
    ```csharp  
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
    ```cpp  
    this->button1->Click +=
       gcnew System::EventHandler(this, &Form1::button1_Click);  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ColorDialog>
- [ColorDialog-Komponente](colordialog-component-windows-forms.md)
