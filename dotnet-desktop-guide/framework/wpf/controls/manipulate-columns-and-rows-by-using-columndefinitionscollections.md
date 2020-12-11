---
title: 'Gewusst wie: Bearbeiten von Spalten und Zeilen mithilfe von ColumnDefinitionsCollections und RowDefinitionsCollections'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], Grid class
- Grid control [WPF], ColumnDefinitionCollection class
- Grid control [WPF], RowDefinitionCollection class
ms.assetid: bfc7160a-45f2-4e17-9961-df414dfb13c5
ms.openlocfilehash: 2f6d174fd54dca3744e5967f198c645e01a94fe5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977291"
---
# <a name="how-to-manipulate-columns-and-rows-by-using-columndefinitionscollections-and-rowdefinitionscollections"></a><span data-ttu-id="7d288-102">Gewusst wie: Bearbeiten von Spalten und Zeilen mithilfe von ColumnDefinitionsCollections und RowDefinitionsCollections</span><span class="sxs-lookup"><span data-stu-id="7d288-102">How to: Manipulate Columns and Rows by Using ColumnDefinitionsCollections and RowDefinitionsCollections</span></span>
<span data-ttu-id="7d288-103">In diesem Beispiel wird gezeigt, wie die-Methoden in der <xref:System.Windows.Controls.ColumnDefinitionCollection> -Klasse und der- <xref:System.Windows.Controls.RowDefinitionCollection> Klasse verwendet werden, um Aktionen wie das Hinzufügen, löschen oder zählen des Inhalts von Zeilen oder Spalten auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7d288-103">This example shows how to use the methods in the <xref:System.Windows.Controls.ColumnDefinitionCollection> and <xref:System.Windows.Controls.RowDefinitionCollection> classes to perform actions like adding, clearing, or counting the contents of rows or columns.</span></span> <span data-ttu-id="7d288-104">Beispielsweise können Sie <xref:System.Windows.Controls.ColumnDefinitionCollection.Add%2A> , <xref:System.Windows.Controls.ColumnDefinitionCollection.Clear%2A> oder <xref:System.Windows.Controls.ColumnDefinitionCollection.Count%2A> die Elemente, die in einem oder enthalten sind <xref:System.Windows.Controls.ColumnDefinition> <xref:System.Windows.Controls.RowDefinition> .</span><span class="sxs-lookup"><span data-stu-id="7d288-104">For example, you can <xref:System.Windows.Controls.ColumnDefinitionCollection.Add%2A>, <xref:System.Windows.Controls.ColumnDefinitionCollection.Clear%2A>, or <xref:System.Windows.Controls.ColumnDefinitionCollection.Count%2A> the items that are included in a <xref:System.Windows.Controls.ColumnDefinition> or <xref:System.Windows.Controls.RowDefinition>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7d288-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7d288-105">Example</span></span>  
 <span data-ttu-id="7d288-106">Im folgenden Beispiel wird ein- <xref:System.Windows.Controls.Grid> Element mit dem-Element erstellt <xref:System.Windows.FrameworkElement.Name%2A> `grid1` .</span><span class="sxs-lookup"><span data-stu-id="7d288-106">The following example creates a <xref:System.Windows.Controls.Grid> element with a <xref:System.Windows.FrameworkElement.Name%2A> of `grid1`.</span></span> <span data-ttu-id="7d288-107">Die <xref:System.Windows.Controls.Grid> enthält ein- <xref:System.Windows.Controls.StackPanel> <xref:System.Windows.Controls.Button> Element, das-Elemente enthält, die jeweils durch eine andere Auflistungs Methode gesteuert werden</span><span class="sxs-lookup"><span data-stu-id="7d288-107">The <xref:System.Windows.Controls.Grid> contains a <xref:System.Windows.Controls.StackPanel> that holds <xref:System.Windows.Controls.Button> elements, each controlled by a different collection method.</span></span> <span data-ttu-id="7d288-108">Wenn Sie auf ein klicken <xref:System.Windows.Controls.Button> , wird in der Code Behind-Datei ein Methoden Aufrufvorgang aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7d288-108">When you click a <xref:System.Windows.Controls.Button>, it activates a method call in the code-behind file.</span></span>  
  
 [!code-xaml[ColumnDefinitionsGrid#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ColumnDefinitionsGrid/CSharp/Window1.xaml#1)]  
  
 <span data-ttu-id="7d288-109">In diesem Beispiel wird eine Reihe von benutzerdefinierten Methoden definiert, die jeweils einem- <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Ereignis in der- [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Datei entsprechen.</span><span class="sxs-lookup"><span data-stu-id="7d288-109">This example defines a series of custom methods, each corresponding to a <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event in the [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] file.</span></span> <span data-ttu-id="7d288-110">Sie können die Anzahl der Spalten und Zeilen in <xref:System.Windows.Controls.Grid> auf verschiedene Weise ändern, darunter das Hinzufügen oder Entfernen von Zeilen und Spalten sowie das zählen der Gesamtzahl von Zeilen und Spalten.</span><span class="sxs-lookup"><span data-stu-id="7d288-110">You can change the number of columns and rows in the <xref:System.Windows.Controls.Grid> in several ways, which includes adding or removing rows and columns; and counting the total number of rows and columns.</span></span> <span data-ttu-id="7d288-111">Um <xref:System.ArgumentOutOfRangeException> -und <xref:System.ArgumentException> -Ausnahmen zu verhindern, können Sie die von der-Methode bereitgestellte Fehler Überprüfungs Funktion verwenden <xref:System.Windows.Controls.ColumnDefinitionCollection.RemoveRange%2A> .</span><span class="sxs-lookup"><span data-stu-id="7d288-111">To prevent <xref:System.ArgumentOutOfRangeException> and <xref:System.ArgumentException> exceptions, you can use the error-checking functionality that the <xref:System.Windows.Controls.ColumnDefinitionCollection.RemoveRange%2A> method provides.</span></span>  
  
 [!code-csharp[ColumnDefinitionsGrid#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ColumnDefinitionsGrid/CSharp/Window1.xaml.cs#2)]
 [!code-vb[ColumnDefinitionsGrid#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ColumnDefinitionsGrid/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a><span data-ttu-id="7d288-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d288-112">See also</span></span>

- <xref:System.Windows.Controls.Grid>
- <xref:System.Windows.Controls.ColumnDefinitionCollection>
- <xref:System.Windows.Controls.RowDefinitionCollection>
