---
title: Multithreading in Steuerelementen
ms.date: 03/30/2017
helpviewer_keywords:
- BackgroundWorker component
- threading [Windows Forms], controls
ms.assetid: c311d652-0f26-45fa-bdcc-b1615d73ce4e
ms.openlocfilehash: 79832e12a10f02c909d2a28270594bcb4ea68656
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975543"
---
# <a name="multithreading-in-windows-forms-controls"></a>Multithreading in Windows Forms-Steuerelementen
In vielen Anwendungen können Sie die Benutzeroberfläche (UI) reaktionsfähiger machen, indem Sie zeitaufwändige Vorgänge in einem anderen Thread ausführen. Zum Multithreading Ihrer Windows Forms-Steuerelemente stehen eine Reihe von Tools zur Verfügung, einschließlich des <xref:System.Threading> -Namespace, der <xref:System.Windows.Forms.Control.BeginInvoke%2A?displayProperty=nameWithType> -Methode und der- `BackgroundWorker` Komponente.  
  
> [!NOTE]
> Die `BackgroundWorker` Komponente ersetzt und fügt Funktionen zum <xref:System.Threading> -Namespace und zur- <xref:System.Windows.Forms.Control.BeginInvoke%2A?displayProperty=nameWithType> Methode hinzu. Diese werden jedoch sowohl für die Abwärtskompatibilität als auch für die zukünftige Verwendung beibehalten, wenn Sie auswählen. Weitere Informationen finden Sie unter [Übersicht über die BackgroundWorker-Komponente](backgroundworker-component-overview.md).  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Vorgehensweise: Threadsicheres Aufrufen von Windows Forms-Steuerelementen](how-to-make-thread-safe-calls-to-windows-forms-controls.md)  
 Zeigt, wie Thread sichere Aufrufe an Windows Forms-Steuerelemente durchführen werden.  
  
 [Vorgehensweise: Verwenden eines Hintergrundthreads zur Dateisuche](how-to-use-a-background-thread-to-search-for-files.md)  
 Zeigt, wie Sie mit dem <xref:System.Threading> -Namespace und der- <xref:System.Windows.Forms.Control.BeginInvoke%2A> Methode asynchron nach Dateien suchen.  
  
## <a name="reference"></a>Verweis  
 <xref:System.ComponentModel.BackgroundWorker>  
 Dokumentiert eine Komponente, die einen Arbeits Thread für asynchrone Vorgänge kapselt.  
  
 <xref:System.Media.SoundPlayer.LoadAsync%2A>  
 Dokumente zum asynchronen Laden eines Sounds.  
  
 <xref:System.Windows.Forms.PictureBox.LoadAsync%2A>  
 Dokumente zum asynchronen Laden eines Bilds.  
  
## <a name="related-sections"></a>Verwandte Abschnitte  
 [How to: Ausführen eines Vorgangs im Hintergrund](how-to-run-an-operation-in-the-background.md)  
 Zeigt, wie ein zeitaufwendiger Vorgang mit der-Komponente durchgeführt wird <xref:System.ComponentModel.BackgroundWorker> .  
  
 [Übersicht über die BackgroundWorker-Komponente](backgroundworker-component-overview.md)  
 Enthält Themen, in denen beschrieben wird, wie die- <xref:System.ComponentModel.BackgroundWorker> Komponente für asynchrone Vorgänge verwendet wird.
