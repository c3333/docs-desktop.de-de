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
# <a name="how-to-share-sizing-properties-between-grids"></a><span data-ttu-id="4a261-102">Gewusst wie: Freigeben von Größeneigenschaften zwischen Grids</span><span class="sxs-lookup"><span data-stu-id="4a261-102">How to: Share Sizing Properties Between Grids</span></span>
<span data-ttu-id="4a261-103">In diesem Beispiel wird gezeigt, wie die Größendaten von Spalten und Zeilen zwischen Elementen gemeinsam genutzt werden, um die <xref:System.Windows.Controls.Grid> Größe konsistent zu halten.</span><span class="sxs-lookup"><span data-stu-id="4a261-103">This example shows how to share the sizing data of columns and rows between <xref:System.Windows.Controls.Grid> elements in order to keep sizing consistent.</span></span>  
  
## <a name="example"></a><span data-ttu-id="4a261-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4a261-104">Example</span></span>  
 <span data-ttu-id="4a261-105">Im folgenden Beispiel werden zwei- <xref:System.Windows.Controls.Grid> Elemente als untergeordnete Elemente eines übergeordneten Elements eingeführt <xref:System.Windows.Controls.DockPanel> .</span><span class="sxs-lookup"><span data-stu-id="4a261-105">The following example introduces two <xref:System.Windows.Controls.Grid> elements as child elements of a parent <xref:System.Windows.Controls.DockPanel>.</span></span> <span data-ttu-id="4a261-106">Die <xref:System.Windows.Controls.Grid.IsSharedSizeScope%2A> angefügte-Eigenschaft von <xref:System.Windows.Controls.Grid> wird für das übergeordnete Element definiert <xref:System.Windows.Controls.DockPanel> .</span><span class="sxs-lookup"><span data-stu-id="4a261-106">The <xref:System.Windows.Controls.Grid.IsSharedSizeScope%2A> attached property of <xref:System.Windows.Controls.Grid> is defined on the parent <xref:System.Windows.Controls.DockPanel>.</span></span>  
  
 <span data-ttu-id="4a261-107">Im Beispiel wird der-Eigenschafts Wert mit zwei- <xref:System.Windows.Controls.Button> Elementen manipuliert. jedes-Element stellt einen der booleschen Eigenschaftswerte dar.</span><span class="sxs-lookup"><span data-stu-id="4a261-107">The example manipulates the property value by using two <xref:System.Windows.Controls.Button> elements; each element represents one of the Boolean property values.</span></span> <span data-ttu-id="4a261-108">Wenn der- <xref:System.Windows.Controls.Grid.IsSharedSizeScope%2A> Eigenschafts Wert auf festgelegt ist `true` , werden bei jedem Spalten-oder Zeilen Mitglied einer Freigabe <xref:System.Windows.Controls.DefinitionBase.SharedSizeGroup%2A> Größen Informationen unabhängig vom Inhalt einer Zeile oder Spalte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4a261-108">When the <xref:System.Windows.Controls.Grid.IsSharedSizeScope%2A> property value is set to `true`, each column or row member of a <xref:System.Windows.Controls.DefinitionBase.SharedSizeGroup%2A> shares sizing information, regardless of the content of a row or column.</span></span>  
  
 [!code-xaml[gridIssharedsizescopeProp#1](~/samples/snippets/csharp/VS_Snippets_Wpf/gridIssharedsizescopeProp/CSharp/Window1.xaml#1)]  
  
 <span data-ttu-id="4a261-109">...</span><span class="sxs-lookup"><span data-stu-id="4a261-109">...</span></span>  
  
 [!code-xaml[gridIssharedsizescopeProp#2](~/samples/snippets/csharp/VS_Snippets_Wpf/gridIssharedsizescopeProp/CSharp/Window1.xaml#2)]  
  
 <span data-ttu-id="4a261-110">Im folgenden Code Behind-Beispiel werden die Methoden behandelt, die das Schaltflächen <xref:System.Windows.Controls.Primitives.ButtonBase.Click> Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="4a261-110">The following code-behind example handles the methods that the button <xref:System.Windows.Controls.Primitives.ButtonBase.Click> event raises.</span></span> <span data-ttu-id="4a261-111">Im Beispiel werden die Ergebnisse dieser Methodenaufrufe in Elemente geschrieben, die <xref:System.Windows.Controls.TextBlock> Verwandte Get-Methoden verwenden, um die neuen Eigenschaftswerte als Zeichen folgen auszugeben.</span><span class="sxs-lookup"><span data-stu-id="4a261-111">The example writes the results of these method calls to <xref:System.Windows.Controls.TextBlock> elements that use related get methods to output the new property values as strings.</span></span>  
  
 [!code-csharp[gridIssharedsizescopeProp#3](~/samples/snippets/csharp/VS_Snippets_Wpf/gridIssharedsizescopeProp/CSharp/Window1.xaml.cs#3)]
 [!code-vb[gridIssharedsizescopeProp#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/gridIssharedsizescopeProp/VisualBasic/Window1.xaml.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="4a261-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a261-112">See also</span></span>

- <xref:System.Windows.Controls.Grid>
- <xref:System.Windows.Controls.Grid.IsSharedSizeScope%2A>
- [<span data-ttu-id="4a261-113">Übersicht über Panel-Elemente</span><span class="sxs-lookup"><span data-stu-id="4a261-113">Panels Overview</span></span>](panels-overview.md)
