---
title: 'Gewusst wie: Freigeben von Größeneigenschaften zwischen Grids'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Grid control [WPF], sharing sizing data of columns
- sizing data in Grid controls [WPF]
- Grid control [WPF], sharing sizing data of rows
ms.assetid: a0535a6f-ff04-4b25-9912-7dd856e11044
ms.openlocfilehash: d5ab2ac612d55c8cbc34ae6d7d9d63b9f8aa23e7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978103"
---
# <a name="how-to-share-sizing-properties-between-grids"></a>Gewusst wie: Freigeben von Größeneigenschaften zwischen Grids
In diesem Beispiel wird gezeigt, wie die Größendaten von Spalten und Zeilen zwischen Elementen gemeinsam genutzt werden, um die <xref:System.Windows.Controls.Grid> Größe konsistent zu halten.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden zwei- <xref:System.Windows.Controls.Grid> Elemente als untergeordnete Elemente eines übergeordneten Elements eingeführt <xref:System.Windows.Controls.DockPanel> . Die <xref:System.Windows.Controls.Grid.IsSharedSizeScope%2A> angefügte-Eigenschaft von <xref:System.Windows.Controls.Grid> wird für das übergeordnete Element definiert <xref:System.Windows.Controls.DockPanel> .  
  
 Im Beispiel wird der-Eigenschafts Wert mit zwei- <xref:System.Windows.Controls.Button> Elementen manipuliert. jedes-Element stellt einen der booleschen Eigenschaftswerte dar. Wenn der- <xref:System.Windows.Controls.Grid.IsSharedSizeScope%2A> Eigenschafts Wert auf festgelegt ist `true` , werden bei jedem Spalten-oder Zeilen Mitglied einer Freigabe <xref:System.Windows.Controls.DefinitionBase.SharedSizeGroup%2A> Größen Informationen unabhängig vom Inhalt einer Zeile oder Spalte angezeigt.  
  
 [!code-xaml[gridIssharedsizescopeProp#1](~/samples/snippets/csharp/VS_Snippets_Wpf/gridIssharedsizescopeProp/CSharp/Window1.xaml#1)]  
  
 ...  
  
 [!code-xaml[gridIssharedsizescopeProp#2](~/samples/snippets/csharp/VS_Snippets_Wpf/gridIssharedsizescopeProp/CSharp/Window1.xaml#2)]  
  
 Im folgenden Code Behind-Beispiel werden die Methoden behandelt, die das Schaltflächen <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Ereignis auslöst. Im Beispiel werden die Ergebnisse dieser Methodenaufrufe in Elemente geschrieben, die <xref:System.Windows.Controls.TextBlock> Verwandte Get-Methoden verwenden, um die neuen Eigenschaftswerte als Zeichen folgen auszugeben.  
  
 [!code-csharp[gridIssharedsizescopeProp#3](~/samples/snippets/csharp/VS_Snippets_Wpf/gridIssharedsizescopeProp/CSharp/Window1.xaml.cs#3)]
 [!code-vb[gridIssharedsizescopeProp#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/gridIssharedsizescopeProp/VisualBasic/Window1.xaml.vb#3)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Grid>
- <xref:System.Windows.Controls.Grid.IsSharedSizeScope%2A>
- [Übersicht über Panel-Elemente](panels-overview.md)
