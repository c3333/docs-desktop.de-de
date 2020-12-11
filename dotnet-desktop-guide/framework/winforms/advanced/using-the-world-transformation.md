---
title: Verwenden der globalen Transformation
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- graphics [Windows Forms], world transformation
- world transformation [Windows Forms], examples
ms.assetid: 1e717711-1361-448e-aa49-0f3ec43110c9
ms.openlocfilehash: f40d7e8cb814344365e8b88c2659751903b79d77
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975833"
---
# <a name="using-the-world-transformation"></a>Verwenden der globalen Transformation
Die Welt Transformation ist eine Eigenschaft der- <xref:System.Drawing.Graphics> Klasse. Die Zahlen, die die globale Transformation angeben, werden in einem- <xref:System.Drawing.Drawing2D.Matrix> Objekt gespeichert, das eine 3 × 3-Matrix darstellt. Die <xref:System.Drawing.Drawing2D.Matrix> -Klasse und die- <xref:System.Drawing.Graphics> Klasse verfügen über mehrere Methoden zum Festlegen der Zahlen in der Transformationsmatrix der Welt.  
  
## <a name="different-types-of-transformations"></a>Verschiedene Typen von Transformationen  
 Im folgenden Beispiel erstellt der Code zunächst ein Rechteck mit 50 × 50 und legt es am Ursprung (0,0) ab. Der Ursprung befindet sich in der oberen linken Ecke des Client Bereichs.  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.MiscLegacyTopics#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#11)]  
  
 Der folgende Code wendet eine Skalierungs Transformation an, die das Rechteck um den Faktor 1,75 in der x-Richtung erweitert und das Rechteck um den Faktor 0,5 in der y-Richtung verkleinert:  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#12](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#12)]
 [!code-vb[System.Drawing.MiscLegacyTopics#12](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#12)]  
  
 Das Ergebnis ist ein Rechteck, das in der x-Richtung länger und kürzer in der y-Richtung als die ursprüngliche ist.  
  
 Um das Rechteck zu drehen, anstatt es zu skalieren, verwenden Sie den folgenden Code:  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#13](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#13)]
 [!code-vb[System.Drawing.MiscLegacyTopics#13](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#13)]  
  
 Verwenden Sie den folgenden Code, um das Rechteck zu übersetzen:  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#14](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#14)]
 [!code-vb[System.Drawing.MiscLegacyTopics#14](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#14)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Drawing2D.Matrix>
- [Koordinatensysteme und Transformationen](coordinate-systems-and-transformations.md)
- [Verwenden von Transformationen in Managed GDI+](using-transformations-in-managed-gdi.md)
