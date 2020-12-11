---
title: 'Exemplarische Vorgehensweise: Ausführen eines Vorgangs im Hintergrund'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- background tasks
- forms [Windows Forms], multithreading
- forms [Windows Forms], background operations
- background threads
- BackgroundWorker class [Windows Forms], examples
- threading [Windows Forms], background operations
- background operations
ms.assetid: 1b9a4e0a-f134-48ff-a1be-c461446a31ba
ms.openlocfilehash: ad0955937965c89b52648e37cd151e0cd266e527
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976593"
---
# <a name="walkthrough-running-an-operation-in-the-background"></a>Exemplarische Vorgehensweise: Ausführen eines Vorgangs im Hintergrund

Gibt es einen Vorgang, der bis zu seinem Abschluss eine lange Zeit in Anspruch nimmt, und Sie möchten keine Verzögerungen in der Benutzeroberfläche verursachen, können Sie die <xref:System.ComponentModel.BackgroundWorker>-Klasse dazu verwenden, den Vorgang über einen anderen Thread auszuführen.

Eine umfassende Liste des in diesem Beispiel verwendeten Codes finden Sie unter Gewusst [wie: Ausführen eines Vorgangs im Hintergrund](how-to-run-an-operation-in-the-background.md).

## <a name="run-an-operation-in-the-background"></a>Ausführen eines Vorgangs im Hintergrund

1. Wenn das Formular in der Windows Forms-Designer in Visual Studio aktiv ist, ziehen Sie zwei-Steuer <xref:System.Windows.Forms.Button> Elemente aus der **Toolbox** auf das Formular, und legen Sie dann die `Name` -Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.Control.Text%2A> der Schaltflächen entsprechend der folgenden Tabelle fest.

    |Schaltfläche|Name|Text|
    |------------|----------|----------|
    |`button1`|`startBtn`|**Starten**|
    |`button2`|`cancelBtn`|**Kündigen**|

2. Öffnen Sie die **Toolbox**, klicken Sie auf die Registerkarte **Komponenten** , und ziehen Sie die <xref:System.ComponentModel.BackgroundWorker> Komponente auf das Formular.

     Die `backgroundWorker1` Komponente wird in der **Komponenten Leiste** angezeigt.

3. Legen Sie im Fenster **Eigenschaften** die Eigenschaft <xref:System.ComponentModel.BackgroundWorker.WorkerSupportsCancellation%2A> auf `true`fest.

4. Klicken Sie im Fenster **Eigenschaften** auf die Schaltfläche **Ereignisse** , und doppelklicken Sie dann <xref:System.ComponentModel.BackgroundWorker.DoWork> auf das-Ereignis und das-Ereignis, <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> um Ereignishandler zu erstellen.

5. Fügen Sie den zeitaufwändigen Code in den- <xref:System.ComponentModel.BackgroundWorker.DoWork> Ereignishandler ein.

6. Extrahieren Sie alle Parameter, die für den Vorgang erforderlich sind, aus der- <xref:System.ComponentModel.DoWorkEventArgs.Argument%2A> Eigenschaft des <xref:System.ComponentModel.DoWorkEventArgs> Parameters.

7. Weisen Sie das Ergebnis der Berechnung der- <xref:System.ComponentModel.DoWorkEventArgs.Result%2A> Eigenschaft von zu <xref:System.ComponentModel.DoWorkEventArgs> .

     Diese ist für den- <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> Ereignishandler verfügbar.

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#2)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#2)]

8. Fügen Sie Code zum Abrufen des Ergebnisses des Vorgangs im- <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> Ereignishandler ein.

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#3)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#3)]

9. Implementieren Sie die `TimeConsumingOperation`-Methode.

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#4)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#4)]

10. Doppelklicken Sie in der Windows Forms-Designer `startButton` auf, um den <xref:System.Windows.Forms.Control.Click> Ereignishandler zu erstellen.

11. Die- <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> Methode wird im- <xref:System.Windows.Forms.Control.Click> Ereignishandler für aufgerufen `startButton` .

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#5)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#5)]

12. Doppelklicken Sie in der Windows Forms-Designer `cancelButton` auf, um den <xref:System.Windows.Forms.Control.Click> Ereignishandler zu erstellen.

13. Die- <xref:System.ComponentModel.BackgroundWorker.CancelAsync%2A> Methode wird im- <xref:System.Windows.Forms.Control.Click> Ereignishandler für aufgerufen `cancelButton` .

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#6](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#6)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#6](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#6)]

14. Importieren Sie am Anfang der Datei die Namespaces System. ComponentModel und System. Threading.

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#7](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#7)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#7](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#7)]

15. Drücken Sie **F6** , um die Projekt Mappe zu erstellen, und drücken Sie dann **STRG** + **F5** , um die Anwendung außerhalb des Debuggers auszuführen.

    > [!NOTE]
    > Wenn Sie **F5** drücken, um die Anwendung unter dem Debugger auszuführen, wird die in der Methode ausgelöste Ausnahme abgefangen `TimeConsumingOperation` und vom Debugger angezeigt. Wenn Sie die Anwendung außerhalb des Debuggers ausführen, <xref:System.ComponentModel.BackgroundWorker> verarbeitet die Ausnahme und speichert Sie in der- <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A> Eigenschaft des-Objekts zwischen <xref:System.ComponentModel.RunWorkerCompletedEventArgs> .

16. Klicken Sie auf die Schaltfläche **Start** , um einen asynchronen Vorgang auszuführen, und klicken Sie dann auf die Schaltfläche **Abbrechen** , um einen laufenden asynchronen Vorgang zu beenden.

     Das Ergebnis jedes Vorgangs wird in einem <xref:System.Windows.Forms.MessageBox>-Steuerelement angezeigt.

## <a name="next-steps"></a>Nächste Schritte

- Implementieren Sie ein Formular, das den Status meldet, wenn ein asynchroner Vorgang fortgesetzt wird. Weitere Informationen finden Sie unter Gewusst [wie: Implementieren eines Formulars, das einen Hintergrund Vorgang verwendet](how-to-implement-a-form-that-uses-a-background-operation.md).

- Implementieren Sie eine Klasse, die das asynchrone Muster für Komponenten unterstützt. Weitere Informationen finden Sie unter [Implementieren des ereignisbasierten asynchronen Musters](/dotnet/standard/asynchronous-programming-patterns/implementing-the-event-based-asynchronous-pattern).

## <a name="see-also"></a>Siehe auch

- <xref:System.ComponentModel.BackgroundWorker>
- <xref:System.ComponentModel.DoWorkEventArgs>
- [How to: Implementieren eines Formulars, das eine Hintergrundoperation verwendet](how-to-implement-a-form-that-uses-a-background-operation.md)
- [How to: Ausführen eines Vorgangs im Hintergrund](how-to-run-an-operation-in-the-background.md)
- [BackgroundWorker-Komponente](backgroundworker-component.md)
