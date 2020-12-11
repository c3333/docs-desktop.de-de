---
title: Vollständige Druckaufträge
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- print jobs [Windows Forms], completing in Windows Forms
- printing [Windows Forms], print jobs
ms.assetid: 23ec74f7-34c5-4710-82a0-ee2914518548
ms.openlocfilehash: 62f67002bfbaf46e73bae06fdaff26efde865c06
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975012"
---
# <a name="how-to-complete-windows-forms-print-jobs"></a><span data-ttu-id="d6608-102">Vorgehensweise: Fertigstellen von Druckaufträgen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d6608-102">How to: Complete Windows Forms Print Jobs</span></span>
<span data-ttu-id="d6608-103">Häufig bieten Word-Prozessoren und andere Anwendungen, die das Drucken einschließen, die Möglichkeit, Benutzern eine Meldung anzuzeigen, dass ein Druckauftrag vollständig ist.</span><span class="sxs-lookup"><span data-stu-id="d6608-103">Frequently, word processors and other applications that involve printing will provide the option to display a message to users that a print job is complete.</span></span> <span data-ttu-id="d6608-104">Sie können diese Funktionalität in Ihrem Windows Forms bereitstellen, indem Sie das- <xref:System.Drawing.Printing.PrintDocument.EndPrint> Ereignis der- <xref:System.Drawing.Printing.PrintDocument> Komponente behandeln.</span><span class="sxs-lookup"><span data-stu-id="d6608-104">You can provide this functionality in your Windows Forms by handling the <xref:System.Drawing.Printing.PrintDocument.EndPrint> event of the <xref:System.Drawing.Printing.PrintDocument> component.</span></span>  
  
 <span data-ttu-id="d6608-105">Das folgende Verfahren erfordert, dass Sie eine Windows-basierte Anwendung mit einer- <xref:System.Drawing.Printing.PrintDocument> Komponente erstellt haben. Dies ist die Standardmethode zum Aktivieren von Drucken aus einer Windows-basierten Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d6608-105">The following procedure requires that you have created a Windows-based application with a <xref:System.Drawing.Printing.PrintDocument> component on it, which is the standard way of enabling printing from a Windows-based application.</span></span> <span data-ttu-id="d6608-106">Weitere Informationen zum Drucken aus Windows Forms mithilfe der- <xref:System.Drawing.Printing.PrintDocument> Komponente finden Sie unter [How to: Create Standard Windows Forms Print Jobs](how-to-create-standard-windows-forms-print-jobs.md).</span><span class="sxs-lookup"><span data-stu-id="d6608-106">For more information about printing from Windows Forms using the <xref:System.Drawing.Printing.PrintDocument> component, see [How to: Create Standard Windows Forms Print Jobs](how-to-create-standard-windows-forms-print-jobs.md).</span></span>  
  
### <a name="to-complete-a-print-job"></a><span data-ttu-id="d6608-107">So vervollständigen Sie einen Druckauftrag</span><span class="sxs-lookup"><span data-stu-id="d6608-107">To complete a print job</span></span>  
  
1. <span data-ttu-id="d6608-108">Legen Sie die- <xref:System.Drawing.Printing.PrintDocument.DocumentName%2A> Eigenschaft der <xref:System.Drawing.Printing.PrintDocument> Komponente fest.</span><span class="sxs-lookup"><span data-stu-id="d6608-108">Set the <xref:System.Drawing.Printing.PrintDocument.DocumentName%2A> property of the <xref:System.Drawing.Printing.PrintDocument> component.</span></span>  
  
    ```vb  
    PrintDocument1.DocumentName = "MyTextFile"  
    ```  
  
    ```csharp  
    printDocument1.DocumentName = "MyTextFile";  
    ```  
  
    ```cpp  
    printDocument1->DocumentName = "MyTextFile";  
    ```  
  
2. <span data-ttu-id="d6608-109">Erstellen Sie Code zur Behandlung des <xref:System.Drawing.Printing.PrintDocument.EndPrint> -Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="d6608-109">Write code to handle the <xref:System.Drawing.Printing.PrintDocument.EndPrint> event.</span></span>  
  
     <span data-ttu-id="d6608-110">Im folgenden Codebeispiel wird ein Meldungs Feld angezeigt, das angibt, dass das Dokument den Druckvorgang abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="d6608-110">In the following code example, a message box is displayed, indicating that the document has finished printing.</span></span>  
  
    ```vb  
    Private Sub PrintDocument1_EndPrint(ByVal sender As Object, ByVal e As System.Drawing.Printing.PrintEventArgs) Handles PrintDocument1.EndPrint  
       MessageBox.Show(PrintDocument1.DocumentName + " has finished printing.")  
    End Sub  
    ```  
  
    ```csharp  
    private void printDocument1_EndPrint(object sender,
    System.Drawing.Printing.PrintEventArgs e)  
    {  
       MessageBox.Show(printDocument1.DocumentName +
          " has finished printing.");  
    }  
    ```  
  
    ```cpp  
    private:  
       void printDocument1_EndPrint(System::Object ^ sender,  
          System::Drawing::Printing::PrintEventArgs ^ e)  
       {  
          MessageBox::Show(String::Concat(printDocument1->DocumentName,  
             " has finished printing."));  
       }  
    ```  
  
     <span data-ttu-id="d6608-111">(Visual c# und Visual C++) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="d6608-111">(Visual C# and Visual C++) Place the following code in the form's constructor to register the event handler.</span></span>  
  
    ```csharp  
    this.printDocument1.EndPrint += new  
       System.Drawing.Printing.PrintEventHandler  
       (this.printDocument1_EndPrint);  
    ```  
  
    ```cpp  
    this->printDocument1->EndPrint += gcnew  
       System::Drawing::Printing::PrintEventHandler  
       (this, &Form1::printDocument1_EndPrint);  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="d6608-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6608-112">See also</span></span>

- <xref:System.Drawing.Printing.PrintDocument>
- [<span data-ttu-id="d6608-113">Druckunterstützung in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d6608-113">Windows Forms Print Support</span></span>](windows-forms-print-support.md)
