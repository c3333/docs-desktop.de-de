---
title: 'Gewusst wie: Verwenden eines Rasters für automatisches Layout'
ms.date: 03/30/2017
helpviewer_keywords:
- grids [WPF], automatic layout
- automatic layout [WPF], grid use
ms.assetid: ab9de407-e0c1-4047-bdf0-24951bf73879
ms.openlocfilehash: 5389d8d6130367d36a5c81b3bdc316c989474ce2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976278"
---
# <a name="how-to-use-a-grid-for-automatic-layout"></a>Gewusst wie: Verwenden eines Rasters für automatisches Layout
Dieses Beispiel beschreibt, wie ein Raster im automatischen Layoutansatz zum Erstellen einer lokalisierbaren Anwendung verwendet wird.  
  
 Die Lokalisierung eines [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] kann ein zeitaufwändiger Prozess sein. Oft müssen Lokalisierungsexperten die Größe von Elementen ändern und sie neu positionieren, um Text zu übersetzen. In der letzten Sprache, in der eine [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] für die erforderliche Anpassung angepasst wurde. Nun können Sie mit den Funktionen von [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Elemente entwerfen, die die Notwendigkeit einer Anpassung verringern. Der Ansatz zum Schreiben von Anwendungen, die leichter neu skaliert und neu positioniert werden können, heißt `auto layout` .  
  
 Das folgende [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beispiel veranschaulicht die Verwendung eines Rasters, um einige Schaltflächen und Text zu positionieren. Beachten Sie, dass die Höhe und Breite der Zellen auf festgelegt ist. aus diesem `Auto` Grund wird die Zelle, die die Schaltfläche mit einem Bild enthält, an das Bild angepasst. Da das <xref:System.Windows.Controls.Grid> Element an seinen Inhalt angepasst werden kann, kann es nützlich sein, wenn das automatische Layoutverfahren zum Entwerfen von Anwendungen eingesetzt wird, die lokalisiert werden können.  
  
## <a name="example"></a>Beispiel  
 Das folgende Beispiel veranschaulicht die Verwendung von eines Rasters.  
  
 [!code-xaml[LocalizationGrid#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LocalizationGrid/CS/Pane1.xaml#1)]  
  
 Die folgende Grafik zeigt die Ausgabe des Codebeispiels.  
  
 ![Rasterbeispiel](./media/glob-grid.png "glob_grid")  
Raster  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Verwendung eines automatischen Layouts](use-automatic-layout-overview.md)
- [Verwenden des automatischen Layouts zum Erstellen einer Schaltfläche](how-to-use-automatic-layout-to-create-a-button.md)
