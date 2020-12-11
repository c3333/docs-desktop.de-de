---
title: 'Gewusst wie: Positionieren einer QuickInfo'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ToolTip control [WPF], positioning
- positioning ToolTip controls [WPF]
ms.assetid: cddf3757-9e5f-4ce3-a6eb-44489cf3804a
ms.openlocfilehash: 851dc3c07e0abb4c7772f55f79900f1852b41232
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978159"
---
# <a name="how-to-position-a-tooltip"></a>Gewusst wie: Positionieren einer QuickInfo
In diesem Beispiel wird gezeigt, wie die Position einer QuickInfo auf dem Bildschirm angegeben wird.  
  
## <a name="example"></a>Beispiel  
 Sie können eine QuickInfo mithilfe eines Satzes von fünf Eigenschaften positionieren, die in der <xref:System.Windows.Controls.ToolTip> -Klasse und der-Klasse definiert sind <xref:System.Windows.Controls.ToolTipService> . In der folgenden Tabelle werden diese beiden Sätze von fünf Eigenschaften angezeigt, und es werden Links zu Ihrer Referenz Dokumentation entsprechend der-Klasse bereitstellt.  
  
### <a name="corresponding-tooltip-properties-according-to-class"></a>Entsprechende QuickInfo-Eigenschaften gemäß Klasse  
  
|<xref:System.Windows.Controls.ToolTip?displayProperty=nameWithType> Klasseneigenschaften|<xref:System.Windows.Controls.ToolTipService?displayProperty=nameWithType> Klasseneigenschaften|  
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
|<xref:System.Windows.Controls.ToolTip.Placement%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.Placement%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.PlacementTarget%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.PlacementTarget%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.PlacementRectangle%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.PlacementRectangle%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.HorizontalOffset%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.HorizontalOffset%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.VerticalOffset%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.VerticalOffset%2A?displayProperty=nameWithType>|  
  
 Wenn Sie den Inhalt einer QuickInfo mithilfe eines- <xref:System.Windows.Controls.ToolTip> Objekts definieren, können Sie die Eigenschaften einer der beiden Klassen verwenden. die Eigenschaften haben jedoch <xref:System.Windows.Controls.ToolTipService> Vorrang. Verwenden Sie die <xref:System.Windows.Controls.ToolTipService> Eigenschaften für Quick Infos, die nicht als-Objekte definiert sind <xref:System.Windows.Controls.ToolTip> .  
  
 In den folgenden Abbildungen wird gezeigt, wie Sie eine QuickInfo mithilfe dieser Eigenschaften positionieren können. Obwohl die [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beispiele in diesen Abbildungen veranschaulichen, wie die Eigenschaften festgelegt werden, die von der-Klasse definiert werden <xref:System.Windows.Controls.ToolTip> , befolgen die entsprechenden Eigenschaften der- <xref:System.Windows.Controls.ToolTipService> Klasse dieselben Layoutregeln. Weitere Informationen zu den möglichen Werten für die Platzierungs Eigenschaft finden Sie unter [Popup-Platzierungs Verhalten](popup-placement-behavior.md).  

 Die folgende Abbildung zeigt die QuickInfo-Platzierung mithilfe der Platzierungs Eigenschaft:  
  
 ![Diagramm, das die QuickInfo-Platzierung mithilfe der Platzierungs Eigenschaft anzeigt.](./media/how-to-position-a-tooltip/tooltip-placement-property.png)

 In der folgenden Abbildung wird die QuickInfo-Platzierung mithilfe der Eigenschaften Placement und placementrechteck angezeigt:

 ![Das Diagramm zeigt die QuickInfo-Platzierung mithilfe einer placementrechteck-Eigenschaft.](./media/how-to-position-a-tooltip/tooltip-placement-rectangle-property.png)  

 Die folgende Abbildung zeigt die QuickInfo-Platzierung mithilfe der Eigenschaften Platzierung, placementrechteck und Offset:
  
 ![Das Diagramm zeigt die QuickInfo-Platzierung mithilfe der Offset-Eigenschaft.](./media/how-to-position-a-tooltip/tooltip-placement-offset-property.png)

 Im folgenden Beispiel wird gezeigt, wie die-Eigenschaften verwendet werden <xref:System.Windows.Controls.ToolTip> , um die Position einer QuickInfo anzugeben, deren Inhalt ein- <xref:System.Windows.Controls.ToolTip> Objekt ist.  
  
 [!code-xaml[ToolTipService#ToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#tooltip)]  
  
 [!code-csharp[ToolTipService#ToolTipCode](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml.cs#tooltipcode)]
 [!code-vb[ToolTipService#ToolTipCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ToolTipService/visualbasic/pane1.xaml.vb#tooltipcode)]  
  
 Im folgenden Beispiel wird gezeigt, wie die-Eigenschaften verwendet werden <xref:System.Windows.Controls.ToolTipService> , um die Position einer QuickInfo anzugeben, deren Inhalt kein- <xref:System.Windows.Controls.ToolTip> Objekt ist.  
  
 [!code-xaml[ToolTipService#NoToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#notooltip)]  
  
 [!code-csharp[ToolTipService#NoToolTipCode](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml.cs#notooltipcode)]
 [!code-vb[ToolTipService#NoToolTipCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ToolTipService/visualbasic/pane1.xaml.vb#notooltipcode)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.ToolTip>
- <xref:System.Windows.Controls.ToolTipService>
- [Artikel zu Vorgehensweisen](tooltip-how-to-topics.md)
- [Übersicht über die QuickInfo](tooltip-overview.md)
