---
title: 'Gewusst wie: Öffnen einer Datei, die auf einem RichTextBox-Steuerelement abgelegt ist'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- drag-and-drop [WPF], RichTextBox
- RichTextBox [WPF], drag-and-drop
- drag-and-drop [WPF], open a dropped file
ms.assetid: 6bb8bb54-f576-41db-a9a7-24102ddeb490
ms.openlocfilehash: e3d0e9597b7ed69368f1755e146433d6e4bad9f6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977749"
---
# <a name="how-to-open-a-file-that-is-dropped-on-a-richtextbox-control"></a>Gewusst wie: Öffnen einer Datei, die auf einem RichTextBox-Steuerelement abgelegt ist

In [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] verfügen die <xref:System.Windows.Controls.TextBox> Steuer <xref:System.Windows.Controls.RichTextBox> Elemente, <xref:System.Windows.Documents.FlowDocument> und über integrierte Drag & amp; Drop-Funktionen. Die integrierte Funktionalität ermöglicht das Drag & Drop von Text innerhalb von und zwischen den Steuerelementen. Es ist jedoch nicht möglich, eine Datei zu öffnen, indem Sie die Datei auf dem Steuerelement ablegen. Diese Steuerelemente markieren auch die Drag & Drop-Ereignisse als behandelt. Daher können Sie standardmäßig keine eigenen Ereignishandler hinzufügen, um Funktionen zum Öffnen von gelöschten Dateien bereitzustellen.

Wenn Sie zusätzliche Behandlung für Drag & Drop-Ereignisse in diesen Steuerelementen hinzufügen möchten, verwenden Sie die- <xref:System.Windows.UIElement.AddHandler%28System.Windows.RoutedEvent%2CSystem.Delegate%2CSystem.Boolean%29> Methode, um die Ereignishandler für die Drag & amp; Drop-Ereignisse hinzuzufügen. Legen Sie den- `handledEventsToo` Parameter auf fest, `true` damit der angegebene Handler für ein Routing Ereignis aufgerufen wird, das bereits von einem anderen Element auf der Ereignis Route als behandelt markiert wurde.

> [!TIP]
> Sie können die integrierte Drag & amp; Drop-Funktion von <xref:System.Windows.Controls.TextBox> , und ersetzen, <xref:System.Windows.Controls.RichTextBox> indem Sie <xref:System.Windows.Documents.FlowDocument> die Vorschau Versionen der Drag & Drop-Ereignisse behandeln und die Vorschau Ereignisse als behandelt markieren. Dadurch werden jedoch die integrierten Drag & amp; Drop-Funktionen deaktiviert, was nicht empfohlen wird.

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird veranschaulicht, wie Handler für das <xref:System.Windows.DragDrop.DragOver> -Ereignis und das- <xref:System.Windows.DragDrop.Drop> Ereignis in einem hinzugefügt werden <xref:System.Windows.Controls.RichTextBox> . In diesem Beispiel <xref:System.Windows.UIElement.AddHandler%28System.Windows.RoutedEvent%2CSystem.Delegate%2CSystem.Boolean%29> wird die-Methode verwendet und der-Parameter auf festgelegt, `handledEventsToo` `true` sodass die Ereignishandler aufgerufen werden, auch wenn <xref:System.Windows.Controls.RichTextBox> diese Ereignisse als behandelt markieren. Der Code in den-Ereignis Handlern fügt Funktionen hinzu, um eine Textdatei zu öffnen, die in gelöscht wird <xref:System.Windows.Controls.RichTextBox> .

Um dieses Beispiel zu testen, ziehen Sie eine Textdatei oder eine RTF-Datei (Rich Textformat) aus Windows-Explorer in das <xref:System.Windows.Controls.RichTextBox> . Die Datei wird im geöffnet <xref:System.Windows.Controls.RichTextBox> . Wenn Sie die UMSCHALTTASTE drücken, bevor Sie die Datei ablegen, wird die Datei als Klartext geöffnet.

[!code-xaml[DragDropSnippets#RtbXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/dragdropsnippets/cs/mainwindow.xaml#rtbxaml)]

[!code-csharp[DragDropSnippets#RtbHandlers](~/samples/snippets/csharp/VS_Snippets_Wpf/dragdropsnippets/cs/mainwindow.xaml.cs#rtbhandlers)]
[!code-vb[DragDropSnippets#RtbHandlers](~/samples/snippets/visualbasic/VS_Snippets_Wpf/dragdropsnippets/vb/mainwindow.xaml.vb#rtbhandlers)]
