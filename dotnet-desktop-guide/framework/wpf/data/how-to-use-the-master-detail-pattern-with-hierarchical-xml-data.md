---
title: 'Gewusst wie: Verwenden des Master/Detail-Musters mit hierarchischen XML-Daten'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], Master-Detail data paradigm
- Master-Detail data paradigm
ms.assetid: eb8dbdd8-5871-42bb-a16b-04e655fea677
ms.openlocfilehash: 0fe42d57fcaf4acee09340fdb3f5df73d7291566
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976549"
---
# <a name="how-to-use-the-master-detail-pattern-with-hierarchical-xml-data"></a><span data-ttu-id="b160d-102">Gewusst wie: Verwenden des Master/Detail-Musters mit hierarchischen XML-Daten</span><span class="sxs-lookup"><span data-stu-id="b160d-102">How to: Use the Master-Detail Pattern with Hierarchical XML Data</span></span>
<span data-ttu-id="b160d-103">Dieses Beispiel zeigt, wie das Master/Detail-Szenario mit XML-Daten implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="b160d-103">This example shows how to implement the master-detail scenario with XML data.</span></span>  
  
## <a name="example"></a><span data-ttu-id="b160d-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b160d-104">Example</span></span>  
 <span data-ttu-id="b160d-105">Dieses Beispiel ist die XML-Daten Version des Beispiels, das unter [Verwenden des Master-Detail Musters mit hierarchischen Daten](how-to-use-the-master-detail-pattern-with-hierarchical-data.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="b160d-105">This example is the XML data version of the example discussed in [Use the Master-Detail Pattern with Hierarchical Data](how-to-use-the-master-detail-pattern-with-hierarchical-data.md).</span></span> <span data-ttu-id="b160d-106">In diesem Beispiel werden die Daten aus der Datei entfernt `League.xml` .</span><span class="sxs-lookup"><span data-stu-id="b160d-106">In this example, the data is from the file `League.xml`.</span></span> <span data-ttu-id="b160d-107">Beachten Sie, wie das dritte-Steuerelement die <xref:System.Windows.Controls.ListBox> Auswahl Änderungen im zweiten-Steuerelement nachverfolgt <xref:System.Windows.Controls.ListBox> , indem es an die <xref:System.Windows.Controls.Primitives.Selector.SelectedValue%2A></span><span class="sxs-lookup"><span data-stu-id="b160d-107">Note how the third <xref:System.Windows.Controls.ListBox> control tracks selection changes in the second <xref:System.Windows.Controls.ListBox> by binding to its <xref:System.Windows.Controls.Primitives.Selector.SelectedValue%2A> property.</span></span>  
  
 [!code-xaml[MasterDetailXml#HowTo1](~/samples/snippets/csharp/VS_Snippets_Wpf/MasterDetailXml/CS/Window1.xaml#howto1)]  
[!code-xaml[MasterDetailXml#HowTo2](~/samples/snippets/csharp/VS_Snippets_Wpf/MasterDetailXml/CS/Window1.xaml#howto2)]  
  
## <a name="see-also"></a><span data-ttu-id="b160d-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b160d-108">See also</span></span>

- <xref:System.Windows.HierarchicalDataTemplate>
- [<span data-ttu-id="b160d-109">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="b160d-109">How-to Topics</span></span>](data-binding-how-to-topics.md)
