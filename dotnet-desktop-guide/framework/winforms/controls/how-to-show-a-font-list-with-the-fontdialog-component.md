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
# <a name="how-to-show-a-font-list-with-the-fontdialog-component"></a><span data-ttu-id="3d8ce-102">Vorgehensweise: Anzeigen einer Schriftartenliste mit der FontDialog-Komponente</span><span class="sxs-lookup"><span data-stu-id="3d8ce-102">How to: Show a Font List with the FontDialog Component</span></span>
<span data-ttu-id="3d8ce-103">Mit der [FontDialog](fontdialog-component-windows-forms.md) -Komponente können Benutzer eine Schriftart auswählen und deren Anzeige Aspekte ändern, wie z. b. die Gewichtung und die Größe.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-103">The [FontDialog](fontdialog-component-windows-forms.md) component allows users to select a font, as well as change its display aspects, such as its weight and size.</span></span>  
  
 <span data-ttu-id="3d8ce-104">Die im Dialogfeld ausgewählte Schriftart wird in der-Eigenschaft zurückgegeben <xref:System.Windows.Forms.FontDialog.Font%2A> .</span><span class="sxs-lookup"><span data-stu-id="3d8ce-104">The font selected in the dialog box is returned in the <xref:System.Windows.Forms.FontDialog.Font%2A> property.</span></span> <span data-ttu-id="3d8ce-105">Daher ist die Nutzung der vom Benutzer ausgewählten Schriftart genauso einfach wie das Lesen einer Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-105">Thus, taking advantage of the font selected by the user is as easy as reading a property.</span></span>  
  
### <a name="to-select-font-properties-using-the-fontdialog-component"></a><span data-ttu-id="3d8ce-106">So wählen Sie Schriftart Eigenschaften mit der FontDialog-Komponente aus</span><span class="sxs-lookup"><span data-stu-id="3d8ce-106">To select font properties using the FontDialog Component</span></span>  
  
1. <span data-ttu-id="3d8ce-107">Zeigen Sie das Dialogfeld mit der- <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode an.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-107">Display the dialog box using the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method.</span></span>  
  
2. <span data-ttu-id="3d8ce-108">Verwenden Sie die- <xref:System.Windows.Forms.DialogResult> Eigenschaft, um zu bestimmen, wie das Dialogfeld geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-108">Use the <xref:System.Windows.Forms.DialogResult> property to determine how the dialog box was closed.</span></span>  
  
3. <span data-ttu-id="3d8ce-109">Verwenden Sie die- <xref:System.Windows.Forms.FontDialog.Font%2A> Eigenschaft, um die gewünschte Schriftart festzulegen.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-109">Use the <xref:System.Windows.Forms.FontDialog.Font%2A> property to set the desired font.</span></span>  
  
     <span data-ttu-id="3d8ce-110">Im folgenden Beispiel <xref:System.Windows.Forms.Button> öffnet der-Ereignishandler des-Steuer Elements <xref:System.Windows.Forms.Control.Click> eine- <xref:System.Windows.Forms.FontDialog> Komponente.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-110">In the example below, the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Click> event handler opens a <xref:System.Windows.Forms.FontDialog> component.</span></span> <span data-ttu-id="3d8ce-111">Wenn eine Schriftart ausgewählt wird und der Benutzer auf **OK** klickt, <xref:System.Windows.Forms.FontDialog.Font%2A> wird die-Eigenschaft eines <xref:System.Windows.Forms.TextBox> Steuer Elements auf dem Formular auf die gewählte Schriftart festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-111">When a font is chosen and the user clicks **OK**, the <xref:System.Windows.Forms.FontDialog.Font%2A> property of a <xref:System.Windows.Forms.TextBox> control that is on the form is set to the chosen font.</span></span> <span data-ttu-id="3d8ce-112">Das Beispiel setzt voraus, dass das Formular über ein <xref:System.Windows.Forms.Button> Steuerelement, ein  <xref:System.Windows.Forms.TextBox> -Steuerelement und eine- <xref:System.Windows.Forms.FontDialog> Komponente verfügt.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-112">The example assumes your form has a <xref:System.Windows.Forms.Button> control, a  <xref:System.Windows.Forms.TextBox> control, and a <xref:System.Windows.Forms.FontDialog> component.</span></span>  
  
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
  
     <span data-ttu-id="3d8ce-113">(Visual c# und Visual C++) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="3d8ce-113">(Visual C# and Visual C++) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
    ```cpp  
    button1->Click += gcnew System::EventHandler(this, &Form1::button1_Click);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="3d8ce-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d8ce-114">See also</span></span>

- <xref:System.Windows.Forms.FontDialog>
- [<span data-ttu-id="3d8ce-115">FontDialog-Komponente</span><span class="sxs-lookup"><span data-stu-id="3d8ce-115">FontDialog Component</span></span>](fontdialog-component-windows-forms.md)
