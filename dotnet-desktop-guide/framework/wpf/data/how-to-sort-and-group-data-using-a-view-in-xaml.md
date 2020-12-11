---
title: 'Gewusst wie: Sortieren und Gruppieren von Daten mit einer Ansicht in XAML'
description: Erfahren Sie, wie Sie eine Ansicht einer Datensammlung zum Gruppieren, Sortieren und Filtern im Windows Presentation Foundation (WPF) erstellen können.
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], grouping data in views in XAML
- XAML [WPF], sorting data in views
- grouping data in views in XAML [WPF]
- data binding [WPF], sorting data in views in XAML
- sorting data in views in XAML [WPF]
- XAML [WPF], grouping data in views
- views [WPF], sorting data
- views [WPF], grouping data
ms.assetid: 145c8c3f-dbdd-4d0d-816f-90b35eba7eda
ms.openlocfilehash: 9149df0867d6d37cf5160ee1bae1ef969a730641
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976260"
---
# <a name="how-to-sort-and-group-data-using-a-view-in-xaml"></a><span data-ttu-id="147c9-103">Gewusst wie: Sortieren und Gruppieren von Daten mit einer Ansicht in XAML</span><span class="sxs-lookup"><span data-stu-id="147c9-103">How to: Sort and Group Data Using a View in XAML</span></span>
<span data-ttu-id="147c9-104">In diesem Beispiel wird gezeigt, wie eine Sicht einer Datensammlung in erstellt wird [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="147c9-104">This example shows how to create a view of a data collection in [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)].</span></span> <span data-ttu-id="147c9-105">Sichten ermöglichen das Gruppieren, sortieren, Filtern und das Konzept eines aktuellen Elements.</span><span class="sxs-lookup"><span data-stu-id="147c9-105">Views allow for the functionalities of grouping, sorting, filtering, and the notion of a current item.</span></span>  
  
## <a name="example"></a><span data-ttu-id="147c9-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="147c9-106">Example</span></span>  
 <span data-ttu-id="147c9-107">Im folgenden Beispiel wird die statische Ressource mit dem Namen *Places* als eine Auflistung von *Place* -Objekten definiert, wobei jedes *Place* -Objekt aus einem Ortsnamen und dem-Zustand besteht.</span><span class="sxs-lookup"><span data-stu-id="147c9-107">In the following example, the static resource named *places* is defined as a collection of *Place* objects, in which each *Place* object is consisted of a city name and the state.</span></span> <span data-ttu-id="147c9-108">Das Präfix *src* wird dem Namespace zugeordnet, in dem die Datenquellen Speicher *Orte* definiert sind.</span><span class="sxs-lookup"><span data-stu-id="147c9-108">The prefix *src* is mapped to the namespace where the data source *Places* is defined.</span></span> <span data-ttu-id="147c9-109">Das Präfix *SCM* wird zugeordnet, `"clr-namespace:System.ComponentModel;assembly=WindowsBase"` und *DAT* wird zugeordnet `"clr-namespace:System.Windows.Data;assembly=PresentationFramework"` .</span><span class="sxs-lookup"><span data-stu-id="147c9-109">The prefix *scm* maps to `"clr-namespace:System.ComponentModel;assembly=WindowsBase"` and *dat* maps to `"clr-namespace:System.Windows.Data;assembly=PresentationFramework"`.</span></span>  
  
 <span data-ttu-id="147c9-110">Im folgenden Beispiel wird eine Ansicht der Datensammlung erstellt, die nach dem Namen der Stadt sortiert und nach dem-Status gruppiert ist.</span><span class="sxs-lookup"><span data-stu-id="147c9-110">The following example creates a view of the data collection that is sorted by the city name and grouped by the state.</span></span>  
  
 [!code-xaml[CollectionViewSource#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionViewSource/CS/window1.xaml#1)]  
  
 <span data-ttu-id="147c9-111">Die Sicht kann dann eine Bindungs Quelle sein, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="147c9-111">The view can then be a binding source, as in the following example:</span></span>  
  
 [!code-xaml[CollectionViewSource#2](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionViewSource/CS/window1.xaml#2)]  
  
 <span data-ttu-id="147c9-112">Für Bindungen an XML-Daten <xref:System.Windows.Data.XmlDataProvider> , die in einer Ressource definiert sind, muss dem XML-Namen ein @-Zeichen vorangestellt werden.</span><span class="sxs-lookup"><span data-stu-id="147c9-112">For bindings to XML data defined in an <xref:System.Windows.Data.XmlDataProvider> resource, precede the XML name with an @ symbol.</span></span>  
  
 [!code-xaml[CollectionViewSource#XDPChunk](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionViewSource/CS/window1.xaml#xdpchunk)]  
  
 [!code-xaml[CollectionViewSource#Attribute](~/samples/snippets/csharp/VS_Snippets_Wpf/CollectionViewSource/CS/window1.xaml#attribute)]  
  
## <a name="see-also"></a><span data-ttu-id="147c9-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="147c9-113">See also</span></span>

- <xref:System.Windows.Data.CollectionViewSource>
- [<span data-ttu-id="147c9-114">Standardansicht einer Datensammlung erhalten</span><span class="sxs-lookup"><span data-stu-id="147c9-114">Get the Default View of a Data Collection</span></span>](how-to-get-the-default-view-of-a-data-collection.md)
- [<span data-ttu-id="147c9-115">Übersicht über die Datenbindung</span><span class="sxs-lookup"><span data-stu-id="147c9-115">Data Binding Overview</span></span>](/dotnet/desktop-wpf/data/data-binding-overview)
- [<span data-ttu-id="147c9-116">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="147c9-116">How-to Topics</span></span>](data-binding-how-to-topics.md)
