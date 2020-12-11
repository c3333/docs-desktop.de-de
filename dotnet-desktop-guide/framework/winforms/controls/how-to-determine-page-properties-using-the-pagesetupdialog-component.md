---
title: 'Vorgehensweise: Bestimmen von Seiteneigenschaften mit der PageSetupDialog-Komponente'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- page properties
- page setup
- PageSetupDialog component
ms.assetid: 6dae05bc-c0fd-4357-bb93-841a1631d98f
ms.openlocfilehash: 8a015c199193dfd9c43bec53cc93cbf9dc201413
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975666"
---
# <a name="how-to-determine-page-properties-using-the-pagesetupdialog-component"></a><span data-ttu-id="5f707-102">Vorgehensweise: Bestimmen von Seiteneigenschaften mit der PageSetupDialog-Komponente</span><span class="sxs-lookup"><span data-stu-id="5f707-102">How to: Determine Page Properties Using the PageSetupDialog Component</span></span>
<span data-ttu-id="5f707-103">Mithilfe der [PageSetupDialog](pagesetupdialog-component-windows-forms.md) -Komponente können Benutzer das Layout, die Papiergröße und weitere Optionen für das Seitenlayout festlegen.</span><span class="sxs-lookup"><span data-stu-id="5f707-103">The [PageSetupDialog](pagesetupdialog-component-windows-forms.md) component presents layout, paper size, and other page layout choices to the user for a document.</span></span>  
  
 <span data-ttu-id="5f707-104">Sie müssen dazu eine Instanz der <xref:System.Drawing.Printing.PrintDocument> -Klasse angeben. Dabei handelt es sich um das Dokument, das gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="5f707-104">You need to specify an instance of the <xref:System.Drawing.Printing.PrintDocument> class—this is the document to be printed.</span></span> <span data-ttu-id="5f707-105">Darüber hinaus benötigen Benutzer einen lokal oder über ein Netzwerk auf dem Computer installierten Drucker, da die <xref:System.Windows.Forms.PageSetupDialog> -Komponente darauf aufbauend die Formatierungsoptionen bestimmt, die dem Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5f707-105">Additionally, users must have a printer installed on their computer, either locally or through a network, as this is partly how the <xref:System.Windows.Forms.PageSetupDialog> component determines the page formatting choices presented to the user.</span></span>  
  
 <span data-ttu-id="5f707-106">Ein wichtiger Aspekt an der Arbeit mit der <xref:System.Windows.Forms.PageSetupDialog> -Komponente ist ihre Interaktionsweise mit der <xref:System.Drawing.Printing.PageSettings> -Klasse.</span><span class="sxs-lookup"><span data-stu-id="5f707-106">An important aspect of working with the <xref:System.Windows.Forms.PageSetupDialog> component is how it interacts with the <xref:System.Drawing.Printing.PageSettings> class.</span></span> <span data-ttu-id="5f707-107">Die <xref:System.Drawing.Printing.PageSettings> -Klasse wird verwendet, um die Einstellungen anzugeben, die die Druckweise einer Seite beeinflussen, z.B. die Ausrichtung, die Seitengröße und die Ränder.</span><span class="sxs-lookup"><span data-stu-id="5f707-107">The <xref:System.Drawing.Printing.PageSettings> class is used to specify settings that modify the way a page will be printed, such as paper orientation, the size of the page, and the margins.</span></span> <span data-ttu-id="5f707-108">Jede dieser Einstellungen wird als Eigenschaft der <xref:System.Drawing.Printing.PageSettings> -Klasse dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5f707-108">Each of these settings is represented as a property of the <xref:System.Drawing.Printing.PageSettings> class.</span></span> <span data-ttu-id="5f707-109">Die <xref:System.Windows.Forms.PageSetupDialog> -Klasse ändert diese Eigenschaftswerte für eine bestimmte Instanz der <xref:System.Drawing.Printing.PageSettings> -Klasse, die mit dem Dokument verknüpft ist (als eine <xref:System.Drawing.Printing.PrintDocument.DefaultPageSettings%2A> -Eigenschaft dargestellt).</span><span class="sxs-lookup"><span data-stu-id="5f707-109">The <xref:System.Windows.Forms.PageSetupDialog> class modifies these property values for a given instance of the <xref:System.Drawing.Printing.PageSettings> class that is associated with the document (and is represented as a <xref:System.Drawing.Printing.PrintDocument.DefaultPageSettings%2A> property).</span></span>  
  
### <a name="to-set-page-properties-using-the-pagesetupdialog-component"></a><span data-ttu-id="5f707-110">So bestimmen Sie die Seiteneigenschaften mit der PageSetupDialog-Komponente</span><span class="sxs-lookup"><span data-stu-id="5f707-110">To set page properties using the PageSetupDialog component</span></span>  
  
1. <span data-ttu-id="5f707-111">Verwenden Sie die <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> -Methode, um das Dialogfeld anzuzeigen, und geben Sie das zu verwendende <xref:System.Drawing.Printing.PrintDocument> an.</span><span class="sxs-lookup"><span data-stu-id="5f707-111">Use the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method to display the dialog box, specifying the <xref:System.Drawing.Printing.PrintDocument> to use.</span></span>  
  
     <span data-ttu-id="5f707-112">Im folgenden Beispiel öffnet der <xref:System.Windows.Forms.Button> -Ereignishandler des <xref:System.Windows.Forms.Control.Click> -Steuerelements eine Instanz der <xref:System.Windows.Forms.PageSetupDialog> -Komponente.</span><span class="sxs-lookup"><span data-stu-id="5f707-112">In the example below, the <xref:System.Windows.Forms.Button> control's <xref:System.Windows.Forms.Control.Click> event handler opens an instance of the <xref:System.Windows.Forms.PageSetupDialog> component.</span></span> <span data-ttu-id="5f707-113">Ein vorhandenes Dokument wird in der <xref:System.Windows.Forms.PageSetupDialog.Document%2A> -Eigenschaft angegeben, und seine <xref:System.Drawing.Printing.PageSettings.Color%2A?displayProperty=nameWithType> -Eigenschaft wird auf `false`festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5f707-113">An existing document is specified in the <xref:System.Windows.Forms.PageSetupDialog.Document%2A> property, and its <xref:System.Drawing.Printing.PageSettings.Color%2A?displayProperty=nameWithType> property is set to `false`.</span></span>  
  
     <span data-ttu-id="5f707-114">Im Beispiel wird davon ausgegangen, dass das Formular über ein <xref:System.Windows.Forms.Button> -Steuerelement, eine <xref:System.Drawing.Printing.PrintDocument> `myDocument` -Komponente und eine- <xref:System.Windows.Forms.PageSetupDialog> Komponente verfügt.</span><span class="sxs-lookup"><span data-stu-id="5f707-114">The example assumes your form has a <xref:System.Windows.Forms.Button> control, a <xref:System.Drawing.Printing.PrintDocument> component named `myDocument`, and a <xref:System.Windows.Forms.PageSetupDialog> component.</span></span>  
  
    ```vb  
    Private Sub Button1_Click(ByVal sender As System.Object, _  
    ByVal e As System.EventArgs) Handles Button1.Click  
       ' The print document 'myDocument' used below  
       ' is merely for an example.  
       'You will have to specify your own print document.  
       PageSetupDialog1.Document = myDocument  
       ' Sets the print document's color setting to false,  
       ' so that the page will not be printed in color.  
       PageSetupDialog1.Document.DefaultPageSettings.Color = False  
       PageSetupDialog1.ShowDialog()  
    End Sub  
    ```  
  
    ```csharp  
    private void button1_Click(object sender, System.EventArgs e)  
    {  
       // The print document 'myDocument' used below  
       // is merely for an example.  
       // You will have to specify your own print document.  
       pageSetupDialog1.Document = myDocument;  
       // Sets the print document's color setting to false,  
       // so that the page will not be printed in color.  
       pageSetupDialog1.Document.DefaultPageSettings.Color = false;  
       pageSetupDialog1.ShowDialog();  
    }  
    ```  
  
    ```cpp  
    private:  
       System::Void button1_Click(System::Object ^  sender,  
          System::EventArgs ^  e)  
       {  
          // The print document 'myDocument' used below  
          // is merely for an example.  
          // You will have to specify your own print document.  
          pageSetupDialog1->Document = myDocument;  
          // Sets the print document's color setting to false,  
          // so that the page will not be printed in color.  
          pageSetupDialog1->Document->DefaultPageSettings->Color = false;  
          pageSetupDialog1->ShowDialog();  
       }  
    ```  
  
     <span data-ttu-id="5f707-115">(Visual c# und Visual C++) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="5f707-115">(Visual C# and Visual C++) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.button1.Click += new System.EventHandler(this.button1_Click);  
    ```  
  
    ```cpp  
    this->button1->Click += gcnew
       System::EventHandler(this, &Form1::button1_Click);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="5f707-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5f707-116">See also</span></span>

- <xref:System.Windows.Forms.PageSetupDialog>
- [<span data-ttu-id="5f707-117">Vorgehensweise: Erstellen von standardmäßigen Druckaufträgen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5f707-117">How to: Create Standard Windows Forms Print Jobs</span></span>](../advanced/how-to-create-standard-windows-forms-print-jobs.md)
- [<span data-ttu-id="5f707-118">PageSetupDialog-Komponente</span><span class="sxs-lookup"><span data-stu-id="5f707-118">PageSetupDialog Component</span></span>](pagesetupdialog-component-windows-forms.md)
