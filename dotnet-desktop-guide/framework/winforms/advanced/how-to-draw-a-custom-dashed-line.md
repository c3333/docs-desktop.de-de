---
title: 'Vorgehensweise: Zeichnen einer benutzerdefinierten gestrichelten Linie'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- lines [Windows Forms], custom
- lines [Windows Forms], drawing
- lines [Windows Forms], dashed
ms.assetid: cd0ed96a-cce4-47b9-b58a-3bae2e3d1bee
ms.openlocfilehash: d2184a8d7d7f24b8f631818608ab4bcdb89857c7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972356"
---
# <a name="how-to-draw-a-custom-dashed-line"></a>Vorgehensweise: Zeichnen einer benutzerdefinierten gestrichelten Linie
GDI+ stellt mehrere Dash-Stile bereit, die in der- <xref:System.Drawing.Drawing2D.DashStyle> Enumeration aufgelistet sind. Wenn diese standardmäßigen Dash-Stile nicht Ihren Anforderungen entsprechen, können Sie ein benutzerdefiniertes Bindestrich Muster erstellen.  
  
## <a name="example"></a>Beispiel  
 Zum Zeichnen einer benutzerdefinierten gestrichelten Linie platzieren Sie die Längen der Bindestriche und Leerzeichen in einem Array, und weisen Sie das Array als Wert der- <xref:System.Drawing.Pen.DashPattern%2A> Eigenschaft eines- <xref:System.Drawing.Pen> Objekts zu. Im folgenden Beispiel wird eine benutzerdefinierte gestrichelte Linie auf Grundlage des-Arrays gezeichnet `{5, 2, 15, 4}` . Wenn Sie die Elemente des Arrays mit der Stift Breite 5 multiplizieren, erhalten Sie `{25, 10, 75, 20}` . Die angezeigten Bindestriche wechseln in eine Länge zwischen 25 und 75 und die Leerzeichen sind in der Länge zwischen 10 und 20.  
  
 In der folgenden Abbildung ist die resultierende gestrichelte Linie dargestellt. Beachten Sie, dass der abschließende Bindestrich kürzer als 25 Einheiten sein muss, damit die Zeile auf (405, 5) enden kann.  
  
 ![Abbildung, die eine gestrichelte Linie anzeigt.](./media/how-to-draw-a-custom-dashed-line/dashed-line-illustration.gif "pens6")  
  
 [!code-csharp[System.Drawing.UsingAPen#51](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.UsingAPen/CS/Class1.cs#51)]
 [!code-vb[System.Drawing.UsingAPen#51](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.UsingAPen/VB/Class1.vb#51)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Erstellen Sie ein Windows Form, und behandeln Sie das-Ereignis des Formulars <xref:System.Windows.Forms.Control.Paint> . Fügen Sie den vorangehenden Code in den- <xref:System.Windows.Forms.Control.Paint> Ereignishandler ein.  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden eines Stifts zum Zeichnen von Linien und Formen](using-a-pen-to-draw-lines-and-shapes.md)
