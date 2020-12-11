---
title: 'Gewusst wie: Abrunden der Ecken einer "RectangleGeometry"'
ms.date: 03/30/2017
helpviewer_keywords:
- corners [WPF], rounding
- RectangleGeometry class [WPF], rounding corners
- graphics [WPF], rounding corners of RectangleGeometry objects [WPF]
- rounding corners of RectangleGeometry objects [WPF]
ms.assetid: 926644bc-1357-4c0b-ac81-694bd090ae87
ms.openlocfilehash: eb2f173bedb903e12b2795264c684524cfa09825
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977269"
---
# <a name="how-to-round-the-corners-of-a-rectanglegeometry"></a>Gewusst wie: Abrunden der Ecken einer "RectangleGeometry"
Um die Ecken eines zu runden <xref:System.Windows.Media.RectangleGeometry> , legen <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> Sie dessen-Eigenschaft und-Eigenschaft <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> auf einen Wert größer 0 (null) fest. Je größer der Wert ist, desto größer ist die Ecke des Rechtecks.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden mehrere <xref:System.Windows.Media.RectangleGeometry> -Objekte mit unterschiedlichen <xref:System.Windows.Media.RectangleGeometry.RadiusX%2A> -und- <xref:System.Windows.Media.RectangleGeometry.RadiusY%2A> Einstellungen angezeigt. Die <xref:System.Windows.Media.RectangleGeometry> Objekte werden mithilfe von- <xref:System.Windows.Shapes.Path> Elementen angezeigt.  
  
 [!code-xaml[GeometryOverviewSamples_snip#GraphicsMMRoundedRectangleGeometryExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/GeometryOverviewSamples_snip/CS/RectangleGeometryRoundedCornerExample.xaml#graphicsmmroundedrectanglegeometryexamplewholepage)]  
  
 ![Rechtecke mit unterschiedlichen RADIUS-&#47;radiin-Einstellungen](./media/graphicsmm-rounded.png "graphicsmm_rounded")  
Rechtecke mit abgerundeten Ecken  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Geometrie](geometry-overview.md)
- [Erstellen einer zusammengesetzten Form](how-to-create-a-composite-shape.md)
- [Erstellen einer Form mithilfe einer PathGeometry](how-to-create-a-shape-by-using-a-pathgeometry.md)
