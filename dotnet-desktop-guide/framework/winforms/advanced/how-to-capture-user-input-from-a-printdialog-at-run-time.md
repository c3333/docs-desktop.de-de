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
# <a name="how-to-capture-user-input-from-a-printdialog-at-run-time"></a>Vorgehensweise: Erfassen von Benutzereingaben in einem „PrintDialog“ zur Laufzeit
Obwohl Sie Optionen zum Drucken zur Entwurfszeit festlegen können, sollten Sie diese Optionen in einigen Fällen zur Laufzeit ändern. Dies liegt wahrscheinlich daran, dass die vom Benutzer getroffenen Entscheidungen getroffen werden. Sie können Benutzereingaben für das Drucken eines Dokuments erfassen, indem Sie die <xref:System.Windows.Forms.PrintDialog> -Komponente und die- <xref:System.Drawing.Printing.PrintDocument> Komponente verwenden.  
  
### <a name="to-change-print-options-programmatically"></a>So ändern Sie Druckoptionen Programm gesteuert  
  
1. Fügen Sie dem <xref:System.Windows.Forms.PrintDialog> Formular eine-Komponente und eine- <xref:System.Drawing.Printing.PrintDocument> Komponente hinzu.  
  
2. Legen Sie die- <xref:System.Windows.Forms.PrintDialog.Document%2A> Eigenschaft von <xref:System.Windows.Forms.PrintDialog> auf die dem <xref:System.Drawing.Printing.PrintDocument> Formular hinzugefügte fest.  
  
    ```vb  
    PrintDialog1.Document = PrintDocument1  
    ```  
  
    ```csharp  
    printDialog1.Document = PrintDocument1;  
    ```  
  
    ```cpp  
    printDialog1->Document = PrintDocument1;  
    ```  
  
3. Zeigen <xref:System.Windows.Forms.PrintDialog> Sie die Komponente mithilfe der- <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode an.  
  
    ```vb  
    PrintDialog1.ShowDialog()  
    ```  
  
    ```csharp  
    printDialog1.ShowDialog();  
    ```  
  
    ```cpp  
    printDialog1->ShowDialog();  
    ```  
  
4. Die Druck Auswahl des Benutzers aus dem Dialogfeld wird in die- <xref:System.Drawing.Printing.PrinterSettings> Eigenschaft der <xref:System.Drawing.Printing.PrintDocument> Komponente kopiert.  
  
## <a name="see-also"></a>Siehe auch

- [How to: Drucken einer mehrseitigen Textdatei in Windows Forms](how-to-print-a-multi-page-text-file-in-windows-forms.md)
- [Druckunterstützung in Windows Forms](windows-forms-print-support.md)
