---
title: Anzeigen der Seitenansicht in Windows Forms-apps
titleSuffix: ''
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- print preview [Windows Forms], displaying
- printing [Windows Forms], print preview
- examples [Windows Forms], print preview
ms.assetid: e394134c-0886-4517-bd8d-edc4a3749eb5
ms.openlocfilehash: 7737cd06001f9acfde5eb44fdff9aaa880f23e79
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975658"
---
# <a name="how-to-display-print-preview-in-windows-forms-applications"></a><span data-ttu-id="ba000-102">Vorgehensweise: Anzeigen der Seitenansicht in Windows Forms-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="ba000-102">How to: Display Print Preview in Windows Forms Applications</span></span>
<span data-ttu-id="ba000-103">Sie können das-Steuerelement verwenden, <xref:System.Windows.Forms.PrintPreviewDialog> um Benutzern das Anzeigen eines Dokuments zu ermöglichen, das häufig vor dem Drucken angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba000-103">You can use the <xref:System.Windows.Forms.PrintPreviewDialog> control to enable users to display a document, often before it is to be printed.</span></span>  
  
 <span data-ttu-id="ba000-104">Zu diesem Zweck müssen Sie eine Instanz der- <xref:System.Drawing.Printing.PrintDocument> Klasse angeben. Dies ist das Dokument, das gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba000-104">To do this, you need to specify an instance of the <xref:System.Drawing.Printing.PrintDocument> class; this is the document to be printed.</span></span> <span data-ttu-id="ba000-105">Weitere Informationen zum Verwenden der Druckvorschau mit der-Komponente finden Sie unter Gewusst <xref:System.Drawing.Printing.PrintDocument> [wie: Drucken in Windows Forms mithilfe](../advanced/how-to-print-in-windows-forms-using-print-preview.md)der Seitenansicht.</span><span class="sxs-lookup"><span data-stu-id="ba000-105">For more information about using print preview with the <xref:System.Drawing.Printing.PrintDocument> component, see [How to: Print in Windows Forms Using Print Preview](../advanced/how-to-print-in-windows-forms-using-print-preview.md).</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ba000-106"><xref:System.Windows.Forms.PrintPreviewDialog>Damit das Steuerelement zur Laufzeit verwendet werden kann, muss auf dem Computer entweder lokal oder über ein Netzwerk ein Drucker installiert sein, da dies dazu führt, dass die <xref:System.Windows.Forms.PrintPreviewDialog> Komponente bestimmt, wie ein Dokument gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ba000-106">To use the <xref:System.Windows.Forms.PrintPreviewDialog> control at run time, users must have a printer installed on their computer, either locally or through a network, as this is partly how the <xref:System.Windows.Forms.PrintPreviewDialog> component determines how a document will look when printed.</span></span>  
  
 <span data-ttu-id="ba000-107">Das- <xref:System.Windows.Forms.PrintPreviewDialog> Steuerelement verwendet die- <xref:System.Drawing.Printing.PrinterSettings> Klasse.</span><span class="sxs-lookup"><span data-stu-id="ba000-107">The <xref:System.Windows.Forms.PrintPreviewDialog> control uses the <xref:System.Drawing.Printing.PrinterSettings> class.</span></span> <span data-ttu-id="ba000-108">Außerdem verwendet das <xref:System.Windows.Forms.PrintPreviewDialog> Steuerelement die- <xref:System.Drawing.Printing.PageSettings> Klasse, genauso wie die- <xref:System.Windows.Forms.PrintPreviewDialog> Komponente.</span><span class="sxs-lookup"><span data-stu-id="ba000-108">Additionally, the <xref:System.Windows.Forms.PrintPreviewDialog> control uses the <xref:System.Drawing.Printing.PageSettings> class, just as the <xref:System.Windows.Forms.PrintPreviewDialog> component does.</span></span> <span data-ttu-id="ba000-109">Das in der-Eigenschaft des-Steuer Elements angegebene Druck Dokument <xref:System.Windows.Forms.PrintPreviewDialog> <xref:System.Windows.Forms.PrintPreviewControl.Document%2A> bezieht sich auf Instanzen der <xref:System.Drawing.Printing.PrinterSettings> -Klasse und der- <xref:System.Drawing.Printing.PageSettings> Klasse, die zum Rendering des Dokuments im Vorschaufenster verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba000-109">The print document specified in the <xref:System.Windows.Forms.PrintPreviewDialog> control's <xref:System.Windows.Forms.PrintPreviewControl.Document%2A> property refers to instances of both the <xref:System.Drawing.Printing.PrinterSettings> and <xref:System.Drawing.Printing.PageSettings> classes, and these are used to render the document in the preview window.</span></span>  
  
### <a name="to-view-pages-using-the-printpreviewdialog-control"></a><span data-ttu-id="ba000-110">So zeigen Sie Seiten mit dem PrintPreviewDialog-Steuerelement an</span><span class="sxs-lookup"><span data-stu-id="ba000-110">To view pages using the PrintPreviewDialog control</span></span>  
  
- <span data-ttu-id="ba000-111">Verwenden Sie die <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> -Methode, um das Dialogfeld anzuzeigen, und geben Sie das zu verwendende <xref:System.Drawing.Printing.PrintDocument> an.</span><span class="sxs-lookup"><span data-stu-id="ba000-111">Use the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method to display the dialog box, specifying the <xref:System.Drawing.Printing.PrintDocument> to use.</span></span>  
  
     <span data-ttu-id="ba000-112">Im folgenden Codebeispiel <xref:System.Windows.Forms.Button> öffnet der-Ereignishandler des-Steuer Elements <xref:System.Windows.Forms.Control.Click> eine Instanz des- <xref:System.Windows.Forms.PrintPreviewDialog> Steuer Elements.</span><span class="sxs-lookup"><span data-stu-id="ba000-112">In the following code example, the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Click> event handler opens an instance of the <xref:System.Windows.Forms.PrintPreviewDialog> control.</span></span> <span data-ttu-id="ba000-113">Das Druck Dokument wird in der- <xref:System.Windows.Forms.PrintDialog.Document%2A> Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="ba000-113">The print document is specified in the <xref:System.Windows.Forms.PrintDialog.Document%2A> property.</span></span> <span data-ttu-id="ba000-114">Im folgenden Beispiel wird kein Druck Dokument angegeben.</span><span class="sxs-lookup"><span data-stu-id="ba000-114">In the example below, no print document is specified.</span></span>  
  
     <span data-ttu-id="ba000-115">Für das Beispiel muss das Formular über ein <xref:System.Windows.Forms.Button> -Steuerelement, eine <xref:System.Drawing.Printing.PrintDocument> -Komponente mit dem Namen `myDocument` und ein-Steuerelement verfügen <xref:System.Windows.Forms.PrintPreviewDialog> .</span><span class="sxs-lookup"><span data-stu-id="ba000-115">The example requires that your form has a <xref:System.Windows.Forms.Button> control, a <xref:System.Drawing.Printing.PrintDocument> component named `myDocument`, and a <xref:System.Windows.Forms.PrintPreviewDialog> control.</span></span>  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, _  
       ByVal e As System.EventArgs) Handles Button1.Click  
       ' The print document 'myDocument' used below  
       ' is merely for an example.  
       ' You will have to specify your own print document.  
       PrintPreviewDialog1.Document = myDocument  
       PrintPreviewDialog1.ShowDialog()  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)  
    {  
       // The print document 'myDocument' used below  
       // is merely for an example.  
       // You will have to specify your own print document.  
       printPreviewDialog1.Document = myDocument;  
       printPreviewDialog1.ShowDialog();  
    }  
    ```  
  
    ```cpp  
    private:  
       void button1_Click(System::Object ^ sender,  
          System::EventArgs ^ e)  
       {  
          // The print document 'myDocument' used below  
          // is merely for an example.  
          // You will have to specify your own print document.  
          printPreviewDialog1->Document = myDocument;  
          printPreviewDialog1->ShowDialog();  
       }  
    ```  
  
     <span data-ttu-id="ba000-116">(Visual c#, Visual C++) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="ba000-116">(Visual C#, Visual C++) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
    ```cpp  
    this->button1->Click += gcnew  
       System::EventHandler(this, &Form1::button1_Click);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="ba000-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba000-117">See also</span></span>

- [<span data-ttu-id="ba000-118">PrintDocument-Komponente</span><span class="sxs-lookup"><span data-stu-id="ba000-118">PrintDocument Component</span></span>](printdocument-component-windows-forms.md)
- [<span data-ttu-id="ba000-119">PrintPreviewDialog-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="ba000-119">PrintPreviewDialog Control</span></span>](printpreviewdialog-control-windows-forms.md)
- [<span data-ttu-id="ba000-120">Druckunterstützung in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ba000-120">Windows Forms Print Support</span></span>](../advanced/windows-forms-print-support.md)
- [<span data-ttu-id="ba000-121">Windows Forms</span><span class="sxs-lookup"><span data-stu-id="ba000-121">Windows Forms</span></span>](../index.yml)
