---
title: Übersicht über die FolderBrowserDialog-Komponente
ms.date: 03/30/2017
f1_keywords:
- FolderBrowserDialog
helpviewer_keywords:
- FolderBrowserDialog component [Windows Forms], about FolderBrowserDialog
- directories [Windows Forms], enabling browsing in applications
- folders [Windows Forms], enabling browsing in applications
ms.assetid: 796b622c-3ba9-4356-93bb-e217fc52f2c7
ms.openlocfilehash: 8b017ba08ae4205e930ac00177c89a89fde17d3b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976000"
---
# <a name="folderbrowserdialog-component-overview-windows-forms"></a>Übersicht über die FolderBrowserDialog-Komponente (Windows Forms)

Die Windows Forms <xref:System.Windows.Forms.FolderBrowserDialog> Komponente ist ein modales Dialogfeld, das zum Durchsuchen und Auswählen von Ordnern verwendet wird. Neue Ordner können auch aus der Komponente erstellt werden <xref:System.Windows.Forms.FolderBrowserDialog> .

> [!NOTE]
> Verwenden Sie die [OpenFileDialog](openfiledialog-component-windows-forms.md) -Komponente, um Dateien anstelle von Ordnern auszuwählen.

Die <xref:System.Windows.Forms.FolderBrowserDialog> Komponente wird zur Laufzeit mithilfe der- <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode angezeigt. Legen <xref:System.Windows.Forms.FolderBrowserDialog.RootFolder%2A> Sie die-Eigenschaft fest, um den obersten Ordner und alle Unterordner zu bestimmen, die in der Strukturansicht des Dialog Felds angezeigt werden. Sobald das Dialogfeld angezeigt wird, können Sie die-Eigenschaft verwenden, <xref:System.Windows.Forms.FolderBrowserDialog.SelectedPath%2A> um den Pfad des ausgewählten Ordners zu erhalten.

Wenn Sie einem Formular hinzugefügt wird, wird die <xref:System.Windows.Forms.FolderBrowserDialog> Komponente in der Leiste am unteren Rand des Windows Forms-Designer in Visual Studio angezeigt.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.FolderBrowserDialog>
- [Vorgehensweise: Auswählen von Ordnern mit der FolderBrowserDialog-Komponente in Windows Forms](how-to-choose-folders-with-the-windows-forms-folderbrowserdialog-component.md)
- [FolderBrowserDialog-Komponente](folderbrowserdialog-component-windows-forms.md)
