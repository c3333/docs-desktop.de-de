---
title: Unterscheiden zwischen Klicks und Doppelklicks
description: Hier werden verschiedene Möglichkeiten beschrieben, um mit einem Steuerelement oder einem Formular für Windows Forms für .NET den Unterschied zwischen einem einfachen Klick und einem Doppelklick zu erkennen.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- mouse [Windows Forms], click
- mouse [Windows Forms], double-click
- mouse clicks [Windows Forms], single versus double
ms.openlocfilehash: 7b58896a85ffd16ae2637b94d58845ed7a721c4d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942036"
---
# <a name="how-to-distinguish-between-clicks-and-double-clicks-windows-forms-net"></a>Unterscheiden zwischen Klicks und Doppelklicks (Windows Forms .NET)

In der Regel wird mit einem einzigen *Klick* eine Benutzerschnittstellenaktion initiiert, und mit einem *Doppelklick* wird die Aktion erweitert. So wird mit einem einzigen Klick ein Element markiert, und mit einem Doppelklick wird das ausgewählte Element bearbeitet. Allerdings lassen sich die Windows Forms-Klickereignisse nicht so einfach an ein Szenario anpassen, in dem ein Klick und ein Doppelklick inkompatible Aktionen ausführen, da eine Aktion, die mit dem <xref:System.Windows.Forms.Control.Click>- oder <xref:System.Windows.Forms.Control.MouseClick>-Ereignis verknüpft ist, ausgeführt wird, bevor die mit dem <xref:System.Windows.Forms.Control.DoubleClick>- oder <xref:System.Windows.Forms.Control.MouseDoubleClick>-Ereignis verknüpfte Aktion ausgeführt wird. In diesem Thema werden zwei Lösungen für dieses Problem erörtert.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

Eine Lösung besteht darin, das Doppelklickereignis zu behandeln und ein Rollback der Aktionen in der Behandlung des Klickereignisses zu initiieren. In selten Fällen müssen Sie ggf. das Klick- und Doppelklickverhalten simulieren, indem Sie das <xref:System.Windows.Forms.Control.MouseDown>-Ereignis behandeln und dabei die Eigenschaften <xref:System.Windows.Forms.SystemInformation.DoubleClickTime%2A> und <xref:System.Windows.Forms.SystemInformation.DoubleClickSize%2A> der <xref:System.Windows.Forms.SystemInformation>-Klasse verwenden. Sie messen die Zeit zwischen den Klicks, und wenn ein zweiter Klick erfolgt, bevor der Wert von <xref:System.Windows.Forms.SystemInformation.DoubleClickTime%2A> erreicht wurde und der Klick innerhalb des von <xref:System.Windows.Forms.SystemInformation.DoubleClickSize%2A> definierten Rechtecks erfolgt ist, führen Sie die Doppelklickaktion aus, andernfalls führen Sie die Klickaktion aus.

## <a name="to-roll-back-a-click-action"></a>So führen Sie ein Rollback einer Klickaktion durch

Vergewissern Sie sich, dass das Steuerelement, mit dem Sie arbeiten, über das standardmäßig Doppelklickverhalten verfügt. Andernfalls aktivieren Sie das Steuerelement mit der <xref:System.Windows.Forms.Control.SetStyle%2A>-Methode. Behandeln Sie das Doppelklickereignis, und führen Sie ein Rollback der Klickaktion und der Doppelklickaktion durch. Im folgenden Codebeispiel wird gezeigt, wie eine benutzerdefinierte Schaltfläche mit aktiviertem Doppelklick erstellt und wie ein Rollback der Klickaktion im Behandlungscode des Doppelklickereignisses initiiert wird.

In diesem Codebeispiel wird ein neues Schaltflächen-Steuerelement verwendet, das Doppelklicks ermöglicht:

:::code language="csharp" source="snippets/how-to-distinguish-between-clicks-and-double-clicks/csharp/DoubleClickButton.cs" id="DoubleClickButton":::
:::code language="vb" source="snippets/how-to-distinguish-between-clicks-and-double-clicks/vb/DoubleClickButton.vb" id="DoubleClickButton":::

Der folgende Code veranschaulicht, wie ein Formular die Rahmenart des neuen Schaltflächen-Steuerelements basierend auf einem Klick oder Doppelklick ändert:

:::code language="csharp" source="snippets/how-to-distinguish-between-clicks-and-double-clicks/csharp/Form1.cs" id="RollbackForm":::
:::code language="vb" source="snippets/how-to-distinguish-between-clicks-and-double-clicks/vb/Form1.vb" id="RollbackForm":::

## <a name="to-distinguish-between-clicks"></a>Unterscheiden zwischen Klicks

Verarbeiten Sie das <xref:System.Windows.Forms.Control.MouseDown>-Ereignis, und ermitteln Sie mit der <xref:System.Windows.Forms.SystemInformation>-Eigenschaft und einer <xref:System.Windows.Forms.Timer>-Komponente die Position und die Zeitspanne zwischen Klicks. Machen Sie die geeignete Aktion davon abhängig, ob ein Klick oder ein Doppelklick stattfindet. Das folgende Codebeispiel veranschaulicht, wie Sie dabei vorgehen.

:::code language="csharp" source="snippets/how-to-distinguish-between-clicks-and-double-clicks/csharp/Form2.cs":::
:::code language="vb" source="snippets/how-to-distinguish-between-clicks-and-double-clicks/vb/Form2.vb":::

## <a name="see-also"></a>Siehe auch

- [Übersicht über die Mausverwendung (Windows Forms .NET)](overview.md)
- [Verwenden von Mausereignissen (Windows Forms .NET)](events.md)
- [Verwalten von Mauszeigern (Windows Forms .NET)](how-to-manage-cursor-pointer.md)
- [Simulieren von Mausereignissen (Windows Forms .NET)](how-to-simulate-events.md)
- <xref:System.Windows.Forms.Control.Click?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.MouseDown?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.SetStyle%2A?displayProperty=nameWithType>
