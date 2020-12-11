---
title: 'Vorgehensweise: Zeichnen einer ausgefüllten Ellipse in Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
f1_keywords:
- Graphics.FillEllipse
helpviewer_keywords:
- ellipses [Windows Forms], drawing
- circles [Windows Forms], drawing
- circular shapes
- drawing [Windows Forms], ellipses
- shapes [Windows Forms], drawing
- forms [Windows Forms], drawing ellipses
ms.assetid: 781db806-950d-4c5b-b022-493f7fd0c4a8
ms.openlocfilehash: 2e7be3f2c4c710bb24568dd2e70f6f5cc4706c63
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972352"
---
# <a name="how-to-draw-a-filled-ellipse-on-a-windows-form"></a>Vorgehensweise: Zeichnen einer ausgefüllten Ellipse in Windows Forms
In diesem Beispiel wird eine ausgefüllte Ellipse in einem Formular gezeichnet.  
  
## <a name="example"></a>Beispiel  
 [!code-cpp[System.Drawing.ConceptualHowTos#1](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/cpp/form1.cpp#1)]
 [!code-csharp[System.Drawing.ConceptualHowTos#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/CS/form1.cs#1)]
 [!code-vb[System.Drawing.ConceptualHowTos#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConceptualHowTos/VB/form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Diese Methode kann nicht im- <xref:System.Windows.Forms.Form.Load> Ereignishandler aufgerufen werden. Der gezeichnete Inhalt wird nicht neu gezeichnet, wenn die Größe des Formulars geändert oder durch ein anderes Formular verdeckt wird. Damit Ihre Inhalte automatisch neu gezeichnet werden, sollten Sie die- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode überschreiben.  
  
## <a name="robust-programming"></a>Stabile Programmierung  
 Sie sollten immer <xref:System.IDisposable.Dispose%2A> für alle-Objekte, die Systemressourcen nutzen, z <xref:System.Drawing.Brush> . b.-und-Objekte, Abrufen <xref:System.Drawing.Graphics> .  
  
## <a name="see-also"></a>Siehe auch

- [Grafik und Zeichnen in Windows Forms](graphics-and-drawing-in-windows-forms.md)
- [Erste Schritte mit Grafikprogrammierung](getting-started-with-graphics-programming.md)
- [Alphablending von Linien und Füllungen](alpha-blending-lines-and-fills.md)
- [Verwenden eines Pinsels zum Ausfüllen von Formen](using-a-brush-to-fill-shapes.md)
