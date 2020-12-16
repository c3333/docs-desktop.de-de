---
title: Drag & Drop-Mausverhalten
description: Hier erfahren Sie mehr über die Funktionsweise von Drag & Drop-Vorgängen im Zusammenhang mit Windows Forms, einschließlich der Ausführung von Drag & Drop-Vorgängen mit der Maus.
ms.date: 10/26/2020
ms.topic: conceptual
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drag and drop [Windows Forms], Windows Forms
- Windows Forms, drag and drop
ms.openlocfilehash: d434b0f0e80c610fffeea26a6fff44b43ca07fed
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942030"
---
# <a name="drag-and-drop-mouse-behavior-overview-windows-forms-net"></a>Übersicht über das Drag-&-Drop-Mausverhalten (Windows Forms .NET)

Windows Forms umfasst eine Reihe von Methoden, Ereignissen und Klassen, die das Drag &amp; Drop-Verhalten implementieren. Dieses Thema enthält eine Übersicht über die Drag &amp; Drop-Unterstützung in Windows Forms.<!-- TODO Also see [Drag-and-Drop Operations and Clipboard Support](./advanced/drag-and-drop-operations-and-clipboard-support.md).-->

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="drag-and-drop-events"></a>Drag & Drop-Ereignisse

Es gibt zwei Kategorien von Ereignissen in einem Drag & Drop-Vorgang: Ereignisse, die im aktuellen Ziel des Drag &amp; Drop-Vorgangs auftreten, und Ereignisse, die in der Quelle des Drag &amp; Drop-Vorgangs auftreten. Sie müssen diese Ereignisse verarbeiten, um Drag & Drop-Vorgänge auszuführen. Wenn Sie die Daten aus den Ereignisargumenten dieser Ereignisse verwenden, können Sie Drag & Drop-Vorgänge problemlos vereinfachen.

## <a name="events-on-the-current-drop-target"></a>Ereignisse im aktuellen Ablageziel

Die folgende Tabelle zeigt die Ereignisse, die im aktuellen Ziel eines Drag &amp; Drop--Vorgangs auftreten.

| Mausereignis                                   | BESCHREIBUNG                                                                                                                                                                                            |
|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <xref:System.Windows.Forms.Control.DragEnter> | Dieses Ereignis tritt auf, wenn ein Objekt in die Begrenzungen des Steuerelements gezogen wird. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.DragEventArgs>.                              |
| <xref:System.Windows.Forms.Control.DragOver>  | Dieses Ereignis tritt auf, wenn ein Objekt gezogen wird, während sich der Mauszeiger innerhalb der Grenzen des Steuerelements befindet. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.DragEventArgs>. |
| <xref:System.Windows.Forms.Control.DragDrop>  | Dieses Ereignis tritt auf, wenn ein Drag &amp; Drop-Vorgang abgeschlossen wurde. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.DragEventArgs>.                                      |
| <xref:System.Windows.Forms.Control.DragLeave> | Dieses Ereignis tritt auf, wenn ein Objekt über die Grenzen des Steuerelements nach außen gezogen wird. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.EventArgs>.                                              |

Die <xref:System.Windows.Forms.DragEventArgs>-Klasse stellt die Position des Mauszeigers, den aktuellen Zustand der Maustasten und der Zusatztasten der Tastatur, die gezogenen Daten und die <xref:System.Windows.Forms.DragDropEffects>-Werte bereit, die die Vorgänge, die für die Quelle des Ziehereignisses zulässig sind, sowie den Zielablegeeffekt für den Vorgang angeben.

## <a name="events-on-the-drop-source"></a>Ereignisse in der Ablagequelle

Die folgende Tabelle zeigt die Ereignisse, die in der Quelle eines Drag &amp; Drop-Vorgangs auftreten.

|Mausereignis|BESCHREIBUNG|
|-----------------|-----------------|
|<xref:System.Windows.Forms.Control.GiveFeedback>|Dieses Ereignis tritt während eines Ziehvorgangs auf. Es bietet die Möglichkeit, dem Benutzer einen visuellen Hinweis zu geben, dass der Drag &amp; Drop-Vorgang auftritt, z. B. Ändern des Mauszeigers. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.GiveFeedbackEventArgs>.|
|<xref:System.Windows.Forms.Control.QueryContinueDrag>|Dieses Ereignis wird während eines Drag & Drop-Vorgangs ausgelöst. Dadurch kann die Quelle des Ziehvorgangs bestimmen, ob der Drag &amp;amp; Drop-Vorgang abgebrochen werden soll. Der Handler für dieses Ereignis empfängt ein Argument des Typs <xref:System.Windows.Forms.QueryContinueDragEventArgs>.|

Die <xref:System.Windows.Forms.QueryContinueDragEventArgs>-Klasse stellt Folgendes bereit: den aktuellen Zustand der Maus und der Zusatztasten der Tastatur, einen Wert, der angibt, ob die ESC-Taste gedrückt wurde, und einen <xref:System.Windows.Forms.DragAction>-Wert, der festgelegt werden kann, um anzugeben, ob der Drag &amp; Drop-Vorgang fortgesetzt werden soll.

## <a name="performing-drag-and-drop"></a>Ausführen von Drag & Drop-Vorgängen

Drag & Drop-Vorgänge umfassen immer zwei Komponenten: die **Ziehquelle** und das **Ablageziel**. Sie müssen ein Steuerelement als Quelle festlegen und das <xref:System.Windows.Forms.Control.MouseDown>-Ereignis verarbeiten, um einen Drag & Drop-Vorgang starten zu können. Rufen Sie im Ereignishandler die <xref:System.Windows.DragDrop.DoDragDrop%2A>-Methode auf, die die Daten bereitstellt, die der Ablage und dem <xref:System.Windows.DragDropEffects>-Wert zugeordnet sind.

Legen Sie die <xref:System.Windows.Forms.Control.AllowDrop>-Eigenschaft des Zielsteuerelements auf `true` fest, damit dieses Steuerelement einen Drag & Drop-Vorgang annehmen kann. Das Ziel verarbeitet zwei Ereignisse. Zuerst wird ein Ereignis als Reaktion auf das Ziehen über das Steuerelement verarbeitet (z. B. <xref:System.Windows.Forms.Control.DragOver>). Danach wird ein zweites Ereignis verarbeitet, bei dem es sich um die Ablageaktion selbst handelt (<xref:System.Windows.Forms.Control.DragDrop>).

Das folgenden Beispiel veranschaulicht das Ziehen von einem <xref:System.Windows.Forms.Label>-Steuerelement in ein <xref:System.Windows.Forms.TextBox>. Wenn der Ziehvorgang abgeschlossen ist, antwortet das `TextBox`, indem es sich den Text der Bezeichnung selbst zuweist.

```csharp
// Initiate the drag
private void label1_MouseDown(object sender, MouseEventArgs e) =>
    DoDragDrop(((Label)sender).Text, DragDropEffects.All);

// Set the effect filter and allow the drop on this control
private void textBox1_DragOver(object sender, DragEventArgs e) =>
    e.Effect = DragDropEffects.All;

// React to the drop on this control
private void textBox1_DragDrop(object sender, DragEventArgs e) =>
    textBox1.Text = (string)e.Data.GetData(typeof(string));
```

```vb
' Initiate the drag
Private Sub Label1_MouseDown(sender As Object, e As MouseEventArgs)
    DoDragDrop(DirectCast(sender, Label).Text, DragDropEffects.All)
End Sub

' Set the effect filter and allow the drop on this control
Private Sub TextBox1_DragOver(sender As Object, e As DragEventArgs)
    e.Effect = DragDropEffects.All
End Sub

' React to the drop on this control
Private Sub TextBox1_DragDrop(sender As Object, e As DragEventArgs)
    TextBox1.Text = e.Data.GetData(GetType(String))
End Sub
```

Weitere Informationen zu den Effekten von Ziehvorgängen finden Sie unter <xref:System.Windows.Forms.DragEventArgs.Data%2A> und <xref:System.Windows.Forms.DragEventArgs.AllowedEffect%2A>.

## <a name="see-also"></a>Siehe auch

- [Übersicht über die Mausverwendung (Windows Forms .NET)](overview.md)
- <xref:System.Windows.Forms.Control.DragDrop?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.DragEnter?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.DragLeave?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.DragOver?displayProperty=nameWithType>
