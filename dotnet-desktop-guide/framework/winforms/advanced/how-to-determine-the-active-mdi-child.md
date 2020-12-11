---
title: 'Vorgehensweise: Bestimmen des aktiven untergeordneten MDI-Elements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Clipboard [Windows Forms], copying data to
- MDI [Windows Forms], child windows
- child forms
- MDI [Windows Forms], activating forms
- MDI [Windows Forms], locating focus
ms.assetid: 33880ec3-0207-4c2b-a616-ff140443cc0f
ms.openlocfilehash: 57491faa10c182630d41565ba236d65e393929b3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972360"
---
# <a name="how-to-determine-the-active-mdi-child"></a><span data-ttu-id="2e0c1-102">Vorgehensweise: Bestimmen des aktiven untergeordneten MDI-Elements</span><span class="sxs-lookup"><span data-stu-id="2e0c1-102">How to: Determine the Active MDI Child</span></span>
<span data-ttu-id="2e0c1-103">Gelegentlich möchten Sie einen Befehl bereitstellen, der auf dem Steuerelement mit Fokus auf das momentan aktive untergeordnete Formular basiert.</span><span class="sxs-lookup"><span data-stu-id="2e0c1-103">On occasion, you will want to provide a command that operates on the control that has focus on the currently active child form.</span></span> <span data-ttu-id="2e0c1-104">Angenommen, Sie möchten den ausgewählten Text aus dem Textfeld des untergeordneten Formulars in die Zwischenablage kopieren.</span><span class="sxs-lookup"><span data-stu-id="2e0c1-104">For example, suppose you want to copy selected text from the child form's text box to the Clipboard.</span></span> <span data-ttu-id="2e0c1-105">Erstellen Sie eine Prozedur, die markierten Text in die Zwischenablage kopiert, indem Sie das- <xref:System.Windows.Forms.Control.Click> Ereignis des Menü Elements Kopieren im Standardmenü Bearbeiten verwenden.</span><span class="sxs-lookup"><span data-stu-id="2e0c1-105">You would create a procedure that copies selected text to the Clipboard using the <xref:System.Windows.Forms.Control.Click> event of the Copy menu item on the standard Edit menu.</span></span>  
  
 <span data-ttu-id="2e0c1-106">Da eine MDI-Anwendung viele Instanzen desselben untergeordneten Formulars aufweisen kann, muss die Prozedur wissen, welches Formular verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2e0c1-106">Because an MDI application can have many instances of the same child form, the procedure needs to know which form to use.</span></span> <span data-ttu-id="2e0c1-107">Um das richtige Formular anzugeben, verwenden Sie die- <xref:System.Windows.Forms.Form.ActiveMdiChild%2A> Eigenschaft, die das untergeordnete Formular zurückgibt, das den Fokus besitzt oder das zuletzt aktiv war.</span><span class="sxs-lookup"><span data-stu-id="2e0c1-107">To specify the correct form, use the <xref:System.Windows.Forms.Form.ActiveMdiChild%2A> property, which returns the child form that has the focus or that was most recently active.</span></span>  
  
 <span data-ttu-id="2e0c1-108">Wenn Sie mehrere Steuerelemente auf einem Formular haben, müssen Sie auch angeben, welches Steuerelement aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="2e0c1-108">When you have several controls on a form, you also need to specify which control is active.</span></span> <span data-ttu-id="2e0c1-109">Wie die- <xref:System.Windows.Forms.Form.ActiveMdiChild%2A> Eigenschaft gibt die- <xref:System.Windows.Forms.ContainerControl.ActiveControl%2A> Eigenschaft das-Steuerelement mit dem Fokus auf das aktive untergeordnete Formular zurück.</span><span class="sxs-lookup"><span data-stu-id="2e0c1-109">Like the <xref:System.Windows.Forms.Form.ActiveMdiChild%2A> property, the <xref:System.Windows.Forms.ContainerControl.ActiveControl%2A> property returns the control with the focus on the active child form.</span></span> <span data-ttu-id="2e0c1-110">Im folgenden Verfahren wird eine Kopier Prozedur veranschaulicht, die über ein untergeordnetes Formular Menü, ein Menü auf dem MDI-Formular oder eine Symbolleisten-Schaltfläche aufgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2e0c1-110">The procedure below illustrates a copy procedure that can be called from a child form menu, a menu on the MDI form, or a toolbar button.</span></span>  
  
### <a name="to-determine-the-active-mdi-child-to-copy-its-text-to-the-clipboard"></a><span data-ttu-id="2e0c1-111">So bestimmen Sie das aktive untergeordnete MDI-Element (um den Text in die Zwischenablage zu kopieren)</span><span class="sxs-lookup"><span data-stu-id="2e0c1-111">To determine the active MDI child (to copy its text to the Clipboard)</span></span>  
  
1. <span data-ttu-id="2e0c1-112">Kopieren Sie in einer Methode den Text des aktiven Steuer Elements des aktiven untergeordneten Formulars in die Zwischenablage.</span><span class="sxs-lookup"><span data-stu-id="2e0c1-112">Within a method, copy the text of the active control of the active child form to the Clipboard.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="2e0c1-113">In diesem Beispiel wird davon ausgegangen, dass ein übergeordnetes MDI-Formular () vorhanden ist, das mindestens ein untergeordnetes `Form1` MDI-Fenster mit einem- <xref:System.Windows.Forms.RichTextBox> Steuerelement</span><span class="sxs-lookup"><span data-stu-id="2e0c1-113">This example assumes there is an MDI parent form (`Form1`) that has one or more MDI child windows containing a <xref:System.Windows.Forms.RichTextBox> control.</span></span> <span data-ttu-id="2e0c1-114">Weitere Informationen finden Sie unter [Erstellen von übergeordneten MDI-Formularen](how-to-create-mdi-parent-forms.md).</span><span class="sxs-lookup"><span data-stu-id="2e0c1-114">For more information, see [Creating MDI Parent Forms](how-to-create-mdi-parent-forms.md).</span></span>  
  
    ```vb  
    Public Sub mniCopy_Click(ByVal sender As Object, _  
       ByVal e As System.EventArgs) Handles mniCopy.Click  
  
       ' Determine the active child form.  
       Dim activeChild As Form = Me.ActiveMDIChild  
  
       ' If there is an active child form, find the active control, which  
       ' in this example should be a RichTextBox.  
       If (Not activeChild Is Nothing) Then  
          Dim theBox As RichTextBox = _  
            TryCast(activeChild.ActiveControl, RichTextBox)  
  
          If (Not theBox Is Nothing) Then  
             'Put selected text on Clipboard.  
             Clipboard.SetDataObject(theBox.SelectedText)  
          Else  
             MessageBox.Show("You need to select a RichTextBox.")  
          End If  
       End If  
    End Sub  
    ```  
  
    ```csharp  
    protected void mniCopy_Click (object sender, System.EventArgs e)  
    {  
       // Determine the active child form.  
       Form activeChild = this.ActiveMdiChild;  
  
       // If there is an active child form, find the active control, which  
       // in this example should be a RichTextBox.  
       if (activeChild != null)  
       {
          try  
          {  
             RichTextBox theBox = (RichTextBox)activeChild.ActiveControl;  
             if (theBox != null)  
             {  
                // Put the selected text on the Clipboard.  
                Clipboard.SetDataObject(theBox.SelectedText);  
  
             }  
          }  
          catch  
          {  
             MessageBox.Show("You need to select a RichTextBox.");  
          }  
       }  
    }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="2e0c1-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2e0c1-115">See also</span></span>

- [<span data-ttu-id="2e0c1-116">MDI-Anwendungen (Multiple Document Interface)</span><span class="sxs-lookup"><span data-stu-id="2e0c1-116">Multiple-Document Interface (MDI) Applications</span></span>](multiple-document-interface-mdi-applications.md)
- [<span data-ttu-id="2e0c1-117">Vorgehensweise: Erstellen von übergeordneten MDI-Formularen</span><span class="sxs-lookup"><span data-stu-id="2e0c1-117">How to: Create MDI Parent Forms</span></span>](how-to-create-mdi-parent-forms.md)
- [<span data-ttu-id="2e0c1-118">Vorgehensweise: Erstellen von untergeordneten MDI-Formularen</span><span class="sxs-lookup"><span data-stu-id="2e0c1-118">How to: Create MDI Child Forms</span></span>](how-to-create-mdi-child-forms.md)
- [<span data-ttu-id="2e0c1-119">Vorgehensweise: Senden von Daten an das aktive untergeordnete MDI-Element</span><span class="sxs-lookup"><span data-stu-id="2e0c1-119">How to: Send Data to the Active MDI Child</span></span>](how-to-send-data-to-the-active-mdi-child.md)
- [<span data-ttu-id="2e0c1-120">Vorgehensweise: Anordnen von untergeordneten MDI-Formularen</span><span class="sxs-lookup"><span data-stu-id="2e0c1-120">How to: Arrange MDI Child Forms</span></span>](how-to-arrange-mdi-child-forms.md)
