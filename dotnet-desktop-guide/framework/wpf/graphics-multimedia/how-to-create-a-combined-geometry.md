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
# <a name="how-to-create-a-combined-geometry"></a>Gewusst wie: Erstellen von kombinierten Geometrien
Dieses Beispiel zeigt, wie Geometrien kombiniert werden. Verwenden Sie zum Kombinieren zweier Geometrien ein- <xref:System.Windows.Media.CombinedGeometry> Objekt. Legen <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> Sie die <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> Eigenschaften und mit den zwei zu kombinierenden Geometrien fest, und legen Sie die- <xref:System.Windows.Media.CombinedGeometry.GeometryCombineMode%2A> Eigenschaft fest, die bestimmt, wie die Geometrien zusammen mit `Union` , `Intersect` , oder kombiniert werden `Exclude` `Xor` .  
  
 Um eine zusammengesetzte Geometrie aus zwei oder mehr Geometrien zu erstellen, verwenden Sie eine <xref:System.Windows.Media.GeometryGroup> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel <xref:System.Windows.Media.CombinedGeometry> wird ein mit einem Geometry-kombinierungsmodus von definiert `Exclude` .  Sowohl als <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> auch <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> werden als Kreise desselben Radius definiert, wobei die zentriert durch 50 versetzt werden.  
  
 [!code-xaml[GeometrySample#21](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#21)]  
  
 ![Ergebnisse des Exclude-Kombinationsmodus](./media/mil-task-combined-geometry-exclude.PNG "mil_task_combined_geometry_exclude")  
Kombinierter Geometry-Ausschluss  
  
 Im folgenden Markup <xref:System.Windows.Media.CombinedGeometry> wird eine mit dem kombinierungsmodus definiert `Intersect` .  Sowohl als <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> auch <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> werden als Kreise desselben Radius definiert, wobei die zentriert durch 50 versetzt werden.  
  
 [!code-xaml[GeometrySample#22](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#22)]  
  
 ![Ergebnisse des Intersect-Kombinationsmodus](./media/mil-task-combined-geometry-intersect.PNG "mil_task_combined_geometry_intersect")  
Kombinierte Geometrie Intersect  
  
 Im folgenden Markup <xref:System.Windows.Media.CombinedGeometry> wird eine mit dem kombinierungsmodus definiert `Union` .  Sowohl als <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> auch <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> werden als Kreise desselben Radius definiert, wobei die zentriert durch 50 versetzt werden.  
  
 [!code-xaml[GeometrySample#23](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#23)]  
  
 ![Ergebnisse des Union-Kombinationsmodus](./media/mil-task-combined-geometry-union.PNG "mil_task_combined_geometry_union")  
Kombinierte Geometrie Union  
  
 Im folgenden Markup <xref:System.Windows.Media.CombinedGeometry> wird eine mit dem kombinierungsmodus definiert `Xor` .  Sowohl als <xref:System.Windows.Media.CombinedGeometry.Geometry1%2A> auch <xref:System.Windows.Media.CombinedGeometry.Geometry2%2A> werden als Kreise desselben Radius definiert, wobei die zentriert durch 50 versetzt werden.  
  
 [!code-xaml[GeometrySample#24](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometrySample/CS/combininggeometriesexample.xaml#24)]  
  
 ![Ergebnisse des Xor-Kombinationsmodus](./media/mil-task-combined-geometry-xor.PNG "mil_task_combined_geometry_xor")  
Kombiniertes Geometry-XOR
