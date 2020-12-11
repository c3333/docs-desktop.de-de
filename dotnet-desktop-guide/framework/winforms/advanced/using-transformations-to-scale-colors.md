---
title: Skalieren von Farben mithilfe von Transformationen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- transformations [Windows Forms], for scaling colors
- colors [Windows Forms], scaling
ms.assetid: df23c887-7fd6-4b15-ad94-e30b5bd4b849
ms.openlocfilehash: 81c0ddf5b937d604559a9eb1a8b598885546c97f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975830"
---
# <a name="using-transformations-to-scale-colors"></a>Skalieren von Farben mithilfe von Transformationen
Eine Skalierungs Transformation multipliziert eine oder mehrere der vier Farbkomponenten mit einer Zahl. Die Farbmatrix Einträge, die die Skalierung darstellen, werden in der folgenden Tabelle angegeben.  
  
|Zu skalierbare Komponente|Matrix Eintrag|  
|----------------------------|------------------|  
|Red|[0][0]|  
|Grün|[1][1]|  
|Blau|[2][2]|  
|Alpha|[3][3]|  
  
## <a name="scaling-one-color"></a>Skalieren einer Farbe  
 Im folgenden Beispiel wird ein- <xref:System.Drawing.Image> Objekt aus der Datei ColorBars2.bmp erstellt. Anschließend skaliert der Code die blaue Komponente jedes Pixels im Bild um den Faktor 2. Das ursprüngliche Bild wird neben dem transformierten Bild gezeichnet.  
  
 [!code-csharp[System.Drawing.RecoloringImages#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.RecoloringImages#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#41)]  
  
 Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das skalierte Bild auf der rechten Seite an:  
  
 ![Screenshot, der die ursprünglichen und skalierten Farben vergleicht.](./media/using-transformations-to-scale-colors/four-bar-scale-one-color.png)  
  
 In der folgenden Tabelle sind die Farb Vektoren für die vier Balken vor und nach der blauen Skalierung aufgelistet. Beachten Sie, dass die blaue Komponente in der vierten Farbleiste von 0,8 zu 0,6 gewechselt ist. Dies liegt daran, dass GDI+ nur den Bruch Teil des Ergebnisses beibehält. Beispiel: (2) (0,8) = 1,6 und der Bruchteil von 1,6 ist 0,6. Wenn nur der Bruchteil beibehalten wird, wird sichergestellt, dass das Ergebnis immer im Intervall [0,0] liegt.  
  
|Original|Läufig|  
|--------------|------------|  
|(0.4, 0.4, 0.4, 1)|(0.4, 0.4, 0.8, 1)|  
|(0.4, 0.2, 0.2, 1)|(0.4, 0.2, 0.4, 1)|  
|(0.2, 0.4, 0.2, 1)|(0.2, 0.4, 0.4, 1)|  
|(0.4, 0.4, 0.8, 1)|(0.4, 0.4, 0.6, 1)|  
  
## <a name="scaling-multiple-colors"></a>Skalieren mehrerer Farben  
 Im folgenden Beispiel wird ein- <xref:System.Drawing.Image> Objekt aus der Datei ColorBars2.bmp erstellt. Anschließend werden im Code die roten, grünen und blauen Komponenten der einzelnen Pixel im Bild skaliert. Die roten Komponenten werden auf 25% herunterskaliert, die grünen Komponenten werden um 35% herunterskaliert, und die blauen Komponenten werden um 50% herunterskaliert.  
  
 [!code-csharp[System.Drawing.RecoloringImages#42](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.RecoloringImages/CS/Class1.cs#42)]
 [!code-vb[System.Drawing.RecoloringImages#42](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.RecoloringImages/VB/Class1.vb#42)]  
  
 Die folgende Abbildung zeigt das ursprüngliche Bild auf der linken Seite und das skalierte Bild auf der rechten Seite an:  
  
 ![Screenshot, der die ursprünglichen und skalierten Farben vergleicht.](./media/using-transformations-to-scale-colors/four-bar-scale-multiple-colors.png)  
  
 In der folgenden Tabelle sind die Farb Vektoren für die vier Balken vor und nach der roten, grünen und blauen Skalierung aufgelistet.  
  
|Original|Läufig|  
|--------------|------------|  
|(0.6, 0.6, 0.6, 1)|(0.45, 0.39, 0.3, 1)|  
|(0, 1, 1, 1)|(0, 0.65, 0.5, 1)|  
|(1, 1, 0, 1)|(0.75, 0.65, 0, 1)|  
|(1, 0, 1, 1)|(0.75, 0, 0.5, 1)|  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Imaging.ColorMatrix>
- <xref:System.Drawing.Imaging.ImageAttributes>
- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Neueinfärben von Bildern](recoloring-images.md)
