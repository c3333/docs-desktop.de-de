---
title: Verwenden eines Pinsels für Farbverläufe zum Ausfüllen von Formen
ms.date: 03/30/2017
helpviewer_keywords:
- brushes [Windows Forms], gradient brushes
- gradient brushes
- examples [Windows Forms], gradient brushes
ms.assetid: 2c6037b9-05bd-44c0-a22a-19584b722524
ms.openlocfilehash: 7ff555ba4fd81e9123e5f9e9feed38a0ec9d0a08
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976044"
---
# <a name="using-a-gradient-brush-to-fill-shapes"></a>Verwenden eines Pinsels für Farbverläufe zum Ausfüllen von Formen
Sie können einen Farbverlaufs Pinsel verwenden, um eine Form mit einer allmählich veränderlichen Farbe auszufüllen. Beispielsweise können Sie einen horizontalen Farbverlauf verwenden, um eine Form mit Farben auszufüllen, die sich allmählich ändert, wenn Sie vom linken Rand der Form zum rechten Rand wechseln. Stellen Sie sich ein Rechteck mit einem linken Rand vor, der schwarz ist (dargestellt durch die rote, grüne und blaue Komponente 0, 0, 0) und einen rechten roten Rand (dargestellt durch 255, 0, 0). Wenn das Rechteck 256 Pixel breit ist, ist die rote Komponente eines gegebenen Pixels eine größer als die rote Komponente des Pixels links. Das äußteste linke Pixel in einer Zeile hat Farbkomponenten (0, 0, 0), das zweite Pixel hat (1, 0, 0), das dritte Pixel hat (2, 0, 0) usw., bis Sie zum äußersten äußersten Pixel mit Farbkomponenten (255, 0,0) gelangen. Diese interpoliert Farbwerte bilden den Farbverlauf.  
  
 Die Farbe eines linearen Farbverlaufs ändert sich, wenn Sie horizontal, vertikal oder parallel zu einer angegebenen schrägen Linie wechseln. Ein Pfad Farbverlauf ändert die Farbe, wenn Sie zum inneren und zur Grenze eines Pfads wechseln. Sie können Pfad Farbverläufe anpassen, um eine Vielzahl von Effekten zu erzielen.  
  
 Die folgende Abbildung zeigt ein Rechteck mit einem linearen Farbverlaufs Pinsel und einer Ellipse, die mit einem Pfad Farbverlaufs Pinsel gefüllt ist:  
  
 ![Ein Rechteck, das mit einem Farbverlaufs Pinsel mit einer Ellipse gefüllt ist.](./media/using-a-gradient-brush-to-fill-shapes/rectangle-ellipse-gradient-brush.png)  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Vorgehensweise: Erstellen eines linearen Farbverlaufs](how-to-create-a-linear-gradient.md)  
 Zeigt, wie ein linearer Farbverlauf mithilfe der-Klasse erstellt wird <xref:System.Drawing.Drawing2D.LinearGradientBrush> .  
  
 [Vorgehensweise: Erstellen eines linearen Pfadfarbverlaufs](how-to-create-a-path-gradient.md)  
 Beschreibt, wie ein Pfad Verlauf mithilfe der- <xref:System.Drawing.Drawing2D.PathGradientBrush> Klasse erstellt wird.  
  
 [Vorgehensweise: Anwenden der Gammakorrektur bei einem Farbverlauf](how-to-apply-gamma-correction-to-a-gradient.md)  
 Erläutert, wie die Gammakorrektur mit einem Farbverlaufs Pinsel verwendet wird.  
  
## <a name="reference"></a>Verweis  
 <xref:System.Drawing.Drawing2D.LinearGradientBrush?displayProperty=nameWithType>  
 Enthält eine Beschreibung dieser Klasse und enthält Links zu allen Membern.  
  
 <xref:System.Drawing.Drawing2D.PathGradientBrush?displayProperty=nameWithType>  
 Enthält eine Beschreibung dieser Klasse und enthält Links zu allen Membern.
