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
# <a name="walkthrough-running-an-operation-in-the-background"></a><span data-ttu-id="5867b-102">Exemplarische Vorgehensweise: Ausführen eines Vorgangs im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5867b-102">Walkthrough: Running an Operation in the Background</span></span>

<span data-ttu-id="5867b-103">Gibt es einen Vorgang, der bis zu seinem Abschluss eine lange Zeit in Anspruch nimmt, und Sie möchten keine Verzögerungen in der Benutzeroberfläche verursachen, können Sie die <xref:System.ComponentModel.BackgroundWorker>-Klasse dazu verwenden, den Vorgang über einen anderen Thread auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5867b-103">If you have an operation that will take a long time to complete, and you do not want to cause delays in your user interface, you can use the <xref:System.ComponentModel.BackgroundWorker> class to run the operation on another thread.</span></span>

<span data-ttu-id="5867b-104">Eine umfassende Liste des in diesem Beispiel verwendeten Codes finden Sie unter Gewusst [wie: Ausführen eines Vorgangs im Hintergrund](how-to-run-an-operation-in-the-background.md).</span><span class="sxs-lookup"><span data-stu-id="5867b-104">For a complete listing of the code used in this example, see [How to: Run an Operation in the Background](how-to-run-an-operation-in-the-background.md).</span></span>

## <a name="run-an-operation-in-the-background"></a><span data-ttu-id="5867b-105">Ausführen eines Vorgangs im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5867b-105">Run an operation in the background</span></span>

1. <span data-ttu-id="5867b-106">Wenn das Formular in der Windows Forms-Designer in Visual Studio aktiv ist, ziehen Sie zwei-Steuer <xref:System.Windows.Forms.Button> Elemente aus der **Toolbox** auf das Formular, und legen Sie dann die `Name` -Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.Control.Text%2A> der Schaltflächen entsprechend der folgenden Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="5867b-106">With your form active in the Windows Forms Designer in Visual Studio, drag two <xref:System.Windows.Forms.Button> controls from the **Toolbox** to the form, and then set the `Name` and <xref:System.Windows.Forms.Control.Text%2A> properties of the buttons according to the following table.</span></span>

    |<span data-ttu-id="5867b-107">Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="5867b-107">Button</span></span>|<span data-ttu-id="5867b-108">Name</span><span class="sxs-lookup"><span data-stu-id="5867b-108">Name</span></span>|<span data-ttu-id="5867b-109">Text</span><span class="sxs-lookup"><span data-stu-id="5867b-109">Text</span></span>|
    |------------|----------|----------|
    |`button1`|`startBtn`|<span data-ttu-id="5867b-110">**Starten**</span><span class="sxs-lookup"><span data-stu-id="5867b-110">**Start**</span></span>|
    |`button2`|`cancelBtn`|<span data-ttu-id="5867b-111">**Kündigen**</span><span class="sxs-lookup"><span data-stu-id="5867b-111">**Cancel**</span></span>|

2. <span data-ttu-id="5867b-112">Öffnen Sie die **Toolbox**, klicken Sie auf die Registerkarte **Komponenten** , und ziehen Sie die <xref:System.ComponentModel.BackgroundWorker> Komponente auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="5867b-112">Open the **Toolbox**, click the **Components** tab, and then drag the <xref:System.ComponentModel.BackgroundWorker> component onto your form.</span></span>

     <span data-ttu-id="5867b-113">Die `backgroundWorker1` Komponente wird in der **Komponenten Leiste** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5867b-113">The `backgroundWorker1` component appears in the **Component Tray**.</span></span>

3. <span data-ttu-id="5867b-114">Legen Sie im Fenster **Eigenschaften** die Eigenschaft <xref:System.ComponentModel.BackgroundWorker.WorkerSupportsCancellation%2A> auf `true`fest.</span><span class="sxs-lookup"><span data-stu-id="5867b-114">In the **Properties** window, set the <xref:System.ComponentModel.BackgroundWorker.WorkerSupportsCancellation%2A> property to `true`.</span></span>

4. <span data-ttu-id="5867b-115">Klicken Sie im Fenster **Eigenschaften** auf die Schaltfläche **Ereignisse** , und doppelklicken Sie dann <xref:System.ComponentModel.BackgroundWorker.DoWork> auf das-Ereignis und das-Ereignis, <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> um Ereignishandler zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5867b-115">In the **Properties** window, click on the **Events** button, and then double-click the <xref:System.ComponentModel.BackgroundWorker.DoWork> and <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> events to create event handlers.</span></span>

5. <span data-ttu-id="5867b-116">Fügen Sie den zeitaufwändigen Code in den- <xref:System.ComponentModel.BackgroundWorker.DoWork> Ereignishandler ein.</span><span class="sxs-lookup"><span data-stu-id="5867b-116">Insert your time-consuming code into the <xref:System.ComponentModel.BackgroundWorker.DoWork> event handler.</span></span>

6. <span data-ttu-id="5867b-117">Extrahieren Sie alle Parameter, die für den Vorgang erforderlich sind, aus der- <xref:System.ComponentModel.DoWorkEventArgs.Argument%2A> Eigenschaft des <xref:System.ComponentModel.DoWorkEventArgs> Parameters.</span><span class="sxs-lookup"><span data-stu-id="5867b-117">Extract any parameters required by the operation from the <xref:System.ComponentModel.DoWorkEventArgs.Argument%2A> property of the <xref:System.ComponentModel.DoWorkEventArgs> parameter.</span></span>

7. <span data-ttu-id="5867b-118">Weisen Sie das Ergebnis der Berechnung der- <xref:System.ComponentModel.DoWorkEventArgs.Result%2A> Eigenschaft von zu <xref:System.ComponentModel.DoWorkEventArgs> .</span><span class="sxs-lookup"><span data-stu-id="5867b-118">Assign the result of the computation to the <xref:System.ComponentModel.DoWorkEventArgs.Result%2A> property of the <xref:System.ComponentModel.DoWorkEventArgs>.</span></span>

     <span data-ttu-id="5867b-119">Diese ist für den- <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> Ereignishandler verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5867b-119">This is will be available to the <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> event handler.</span></span>

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#2)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#2)]

8. <span data-ttu-id="5867b-120">Fügen Sie Code zum Abrufen des Ergebnisses des Vorgangs im- <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> Ereignishandler ein.</span><span class="sxs-lookup"><span data-stu-id="5867b-120">Insert code for retrieving the result of your operation in the <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> event handler.</span></span>

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#3)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#3)]

9. <span data-ttu-id="5867b-121">Implementieren Sie die `TimeConsumingOperation`-Methode.</span><span class="sxs-lookup"><span data-stu-id="5867b-121">Implement the `TimeConsumingOperation` method.</span></span>

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#4)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#4)]

10. <span data-ttu-id="5867b-122">Doppelklicken Sie in der Windows Forms-Designer `startButton` auf, um den <xref:System.Windows.Forms.Control.Click> Ereignishandler zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5867b-122">In the Windows Forms Designer, double-click `startButton` to create the <xref:System.Windows.Forms.Control.Click> event handler.</span></span>

11. <span data-ttu-id="5867b-123">Die- <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> Methode wird im- <xref:System.Windows.Forms.Control.Click> Ereignishandler für aufgerufen `startButton` .</span><span class="sxs-lookup"><span data-stu-id="5867b-123">Call the <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> method in the <xref:System.Windows.Forms.Control.Click> event handler for `startButton`.</span></span>

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#5)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#5)]

12. <span data-ttu-id="5867b-124">Doppelklicken Sie in der Windows Forms-Designer `cancelButton` auf, um den <xref:System.Windows.Forms.Control.Click> Ereignishandler zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5867b-124">In the Windows Forms Designer, double-click `cancelButton` to create the <xref:System.Windows.Forms.Control.Click> event handler.</span></span>

13. <span data-ttu-id="5867b-125">Die- <xref:System.ComponentModel.BackgroundWorker.CancelAsync%2A> Methode wird im- <xref:System.Windows.Forms.Control.Click> Ereignishandler für aufgerufen `cancelButton` .</span><span class="sxs-lookup"><span data-stu-id="5867b-125">Call the <xref:System.ComponentModel.BackgroundWorker.CancelAsync%2A> method in the <xref:System.Windows.Forms.Control.Click> event handler for `cancelButton`.</span></span>

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#6](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#6)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#6](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#6)]

14. <span data-ttu-id="5867b-126">Importieren Sie am Anfang der Datei die Namespaces System. ComponentModel und System. Threading.</span><span class="sxs-lookup"><span data-stu-id="5867b-126">At the top of the file, import the System.ComponentModel and System.Threading namespaces.</span></span>

     [!code-csharp[System.ComponentModel.BackgroundWorker.Example#7](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/CS/Form1.cs#7)]
     [!code-vb[System.ComponentModel.BackgroundWorker.Example#7](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.Example/VB/Form1.vb#7)]

15. <span data-ttu-id="5867b-127">Drücken Sie **F6** , um die Projekt Mappe zu erstellen, und drücken Sie dann **STRG** + **F5** , um die Anwendung außerhalb des Debuggers auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5867b-127">Press **F6** to build the solution, and then press **Ctrl**+**F5** to run the application outside the debugger.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5867b-128">Wenn Sie **F5** drücken, um die Anwendung unter dem Debugger auszuführen, wird die in der Methode ausgelöste Ausnahme abgefangen `TimeConsumingOperation` und vom Debugger angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5867b-128">If you press **F5** to run the application under the debugger, the exception raised in the `TimeConsumingOperation` method is caught and displayed by the debugger.</span></span> <span data-ttu-id="5867b-129">Wenn Sie die Anwendung außerhalb des Debuggers ausführen, <xref:System.ComponentModel.BackgroundWorker> verarbeitet die Ausnahme und speichert Sie in der- <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A> Eigenschaft des-Objekts zwischen <xref:System.ComponentModel.RunWorkerCompletedEventArgs> .</span><span class="sxs-lookup"><span data-stu-id="5867b-129">When you run the application outside the debugger, the <xref:System.ComponentModel.BackgroundWorker> handles the exception and caches it in the <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A> property of the <xref:System.ComponentModel.RunWorkerCompletedEventArgs>.</span></span>

16. <span data-ttu-id="5867b-130">Klicken Sie auf die Schaltfläche **Start** , um einen asynchronen Vorgang auszuführen, und klicken Sie dann auf die Schaltfläche **Abbrechen** , um einen laufenden asynchronen Vorgang zu beenden.</span><span class="sxs-lookup"><span data-stu-id="5867b-130">Click the **Start** button to run an asynchronous operation, and then click the **Cancel** button to stop a running asynchronous operation.</span></span>

     <span data-ttu-id="5867b-131">Das Ergebnis jedes Vorgangs wird in einem <xref:System.Windows.Forms.MessageBox>-Steuerelement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5867b-131">The outcome of each operation is displayed in a <xref:System.Windows.Forms.MessageBox>.</span></span>

## <a name="next-steps"></a><span data-ttu-id="5867b-132">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="5867b-132">Next steps</span></span>

- <span data-ttu-id="5867b-133">Implementieren Sie ein Formular, das den Status meldet, wenn ein asynchroner Vorgang fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="5867b-133">Implement a form that reports progress as an asynchronous operation proceeds.</span></span> <span data-ttu-id="5867b-134">Weitere Informationen finden Sie unter Gewusst [wie: Implementieren eines Formulars, das einen Hintergrund Vorgang verwendet](how-to-implement-a-form-that-uses-a-background-operation.md).</span><span class="sxs-lookup"><span data-stu-id="5867b-134">For more information, see [How to: Implement a Form That Uses a Background Operation](how-to-implement-a-form-that-uses-a-background-operation.md).</span></span>

- <span data-ttu-id="5867b-135">Implementieren Sie eine Klasse, die das asynchrone Muster für Komponenten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5867b-135">Implement a class that supports the Asynchronous Pattern for Components.</span></span> <span data-ttu-id="5867b-136">Weitere Informationen finden Sie unter [Implementieren des ereignisbasierten asynchronen Musters](/dotnet/standard/asynchronous-programming-patterns/implementing-the-event-based-asynchronous-pattern).</span><span class="sxs-lookup"><span data-stu-id="5867b-136">For more information, see [Implementing the Event-based Asynchronous Pattern](/dotnet/standard/asynchronous-programming-patterns/implementing-the-event-based-asynchronous-pattern).</span></span>

## <a name="see-also"></a><span data-ttu-id="5867b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5867b-137">See also</span></span>

- <xref:System.ComponentModel.BackgroundWorker>
- <xref:System.ComponentModel.DoWorkEventArgs>
- [<span data-ttu-id="5867b-138">How to: Implementieren eines Formulars, das eine Hintergrundoperation verwendet</span><span class="sxs-lookup"><span data-stu-id="5867b-138">How to: Implement a Form That Uses a Background Operation</span></span>](how-to-implement-a-form-that-uses-a-background-operation.md)
- [<span data-ttu-id="5867b-139">How to: Ausführen eines Vorgangs im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5867b-139">How to: Run an Operation in the Background</span></span>](how-to-run-an-operation-in-the-background.md)
- [<span data-ttu-id="5867b-140">BackgroundWorker-Komponente</span><span class="sxs-lookup"><span data-stu-id="5867b-140">BackgroundWorker Component</span></span>](backgroundworker-component.md)
