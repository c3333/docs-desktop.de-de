---
title: Übersicht über das PrintPreviewControl-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- PrintPreviewControl
helpviewer_keywords:
- print preview
- PrintPreviewControl control
ms.assetid: 4513c6c7-5e9b-4f4c-82ca-00f993a26955
ms.openlocfilehash: 8dfe5802a24d5ec85ed908fd04c5550e1fbec012
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976885"
---
# <a name="printpreviewcontrol-control-overview-windows-forms"></a>Übersicht über das PrintPreviewControl-Steuerelement (Windows Forms)
Der Windows Forms <xref:System.Windows.Forms.PrintPreviewControl> wird zum Anzeigen eines [PrintDocument](printdocument-component-windows-forms.md) verwendet, so wie es gedruckt wird. Da dieses Steuerelement weder Schaltflächen noch andere Elemente einer Benutzeroberfläche besitzt, verwenden Sie <xref:System.Windows.Forms.PrintPreviewControl> in der Regel nur, wenn Sie eine eigene Benutzeroberfläche für die Seitenansicht programmieren möchten. Wenn Sie die Standardbenutzer Oberfläche verwenden möchten, verwenden Sie ein- <xref:System.Windows.Forms.PrintPreviewDialog> Steuerelement. eine Übersicht finden Sie unter [Übersicht über das PrintPreviewDialog-Steuer](printpreviewdialog-control-overview-windows-forms.md) Element.  
  
## <a name="key-properties"></a>Schlüsseleigenschaften  
 Die Schlüsseleigenschaft des Steuer Elements ist <xref:System.Windows.Forms.PrintPreviewControl.Document%2A> , wodurch das Dokument in der Vorschau angezeigt wird. Das Dokument muss ein- <xref:System.Drawing.Printing.PrintDocument> Objekt sein. Eine Übersicht über das Erstellen von Dokumenten für den Druck finden Sie unter Übersicht über die [PrintDocument-Komponente](printdocument-component-overview-windows-forms.md) und [Windows Forms Druckunterstützung](../advanced/windows-forms-print-support.md). Die <xref:System.Windows.Forms.PrintPreviewControl.Columns%2A> <xref:System.Windows.Forms.PrintPreviewControl.Rows%2A> Eigenschaften und bestimmen die Anzahl der Seiten, die horizontal und vertikal auf dem Steuerelement angezeigt werden. Das Antialiasing kann dazu führen, dass der Text glatter erscheint, aber auch die Anzeige langsamer wird. um es zu verwenden, legen Sie die- <xref:System.Windows.Forms.PrintPreviewControl.UseAntiAlias%2A> Eigenschaft auf fest `true` .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.PrintPreviewControl>
- [Übersicht über das PrintPreviewDialog-Steuerelement](printpreviewdialog-control-overview-windows-forms.md)
- [PrintPreviewControl-Steuerelement](printpreviewcontrol-control-windows-forms.md)
- [Dialogfeld-Steuerelemente und -Komponenten](dialog-box-controls-and-components-windows-forms.md)
