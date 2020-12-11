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
# <a name="how-to-download-a-file-in-the-background"></a><span data-ttu-id="5bd0a-102">Vorgehensweise: Downloaden einer Datei im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5bd0a-102">How to: Download a File in the Background</span></span>
<span data-ttu-id="5bd0a-103">Das Herunterladen von Dateien ist eine häufige Aufgabe, und es ist oft sinnvoll, diesen potenziell zeitaufwendigen Vorgang in einem separaten Thread auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-103">Downloading a file is a common task, and it is often useful to run this potentially time-consuming operation on a separate thread.</span></span> <span data-ttu-id="5bd0a-104">Mithilfe der <xref:System.ComponentModel.BackgroundWorker>-Komponente können Sie diese Aufgabe mit nur wenigen Codezeilen ausführen.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-104">Use the <xref:System.ComponentModel.BackgroundWorker> component to accomplish this task with very little code.</span></span>  
  
## <a name="example"></a><span data-ttu-id="5bd0a-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5bd0a-105">Example</span></span>  
 <span data-ttu-id="5bd0a-106">Im folgenden Codebeispiel wird die Verwendung einer <xref:System.ComponentModel.BackgroundWorker>-Komponente zum Laden einer XML-Datei über eine URL veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-106">The following code example demonstrates how to use a <xref:System.ComponentModel.BackgroundWorker> component to load an XML file from a URL.</span></span> <span data-ttu-id="5bd0a-107">Wenn der Benutzer auf die Schaltfläche **herunterladen** klickt, <xref:System.Windows.Forms.Control.Click> ruft der Ereignishandler die- <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> Methode einer <xref:System.ComponentModel.BackgroundWorker> Komponente auf, um den Downloadvorgang zu starten.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-107">When the user clicks the **Download** button, the <xref:System.Windows.Forms.Control.Click> event handler calls the <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> method of a <xref:System.ComponentModel.BackgroundWorker> component to start the download operation.</span></span> <span data-ttu-id="5bd0a-108">Während des Downloads ist die Schaltfläche deaktiviert, und nach Abschluss des Downloads wird sie wieder aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-108">The button is disabled for the duration of the download, and then enabled when the download is complete.</span></span> <span data-ttu-id="5bd0a-109">Ein <xref:System.Windows.Forms.MessageBox> zeigt den Inhalt der Datei an.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-109">A <xref:System.Windows.Forms.MessageBox> displays the contents of the file.</span></span>  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#1)]  
  
 <span data-ttu-id="5bd0a-110">**Herunterladen der Datei**</span><span class="sxs-lookup"><span data-stu-id="5bd0a-110">**Downloading the file**</span></span>  
  
 <span data-ttu-id="5bd0a-111">Die Datei wird im Arbeitsthread der <xref:System.ComponentModel.BackgroundWorker>-Komponente heruntergeladen, der den <xref:System.ComponentModel.BackgroundWorker.DoWork>-Ereignishandler ausführt.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-111">The file is downloaded on the <xref:System.ComponentModel.BackgroundWorker> component's worker thread, which runs the <xref:System.ComponentModel.BackgroundWorker.DoWork> event handler.</span></span> <span data-ttu-id="5bd0a-112">Dieser Thread startet, wenn vom Code die <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A>-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-112">This thread starts when your code calls the <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> method.</span></span>  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#3)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#3)]  
  
 <span data-ttu-id="5bd0a-113">**Warten auf die Beendigung von „BackgroundWorker“**</span><span class="sxs-lookup"><span data-stu-id="5bd0a-113">**Waiting for a BackgroundWorker to finish**</span></span>  
  
 <span data-ttu-id="5bd0a-114">Der `downloadButton_Click`-Ereignishandler veranschaulicht, wie auf den Abschluss der asynchronen Aufgabe einer <xref:System.ComponentModel.BackgroundWorker>-Komponente gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-114">The `downloadButton_Click` event handler demonstrates how to wait for a <xref:System.ComponentModel.BackgroundWorker> component to finish its asynchronous task.</span></span>  
  
 <span data-ttu-id="5bd0a-115">Wenn die Anwendung nur auf Ereignisse reagieren soll und im Hauptthread keine Vorgänge ausgeführt werden sollen, während auf den Abschluss des Hintergrundthreads gewartet wird, können Sie den Handler einfach beenden.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-115">If you only want the application to respond to events and do not want to do any work in the main thread while you wait for the background thread to complete, just exit the handler.</span></span>  
  
 <span data-ttu-id="5bd0a-116">Wenn Sie im Hauptthread weitere Schritte ausführen möchten, verwenden Sie die <xref:System.ComponentModel.BackgroundWorker.IsBusy%2A>-Eigenschaft, um zu ermitteln, ob der <xref:System.ComponentModel.BackgroundWorker>-Thread noch ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-116">If you want to continue doing work in the main thread, use the <xref:System.ComponentModel.BackgroundWorker.IsBusy%2A> property to determine whether the <xref:System.ComponentModel.BackgroundWorker> thread is still running.</span></span> <span data-ttu-id="5bd0a-117">Im Beispiel wird eine Statusanzeige aktualisiert, während der Download verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-117">In the example, a progress bar is updated while the download is processing.</span></span> <span data-ttu-id="5bd0a-118">Sie müssen die <xref:System.Windows.Forms.Application.DoEvents%2A?displayProperty=nameWithType>-Methode aufrufen, damit die Benutzeroberfläche weiterhin auf Aktionen reagiert.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-118">Be sure to call the <xref:System.Windows.Forms.Application.DoEvents%2A?displayProperty=nameWithType> method to keep the UI responsive.</span></span>  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#2)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#2)]  
  
 <span data-ttu-id="5bd0a-119">**Anzeigen des Ergebnisses**</span><span class="sxs-lookup"><span data-stu-id="5bd0a-119">**Displaying the result**</span></span>  
  
 <span data-ttu-id="5bd0a-120">Die `backgroundWorker1_RunWorkerCompleted`-Methode behandelt das <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted>-Ereignis und wird aufgerufen, wenn der Hintergrundvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-120">The `backgroundWorker1_RunWorkerCompleted` method handles the <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> event and is called when the background operation is completed.</span></span> <span data-ttu-id="5bd0a-121">Diese Methode überprüft zuerst die <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType>-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-121">This method first checks the <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType> property.</span></span> <span data-ttu-id="5bd0a-122">Wenn <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType> den Wert `null` aufweist, zeigt die Methode den Inhalt der Datei an.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-122">If <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType> is `null`, then this method displays the contents of the file.</span></span> <span data-ttu-id="5bd0a-123">Anschließend wird die Schaltfläche "Herunterladen" wieder aktiviert, die zu Beginn des Downloads deaktiviert wurde, und die Statusanzeige wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-123">It then enables the download button, which was disabled when the download began, and it resets the progress bar.</span></span>  
  
 [!code-csharp[System.ComponentModel.BackgroundWorker.IsBusy#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/CS/Form1.cs#4)]
 [!code-vb[System.ComponentModel.BackgroundWorker.IsBusy#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker.IsBusy/VB/Form1.vb#4)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="5bd0a-124">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="5bd0a-124">Compiling the Code</span></span>  
 <span data-ttu-id="5bd0a-125">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5bd0a-125">This example requires:</span></span>  
  
- <span data-ttu-id="5bd0a-126">Verweise auf die Assemblys "System.Drawing", "System.Windows.Forms" und "System.XML".</span><span class="sxs-lookup"><span data-stu-id="5bd0a-126">References to the System.Drawing, System.Windows.Forms, and System.Xml assemblies.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="5bd0a-127">Stabile Programmierung</span><span class="sxs-lookup"><span data-stu-id="5bd0a-127">Robust Programming</span></span>  
 <span data-ttu-id="5bd0a-128">Überprüfen Sie immer die <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType>-Eigenschaft im <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted>-Ereignishandler, bevor Sie auf die <xref:System.ComponentModel.RunWorkerCompletedEventArgs.Result%2A?displayProperty=nameWithType>-Eigenschaft oder auf ein anderes Objekt zugreifen, auf das der <xref:System.ComponentModel.BackgroundWorker.DoWork>-Ereignishandler Einfluss haben kann.</span><span class="sxs-lookup"><span data-stu-id="5bd0a-128">Always check the <xref:System.ComponentModel.AsyncCompletedEventArgs.Error%2A?displayProperty=nameWithType> property in your <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> event handler before attempting to access the <xref:System.ComponentModel.RunWorkerCompletedEventArgs.Result%2A?displayProperty=nameWithType> property or any other object that may have been affected by the <xref:System.ComponentModel.BackgroundWorker.DoWork> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="5bd0a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bd0a-129">See also</span></span>

- <xref:System.ComponentModel.BackgroundWorker>
- [<span data-ttu-id="5bd0a-130">How to: Ausführen eines Vorgangs im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="5bd0a-130">How to: Run an Operation in the Background</span></span>](how-to-run-an-operation-in-the-background.md)
- [<span data-ttu-id="5bd0a-131">How to: Implementieren eines Formulars, das eine Hintergrundoperation verwendet</span><span class="sxs-lookup"><span data-stu-id="5bd0a-131">How to: Implement a Form That Uses a Background Operation</span></span>](how-to-implement-a-form-that-uses-a-background-operation.md)
