---
title: 'Vorgehensweise: Abflachen eines Kurvenpfads zu einer Linie'
ms.date: 03/30/2017
helpviewer_keywords:
- graphics [Windows Forms], flattening curves into lines
- curves [Windows Forms], flattening
- GraphicsPath object
- paths [Windows Forms], flattening
- drawing [Windows Forms], flattening curves
ms.assetid: e654b8de-25f4-4735-9208-42e4514a589c
ms.openlocfilehash: d59a802618ddd5080c651e822ed4c09641f7f170
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976162"
---
# <a name="how-to-flatten-a-curved-path-into-a-line"></a>Vorgehensweise: Abflachen eines Kurvenpfads zu einer Linie
Ein <xref:System.Drawing.Drawing2D.GraphicsPath> -Objekt speichert eine Sequenz von Linien und Bézier-Splines. Sie können einem Pfad mehrere Arten von Kurven (Ellipsen, Arcs, kardinale Splines) hinzufügen, aber jede Kurve wird in eine Bézier-Spline konvertiert, bevor Sie im Pfad gespeichert wird. Das Vereinfachen eines Pfads besteht darin, jede Bézier-Spline im Pfad in eine Sequenz von geraden Zeilen umzuwandeln. Die folgende Abbildung zeigt einen Pfad vor und nach der Vereinfachung.  
  
 ![Gerade Linien und Kurven](./media/aboutgdip02-art32a.gif "AboutGdip02_Art32A")  
  
### <a name="to-flatten-a-path"></a>So vereinfachen Sie einen Pfad  
  
- Ruft die- <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> Methode eines- <xref:System.Drawing.Drawing2D.GraphicsPath> Objekts auf. Die <xref:System.Drawing.Drawing2D.GraphicsPath.Flatten%2A> -Methode empfängt ein abflachungs-Argument, das den maximalen Abstand zwischen dem vereinfachten Pfad und dem ursprünglichen Pfad angibt.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Drawing2D.GraphicsPath?displayProperty=nameWithType>
- [Linien, Kurven und Formen](lines-curves-and-shapes.md)
- [Erstellen und Zeichnen von Pfaden](constructing-and-drawing-paths.md)
