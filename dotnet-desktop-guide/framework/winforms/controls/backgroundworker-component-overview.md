---
title: Übersicht über die BackgroundWorker-Komponente
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- BackgroundWorker
helpviewer_keywords:
- BackgroundWorker component
- background tasks
- Asynchronous Pattern
- forms [Windows Forms], multithreading
- components [Windows Forms], asynchronous
- forms [Windows Forms], background operations
- threading [Windows Forms], background operations
- background operations
ms.assetid: 64e9b3ab-7443-4a77-ab17-b8b8c0cb3f62
ms.openlocfilehash: ba197331863b1b6dd49fbb26249bfd4a46106e34
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975786"
---
# <a name="backgroundworker-component-overview"></a><span data-ttu-id="cb298-102">Übersicht über die BackgroundWorker-Komponente</span><span class="sxs-lookup"><span data-stu-id="cb298-102">BackgroundWorker Component Overview</span></span>

<span data-ttu-id="cb298-103">Es gibt viele häufig verwendete Operationen, deren Ausführung lange dauern kann.</span><span class="sxs-lookup"><span data-stu-id="cb298-103">There are many commonly performed operations that can take a long time to execute.</span></span> <span data-ttu-id="cb298-104">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cb298-104">For example:</span></span>  
  
- <span data-ttu-id="cb298-105">Bilddownloads</span><span class="sxs-lookup"><span data-stu-id="cb298-105">Image downloads</span></span>  
  
- <span data-ttu-id="cb298-106">Webdienstaufrufe</span><span class="sxs-lookup"><span data-stu-id="cb298-106">Web service invocations</span></span>  
  
- <span data-ttu-id="cb298-107">Dateidownloads und -uploads (einschließlich für Peer-to-Peer-Anwendungen)</span><span class="sxs-lookup"><span data-stu-id="cb298-107">File downloads and uploads (including for peer-to-peer applications)</span></span>  
  
- <span data-ttu-id="cb298-108">Komplexe lokale Berechnungen</span><span class="sxs-lookup"><span data-stu-id="cb298-108">Complex local computations</span></span>  
  
- <span data-ttu-id="cb298-109">Datenbanktransaktionen</span><span class="sxs-lookup"><span data-stu-id="cb298-109">Database transactions</span></span>  
  
- <span data-ttu-id="cb298-110">Lokaler Festplattenzugriff, angesichts der langsamen Geschwindigkeit relativ zum Arbeitsspeicherzugriff</span><span class="sxs-lookup"><span data-stu-id="cb298-110">Local disk access, given its slow speed relative to memory access</span></span>  
  
 <span data-ttu-id="cb298-111">Vorgänge wie diese können dazu führen, dass Ihre Benutzeroberfläche blockiert wird, während Sie ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cb298-111">Operations like these can cause your user interface to block while they are running.</span></span> <span data-ttu-id="cb298-112">Wenn Sie dies vermeiden möchten und bei solchen Operationen lange Verzögerungen auftreten, stellt die <xref:System.ComponentModel.BackgroundWorker>-Komponente eine geeignete Alternative dar.</span><span class="sxs-lookup"><span data-stu-id="cb298-112">When you want a responsive UI and you are faced with long delays associated with such operations, the <xref:System.ComponentModel.BackgroundWorker> component provides a convenient solution.</span></span>  
  
 <span data-ttu-id="cb298-113">Die <xref:System.ComponentModel.BackgroundWorker>-Komponente ermöglicht es Ihnen, zeitaufwändige Operationen asynchron ("im Hintergrund") auf einem anderen Thread als dem primären UI-Thread der Anwendung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="cb298-113">The <xref:System.ComponentModel.BackgroundWorker> component gives you the ability to execute time-consuming operations asynchronously ("in the background"), on a thread different from your application's main UI thread.</span></span> <span data-ttu-id="cb298-114">Um einen <xref:System.ComponentModel.BackgroundWorker> zu verwenden, müssen Sie lediglich festlegen, welche zeitaufwändige Workermethode im Hintergrund ausgeführt werden soll, und anschließend die <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A>-Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cb298-114">To use a <xref:System.ComponentModel.BackgroundWorker>, you simply tell it what time-consuming worker method to execute in the background, and then you call the <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> method.</span></span> <span data-ttu-id="cb298-115">Der aufrufende Thread wird weiterhin wie gewohnt ausgeführt, während die Workermethode asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cb298-115">Your calling thread continues to run normally while the worker method runs asynchronously.</span></span> <span data-ttu-id="cb298-116">Nach Abschluss der Methode gibt der <xref:System.ComponentModel.BackgroundWorker> eine Warnung an den aufrufenden Thread aus, indem er das <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted>-Ereignis auslöst, das optional die Ergebnisse der Operation enthält.</span><span class="sxs-lookup"><span data-stu-id="cb298-116">When the method is finished, the <xref:System.ComponentModel.BackgroundWorker> alerts the calling thread by firing the <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted> event, which optionally contains the results of the operation.</span></span>  
  
 <span data-ttu-id="cb298-117">Die <xref:System.ComponentModel.BackgroundWorker> Komponente ist über die **Toolbox** auf der Registerkarte **Komponenten** verfügbar. Um dem Formular eine hinzuzufügen <xref:System.ComponentModel.BackgroundWorker> , ziehen Sie die <xref:System.ComponentModel.BackgroundWorker> Komponente auf das Formular.</span><span class="sxs-lookup"><span data-stu-id="cb298-117">The <xref:System.ComponentModel.BackgroundWorker> component is available from the **Toolbox**, in the **Components** tab. To add a <xref:System.ComponentModel.BackgroundWorker> to your form, drag the <xref:System.ComponentModel.BackgroundWorker> component onto your form.</span></span> <span data-ttu-id="cb298-118">Er wird in der Komponenten Leiste angezeigt, und seine Eigenschaften werden im Fenster **Eigenschaften** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cb298-118">It appears in the component tray, and its properties appear in the **Properties** window.</span></span>  
  
 <span data-ttu-id="cb298-119">Um die asynchrone Operation zu starten, verwenden Sie die <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A>-Methode.</span><span class="sxs-lookup"><span data-stu-id="cb298-119">To start your asynchronous operation, use the <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> method.</span></span> <span data-ttu-id="cb298-120"><xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> nimmt einen optionalen- `object` Parameter an, der verwendet werden kann, um Argumente an die Worker-Methode zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="cb298-120"><xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> takes an optional `object` parameter, which can be used to pass arguments to your worker method.</span></span> <span data-ttu-id="cb298-121">Die <xref:System.ComponentModel.BackgroundWorker>-Klasse macht das <xref:System.ComponentModel.BackgroundWorker.DoWork>-Ereignis verfügbar, mit dem der Workerthread über einen <xref:System.ComponentModel.BackgroundWorker.DoWork>-Ereignishandler verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="cb298-121">The <xref:System.ComponentModel.BackgroundWorker> class exposes the <xref:System.ComponentModel.BackgroundWorker.DoWork> event, to which your worker thread is attached through a <xref:System.ComponentModel.BackgroundWorker.DoWork> event handler.</span></span>  
  
 <span data-ttu-id="cb298-122">Der <xref:System.ComponentModel.BackgroundWorker.DoWork>-Ereignishandler verwendet einen <xref:System.ComponentModel.DoWorkEventArgs>-Parameter, der über eine <xref:System.ComponentModel.DoWorkEventArgs.Argument%2A>-Eigenschaft verfügt.</span><span class="sxs-lookup"><span data-stu-id="cb298-122">The <xref:System.ComponentModel.BackgroundWorker.DoWork> event handler takes a <xref:System.ComponentModel.DoWorkEventArgs> parameter, which has an <xref:System.ComponentModel.DoWorkEventArgs.Argument%2A> property.</span></span> <span data-ttu-id="cb298-123">Diese Eigenschaft empfängt den Parameter von <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> und kann an die Workermethode übergeben werden, die im <xref:System.ComponentModel.BackgroundWorker.DoWork>-Ereignishandler aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cb298-123">This property receives the parameter from <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> and can be passed to your worker method, which will be called in the <xref:System.ComponentModel.BackgroundWorker.DoWork> event handler.</span></span> <span data-ttu-id="cb298-124">Im folgenden Beispiel wird gezeigt, wie ein Ergebnis von einer Workermethode mit dem Namen `ComputeFibonacci` zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cb298-124">The following example shows how to assign a result from a worker method called `ComputeFibonacci`.</span></span> <span data-ttu-id="cb298-125">Es ist Teil eines größeren Beispiels, das Sie unter Gewusst [wie: Implementieren eines Formulars finden, das einen Hintergrund Vorgang verwendet](how-to-implement-a-form-that-uses-a-background-operation.md).</span><span class="sxs-lookup"><span data-stu-id="cb298-125">It is part of a larger example, which you can find at [How to: Implement a Form That Uses a Background Operation](how-to-implement-a-form-that-uses-a-background-operation.md).</span></span>  
  
 [!code-cpp[System.ComponentModel.BackgroundWorker#5](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#5)]
 [!code-csharp[System.ComponentModel.BackgroundWorker#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#5)]
 [!code-vb[System.ComponentModel.BackgroundWorker#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#5)]  
  
 <span data-ttu-id="cb298-126">Weitere Informationen zur Verwendung von Ereignis Handlern finden Sie unter [Ereignisse](/dotnet/standard/events/index).</span><span class="sxs-lookup"><span data-stu-id="cb298-126">For more information on using event handlers, see [Events](/dotnet/standard/events/index).</span></span>  
  
> [!CAUTION]
> <span data-ttu-id="cb298-127">Wenn Sie Multithreading verwenden, setzen Sie sich möglicherweise sehr ernsten und komplexen Problemen aus.</span><span class="sxs-lookup"><span data-stu-id="cb298-127">When using multithreading of any sort, you potentially expose yourself to very serious and complex bugs.</span></span> <span data-ttu-id="cb298-128">Beachten Sie die Informationen unter [Empfohlene Vorgehensweise für das verwaltete Threading](/dotnet/standard/threading/managed-threading-best-practices), bevor Sie eine Projektmappe implementieren, die Multithreading verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb298-128">Consult the [Managed Threading Best Practices](/dotnet/standard/threading/managed-threading-best-practices) before implementing any solution that uses multithreading.</span></span>  
  
 <span data-ttu-id="cb298-129">Weitere Informationen zur Verwendung der- <xref:System.ComponentModel.BackgroundWorker> Klasse finden Sie unter Gewusst [wie: Ausführen eines Vorgangs im Hintergrund](how-to-run-an-operation-in-the-background.md).</span><span class="sxs-lookup"><span data-stu-id="cb298-129">For more information on using the <xref:System.ComponentModel.BackgroundWorker> class, see [How to: Run an Operation in the Background](how-to-run-an-operation-in-the-background.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="cb298-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb298-130">See also</span></span>

- [<span data-ttu-id="cb298-131">Verwaltetes Threading</span><span class="sxs-lookup"><span data-stu-id="cb298-131">Managed Threading</span></span>](/dotnet/standard/threading/index)
- [<span data-ttu-id="cb298-132">Event-based Asynchronous Pattern Overview (Übersicht über ereignisbasierte asynchrone Muster)</span><span class="sxs-lookup"><span data-stu-id="cb298-132">Event-based Asynchronous Pattern Overview</span></span>](/dotnet/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview)
- [<span data-ttu-id="cb298-133">How to: Implementieren eines Formulars, das eine Hintergrundoperation verwendet</span><span class="sxs-lookup"><span data-stu-id="cb298-133">How to: Implement a Form That Uses a Background Operation</span></span>](how-to-implement-a-form-that-uses-a-background-operation.md)
