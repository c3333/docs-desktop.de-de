---
title: Bereiche in GDI+
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- GDI+, regions
- drawing [Windows Forms], regions
- regions
ms.assetid: 52184f9b-16dd-4bbd-85be-029112644ceb
ms.openlocfilehash: 33d4f4ecca7b9d777fa4eab5b6d031de10f03ccc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975248"
---
# <a name="regions-in-gdi"></a>Bereiche in GDI+
Eine Region ist ein Teil des Anzeige Bereichs eines Ausgabegeräts. Bereiche können einfach (ein einzelnes Rechteck) oder komplex sein (eine Kombination aus Polygonen und geschlossenen Kurven). Die folgende Abbildung zeigt zwei Bereiche: eine, die aus einem Rechteck erstellt wurde, und die andere, die aus einem Pfad erstellt wurde.  
  
 ![Regionen](./media/aboutgdip02-art27.gif "AboutGdip02_Art27")  
  
## <a name="using-regions"></a>Verwenden von Bereichen  
 Regionen werden häufig für Clipping-und Treffer Tests verwendet. Beim Clipping wird das Zeichnen auf eine bestimmte Region des Anzeige Bereichs eingeschränkt, in der Regel der Teil, der aktualisiert werden muss. Bei Treffer Tests muss überprüft werden, ob sich der Cursor in einem bestimmten Bereich des Bildschirms befindet, wenn eine Maustaste gedrückt wird.  
  
 Sie können einen Bereich mithilfe eines Rechtecks oder eines Pfads erstellen. Sie können auch komplexe Regionen erstellen, indem Sie vorhandene Regionen kombinieren. Die- <xref:System.Drawing.Region> Klasse stellt die folgenden Methoden zum Kombinieren von Bereichen bereit: <xref:System.Drawing.Region.Intersect%2A> , <xref:System.Drawing.Region.Union%2A> , <xref:System.Drawing.Region.Xor%2A> , <xref:System.Drawing.Region.Exclude%2A> und <xref:System.Drawing.Region.Complement%2A> .  
  
 Die Schnittmenge zweier Regionen ist der Satz aller Punkte, die zu beiden Regionen gehören. Die Union ist der Satz aller Punkte, die zu einer oder den beiden Regionen gehören. Das Komplement einer Region ist der Satz aller Punkte, die sich nicht in der Region befinden. Die folgende Abbildung zeigt die Schnittmenge und die Gesamtmenge der beiden Regionen, die in der obigen Abbildung dargestellt sind.  
  
 ![Regionen](./media/aboutgdip02-art28.gif "AboutGdip02_Art28")  
  
 Die <xref:System.Drawing.Region.Xor%2A> auf ein paar von Regionen angewendete-Methode erzeugt einen Bereich, der alle Punkte enthält, die zu einem Bereich oder dem anderen gehören, aber nicht beides. Die <xref:System.Drawing.Region.Exclude%2A> auf ein paar von Regionen angewendete-Methode erzeugt einen Bereich, der alle Punkte in der ersten Region enthält, die sich nicht in der zweiten Region befinden. Die folgende Abbildung zeigt die Bereiche, die sich aus der Anwendung der <xref:System.Drawing.Region.Xor%2A> -Methode und der- <xref:System.Drawing.Region.Exclude%2A> Methode auf die beiden Regionen am Anfang dieses Themas ergeben.  
  
 ![Regionen](./media/aboutgdip02-art29.gif "AboutGdip02_Art29")  
  
 Um einen Bereich auszufüllen, benötigen Sie ein <xref:System.Drawing.Graphics> -Objekt, ein <xref:System.Drawing.Brush> -Objekt und ein-Objekt <xref:System.Drawing.Region> . Das <xref:System.Drawing.Graphics> -Objekt stellt die <xref:System.Drawing.Graphics.FillRegion%2A> -Methode bereit, und das- <xref:System.Drawing.Brush> Objekt speichert Attribute der Fill-Methode, z. b. Farbe oder Muster. Im folgenden Beispiel wird ein Bereich mit einer voll Tonfarbe gefüllt.  
  
 [!code-csharp[LinesCurvesAndShapes#61](~/samples/snippets/csharp/VS_Snippets_Winforms/LinesCurvesAndShapes/CS/Class1.cs#61)]
 [!code-vb[LinesCurvesAndShapes#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/LinesCurvesAndShapes/VB/Class1.vb#61)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Region?displayProperty=nameWithType>
- [Linien, Kurven und Formen](lines-curves-and-shapes.md)
- [Verwenden von Bereichen](using-regions.md)
