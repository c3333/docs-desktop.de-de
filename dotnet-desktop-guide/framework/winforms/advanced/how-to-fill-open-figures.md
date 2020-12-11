---
title: 'Vorgehensweise: Ausfüllen offener Körper'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- open figures [Windows Forms], filling
- figures [Windows Forms], filling
ms.assetid: 5a36b0e4-f1f4-46c0-a85a-22ae98491950
ms.openlocfilehash: 6ecea7d3edb0c3e25fb4e69ff12b88019e530021
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975910"
---
# <a name="how-to-fill-open-figures"></a>Vorgehensweise: Ausfüllen offener Körper
Sie können einen Pfad ausfüllen, indem Sie ein- <xref:System.Drawing.Drawing2D.GraphicsPath> Objekt an die- <xref:System.Drawing.Graphics.FillPath%2A> Methode übergeben. Die- <xref:System.Drawing.Graphics.FillPath%2A> Methode füllt den Pfad gemäß dem Füll Modus (Alternative oder Winding), der derzeit für den Pfad festgelegt ist. Wenn für den Pfad offene Abbildungen vorhanden sind, wird der Pfad so aufgefüllt, als ob diese Abbildungen geschlossen wurden. GDI+ schließt eine Abbildung, indem eine gerade Linie von ihrem Endpunkt zum Ausgangspunkt gezeichnet wird.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein Pfad erstellt, der über eine offene Abbildung (einen Bogen) und eine geschlossene Abbildung (eine Ellipse) verfügt. Die- <xref:System.Drawing.Graphics.FillPath%2A> Methode füllt den Pfad gemäß dem Standard Füll Modus, d <xref:System.Drawing.Drawing2D.FillMode.Alternate> . h..  
  
 Die folgende Abbildung zeigt die Ausgabe des Beispielcodes. Beachten Sie, dass der Pfad (entsprechend) ausgefüllt wird, <xref:System.Drawing.Drawing2D.FillMode.Alternate> als ob die öffnende Figur durch eine gerade Linie von ihrem Endpunkt bis zum Ausgangspunkt geschlossen wurde.  
  
 ![Diagramm, das die Ausgabe der FillPath-Methode anzeigt](./media/how-to-fill-open-figures/fill-path-alternate-mode.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingPaths#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.ConstructingDrawingPaths#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Drawing2D.GraphicsPath>
- [Grafikpfade in GDI+](graphics-paths-in-gdi.md)
