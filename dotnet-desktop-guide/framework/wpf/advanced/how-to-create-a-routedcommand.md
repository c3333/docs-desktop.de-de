---
title: 'Gewusst wie: Erstellen eines RoutedCommand'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- RoutedCommand class [WPF], creating
ms.assetid: aaf6979f-69ab-406f-979f-5766daa85fa0
ms.openlocfilehash: d433658a3039c262d2f682eff09df646d978018c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977551"
---
# <a name="how-to-create-a-routedcommand"></a>Gewusst wie: Erstellen eines RoutedCommand
In diesem Beispiel wird gezeigt, wie ein benutzerdefiniertes erstellt <xref:System.Windows.Input.RoutedCommand> wird und wie der benutzerdefinierte Befehl implementiert wird, indem ein <xref:System.Windows.Input.ExecutedRoutedEventHandler> und ein erstellt <xref:System.Windows.Input.CanExecuteRoutedEventHandler> und an einen angefügt werden <xref:System.Windows.Input.CommandBinding> .  Weitere Informationen zu den Befehls Informationen finden Sie in der [Befehls Übersicht](commanding-overview.md).  
  
## <a name="example"></a>Beispiel  
 Der erste Schritt beim Erstellen eines <xref:System.Windows.Input.RoutedCommand> ist das Definieren des Befehls und das instanziieren.  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCommandDefinition](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcommanddefinition)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCommandDefinition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcommanddefinition)]  
  
 Um den Befehl in einer Anwendung verwenden zu können, müssen Ereignishandler, die definieren, was der Befehl bewirkt, erstellt werden.  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewExecuted](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewexecuted)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewExecuted](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewexecuted)]  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCanExecute](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcanexecute)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCanExecute](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcanexecute)]  
  
 Als nächstes  <xref:System.Windows.Input.CommandBinding> wird eine erstellt, die den-Befehl den Ereignis Handlern zuordnet. Der <xref:System.Windows.Input.CommandBinding> wird für ein bestimmtes-Objekt erstellt.  Dieses Objekt definiert den Gültigkeitsbereich der <xref:System.Windows.Input.CommandBinding> in der Elementstruktur.  
  
 [!code-xaml[CommandingOverviewSnippets#CommandingOverviewWindowCommandBindingXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml#commandingoverviewwindowcommandbindingxaml)]  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCustomCommandBindingCodeBehind](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcustomcommandbindingcodebehind)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCustomCommandBindingCodeBehind](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcustomcommandbindingcodebehind)]  
  
 Der letzte Schritt besteht darin, den Befehl aufzurufen.  Eine Möglichkeit, einen Befehl aufzurufen, besteht darin, den Befehl einem zuzuordnen <xref:System.Windows.Input.ICommandSource> , z <xref:System.Windows.Controls.Button> . b..  
  
 [!code-xaml[CommandingOverviewSnippets#CommandingOverviewCustomCommandSourceXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml#commandingoverviewcustomcommandsourcexaml)]  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCustomCommandSourceCodeBehind](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcustomcommandsourcecodebehind)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCustomCommandSourceCodeBehind](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcustomcommandsourcecodebehind)]  
  
 Wenn auf die Schaltfläche geklickt wird, wird die- <xref:System.Windows.Input.RoutedCommand.Execute%2A> Methode für die benutzerdefinierte <xref:System.Windows.Input.RoutedCommand> aufgerufen.  Löst <xref:System.Windows.Input.RoutedCommand> das <xref:System.Windows.Input.CommandManager.PreviewExecuted> -Routing Ereignis und das-Routing <xref:System.Windows.Input.CommandManager.Executed> Ereignis aus.  Diese Ereignisse durchlaufen die Elementstruktur, die nach einem-Element <xref:System.Windows.Input.CommandBinding> für diesen speziellen Befehl sucht.  Wenn eine <xref:System.Windows.Input.CommandBinding> gefunden wird, wird der zugeordnete <xref:System.Windows.Input.ExecutedRoutedEventHandler> <xref:System.Windows.Input.CommandBinding> aufgerufen.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Input.RoutedCommand>
- [Befehlsübersicht](commanding-overview.md)
