---
title: Drei Kategorien von Grafikdiensten
ms.date: 03/30/2017
helpviewer_keywords:
- imaging
- graphics [Windows Forms], categories
- 2D vector graphics
- vector graphics
- typography
ms.assetid: 068c0ef3-f6ee-4d58-a7b6-eb2531ead408
ms.openlocfilehash: fa7391ef0f7170ddb9d9d24aa5a1a03635bf46e0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975227"
---
# <a name="three-categories-of-graphics-services"></a>Drei Kategorien von Grafikdiensten
Die Grafik Angebote in Windows Forms in die folgenden drei allgemeinen Kategorien eingeteilt:  
  
- Zweidimensionale (2D) Vektorgrafiken  
  
- Bildverarbeitung  
  
- Typografie  
  
## <a name="2d-vector-graphics"></a>2D-Vektorgrafiken  
 Zweidimensionale Vektorgrafiken, z. b. Linien, Kurven und Abbildungen, sind primitive, die durch Sätze von Punkten auf einem Koordinatensystem angegeben werden. Beispielsweise wird eine gerade Linie durch die beiden Endpunkte angegeben, und ein Rechteck wird durch einen Punkt angegeben, der die Position der linken oberen Ecke und ein Nummern Paar mit der Breite und Höhe gibt. Ein einfacher Pfad wird durch ein Array von Punkten angegeben, die durch gerade Linien miteinander verbunden sind. Eine Bézier-Spline ist eine ausgereifte Kurve, die durch vier Steuerungs Punkte angegeben wird.  
  
 GDI+ stellt Klassen und Strukturen bereit, die Informationen zu den primitiven selbst speichern, Klassen, in denen Informationen zur Art und Weise des Zeichnens der primitiven gespeichert werden, sowie Klassen, die die Zeichnung tatsächlich durchführen. Beispielsweise speichert die <xref:System.Drawing.Rectangle> -Struktur die Position und Größe eines Rechtecks. die- <xref:System.Drawing.Pen> Klasse speichert Informationen über die Linien Farbe, die Linienstärke und den Linienstil, und die- <xref:System.Drawing.Graphics> Klasse verfügt über Methoden zum Zeichnen von Linien, Rechtecke, Pfaden und anderen Abbildungen. Außerdem gibt es mehrere <xref:System.Drawing.Brush> Klassen, die Informationen darüber speichern, wie geschlossene Abbildungen und Pfade mit Farben oder Mustern gefüllt werden.  
  
 Sie können ein Vektorbild, das eine Sequenz von Grafik Befehlen ist, in einer Metadatei aufzeichnen. GDI+ stellt die <xref:System.Drawing.Imaging.Metafile> -Klasse zum Aufzeichnen, anzeigen und Speichern von Metadateien bereit. Mit der <xref:System.Drawing.Imaging.MetafileHeader> -Klasse und der- <xref:System.Drawing.Imaging.MetaHeader> Klasse können Sie die in einem Metadatei-Header gespeicherten Daten überprüfen.  
  
## <a name="imaging"></a>Bildverarbeitung  
 Es ist schwierig oder unmöglich, bestimmte Arten von Bildern mit den Techniken von Vektorgrafiken anzuzeigen. Beispielsweise können die Bilder auf den Symbolleisten Schaltflächen und die Bilder, die als Symbole angezeigt werden, schwierig als Auflistungen von Linien und Kurven angegeben werden. Ein qualitativ hochauflösendes digitales Foto eines überfüllten Baseball-Stadions ist sogar noch schwieriger zu erstellen mit Vektor Techniken. Bilder dieses Typs werden als Bitmaps gespeichert, bei denen es sich um Arrays von Zahlen handelt, die die Farben einzelner Punkte auf dem Bildschirm darstellen. GDI+ stellt die- <xref:System.Drawing.Bitmap> Klasse zum Anzeigen, bearbeiten und Speichern von Bitmaps bereit.  
  
## <a name="typography"></a>Typografie  
 Typografiedarstellung ist die Anzeige von Text in einer Vielzahl von Schriftarten, Größen und Stilen. GDI+ bietet umfassende Unterstützung für diese komplexe Aufgabe. Eines der neuen Features in GDI+ ist Subpixel-Antialiasing, wodurch Text auf einem LCD-Bildschirm gerendert wird.  
  
 Außerdem bietet Windows Forms die Option zum Zeichnen von Text mit GDI-Funktionen in der- <xref:System.Windows.Forms.TextRenderer> Klasse.  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Grafiken](graphics-overview-windows-forms.md)
- [Verwalteter Code in GDI+](about-gdi-managed-code.md)
- [Verwenden von verwalteten Grafikklassen](using-managed-graphics-classes.md)
