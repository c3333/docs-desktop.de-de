---
title: Anzeigen der Print Dialog-Komponente
ms.date: 03/30/2017
helpviewer_keywords:
- Print dialog box [Windows Forms], displaying
- PrintDialog component [Windows Forms], displaying
- printing [Windows Forms], displaying print dialog box
ms.assetid: 745a8db7-0526-4b21-b09d-18e13ed32014
ms.openlocfilehash: de0acc655bbcf0cfc017d594545fae56cc27f981
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975654"
---
# <a name="how-to-display-the-printdialog-component"></a>Anzeigen der Print Dialog-Komponente

<xref:System.Windows.Forms.PrintDialog>Bei der Komponente handelt es sich um das Standard Dialogfeld für den Windows-Druck, das viele Ihrer Benutzer kennen. Da Ihre Benutzer sofort damit vertraut sind, ist es vorteilhaft, die Komponente zu verwenden <xref:System.Windows.Forms.PrintDialog> .

## <a name="to-display-the-printdialog-component"></a>So zeigen Sie die PrintDialog-Komponente an

- Ruft die- <xref:System.Windows.Forms.Form.ShowDialog%2A> Methode aus dem Code der Anwendung heraus auf.

     Sobald die Komponente angezeigt wird, können die Benutzer damit interagieren und die Eigenschaften für den Druckauftrag einstellen. Diese werden in der  <xref:System.Drawing.Printing.PrinterSettings> -Klasse (und der- <xref:System.Drawing.Printing.PageSettings> Klasse) gespeichert, wenn der Benutzer über die-Komponente auf die [PageSetupDialog-Komponente](pagesetupdialog-component-windows-forms.md) zugreift, die <xref:System.Windows.Forms.PrintDialog> diesem Druckauftrag zugeordnet ist. Dann können Sie Aufrufe an die von ihnen eingestellten Eigenschaften durchführen, um die spezifischen Merkmale des Druckauftrags anzugeben.

## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Erstellen von standardmäßigen Druckaufträgen in Windows Forms](../advanced/how-to-create-standard-windows-forms-print-jobs.md)
- [Vorgehensweise: Erfassen von Benutzereingaben in einem „PrintDialog“ zur Laufzeit](../advanced/how-to-capture-user-input-from-a-printdialog-at-run-time.md)
- [PrintPreviewDialog-Steuerelement](printpreviewdialog-control-windows-forms.md)
- [PrintDialog-Komponente](printdialog-component-windows-forms.md)
- [Druckunterstützung in Windows Forms](../advanced/windows-forms-print-support.md)
- [Windows Forms Steuerelemente](index.md)
