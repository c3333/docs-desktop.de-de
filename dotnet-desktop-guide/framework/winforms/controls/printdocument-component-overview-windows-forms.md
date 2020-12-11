---
title: Übersicht über die PrintDocument-Komponente
ms.date: 03/30/2017
f1_keywords:
- PrintDocument
helpviewer_keywords:
- PrintDocument component [Windows Forms], about PrintDocument component
- printing [Windows Forms], PrintDocument component
ms.assetid: b59b4b60-dce5-42ca-8421-3a54a2f7bab0
ms.openlocfilehash: 96b18a44853d836cb0f16ba0e8372a825e998b74
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975527"
---
# <a name="printdocument-component-overview-windows-forms"></a>Übersicht über die PrintDocument-Komponente (Windows Forms)

Die Komponente [PrintDocument](printdocument-component-windows-forms.md) von Windows Forms wird verwendet, um die Eigenschaften festzulegen, die beschreiben, was gedruckt werden soll. Außerdem wird sie verwendet, um das Dokument in Windows-basierten Anwendungen drucken zu können. Sie kann zusammen mit der Komponente [PrintDialog](printdialog-component-windows-forms.md) verwendet werden, um alle Aspekte des Druckens eines Dokuments zu steuern.

## <a name="working-with-the-printdocument-component"></a>Arbeiten mit der PrintDocument-Komponente

Zwei der wichtigsten Szenarien, in denen die- <xref:System.Drawing.Printing.PrintDocument> Komponente enthalten ist, sind:

- Einfache Druckaufträge wie das Drucken einer einzelnen Textdatei. In einem solchen Fall würden Sie die <xref:System.Drawing.Printing.PrintDocument> Komponente zu einem Windows Form hinzufügen und dann eine Programmierlogik hinzufügen, die eine Datei im- <xref:System.Drawing.Printing.PrintDocument.PrintPage> Ereignishandler ausgibt. Die Programmierlogik sollte mit der- <xref:System.Drawing.Printing.PrintDocument.Print%2A> Methode zum Drucken des Dokuments in die-Methode münden. Diese Methode sendet ein- <xref:System.Drawing.Graphics> Objekt, das in der- <xref:System.Drawing.Printing.PrintPageEventArgs.Graphics%2A> Eigenschaft der- <xref:System.Drawing.Printing.PrintPageEventArgs> Klasse enthalten ist, an den Drucker. Ein Beispiel, das zeigt, wie ein Textdokument mithilfe der- <xref:System.Drawing.Printing.PrintDocument> Komponente gedruckt wird, finden Sie unter Gewusst [wie: Drucken einer mehrseitigen Textdatei in Windows Forms](../advanced/how-to-print-a-multi-page-text-file-in-windows-forms.md).

- Komplexere Druckaufträge, z.B. eine Situation, in der Sie bereits geschriebene Drucklogik wiederverwenden möchten. In einem solchen Fall leiten Sie eine neue Komponente von der <xref:System.Drawing.Printing.PrintDocument> Komponente ab und überschreiben (siehe [außer Kraft](/dotnet/csharp/language-reference/keywords/override) setzungen für Visual Basic oder [über](/dotnet/visual-basic/language-reference/modifiers/overrides) schreiben für c#) das <xref:System.Drawing.Printing.PrintDocument.PrintPage> Ereignis.

Wenn Sie einem Formular hinzugefügt wird, wird die <xref:System.Drawing.Printing.PrintDocument> Komponente in der Leiste am unteren Rand des Windows Forms-Designer in Visual Studio angezeigt.

## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Graphics>
- <xref:System.Drawing.Printing.PrintDocument>
- [Druckunterstützung in Windows Forms](../advanced/windows-forms-print-support.md)
- [PrintDocument-Komponente](printdocument-component-windows-forms.md)
