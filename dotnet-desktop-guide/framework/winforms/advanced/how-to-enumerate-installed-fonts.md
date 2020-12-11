---
title: 'Vorgehensweise: Auflisten installierter Schriftarten'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- fonts [Windows Forms], enumerating installed
- examples [Windows Forms], fonts
ms.assetid: 26d74ef5-0f39-4eeb-8d20-00e66e014abe
ms.openlocfilehash: 92f27399cce9e03a4679c8a34fbdafcf28c32252
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976170"
---
# <a name="how-to-enumerate-installed-fonts"></a>Vorgehensweise: Auflisten installierter Schriftarten
Die <xref:System.Drawing.Text.InstalledFontCollection> Klasse erbt von der <xref:System.Drawing.Text.FontCollection> abstrakten Basisklasse. Sie können ein- <xref:System.Drawing.Text.InstalledFontCollection> Objekt verwenden, um die auf dem Computer installierten Schriftarten aufzulisten. Die- <xref:System.Drawing.Text.FontCollection.Families%2A> Eigenschaft eines <xref:System.Drawing.Text.InstalledFontCollection> Objekts ist ein Array von- <xref:System.Drawing.FontFamily> Objekten.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden die Namen aller auf dem Computer installierten Schriftfamilien aufgelistet. Der Code Ruft die- <xref:System.Drawing.FontFamily.Name%2A> Eigenschaft jedes <xref:System.Drawing.FontFamily> Objekts in dem von der-Eigenschaft zurückgegebenen Array ab <xref:System.Drawing.Text.FontCollection.Families%2A> . Wenn die Familiennamen abgerufen werden, werden Sie verkettet, um eine durch Trennzeichen getrennte Liste zu bilden. Dann <xref:System.Drawing.Graphics.DrawString%2A> zeichnet die-Methode der <xref:System.Drawing.Graphics> -Klasse die durch Trennzeichen getrennte Liste in einem Rechteck.  
  
 Wenn Sie den Beispielcode ausführen, wird die Ausgabe ähnlich wie in der folgenden Abbildung dargestellt:  
  
 ![Screenshot mit den installierten Schriftfamilien.](./media/how-to-enumerate-installed-fonts/list-installed-font-families.png)  
  
 [!code-csharp[System.Drawing.FontsAndText#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.FontsAndText#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> . Außerdem sollten Sie den- <xref:System.Drawing.Text> Namespace importieren.  
  
## <a name="see-also"></a>Siehe auch

- [Verwenden von Schriftarten und Text](using-fonts-and-text.md)
