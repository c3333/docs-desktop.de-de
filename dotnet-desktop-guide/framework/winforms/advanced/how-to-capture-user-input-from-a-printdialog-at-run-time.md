---
title: 'Vorgehensweise: Erfassen von Benutzereingaben in einem „PrintDialog“ zur Laufzeit'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- print options [Windows Forms], changing at run time
- printing [Windows Forms], options
- print options
- run time [Windows Forms], changing print options
ms.assetid: 438501d8-9a70-4fb3-aae6-e46579aba0c6
ms.openlocfilehash: 2aaf988f362baf9cd80eb16e4a08f7f65a5077bb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975370"
---
# <a name="how-to-capture-user-input-from-a-printdialog-at-run-time"></a><span data-ttu-id="c28a3-102">Vorgehensweise: Erfassen von Benutzereingaben in einem „PrintDialog“ zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="c28a3-102">How to: Capture User Input from a PrintDialog at Run Time</span></span>
<span data-ttu-id="c28a3-103">Obwohl Sie Optionen zum Drucken zur Entwurfszeit festlegen können, sollten Sie diese Optionen in einigen Fällen zur Laufzeit ändern. Dies liegt wahrscheinlich daran, dass die vom Benutzer getroffenen Entscheidungen getroffen werden.</span><span class="sxs-lookup"><span data-stu-id="c28a3-103">While you can set options related to printing at design time, you will sometimes want to change these options at run time, most likely because of choices made by the user.</span></span> <span data-ttu-id="c28a3-104">Sie können Benutzereingaben für das Drucken eines Dokuments erfassen, indem Sie die <xref:System.Windows.Forms.PrintDialog> -Komponente und die- <xref:System.Drawing.Printing.PrintDocument> Komponente verwenden.</span><span class="sxs-lookup"><span data-stu-id="c28a3-104">You can capture user input for printing a document using the <xref:System.Windows.Forms.PrintDialog> and the <xref:System.Drawing.Printing.PrintDocument> components.</span></span>  
  
### <a name="to-change-print-options-programmatically"></a><span data-ttu-id="c28a3-105">So ändern Sie Druckoptionen Programm gesteuert</span><span class="sxs-lookup"><span data-stu-id="c28a3-105">To change print options programmatically</span></span>  
  
1. <span data-ttu-id="c28a3-106">Fügen Sie dem <xref:System.Windows.Forms.PrintDialog> Formular eine-Komponente und eine- <xref:System.Drawing.Printing.PrintDocument> Komponente hinzu.</span><span class="sxs-lookup"><span data-stu-id="c28a3-106">Add a <xref:System.Windows.Forms.PrintDialog> and a <xref:System.Drawing.Printing.PrintDocument> component to your form.</span></span>  
  
2. <span data-ttu-id="c28a3-107">Legen Sie die- <xref:System.Windows.Forms.PrintDialog.Document%2A> Eigenschaft von <xref:System.Windows.Forms.PrintDialog> auf die dem <xref:System.Drawing.Printing.PrintDocument> Formular hinzugefügte fest.</span><span class="sxs-lookup"><span data-stu-id="c28a3-107">Set the <xref:System.Windows.Forms.PrintDialog.Document%2A> property of the <xref:System.Windows.Forms.PrintDialog> to the <xref:System.Drawing.Printing.PrintDocument> added to the form.</span></span>  
  
    ```vb  
    PrintDialog1.Document = PrintDocument1  
    ```  
  
    ```csharp  
    printDialog1.Document = PrintDocument1;  
    ```  
  
    ```cpp  
    printDialog1->Document = PrintDocument1;  
    ```  
  
3. <span data-ttu-id="c28a3-108">Zeigen <xref:System.Windows.Forms.PrintDialog> Sie die Komponente mithilfe der- <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode an.</span><span class="sxs-lookup"><span data-stu-id="c28a3-108">Display the <xref:System.Windows.Forms.PrintDialog> component by using the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method.</span></span>  
  
    ```vb  
    PrintDialog1.ShowDialog()  
    ```  
  
    ```csharp  
    printDialog1.ShowDialog();  
    ```  
  
    ```cpp  
    printDialog1->ShowDialog();  
    ```  
  
4. <span data-ttu-id="c28a3-109">Die Druck Auswahl des Benutzers aus dem Dialogfeld wird in die- <xref:System.Drawing.Printing.PrinterSettings> Eigenschaft der <xref:System.Drawing.Printing.PrintDocument> Komponente kopiert.</span><span class="sxs-lookup"><span data-stu-id="c28a3-109">The user's printing choices from the dialog will be copied to the <xref:System.Drawing.Printing.PrinterSettings> property of the <xref:System.Drawing.Printing.PrintDocument> component.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c28a3-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c28a3-110">See also</span></span>

- [<span data-ttu-id="c28a3-111">How to: Drucken einer mehrseitigen Textdatei in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c28a3-111">How to: Print a Multi-Page Text File in Windows Forms</span></span>](how-to-print-a-multi-page-text-file-in-windows-forms.md)
- [<span data-ttu-id="c28a3-112">Druckunterstützung in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c28a3-112">Windows Forms Print Support</span></span>](windows-forms-print-support.md)
