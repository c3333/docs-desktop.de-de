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
# <a name="how-to-change-the-flowdirection-of-content-programmatically"></a><span data-ttu-id="222cc-102">Gewusst wie: Programmgesteuertes Ändern der FlowDirection des Inhalts</span><span class="sxs-lookup"><span data-stu-id="222cc-102">How to: Change the FlowDirection of Content Programmatically</span></span>
<span data-ttu-id="222cc-103">In diesem Beispiel wird gezeigt, wie die-Eigenschaft eines Programm gesteuert geändert wird <xref:System.Windows.FrameworkElement.FlowDirection%2A> <xref:System.Windows.Controls.FlowDocumentReader> .</span><span class="sxs-lookup"><span data-stu-id="222cc-103">This example shows how to programmatically change the <xref:System.Windows.FrameworkElement.FlowDirection%2A> property of a <xref:System.Windows.Controls.FlowDocumentReader>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="222cc-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="222cc-104">Example</span></span>  
 <span data-ttu-id="222cc-105"><xref:System.Windows.Controls.Button>Es werden zwei-Elemente erstellt, die jeweils einen der möglichen Werte von darstellen <xref:System.Windows.FlowDirection> .</span><span class="sxs-lookup"><span data-stu-id="222cc-105">Two <xref:System.Windows.Controls.Button> elements are created, each representing one of the possible values of <xref:System.Windows.FlowDirection>.</span></span> <span data-ttu-id="222cc-106">Wenn auf eine Schaltfläche geklickt wird, wird der zugehörige Eigenschafts Wert auf den Inhalt eines mit dem <xref:System.Windows.Controls.FlowDocumentReader> Namen angewendet `tf1` .</span><span class="sxs-lookup"><span data-stu-id="222cc-106">When a button is clicked, the associated property value is applied to the contents of a <xref:System.Windows.Controls.FlowDocumentReader> named `tf1`.</span></span>  <span data-ttu-id="222cc-107">Der-Eigenschafts Wert wird auch in einen mit dem <xref:System.Windows.Controls.TextBlock> Namen geschrieben `txt1` .</span><span class="sxs-lookup"><span data-stu-id="222cc-107">The property value is also written to a <xref:System.Windows.Controls.TextBlock> named `txt1`.</span></span>  
  
 [!code-xaml[FlowDirectionSnippets#_FlowDirectionXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDirectionSnippets/CSharp/Window1.xaml#_flowdirectionxaml)]  
  
## <a name="example"></a><span data-ttu-id="222cc-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="222cc-108">Example</span></span>  
 <span data-ttu-id="222cc-109">Die Ereignisse, die den oben definierten Schaltflächen Klicks zugeordnet sind, werden in einer c#-Code Behind-Datei behandelt.</span><span class="sxs-lookup"><span data-stu-id="222cc-109">The events associated with the button clicks defined above are handled in a C# code-behind file.</span></span>  
  
 [!code-csharp[FlowDirectionSnippets#_FlowDirection](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDirectionSnippets/CSharp/Window1.xaml.cs#_flowdirection)]
 [!code-vb[FlowDirectionSnippets#_FlowDirection](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDirectionSnippets/VisualBasic/Window1.xaml.vb#_flowdirection)]
