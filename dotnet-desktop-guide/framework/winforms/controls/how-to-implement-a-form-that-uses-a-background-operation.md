---
title: 'Vorgehensweise: Implementieren eines Formulars, das eine Hintergrundoperation verwendet'
description: Erfahren Sie, wie Sie ein Windows Form implementieren, das einen Hintergrund Vorgang verwendet, damit ein Vorgang weiterhin ausgeführt werden kann, während ein anderer Vorgang ausgeführt wird.
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
- components [Windows Forms], asynchronous
- forms [Windows Forms], background operations
- background threads
- threading [Windows Forms], background operations
- background operations
ms.assetid: 9f483f93-1613-4be1-a021-b4934e9c78f3
ms.openlocfilehash: 85a583ce81c8d7e169302dd9e3e304c22977327a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976479"
---
# <a name="how-to-implement-a-form-that-uses-a-background-operation"></a><span data-ttu-id="d745d-103">Vorgehensweise: Implementieren eines Formulars, das eine Hintergrundoperation verwendet</span><span class="sxs-lookup"><span data-stu-id="d745d-103">How to: Implement a Form That Uses a Background Operation</span></span>

<span data-ttu-id="d745d-104">Mit dem folgenden Beispielprogramm wird ein Formular erstellt, das Fibonacci-Zahlen berechnet.</span><span class="sxs-lookup"><span data-stu-id="d745d-104">The following example program creates a form that calculates Fibonacci numbers.</span></span> <span data-ttu-id="d745d-105">Die Berechnung erfolgt in einem separaten (vom Thread der Benutzeroberfläche unabhängigen) Thread, sodass die Benutzeroberfläche während der Berechnung weiterhin ohne Verzögerungen ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d745d-105">The calculation runs on a thread that is separate from the user interface thread, so the user interface continues to run without delays as the calculation proceeds.</span></span>  
  
 <span data-ttu-id="d745d-106">Visual Studio bietet umfassende Unterstützung für diese Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="d745d-106">There is extensive support for this task in Visual Studio.</span></span>  
  
 <span data-ttu-id="d745d-107">Siehe auch[Exemplarische Vorgehensweise: Implementieren eines Formulars, das eine Hintergrundoperation verwendet](walkthrough-implementing-a-form-that-uses-a-background-operation.md).</span><span class="sxs-lookup"><span data-stu-id="d745d-107">Also see [Walkthrough: Implementing a Form That Uses a Background Operation](walkthrough-implementing-a-form-that-uses-a-background-operation.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="d745d-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d745d-108">Example</span></span>  

 [!code-cpp[System.ComponentModel.BackgroundWorker#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CPP/fibonacciform.cpp#1)]
 [!code-csharp[System.ComponentModel.BackgroundWorker#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/CS/fibonacciform.cs#1)]
 [!code-vb[System.ComponentModel.BackgroundWorker#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.BackgroundWorker/VB/fibonacciform.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="d745d-109">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="d745d-109">Compiling the Code</span></span>  

 <span data-ttu-id="d745d-110">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d745d-110">This example requires:</span></span>  
  
- <span data-ttu-id="d745d-111">Verweise auf die Assemblys "System", "System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="d745d-111">References to the System, System.Drawing, and System.Windows.Forms assemblies.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="d745d-112">Stabile Programmierung</span><span class="sxs-lookup"><span data-stu-id="d745d-112">Robust Programming</span></span>  
  
> [!CAUTION]
> <span data-ttu-id="d745d-113">Wenn Sie Multithreading verwenden, setzen Sie sich möglicherweise sehr ernsten und komplexen Problemen aus.</span><span class="sxs-lookup"><span data-stu-id="d745d-113">When using multithreading of any sort, you potentially expose yourself to very serious and complex bugs.</span></span> <span data-ttu-id="d745d-114">Beachten Sie die Informationen unter [Empfohlene Vorgehensweise für das verwaltete Threading](/dotnet/standard/threading/managed-threading-best-practices), bevor Sie eine Projektmappe implementieren, die Multithreading verwendet.</span><span class="sxs-lookup"><span data-stu-id="d745d-114">Consult the [Managed Threading Best Practices](/dotnet/standard/threading/managed-threading-best-practices) before implementing any solution that uses multithreading.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d745d-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d745d-115">See also</span></span>

- <xref:System.ComponentModel.BackgroundWorker>
- <xref:System.ComponentModel.DoWorkEventArgs>
- [<span data-ttu-id="d745d-116">Event-based Asynchronous Pattern Overview (Übersicht über ereignisbasierte asynchrone Muster)</span><span class="sxs-lookup"><span data-stu-id="d745d-116">Event-based Asynchronous Pattern Overview</span></span>](/dotnet/standard/asynchronous-programming-patterns/event-based-asynchronous-pattern-overview)
- [<span data-ttu-id="d745d-117">Empfohlene Vorgehensweise für das verwaltete Threading</span><span class="sxs-lookup"><span data-stu-id="d745d-117">Managed Threading Best Practices</span></span>](/dotnet/standard/threading/managed-threading-best-practices)
