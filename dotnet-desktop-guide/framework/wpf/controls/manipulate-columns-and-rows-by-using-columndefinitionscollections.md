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
# <a name="how-to-manipulate-columns-and-rows-by-using-columndefinitionscollections-and-rowdefinitionscollections"></a>Gewusst wie: Bearbeiten von Spalten und Zeilen mithilfe von ColumnDefinitionsCollections und RowDefinitionsCollections
In diesem Beispiel wird gezeigt, wie die-Methoden in der <xref:System.Windows.Controls.ColumnDefinitionCollection> -Klasse und der- <xref:System.Windows.Controls.RowDefinitionCollection> Klasse verwendet werden, um Aktionen wie das Hinzufügen, löschen oder zählen des Inhalts von Zeilen oder Spalten auszuführen. Beispielsweise können Sie <xref:System.Windows.Controls.ColumnDefinitionCollection.Add%2A> , <xref:System.Windows.Controls.ColumnDefinitionCollection.Clear%2A> oder <xref:System.Windows.Controls.ColumnDefinitionCollection.Count%2A> die Elemente, die in einem oder enthalten sind <xref:System.Windows.Controls.ColumnDefinition> <xref:System.Windows.Controls.RowDefinition> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein- <xref:System.Windows.Controls.Grid> Element mit dem-Element erstellt <xref:System.Windows.FrameworkElement.Name%2A> `grid1` . Die <xref:System.Windows.Controls.Grid> enthält ein- <xref:System.Windows.Controls.StackPanel> <xref:System.Windows.Controls.Button> Element, das-Elemente enthält, die jeweils durch eine andere Auflistungs Methode gesteuert werden Wenn Sie auf ein klicken <xref:System.Windows.Controls.Button> , wird in der Code Behind-Datei ein Methoden Aufrufvorgang aktiviert.  
  
 [!code-xaml[ColumnDefinitionsGrid#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ColumnDefinitionsGrid/CSharp/Window1.xaml#1)]  
  
 In diesem Beispiel wird eine Reihe von benutzerdefinierten Methoden definiert, die jeweils einem- <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Ereignis in der- [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Datei entsprechen. Sie können die Anzahl der Spalten und Zeilen in <xref:System.Windows.Controls.Grid> auf verschiedene Weise ändern, darunter das Hinzufügen oder Entfernen von Zeilen und Spalten sowie das zählen der Gesamtzahl von Zeilen und Spalten. Um <xref:System.ArgumentOutOfRangeException> -und <xref:System.ArgumentException> -Ausnahmen zu verhindern, können Sie die von der-Methode bereitgestellte Fehler Überprüfungs Funktion verwenden <xref:System.Windows.Controls.ColumnDefinitionCollection.RemoveRange%2A> .  
  
 [!code-csharp[ColumnDefinitionsGrid#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ColumnDefinitionsGrid/CSharp/Window1.xaml.cs#2)]
 [!code-vb[ColumnDefinitionsGrid#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ColumnDefinitionsGrid/VisualBasic/Window1.xaml.vb#2)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Grid>
- <xref:System.Windows.Controls.ColumnDefinitionCollection>
- <xref:System.Windows.Controls.RowDefinitionCollection>
