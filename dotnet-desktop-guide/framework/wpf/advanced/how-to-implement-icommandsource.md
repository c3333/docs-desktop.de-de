---
title: 'Gewusst wie: Implementieren von "ICommandSource"'
ms.date: 12/05/2019
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ICommandSource interfaces [WPF], implementing
ms.assetid: 7452dd39-6e11-44bf-806a-31d87f3772ac
ms.openlocfilehash: 2d8238eb4e008b8032ca0c22da44a554438765fc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976680"
---
# <a name="how-to-implement-icommandsource"></a>Gewusst wie: Implementieren von "ICommandSource"

In diesem Beispiel wird gezeigt, wie eine Befehls Quelle durch Implementieren von erstellt wird <xref:System.Windows.Input.ICommandSource> . Eine Befehls Quelle ist ein Objekt, das weiß, wie ein Befehl aufgerufen wird. Die- <xref:System.Windows.Input.ICommandSource> Schnittstelle macht drei Member verfügbar:

- <xref:System.Windows.Input.ICommandSource.Command%2A>: der Befehl, der aufgerufen wird.
- <xref:System.Windows.Input.ICommandSource.CommandParameter%2A>: ein benutzerdefinierter Datentyp, der von der Befehls Quelle an die Methode, die den Befehl verarbeitet, übermittelt wird.
- <xref:System.Windows.Input.ICommandSource.CommandTarget%2A>: das-Objekt, für das der Befehl ausgeführt wird.

In diesem Beispiel wird eine-Klasse erstellt, die vom-Steuerelement erbt <xref:System.Windows.Controls.Slider> und die-  <xref:System.Windows.Input.ICommandSource> Schnittstelle implementiert.
  
## <a name="example"></a>Beispiel

WPF stellt eine Reihe von Klassen bereit, die implementieren <xref:System.Windows.Input.ICommandSource> , <xref:System.Windows.Controls.Button> z <xref:System.Windows.Controls.MenuItem> . b <xref:System.Windows.Documents.Hyperlink> ., und. Eine Befehls Quelle definiert, wie Sie einen Befehl aufruft. Diese Klassen rufen einen Befehl auf, wenn auf Sie geklickt wird, und werden nur zu einer Befehls Quelle, wenn Ihre- <xref:System.Windows.Input.ICommandSource.Command%2A> Eigenschaft festgelegt ist.

In diesem Beispiel rufen Sie den Befehl auf, wenn der Schieberegler verschoben wird, oder genauer, wenn die <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> Eigenschaft geändert wird.

Im folgenden finden Sie die Klassendefinition:

[!code-csharp[ImplementICommandSource#ImplementICommandSourceClassDefinition](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandsourceclassdefinition)]
[!code-vb[ImplementICommandSource#ImplementICommandSourceClassDefinition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandsourceclassdefinition)]

Der nächste Schritt besteht darin, die Member zu implementieren <xref:System.Windows.Input.ICommandSource> . In diesem Beispiel werden die-Eigenschaften als- <xref:System.Windows.DependencyProperty> Objekte implementiert. Dadurch können die Eigenschaften die Datenbindung verwenden. Weitere Informationen zur- <xref:System.Windows.DependencyProperty> Klasse finden Sie unter [Übersicht über Abhängigkeits Eigenschaften](dependency-properties-overview.md). Weitere Informationen zur Datenbindung finden Sie unter Übersicht über die [Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview).

Hier wird nur die- <xref:System.Windows.Input.ICommandSource.Command%2A> Eigenschaft angezeigt.

[!code-csharp[ImplementICommandSource#ImplementICommandSourceCommandPropertyDefinition](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandsourcecommandpropertydefinition)]
[!code-vb[ImplementICommandSource#ImplementICommandSourceCommandPropertyDefinition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandsourcecommandpropertydefinition)]  
  
Der Änderungs Rückruf lautet wie folgt <xref:System.Windows.DependencyProperty> :

[!code-csharp[ImplementICommandSource#ImplementICommandSourceCommandChanged](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandsourcecommandchanged)]
[!code-vb[ImplementICommandSource#ImplementICommandSourceCommandChanged](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandsourcecommandchanged)]

Der nächste Schritt besteht darin, den Befehl hinzuzufügen und zu entfernen, der der Befehls Quelle zugeordnet ist. Die- <xref:System.Windows.Input.ICommandSource.Command%2A> Eigenschaft kann nicht einfach überschrieben werden, wenn ein neuer Befehl hinzugefügt wird, da die dem vorherigen Befehl zugeordneten Ereignishandler (sofern vorhanden) zuerst entfernt werden müssen.

[!code-csharp[ImplementICommandSource#ImplementICommandSourceHookUnHookCommands](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandsourcehookunhookcommands)]
[!code-vb[ImplementICommandSource#ImplementICommandSourceHookUnHookCommands](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandsourcehookunhookcommands)]

Der nächste Schritt besteht darin, die Logik für den Handler zu erstellen <xref:System.Windows.Input.ICommand.CanExecuteChanged> .

Das- <xref:System.Windows.Input.ICommand.CanExecuteChanged> Ereignis benachrichtigt die Befehls Quelle, dass die Fähigkeit des Befehls, der für das aktuelle Befehls Ziel ausgeführt werden kann, möglicherweise geändert wurde. Wenn eine Befehls Quelle dieses Ereignis empfängt, ruft Sie in der Regel die- <xref:System.Windows.Input.ICommand.CanExecute%2A> Methode für den Befehl auf. Wenn der Befehl nicht für das aktuelle Befehls Ziel ausgeführt werden kann, wird die Befehls Quelle in der Regel deaktiviert. Wenn der Befehl für das aktuelle Befehls Ziel ausgeführt werden kann, wird die Befehls Quelle in der Regel selbst aktiviert.

[!code-csharp[ImplementICommandSource#ImplementICommandCanExecuteChanged](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandcanexecutechanged)]
[!code-vb[ImplementICommandSource#ImplementICommandCanExecuteChanged](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandcanexecutechanged)]

Der letzte Schritt ist die- <xref:System.Windows.Input.ICommand.Execute%2A> Methode. Wenn der Befehl eine ist <xref:System.Windows.Input.RoutedCommand> , wird die- <xref:System.Windows.Input.RoutedCommand> <xref:System.Windows.Input.RoutedCommand.Execute%2A> Methode aufgerufen; andernfalls wird die- <xref:System.Windows.Input.ICommand> <xref:System.Windows.Input.ICommand.Execute%2A> Methode aufgerufen.

[!code-csharp[ImplementICommandSource#ImplementICommandExecute](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandexecute)]
[!code-vb[ImplementICommandSource#ImplementICommandExecute](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandexecute)]

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Input.ICommandSource>
- <xref:System.Windows.Input.ICommand>
- <xref:System.Windows.Input.RoutedCommand>
- [Befehlsübersicht](commanding-overview.md)
