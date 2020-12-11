---
title: 'Exemplarische Vorgehensweise: Implementieren eines Formulars, das eine Hintergrundoperation verwendet'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- threading [Windows Forms], forms
- BackgroundWorker component
- background tasks
- forms [Windows Forms], multithreading
- threading [Windows Forms], walkthroughs
- forms [Windows Forms], background operations
- threading [Windows Forms], background operations
- background operations
ms.assetid: 4691b796-9200-471a-89c3-ba4c7cc78c03
ms.openlocfilehash: bdd82b0f32f93fbcdd5713bfb9ba9081f653298b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976600"
---
# <a name="walkthrough-implementing-a-form-that-uses-a-background-operation"></a>Exemplarische Vorgehensweise: Implementieren eines Formulars, das eine Hintergrundoperation verwendet

Wenn Sie über einen Vorgang verfügen, der viel Zeit in Anspruch nimmt, und Sie nicht möchten, dass die Benutzeroberfläche nicht mehr reagiert oder blockiert wird, können Sie die-Klasse verwenden, <xref:System.ComponentModel.BackgroundWorker> um den Vorgang auf einem anderen Thread auszuführen.

In dieser exemplarischen Vorgehensweise wird veranschaulicht <xref:System.ComponentModel.BackgroundWorker> , wie die-Klasse verwendet wird, um zeitaufwändige Berechnungen "im Hintergrund" auszuführen, während die Benutzeroberfläche weiterhin reaktionsfähig ist.  Wenn Sie diese exemplarische Vorgehensweise abgeschlossen haben, verfügen Sie über eine Anwendung, die Fibonacci-Zahlen asynchron berechnet. Obwohl das Berechnen einer großen Fibonacci-Zahl merklich Zeit in Anspruch nimmt, wird der Haupt-UI-Thread nicht von dieser Verzögerung unterbrochen, und das Formular behält während der Berechnung seine Reaktionsfähigkeit.

In dieser exemplarischen Vorgehensweise werden u. a. folgende Aufgaben veranschaulicht:

- Erstellen einer Windows-basierten Anwendung

- Erstellen einer <xref:System.ComponentModel.BackgroundWorker> in Ihrem Formular

- Hinzufügen Asynchroner Ereignishandler

- Hinzufügen von Statusberichterstellung und Abbruchunterstützung

Eine vollständige Liste des in diesem Beispiel verwendeten Codes finden Sie unter [Vorgehensweise: Implementieren eines Formulars, das eine Hintergrundoperation verwendet](how-to-implement-a-form-that-uses-a-background-operation.md).

## <a name="create-a-form-that-uses-a-background-operation"></a>Erstellen eines Formulars, das einen Hintergrund Vorgang verwendet

1. Erstellen Sie in Visual Studio ein Windows-basiertes Anwendungsprojekt mit dem Namen `BackgroundWorkerExample` (**File**  >  **New**  >  **Project**  >  **Visual c#** oder **Visual Basic**  >  **Classic Desktop**  >  **Windows Forms Anwendung**).

2. Klicken Sie im **Projektmappen-Explorer** mit der rechten Maustaste auf **Form1**, und wählen Sie im Kontextmenü **Umbenennen** aus. Ändern Sie den Dateinamen in `FibonacciCalculator`. Klicken Sie auf die Schaltfläche **Ja**, wenn Sie gefragt werden, ob alle Verweise auf das Codeelement `Form1` umbenannt werden sollen.

3. Ziehen Sie ein- <xref:System.Windows.Forms.NumericUpDown> Steuerelement aus der **Toolbox** auf das Formular. Legen <xref:System.Windows.Forms.NumericUpDown.Minimum%2A> Sie die-Eigenschaft auf `1` und die- <xref:System.Windows.Forms.NumericUpDown.Maximum%2A> Eigenschaft auf fest `91` .

4. Fügen Sie <xref:System.Windows.Forms.Button> dem Formular zwei-Steuerelemente hinzu.

5. Benennen Sie das erste <xref:System.Windows.Forms.Button> Steuerelement `startAsyncButton` um und legen Sie die- <xref:System.Windows.Forms.Control.Text%2A> Eigenschaft auf fest `Start Async` Benennen Sie das zweite <xref:System.Windows.Forms.Button> Steuerelement `cancelAsyncButton` um und legen Sie die- <xref:System.Windows.Forms.Control.Text%2A> Eigenschaft auf fest `Cancel Async` . Legen Sie die- <xref:System.Windows.Forms.Control.Enabled%2A> Eigenschaft auf fest `false` .

6. Erstellen Sie einen Ereignishandler für beide Ereignisse der-Steuer <xref:System.Windows.Forms.Button> Elemente <xref:System.Windows.Forms.Control.Click> . Weitere Informationen finden Sie unter [Vorgehensweise: Erstellen von Ereignishandlern mithilfe des Designers](/previous-versions/visualstudio/visual-studio-2010/zwwsdtbk(v=vs.100)).

7. Ziehen <xref:System.Windows.Forms.Label> Sie ein-Steuerelement aus der **Toolbox** auf das Formular, und benennen Sie es um `resultLabel` .

8. Ziehen Sie ein- <xref:System.Windows.Forms.ProgressBar> Steuerelement aus der **Toolbox** auf das Formular.

## <a name="create-a-backgroundworker-with-the-designer"></a>Erstellen eines BackgroundWorker mit dem Designer

Sie können den <xref:System.ComponentModel.BackgroundWorker> für den asynchronen Vorgang mit dem **Windows** **Forms-Designer** erstellen.

Ziehen Sie auf der Registerkarte **Komponenten** der **Toolbox** eine <xref:System.ComponentModel.BackgroundWorker> auf das Formular.

## <a name="add-asynchronous-event-handlers"></a>Asynchrone Ereignishandler hinzufügen

Sie können nun Ereignishandler für die <xref:System.ComponentModel.BackgroundWorker> asynchronen Ereignisse der Komponente hinzufügen. Der zeitaufwändige Vorgang im Hintergrund, der die Fibonacci-Zahlen berechnet, wird von einem dieser Ereignishandler aufgerufen.

1. Klicken Sie im Fenster **Eigenschaften** , während die <xref:System.ComponentModel.BackgroundWorker> Komponente noch ausgewählt ist, auf die Schaltfläche **Ereignisse** . Doppelklicken Sie <xref:System.ComponentModel.BackgroundWorker.DoWork> auf das-Ereignis und das- <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> Ereignis, um Ereignishandler zu erstellen. Informationen zur Verwendung von Ereignishandlern finden Sie unter [Vorgehensweise: Erstellen von Ereignishandlern mithilfe des Designers](/previous-versions/visualstudio/visual-studio-2010/zwwsdtbk(v=vs.100)).

2. Erstellen Sie im Formular eine neue Methode namens `ComputeFibonacci`. Diese Methode führt die eigentliche Arbeit aus und wird im Hintergrund ausgeführt. Dieser Code veranschaulicht die rekursive Umsetzung des Fibonacci-Algorithmus, der deutlich ineffizient ist und wesentlich mehr Zeit in Anspruch nimmt, große Zahlen abzuschließen. Er wird hier verwendet, um einen Vorgang zu veranschaulichen, der lange Verzögerungen in der Anwendung verursachen kann.

     [!code-cpp[System.ComponentModel.BackgroundWorker#10](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#10)]
     [!code-csharp[System.ComponentModel.BackgroundWorker#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#10)]
     [!code-vb[System.ComponentModel.BackgroundWorker#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#10)]

3. <xref:System.ComponentModel.BackgroundWorker.DoWork>Fügen Sie im-Ereignishandler einen aufzurufenden- `ComputeFibonacci` Methode hinzu. Verwenden Sie den ersten Parameter für `ComputeFibonacci` aus der- <xref:System.ComponentModel.DoWorkEventArgs.Argument%2A> Eigenschaft der <xref:System.ComponentModel.DoWorkEventArgs> . Der <xref:System.ComponentModel.BackgroundWorker> -Parameter und der- <xref:System.ComponentModel.DoWorkEventArgs> Parameter werden später für die Fortschritts Berichterstattung und Abbruch Unterstützung verwendet. Weisen Sie der-Eigenschaft des den Rückgabewert von `ComputeFibonacci` zu <xref:System.ComponentModel.DoWorkEventArgs.Result%2A> <xref:System.ComponentModel.DoWorkEventArgs> . Dieses Ergebnis steht dem- <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> Ereignishandler zur Verfügung.

    > [!NOTE]
    > Der <xref:System.ComponentModel.BackgroundWorker.DoWork> Ereignishandler verweist nicht `backgroundWorker1` direkt auf die Instanzvariable, da dieser Ereignishandler mit einer bestimmten Instanz von verknüpfen würde <xref:System.ComponentModel.BackgroundWorker> . Stattdessen wird ein Verweis auf den, der <xref:System.ComponentModel.BackgroundWorker> Dieses Ereignis ausgelöst hat, aus dem-Parameter wieder hergestellt `sender` . Dies ist wichtig, wenn das Formular mehrere Hosts hostet <xref:System.ComponentModel.BackgroundWorker> . Es ist auch wichtig, keine Benutzeroberflächen Objekte in Ihrem <xref:System.ComponentModel.BackgroundWorker.DoWork> Ereignishandler zu bearbeiten. Kommunizieren Sie stattdessen über die-Ereignisse mit der Benutzeroberfläche <xref:System.ComponentModel.BackgroundWorker> .

     [!code-cpp[System.ComponentModel.BackgroundWorker#5](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#5)]
     [!code-csharp[System.ComponentModel.BackgroundWorker#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#5)]
     [!code-vb[System.ComponentModel.BackgroundWorker#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#5)]

4. `startAsyncButton`Fügen Sie im- <xref:System.Windows.Forms.Control.Click> Ereignishandler des Steuer Elements den Code hinzu, der den asynchronen Vorgang startet.

     [!code-cpp[System.ComponentModel.BackgroundWorker#13](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#13)]
     [!code-csharp[System.ComponentModel.BackgroundWorker#13](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#13)]
     [!code-vb[System.ComponentModel.BackgroundWorker#13](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#13)]

5. <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted>Weisen Sie im-Ereignishandler das Ergebnis der Berechnung dem-Steuerelement zu `resultLabel` .

     [!code-cpp[System.ComponentModel.BackgroundWorker#6](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#6)]
     [!code-csharp[System.ComponentModel.BackgroundWorker#6](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#6)]
     [!code-vb[System.ComponentModel.BackgroundWorker#6](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#6)]

## <a name="adding-progress-reporting-and-support-for-cancellation"></a>Hinzufügen von Statusberichterstellung und Abbruchunterstützung

Bei asynchronen Vorgängen, die viel Zeit in Anspruch nehmen, ist es oft ratsam, dem Benutzer den Fortschritt zu berichten und die Möglichkeit zu geben, den Vorgang abzubrechen. Die- <xref:System.ComponentModel.BackgroundWorker> Klasse stellt ein Ereignis bereit, das es Ihnen ermöglicht, den Fortschritt während des Vorgangs im Hintergrund zu veröffentlichen. Außerdem wird ein Flag bereitgestellt, mit dem Ihr Workercode einen-Rückruf erkennen <xref:System.ComponentModel.BackgroundWorker.CancelAsync%2A> und selbst unterbrechen kann.

### <a name="implement-progress-reporting"></a>Implementieren der Fortschritts Berichterstattung

1. Wählen Sie im Fenster **Eigenschaften**`backgroundWorker1` aus. Legen Sie für die Eigenschaften <xref:System.ComponentModel.BackgroundWorker.WorkerReportsProgress%2A> (Breite) und <xref:System.ComponentModel.BackgroundWorker.WorkerSupportsCancellation%2A> (Höhe) den Wert `true` fest.

2. Deklarieren Sie zwei Variablen im Formular `FibonacciCalculator`. Diese werden verwendet, um den Fortschritt nachzuverfolgen.

     [!code-cpp[System.ComponentModel.BackgroundWorker#14](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#14)]
     [!code-csharp[System.ComponentModel.BackgroundWorker#14](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#14)]
     [!code-vb[System.ComponentModel.BackgroundWorker#14](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#14)]

3. Fügen Sie einen Ereignishandler für das <xref:System.ComponentModel.BackgroundWorker.ProgressChanged>-Ereignis hinzu. Aktualisieren Sie im- <xref:System.ComponentModel.BackgroundWorker.ProgressChanged> Ereignishandler <xref:System.Windows.Forms.ProgressBar> mit der- <xref:System.ComponentModel.ProgressChangedEventArgs.ProgressPercentage%2A> Eigenschaft des- <xref:System.ComponentModel.ProgressChangedEventArgs> Parameters.

     [!code-cpp[System.ComponentModel.BackgroundWorker#7](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#7)]
     [!code-csharp[System.ComponentModel.BackgroundWorker#7](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#7)]
     [!code-vb[System.ComponentModel.BackgroundWorker#7](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#7)]

### <a name="implement-support-for-cancellation"></a>Unterstützung für Abbruch implementieren

1. `cancelAsyncButton`Fügen Sie im- <xref:System.Windows.Forms.Control.Click> Ereignishandler des Steuer Elements den Code hinzu, der den asynchronen Vorgang abbricht.

     [!code-cpp[System.ComponentModel.BackgroundWorker#4](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#4)]
     [!code-csharp[System.ComponentModel.BackgroundWorker#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#4)]
     [!code-vb[System.ComponentModel.BackgroundWorker#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#4)]

2. Die folgenden Codefragmente in der Methode `ComputeFibonacci` berichten Fortschritt und Abbruchunterstützung.

     [!code-cpp[System.ComponentModel.BackgroundWorker#11](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#11)]
     [!code-csharp[System.ComponentModel.BackgroundWorker#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#11)]
     [!code-vb[System.ComponentModel.BackgroundWorker#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#11)]
    [!code-cpp[System.ComponentModel.BackgroundWorker#12](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#12)]
    [!code-csharp[System.ComponentModel.BackgroundWorker#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#12)]
    [!code-vb[System.ComponentModel.BackgroundWorker#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#12)]

## <a name="checkpoint"></a>Prüfpunkt

An diesem Punkt können Sie die Anwendung Fibonacci Calculator kompilieren.

Drücken Sie **F5** , um die Anwendung zu kompilieren und auszuführen.

Während die Berechnung im Hintergrund ausgeführt wird, sehen Sie, dass der <xref:System.Windows.Forms.ProgressBar> Fortschritt der Berechnung bis zur Fertigstellung angezeigt wird. Sie können auch ausstehenden Vorgang auch abbrechen.

Bei kleinen Zahlen sollte die Berechnung sehr schnell sein, aber bei größeren Zahlen sollten Sie eine merkliche Verzögerung feststellen. Wenn Sie einen Wert von 30 oder höher eingeben, sollten Sie, abhängig von Ihrem Computer, eine Verzögerung von mehreren Sekunden feststellen. Bei Werten, die höher als 40 sind, kann es Minuten oder Stunden dauern, die Berechnung abzuschließen. Beachten Sie, dass Sie das Formular frei verschieben, minimieren, maximieren und sogar schließen, während der Rechner eine hohe Fibonacci-Zahl berechnet. Dies liegt daran, dass der Haupt-UI-Thread nicht wartet, bis die Berechnung abgeschlossen ist.

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie nun ein Formular implementiert haben, das eine- <xref:System.ComponentModel.BackgroundWorker> Komponente zum Ausführen einer Berechnung im Hintergrund verwendet, können Sie weitere Möglichkeiten für asynchrone Vorgänge untersuchen:

- Verwenden Sie mehrere- <xref:System.ComponentModel.BackgroundWorker> Objekte für mehrere gleichzeitige Vorgänge.

- Informationen zum Debuggen Ihrer Multithreadanwendung finden Sie unter [Vorgehensweise: Verwenden des Fensters „Threads“](/visualstudio/debugger/how-to-use-the-threads-window).

- Implementieren Sie eine eigene Komponente, die das asynchrone Programmiermodell unterstützt. Weitere Informationen finden Sie unter [Übersicht über ereignisbasierte asynchrone Muster](/dotnet/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview).

    > [!CAUTION]
    > Wenn Sie Multithreading verwenden, setzen Sie sich möglicherweise sehr ernsten und komplexen Problemen aus. Beachten Sie die Informationen unter [Empfohlene Vorgehensweise für das verwaltete Threading](/dotnet/standard/threading/managed-threading-best-practices), bevor Sie eine Projektmappe implementieren, die Multithreading verwendet.

## <a name="see-also"></a>Siehe auch

- <xref:System.ComponentModel.BackgroundWorker?displayProperty=nameWithType>
- [Verwaltetes Threading](/dotnet/standard/threading/index)
- [Empfohlene Vorgehensweise für das verwaltete Threading](/dotnet/standard/threading/managed-threading-best-practices)
- [Event-based Asynchronous Pattern Overview (Übersicht über ereignisbasierte asynchrone Muster)](/dotnet/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview)
- [How to: Implementieren eines Formulars, das eine Hintergrundoperation verwendet](how-to-implement-a-form-that-uses-a-background-operation.md)
- [Exemplarische Vorgehensweise: Ausführen eines Vorgangs im Hintergrund](walkthrough-running-an-operation-in-the-background.md)
- [BackgroundWorker-Komponente](backgroundworker-component.md)
