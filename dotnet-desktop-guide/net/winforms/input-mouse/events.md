---
title: Verwenden von Mausereignissen
description: Hier erhalten Sie einen Überblick über Mausereignisse zum Verarbeiten von Mauseingaben. Jedes Ereignis kann dazugehörige Daten bereitstellen. Dieser Artikel enthält eine Liste dieser Mausereignisse.
ms.date: 10/26/2020
ms.topic: conceptual
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Click event [Windows Forms]
- mouse [Windows Forms], mouse events
- Click event
- MouseClick event
- DoubleClick event
- MouseDown event
- MouseEnter event
- MouseHover event
- MouseLeave event
- MouseMove event
- MouseUp event
- MouseWheel event
- mouse events
- events [Windows Forms], mouse
ms.openlocfilehash: 84d3fc0ef8bca25defead65590d1e50369e628b4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942034"
---
# <a name="using-mouse-events-windows-forms-net"></a>Verwenden von Mausereignissen (Windows Forms .NET)

Die meisten Windows Forms-Programme verarbeiten Mauseingaben, indem sie Mausereignisse verarbeiten. Dieser Artikel enthält eine Übersicht über die Mausereignisse, einschließlich Details dazu, wann jedes Ereignis verwendet wird sowie zu den Daten, die für jedes Ereignis übergeben werden. Weitere Informationen zu Ereignissen im Allgemeinen finden Sie unter [Übersicht zu Ereignissen (Windows Forms .NET)](../forms/events.md).

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="mouse-events"></a>Mausereignisse

Die Hauptmöglichkeit, auf Mauseingaben zu reagieren, ist die Verarbeitung von Mausereignissen. In der folgenden Tabelle finden Sie Mausereignisse sowie eine Erklärung dazu, wann ein jeweiliges Ereignis auftritt.

| Mausereignis                                          | BESCHREIBUNG                                             |
|------------------------------------------------------|---------------------------------------------------------|
| <xref:System.Windows.Forms.Control.Click>            | Dieses Ereignis tritt auf, wenn die Maustaste losgelassen wird, in der Regel vor dem <xref:System.Windows.Forms.Control.MouseUp>-Ereignis. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.EventArgs>. Verarbeiten Sie dieses Ereignis, wenn Sie nur bestimmen müssen, wann ein Klick auftritt.                                                                             |
| <xref:System.Windows.Forms.Control.MouseClick>       | Dieses Ereignis tritt ein, wenn der Benutzer mit der Maus auf das Steuerelement klickt. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.MouseEventArgs>. Verarbeiten Sie dieses Ereignis, wenn Sie Informationen zur Maus erhalten möchten, wenn ein Klick auftritt.                                                                                                   |
| <xref:System.Windows.Forms.Control.DoubleClick>      | Dieses Ereignis tritt beim Doppelklicken auf das Steuerelement ein. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.EventArgs>. Verarbeiten Sie dieses Ereignis, wenn Sie nur bestimmen müssen, wann ein Doppelklick auftritt.                                                                                                                                             |
| <xref:System.Windows.Forms.Control.MouseDoubleClick> | Dieses Ereignis tritt ein, wenn der Benutzer mit der Maus auf das Steuerelement doppelklickt. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.MouseEventArgs>. Verarbeiten Sie dieses Ereignis, wenn Sie Informationen zur Maus erhalten möchten, wenn ein Doppelklick auftritt.                                                                                     |
| <xref:System.Windows.Forms.Control.MouseDown>        | Dieser Ereignis tritt ein, wenn sich der Mauszeiger über dem Steuerelement befindet und der Benutzer eine Maustaste drückt. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.MouseEventArgs>.                                                                                                                                                            |
| <xref:System.Windows.Forms.Control.MouseEnter>       | Dieses Ereignis tritt je nach Art des Steuerelements auf, wenn der Mauszeiger die Grenze oder den Clientbereich des Steuerelements überschreitet. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.EventArgs>.                                                                                                                                                     |
| <xref:System.Windows.Forms.Control.MouseHover>       | Dieses Ereignis tritt auf, wenn der Mauszeiger angehalten wird und über dem Steuerelement verbleibt. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.EventArgs>.                                                                                                                                                                                                      |
| <xref:System.Windows.Forms.Control.MouseLeave>       | Dieses Ereignis tritt je nach Typ des Steuerelements auf, wenn der Mauszeiger die Grenzen oder den Clientbereich eines Steuerelements verlässt. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.EventArgs>.                                                                                                                                                 |
| <xref:System.Windows.Forms.Control.MouseMove>        | Dieses Ereignis tritt auf, wenn der Mauszeiger bewegt wird, während er sich über einem Steuerelement befindet. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.MouseEventArgs>.                                                                                                                                                                                   |
| <xref:System.Windows.Forms.Control.MouseUp>          | Dieses Ereignis tritt ein, wenn sich der Mauszeiger über dem Steuerelement befindet und der Benutzer eine Maustaste loslässt. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.MouseEventArgs>.                                                                                                                                                           |
| <xref:System.Windows.Forms.Control.MouseWheel>       | Dieses Ereignis tritt auf, wenn der Benutzer das Mausrad dreht, während der Fokus auf dem Steuerelement liegt. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.MouseEventArgs>. Sie können die <xref:System.Windows.Forms.MouseEventArgs.Delta%2A>-Eigenschaft von <xref:System.Windows.Forms.MouseEventArgs> verwenden, um zu bestimmen, wie weit die Maus gescrollt wurde. |

## <a name="mouse-information"></a>Mausinformationen

Ein <xref:System.Windows.Forms.MouseEventArgs> wird an Handler von Mausereignissen gesendet, die beim Drücken einer Maustaste und Verfolgen von Mausbewegungen ausgelöst werden. <xref:System.Windows.Forms.MouseEventArgs> enthält Informationen zum aktuellen Zustand der Maus, z. B. die Position des Mauszeigers in Clientkoordinaten, welche Maustasten gedrückt werden und ob das Mausrad bewegt wurde. Zahlreiche Mausereignisse, beispielsweise Ereignisse, die ausgelöst werden, wenn der Mauszeiger die Grenzen eines Steuerelements überschritten oder verlassen hat, senden eine <xref:System.EventArgs>-Klasse ohne weitere Informationen an den Ereignishandler.

Wenn Sie den aktuellen Zustand der Maustasten oder die Position des Mauszeigers erfahren möchten, ohne ein Mausereignis zu behandeln, können Sie auch die <xref:System.Windows.Forms.Control.MouseButtons%2A>-Eigenschaft und die <xref:System.Windows.Forms.Control.MousePosition%2A>-Eigenschaft der <xref:System.Windows.Forms.Control>-Klasse verwenden. <xref:System.Windows.Forms.Control.MouseButtons%2A> gibt Informationen darüber zurück, welche Maustasten aktuell gedrückt werden. <xref:System.Windows.Forms.Control.MousePosition%2A> gibt die Bildschirmkoordinaten des Mauszeigers zurück, was dem von <xref:System.Windows.Forms.Cursor.Position%2A> zurückgegebenen Wert entspricht.

## <a name="converting-between-screen-and-client-coordinates"></a>Konvertieren zwischen Bildschirm- und Clientkoordinaten

Da einige Mauspositionsinformationen in Clientkoordinaten und einige in Bildschirmkoordinaten vorhanden sind, müssen Sie möglicherweise einen Punkt aus einem Koordinatensystem in das andere Koordinatensystem konvertieren. Eine einfache Möglichkeit hierzu bieten die <xref:System.Windows.Forms.Control.PointToClient%2A>-Methode und die <xref:System.Windows.Forms.Control.PointToScreen%2A>-Methode der <xref:System.Windows.Forms.Control>-Klasse.

## <a name="standard-click-event-behavior"></a>Standardverhalten bei Mausklickereignissen

Wenn Sie Mausklickereignisse in der richtigen Reihenfolge behandeln möchten, müssen Sie die Reihenfolge kennen, in der Mausklickereignisse in Windows Forms-Steuerelementen ausgelöst werden. Wenn eine unterstützte Maustaste gedrückt und wieder losgelassen wird, lösen alle Windows Forms-Steuerelemente Mausklickereignisse in derselben Reihenfolge aus. Ausnahmen für einzelne Steuerelemente sind in der folgenden Liste aufgeführt. In der folgenden Liste ist die Reihenfolge der Ereignisse aufgeführt, die bei einem einzelnen Mausklick ausgelöst werden:

01. <xref:System.Windows.Forms.Control.MouseDown> -Ereignis.
01. <xref:System.Windows.Forms.Control.Click> -Ereignis.
01. <xref:System.Windows.Forms.Control.MouseClick> -Ereignis.
01. <xref:System.Windows.Forms.Control.MouseUp> -Ereignis.

In der folgenden Liste ist die Reihenfolge der Ereignisse aufgeführt, die bei einem Doppelklick mit der Maus ausgelöst werden:

01. <xref:System.Windows.Forms.Control.MouseDown> -Ereignis.
01. <xref:System.Windows.Forms.Control.Click> -Ereignis.
01. <xref:System.Windows.Forms.Control.MouseClick> -Ereignis.
01. <xref:System.Windows.Forms.Control.MouseUp> -Ereignis.
01. <xref:System.Windows.Forms.Control.MouseDown> -Ereignis.
01. <xref:System.Windows.Forms.Control.DoubleClick> -Ereignis.

    Dies kann abhängig davon variieren, ob für das betreffende Steuerelement das <xref:System.Windows.Forms.ControlStyles.StandardDoubleClick>-Stilbit auf `true` festgelegt ist. Weitere Informationen zum Festlegen eines <xref:System.Windows.Forms.ControlStyles>-Bits finden Sie unter der <xref:System.Windows.Forms.Control.SetStyle%2A>-Methode.

01. <xref:System.Windows.Forms.Control.MouseDoubleClick> -Ereignis.
01. <xref:System.Windows.Forms.Control.MouseUp> -Ereignis.

### <a name="individual-controls"></a>Einzelne Steuerelemente

Die folgenden Steuerelemente weisen nicht das Standardverhalten bei Mausklickereignissen auf:

- <xref:System.Windows.Forms.Button>
- <xref:System.Windows.Forms.CheckBox>
- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.RadioButton>

  > [!NOTE]
  > Für das <xref:System.Windows.Forms.ComboBox>-Steuerelement tritt das im Folgenden beschriebene Verhalten auf, wenn der Benutzer auf das Bearbeitungsfeld, die Schaltfläche oder ein Element in der Liste klickt.

  - **Klick mit der linken Maustaste:** <xref:System.Windows.Forms.Control.Click>, <xref:System.Windows.Forms.Control.MouseClick>
  - **Klick mit der rechten Maustaste:** Es werden keine Klickereignisse ausgelöst.
  - **Doppelklick mit der linken Maustaste:** <xref:System.Windows.Forms.Control.Click>, <xref:System.Windows.Forms.Control.MouseClick>, <xref:System.Windows.Forms.Control.Click>, <xref:System.Windows.Forms.Control.MouseClick>
  - **Doppelklick mit der rechten Maustaste:** Es werden keine Klickereignisse ausgelöst.

- <xref:System.Windows.Forms.TextBox>-Steuerelement, <xref:System.Windows.Forms.RichTextBox>-Steuerelement, <xref:System.Windows.Forms.ListBox>-Steuerelement, <xref:System.Windows.Forms.MaskedTextBox>-Steuerelement und <xref:System.Windows.Forms.CheckedListBox>-Steuerelement

  > [!NOTE]
  > Das im Folgenden beschriebene Verhalten tritt auf, wenn der Benutzer innerhalb dieser Steuerelemente auf eine beliebige Stelle klickt.

  - **Klick mit der linken Maustaste:** <xref:System.Windows.Forms.Control.Click>, <xref:System.Windows.Forms.Control.MouseClick>
  - **Klick mit der rechten Maustaste:** Es werden keine Klickereignisse ausgelöst.
  - **Doppelklick mit der linken Maustaste:** <xref:System.Windows.Forms.Control.Click>, <xref:System.Windows.Forms.Control.MouseClick>, <xref:System.Windows.Forms.Control.DoubleClick>, <xref:System.Windows.Forms.Control.MouseDoubleClick>
  - **Doppelklick mit der rechten Maustaste:** Es werden keine Klickereignisse ausgelöst.

- <xref:System.Windows.Forms.ListView>-Steuerelement

  > [!NOTE]
  > Das im Folgenden beschriebene Verhalten tritt nur auf, wenn der Benutzer auf die Elemente im <xref:System.Windows.Forms.ListView>-Steuerelement klickt. Wenn der Benutzer im Steuerelement auf eine andere Stelle klickt, werden keine Ereignisse ausgelöst. Neben den weiter unten beschriebenen Ereignissen könnten auch das <xref:System.Windows.Forms.ListView.BeforeLabelEdit>-Ereignis und das <xref:System.Windows.Forms.ListView.AfterLabelEdit>-Ereignis für Sie von Interesse sein, wenn Sie eine Validierung mit dem <xref:System.Windows.Forms.ListView>-Steuerelement durchführen möchten.

  - **Klick mit der linken Maustaste:** <xref:System.Windows.Forms.Control.Click>, <xref:System.Windows.Forms.Control.MouseClick>
  - **Klick mit der rechten Maustaste:** <xref:System.Windows.Forms.Control.Click>, <xref:System.Windows.Forms.Control.MouseClick>
  - **Doppelklick mit der linken Maustaste:** <xref:System.Windows.Forms.Control.Click>, <xref:System.Windows.Forms.Control.MouseClick>, <xref:System.Windows.Forms.Control.DoubleClick>, <xref:System.Windows.Forms.Control.MouseDoubleClick>
  - **Doppelklick mit der rechten Maustaste:** <xref:System.Windows.Forms.Control.Click>, <xref:System.Windows.Forms.Control.MouseClick>, <xref:System.Windows.Forms.Control.DoubleClick>, <xref:System.Windows.Forms.Control.MouseDoubleClick>

- <xref:System.Windows.Forms.TreeView>-Steuerelement

  > [!NOTE]
  > Das im Folgenden beschriebene Verhalten tritt nur auf, wenn der Benutzer im <xref:System.Windows.Forms.TreeView>-Steuerelement auf die Elemente selbst oder rechts neben sie klickt. Wenn der Benutzer im Steuerelement auf eine andere Stelle klickt, werden keine Ereignisse ausgelöst. Neben den weiter unten beschriebenen Ereignissen könnten auch die Ereignisse <xref:System.Windows.Forms.TreeView.BeforeCheck>, <xref:System.Windows.Forms.TreeView.BeforeSelect>, <xref:System.Windows.Forms.TreeView.BeforeLabelEdit>, <xref:System.Windows.Forms.TreeView.AfterSelect>, <xref:System.Windows.Forms.TreeView.AfterCheck> und <xref:System.Windows.Forms.TreeView.AfterLabelEdit> für Sie von Interesse sein, wenn Sie eine Validierung mit dem <xref:System.Windows.Forms.TreeView>-Steuerelement durchführen möchten.

  - **Klick mit der linken Maustaste:** <xref:System.Windows.Forms.Control.Click>, <xref:System.Windows.Forms.Control.MouseClick>
  - **Klick mit der rechten Maustaste:** <xref:System.Windows.Forms.Control.Click>, <xref:System.Windows.Forms.Control.MouseClick>
  - **Doppelklick mit der linken Maustaste:** <xref:System.Windows.Forms.Control.Click>, <xref:System.Windows.Forms.Control.MouseClick>, <xref:System.Windows.Forms.Control.DoubleClick>, <xref:System.Windows.Forms.Control.MouseDoubleClick>
  - **Doppelklick mit der rechten Maustaste:** <xref:System.Windows.Forms.Control.Click>, <xref:System.Windows.Forms.Control.MouseClick>, <xref:System.Windows.Forms.Control.DoubleClick>, <xref:System.Windows.Forms.Control.MouseDoubleClick>

## <a name="painting-behavior-of-toggle-controls"></a>Zeichnungsverhalten umschaltbarer Steuerelemente

Umschaltbare Steuerelemente, wie die Steuerelemente, die von der <xref:System.Windows.Forms.ButtonBase>-Klasse abgeleitet werden, weisen bei Mausklickereignissen das folgende Zeichnungsverhalten auf:

01. Der Benutzer drückt die Maustaste.
01. Das Steuerelement zeichnet im gedrückten Zustand.
01. Das <xref:System.Windows.Forms.Control.MouseDown>-Ereignis wird ausgelöst.
01. Der Benutzer lässt die Maustaste los.
01. Das Steuerelement zeichnet im erhöhten Zustand.
01. Das <xref:System.Windows.Forms.Control.Click>-Ereignis wird ausgelöst.
01. Das <xref:System.Windows.Forms.Control.MouseClick>-Ereignis wird ausgelöst.
01. Das <xref:System.Windows.Forms.Control.MouseUp>-Ereignis wird ausgelöst.

    > [!NOTE]
    > Wenn der Benutzer den Mauszeiger bei gedrückter Maustaste aus dem umschaltbaren Steuerelement bewegt (z. B. wenn er die Maus bei gedrückter Maustaste vom <xref:System.Windows.Forms.Button>-Steuerelement weg bewegt), zeichnet das umschaltbare Steuerelement im erhöhten Zustand, und es tritt nur das <xref:System.Windows.Forms.Control.MouseUp>-Ereignis auf. Das <xref:System.Windows.Forms.Control.Click>-Ereignis oder das <xref:System.Windows.Forms.Control.MouseClick>-Ereignis tritt in dieser Situation nicht auf.

## <a name="see-also"></a>Siehe auch

- [Übersicht über die Mausverwendung (Windows Forms .NET)](overview.md)
- [Verwalten von Mauszeigern (Windows Forms .NET)](how-to-manage-cursor-pointer.md)
- [Simulieren von Mausereignissen (Windows Forms .NET)](how-to-simulate-events.md)
- <xref:System.Windows.Forms.Control?displayProperty=nameWithType>
