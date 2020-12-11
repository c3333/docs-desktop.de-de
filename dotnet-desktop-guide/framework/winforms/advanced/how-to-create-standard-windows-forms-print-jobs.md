---
title: Standard Druckaufträge erstellen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- printing [Windows Forms]
- printing [Windows Forms], creating print jobs
- printing [Visual Basic], in Windows applications
ms.assetid: 03342b90-9cfe-40b2-838b-b479a13c5dea
ms.openlocfilehash: d9607de7c74132e0d7dce605b16d62c79b7dbccb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975265"
---
# <a name="how-to-create-standard-windows-forms-print-jobs"></a><span data-ttu-id="bd536-102">Vorgehensweise: Erstellen von standardmäßigen Druckaufträgen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="bd536-102">How to: Create Standard Windows Forms Print Jobs</span></span>
<span data-ttu-id="bd536-103">Die Grundlage für das Drucken in Windows Forms ist die <xref:System.Drawing.Printing.PrintDocument> Komponente – genauer gesagt das <xref:System.Drawing.Printing.PrintDocument.PrintPage> Ereignis.</span><span class="sxs-lookup"><span data-stu-id="bd536-103">The foundation of printing in Windows Forms is the <xref:System.Drawing.Printing.PrintDocument> component—more specifically, the <xref:System.Drawing.Printing.PrintDocument.PrintPage> event.</span></span> <span data-ttu-id="bd536-104">Wenn Sie Code schreiben, um das Ereignis zu behandeln <xref:System.Drawing.Printing.PrintDocument.PrintPage> , können Sie angeben, was gedruckt und gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd536-104">By writing code to handle the <xref:System.Drawing.Printing.PrintDocument.PrintPage> event, you can specify what to print and how to print it.</span></span>  
  
### <a name="to-create-a-print-job"></a><span data-ttu-id="bd536-105">So erstellen Sie einen Druckauftrag</span><span class="sxs-lookup"><span data-stu-id="bd536-105">To create a print job</span></span>  
  
1. <span data-ttu-id="bd536-106">Fügen Sie dem <xref:System.Drawing.Printing.PrintDocument> Formular eine Komponente hinzu.</span><span class="sxs-lookup"><span data-stu-id="bd536-106">Add a <xref:System.Drawing.Printing.PrintDocument> component to your form.</span></span>  
  
2. <span data-ttu-id="bd536-107">Erstellen Sie Code zur Behandlung des <xref:System.Drawing.Printing.PrintDocument.PrintPage> -Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="bd536-107">Write code to handle the <xref:System.Drawing.Printing.PrintDocument.PrintPage> event.</span></span>  
  
     <span data-ttu-id="bd536-108">Sie müssen ihre eigene Druck Logik programmieren.</span><span class="sxs-lookup"><span data-stu-id="bd536-108">You will have to code your own printing logic.</span></span> <span data-ttu-id="bd536-109">Außerdem müssen Sie das Material angeben, das gedruckt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd536-109">Additionally, you will have to specify the material to be printed.</span></span>  
  
     <span data-ttu-id="bd536-110">Im folgenden Codebeispiel wird eine Beispiel Grafik in der Form eines roten Rechtecks im-Ereignishandler erstellt, der <xref:System.Drawing.Printing.PrintDocument.PrintPage> als Material zum Drucken fungiert.</span><span class="sxs-lookup"><span data-stu-id="bd536-110">In the following code example, a sample graphic in the shape of a red rectangle is created in the <xref:System.Drawing.Printing.PrintDocument.PrintPage> event handler to act as material to be printed.</span></span>  
  
    ```vb  
    Private Sub PrintDocument1_PrintPage(ByVal sender As Object, ByVal e As System.Drawing.Printing.PrintPageEventArgs) Handles PrintDocument1.PrintPage  
       e.Graphics.FillRectangle(Brushes.Red, New Rectangle(500, 500, 500, 500))  
    End Sub  
    ```  
  
    ```csharp  
    private void printDocument1_PrintPage(object sender,
    System.Drawing.Printing.PrintPageEventArgs e)  
    {  
       e.Graphics.FillRectangle(Brushes.Red,
         new Rectangle(500, 500, 500, 500));  
    }  
    ```  
  
    ```cpp  
    private:  
       void printDocument1_PrintPage(System::Object ^ sender,  
          System::Drawing::Printing::PrintPageEventArgs ^ e)  
       {  
          e->Graphics->FillRectangle(Brushes::Red,  
             Rectangle(500, 500, 500, 500));  
       }  
    ```  
  
     <span data-ttu-id="bd536-111">(Visual c# und Visual C++) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="bd536-111">(Visual C# and Visual C++) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.printDocument1.PrintPage += new  
       System.Drawing.Printing.PrintPageEventHandler  
       (this.printDocument1_PrintPage);  
    ```  
  
    ```cpp  
    printDocument1->PrintPage += gcnew  
       System::Drawing::Printing::PrintPageEventHandler  
       (this, &Form1::printDocument1_PrintPage);  
    ```  
  
     <span data-ttu-id="bd536-112">Möglicherweise möchten Sie auch Code für das <xref:System.Drawing.Printing.PrintDocument.BeginPrint> -Ereignis und das-Ereignis schreiben, z. b. <xref:System.Drawing.Printing.PrintDocument.EndPrint> eine ganze Zahl, die die Gesamtzahl der zu druckenden Seiten darstellt, die bei jeder Seite gedruckt wird.</span><span class="sxs-lookup"><span data-stu-id="bd536-112">You may also want to write code for the <xref:System.Drawing.Printing.PrintDocument.BeginPrint> and <xref:System.Drawing.Printing.PrintDocument.EndPrint> events, perhaps including an integer representing the total number of pages to print that is decremented as each page prints.</span></span>  
  
    > [!NOTE]
    > <span data-ttu-id="bd536-113">Sie können dem Formular eine Komponente hinzufügen <xref:System.Windows.Forms.PrintDialog> , um Benutzern eine saubere und effiziente Benutzeroberfläche zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="bd536-113">You can add a <xref:System.Windows.Forms.PrintDialog> component to your form to provide a clean and efficient user interface (UI) to your users.</span></span> <span data-ttu-id="bd536-114">Durch Festlegen der- <xref:System.Windows.Forms.PrintDialog.Document%2A> Eigenschaft der- <xref:System.Windows.Forms.PrintDialog> Komponente können Sie Eigenschaften festlegen, die sich auf das Druck Dokument beziehen, mit dem Sie in Ihrem Formular arbeiten.</span><span class="sxs-lookup"><span data-stu-id="bd536-114">Setting the <xref:System.Windows.Forms.PrintDialog.Document%2A> property of the <xref:System.Windows.Forms.PrintDialog> component enables you to set properties related to the print document you are working with on your form.</span></span> <span data-ttu-id="bd536-115">Weitere Informationen zur- <xref:System.Windows.Forms.PrintDialog> Komponente finden Sie unter [PrintDialog-Komponente](../controls/printdialog-component-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="bd536-115">For more information about the <xref:System.Windows.Forms.PrintDialog> component, see [PrintDialog Component](../controls/printdialog-component-windows-forms.md).</span></span>  
  
     <span data-ttu-id="bd536-116">Weitere Informationen zu den Besonderheiten Windows Forms Druckaufträgen, einschließlich der programmgesteuerten Erstellung eines Druckauftrags, finden Sie unter <xref:System.Drawing.Printing.PrintPageEventArgs> .</span><span class="sxs-lookup"><span data-stu-id="bd536-116">For more information about the specifics of Windows Forms print jobs, including how to create a print job programmatically, see <xref:System.Drawing.Printing.PrintPageEventArgs>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="bd536-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd536-117">See also</span></span>

- <xref:System.Drawing.Printing.PrintDocument>
- [<span data-ttu-id="bd536-118">Druckunterstützung in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="bd536-118">Windows Forms Print Support</span></span>](windows-forms-print-support.md)
