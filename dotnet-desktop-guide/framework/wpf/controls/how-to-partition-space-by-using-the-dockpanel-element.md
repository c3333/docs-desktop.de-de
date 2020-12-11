---
title: 'Gewusst wie: Aufteilen von Bereichen mithilfe des DockPanel-Elements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- controls [WPF], DockPanel
- DockPanel control [WPF], partitioning space
- partitioning space [WPF]
ms.assetid: a219b9e5-b205-4438-89b5-0a137ac463ab
ms.openlocfilehash: 3682acc559e4e8740b97f781b6f927eac1e380d7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978160"
---
# <a name="how-to-partition-space-by-using-the-dockpanel-element"></a>Gewusst wie: Aufteilen von Bereichen mithilfe des DockPanel-Elements
Im folgenden Beispiel wird ein einfaches [!INCLUDE[TLA#tla_ui](../../../includes/tlasharptla-ui-md.md)] Framework mit einem- <xref:System.Windows.Controls.DockPanel> Element erstellt. Der <xref:System.Windows.Controls.DockPanel> verfügbare Speicherplatz der Partitionen für seine untergeordneten Elemente.  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel wird die- <xref:System.Windows.Controls.DockPanel.Dock%2A> Eigenschaft, die eine angefügte Eigenschaft ist, zum Andocken zweier identischer <xref:System.Windows.Controls.Border> Elemente an der <xref:System.Windows.Controls.Dock.Top> des partitionierten Raums verwendet. Ein drittes <xref:System.Windows.Controls.Border> Element wird an den angedockt <xref:System.Windows.Controls.Dock.Left> , wobei seine Breite auf 200 Pixel festgelegt ist. Ein viertes <xref:System.Windows.Controls.Border> wird an den <xref:System.Windows.Controls.Dock.Bottom> des Bildschirms angedockt. Das letzte <xref:System.Windows.Controls.Border> Element füllt den verbleibenden Platz automatisch aus.  
  
 [!code-cpp[DockPanelOvwSample#1](~/samples/snippets/cpp/VS_Snippets_Wpf/DockPanelOvwSample/CPP/DockPanel_Ovw_Sample.cpp#1)]
 [!code-csharp[DockPanelOvwSample#1](~/samples/snippets/csharp/VS_Snippets_Wpf/DockPanelOvwSample/CSharp/DockPanel_Ovw_Sample.cs#1)]
 [!code-vb[DockPanelOvwSample#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DockPanelOvwSample/VisualBasic/dockpanel_vb.vb#1)]
 [!code-xaml[DockPanelOvwSample#1](~/samples/snippets/xaml/VS_Snippets_Wpf/DockPanelOvwSample/XAML/default.xaml#1)]  
  
> [!NOTE]
> Standardmäßig füllt das letzte untergeordnete Element eines- <xref:System.Windows.Controls.DockPanel> Elements den verbleibenden nicht zugeordneten Speicherplatz. Wenn Sie dieses Verhalten nicht wünschen, legen Sie `LastChildFill="False"` fest.  
  
 Die kompilierte Anwendung gibt eine neue Benutzeroberfläche aus, die folgendermaßen aussieht.  
  
 ![Ein typisches DockPanel-Szenario.](./media/panel-intro-dockpanel.PNG "panel_intro_dockpanel")  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.DockPanel>
- [Übersicht über Panel-Elemente](panels-overview.md)
