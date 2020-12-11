---
title: 'Vorgehensweise: Ausfüllen einer Form mit einer Schraffur'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- patterns [Windows Forms], adding to shapes
- shapes [Windows Forms], filling with patterns
- brushes [Windows Forms], using hatch brushes
ms.assetid: 9c8300ff-187b-404f-af1f-ebd499f5b16f
ms.openlocfilehash: b80708f0ce722b1809fe49190639231e7e4c8329
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976165"
---
# <a name="how-to-fill-a-shape-with-a-hatch-pattern"></a>Vorgehensweise: Ausfüllen einer Form mit einer Schraffur
Ein Schraffurmuster wird aus zwei Farben erstellt: eine für den Hintergrund und eine für die Linien, die das Muster über den Hintergrund bilden. Um eine geschlossene Form mit einem Schraffurmuster auszufüllen, verwenden Sie ein- <xref:System.Drawing.Drawing2D.HatchBrush> Objekt. Im folgenden Beispiel wird veranschaulicht, wie Sie eine Ellipse mit einem Schraffurmuster ausfüllen:  
  
## <a name="example"></a>Beispiel  
 Der <xref:System.Drawing.Drawing2D.HatchBrush.%23ctor%2A> Konstruktor benötigt drei Argumente: die Schraffurart, die Farbe der schraffurzeile und die Farbe des Hintergrunds. Das schraffurargumentgument kann ein beliebiger Wert aus der- <xref:System.Drawing.Drawing2D.HatchStyle> Enumeration sein. In der-Enumeration sind mehr als 50 Elemente vorhanden <xref:System.Drawing.Drawing2D.HatchStyle> . einige dieser Elemente werden in der folgenden Liste angezeigt:  
  
- <xref:System.Drawing.Drawing2D.HatchStyle.Horizontal>  
  
- <xref:System.Drawing.Drawing2D.HatchStyle.Vertical>  
  
- <xref:System.Drawing.Drawing2D.HatchStyle.ForwardDiagonal>  
  
- <xref:System.Drawing.Drawing2D.HatchStyle.BackwardDiagonal>  
  
- <xref:System.Drawing.Drawing2D.HatchStyle.Cross>  
  
- <xref:System.Drawing.Drawing2D.HatchStyle.DiagonalCross>  
  
 Die folgende Abbildung zeigt die gefüllte Ellipse.  
  
  ![Screenshot, der zeigt, wie eine Ellipse mit einem Schraffurmuster aussieht.](./media/how-to-fill-a-shape-with-a-hatch-pattern/ellipse-filled-hatch.png "hatch1")
  
 [!code-csharp[System.Drawing.UsingABrush#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingABrush/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.UsingABrush#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingABrush/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das obige Beispiel ist für die Verwendung in Windows Forms konzipiert und erfordert <xref:System.Windows.Forms.PaintEventArgs>`e`, einen Parameter des <xref:System.Windows.Forms.Control.Paint>-Ereignishandlers.  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden eines Pinsels zum Ausfüllen von Formen](using-a-brush-to-fill-shapes.md)
