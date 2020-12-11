---
title: 'Gewusst wie: Auswählen von StackPanel oder DockPanel'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- controls [WPF], DockPanel
- DockPanel control [WPF], StackPanel control compared to
- StackPanel control [WPF], DockPanel control compared to
- controls [WPF], StackPanel
ms.assetid: f9239086-451f-42e6-81f7-ef89ef349742
ms.openlocfilehash: bdf4b38e67a7856136224368e86609c135e5ad6f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978086"
---
# <a name="how-to-choose-between-stackpanel-and-dockpanel"></a>Gewusst wie: Auswählen von StackPanel oder DockPanel
In diesem Beispiel wird gezeigt, wie Sie zwischen <xref:System.Windows.Controls.StackPanel> der Verwendung eines oder eines auswählen, <xref:System.Windows.Controls.DockPanel> Wenn Sie Inhalt in einem Stapeln <xref:System.Windows.Controls.Panel> .

## <a name="example"></a>Beispiel
 Obwohl Sie entweder <xref:System.Windows.Controls.DockPanel> oder <xref:System.Windows.Controls.StackPanel> zum Stapeln untergeordneter Elemente verwenden können, werden die beiden-Steuerelemente nicht immer die gleichen Ergebnisse liefern. Beispielsweise kann sich die Reihenfolge, in der Sie untergeordnete Elemente platzieren, auf die Größe der untergeordneten Elemente in einer, <xref:System.Windows.Controls.DockPanel> aber nicht in einer auswirken <xref:System.Windows.Controls.StackPanel> . Dieses unterschiedliche Verhalten tritt <xref:System.Windows.Controls.StackPanel> auf, weil Measures in der Stapel Richtung bei [Double. PositiveInfinity](xref:System.Double.PositiveInfinity), jedoch <xref:System.Windows.Controls.DockPanel> nur die verfügbare Größe messen.

 Im folgenden Beispiel wird dieser Hauptunterschied zwischen <xref:System.Windows.Controls.DockPanel> und veranschaulicht <xref:System.Windows.Controls.StackPanel> .

 [!code-cpp[StackPanelOvw4#1](~/samples/snippets/cpp/VS_Snippets_Wpf/StackPanelOvw4/CPP/StackPanel_Ovw_Sample4.cpp#1)]
 [!code-csharp[StackPanelOvw4#1](~/samples/snippets/csharp/VS_Snippets_Wpf/StackPanelOvw4/CSharp/StackPanel_Ovw_Sample4.cs#1)]
 [!code-vb[StackPanelOvw4#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/StackPanelOvw4/VisualBasic/StackPanelSamp.vb#1)]
 [!code-xaml[StackPanelOvw4#1](~/samples/snippets/xaml/VS_Snippets_Wpf/StackPanelOvw4/XAML/default.xaml#1)]

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.StackPanel>
- <xref:System.Windows.Controls.DockPanel>
- [Übersicht über Panel-Elemente](panels-overview.md)
