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
# <a name="how-to-create-a-grid-element"></a>Gewusst wie: Erstellen eines Elements von Grid
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird gezeigt, wie eine Instanz von mithilfe von-oder-Code erstellt und verwendet <xref:System.Windows.Controls.Grid> wird [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] . In diesem Beispiel <xref:System.Windows.Controls.ColumnDefinition> werden drei-Objekte und drei-Objekte verwendet, <xref:System.Windows.Controls.RowDefinition> um ein Raster mit neun Zellen (z. b. in einem Arbeitsblatt) zu erstellen. Jede Zelle enthält ein <xref:System.Windows.Controls.TextBlock> -Element, das Daten darstellt, und die obere Zeile enthält ein-Objekt, auf <xref:System.Windows.Controls.TextBlock> das die- <xref:System.Windows.Controls.Grid.ColumnSpan%2A> Eigenschaft angewendet wird. Um die Grenzen jeder Zelle anzuzeigen, wird die- <xref:System.Windows.Controls.Grid.ShowGridLines%2A> Eigenschaft aktiviert.  
  
 [!code-csharp[Grid#3](~/samples/snippets/csharp/VS_Snippets_Wpf/Grid/CSharp/Grid_Code.cs#3)]
 [!code-vb[Grid#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/Grid/VisualBasic/grid_vb.vb#3)]
 [!code-xaml[Grid#3](~/samples/snippets/xaml/VS_Snippets_Wpf/Grid/XAML/default.xaml#3)]  
  
  Beide Ansätze generieren eine Benutzeroberfläche, die ähnlich aussieht, wie im folgenden Beispiel gezeigt.

  ![ein Screenshot zeigt eine WPF-Benutzeroberfläche, die ein Raster enthält, das in drei Spalten unterteilt ist.  Sie trägt die Überschrift "2018 Products-Produkte", die alle Spalten der obersten Zeile umfasst, und verfügt jeweils über drei Spalten mit Umsatzzahlen für ein bestimmtes Quartal.  Die untere Zeile enthält Text, der zwei Spalten mit der Meldung "Gesamt Einheiten: 300.000" umfasst.](././media/how-to-create-a-grid-element/how-to-create-a-grid-element.png)
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Grid>
- [Übersicht über Panel-Elemente](panels-overview.md)
