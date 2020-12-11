---
title: 'Gewusst wie: Drucken von Grafiken'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- graphics [Windows Forms], printing
- printing [Windows Forms], graphics
ms.assetid: 32b891e6-52ff-4fea-a9ff-2ce5db20a4c6
ms.openlocfilehash: 15f3a507839430ce058302e7f5abd317ef84626f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976141"
---
# <a name="how-to-print-graphics-in-windows-forms"></a>Vorgehensweise: Drucken von Grafiken in Windows Forms
Häufig möchten Sie Grafiken in Ihrer Windows-basierten Anwendung drucken. Die- <xref:System.Drawing.Graphics> Klasse stellt Methoden zum Zeichnen von Objekten für ein Gerät bereit, z. b. einen Bildschirm oder Drucker.  
  
### <a name="to-print-graphics"></a>So drucken Sie Grafiken  
  
1. Fügen Sie dem <xref:System.Drawing.Printing.PrintDocument> Formular eine Komponente hinzu.  
  
2. <xref:System.Drawing.Printing.PrintDocument.PrintPage>Verwenden Sie im-Ereignishandler die- <xref:System.Drawing.Printing.PrintPageEventArgs.Graphics%2A> Eigenschaft der-Klasse, <xref:System.Drawing.Printing.PrintPageEventArgs> um den Drucker anzuweisen, welche Art von Grafiken gedruckt werden soll.  
  
     Das folgende Codebeispiel zeigt einen Ereignishandler, mit dem eine blaue Ellipse in einem umschließenden Rechteck erstellt wird. Das Rechteck verfügt über die folgenden Speicherorte und Dimensionen: beginnend bei 100, 150 mit einer Breite von 250 und einer Höhe von 250.  
  
    ```vb  
    Private Sub PrintDocument1_PrintPage(ByVal sender As Object, ByVal e As System.Drawing.Printing.PrintPageEventArgs) Handles PrintDocument1.PrintPage  
       e.Graphics.FillEllipse(Brushes.Blue, New Rectangle(100, 150, 250, 250))  
    End Sub  
    ```  
  
    ```csharp  
    private void printDocument1_PrintPage(object sender,
    System.Drawing.Printing.PrintPageEventArgs e)  
    {  
       e.Graphics.FillRectangle(Brushes.Blue,
         new Rectangle(100, 150, 250, 250));  
    }  
    ```  
  
    ```cpp  
    private:  
       void printDocument1_PrintPage(System::Object ^ sender,  
          System::Drawing::Printing::PrintPageEventArgs ^ e)  
       {  
          e->Graphics->FillRectangle(Brushes::Blue,  
             Rectangle(100, 150, 250, 250));  
       }  
    ```  
  
     (Visual c# und Visual C++) Fügen Sie den folgenden Code in den Konstruktor des Formulars ein, um den Ereignishandler zu registrieren.  
  
    ```csharp  
    this.printDocument1.PrintPage += new  
       System.Drawing.Printing.PrintPageEventHandler  
       (this.printDocument1_PrintPage);  
    ```  
  
    ```cpp  
    this->printDocument1->PrintPage += gcnew  
       System::Drawing::Printing::PrintPageEventHandler  
       (this, &Form1::printDocument1_PrintPage);  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Graphics>
- <xref:System.Drawing.Brush>
- [Druckunterstützung in Windows Forms](windows-forms-print-support.md)
