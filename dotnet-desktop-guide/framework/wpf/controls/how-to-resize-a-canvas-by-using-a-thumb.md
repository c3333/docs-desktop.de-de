---
title: 'Gewusst wie: Ändern der Canvas-Größe mithilfe eines Ziehpunkts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- resizing Canvas control [WPF]
- controls [WPF], Thumb
- controls [WPF], Canvas
- Thumb control [WPF]
- Canvas control [WPF]
ms.assetid: 7dc9f435-726c-4d4d-be41-eb24cfe17bef
ms.openlocfilehash: 84f5ac2b53124b7f4d7c15741e94b40e7ee81526
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977033"
---
# <a name="how-to-resize-a-canvas-by-using-a-thumb"></a><span data-ttu-id="0494b-102">Gewusst wie: Ändern der Canvas-Größe mithilfe eines Ziehpunkts</span><span class="sxs-lookup"><span data-stu-id="0494b-102">How to: Resize a Canvas by Using a Thumb</span></span>
<span data-ttu-id="0494b-103">Dieses Beispiel zeigt, wie ein- <xref:System.Windows.Controls.Primitives.Thumb> Steuerelement zum Ändern der Größe eines-Steuer Elements verwendet wird <xref:System.Windows.Controls.Canvas> .</span><span class="sxs-lookup"><span data-stu-id="0494b-103">This example shows how to use a <xref:System.Windows.Controls.Primitives.Thumb> control to resize a <xref:System.Windows.Controls.Canvas> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0494b-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0494b-104">Example</span></span>  
 <span data-ttu-id="0494b-105">Das <xref:System.Windows.Controls.Primitives.Thumb> -Steuerelement stellt Drag-Funktionen bereit, die zum Verschieben oder Ändern der Größe von Steuerelementen verwendet werden können, indem die <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> -und- <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> Ereignisse von <xref:System.Windows.Controls.Primitives.Thumb> überwacht werden</span><span class="sxs-lookup"><span data-stu-id="0494b-105">The <xref:System.Windows.Controls.Primitives.Thumb> control provides drag functionality that can be used to move or resize controls by monitoring the <xref:System.Windows.Controls.Primitives.Thumb.DragStarted>, <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> and <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> events of the <xref:System.Windows.Controls.Primitives.Thumb>.</span></span>  
  
 <span data-ttu-id="0494b-106">Der Benutzer startet einen Zieh Vorgang durch Drücken der linken Maustaste, wenn der Mauszeiger auf dem Steuerelement angehalten wird <xref:System.Windows.Controls.Primitives.Thumb> .</span><span class="sxs-lookup"><span data-stu-id="0494b-106">The user begins a drag operation by pressing the left mouse button when the mouse pointer is paused on the <xref:System.Windows.Controls.Primitives.Thumb> control.</span></span> <span data-ttu-id="0494b-107">Der Zieh Vorgang wird fortgesetzt, solange die linke Maustaste gedrückt bleibt.</span><span class="sxs-lookup"><span data-stu-id="0494b-107">The drag operation continues as long as the left mouse button remains pressed.</span></span> <span data-ttu-id="0494b-108">Während des Zieh Vorgangs kann das mehrmals <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> vorkommen.</span><span class="sxs-lookup"><span data-stu-id="0494b-108">During the drag operation, the <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> can occur more than once.</span></span> <span data-ttu-id="0494b-109">Jedes Mal, wenn es auftritt, stellt die- <xref:System.Windows.Controls.Primitives.DragDeltaEventArgs> Klasse die Änderung an der Position bereit, die der Änderung in der Mausposition entspricht.</span><span class="sxs-lookup"><span data-stu-id="0494b-109">Each time it occurs, the <xref:System.Windows.Controls.Primitives.DragDeltaEventArgs> class provides the change in position that corresponds to the change in mouse position.</span></span> <span data-ttu-id="0494b-110">Wenn der Benutzer die linke Maustaste loslässt, ist der Zieh Vorgang abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0494b-110">When the user releases the left mouse button, the drag operation is finished.</span></span> <span data-ttu-id="0494b-111">Der Zieh Vorgang bietet nur neue Koordinaten. die wird nicht automatisch neu positioniert <xref:System.Windows.Controls.Primitives.Thumb> .</span><span class="sxs-lookup"><span data-stu-id="0494b-111">The drag operation only provides new coordinates; it does not automatically reposition the <xref:System.Windows.Controls.Primitives.Thumb>.</span></span>  
  
 <span data-ttu-id="0494b-112">Im folgenden Beispiel wird ein- <xref:System.Windows.Controls.Primitives.Thumb> Steuerelement gezeigt, das das untergeordnete-Element eines-Steuer Elements ist <xref:System.Windows.Controls.Canvas> .</span><span class="sxs-lookup"><span data-stu-id="0494b-112">The following example shows a <xref:System.Windows.Controls.Primitives.Thumb> control that is the child element of a <xref:System.Windows.Controls.Canvas> control.</span></span> <span data-ttu-id="0494b-113">Der Ereignishandler für das <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> zugehörige-Ereignis stellt die Logik zum Verschieben der <xref:System.Windows.Controls.Primitives.Thumb> und zum Ändern der Größe des bereit <xref:System.Windows.Controls.Canvas> .</span><span class="sxs-lookup"><span data-stu-id="0494b-113">The event handler for its <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> event provides the logic to move the <xref:System.Windows.Controls.Primitives.Thumb> and resize the <xref:System.Windows.Controls.Canvas>.</span></span> <span data-ttu-id="0494b-114">Die Ereignishandler für das <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> -Ereignis und das- <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> Ereignis ändern die Farbe von <xref:System.Windows.Controls.Primitives.Thumb> während eines Zieh Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="0494b-114">The event handlers for the <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> and <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> event change the color of the <xref:System.Windows.Controls.Primitives.Thumb> during a drag operation.</span></span> <span data-ttu-id="0494b-115">Im folgenden Beispiel wird der definiert <xref:System.Windows.Controls.Primitives.Thumb> .</span><span class="sxs-lookup"><span data-stu-id="0494b-115">The following example defines the <xref:System.Windows.Controls.Primitives.Thumb>.</span></span>  
  
 [!code-xaml[Thumb#thumb](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml#thumb)]  
  
 <span data-ttu-id="0494b-116">Das folgende Beispiel zeigt den <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> Ereignishandler, der das verschiebt <xref:System.Windows.Controls.Primitives.Thumb> und die Größe des <xref:System.Windows.Controls.Canvas> in Reaktion auf eine Mausbewegung ändert.</span><span class="sxs-lookup"><span data-stu-id="0494b-116">The following example shows the <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> event handler that moves the <xref:System.Windows.Controls.Primitives.Thumb> and resizes the <xref:System.Windows.Controls.Canvas> in response to a mouse movement.</span></span>  
  
 [!code-csharp[Thumb#2](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml.cs#2)]  
  
 <span data-ttu-id="0494b-117">Das folgende Beispiel zeigt den- <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="0494b-117">The following example shows the <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> event handler.</span></span>  
  
 [!code-csharp[Thumb#DragStartedHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml.cs#dragstartedhandler)]
 [!code-vb[Thumb#DragStartedHandler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Thumb/VisualBasic/Pane1.xaml.vb#dragstartedhandler)]  
  
 <span data-ttu-id="0494b-118">Das folgende Beispiel zeigt den- <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> Ereignishandler.</span><span class="sxs-lookup"><span data-stu-id="0494b-118">The following example shows the <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> event handler.</span></span>  
  
 [!code-csharp[Thumb#DragCompletedHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml.cs#dragcompletedhandler)]
 [!code-vb[Thumb#DragCompletedHandler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Thumb/VisualBasic/Pane1.xaml.vb#dragcompletedhandler)]  
  
 <span data-ttu-id="0494b-119">Das komplette Beispiel finden Sie unter [Beispiel für Thumb Drag-Funktionalität](https://github.com/Microsoft/WPF-Samples/tree/master/Drag%20and%20Drop/DragDropThumbOps).</span><span class="sxs-lookup"><span data-stu-id="0494b-119">For the complete sample, see [Thumb Drag Functionality Sample](https://github.com/Microsoft/WPF-Samples/tree/master/Drag%20and%20Drop/DragDropThumbOps).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0494b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0494b-120">See also</span></span>

- <xref:System.Windows.Controls.Primitives.Thumb>
- <xref:System.Windows.Controls.Primitives.Thumb.DragStarted>
- <xref:System.Windows.Controls.Primitives.Thumb.DragDelta>
- <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted>
