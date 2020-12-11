---
title: 'Gewusst wie: Erstellen eines benutzerdefinierten Bereichselements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Panel control [WPF]
- custom Panel elements [WPF]
ms.assetid: e0df4f1e-8c07-4e86-89a3-e22acfffdc2a
ms.openlocfilehash: 31edc75114c5dad613e5b65e7d8b051e2c3713af
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978074"
---
# <a name="how-to-create-a-custom-panel-element"></a>Gewusst wie: Erstellen eines benutzerdefinierten Bereichselements
## <a name="example"></a>Beispiel  
 In diesem Beispiel wird gezeigt, wie das Standardlayoutverhalten des <xref:System.Windows.Controls.Panel> -Elements überschrieben und benutzerdefinierte Layoutelemente erstellt werden, die von abgeleitet werden <xref:System.Windows.Controls.Panel> .  
  
 Im Beispiel wird ein einfaches benutzerdefiniertes <xref:System.Windows.Controls.Panel> Element namens definiert `PlotPanel` , das untergeordnete Elemente nach zwei hart codierten x-und y-Koordinaten positioniert. In diesem Beispiel `x` sind und auf `y` festgelegt `50` . Daher werden alle untergeordneten Elemente an dieser Stelle auf der x-und der y-Achse positioniert.  
  
 Zum Implementieren von benutzerdefiniertem <xref:System.Windows.Controls.Panel> Verhalten verwendet das Beispiel die <xref:System.Windows.FrameworkElement.MeasureOverride%2A> -Methode und die- <xref:System.Windows.FrameworkElement.ArrangeOverride%2A> Methode. Jede Methode gibt die <xref:System.Windows.Size> Daten zurück, die erforderlich sind, um untergeordnete Elemente zu positionieren und zu Rendering.  
  
 [!code-cpp[PlotPanel#1](~/samples/snippets/cpp/VS_Snippets_Wpf/PlotPanel/CPP/PlotPanel.cpp#1)]
 [!code-csharp[PlotPanel#1](~/samples/snippets/csharp/VS_Snippets_Wpf/PlotPanel/CSharp/PlotPanel.cs#1)]
 [!code-vb[PlotPanel#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PlotPanel/VisualBasic/PlotPanel.vb#1)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Panel>
- [Übersicht über Panel-Elemente](panels-overview.md)
