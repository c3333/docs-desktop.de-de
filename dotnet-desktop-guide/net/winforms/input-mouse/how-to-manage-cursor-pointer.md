---
title: Verwalten von Mauszeigern
description: Hier erfahren Sie, wie Sie in Windows Forms für .NET auf den Mauszeiger zugreifen, ihn steuern und ihn ändern.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- pointers [Windows Forms], setting
- mouse pointers
- mouse cursors
- mouse pointers [Windows Forms], setting
- cursors [Windows Forms], setting
- mouse [Windows Forms], cursors
ms.openlocfilehash: b4439c34bf7a7f41a94ce5ec5971520d9c82e469
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942098"
---
# <a name="manage-mouse-pointers-windows-forms-net"></a>Verwalten von Mauszeigern (Windows Forms .NET)

Beim *Mauszeiger*, der manchmal auch als Cursor bezeichnet wird, handelt es sich um eine Bitmap, die einen Fokuspunkt auf dem Bildschirm für Benutzereingabe mit der Maus angibt. In diesem Thema erhalten Sie eine Übersicht über den Mauszeiger in Windows Forms. Außerdem werden einige Möglichkeiten erläutert, um den Mauszeiger zu ändern und zu steuern.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="accessing-the-mouse-pointer"></a>Zugreifen auf den Mauszeiger

Der Mauszeiger wird von der <xref:System.Windows.Forms.Cursor>-Klasse dargestellt. Jede <xref:System.Windows.Forms.Control>-Klasse verfügt über eine <xref:System.Windows.Forms.Control.Cursor%2A?displayProperty=nameWithType>-Eigenschaft, die den Zeiger für das entsprechende Steuerelement angibt. Die <xref:System.Windows.Forms.Cursor>-Klasse enthält Eigenschaften, die den Zeiger beschreiben, z. B. die Eigenschaften <xref:System.Windows.Forms.Cursor.Position%2A> und <xref:System.Windows.Forms.Cursor.HotSpot%2A>, sowie Methoden, die das Aussehen des Zeigers ändern können, z. B. die Methoden <xref:System.Windows.Forms.Cursor.Show%2A>, <xref:System.Windows.Forms.Cursor.Hide%2A> und <xref:System.Windows.Forms.Cursor.DrawStretched%2A>.

Im folgenden Beispiel wird der Cursor ausgeblendet, wenn er sich über einer Schaltfläche befindet:

:::code language="csharp" source="snippets/how-to-manage-cursor-pointer/csharp/Form1.cs" id="ShowHideCursor":::
:::code language="vb" source="snippets/how-to-manage-cursor-pointer/vb/Form1.vb" id="ShowHideCursor":::

## <a name="controlling-the-mouse-pointer"></a>Steuern des Mauszeigers

Manchmal sollten Sie den Bereich begrenzen, in dem der Mauszeiger verwendet werden kann, oder die Position der Maus ändern. Sie können die aktuelle Position der Maus mithilfe der <xref:System.Windows.Forms.Cursor.Position%2A>-Eigenschaft von <xref:System.Windows.Forms.Cursor> abrufen oder festlegen. Zusätzlich können Sie den Bereich einschränken, in dem der Mauszeiger verwendet werden kann, indem Sie die <xref:System.Windows.Forms.Cursor.Clip%2A>-Eigenschaft festlegen. Der Standardbereich, der eingeschränkt werden kann, ist die gesamte Anzeige.

Im folgenden Beispiel wird der Mauszeiger zwischen zwei Schaltflächen positioniert, wenn auf diese geklickt wird:

:::code language="csharp" source="snippets/how-to-manage-cursor-pointer/csharp/Form1.cs" id="MoveCursor":::
:::code language="vb" source="snippets/how-to-manage-cursor-pointer/vb/Form1.vb" id="MoveCursor":::

## <a name="changing-the-mouse-pointer"></a>Ändern des Mauszeigers

Das Ändern des Mauszeigers ist eine wichtige Möglichkeit, dem Benutzer Feedback zu geben. Der Mauszeiger kann beispielsweise in den Handlern der Ereignisse <xref:System.Windows.Forms.Control.MouseEnter> und <xref:System.Windows.Forms.Control.MouseLeave> geändert werden, um den Benutzer darüber zu informieren, dass Berechnungen durchgeführt werden, und um die Benutzerinteraktion im Steuerelement einzuschränken. Manchmal wird der Mauszeiger aufgrund von Systemereignissen geändert, z. B. wenn Ihre Anwendung an einem Drag & Drop-Vorgang beteiligt ist.

Die Hauptmöglichkeit, den Mauszeiger zu ändern, besteht darin, die Eigenschaft <xref:System.Windows.Forms.Control.Cursor%2A?displayProperty=nameWithType> oder <xref:System.Windows.Forms.Control.DefaultCursor%2A> eines Steuerelements auf eine neue <xref:System.Windows.Forms.Cursor>-Klasse festzulegen. Beispiele zum Ändern des Mauszeigers finden Sie im Codebeispiel in der <xref:System.Windows.Forms.Cursor>-Klasse. Zusätzlich macht die <xref:System.Windows.Forms.Cursors>-Klasse mehrere <xref:System.Windows.Forms.Cursor>-Objekte für verschiedene Zeigertypen verfügbar, z. B. ein Zeiger, der einer Hand ähnelt.

Im folgenden Beispiel wird der Cursor des Mauszeigers für eine Schaltfläche in eine Hand geändert:

:::code language="csharp" source="snippets/how-to-manage-cursor-pointer/csharp/Form1.cs" id="SetControlCursor":::
:::code language="vb" source="snippets/how-to-manage-cursor-pointer/vb/Form1.vb" id="SetControlCursor":::

Verwenden Sie die <xref:System.Windows.Forms.Control.UseWaitCursor%2A>-Eigenschaft der <xref:System.Windows.Forms.Control>-Klasse, damit der Wartezeiger angezeigt wird, der einer Sanduhr ähnelt, sobald sich der Mauszeiger auf dem Steuerelement befindet.

## <a name="see-also"></a>Siehe auch

- [Übersicht über die Mausverwendung (Windows Forms .NET)](overview.md)
- [Verwenden von Mausereignissen (Windows Forms .NET)](events.md)
- [Unterscheiden zwischen Klicks und Doppelklicks (Windows Forms .NET)](how-to-distinguish-between-clicks-and-double-clicks.md)
- [Simulieren von Mausereignissen (Windows Forms .NET)](how-to-simulate-events.md)
- <xref:System.Windows.Forms.Cursor?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Cursor.Position%2A?displayProperty=nameWithType>
