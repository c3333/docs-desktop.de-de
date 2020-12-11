---
title: Übersicht über das ProgressBar-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- ProgressBar
helpviewer_keywords:
- ProgressBar control [Windows Forms], about ProgressBar control
- progress controls [Windows Forms], about progress controls
ms.assetid: a05d9cba-3a6a-4f8f-94b8-8ec12799fb80
ms.openlocfilehash: a0c4a0401d06614ab3ad148b932ebc64080c592c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972344"
---
# <a name="progressbar-control-overview-windows-forms"></a>Übersicht über das ProgressBar-Steuerelement (Windows Forms)
> [!IMPORTANT]
> Obwohl das <xref:System.Windows.Forms.ToolStripProgressBar>-Steuerelement das <xref:System.Windows.Forms.ProgressBar>-Steuerelement ersetzt und funktionell erweitert, wird das <xref:System.Windows.Forms.ProgressBar>-Steuerelement sowohl aus Gründen der Abwärtskompatibilität als auch, falls gewünscht, für die zukünftige Verwendung beibehalten.  
  
 Das Windows Forms- <xref:System.Windows.Forms.ProgressBar> Steuerelement gibt den Fortschritt eines Prozesses an, indem eine entsprechende Anzahl von Rechtecke in einem horizontalen Balken angezeigt wird. Wenn der Prozess vollständig ist, wird der Balken ausgefüllt. Status anzeigen werden häufig verwendet, um dem Benutzer eine Vorstellung davon zu verschaffen, wie lange auf den Abschluss eines Prozesses gewartet werden soll. zum Beispiel beim Laden einer großen Datei.  
  
> [!NOTE]
> Das <xref:System.Windows.Forms.ProgressBar> Steuerelement kann nur horizontal auf dem Formular ausgerichtet werden.  
  
## <a name="key-properties-and-methods"></a>Schlüsseleigenschaften und-Methoden  
 Die Schlüsseleigenschaften des <xref:System.Windows.Forms.ProgressBar> -Steuer Elements sind <xref:System.Windows.Forms.ProgressBar.Value%2A> , <xref:System.Windows.Forms.ProgressBar.Minimum%2A> und <xref:System.Windows.Forms.ProgressBar.Maximum%2A> . Die <xref:System.Windows.Forms.ProgressBar.Minimum%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Forms.ProgressBar.Maximum%2A> legen die maximalen und minimalen Werte fest, die die Statusanzeige anzeigen kann. Die- <xref:System.Windows.Forms.ProgressBar.Value%2A> Eigenschaft stellt den Fortschritt dar, der zum Abschließen des Vorgangs durchgeführt wurde. Da der im-Steuerelement angezeigte Balken aus-Blöcken besteht, wird der Wert, der vom-Steuerelement angezeigt wird, <xref:System.Windows.Forms.ProgressBar> nur dem <xref:System.Windows.Forms.ProgressBar.Value%2A> aktuellen Wert der Eigenschaft entspricht. Basierend auf der Größe des <xref:System.Windows.Forms.ProgressBar> Steuer Elements bestimmt die- <xref:System.Windows.Forms.ProgressBar.Value%2A> Eigenschaft, wann der nächste Block angezeigt werden soll.  
  
 Die gängigste Methode zum Aktualisieren des aktuellen Fortschritts Werts ist das Schreiben von Code, um die-Eigenschaft festzulegen <xref:System.Windows.Forms.ProgressBar.Value%2A> . Im Beispiel für das Laden einer großen Datei können Sie die maximale Größe der Datei in Kilobyte festlegen. Wenn beispielsweise die- <xref:System.Windows.Forms.ProgressBar.Maximum%2A> Eigenschaft auf 100 festgelegt ist, <xref:System.Windows.Forms.ProgressBar.Minimum%2A> wird die-Eigenschaft auf 10 festgelegt, und die- <xref:System.Windows.Forms.ProgressBar.Value%2A> Eigenschaft wird auf 50 festgelegt, 5 Rechtecke werden angezeigt. Dies ist die Hälfte der Zahl, die angezeigt werden kann.  
  
 Es gibt jedoch weitere Möglichkeiten, den Wert zu ändern, der vom <xref:System.Windows.Forms.ProgressBar> Steuerelement angezeigt wird, abgesehen von der direkten Festlegung der- <xref:System.Windows.Forms.ProgressBar.Value%2A> Eigenschaft. Die- <xref:System.Windows.Forms.ProgressBar.Step%2A> Eigenschaft kann verwendet werden, um einen Wert anzugeben, durch den die-Eigenschaft Inkrement erhöht wird <xref:System.Windows.Forms.ProgressBar.Value%2A> . Beim Aufrufen der- <xref:System.Windows.Forms.ProgressBar.PerformStep%2A> Methode wird der Wert erhöht. Um den Inkrement-Wert zu verändern, können Sie die <xref:System.Windows.Forms.ProgressBar.Increment%2A> -Methode verwenden und einen Wert angeben, mit dem die-Eigenschaft Inkrement erhöht werden soll <xref:System.Windows.Forms.ProgressBar.Value%2A> .  
  
 Ein weiteres Steuerelement, das den Benutzer grafisch über eine aktuelle Aktion informiert, ist das <xref:System.Windows.Forms.StatusBar> Steuerelement.  
  
> [!IMPORTANT]
> Das-Steuerelement und das-Steuerelement <xref:System.Windows.Forms.StatusStrip> <xref:System.Windows.Forms.ToolStripStatusLabel> ersetzen und fügen Funktionen zu den <xref:System.Windows.Forms.StatusBar> -und-Steuer <xref:System.Windows.Forms.StatusBarPanel> Elementen hinzu. die Steuerelemente <xref:System.Windows.Forms.StatusBar> und werden jedoch sowohl für die abwärts <xref:System.Windows.Forms.StatusBarPanel> Kompatibilität als auch für die zukünftige Verwendung beibehalten.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ProgressBar>
- [ProgressBar-Steuerelement](progressbar-control-windows-forms.md)
