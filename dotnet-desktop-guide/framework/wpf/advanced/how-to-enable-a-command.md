---
title: 'Gewusst wie: Aktivieren eines Befehls'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- CommandBindings [WPF]
- commanding [WPF]
ms.assetid: d8016266-58d9-48f7-8298-a86b7ed49fbd
ms.openlocfilehash: a2044f9504b3f2ee05ccaa63fa5e0277e2798b60
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977548"
---
# <a name="how-to-enable-a-command"></a>Gewusst wie: Aktivieren eines Befehls
Im folgenden Beispiel wird veranschaulicht, wie die Befehls Befehle in verwendet werden [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] .  Im Beispiel wird gezeigt, wie einem eine <xref:System.Windows.Input.RoutedCommand> zugeordnet <xref:System.Windows.Controls.Button> wird, ein erstellt <xref:System.Windows.Input.CommandBinding> und die Ereignishandler erstellt werden, die implementieren <xref:System.Windows.Input.RoutedCommand> .  Weitere Informationen zu den Befehls Informationen finden Sie in der [Befehls Übersicht](commanding-overview.md).  
  
## <a name="example"></a>Beispiel  
 Der erste Code Abschnitt erstellt das [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] , das aus einem <xref:System.Windows.Controls.Button> und einem besteht <xref:System.Windows.Controls.StackPanel> , und erstellt ein, <xref:System.Windows.Input.CommandBinding> das die Befehls Handler mit verknüpft <xref:System.Windows.Input.RoutedCommand> .  
  
 Die- <xref:System.Windows.Input.ICommandSource.Command%2A> Eigenschaft von <xref:System.Windows.Controls.Button> ist dem Befehl zugeordnet <xref:System.Windows.Input.ApplicationCommands.Close%2A> .  
  
 Der <xref:System.Windows.Input.CommandBinding> wird dem des Stamms hinzugefügt <xref:System.Windows.Input.CommandBindingCollection> <xref:System.Windows.Window> . Die <xref:System.Windows.Input.CommandBinding.Executed> <xref:System.Windows.Input.CommandBinding.CanExecute> Ereignishandler und werden an diese Bindung angefügt und dem Befehl zugeordnet <xref:System.Windows.Input.ApplicationCommands.Close%2A> .  
  
 Ohne dass <xref:System.Windows.Input.CommandBinding> keine Befehls Logik vorhanden ist, wird nur ein Mechanismus zum Aufrufen des Befehls angezeigt.  Wenn <xref:System.Windows.Controls.Button> auf das geklickt wird, <xref:System.Windows.Input.CommandManager.PreviewExecuted> <xref:System.Windows.RoutedEvent> wird der auf dem Befehls Ziel ausgelöst, gefolgt von <xref:System.Windows.Input.CommandManager.Executed> <xref:System.Windows.RoutedEvent> .  Diese Ereignisse durchlaufen die Elementstruktur, indem nach einem <xref:System.Windows.Input.CommandBinding> für diesen bestimmten Befehl gesucht wird.  Beachten Sie, dass bei einem <xref:System.Windows.RoutedEvent> Tunnel und einer Blase durch die Elementstruktur sorgfältig vorgegangen werden muss, wo der <xref:System.Windows.Input.CommandBinding> eingefügt wird.   Wenn sich das auf einem gleich geordneten Element <xref:System.Windows.Input.CommandBinding> des Befehls Ziels oder auf einem anderen Knoten befindet, der sich nicht auf der Route von befindet, wird auf <xref:System.Windows.RoutedEvent> das <xref:System.Windows.Input.CommandBinding> nicht zugegriffen.  
  
 [!code-xaml[EnableCloseCommand#CloseCommandBinding](~/samples/snippets/csharp/VS_Snippets_Wpf/EnableCloseCommand/CSharp/Window1.xaml#closecommandbinding)]  
  
 [!code-csharp[EnableCloseCommand#CloseCommandBindingCodeBehind](~/samples/snippets/csharp/VS_Snippets_Wpf/EnableCloseCommand/CSharp/Window1.xaml.cs#closecommandbindingcodebehind)]
 [!code-vb[EnableCloseCommand#CloseCommandBindingCodeBehind](~/samples/snippets/visualbasic/VS_Snippets_Wpf/EnableCloseCommand/VisualBasic/Window1.xaml.vb#closecommandbindingcodebehind)]  
  
 Der nächste Code Abschnitt implementiert die <xref:System.Windows.Input.CommandManager.Executed> <xref:System.Windows.Input.CommandBinding.CanExecute> Ereignishandler und.  
  
 Der <xref:System.Windows.Input.CommandManager.Executed> Handler Ruft eine-Methode auf, um die geöffnete Datei zu schließen.  Der- <xref:System.Windows.Input.CommandBinding.CanExecute> Handler Ruft eine-Methode auf, um zu bestimmen, ob eine Datei geöffnet ist.  Wenn eine Datei geöffnet ist, <xref:System.Windows.Input.CanExecuteRoutedEventArgs.CanExecute%2A> wird auf festgelegt, `true` andernfalls wird Sie auf festgelegt `false` .  
  
 [!code-csharp[EnableCloseCommand#CloseCommandHandler](~/samples/snippets/csharp/VS_Snippets_Wpf/EnableCloseCommand/CSharp/Window1.xaml.cs#closecommandhandler)]
 [!code-vb[EnableCloseCommand#CloseCommandHandler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/EnableCloseCommand/VisualBasic/Window1.xaml.vb#closecommandhandler)]  
  
## <a name="see-also"></a>Siehe auch

- [Befehlsübersicht](commanding-overview.md)
