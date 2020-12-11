---
title: 'Gewusst wie: Programmgesteuertes Ändern der FlowDirection des Inhalts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- FlowDirection property [WPF], changing programmatically
- documents [WPF], changing FlowDirection property programmatically
ms.assetid: 02f5a8ba-f8c0-4e5a-84b9-4c5bf12922a2
ms.openlocfilehash: ec159ed0efce8b5514788331e8715a55e7a8a638
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976935"
---
# <a name="how-to-change-the-flowdirection-of-content-programmatically"></a>Gewusst wie: Programmgesteuertes Ändern der FlowDirection des Inhalts
In diesem Beispiel wird gezeigt, wie die-Eigenschaft eines Programm gesteuert geändert wird <xref:System.Windows.FrameworkElement.FlowDirection%2A> <xref:System.Windows.Controls.FlowDocumentReader> .  
  
## <a name="example"></a>Beispiel  
 <xref:System.Windows.Controls.Button>Es werden zwei-Elemente erstellt, die jeweils einen der möglichen Werte von darstellen <xref:System.Windows.FlowDirection> . Wenn auf eine Schaltfläche geklickt wird, wird der zugehörige Eigenschafts Wert auf den Inhalt eines mit dem <xref:System.Windows.Controls.FlowDocumentReader> Namen angewendet `tf1` .  Der-Eigenschafts Wert wird auch in einen mit dem <xref:System.Windows.Controls.TextBlock> Namen geschrieben `txt1` .  
  
 [!code-xaml[FlowDirectionSnippets#_FlowDirectionXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDirectionSnippets/CSharp/Window1.xaml#_flowdirectionxaml)]  
  
## <a name="example"></a>Beispiel  
 Die Ereignisse, die den oben definierten Schaltflächen Klicks zugeordnet sind, werden in einer c#-Code Behind-Datei behandelt.  
  
 [!code-csharp[FlowDirectionSnippets#_FlowDirection](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDirectionSnippets/CSharp/Window1.xaml.cs#_flowdirection)]
 [!code-vb[FlowDirectionSnippets#_FlowDirection](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDirectionSnippets/VisualBasic/Window1.xaml.vb#_flowdirection)]
