---
title: 'Vorgehensweise: Verwenden von Ausschneiden mit einem Bereich'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- regions [Windows Forms], clipping
- regions [Windows Forms], restricting drawing surface
ms.assetid: 43d121b4-e14c-4901-b25c-2d6c25ba4e29
ms.openlocfilehash: e62be137b36a2f369c02151466154f6b3bab090b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975860"
---
# <a name="how-to-use-clipping-with-a-region"></a>Vorgehensweise: Verwenden von Ausschneiden mit einem Bereich
Eine der Eigenschaften der- <xref:System.Drawing.Graphics> Klasse ist der Clip Bereich. Alle Zeichnungen, die von einem bestimmten Objekt durchgeführt werden <xref:System.Drawing.Graphics> , sind auf den Ausschneide Bereich dieses <xref:System.Drawing.Graphics> Objekts beschränkt. Sie können den Clip Bereich festlegen, indem Sie die- <xref:System.Drawing.Graphics.SetClip%2A> Methode aufrufen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein Pfad erstellt, der aus einem einzelnen Polygon besteht. Anschließend erstellt der Code basierend auf diesem Pfad einen Bereich. Der Bereich wird an die <xref:System.Drawing.Graphics.SetClip%2A> -Methode eines <xref:System.Drawing.Graphics> -Objekts weitergegeben, und dann werden zwei Zeichen folgen gezeichnet.  
  
 Die folgende Abbildung zeigt die ausgeschnittenen Zeichen folgen:  
  
 ![Screenshot, in dem abgeschnittene Zeichen folgen angezeigt werden.](./media/how-to-use-clipping-with-a-region/clipped-strings-polygon.png)  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.MiscLegacyTopics#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- [Bereiche in GDI+](regions-in-gdi.md)
- [Verwenden von Bereichen](using-regions.md)
