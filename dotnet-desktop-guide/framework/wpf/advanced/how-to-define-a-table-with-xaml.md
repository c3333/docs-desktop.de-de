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
# <a name="how-to-define-a-table-with-xaml"></a>Gewusst wie: Definieren einer Tabelle mit XAML
Im folgenden Beispiel wird veranschaulicht, wie ein mithilfe von definiert wird <xref:System.Windows.Documents.Table> [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] .  Die Beispiel Tabelle enthält vier Spalten (dargestellt durch- <xref:System.Windows.Documents.TableColumn> Elemente) und mehrere Zeilen (dargestellt durch- <xref:System.Windows.Documents.TableRow> Elemente), die Daten sowie Titel-, Header-und Footerinformationen enthalten.  Zeilen müssen in einem-Element enthalten sein <xref:System.Windows.Documents.TableRowGroup> .  Jede Zeile in der Tabelle besteht aus mindestens einer Zelle (dargestellt durch- <xref:System.Windows.Documents.TableCell> Elemente).  Der Inhalt in einer Tabellenzelle muss in einem- <xref:System.Windows.Documents.Block> Element enthalten sein. in diesem Fall <xref:System.Windows.Documents.Paragraph> werden-Elemente verwendet.  Die Tabelle hostet außerdem einen Hyperlink (dargestellt durch das- <xref:System.Windows.Documents.Hyperlink> Element) in der Footerzeile.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[TableSnippetsXAML#_TableXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TableSnippetsXAML/CS/Window1.xaml#_tablexaml)]  
  
 In der folgenden Abbildung wird gezeigt, wie die in diesem Beispiel definierte Tabelle Folgendes rendert:  
  
 ![Screenshot einer Tabelle, die mit XAML definiert ist.](./media/how-to-define-a-table-with-xaml/planetary-information-xaml-table.png)
