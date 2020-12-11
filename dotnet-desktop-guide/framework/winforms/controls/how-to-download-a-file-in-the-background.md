---
title: 'Vorgehensweise: Downloaden einer Datei im Hintergrund'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- BackgroundWorker component
- background tasks
- Asynchronous Pattern
- forms [Windows Forms], multithreading
- components [Windows Forms], asynchronous
- forms [Windows Forms], background operations
- threading [Windows Forms], background operations
- background operations
ms.assetid: 9b7bc5ae-051c-4904-9720-18f6667388bd
ms.openlocfilehash: ed7d5593a29726412f5ea75812cf5a6d800ee77a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975646"
---
# <a name="how-to-download-a-file-in-the-background"></a>Vorgehensweise: Downloaden einer Datei im Hintergrund
Das Herunterladen von Dateien ist eine häufige Aufgabe, und es ist oft sinnvoll, diesen potenziell zeitaufwendigen Vorgang in einem separaten Thread auszuführen. Mithilfe der <xref:System.ComponentModel.BackgroundWorker>-Komponente können Sie diese Aufgabe mit nur wenigen Codezeilen ausführen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird die Verwendung einer <xref:System.ComponentModel.BackgroundWorker>-Komponente zum Laden einer XML-Datei über eine URL veranschaulicht. Wenn der Benutzer auf die Schaltfläche **herunterladen** klickt, <xref:System.Windows.Forms.Control.Click> ruft der Ereignishandler die- <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> Methode einer <xref:System.ComponentModel.BackgroundWorker> Komponente auf, um den Downloadvorgang zu starten. Während des Downloads ist die Schaltfläche deaktiviert, und nach Abschluss des Downloads wird sie wieder aktiviert. Ein <xref:System.Windows.Forms.MessageBox> zeigt den Inhalt der Datei an.  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#1)]  
  
 **Herunterladen der Datei**  
  
 Die Datei wird im Arbeitsthread der <xref:System.ComponentModel.BackgroundWorker>-Komponente heruntergeladen, der den <xref:System.ComponentModel.BackgroundWorker.DoWork>-Ereignishandler ausführt. Dieser Thread startet, wenn vom Code die <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A>-Methode aufgerufen wird.  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#3)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#3)]  
  
 **Warten auf die Beendigung von „BackgroundWorker“**  
  
 Der `downloadButton_Click`-Ereignishandler veranschaulicht, wie auf den Abschluss der asynchronen Aufgabe einer <xref:System.ComponentModel.BackgroundWorker>-Komponente gewartet wird.  
  
 Wenn die Anwendung nur auf Ereignisse reagieren soll und im Hauptthread keine Vorgänge ausgeführt werden sollen, während auf den Abschluss des Hintergrundthreads gewartet wird, können Sie den Handler einfach beenden.  
  
 Wenn Sie im Hauptthread weitere Schritte ausführen möchten, verwenden Sie die <xref:System.ComponentModel.BackgroundWorker.IsBusy%2A>-Eigenschaft, um zu ermitteln, ob der <xref:System.ComponentModel.BackgroundWorker>-Thread noch ausgeführt wird. Im Beispiel wird eine Statusanzeige aktualisiert, während der Download verarbeitet wird. Sie müssen die <xref:System.Windows.Forms.Application.DoEvents%2A?displayProperty=nameWithType>-Methode aufrufen, damit die Benutzeroberfläche weiterhin auf Aktionen reagiert.  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#2)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#2)]  
  
 **Anzeigen des Ergebnisses**  
  
 Die `backgroundWorker1_RunWorkerCompleted`-Methode behandelt das <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted>-Ereignis und wird aufgerufen, wenn der Hintergrundvorgang abgeschlossen ist. Diese Methode überprüft zuerst die <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType>-Eigenschaft. Wenn <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType> den Wert `null` aufweist, zeigt die Methode den Inhalt der Datei an. Anschließend wird die Schaltfläche "Herunterladen" wieder aktiviert, die zu Beginn des Downloads deaktiviert wurde, und die Statusanzeige wird zurückgesetzt.  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#4)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#4)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Verweise auf die Assemblys "System.Drawing", "System.Windows.Forms" und "System.XML".  
  
## <a name="robust-programming"></a>Stabile Programmierung  
 Überprüfen Sie immer die <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType>-Eigenschaft im <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted>-Ereignishandler, bevor Sie auf die <xref:System.ComponentModel.RunWorkerCompletedEventArgs.Result%2A?displayProperty=nameWithType>-Eigenschaft oder auf ein anderes Objekt zugreifen, auf das der <xref:System.ComponentModel.BackgroundWorker.DoWork>-Ereignishandler Einfluss haben kann.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.ComponentModel.BackgroundWorker>
- [How to: Ausführen eines Vorgangs im Hintergrund](how-to-run-an-operation-in-the-background.md)
- [How to: Implementieren eines Formulars, das eine Hintergrundoperation verwendet](how-to-implement-a-form-that-uses-a-background-operation.md)
