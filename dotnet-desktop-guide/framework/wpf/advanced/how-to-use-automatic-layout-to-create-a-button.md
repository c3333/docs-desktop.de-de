---
title: 'Gewusst wie: Verwenden des automatischen Layouts zum Erstellen einer Schaltfläche'
ms.date: 03/30/2017
helpviewer_keywords:
- Button controls [WPF], creating with automatic layout
- automatic layout [WPF], creating buttons
ms.assetid: 96c206d0-9e77-4784-9d2d-5045aed2021c
ms.openlocfilehash: 05b874f9894841d3c318ee131d15165111fd596a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976271"
---
# <a name="how-to-use-automatic-layout-to-create-a-button"></a>Gewusst wie: Verwenden des automatischen Layouts zum Erstellen einer Schaltfläche
Dieses Beispiel beschreibt, wie der automatische Layoutansatz zum Erstellen einer Schaltfläche in einer lokalisierbaren Anwendung verwendet wird.  
  
 Die Lokalisierung eines [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] kann ein zeitaufwändiger Prozess sein. Oft müssen Lokalisierungsexperten die Größe von Elementen ändern und sie neu positionieren, um Text zu übersetzen. In der letzten Sprache, in der eine [!INCLUDE[TLA2#tla_ui](../../../includes/tla2sharptla-ui-md.md)] für die erforderliche Anpassung angepasst wurde. Nun können Sie mit den Funktionen von [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Elemente entwerfen, die die Notwendigkeit einer Anpassung verringern. Der Ansatz zum Schreiben von Anwendungen, die einfacher geändert und neu positioniert werden können, wird als bezeichnet `automatic layout` .  
  
## <a name="example"></a>Beispiel  

In den folgenden beiden [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beispielen werden Anwendungen erstellt, die eine Schaltfläche instanziieren, eine mit englischem Text und eine mit spanischem Text. Beachten Sie, dass der Code mit Ausnahme des Texts der gleiche ist; die Schaltfläche wird an den Text angepasst.

[!code-xaml[LocalizationBtn_snip#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LocalizationBtn_snip/CS/Pane1.xaml#1)]  
  
[!code-xaml[LocalizationBtn#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LocalizationBtn/CS/Pane1.xaml#1)]  
  
 Die folgende Grafik zeigt die Ausgabe der Codebeispiele mit Schaltflächen, die automatisch geändert werden könnten:
  
 ![Die gleiche Schaltfläche mit Text in unterschiedlichen Sprachen](./media/use-automatic-layout-overview/auto-resizable-button.png)  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über die Verwendung eines automatischen Layouts](use-automatic-layout-overview.md)
- [Verwenden eines Rasters für automatisches Layout](how-to-use-a-grid-for-automatic-layout.md)
