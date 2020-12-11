---
title: 'Gewusst wie: Erstellen eines Elements von Grid'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Grid control [WPF], creating [WPF], grid instance
ms.assetid: b2f07626-9df8-43b8-8d36-492f3cb42837
ms.openlocfilehash: c87ca1d6642bd18fa85806c92caab049d259d45e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978070"
---
# <a name="how-to-create-a-grid-element"></a><span data-ttu-id="fa793-102">Gewusst wie: Erstellen eines Elements von Grid</span><span class="sxs-lookup"><span data-stu-id="fa793-102">How to: Create a Grid Element</span></span>
## <a name="example"></a><span data-ttu-id="fa793-103">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fa793-103">Example</span></span>  
 <span data-ttu-id="fa793-104">Im folgenden Beispiel wird gezeigt, wie eine Instanz von mithilfe von-oder-Code erstellt und verwendet <xref:System.Windows.Controls.Grid> wird [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="fa793-104">The following example shows how to create and use an instance of <xref:System.Windows.Controls.Grid> by using either [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] or code.</span></span> <span data-ttu-id="fa793-105">In diesem Beispiel <xref:System.Windows.Controls.ColumnDefinition> werden drei-Objekte und drei-Objekte verwendet, <xref:System.Windows.Controls.RowDefinition> um ein Raster mit neun Zellen (z. b. in einem Arbeitsblatt) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fa793-105">This example uses three <xref:System.Windows.Controls.ColumnDefinition> objects and three <xref:System.Windows.Controls.RowDefinition> objects to create a grid that has nine cells, such as in a worksheet.</span></span> <span data-ttu-id="fa793-106">Jede Zelle enthält ein <xref:System.Windows.Controls.TextBlock> -Element, das Daten darstellt, und die obere Zeile enthält ein-Objekt, auf <xref:System.Windows.Controls.TextBlock> das die- <xref:System.Windows.Controls.Grid.ColumnSpan%2A> Eigenschaft angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa793-106">Each cell contains a <xref:System.Windows.Controls.TextBlock> element that represents data, and the top row contains a <xref:System.Windows.Controls.TextBlock> with the <xref:System.Windows.Controls.Grid.ColumnSpan%2A> property applied.</span></span> <span data-ttu-id="fa793-107">Um die Grenzen jeder Zelle anzuzeigen, wird die- <xref:System.Windows.Controls.Grid.ShowGridLines%2A> Eigenschaft aktiviert.</span><span class="sxs-lookup"><span data-stu-id="fa793-107">To show the boundaries of each cell, the <xref:System.Windows.Controls.Grid.ShowGridLines%2A> property is enabled.</span></span>  
  
 [!code-csharp[Grid#3](~/samples/snippets/csharp/VS_Snippets_Wpf/Grid/CSharp/Grid_Code.cs#3)]
 [!code-vb[Grid#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Grid/VisualBasic/grid_vb.vb#3)]
 [!code-xaml[Grid#3](~/samples/snippets/xaml/VS_Snippets_Wpf/Grid/XAML/default.xaml#3)]  
  
  <span data-ttu-id="fa793-108">Beide Ansätze generieren eine Benutzeroberfläche, die ähnlich aussieht, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="fa793-108">Either approach will generate a user interface that looks much the same, like the one below.</span></span>

  ![ein Screenshot zeigt eine WPF-Benutzeroberfläche, die ein Raster enthält, das in drei Spalten unterteilt ist.](././media/how-to-create-a-grid-element/how-to-create-a-grid-element.png)
## <a name="see-also"></a><span data-ttu-id="fa793-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa793-112">See also</span></span>

- <xref:System.Windows.Controls.Grid>
- [<span data-ttu-id="fa793-113">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="fa793-113">Panels Overview</span></span>](panels-overview.md)
