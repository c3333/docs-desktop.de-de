---
title: 'Vorgehensweise: Festlegen der Farbe eines Stiftes'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- pens [Windows Forms], setting color
- colored pens
ms.assetid: a9df06f9-a6d5-4d9b-a2d1-583943540775
ms.openlocfilehash: ee2d3f8cdf6dd10ca2a9ff0dd3e66b164c84f21b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976118"
---
# <a name="how-to-set-the-color-of-a-pen"></a>Vorgehensweise: Festlegen der Farbe eines Stiftes
In diesem Beispiel wird die Farbe eines bereits vorhandenen Objekts geändert. <xref:System.Drawing.Pen>  
  
## <a name="example"></a>Beispiel  
 [!code-cpp[System.Drawing.ConceptualHowTos#9](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#9)]
 [!code-csharp[System.Drawing.ConceptualHowTos#9](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#9)]
 [!code-vb[System.Drawing.ConceptualHowTos#9](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#9)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Ein-Objekt mit dem <xref:System.Drawing.Pen> Namen `myPen` .  
  
## <a name="robust-programming"></a>Stabile Programmierung  
 Sie sollten <xref:System.Drawing.Pen.Dispose%2A> für-Objekte, die Systemressourcen (z. b.- <xref:System.Drawing.Pen> Objekte) verwenden, nach der Verwendung von aufgerufen werden.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Pen>
- [Erste Schritte mit Grafikprogrammierung](getting-started-with-graphics-programming.md)
- [Vorgehensweise: Erstellen eines Stifts](how-to-create-a-pen.md)
- [Verwenden eines Stifts zum Zeichnen von Linien und Formen](using-a-pen-to-draw-lines-and-shapes.md)
- [Stifte, Linien und Rechtecke in GDI+](pens-lines-and-rectangles-in-gdi.md)
