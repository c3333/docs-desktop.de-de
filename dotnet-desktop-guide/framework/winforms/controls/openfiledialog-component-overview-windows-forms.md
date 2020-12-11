---
title: Übersicht über die OpenFileDialog-Komponente
ms.date: 03/30/2017
f1_keywords:
- OpenFileDialog
helpviewer_keywords:
- OpenFileDialog component [Windows Forms], about OpenFileDialog
- Open File dialog box [Windows Forms], displaying in Windows Forms
ms.assetid: cd717300-46b6-4f82-8207-b218fa7fa407
ms.openlocfilehash: c519b373150a49ee41dbb0c503f7d5a4862477d5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976697"
---
# <a name="openfiledialog-component-overview-windows-forms"></a>Übersicht über die OpenFileDialog-Komponente (Windows Forms)

Bei der Windows Forms-Komponente <xref:System.Windows.Forms.OpenFileDialog> handelt es sich um ein vorkonfiguriertes Dialogfeld. Es ist das gleiche Dialogfeld **Öffnen** , das vom Windows-Betriebssystem verfügbar gemacht wird. Sie erbt von der <xref:System.Windows.Forms.CommonDialog>-Klasse.

## <a name="use-this-component"></a>Diese Komponente verwenden

Verwenden Sie diese Komponente in der Windows-basierten Anwendung als einfache Lösung für die Dateiauswahl, anstatt ein eigenes Dialogfeld zu konfigurieren. Durch die Verwendung von Windows-Standarddialogfeldern erstellen Sie Anwendungen, deren Basisfunktionen Benutzern sofort vertraut sind. Beachten Sie jedoch, dass Sie bei Verwendung der- <xref:System.Windows.Forms.OpenFileDialog> Komponente eine eigene Datei öffnende Logik schreiben müssen.

Verwenden Sie die- <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode, um das Dialogfeld zur Laufzeit anzuzeigen. Sie können es Benutzern ermöglichen, Dateien mit mehreren SELECT-Dateien zu öffnen, die mit der-Eigenschaft geöffnet werden <xref:System.Windows.Forms.OpenFileDialog.Multiselect%2A> . Darüber hinaus können Sie die- <xref:System.Windows.Forms.OpenFileDialog.ShowReadOnly%2A> Eigenschaft verwenden, um zu bestimmen, ob im Dialogfeld ein Schreib geschütztes Kontrollkästchen angezeigt wird. Die- <xref:System.Windows.Forms.OpenFileDialog.ReadOnlyChecked%2A> Eigenschaft gibt an, ob das Kontrollkästchen Schreibgeschützt aktiviert ist. Schließlich legt die- <xref:System.Windows.Forms.FileDialog.Filter%2A> Eigenschaft die aktuelle Filter Zeichenfolge für den Dateinamen fest, die die im Dialogfeld im Feld "Dateityp" angezeigten Optionen bestimmt.

Wenn Sie einem Formular hinzugefügt wird, wird die <xref:System.Windows.Forms.OpenFileDialog> Komponente in der Leiste am unteren Rand des Windows Forms-Designer in Visual Studio angezeigt.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.OpenFileDialog>
- [OpenFileDialog-Komponente](openfiledialog-component-windows-forms.md)
