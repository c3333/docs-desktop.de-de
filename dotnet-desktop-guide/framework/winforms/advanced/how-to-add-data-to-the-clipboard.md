---
title: 'Vorgehensweise: Hinzufügen von Daten zur Zwischenablage'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Clipboard [Windows Forms], copying data to
- data [Windows Forms], copying to Clipboard
ms.assetid: 25152454-0e78-40a9-8a9e-a2a5a274e517
ms.openlocfilehash: 0d9b82f01080d18353ecb91578a8005260bbe739
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972384"
---
# <a name="how-to-add-data-to-the-clipboard"></a>Vorgehensweise: Hinzufügen von Daten zur Zwischenablage

Die- <xref:System.Windows.Forms.Clipboard> Klasse stellt Methoden bereit, die Sie verwenden können, um mit der Zwischenablage des Windows-Betriebssystems zu interagieren. Viele Anwendungen verwenden die Zwischenablage als temporäres Repository für-Daten. Beispielsweise wird die Zwischenablage von Word-Prozessoren während Ausschneide-und Einfügevorgängen verwendet. Die Zwischenablage ist auch nützlich für die Übertragung von Daten von einer Anwendung in eine andere.

Wenn Sie der Zwischenablage Daten hinzufügen, können Sie das Datenformat angeben, damit andere Anwendungen die Daten erkennen können, wenn Sie dieses Format verwenden können. Sie können der Zwischenablage auch Daten in mehreren verschiedenen Formaten hinzufügen, um die Anzahl von anderen Anwendungen zu erhöhen, die die Daten potenziell verwenden können.

Ein Zwischenablage Format ist eine Zeichenfolge, die das Format identifiziert, sodass eine Anwendung, die dieses Format verwendet, die zugeordneten Daten abrufen kann. Die- <xref:System.Windows.Forms.DataFormats> Klasse stellt vordefinierte Format Namen für ihre Verwendung bereit. Sie können auch Ihre eigenen Format Namen verwenden oder den Typ eines Objekts als Format verwenden.

Verwenden Sie die-Methode, um der Zwischenablage in einem oder mehreren Formaten Daten hinzuzufügen <xref:System.Windows.Forms.Clipboard.SetDataObject%2A> . Sie können ein beliebiges-Objekt an diese Methode übergeben, aber zum Hinzufügen von Daten in mehreren Formaten müssen Sie die Daten zunächst einem separaten-Objekt hinzufügen, das für die Verwendung mit mehreren Formaten entworfen wurde. In der Regel fügen Sie die Daten zu einem hinzu <xref:System.Windows.Forms.DataObject> , aber Sie können einen beliebigen Typ verwenden, der die- <xref:System.Windows.Forms.IDataObject> Schnittstelle implementiert.

In .NET Framework 2,0 können Sie Daten direkt der Zwischenablage hinzufügen, indem Sie neue Methoden verwenden, die dazu dienen, grundlegende Aufgaben in der Zwischenablage zu vereinfachen. Verwenden Sie diese Methoden, wenn Sie mit Daten in einem einzelnen, allgemeinen Format wie z. b. Text arbeiten.

> [!NOTE]
> Alle Windows-basierten Anwendungen verwenden die Zwischenablage gemeinsam. Daher können sich die Inhalte ändern, wenn Sie zu einer anderen Anwendung wechseln.
>
> Die- <xref:System.Windows.Forms.Clipboard> Klasse kann nur in Threads verwendet werden, die auf den STA-Modus (Single Thread Apartment) festgelegt sind. Um diese Klasse zu verwenden, stellen Sie sicher, dass `Main` die-Methode mit dem-Attribut gekennzeichnet ist <xref:System.STAThreadAttribute> .
>
> Ein Objekt muss serialisierbar sein, damit es in die Zwischenablage eingefügt werden kann. Um einen Typ serialisierbar zu machen, markieren Sie ihn mit dem- <xref:System.SerializableAttribute> Attribut. Wenn Sie ein nicht serialisierbares Objekt an eine Zwischenablage Methode übergeben, schlägt die Methode fehl, ohne dass eine Ausnahme ausgelöst wird. Weitere Informationen zur Serialisierung finden Sie unter <xref:System.Runtime.Serialization>.

### <a name="to-add-data-to-the-clipboard-in-a-single-common-format"></a>So fügen Sie der Zwischenablage Daten in einem einzelnen, allgemeinen Format hinzu

1. Verwenden Sie die-,-,- <xref:System.Windows.Forms.Clipboard.SetAudio%2A> <xref:System.Windows.Forms.Clipboard.SetFileDropList%2A> oder- <xref:System.Windows.Forms.Clipboard.SetImage%2A> <xref:System.Windows.Forms.Clipboard.SetText%2A> Methode. Diese Methoden sind nur in .NET Framework 2,0 verfügbar.

    [!code-csharp[System.Windows.Forms.Clipboard#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Clipboard/CS/form1.cs#2)]
    [!code-vb[System.Windows.Forms.Clipboard#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Clipboard/vb/form1.vb#2)]

### <a name="to-add-data-to-the-clipboard-in-a-custom-format"></a>So fügen Sie der Zwischenablage Daten in einem benutzerdefinierten Format hinzu

1. Verwenden Sie die- <xref:System.Windows.Forms.Clipboard.SetData%2A> Methode mit einem benutzerdefinierten Format Namen. Diese Methode ist nur in .NET Framework 2,0 verfügbar.

    Sie können auch vordefinierte Format Namen mit der- <xref:System.Windows.Forms.Clipboard.SetData%2A> Methode verwenden. Weitere Informationen finden Sie unter <xref:System.Windows.Forms.DataFormats>.

    [!code-csharp[System.Windows.Forms.Clipboard#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Clipboard/CS/form1.cs#3)]
    [!code-vb[System.Windows.Forms.Clipboard#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Clipboard/vb/form1.vb#3)]
    [!code-csharp[System.Windows.Forms.Clipboard#100](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Clipboard/CS/form1.cs#100)]
    [!code-vb[System.Windows.Forms.Clipboard#100](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Clipboard/vb/form1.vb#100)]

### <a name="to-add-data-to-the-clipboard-in-multiple-formats"></a>So fügen Sie der Zwischenablage Daten in mehreren Formaten hinzu

1. Verwenden <xref:System.Windows.Forms.Clipboard.SetDataObject%2A?displayProperty=nameWithType> Sie die-Methode, und übergeben <xref:System.Windows.Forms.DataObject> Sie einen, der Ihre Daten enthält. Sie müssen diese Methode verwenden, um der Zwischenablage in früheren Versionen als .NET Framework 2,0 Daten hinzuzufügen.

    [!code-csharp[System.Windows.Forms.Clipboard#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Clipboard/CS/form1.cs#4)]
    [!code-vb[System.Windows.Forms.Clipboard#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Clipboard/vb/form1.vb#4)]
    [!code-csharp[System.Windows.Forms.Clipboard#100](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Clipboard/CS/form1.cs#100)]
    [!code-vb[System.Windows.Forms.Clipboard#100](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Clipboard/vb/form1.vb#100)]

## <a name="see-also"></a>Siehe auch

- [Drag &amp;amp; Drop-Operationen und Unterstützung der Zwischenablage](drag-and-drop-operations-and-clipboard-support.md)
- [Vorgehensweise: Abrufen von Daten aus der Zwischenablage](how-to-retrieve-data-from-the-clipboard.md)
