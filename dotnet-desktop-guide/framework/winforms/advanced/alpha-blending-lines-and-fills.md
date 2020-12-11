---
title: Alphablending von Linien und Füllungen
ms.date: 03/30/2017
helpviewer_keywords:
- lines [Windows Forms], adding transparency
- examples [Windows Forms], alpha blending
- alpha blending [Windows Forms], using with lines
- alpha blending
- lines [Windows Forms], alpha blending
- fills [Windows Forms], alpha blending
- alpha blending [Windows Forms], using with fills
- shapes [Windows Forms], adding transparency
ms.assetid: 5440f48c-3ac9-44c3-b170-c1c110bdbab8
ms.openlocfilehash: 66061341ee6539e2172c537a0b2a6ec9ff87565c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974911"
---
# <a name="alpha-blending-lines-and-fills"></a>Alphablending von Linien und Füllungen
In GDI+ ist eine Farbe ein 32-Bit-Wert mit 8 Bits für Alpha, rot, grün und blau. Der Alpha-Wert gibt die Transparenz der Farbe an – das Ausmaß, in dem die Farbe mit der Hintergrundfarbe gemischt wird. Alpha Werte reichen von 0 bis 255, wobei 0 eine vollständig transparente Farbe darstellt und 255 eine vollständig nicht transparente Farbe darstellt.  
  
 Alpha Blending ist eine pixelweise Mischung aus Quell-und Hintergrund Farbdaten. Jede der drei Komponenten (rot, grün, blau) einer angegebenen Quellfarbe wird mit der entsprechenden Komponente der Hintergrundfarbe entsprechend der folgenden Formel gemischt:  
  
 Display Color = sourcecolor × Alpha/255 + BackgroundColor × (255 – Alpha)/255  
  
 Nehmen wir beispielsweise an, die rote Komponente der Quellfarbe ist 150, und die rote Komponente der Hintergrundfarbe ist 100. Wenn der Alpha-Wert 200 ist, wird die rote Komponente der resultierenden Farbe wie folgt berechnet:  
  
 150 × 200 / 255 + 100 × (255 – 200) / 255 = 139  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Vorgehensweise: Zeichnen deckender und halbtransparenter Linien](how-to-draw-opaque-and-semitransparent-lines.md)  
 Zeigt, wie Alpha gemischte Linien gezeichnet werden.  
  
 [Vorgehensweise: Zeichnen mit nicht transparenten und halb transparenten Pinseln](how-to-draw-with-opaque-and-semitransparent-brushes.md)  
 Erläutert die Alpha Mischung mit Pinseln.  
  
 [Vorgehensweise: Verwenden des Mischmodus zum Steuern des Alphablendings](how-to-use-compositing-mode-to-control-alpha-blending.md)  
 Beschreibt, wie die Alpha Mischung mithilfe von gesteuert wird <xref:System.Drawing.Drawing2D.CompositingMode> .  
  
 [Vorgehensweise: Verwenden einer Farbmatrix zum Festlegen von Alphawerten in Bildern](how-to-use-a-color-matrix-to-set-alpha-values-in-images.md)  
 Erläutert, wie ein- <xref:System.Drawing.Imaging.ColorMatrix> Objekt verwendet wird, um Alpha Blending zu steuern.
