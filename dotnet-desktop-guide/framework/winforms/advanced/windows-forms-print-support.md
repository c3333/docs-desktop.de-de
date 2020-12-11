---
title: Druckunterstützung
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, printing
- printing [Windows Forms]
- forms [Windows Forms], printing (using designer)
- printing [Windows Forms], Windows Forms, support
- printing [Windows Forms], print support
ms.assetid: a4a2960c-eb70-48e2-b641-cfb222704e46
ms.openlocfilehash: d6e8f60db7afe2f1b04eaae6fe71aa93e5c22cae
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975808"
---
# <a name="windows-forms-print-support"></a>Druckunterstützung in Windows Forms
Das Drucken in Windows Forms besteht hauptsächlich aus der Verwendung der [PrintDocument-Komponenten](../controls/printdocument-component-windows-forms.md) Komponente, um dem Benutzer das Drucken zu ermöglichen, und dem [PrintPreviewDialog-Steuer](../controls/printpreviewdialog-control-windows-forms.md) Element-Steuerelement, der [PrintDialog-Komponente](../controls/printdialog-component-windows-forms.md) und den [PageSetupDialog](../controls/pagesetupdialog-component-windows-forms.md) -Komponenten Komponenten, um Benutzern eine vertraute grafische Oberfläche bereitzustellen  
  
 In der Regel erstellen Sie eine neue Instanz der <xref:System.Drawing.Printing.PrintDocument> Komponente, legen die Eigenschaften fest, die beschreiben, was mit der <xref:System.Drawing.Printing.PrinterSettings> -Klasse und der- <xref:System.Drawing.Printing.PageSettings> Klasse gedruckt werden soll, und rufen die- <xref:System.Drawing.Printing.PrintDocument.Print%2A> Methode auf, um das Dokument zu drucken.  
  
 Während des Druckens aus einer Windows-basierten Anwendung <xref:System.Drawing.Printing.PrintDocument> zeigt die Komponente ein Dialogfeld zum Abbrechen des Abbruchs an, in dem Benutzer darauf aufmerksam gemacht werden, dass der Druckvorgang abgebrochen wird und der Druckauftrag abgebrochen werden kann.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Vorgehensweise: Erstellen von standardmäßigen Druckaufträgen in Windows Forms](how-to-create-standard-windows-forms-print-jobs.md)  
 Erläutert, wie die- <xref:System.Drawing.Printing.PrintDocument> Komponente verwendet wird, um aus einem Windows Form zu drucken.  
  
 [Vorgehensweise: Erfassen von Benutzereingaben in einem „PrintDialog“ zur Laufzeit](how-to-capture-user-input-from-a-printdialog-at-run-time.md)  
 Erläutert, wie ausgewählte Druckoptionen Programm gesteuert mithilfe der- <xref:System.Windows.Forms.PrintDialog> Komponente geändert werden.  
  
 [Vorgehensweise: Auswählen der einem Benutzercomputer zugewiesenen Drucker in Windows Forms](how-to-choose-the-printers-attached-to-user-computer-in-windows-forms.md)  
 Beschreibt das Ändern des Druckers für das Drucken in mithilfe der <xref:System.Windows.Forms.PrintDialog> Komponente zur Laufzeit.  
  
 [How to: Drucken von Grafiken in Windows Forms](how-to-print-graphics-in-windows-forms.md)  
 Beschreibt das Senden von Grafiken an den Drucker.  
  
 [How to: Drucken einer mehrseitigen Textdatei in Windows Forms](how-to-print-a-multi-page-text-file-in-windows-forms.md)  
 Beschreibt das Senden von Text an den Drucker.  
  
 [Vorgehensweise: Fertigstellen von Druckaufträgen in Windows Forms](how-to-complete-windows-forms-print-jobs.md)  
 Erläutert, wie Benutzer zur Beendigung eines Druckauftrags gewarnt werden.  
  
 [Vorgehensweise: Drucken in Windows Forms](how-to-print-a-windows-form.md)  
 Zeigt, wie eine Kopie des aktuellen Formulars gedruckt wird.  
  
 [Vorgehensweise: Drucken in Windows Forms unter Verwendung der Seitenansicht](how-to-print-in-windows-forms-using-print-preview.md)  
 Zeigt, wie ein <xref:System.Windows.Forms.PrintPreviewDialog> zum Drucken eines Dokuments verwendet wird.  
  
## <a name="related-sections"></a>Verwandte Abschnitte  
 [PrintDocument-Komponente](../controls/printdocument-component-windows-forms.md)  
 Erläutert die Verwendung der- <xref:System.Drawing.Printing.PrintDocument> Komponente.  
  
 [PrintDialog-Komponente](../controls/printdialog-component-windows-forms.md)  
 Erläutert die Verwendung der- <xref:System.Windows.Forms.PrintDialog> Komponente.  
  
 [PrintPreviewDialog-Steuerelement](../controls/printpreviewdialog-control-windows-forms.md)  
 Erläutert die Verwendung des- <xref:System.Windows.Forms.PrintPreviewDialog> Steuer Elements.  
  
 [PageSetupDialog-Komponente](../controls/pagesetupdialog-component-windows-forms.md)  
 Erläutert die Verwendung der- <xref:System.Windows.Forms.PageSetupDialog> Komponente.  
  
 <xref:System.Drawing.Printing>  
 Beschreibt die Klassen im- <xref:System.Drawing.Printing> Namespace.
