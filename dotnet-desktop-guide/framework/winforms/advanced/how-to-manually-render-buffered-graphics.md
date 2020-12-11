---
title: 'Vorgehensweise: Manuelles Rendern von gepufferten Grafiken'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- flicker [Windows Forms], reducing by manually rendering graphics
- graphics [Windows Forms], rendering
ms.assetid: 5192295e-bd8e-45f7-8bd6-5c4f6bd21e61
ms.openlocfilehash: a6655652a7c5dedb8e183356688972c07a705cbc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975900"
---
# <a name="how-to-manually-render-buffered-graphics"></a>Vorgehensweise: Manuelles Rendern von gepufferten Grafiken
Wenn Sie Ihre eigenen gepufferten Grafiken verwalten, müssen Sie Grafikpuffer erstellen und rendern können. Sie können Instanzen der <xref:System.Drawing.BufferedGraphics>-Klasse erstellen, die mit Zeichenflächen auf dem Bildschirm verknüpft ist. Dazu rufen Sie die <xref:System.Drawing.BufferedGraphicsContext.Allocate%2A>-Methode auf. Diese Methode erstellt eine <xref:System.Drawing.BufferedGraphics>-Instanz, die mit einer bestimmten Darstellungsoberfläche verknüpft ist, beispielsweise mit einem Formular oder Steuerelement. Nachdem Sie eine <xref:System.Drawing.BufferedGraphics>-Instanz erstellt haben, können Sie mit der<xref:System.Drawing.BufferedGraphics.Graphics%2A>-Eigenschaft Grafiken in den Puffer schreiben, dem die Instanz entspricht. Nachdem Sie alle Grafikvorgänge ausgeführt haben, können Sie den Inhalt des Puffers auf den Bildschirm kopieren, indem Sie die <xref:System.Drawing.BufferedGraphics.Render%2A>-Methode aufrufen.  
  
> [!NOTE]
> Wenn Sie Ihr eigenes Rendering ausführen, erhöht sich die Arbeitsspeichernutzung, allerdings wahrscheinlich nur geringfügig.  
  
### <a name="to-manually-display-buffered-graphics"></a>So zeigen Sie gepufferte Grafiken manuell an  
  
1. Rufen Sie einen Verweis auf eine Instanz der <xref:System.Drawing.BufferedGraphicsContext>-Klasse ab. Weitere Informationen finden Sie unter Gewusst [wie: Manuelles Verwalten von gepufferten Grafiken](how-to-manually-manage-buffered-graphics.md).  
  
2. Erstellen Sie eine Instanz der <xref:System.Drawing.BufferedGraphics>-Klasse, indem Sie die <xref:System.Drawing.BufferedGraphicsContext.Allocate%2A>-Methode wie im folgenden Codebeispiel gezeigt aufrufen.  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#21)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#21)]  
  
3. Zeichnen Sie Grafiken in den Grafikpuffer, indem Sie die <xref:System.Drawing.BufferedGraphics.Graphics%2A>-Eigenschaft festlegen. Beispiel:  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#22](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#22)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#22](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#22)]  
  
4. Wenn Sie Ihre Zeichenvorgänge für den Grafikpuffer abgeschlossen haben, rufen Sie die <xref:System.Drawing.BufferedGraphics.Render%2A>-Methode auf, um den Puffer, wie im folgenden Codebeispiel gezeigt, entweder auf der Zeichenfläche, die mit diesem Puffer verknüpft ist, oder auf einer angegebenen Zeichenfläche zu rendern.  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#23](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#23)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#23](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#23)]  
  
5. Wenn Sie das Rendern der Grafiken abgeschlossen haben, rufen Sie die `Dispose`-Methode für die <xref:System.Drawing.BufferedGraphics>-Instanz auf, um Systemressourcen freizugeben.  
  
     [!code-csharp[System.Windows.Forms.LegacyBufferedGraphics#24](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/CS/Class1.cs#24)]
     [!code-vb[System.Windows.Forms.LegacyBufferedGraphics#24](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.LegacyBufferedGraphics/VB/Class1.vb#24)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.BufferedGraphicsContext>
- <xref:System.Drawing.BufferedGraphics>
- [Doppelt gepufferte Grafiken](double-buffered-graphics.md)
- [Vorgehensweise: Manuelles Verwalten von gepufferten Grafiken](how-to-manually-manage-buffered-graphics.md)
