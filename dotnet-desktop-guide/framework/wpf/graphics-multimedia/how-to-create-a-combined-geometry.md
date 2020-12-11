---
title: 'Gewusst wie: Erstellen von kombinierten Geometrien'
ms.date: 03/30/2017
helpviewer_keywords:
- combining geometries [WPF]
- graphics [WPF], combining geometries
- geometries [WPF], combining
ms.assetid: 54c3277c-6b6e-4b25-91be-fda0bbc706b4
ms.openlocfilehash: c5ebe87abd4c2cf70f8fa17f1fcc773293f3ad27
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977614"
---
# <a name="how-to-create-a-combined-geometry"></a><span data-ttu-id="7e30d-102">Gewusst wie: Erstellen von kombinierten Geometrien</span><span class="sxs-lookup"><span data-stu-id="7e30d-102">How to: Create a Combined Geometry</span></span>
<span data-ttu-id="7e30d-103">Dieses Beispiel zeigt, wie Geometrien kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="7e30d-103">This example shows how to combine geometries.</span></span> <span data-ttu-id="7e30d-104">Verwenden Sie zum Kombinieren zweier Geometrien ein- <xref:System.Windows.Media.CombinedGeometry> Objekt.</span><span class="sxs-lookup"><span data-stu-id="7e30d-104">To combine two geometries, use a <xref:System.Windows.Media.CombinedGeometry> object.</span></span> <span data-ttu-id="7e30d-105">Legen <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> Sie die <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> Eigenschaften und mit den zwei zu kombinierenden Geometrien fest, und legen Sie die- <xref:System.Windows.Media.CombinedGeometry.GeometryCombineMode%2A> Eigenschaft fest, die bestimmt, wie die Geometrien zusammen mit `Union` , `Intersect` , oder kombiniert werden `Exclude` `Xor` .</span><span class="sxs-lookup"><span data-stu-id="7e30d-105">Set its <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> and <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> properties  with the two geometries to combine, and set the <xref:System.Windows.Media.CombinedGeometry.GeometryCombineMode%2A> property, which determines how the geometries will be combined together, to `Union`, `Intersect`, `Exclude`, or `Xor`.</span></span>  
  
 <span data-ttu-id="7e30d-106">Um eine zusammengesetzte Geometrie aus zwei oder mehr Geometrien zu erstellen, verwenden Sie eine <xref:System.Windows.Media.GeometryGroup> .</span><span class="sxs-lookup"><span data-stu-id="7e30d-106">To create a composite geometry from two or more geometries, use a <xref:System.Windows.Media.GeometryGroup>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7e30d-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7e30d-107">Example</span></span>  
 <span data-ttu-id="7e30d-108">Im folgenden Beispiel <xref:System.Windows.Media.CombinedGeometry> wird ein mit einem Geometry-kombinierungsmodus von definiert `Exclude` .</span><span class="sxs-lookup"><span data-stu-id="7e30d-108">In the following example, a <xref:System.Windows.Media.CombinedGeometry> is defined with a geometry combine mode of `Exclude`.</span></span>  <span data-ttu-id="7e30d-109">Sowohl als <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> auch <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> werden als Kreise desselben Radius definiert, wobei die zentriert durch 50 versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="7e30d-109">Both <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> and the <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> are defined as circles of the same radius, but with centers offset by 50.</span></span>  
  
 [!code-xaml[GeometrySample#21](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#21)]  
  
 <span data-ttu-id="7e30d-110">![Ergebnisse des Exclude-Kombinationsmodus](./media/mil-task-combined-geometry-exclude.PNG "mil_task_combined_geometry_exclude")</span><span class="sxs-lookup"><span data-stu-id="7e30d-110">![Results of the Exclude combine mode](./media/mil-task-combined-geometry-exclude.PNG "mil_task_combined_geometry_exclude")</span></span>  
<span data-ttu-id="7e30d-111">Kombinierter Geometry-Ausschluss</span><span class="sxs-lookup"><span data-stu-id="7e30d-111">Combined Geometry Exclude</span></span>  
  
 <span data-ttu-id="7e30d-112">Im folgenden Markup <xref:System.Windows.Media.CombinedGeometry> wird eine mit dem kombinierungsmodus definiert `Intersect` .</span><span class="sxs-lookup"><span data-stu-id="7e30d-112">In the following markup, a <xref:System.Windows.Media.CombinedGeometry> is defined with a combine mode of `Intersect`.</span></span>  <span data-ttu-id="7e30d-113">Sowohl als <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> auch <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> werden als Kreise desselben Radius definiert, wobei die zentriert durch 50 versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="7e30d-113">Both <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> and the <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> are defined as circles of the same radius, but with centers offset by 50.</span></span>  
  
 [!code-xaml[GeometrySample#22](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#22)]  
  
 <span data-ttu-id="7e30d-114">![Ergebnisse des Intersect-Kombinationsmodus](./media/mil-task-combined-geometry-intersect.PNG "mil_task_combined_geometry_intersect")</span><span class="sxs-lookup"><span data-stu-id="7e30d-114">![Results of the Intersect combine mode](./media/mil-task-combined-geometry-intersect.PNG "mil_task_combined_geometry_intersect")</span></span>  
<span data-ttu-id="7e30d-115">Kombinierte Geometrie Intersect</span><span class="sxs-lookup"><span data-stu-id="7e30d-115">Combined Geometry Intersect</span></span>  
  
 <span data-ttu-id="7e30d-116">Im folgenden Markup <xref:System.Windows.Media.CombinedGeometry> wird eine mit dem kombinierungsmodus definiert `Union` .</span><span class="sxs-lookup"><span data-stu-id="7e30d-116">In the following markup, a <xref:System.Windows.Media.CombinedGeometry> is defined with a combine mode of `Union`.</span></span>  <span data-ttu-id="7e30d-117">Sowohl als <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> auch <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> werden als Kreise desselben Radius definiert, wobei die zentriert durch 50 versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="7e30d-117">Both <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> and the <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> are defined as circles of the same radius, but with centers offset by 50.</span></span>  
  
 [!code-xaml[GeometrySample#23](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#23)]  
  
 <span data-ttu-id="7e30d-118">![Ergebnisse des Union-Kombinationsmodus](./media/mil-task-combined-geometry-union.PNG "mil_task_combined_geometry_union")</span><span class="sxs-lookup"><span data-stu-id="7e30d-118">![Results of the Union combine mode](./media/mil-task-combined-geometry-union.PNG "mil_task_combined_geometry_union")</span></span>  
<span data-ttu-id="7e30d-119">Kombinierte Geometrie Union</span><span class="sxs-lookup"><span data-stu-id="7e30d-119">Combined Geometry Union</span></span>  
  
 <span data-ttu-id="7e30d-120">Im folgenden Markup <xref:System.Windows.Media.CombinedGeometry> wird eine mit dem kombinierungsmodus definiert `Xor` .</span><span class="sxs-lookup"><span data-stu-id="7e30d-120">In the following markup, a <xref:System.Windows.Media.CombinedGeometry> is defined with a combine mode of `Xor`.</span></span>  <span data-ttu-id="7e30d-121">Sowohl als <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> auch <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> werden als Kreise desselben Radius definiert, wobei die zentriert durch 50 versetzt werden.</span><span class="sxs-lookup"><span data-stu-id="7e30d-121">Both <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> and the <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> are defined as circles of the same radius, but with centers offset by 50.</span></span>  
  
 [!code-xaml[GeometrySample#24](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#24)]  
  
 <span data-ttu-id="7e30d-122">![Ergebnisse des Xor-Kombinationsmodus](./media/mil-task-combined-geometry-xor.PNG "mil_task_combined_geometry_xor")</span><span class="sxs-lookup"><span data-stu-id="7e30d-122">![Results of the Xor combine mode](./media/mil-task-combined-geometry-xor.PNG "mil_task_combined_geometry_xor")</span></span>  
<span data-ttu-id="7e30d-123">Kombiniertes Geometry-XOR</span><span class="sxs-lookup"><span data-stu-id="7e30d-123">Combined Geometry Xor</span></span>
