---
title: Verwenden von Schriftarten und Text
ms.date: 03/30/2017
helpviewer_keywords:
- GDI [Windows Forms], drawing text [Windows Forms]
- text [Windows Forms], drawing in Windows Forms
- examples [Windows Forms], fonts and text
- fonts [Windows Forms], using in Windows Forms
- strings [Windows Forms], drawing in Windows Forms
ms.assetid: d43640f3-da94-4df2-a29d-a9d021a1c069
ms.openlocfilehash: 73a4af5fe7367e777fcb83af8c84c09be91e5b1e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976045"
---
# <a name="using-fonts-and-text"></a>Verwenden von Schriftarten und Text
Es gibt mehrere Klassen, die von GDI+ und GDI zum Zeichnen von Text auf Windows Forms angeboten werden. Die GDI+- <xref:System.Drawing.Graphics> Klasse verfügt über mehrere <xref:System.Drawing.Graphics.DrawString%2A> Methoden, mit denen Sie verschiedene Funktionen von Text, z. b. Speicherort, umgebenden Rechteck, Schriftart und Format, angeben können. Außerdem können Sie mithilfe der statischen <xref:System.Windows.Forms.TextRenderer.DrawText%2A> -und-Methoden, die <xref:System.Windows.Forms.TextRenderer.MeasureText%2A> von der-Klasse angeboten werden, Text mit GDI Zeichnen und Messen `TextRenderer` . Mit den GDI-Methoden können Sie auch den Speicherort, die Schriftart und das Format angeben. Sie können entweder GDI oder GDI+ für Text Rendering auswählen. GDI bietet jedoch im Allgemeinen eine bessere Leistung und eine genauere Text Messung. Weitere Klassen, die zum Text Rendering beitragen `FontFamily` , sind, `Font` , <xref:System.Drawing.StringFormat> und `TextFormatFlags` .  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Vorgehensweise: Erstellen von Schriftartfamilien und Schriftarten](how-to-construct-font-families-and-fonts.md)  
 Zeigt, wie `Font` -Objekte und-Objekte erstellt werden `FontFamily` .  
  
 [Vorgehensweise: Zeichnen von Text an einer angegebenen Position](how-to-draw-text-at-a-specified-location.md)  
 Beschreibt das Zeichnen von Text an einem bestimmten Speicherort mithilfe von GDI+ und GDI.  
  
 [Vorgehensweise: Zeichnen von umbrochenem Text in einem Rechteck](how-to-draw-wrapped-text-in-a-rectangle.md)  
 Erläutert das Zeichnen von Text in einem Rechteck mithilfe von GDI+ und GDI.  
  
 [Vorgehensweise: Zeichnen von Text mit GDI](how-to-draw-text-with-gdi.md)  
 Veranschaulicht, wie GDI zum Zeichnen von Text verwendet wird.  
  
 [Vorgehensweise: Ausrichten von gezeichnetem Text](how-to-align-drawn-text.md)  
 Zeigt, wie Sie GDI+-und GDI-Text formatieren.  
  
 [Vorgehensweise: Erstellen von vertikalem Text](how-to-create-vertical-text.md)  
 Beschreibt, wie vertikal ausgerichteten Text mit GDI+ gezeichnet wird.  
  
 [Vorgehensweise: Festlegen von Tabstopps in gezeichnetem Text](how-to-set-tab-stops-in-drawn-text.md)  
 Zeigt, wie Text mit Tabstopps mit GDI+ gezeichnet wird.  
  
 [Vorgehensweise: Auflisten installierter Schriftarten](how-to-enumerate-installed-fonts.md)  
 Erläutert, wie Sie die Namen der installierten Schriftarten auflisten.  
  
 [Vorgehensweise: Erstellen einer privaten Schriftartenauflistung](how-to-create-a-private-font-collection.md)  
 Beschreibt, wie ein- <xref:System.Drawing.Text.PrivateFontCollection> Objekt erstellt wird.  
  
 [Vorgehensweise: Abrufen von Schriftarteigenschaften](how-to-obtain-font-metrics.md)  
 Zeigt, wie Sie Schriftart Metriken wie z. b. den Zellen Aufstieg und den Abstieg abrufen  
  
 [Vorgehensweise: Verwenden der Bildkantenglättung mit Text](how-to-use-antialiasing-with-text.md)  
 Erläutert, wie Antialiasing beim Zeichnen von Text verwendet wird.  
  
## <a name="reference"></a>Verweis  
 <xref:System.Drawing.Font>  
 Beschreibt diese Klasse und enthält Links zu allen Membern.  
  
 <xref:System.Drawing.FontFamily>  
 Beschreibt diese Klasse und enthält Links zu allen Membern.  
  
 <xref:System.Drawing.Text.PrivateFontCollection>  
 Beschreibt diese Klasse und enthält Links zu allen Membern.  
  
 <xref:System.Windows.Forms.TextRenderer>  
 Beschreibt diese Klasse und enthält Links zu allen Membern.  
  
 <xref:System.Windows.Forms.TextFormatFlags>  
 Beschreibt diese Klasse und enthält Links zu allen Membern.
