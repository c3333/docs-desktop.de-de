---
title: 'Gewusst wie: Abrufen der Standardansicht einer Datenauflistung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data collections [WPF], creating views of
- data binding [WPF], creating views of data collections
ms.assetid: b641e96c-c2f6-42ea-9c5d-bac81176ad65
ms.openlocfilehash: 17ec2a40bf2c274f50b39875a23541932438a317
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978142"
---
# <a name="how-to-get-the-default-view-of-a-data-collection"></a><span data-ttu-id="3d0a5-102">Gewusst wie: Abrufen der Standardansicht einer Datenauflistung</span><span class="sxs-lookup"><span data-stu-id="3d0a5-102">How to: Get the Default View of a Data Collection</span></span>
<span data-ttu-id="3d0a5-103">In Sichten kann die gleiche Datensammlung je nach Sortier-, Filter-oder Gruppierungs Kriterien auf unterschiedliche Weise angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="3d0a5-103">Views allow the same data collection to be viewed in different ways, depending on sorting, filtering, or grouping criteria.</span></span> <span data-ttu-id="3d0a5-104">Jede Sammlung verfügt über eine freigegebene Standardansicht, die als tatsächliche Bindungs Quelle verwendet wird, wenn eine Bindung eine Auflistung als Quelle angibt.</span><span class="sxs-lookup"><span data-stu-id="3d0a5-104">Every collection has one shared default view, which is used as the actual binding source when a binding specifies a collection as its source.</span></span> <span data-ttu-id="3d0a5-105">Dieses Beispiel zeigt, wie Sie die Standardansicht einer Auflistung erhalten.</span><span class="sxs-lookup"><span data-stu-id="3d0a5-105">This example shows how to get the default view of a collection.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3d0a5-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3d0a5-106">Example</span></span>  
 <span data-ttu-id="3d0a5-107">Um die Ansicht zu erstellen, benötigen Sie einen Objekt Verweis auf die Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3d0a5-107">To create the view, you need an object reference to the collection.</span></span> <span data-ttu-id="3d0a5-108">Dieses Datenobjekt kann abgerufen werden, indem Sie auf Ihr eigenes Code-Behind-Objekt verweisen, indem Sie den Datenkontext erhalten, indem Sie eine Eigenschaft der Datenquelle erhalten oder eine Eigenschaft der Bindung erhalten.</span><span class="sxs-lookup"><span data-stu-id="3d0a5-108">This data object can be obtained by referencing your own code-behind object, by getting the data context, by getting a property of the data source, or by getting a property of the binding.</span></span> <span data-ttu-id="3d0a5-109">Dieses Beispiel zeigt, wie Sie den <xref:System.Windows.FrameworkElement.DataContext%2A> eines Datenobjekts abrufen und verwenden können, um die Standard Auflistungs Ansicht für diese Auflistung direkt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3d0a5-109">This example shows how to get the <xref:System.Windows.FrameworkElement.DataContext%2A> of a data object and use it to directly obtain the default collection view for this collection.</span></span>  
  
 [!code-csharp[CollectionView#2](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionView/CSharp/Page1.xaml.cs#2)]
 [!code-vb[CollectionView#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CollectionView/VisualBasic/Page1.xaml.vb#2)]  
  
 <span data-ttu-id="3d0a5-110">In diesem Beispiel ist das Stamm Element ein <xref:System.Windows.Controls.StackPanel> .</span><span class="sxs-lookup"><span data-stu-id="3d0a5-110">In this example, the root element is a <xref:System.Windows.Controls.StackPanel>.</span></span> <span data-ttu-id="3d0a5-111">Der <xref:System.Windows.FrameworkElement.DataContext%2A> wird auf *MyDatasource* festgelegt, was auf einen Datenanbieter verweist, <xref:System.Collections.ObjectModel.ObservableCollection%601> der ein von *Order* -Objekten ist.</span><span class="sxs-lookup"><span data-stu-id="3d0a5-111">The <xref:System.Windows.FrameworkElement.DataContext%2A> is set to *myDataSource*, which refers to a data provider that is an <xref:System.Collections.ObjectModel.ObservableCollection%601> of *Order* objects.</span></span>  
  
 [!code-xaml[CollectionView#CollectionViewDataContext](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionView/CSharp/Page1.xaml#collectionviewdatacontext)]  
  
 <span data-ttu-id="3d0a5-112">Alternativ können Sie mithilfe der-Klasse instanziieren und an Ihre eigene Auflistungs Ansicht binden <xref:System.Windows.Data.CollectionViewSource> .</span><span class="sxs-lookup"><span data-stu-id="3d0a5-112">Alternatively, you can instantiate and bind to your own collection view using the <xref:System.Windows.Data.CollectionViewSource> class.</span></span> <span data-ttu-id="3d0a5-113">Diese Auflistungs Ansicht wird nur von Steuerelementen gemeinsam genutzt, die direkt an Sie gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="3d0a5-113">This collection view is only shared by controls that bind to it directly.</span></span> <span data-ttu-id="3d0a5-114">Ein Beispiel finden Sie im Abschnitt How to Create a View in der [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview).</span><span class="sxs-lookup"><span data-stu-id="3d0a5-114">For an example, see the How to Create a View section in the [Data Binding Overview](/dotnet/desktop-wpf/data/data-binding-overview).</span></span>  
  
 <span data-ttu-id="3d0a5-115">Beispiele für die von einer Auflistungs Ansicht bereitgestellte Funktionalität finden Sie unter [Sortieren von Daten in einer Ansicht](how-to-sort-data-in-a-view.md), [Filtern von Daten in einer Ansicht](how-to-filter-data-in-a-view.md)und [Navigieren durch die Objekte in einer Daten CollectionView](how-to-navigate-through-the-objects-in-a-data-collectionview.md).</span><span class="sxs-lookup"><span data-stu-id="3d0a5-115">For examples of the functionality provided by a collection view, see [Sort Data in a View](how-to-sort-data-in-a-view.md), [Filter Data in a View](how-to-filter-data-in-a-view.md), and [Navigate Through the Objects in a Data CollectionView](how-to-navigate-through-the-objects-in-a-data-collectionview.md).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="3d0a5-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3d0a5-116">See also</span></span>

- [<span data-ttu-id="3d0a5-117">Sortieren und Gruppieren von Daten mit einer Ansicht in XAML</span><span class="sxs-lookup"><span data-stu-id="3d0a5-117">Sort and Group Data Using a View in XAML</span></span>](how-to-sort-and-group-data-using-a-view-in-xaml.md)
- [<span data-ttu-id="3d0a5-118">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="3d0a5-118">How-to Topics</span></span>](data-binding-how-to-topics.md)
