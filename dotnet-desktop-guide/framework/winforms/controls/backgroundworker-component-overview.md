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
# <a name="backgroundworker-component-overview"></a>Übersicht über die BackgroundWorker-Komponente

Es gibt viele häufig verwendete Operationen, deren Ausführung lange dauern kann. Beispiel:  
  
- Bilddownloads  
  
- Webdienstaufrufe  
  
- Dateidownloads und -uploads (einschließlich für Peer-to-Peer-Anwendungen)  
  
- Komplexe lokale Berechnungen  
  
- Datenbanktransaktionen  
  
- Lokaler Festplattenzugriff, angesichts der langsamen Geschwindigkeit relativ zum Arbeitsspeicherzugriff  
  
 Vorgänge wie diese können dazu führen, dass Ihre Benutzeroberfläche blockiert wird, während Sie ausgeführt werden. Wenn Sie dies vermeiden möchten und bei solchen Operationen lange Verzögerungen auftreten, stellt die <xref:System.ComponentModel.BackgroundWorker>-Komponente eine geeignete Alternative dar.  
  
 Die <xref:System.ComponentModel.BackgroundWorker>-Komponente ermöglicht es Ihnen, zeitaufwändige Operationen asynchron ("im Hintergrund") auf einem anderen Thread als dem primären UI-Thread der Anwendung auszuführen. Um einen <xref:System.ComponentModel.BackgroundWorker> zu verwenden, müssen Sie lediglich festlegen, welche zeitaufwändige Workermethode im Hintergrund ausgeführt werden soll, und anschließend die <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A>-Methode aufrufen. Der aufrufende Thread wird weiterhin wie gewohnt ausgeführt, während die Workermethode asynchron ausgeführt wird. Nach Abschluss der Methode gibt der <xref:System.ComponentModel.BackgroundWorker> eine Warnung an den aufrufenden Thread aus, indem er das <xref:System.ComponentModel.BackgroundWorker.RunWorkerCompleted>-Ereignis auslöst, das optional die Ergebnisse der Operation enthält.  
  
 Die <xref:System.ComponentModel.BackgroundWorker> Komponente ist über die **Toolbox** auf der Registerkarte **Komponenten** verfügbar. Um dem Formular eine hinzuzufügen <xref:System.ComponentModel.BackgroundWorker> , ziehen Sie die <xref:System.ComponentModel.BackgroundWorker> Komponente auf das Formular. Er wird in der Komponenten Leiste angezeigt, und seine Eigenschaften werden im Fenster **Eigenschaften** angezeigt.  
  
 Um die asynchrone Operation zu starten, verwenden Sie die <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A>-Methode. <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> nimmt einen optionalen- `object` Parameter an, der verwendet werden kann, um Argumente an die Worker-Methode zu übergeben. Die <xref:System.ComponentModel.BackgroundWorker>-Klasse macht das <xref:System.ComponentModel.BackgroundWorker.DoWork>-Ereignis verfügbar, mit dem der Workerthread über einen <xref:System.ComponentModel.BackgroundWorker.DoWork>-Ereignishandler verbunden ist.  
  
 Der <xref:System.ComponentModel.BackgroundWorker.DoWork>-Ereignishandler verwendet einen <xref:System.ComponentModel.DoWorkEventArgs>-Parameter, der über eine <xref:System.ComponentModel.DoWorkEventArgs.Argument%2A>-Eigenschaft verfügt. Diese Eigenschaft empfängt den Parameter von <xref:System.ComponentModel.BackgroundWorker.RunWorkerAsync%2A> und kann an die Workermethode übergeben werden, die im <xref:System.ComponentModel.BackgroundWorker.DoWork>-Ereignishandler aufgerufen wird. Im folgenden Beispiel wird gezeigt, wie ein Ergebnis von einer Workermethode mit dem Namen `ComputeFibonacci` zugewiesen wird. Es ist Teil eines größeren Beispiels, das Sie unter Gewusst [wie: Implementieren eines Formulars finden, das einen Hintergrund Vorgang verwendet](how-to-implement-a-form-that-uses-a-background-operation.md).  
  
 [!code-cpp[System.ComponentModel.BackgroundWorker#5](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#5)]
 [!code-csharp[System.ComponentModel.BackgroundWorker#5](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#5)]
 [!code-vb[System.ComponentModel.BackgroundWorker#5](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#5)]  
  
 Weitere Informationen zur Verwendung von Ereignis Handlern finden Sie unter [Ereignisse](/dotnet/standard/events/index).  
  
> [!CAUTION]
> Wenn Sie Multithreading verwenden, setzen Sie sich möglicherweise sehr ernsten und komplexen Problemen aus. Beachten Sie die Informationen unter [Empfohlene Vorgehensweise für das verwaltete Threading](/dotnet/standard/threading/managed-threading-best-practices), bevor Sie eine Projektmappe implementieren, die Multithreading verwendet.  
  
 Weitere Informationen zur Verwendung der- <xref:System.ComponentModel.BackgroundWorker> Klasse finden Sie unter Gewusst [wie: Ausführen eines Vorgangs im Hintergrund](how-to-run-an-operation-in-the-background.md).  
  
## <a name="see-also"></a>Siehe auch

- [Verwaltetes Threading](/dotnet/standard/threading/index)
- [Event-based Asynchronous Pattern Overview (Übersicht über ereignisbasierte asynchrone Muster)](/dotnet/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview)
- [How to: Implementieren eines Formulars, das eine Hintergrundoperation verwendet](how-to-implement-a-form-that-uses-a-background-operation.md)
