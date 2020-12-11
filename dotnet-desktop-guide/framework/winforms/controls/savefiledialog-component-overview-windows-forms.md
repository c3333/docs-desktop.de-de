---
title: Übersicht über die SaveFileDialog-Komponente
ms.date: 03/30/2017
f1_keywords:
- SaveFileDialog
helpviewer_keywords:
- Save File dialog box [Windows Forms], displaying
- SaveFileDialog component [Windows Forms], about SaveFileDialog
ms.assetid: be7a625f-46fd-4d06-9985-b613dcbf9bd2
ms.openlocfilehash: 7609c29b7e932ecee7dc8a289617094bd8d480e2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972338"
---
# <a name="savefiledialog-component-overview-windows-forms"></a>Übersicht über die SaveFileDialog-Komponente (Windows Forms)

Bei der Windows Forms-Komponente <xref:System.Windows.Forms.SaveFileDialog> handelt es sich um ein vorkonfiguriertes Dialogfeld. Dies ist das gleiche wie das von Windows verwendete Standard Dialogfeld zum **Speichern von Dateien** . Sie erbt von der <xref:System.Windows.Forms.CommonDialog>-Klasse.

## <a name="working-with-the-savefiledialog-component"></a>Arbeiten mit der SaveFileDialog-Komponente

Verwenden Sie es als einfache Lösung, um Benutzern das Speichern von Dateien zu ermöglichen, anstatt ein eigenes Dialogfeld zu konfigurieren. Wenn Sie sich auf standardmäßige Windows-Dialogfelder verlassen, sind die grundlegenden Funktionen der Anwendungen, die Sie erstellen, Benutzern sofort vertraut. Beachten Sie jedoch, dass Sie bei der Verwendung der- <xref:System.Windows.Forms.SaveFileDialog> Komponente eine eigene Logik zum Speichern von Dateien schreiben müssen.

Sie können die- <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode verwenden, um das Dialogfeld zur Laufzeit anzuzeigen. Sie können eine Datei im Lese-/Schreibmodus mit der- <xref:System.Windows.Forms.SaveFileDialog.OpenFile%2A> Methode öffnen.

Wenn Sie einem Formular hinzugefügt wird, wird die <xref:System.Windows.Forms.SaveFileDialog> Komponente in der Leiste am unteren Rand des Windows Forms-Designer in Visual Studio angezeigt.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.SaveFileDialog>
- [SaveFileDialog-Komponente](savefiledialog-component-windows-forms.md)
