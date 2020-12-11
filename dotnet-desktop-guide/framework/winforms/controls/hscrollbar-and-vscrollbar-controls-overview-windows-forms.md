---
title: Übersicht über das HScrollBar-Steuerelement und das VScrollBar-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- HScrollBar
- VScrollBar
helpviewer_keywords:
- ScrollBar control [Windows Forms]
- HScrollBar control [Windows Forms], about HScrollBar
- VScrollBar control [Windows Forms], about VScrollBar control
- ScrollBar control [Windows Forms], about ScrollBar control
- scroll bars [Windows Forms], about scroll bars
ms.assetid: 8b307679-1cae-41d8-99aa-3d1efd207cd6
ms.openlocfilehash: abe0c8da9723f17cb80715454f6ab7297724a21f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976738"
---
# <a name="hscrollbar-and-vscrollbar-controls-overview-windows-forms"></a>Übersicht über das HScrollBar-Steuerelement und das VScrollBar-Steuerelement (Windows Forms)
Windows Forms Steuer <xref:System.Windows.Forms.ScrollBar> Elemente werden verwendet, um eine einfache Navigation durch eine lange Liste von Elementen oder eine große Menge an Informationen zu ermöglichen, indem Sie in einer Anwendung oder einem Steuerelement entweder horizontal oder vertikal scrollen. Scrollleisten sind ein gängiges Element der Windows-Benutzeroberfläche, sodass das <xref:System.Windows.Forms.ScrollBar> Steuerelement häufig mit Steuerelementen verwendet wird, die nicht von der-Klasse abgeleitet werden <xref:System.Windows.Forms.ScrollableControl> . Ebenso entscheiden sich viele Entwickler <xref:System.Windows.Forms.ScrollBar> beim Erstellen Ihrer eigenen Benutzer Steuerelemente für das Steuerelement.  
  
 Die <xref:System.Windows.Forms.HScrollBar> (horizontalen) und <xref:System.Windows.Forms.VScrollBar> (vertikalen) Steuerelemente agieren unabhängig von anderen Steuerelementen und verfügen über einen eigenen Satz von Ereignissen, Eigenschaften und Methoden. <xref:System.Windows.Forms.ScrollBar> Steuerelemente sind nicht identisch mit den integrierten Bild Lauf leisten, die an Textfelder, Listenfelder, Kombinations Felder oder MDI-Formulare angefügt sind. (das <xref:System.Windows.Forms.TextBox> Steuerelement verfügt über eine- <xref:System.Windows.Forms.TextBox.ScrollBars%2A> Eigenschaft zum Anzeigen oder Ausblenden von Bild Lauf leisten, die an das Steuerelement angefügt sind.)  
  
 Die Steuer <xref:System.Windows.Forms.ScrollBar> Elemente verwenden das- <xref:System.Windows.Forms.ScrollBar.Scroll> Ereignis, um die Bewegung des Bild Lauf Felds (manchmal auch als Ziehpunkt bezeichnet) entlang der Bild Lauf Leiste zu überwachen. Die Verwendung des- <xref:System.Windows.Forms.ScrollBar.Scroll> Ereignisses ermöglicht den Zugriff auf den ScrollBar-Wert, während er gezogen wird.  
  
## <a name="value-property"></a>Value-Eigenschaft  
 Die- <xref:System.Windows.Forms.ScrollBar.Value%2A> Eigenschaft (standardmäßig 0) ist ein Wert, der `integer` der Position des Bild Lauf Felds auf der Bild Lauf Leiste entspricht. Wenn die Position des Bild Lauf Felds den Minimalwert hat, wechselt es zur äußersten linken Position (bei horizontalen Schiebe leisten) oder zur obersten Position (bei vertikalen Schiebe leisten). Wenn das Bild Lauf Feld den maximalen Wert hat, wechselt das Bild Lauf Feld nach rechts oder unten. Entsprechend wird ein Wert, der sich in der Mitte zwischen dem unteren und oberen Bereich des Bereichs befand, in der Mitte der Bild Lauf Leiste den führenden Rand des Bild Lauf Felds platziert.  
  
 Zusätzlich zur Verwendung von Mausklicks zum Ändern des Bild Lauf leisten Werts kann ein Benutzer auch das Bild Lauf Feld an einen beliebigen Punkt entlang der Leiste ziehen. Der resultierende Wert hängt von der Position des Bild Lauf Felds ab, liegt jedoch immer innerhalb des Bereichs der <xref:System.Windows.Forms.ScrollBar.Minimum%2A> <xref:System.Windows.Forms.ScrollBar.Maximum%2A> vom Benutzer festgelegten Eigenschaften.  
  
## <a name="largechange-and-smallchange-properties"></a>LargeChange-und SmallChange-Eigenschaften  
 Wenn der Benutzer die Bild-auf-oder Bild-ab-Taste drückt oder in der Scrollleiste auf beiden Seiten des Bild Lauf Felds klickt, wird die- <xref:System.Windows.Forms.ScrollBar.Value%2A> Eigenschaft entsprechend dem in der-Eigenschaft festgelegten Wert geändert <xref:System.Windows.Forms.ScrollBar.LargeChange%2A> .  
  
 Wenn der Benutzer eine der Pfeiltasten drückt oder auf eine der Schiebe leisten Schaltflächen klickt, wird die- <xref:System.Windows.Forms.ScrollBar.Value%2A> Eigenschaft entsprechend dem in der-Eigenschaft festgelegten Wert geändert <xref:System.Windows.Forms.ScrollBar.SmallChange%2A> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.HScrollBar>
- <xref:System.Windows.Forms.VScrollBar>
- [Steuerelemente für Windows Forms](controls-to-use-on-windows-forms.md)
