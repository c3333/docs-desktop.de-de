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
# <a name="how-to-implement-icommandsource"></a><span data-ttu-id="5faa4-102">Gewusst wie: Implementieren von "ICommandSource"</span><span class="sxs-lookup"><span data-stu-id="5faa4-102">How to: Implement ICommandSource</span></span>

<span data-ttu-id="5faa4-103">In diesem Beispiel wird gezeigt, wie eine Befehls Quelle durch Implementieren von erstellt wird <xref:System.Windows.Input.ICommandSource> .</span><span class="sxs-lookup"><span data-stu-id="5faa4-103">This example shows how to create a command source by implementing <xref:System.Windows.Input.ICommandSource>.</span></span> <span data-ttu-id="5faa4-104">Eine Befehls Quelle ist ein Objekt, das weiß, wie ein Befehl aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5faa4-104">A command source is an object that knows how to invoke a command.</span></span> <span data-ttu-id="5faa4-105">Die- <xref:System.Windows.Input.ICommandSource> Schnittstelle macht drei Member verfügbar:</span><span class="sxs-lookup"><span data-stu-id="5faa4-105">The <xref:System.Windows.Input.ICommandSource> interface exposes three members:</span></span>

- <span data-ttu-id="5faa4-106"><xref:System.Windows.Input.ICommandSource.Command%2A>: der Befehl, der aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5faa4-106"><xref:System.Windows.Input.ICommandSource.Command%2A>: the command that will be invoked.</span></span>
- <span data-ttu-id="5faa4-107"><xref:System.Windows.Input.ICommandSource.CommandParameter%2A>: ein benutzerdefinierter Datentyp, der von der Befehls Quelle an die Methode, die den Befehl verarbeitet, übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="5faa4-107"><xref:System.Windows.Input.ICommandSource.CommandParameter%2A>: a user-defined data type which is passed from the command source to the method that handles the command.</span></span>
- <span data-ttu-id="5faa4-108"><xref:System.Windows.Input.ICommandSource.CommandTarget%2A>: das-Objekt, für das der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5faa4-108"><xref:System.Windows.Input.ICommandSource.CommandTarget%2A>: the object that the command is being executed on.</span></span>

<span data-ttu-id="5faa4-109">In diesem Beispiel wird eine-Klasse erstellt, die vom-Steuerelement erbt <xref:System.Windows.Controls.Slider> und die-  <xref:System.Windows.Input.ICommandSource> Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="5faa4-109">In this example, a class is created that inherits from the <xref:System.Windows.Controls.Slider> control and implements the  <xref:System.Windows.Input.ICommandSource> interface.</span></span>
  
## <a name="example"></a><span data-ttu-id="5faa4-110">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5faa4-110">Example</span></span>

<span data-ttu-id="5faa4-111">WPF stellt eine Reihe von Klassen bereit, die implementieren <xref:System.Windows.Input.ICommandSource> , <xref:System.Windows.Controls.Button> z <xref:System.Windows.Controls.MenuItem> . b <xref:System.Windows.Documents.Hyperlink> ., und.</span><span class="sxs-lookup"><span data-stu-id="5faa4-111">WPF provides a number of classes which implement <xref:System.Windows.Input.ICommandSource>, such as <xref:System.Windows.Controls.Button>, <xref:System.Windows.Controls.MenuItem>, and <xref:System.Windows.Documents.Hyperlink>.</span></span> <span data-ttu-id="5faa4-112">Eine Befehls Quelle definiert, wie Sie einen Befehl aufruft.</span><span class="sxs-lookup"><span data-stu-id="5faa4-112">A command source defines how it invokes a command.</span></span> <span data-ttu-id="5faa4-113">Diese Klassen rufen einen Befehl auf, wenn auf Sie geklickt wird, und werden nur zu einer Befehls Quelle, wenn Ihre- <xref:System.Windows.Input.ICommandSource.Command%2A> Eigenschaft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="5faa4-113">These classes invoke a command when they're clicked and they only become a command source when their <xref:System.Windows.Input.ICommandSource.Command%2A> property is set.</span></span>

<span data-ttu-id="5faa4-114">In diesem Beispiel rufen Sie den Befehl auf, wenn der Schieberegler verschoben wird, oder genauer, wenn die <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> Eigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5faa4-114">In this example, you'll invoke the command when the slider is moved, or more accurately, when the <xref:System.Windows.Controls.Primitives.RangeBase.Value%2A> property is changed.</span></span>

<span data-ttu-id="5faa4-115">Im folgenden finden Sie die Klassendefinition:</span><span class="sxs-lookup"><span data-stu-id="5faa4-115">The following is the class definition:</span></span>

[!code-csharp[ImplementICommandSource#ImplementICommandSourceClassDefinition](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandsourceclassdefinition)]
[!code-vb[ImplementICommandSource#ImplementICommandSourceClassDefinition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandsourceclassdefinition)]

<span data-ttu-id="5faa4-116">Der nächste Schritt besteht darin, die Member zu implementieren <xref:System.Windows.Input.ICommandSource> .</span><span class="sxs-lookup"><span data-stu-id="5faa4-116">The next step is to implement the <xref:System.Windows.Input.ICommandSource> members.</span></span> <span data-ttu-id="5faa4-117">In diesem Beispiel werden die-Eigenschaften als- <xref:System.Windows.DependencyProperty> Objekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="5faa4-117">In this example, the properties are implemented as <xref:System.Windows.DependencyProperty> objects.</span></span> <span data-ttu-id="5faa4-118">Dadurch können die Eigenschaften die Datenbindung verwenden.</span><span class="sxs-lookup"><span data-stu-id="5faa4-118">This enables the properties to use data binding.</span></span> <span data-ttu-id="5faa4-119">Weitere Informationen zur- <xref:System.Windows.DependencyProperty> Klasse finden Sie unter [Übersicht über Abhängigkeits Eigenschaften](dependency-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="5faa4-119">For more information about the <xref:System.Windows.DependencyProperty> class, see the [Dependency Properties Overview](dependency-properties-overview.md).</span></span> <span data-ttu-id="5faa4-120">Weitere Informationen zur Datenbindung finden Sie unter Übersicht über die [Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview).</span><span class="sxs-lookup"><span data-stu-id="5faa4-120">For more information about data binding, see the [Data Binding Overview](/dotnet/desktop-wpf/data/data-binding-overview).</span></span>

<span data-ttu-id="5faa4-121">Hier wird nur die- <xref:System.Windows.Input.ICommandSource.Command%2A> Eigenschaft angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5faa4-121">Only the <xref:System.Windows.Input.ICommandSource.Command%2A> property is shown here.</span></span>

[!code-csharp[ImplementICommandSource#ImplementICommandSourceCommandPropertyDefinition](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandsourcecommandpropertydefinition)]
[!code-vb[ImplementICommandSource#ImplementICommandSourceCommandPropertyDefinition](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandsourcecommandpropertydefinition)]  
  
<span data-ttu-id="5faa4-122">Der Änderungs Rückruf lautet wie folgt <xref:System.Windows.DependencyProperty> :</span><span class="sxs-lookup"><span data-stu-id="5faa4-122">The following is the <xref:System.Windows.DependencyProperty> change callback:</span></span>

[!code-csharp[ImplementICommandSource#ImplementICommandSourceCommandChanged](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandsourcecommandchanged)]
[!code-vb[ImplementICommandSource#ImplementICommandSourceCommandChanged](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandsourcecommandchanged)]

<span data-ttu-id="5faa4-123">Der nächste Schritt besteht darin, den Befehl hinzuzufügen und zu entfernen, der der Befehls Quelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="5faa4-123">The next step is to add and remove the command which is associated with the command source.</span></span> <span data-ttu-id="5faa4-124">Die- <xref:System.Windows.Input.ICommandSource.Command%2A> Eigenschaft kann nicht einfach überschrieben werden, wenn ein neuer Befehl hinzugefügt wird, da die dem vorherigen Befehl zugeordneten Ereignishandler (sofern vorhanden) zuerst entfernt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="5faa4-124">The <xref:System.Windows.Input.ICommandSource.Command%2A> property cannot simply be overwritten when a new command is added, because the event handlers associated with the previous command, if there was one, must be removed first.</span></span>

[!code-csharp[ImplementICommandSource#ImplementICommandSourceHookUnHookCommands](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandsourcehookunhookcommands)]
[!code-vb[ImplementICommandSource#ImplementICommandSourceHookUnHookCommands](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandsourcehookunhookcommands)]

<span data-ttu-id="5faa4-125">Der nächste Schritt besteht darin, die Logik für den Handler zu erstellen <xref:System.Windows.Input.ICommand.CanExecuteChanged> .</span><span class="sxs-lookup"><span data-stu-id="5faa4-125">The next step is to create logic for the <xref:System.Windows.Input.ICommand.CanExecuteChanged> handler.</span></span>

<span data-ttu-id="5faa4-126">Das- <xref:System.Windows.Input.ICommand.CanExecuteChanged> Ereignis benachrichtigt die Befehls Quelle, dass die Fähigkeit des Befehls, der für das aktuelle Befehls Ziel ausgeführt werden kann, möglicherweise geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5faa4-126">The <xref:System.Windows.Input.ICommand.CanExecuteChanged> event notifies the command source that the ability of the command to execute on the current command target may have changed.</span></span> <span data-ttu-id="5faa4-127">Wenn eine Befehls Quelle dieses Ereignis empfängt, ruft Sie in der Regel die- <xref:System.Windows.Input.ICommand.CanExecute%2A> Methode für den Befehl auf.</span><span class="sxs-lookup"><span data-stu-id="5faa4-127">When a command source receives this event, it typically calls the <xref:System.Windows.Input.ICommand.CanExecute%2A> method on the command.</span></span> <span data-ttu-id="5faa4-128">Wenn der Befehl nicht für das aktuelle Befehls Ziel ausgeführt werden kann, wird die Befehls Quelle in der Regel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="5faa4-128">If the command cannot execute on the current command target, the command source will typically disable itself.</span></span> <span data-ttu-id="5faa4-129">Wenn der Befehl für das aktuelle Befehls Ziel ausgeführt werden kann, wird die Befehls Quelle in der Regel selbst aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5faa4-129">If the command can execute on the current command target, the command source will typically enable itself.</span></span>

[!code-csharp[ImplementICommandSource#ImplementICommandCanExecuteChanged](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandcanexecutechanged)]
[!code-vb[ImplementICommandSource#ImplementICommandCanExecuteChanged](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandcanexecutechanged)]

<span data-ttu-id="5faa4-130">Der letzte Schritt ist die- <xref:System.Windows.Input.ICommand.Execute%2A> Methode.</span><span class="sxs-lookup"><span data-stu-id="5faa4-130">The last step is the <xref:System.Windows.Input.ICommand.Execute%2A> method.</span></span> <span data-ttu-id="5faa4-131">Wenn der Befehl eine ist <xref:System.Windows.Input.RoutedCommand> , wird die- <xref:System.Windows.Input.RoutedCommand> <xref:System.Windows.Input.RoutedCommand.Execute%2A> Methode aufgerufen; andernfalls wird die- <xref:System.Windows.Input.ICommand> <xref:System.Windows.Input.ICommand.Execute%2A> Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5faa4-131">If the command is a <xref:System.Windows.Input.RoutedCommand>, the <xref:System.Windows.Input.RoutedCommand> <xref:System.Windows.Input.RoutedCommand.Execute%2A> method is called; otherwise, the <xref:System.Windows.Input.ICommand> <xref:System.Windows.Input.ICommand.Execute%2A> method is called.</span></span>

[!code-csharp[ImplementICommandSource#ImplementICommandExecute](~/samples/snippets/csharp/VS_Snippets_Wpf/ImplementICommandSource/CSharp/CommandSlider.cs#implementicommandexecute)]
[!code-vb[ImplementICommandSource#ImplementICommandExecute](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ImplementICommandSource/visualbasic/commandslider.vb#implementicommandexecute)]

## <a name="see-also"></a><span data-ttu-id="5faa4-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5faa4-132">See also</span></span>

- <xref:System.Windows.Input.ICommandSource>
- <xref:System.Windows.Input.ICommand>
- <xref:System.Windows.Input.RoutedCommand>
- [<span data-ttu-id="5faa4-133">Befehlsübersicht</span><span class="sxs-lookup"><span data-stu-id="5faa4-133">Commanding Overview</span></span>](commanding-overview.md)
