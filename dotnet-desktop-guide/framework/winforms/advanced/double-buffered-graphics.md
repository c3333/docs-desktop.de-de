---
title: Doppelt gepufferte Grafiken
ms.date: 03/30/2017
helpviewer_keywords:
- double buffering
- graphics [Windows Forms], double-buffered
- flicker [Windows Forms], reducing with double buffering
- examples [Windows Forms], double-buffered graphics
ms.assetid: 4f6fef99-0972-436e-9d73-0167e4033f71
ms.openlocfilehash: 20ec03e6b84110f7ea00c134dc18b23f233c5f58
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975373"
---
# <a name="double-buffered-graphics"></a>Doppelt gepufferte Grafiken
Flimmern ist ein häufiges Problem beim Programmieren von Grafiken. Grafikoperationen, die mehrere komplexe Zeichenvorgänge erfordern, können dazu führen, dass gerenderte Bilder flimmern oder anderweitig nicht ordnungsgemäß dargestellt werden. Um diese Probleme zu beheben, stellt .NET Framework Zugriff auf doppelte Pufferung bereit.  
  
 Bei der doppelten Pufferung werden Flimmerprobleme, die durch mehrere Zeichenoperationen entstehen, mithilfe eines Arbeitsspeicherpuffers behoben. Wenn die doppelte Pufferung aktiviert ist, werden alle Zeichenoperationen anstelle der Zeichenoberfläche auf dem Bildschirm zunächst in einen Arbeitsspeicherpuffer gerendert. Nachdem alle Zeichenoperationen abgeschlossen sind, wird der Arbeitsspeicherpuffer direkt in die damit verbundene Zeichenoberfläche kopiert. Da auf dem Bildschirm nur eine Grafikoperation ausgeführt wird, wird das durch komplexe Zeichenoperationen ausgelöste Bildflimmern beseitigt.  
  
## <a name="default-double-buffering"></a>Standardmäßige doppelte Pufferung  
 Die einfachste Möglichkeit, die doppelte Pufferung in Anwendungen zu verwenden, bietet die doppelte Pufferung für Formulare und Steuerelemente, die standardmäßig von .NET Framework bereitgestellt wird. Sie können die standardmäßige doppelte Pufferung für Ihre Windows Forms und die erstellten Windows-Steuerelemente aktivieren, indem Sie die- <xref:System.Windows.Forms.Control.DoubleBuffered%2A> Eigenschaft auf `true` oder mithilfe der- <xref:System.Windows.Forms.Control.SetStyle%2A> Methode festlegen. Weitere Informationen finden Sie unter [Gewusst wie: Reduzieren von Grafikflimmern mit doppelter Pufferung für Formulare und Steuerelemente](how-to-reduce-graphics-flicker-with-double-buffering-for-forms-and-controls.md).  
  
## <a name="manually-managing-buffered-graphics"></a>Manuelles Verwalten gepufferter Grafiken  
 Bei anspruchsvolleren Szenarien mit doppelter Pufferung, wie Animationen oder erweiterter Speicherverwaltung, können Sie mithilfe der .NET Framework-Klassen Ihre eigene doppelte Pufferungslogik implementieren. Die Klasse, die für das zuordnen und Verwalten einzelner Grafik Puffer zuständig ist, ist die- <xref:System.Drawing.BufferedGraphicsContext> Klasse. Jede Anwendungsdomäne verfügt über eine eigene Standard <xref:System.Drawing.BufferedGraphicsContext> Instanz, die die standardmäßige doppelte Pufferung für diese Anwendung verwaltet. In den meisten Fällen gibt es nur eine Anwendungsdomäne pro Anwendung, daher ist in der Regel ein Standardwert <xref:System.Drawing.BufferedGraphicsContext> pro Anwendung vorhanden. Standard <xref:System.Drawing.BufferedGraphicsContext> Instanzen werden von der- <xref:System.Drawing.BufferedGraphicsManager> Klasse verwaltet. Sie können einen Verweis auf die Standard Instanz abrufen, <xref:System.Drawing.BufferedGraphicsContext> indem Sie aufrufen <xref:System.Drawing.BufferedGraphicsManager.Current%2A> . Sie können auch eine dedizierte- <xref:System.Drawing.BufferedGraphicsContext> Instanz erstellen, die die Leistung für grafisch intensive Anwendungen verbessern kann. Weitere Informationen zum Erstellen einer-Instanz finden Sie unter Gewusst <xref:System.Drawing.BufferedGraphicsContext> [wie: Manuelles Verwalten von gepufferten Grafiken](how-to-manually-manage-buffered-graphics.md).  
  
## <a name="manually-displaying-buffered-graphics"></a>Manuelles Anzeigen gepufferter Grafiken  
 Sie können eine Instanz der-Klasse verwenden, <xref:System.Drawing.BufferedGraphicsContext> um Grafik Puffer durch Aufrufen von zu erstellen <xref:System.Drawing.BufferedGraphicsContext.Allocate%2A?displayProperty=nameWithType> , die eine Instanz der-Klasse zurückgibt <xref:System.Drawing.BufferedGraphics> . Ein- <xref:System.Drawing.BufferedGraphics> Objekt verwaltet einen Arbeitsspeicher Puffer, der einer Renderingoberfläche zugeordnet ist, z. b. ein Formular oder ein Steuerelement.  
  
 Nachdem die Klasse instanziiert wurde, <xref:System.Drawing.BufferedGraphics> verwaltet Sie das Rendering zu einem in-Memory-Grafik Puffer. Sie können Grafiken in den Arbeitsspeicher Puffer über das Renderern <xref:System.Drawing.BufferedGraphics.Graphics%2A> , das ein- <xref:System.Drawing.Graphics> Objekt verfügbar macht, das den Speicherpuffer direkt darstellt. Sie können <xref:System.Drawing.Graphics> genau wie bei einem- <xref:System.Drawing.Graphics> Objekt, das eine Zeichen Oberfläche darstellt, zu diesem Objekt zeichnen. Nachdem alle Grafiken in den Puffer gezogen wurden, können Sie den <xref:System.Drawing.BufferedGraphics.Render%2A?displayProperty=nameWithType> Inhalt des Puffers mit dem auf die Zeichen Oberfläche auf dem Bildschirm kopieren.  
  
 Weitere Informationen zur Verwendung der- <xref:System.Drawing.BufferedGraphics> Klasse finden Sie unter [Manuelles Rendern von gepufferten Grafiken](how-to-manually-render-buffered-graphics.md). Weitere Informationen zum Rendern von Grafiken finden Sie unter [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.BufferedGraphics>
- <xref:System.Drawing.BufferedGraphicsContext>
- <xref:System.Drawing.BufferedGraphicsManager>
- [Vorgehensweise: Manuelles Rendern von gepufferten Grafiken](how-to-manually-render-buffered-graphics.md)
- [Vorgehensweise: Reduzieren von Grafikflimmern mit doppelter Pufferung für Formulare und Steuerelemente](how-to-reduce-graphics-flicker-with-double-buffering-for-forms-and-controls.md)
- [Vorgehensweise: Manuelles Verwalten von gepufferten Grafiken](how-to-manually-manage-buffered-graphics.md)
- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
