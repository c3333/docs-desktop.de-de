---
title: 'Vorgehensweise: Manuelles Verwalten von gepufferten Grafiken'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flicker [Windows Forms], reducing by manually managing graphics
- graphics [Windows Forms], managing buffered
ms.assetid: 4c2a90ee-bbbe-4ff6-9170-1b06c195c918
ms.openlocfilehash: 6010d52750b20c07db51917621f8643e9d9b47d7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976149"
---
# <a name="how-to-manually-manage-buffered-graphics"></a>Vorgehensweise: Manuelles Verwalten von gepufferten Grafiken
Für erweiterte Szenarien mit doppelter Pufferung können Sie die .NET Framework-Klassen verwenden, um Ihre eigene, doppelte pufferinglogik zu implementieren. Die Klasse, die für das zuordnen und Verwalten einzelner Grafik Puffer zuständig ist, ist die- <xref:System.Drawing.BufferedGraphicsContext> Klasse. Jede Anwendung verfügt über einen eigenen Standard <xref:System.Drawing.BufferedGraphicsContext> , der die standardmäßige doppelte Pufferung für diese Anwendung verwaltet. Sie können einen Verweis auf diese Instanz abrufen, indem Sie aufrufen <xref:System.Drawing.BufferedGraphicsManager.Current%2A> .  
  
### <a name="to-obtain-a-reference-to-the-default-bufferedgraphicscontext"></a>So rufen Sie einen Verweis auf den Standardwert von BufferedGraphicsContext ab  
  
- Legen Sie die- <xref:System.Drawing.BufferedGraphicsManager.Current%2A> Eigenschaft fest, wie im folgenden Codebeispiel gezeigt.  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#11)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#11)]  
  
    > [!NOTE]
    > Sie müssen die- `Dispose` Methode für den <xref:System.Drawing.BufferedGraphicsContext> Verweis, den Sie von der-Klasse empfangen, nicht aufzurufen <xref:System.Drawing.BufferedGraphicsManager> . Der <xref:System.Drawing.BufferedGraphicsManager> verarbeitet die gesamte Speicher Belegung und-Verteilung für Standard <xref:System.Drawing.BufferedGraphicsContext> Instanzen.  
  
     Für grafisch intensive Anwendungen, wie z. b. Animation, kann die Leistung manchmal verbessert werden, indem ein dedizierter <xref:System.Drawing.BufferedGraphicsContext> anstelle der <xref:System.Drawing.BufferedGraphicsContext> von bereitgestellten verwendet wird <xref:System.Drawing.BufferedGraphicsManager> . Dies ermöglicht es Ihnen, Grafik Puffer einzeln zu erstellen und zu verwalten, ohne dass der Aufwand für die Verwaltung aller anderen gepufferten Grafiken, die der Anwendung zugeordnet sind, entstehen soll, obwohl der von der Anwendung genutzte Arbeitsspeicher größer ist.  
  
### <a name="to-create-a-dedicated-bufferedgraphicscontext"></a>So erstellen Sie einen dedizierten BufferedGraphicsContext  
  
- Deklarieren und erstellen Sie eine neue Instanz der- <xref:System.Drawing.BufferedGraphicsContext> Klasse, wie im folgenden Codebeispiel gezeigt.  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#12)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#12)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.BufferedGraphicsContext>
- [Doppelt gepufferte Grafiken](double-buffered-graphics.md)
- [Vorgehensweise: Manuelles Rendern von gepufferten Grafiken](how-to-manually-render-buffered-graphics.md)
