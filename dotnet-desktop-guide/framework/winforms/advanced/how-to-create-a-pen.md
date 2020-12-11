---
title: 'Vorgehensweise: Erstellen eines Stifts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- graphics [Windows Forms], creating pens
- pens [Windows Forms], creating
- Pen object
ms.assetid: 7fbea8b7-7ac1-4413-9c17-733a850381e3
ms.openlocfilehash: 69fe6157c710ae63df9dbf391a5d355d1c3f9765
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974844"
---
# <a name="how-to-create-a-pen"></a>Vorgehensweise: Erstellen eines Stifts
In diesem Beispiel wird ein- <xref:System.Drawing.Pen> Objekt erstellt.  
  
## <a name="example"></a>Beispiel  
 [!code-cpp[System.Drawing.ConceptualHowTos#3](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#3)]
 [!code-csharp[System.Drawing.ConceptualHowTos#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#3)]
 [!code-vb[System.Drawing.ConceptualHowTos#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#3)]  
  
## <a name="robust-programming"></a>Stabile Programmierung  
 Wenn Sie die Verwendung von Objekten, die Systemressourcen beanspruchen (z. b.-Objekte), abgeschlossen haben <xref:System.Drawing.Pen> , sollten Sie <xref:System.Drawing.Pen.Dispose%2A> für Sie verwenden.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Pen>
- [Erste Schritte mit Grafikprogrammierung](getting-started-with-graphics-programming.md)
- [Stifte, Linien und Rechtecke in GDI+](pens-lines-and-rectangles-in-gdi.md)
