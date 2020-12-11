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
# <a name="how-to-position-a-tooltip"></a><span data-ttu-id="cb116-102">Gewusst wie: Positionieren einer QuickInfo</span><span class="sxs-lookup"><span data-stu-id="cb116-102">How to: Position a ToolTip</span></span>
<span data-ttu-id="cb116-103">In diesem Beispiel wird gezeigt, wie die Position einer QuickInfo auf dem Bildschirm angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cb116-103">This example shows how to specify the position of a tooltip on the screen.</span></span>  
  
## <a name="example"></a><span data-ttu-id="cb116-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="cb116-104">Example</span></span>  
 <span data-ttu-id="cb116-105">Sie können eine QuickInfo mithilfe eines Satzes von fünf Eigenschaften positionieren, die in der <xref:System.Windows.Controls.ToolTip> -Klasse und der-Klasse definiert sind <xref:System.Windows.Controls.ToolTipService> .</span><span class="sxs-lookup"><span data-stu-id="cb116-105">You can position a tooltip by using a set of five properties that are defined in both the <xref:System.Windows.Controls.ToolTip> and <xref:System.Windows.Controls.ToolTipService> classes.</span></span> <span data-ttu-id="cb116-106">In der folgenden Tabelle werden diese beiden Sätze von fünf Eigenschaften angezeigt, und es werden Links zu Ihrer Referenz Dokumentation entsprechend der-Klasse bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cb116-106">The following table shows these two sets of five properties and provides links to their reference documentation according to class.</span></span>  
  
### <a name="corresponding-tooltip-properties-according-to-class"></a><span data-ttu-id="cb116-107">Entsprechende QuickInfo-Eigenschaften gemäß Klasse</span><span class="sxs-lookup"><span data-stu-id="cb116-107">Corresponding tooltip properties according to class</span></span>  
  
|<span data-ttu-id="cb116-108"><xref:System.Windows.Controls.ToolTip?displayProperty=nameWithType> Klasseneigenschaften</span><span class="sxs-lookup"><span data-stu-id="cb116-108"><xref:System.Windows.Controls.ToolTip?displayProperty=nameWithType> class properties</span></span>|<span data-ttu-id="cb116-109"><xref:System.Windows.Controls.ToolTipService?displayProperty=nameWithType> Klasseneigenschaften</span><span class="sxs-lookup"><span data-stu-id="cb116-109"><xref:System.Windows.Controls.ToolTipService?displayProperty=nameWithType> class properties</span></span>|  
|--------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|  
|<xref:System.Windows.Controls.ToolTip.Placement%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.Placement%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.PlacementTarget%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.PlacementTarget%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.PlacementRectangle%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.PlacementRectangle%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.HorizontalOffset%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.HorizontalOffset%2A?displayProperty=nameWithType>|  
|<xref:System.Windows.Controls.ToolTip.VerticalOffset%2A?displayProperty=nameWithType>|<xref:System.Windows.Controls.ToolTipService.VerticalOffset%2A?displayProperty=nameWithType>|  
  
 <span data-ttu-id="cb116-110">Wenn Sie den Inhalt einer QuickInfo mithilfe eines- <xref:System.Windows.Controls.ToolTip> Objekts definieren, können Sie die Eigenschaften einer der beiden Klassen verwenden. die Eigenschaften haben jedoch <xref:System.Windows.Controls.ToolTipService> Vorrang.</span><span class="sxs-lookup"><span data-stu-id="cb116-110">If you define the contents of a tooltip by using a <xref:System.Windows.Controls.ToolTip> object, you can use the properties of either class; however, the <xref:System.Windows.Controls.ToolTipService> properties take precedence.</span></span> <span data-ttu-id="cb116-111">Verwenden Sie die <xref:System.Windows.Controls.ToolTipService> Eigenschaften für Quick Infos, die nicht als-Objekte definiert sind <xref:System.Windows.Controls.ToolTip> .</span><span class="sxs-lookup"><span data-stu-id="cb116-111">Use the <xref:System.Windows.Controls.ToolTipService> properties for tooltips that are not defined as <xref:System.Windows.Controls.ToolTip> objects.</span></span>  
  
 <span data-ttu-id="cb116-112">In den folgenden Abbildungen wird gezeigt, wie Sie eine QuickInfo mithilfe dieser Eigenschaften positionieren können.</span><span class="sxs-lookup"><span data-stu-id="cb116-112">The following illustrations show how to position a tooltip by using these properties.</span></span> <span data-ttu-id="cb116-113">Obwohl die [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] Beispiele in diesen Abbildungen veranschaulichen, wie die Eigenschaften festgelegt werden, die von der-Klasse definiert werden <xref:System.Windows.Controls.ToolTip> , befolgen die entsprechenden Eigenschaften der- <xref:System.Windows.Controls.ToolTipService> Klasse dieselben Layoutregeln.</span><span class="sxs-lookup"><span data-stu-id="cb116-113">Although, the [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] examples in these illustrations show how to set the properties that are defined by the <xref:System.Windows.Controls.ToolTip> class, the corresponding properties of the <xref:System.Windows.Controls.ToolTipService> class follow the same layout rules.</span></span> <span data-ttu-id="cb116-114">Weitere Informationen zu den möglichen Werten für die Platzierungs Eigenschaft finden Sie unter [Popup-Platzierungs Verhalten](popup-placement-behavior.md).</span><span class="sxs-lookup"><span data-stu-id="cb116-114">For more information about the possible values for the Placement property, see [Popup Placement Behavior](popup-placement-behavior.md).</span></span>  

 <span data-ttu-id="cb116-115">Die folgende Abbildung zeigt die QuickInfo-Platzierung mithilfe der Platzierungs Eigenschaft:</span><span class="sxs-lookup"><span data-stu-id="cb116-115">The following image shows tooltip placement by using the Placement property:</span></span>  
  
 ![Diagramm, das die QuickInfo-Platzierung mithilfe der Platzierungs Eigenschaft anzeigt.](./media/how-to-position-a-tooltip/tooltip-placement-property.png)

 <span data-ttu-id="cb116-117">In der folgenden Abbildung wird die QuickInfo-Platzierung mithilfe der Eigenschaften Placement und placementrechteck angezeigt:</span><span class="sxs-lookup"><span data-stu-id="cb116-117">The following image shows tooltip placement by using the Placement and PlacementRectangle properties:</span></span>

 ![Das Diagramm zeigt die QuickInfo-Platzierung mithilfe einer placementrechteck-Eigenschaft.](./media/how-to-position-a-tooltip/tooltip-placement-rectangle-property.png)  

 <span data-ttu-id="cb116-119">Die folgende Abbildung zeigt die QuickInfo-Platzierung mithilfe der Eigenschaften Platzierung, placementrechteck und Offset:</span><span class="sxs-lookup"><span data-stu-id="cb116-119">The following image shows tooltip placement by using the Placement, PlacementRectangle, and Offset properties:</span></span>
  
 ![Das Diagramm zeigt die QuickInfo-Platzierung mithilfe der Offset-Eigenschaft.](./media/how-to-position-a-tooltip/tooltip-placement-offset-property.png)

 <span data-ttu-id="cb116-121">Im folgenden Beispiel wird gezeigt, wie die-Eigenschaften verwendet werden <xref:System.Windows.Controls.ToolTip> , um die Position einer QuickInfo anzugeben, deren Inhalt ein- <xref:System.Windows.Controls.ToolTip> Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="cb116-121">The following example shows how to use the <xref:System.Windows.Controls.ToolTip> properties to specify the position of a tooltip whose content is a <xref:System.Windows.Controls.ToolTip> object.</span></span>  
  
 [!code-xaml[ToolTipService#ToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#tooltip)]  
  
 [!code-csharp[ToolTipService#ToolTipCode](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml.cs#tooltipcode)]
 [!code-vb[ToolTipService#ToolTipCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ToolTipService/visualbasic/pane1.xaml.vb#tooltipcode)]  
  
 <span data-ttu-id="cb116-122">Im folgenden Beispiel wird gezeigt, wie die-Eigenschaften verwendet werden <xref:System.Windows.Controls.ToolTipService> , um die Position einer QuickInfo anzugeben, deren Inhalt kein- <xref:System.Windows.Controls.ToolTip> Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="cb116-122">The following example shows how to use the <xref:System.Windows.Controls.ToolTipService> properties to specify the position of a tooltip whose content is not a <xref:System.Windows.Controls.ToolTip> object.</span></span>  
  
 [!code-xaml[ToolTipService#NoToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml#notooltip)]  
  
 [!code-csharp[ToolTipService#NoToolTipCode](~/samples/snippets/csharp/VS_Snippets_Wpf/ToolTipService/CSharp/Pane1.xaml.cs#notooltipcode)]
 [!code-vb[ToolTipService#NoToolTipCode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ToolTipService/visualbasic/pane1.xaml.vb#notooltipcode)]  
  
## <a name="see-also"></a><span data-ttu-id="cb116-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb116-123">See also</span></span>

- <xref:System.Windows.Controls.ToolTip>
- <xref:System.Windows.Controls.ToolTipService>
- [<span data-ttu-id="cb116-124">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="cb116-124">How-to Topics</span></span>](tooltip-how-to-topics.md)
- [<span data-ttu-id="cb116-125">Übersicht über die QuickInfo</span><span class="sxs-lookup"><span data-stu-id="cb116-125">ToolTip Overview</span></span>](tooltip-overview.md)
