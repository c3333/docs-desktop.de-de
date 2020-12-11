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
# <a name="how-to-resize-a-canvas-by-using-a-thumb"></a>Gewusst wie: Ändern der Canvas-Größe mithilfe eines Ziehpunkts
Dieses Beispiel zeigt, wie ein- <xref:System.Windows.Controls.Primitives.Thumb> Steuerelement zum Ändern der Größe eines-Steuer Elements verwendet wird <xref:System.Windows.Controls.Canvas> .  
  
## <a name="example"></a>Beispiel  
 Das <xref:System.Windows.Controls.Primitives.Thumb> -Steuerelement stellt Drag-Funktionen bereit, die zum Verschieben oder Ändern der Größe von Steuerelementen verwendet werden können, indem die <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> -und- <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> Ereignisse von <xref:System.Windows.Controls.Primitives.Thumb> überwacht werden  
  
 Der Benutzer startet einen Zieh Vorgang durch Drücken der linken Maustaste, wenn der Mauszeiger auf dem Steuerelement angehalten wird <xref:System.Windows.Controls.Primitives.Thumb> . Der Zieh Vorgang wird fortgesetzt, solange die linke Maustaste gedrückt bleibt. Während des Zieh Vorgangs kann das mehrmals <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> vorkommen. Jedes Mal, wenn es auftritt, stellt die- <xref:System.Windows.Controls.Primitives.DragDeltaEventArgs> Klasse die Änderung an der Position bereit, die der Änderung in der Mausposition entspricht. Wenn der Benutzer die linke Maustaste loslässt, ist der Zieh Vorgang abgeschlossen. Der Zieh Vorgang bietet nur neue Koordinaten. die wird nicht automatisch neu positioniert <xref:System.Windows.Controls.Primitives.Thumb> .  
  
 Im folgenden Beispiel wird ein- <xref:System.Windows.Controls.Primitives.Thumb> Steuerelement gezeigt, das das untergeordnete-Element eines-Steuer Elements ist <xref:System.Windows.Controls.Canvas> . Der Ereignishandler für das <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> zugehörige-Ereignis stellt die Logik zum Verschieben der <xref:System.Windows.Controls.Primitives.Thumb> und zum Ändern der Größe des bereit <xref:System.Windows.Controls.Canvas> . Die Ereignishandler für das <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> -Ereignis und das- <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> Ereignis ändern die Farbe von <xref:System.Windows.Controls.Primitives.Thumb> während eines Zieh Vorgangs. Im folgenden Beispiel wird der definiert <xref:System.Windows.Controls.Primitives.Thumb> .  
  
 [!code-xaml[Thumb#thumb](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml#thumb)]  
  
 Das folgende Beispiel zeigt den <xref:System.Windows.Controls.Primitives.Thumb.DragDelta> Ereignishandler, der das verschiebt <xref:System.Windows.Controls.Primitives.Thumb> und die Größe des <xref:System.Windows.Controls.Canvas> in Reaktion auf eine Mausbewegung ändert.  
  
 [!code-csharp[Thumb#2](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml.cs#2)]  
  
 Das folgende Beispiel zeigt den- <xref:System.Windows.Controls.Primitives.Thumb.DragStarted> Ereignishandler.  
  
 [!code-csharp[Thumb#DragStartedHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml.cs#dragstartedhandler)]
 [!code-vb[Thumb#DragStartedHandler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Thumb/VisualBasic/Pane1.xaml.vb#dragstartedhandler)]  
  
 Das folgende Beispiel zeigt den- <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted> Ereignishandler.  
  
 [!code-csharp[Thumb#DragCompletedHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/Thumb/CSharp/Pane1.xaml.cs#dragcompletedhandler)]
 [!code-vb[Thumb#DragCompletedHandler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Thumb/VisualBasic/Pane1.xaml.vb#dragcompletedhandler)]  
  
 Das komplette Beispiel finden Sie unter [Beispiel für Thumb Drag-Funktionalität](https://github.com/Microsoft/WPF-Samples/tree/master/Drag%20and%20Drop/DragDropThumbOps).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Primitives.Thumb>
- <xref:System.Windows.Controls.Primitives.Thumb.DragStarted>
- <xref:System.Windows.Controls.Primitives.Thumb.DragDelta>
- <xref:System.Windows.Controls.Primitives.Thumb.DragCompleted>
