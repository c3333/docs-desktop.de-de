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
# <a name="how-to-create-a-routedcommand"></a><span data-ttu-id="9f496-102">Gewusst wie: Erstellen eines RoutedCommand</span><span class="sxs-lookup"><span data-stu-id="9f496-102">How to: Create a RoutedCommand</span></span>
<span data-ttu-id="9f496-103">In diesem Beispiel wird gezeigt, wie ein benutzerdefiniertes erstellt <xref:System.Windows.Input.RoutedCommand> wird und wie der benutzerdefinierte Befehl implementiert wird, indem ein <xref:System.Windows.Input.ExecutedRoutedEventHandler> und ein erstellt <xref:System.Windows.Input.CanExecuteRoutedEventHandler> und an einen angefügt werden <xref:System.Windows.Input.CommandBinding> .</span><span class="sxs-lookup"><span data-stu-id="9f496-103">This example shows how to create a custom <xref:System.Windows.Input.RoutedCommand> and how to implement the custom command by creating a <xref:System.Windows.Input.ExecutedRoutedEventHandler> and a <xref:System.Windows.Input.CanExecuteRoutedEventHandler> and attaching them to a <xref:System.Windows.Input.CommandBinding>.</span></span>  <span data-ttu-id="9f496-104">Weitere Informationen zu den Befehls Informationen finden Sie in der [Befehls Übersicht](commanding-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9f496-104">For more information on commanding, see the [Commanding Overview](commanding-overview.md).</span></span>  
  
## <a name="example"></a><span data-ttu-id="9f496-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9f496-105">Example</span></span>  
 <span data-ttu-id="9f496-106">Der erste Schritt beim Erstellen eines <xref:System.Windows.Input.RoutedCommand> ist das Definieren des Befehls und das instanziieren.</span><span class="sxs-lookup"><span data-stu-id="9f496-106">The first step in creating a <xref:System.Windows.Input.RoutedCommand> is defining the command and instantiating it.</span></span>  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCommandDefinition](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcommanddefinition)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCommandDefinition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcommanddefinition)]  
  
 <span data-ttu-id="9f496-107">Um den Befehl in einer Anwendung verwenden zu können, müssen Ereignishandler, die definieren, was der Befehl bewirkt, erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9f496-107">In order to use the command in an application, event handlers which define what the command does must be created</span></span>  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewExecuted](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewexecuted)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewExecuted](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewexecuted)]  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCanExecute](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcanexecute)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCanExecute](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcanexecute)]  
  
 <span data-ttu-id="9f496-108">Als nächstes  <xref:System.Windows.Input.CommandBinding> wird eine erstellt, die den-Befehl den Ereignis Handlern zuordnet.</span><span class="sxs-lookup"><span data-stu-id="9f496-108">Next, a  <xref:System.Windows.Input.CommandBinding> is created which associates the command with the event handlers.</span></span> <span data-ttu-id="9f496-109">Der <xref:System.Windows.Input.CommandBinding> wird für ein bestimmtes-Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="9f496-109">The <xref:System.Windows.Input.CommandBinding> is created on a specific object.</span></span>  <span data-ttu-id="9f496-110">Dieses Objekt definiert den Gültigkeitsbereich der <xref:System.Windows.Input.CommandBinding> in der Elementstruktur.</span><span class="sxs-lookup"><span data-stu-id="9f496-110">This object defines the scope of the <xref:System.Windows.Input.CommandBinding> in the element tree</span></span>  
  
 [!code-xaml[CommandingOverviewSnippets#CommandingOverviewWindowCommandBindingXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml#commandingoverviewwindowcommandbindingxaml)]  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCustomCommandBindingCodeBehind](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcustomcommandbindingcodebehind)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCustomCommandBindingCodeBehind](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcustomcommandbindingcodebehind)]  
  
 <span data-ttu-id="9f496-111">Der letzte Schritt besteht darin, den Befehl aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9f496-111">The final step is invoking the command.</span></span>  <span data-ttu-id="9f496-112">Eine Möglichkeit, einen Befehl aufzurufen, besteht darin, den Befehl einem zuzuordnen <xref:System.Windows.Input.ICommandSource> , z <xref:System.Windows.Controls.Button> . b..</span><span class="sxs-lookup"><span data-stu-id="9f496-112">One way to invoke a command is to associate it with a <xref:System.Windows.Input.ICommandSource>, such as a <xref:System.Windows.Controls.Button>.</span></span>  
  
 [!code-xaml[CommandingOverviewSnippets#CommandingOverviewCustomCommandSourceXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml#commandingoverviewcustomcommandsourcexaml)]  
  
 [!code-csharp[CommandingOverviewSnippets#CommandingOverviewCustomCommandSourceCodeBehind](~/samples/snippets/csharp/VS_Snippets_Wpf/CommandingOverviewSnippets/CSharp/Window1.xaml.cs#commandingoverviewcustomcommandsourcecodebehind)]
 [!code-vb[CommandingOverviewSnippets#CommandingOverviewCustomCommandSourceCodeBehind](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CommandingOverviewSnippets/visualbasic/window1.xaml.vb#commandingoverviewcustomcommandsourcecodebehind)]  
  
 <span data-ttu-id="9f496-113">Wenn auf die Schaltfläche geklickt wird, wird die- <xref:System.Windows.Input.RoutedCommand.Execute%2A> Methode für die benutzerdefinierte <xref:System.Windows.Input.RoutedCommand> aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9f496-113">When the Button is clicked, the <xref:System.Windows.Input.RoutedCommand.Execute%2A> method on the custom <xref:System.Windows.Input.RoutedCommand> is called.</span></span>  <span data-ttu-id="9f496-114">Löst <xref:System.Windows.Input.RoutedCommand> das <xref:System.Windows.Input.CommandManager.PreviewExecuted> -Routing Ereignis und das-Routing <xref:System.Windows.Input.CommandManager.Executed> Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="9f496-114">The <xref:System.Windows.Input.RoutedCommand> raises the <xref:System.Windows.Input.CommandManager.PreviewExecuted> and <xref:System.Windows.Input.CommandManager.Executed> routed events.</span></span>  <span data-ttu-id="9f496-115">Diese Ereignisse durchlaufen die Elementstruktur, die nach einem-Element <xref:System.Windows.Input.CommandBinding> für diesen speziellen Befehl sucht.</span><span class="sxs-lookup"><span data-stu-id="9f496-115">These events traverse the element tree looking for a <xref:System.Windows.Input.CommandBinding> for this particular command.</span></span>  <span data-ttu-id="9f496-116">Wenn eine <xref:System.Windows.Input.CommandBinding> gefunden wird, wird der zugeordnete <xref:System.Windows.Input.ExecutedRoutedEventHandler> <xref:System.Windows.Input.CommandBinding> aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9f496-116">If a <xref:System.Windows.Input.CommandBinding> is found, the <xref:System.Windows.Input.ExecutedRoutedEventHandler> associated with <xref:System.Windows.Input.CommandBinding> is called.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="9f496-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f496-117">See also</span></span>

- <xref:System.Windows.Input.RoutedCommand>
- [<span data-ttu-id="9f496-118">Befehlsübersicht</span><span class="sxs-lookup"><span data-stu-id="9f496-118">Commanding Overview</span></span>](commanding-overview.md)
