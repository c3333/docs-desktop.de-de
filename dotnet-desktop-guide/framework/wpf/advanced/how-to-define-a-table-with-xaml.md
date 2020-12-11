---
title: 'Gewusst wie: Definieren einer Tabelle mit XAML'
ms.date: 03/30/2017
helpviewer_keywords:
- XAML [WPF], defining tables
- documents [WPF], defining tables with XAML
- tables [WPF], defining with XAML
ms.assetid: 83f2dc58-437e-4cdc-b5dd-0019810c7a85
ms.openlocfilehash: 709e977670b867f6513bf166918d3bcba0a8c62c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976565"
---
# <a name="how-to-define-a-table-with-xaml"></a><span data-ttu-id="29c66-102">Gewusst wie: Definieren einer Tabelle mit XAML</span><span class="sxs-lookup"><span data-stu-id="29c66-102">How to: Define a Table with XAML</span></span>
<span data-ttu-id="29c66-103">Im folgenden Beispiel wird veranschaulicht, wie ein mithilfe von definiert wird <xref:System.Windows.Documents.Table> [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="29c66-103">The following example demonstrates how to define a <xref:System.Windows.Documents.Table> using [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)].</span></span>  <span data-ttu-id="29c66-104">Die Beispiel Tabelle enthält vier Spalten (dargestellt durch- <xref:System.Windows.Documents.TableColumn> Elemente) und mehrere Zeilen (dargestellt durch- <xref:System.Windows.Documents.TableRow> Elemente), die Daten sowie Titel-, Header-und Footerinformationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="29c66-104">The example table has four columns (represented by <xref:System.Windows.Documents.TableColumn> elements) and several rows (represented by <xref:System.Windows.Documents.TableRow> elements) containing data as well as title, header, and footer information.</span></span>  <span data-ttu-id="29c66-105">Zeilen müssen in einem-Element enthalten sein <xref:System.Windows.Documents.TableRowGroup> .</span><span class="sxs-lookup"><span data-stu-id="29c66-105">Rows must be contained in a <xref:System.Windows.Documents.TableRowGroup> element.</span></span>  <span data-ttu-id="29c66-106">Jede Zeile in der Tabelle besteht aus mindestens einer Zelle (dargestellt durch- <xref:System.Windows.Documents.TableCell> Elemente).</span><span class="sxs-lookup"><span data-stu-id="29c66-106">Each row in the table is comprised of one or more cells (represented by <xref:System.Windows.Documents.TableCell> elements).</span></span>  <span data-ttu-id="29c66-107">Der Inhalt in einer Tabellenzelle muss in einem- <xref:System.Windows.Documents.Block> Element enthalten sein. in diesem Fall <xref:System.Windows.Documents.Paragraph> werden-Elemente verwendet.</span><span class="sxs-lookup"><span data-stu-id="29c66-107">Content in a table cell must be contained in a <xref:System.Windows.Documents.Block> element; in this case <xref:System.Windows.Documents.Paragraph> elements are used.</span></span>  <span data-ttu-id="29c66-108">Die Tabelle hostet außerdem einen Hyperlink (dargestellt durch das- <xref:System.Windows.Documents.Hyperlink> Element) in der Footerzeile.</span><span class="sxs-lookup"><span data-stu-id="29c66-108">The table also hosts a hyperlink (represented by the <xref:System.Windows.Documents.Hyperlink> element) in the footer row.</span></span>  
  
## <a name="example"></a><span data-ttu-id="29c66-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="29c66-109">Example</span></span>  
 [!code-xaml[TableSnippetsXAML#_TableXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippetsXAML/CS/Window1.xaml#_tablexaml)]  
  
 <span data-ttu-id="29c66-110">In der folgenden Abbildung wird gezeigt, wie die in diesem Beispiel definierte Tabelle Folgendes rendert:</span><span class="sxs-lookup"><span data-stu-id="29c66-110">The following figure shows how the table defined in this example renders:</span></span>  
  
 ![Screenshot einer Tabelle, die mit XAML definiert ist.](./media/how-to-define-a-table-with-xaml/planetary-information-xaml-table.png)
