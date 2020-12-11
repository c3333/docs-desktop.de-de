---
title: Verhalten beim Platzieren von Popups
description: Erfahren Sie, wie Sie die Position eines Windows Presentation Foundation-Popup in Relation zu einem Steuerelement, der Maus oder dem Bildschirm mithilfe von Eigenschaften angeben.
ms.date: 03/30/2017
helpviewer_keywords:
- popups [WPF]
- Popup control [WPF], placing
- placing popups [WPF]
- positioning popups [WPF]
ms.assetid: fbf642e9-f670-4efd-a7af-a67468a1c8e1
ms.openlocfilehash: 8184805518bc56693ead4c7d1f0e9a1bff9bff8f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977706"
---
# <a name="popup-placement-behavior"></a>Verhalten beim Platzieren von Popups
Ein- <xref:System.Windows.Controls.Primitives.Popup> Steuerelement zeigt Inhalt in einem separaten Fenster an, das über eine Anwendung schwebt. <xref:System.Windows.Controls.Primitives.Popup>Mithilfe der <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> Eigenschaften,, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> , <xref:System.Windows.Controls.Primitives.Popup.HorizontalOffset%2A> und können Sie die Position eines relativ zu einem Steuerelement, der Maus oder dem Bildschirm angeben <xref:System.Windows.Controls.Primitives.Popup.VerticalOffset%2A> .  Diese Eigenschaften arbeiten zusammen, um Ihnen Flexibilität bei der Angabe der Position von zu bieten <xref:System.Windows.Controls.Primitives.Popup> .  
  
> [!NOTE]
> Die <xref:System.Windows.Controls.ToolTip> <xref:System.Windows.Controls.ContextMenu> Klassen und definieren außerdem diese fünf Eigenschaften und Verhalten sich ähnlich.  

<a name="Positioning"></a>
## <a name="positioning-the-popup"></a>Positionieren von Popups  
 Die Platzierung eines <xref:System.Windows.Controls.Primitives.Popup> kann relativ zu einem <xref:System.Windows.UIElement> oder zum gesamten Bildschirm sein.  Im folgenden Beispiel werden vier Steuer <xref:System.Windows.Controls.Primitives.Popup> Elemente erstellt, die relativ zu einem <xref:System.Windows.UIElement> – in diesem Fall ein Bild sind. Für alle-Steuer <xref:System.Windows.Controls.Primitives.Popup> Elemente ist die- <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> Eigenschaft auf festgelegt `image1` , aber jede <xref:System.Windows.Controls.Primitives.Popup> weist einen anderen Wert für die Placement-Eigenschaft auf.  
  
 [!code-xaml[PopupPositionSnippet#3](~/samples/snippets/csharp/VS_Snippets_Wpf/PopupPositionSnippet/CS/Window1.xaml#3)]  
  
 Die folgende Abbildung zeigt das Bild und die Steuer <xref:System.Windows.Controls.Primitives.Popup> Elemente.  
  
 ![Bild mit vier Popup-Steuerelementen](./media/popup-placement-behavior/popup-placement-intro.png "Bild mit vier Popups")
  
 In diesem einfachen Beispiel wird veranschaulicht, wie die-Eigenschaft und die-Eigenschaft festgelegt <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> werden. mit den <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> <xref:System.Windows.Controls.Primitives.Popup.HorizontalOffset%2A> Eigenschaften, und <xref:System.Windows.Controls.Primitives.Popup.VerticalOffset%2A> haben Sie jedoch noch mehr Kontrolle darüber, wo <xref:System.Windows.Controls.Primitives.Popup> positioniert ist.  
  
<a name="Definitions"></a>
## <a name="definitions-of-terms-the-anatomy-of-a-popup"></a>Begriffsdefinition: der Aufbau eines Popups  
 Die folgenden Begriffe sind hilfreich, um zu verstehen, wie <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> sich die <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> Eigenschaften,, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> , und in Beziehung zueinander <xref:System.Windows.Controls.Primitives.Popup.HorizontalOffset%2A> <xref:System.Windows.Controls.Primitives.Popup.VerticalOffset%2A> und <xref:System.Windows.Controls.Primitives.Popup> befinden.  
  
- Zielobjekt  
  
- Der Zielbereich  
  
- Der Zielursprung  
  
- Der Popupausrichtungspunkt  
  
 Diese Begriffe stellen eine bequeme Möglichkeit dar, auf verschiedene Aspekte von und auf das Steuerelement zu verweisen <xref:System.Windows.Controls.Primitives.Popup> , dem es zugeordnet ist.  
  
### <a name="target-object"></a>Zielobjekt  
 Das *Zielobjekt* ist das Element, dem der <xref:System.Windows.Controls.Primitives.Popup> zugeordnet ist. Wenn die- <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> Eigenschaft festgelegt ist, wird das Zielobjekt angegeben.  Wenn <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> nicht festgelegt ist und der <xref:System.Windows.Controls.Primitives.Popup> über ein übergeordnetes Element verfügt, ist das übergeordnete Objekt das Zielobjekt.  Wenn kein <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> Wert und kein übergeordnetes Element vorhanden ist, gibt es kein Zielobjekt, und das-Objekt ist <xref:System.Windows.Controls.Primitives.Popup> relativ zum Bildschirm positioniert.  
  
 Im folgenden Beispiel wird eine erstellt <xref:System.Windows.Controls.Primitives.Popup> , die das untergeordnete Element von ist <xref:System.Windows.Controls.Canvas> .  Im Beispiel wird die-Eigenschaft nicht auf festgelegt <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> <xref:System.Windows.Controls.Primitives.Popup> . Der Standardwert für <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> ist <xref:System.Windows.Controls.Primitives.PlacementMode.Bottom?displayProperty=nameWithType> , sodass <xref:System.Windows.Controls.Primitives.Popup> unter dem angezeigt wird <xref:System.Windows.Controls.Canvas> .  
  
 [!code-xaml[PopupPositionSnippet#1](~/samples/snippets/csharp/VS_Snippets_Wpf/PopupPositionSnippet/CS/Window1.xaml#1)]  
  
 Die folgende Abbildung zeigt, dass der <xref:System.Windows.Controls.Primitives.Popup> relativ zum positioniert ist <xref:System.Windows.Controls.Canvas> .  
  
 ![Popup-Steuerelement ohne PlacementTarget](./media/popup-placement-behavior/popup-placement-no-placement-target.png "Popup ohne PlacementTarget.")  

 Im folgenden Beispiel wird eine erstellt, <xref:System.Windows.Controls.Primitives.Popup> die das untergeordnete Element von ist <xref:System.Windows.Controls.Canvas> , aber dieses Mal <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> wird auf festgelegt `ellipse1` , sodass das Popup unter dem angezeigt wird <xref:System.Windows.Shapes.Ellipse> .  
  
 [!code-xaml[PopupPositionSnippet#2](~/samples/snippets/csharp/VS_Snippets_Wpf/PopupPositionSnippet/CS/Window1.xaml#2)]  
  
 Die folgende Abbildung zeigt, dass der <xref:System.Windows.Controls.Primitives.Popup> relativ zum positioniert ist <xref:System.Windows.Shapes.Ellipse> .  
  
 ![Relativ zu einer Ellipse platziertes Popup](./media/popup-placement-behavior/popup-placement-with-placement-target.png "Popup mit PlacementTarget")
  
> [!NOTE]
> Für <xref:System.Windows.Controls.ToolTip> ist der Standardwert von <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> <xref:System.Windows.Controls.Primitives.PlacementMode.Mouse> .  Für <xref:System.Windows.Controls.ContextMenu> ist der Standardwert von <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> <xref:System.Windows.Controls.Primitives.PlacementMode.MousePoint> . Diese Werte werden später in „Zusammenwirken der Eigenschaften“ erklärt.  
  
### <a name="target-area"></a>Der Zielbereich  
 Der *Zielbereich* ist der Bereich auf dem Bildschirm, <xref:System.Windows.Controls.Primitives.Popup> zu dem der relativ ist. In den vorherigen Beispielen wird der an <xref:System.Windows.Controls.Primitives.Popup> den Begrenzungen des Zielobjekts ausgerichtet, aber in einigen Fällen <xref:System.Windows.Controls.Primitives.Popup> wird der an anderen Begrenzungen ausgerichtet, auch wenn der <xref:System.Windows.Controls.Primitives.Popup> über ein Zielobjekt verfügt.  Wenn die- <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> Eigenschaft festgelegt wird, unterscheidet sich der Zielbereich von den Begrenzungen des Zielobjekts.  
  
 Im folgenden Beispiel werden zwei <xref:System.Windows.Controls.Canvas> -Objekte erstellt, die jeweils einen <xref:System.Windows.Shapes.Rectangle> und einen enthalten <xref:System.Windows.Controls.Primitives.Popup> .  In beiden Fällen ist das Zielobjekt für das <xref:System.Windows.Controls.Primitives.Popup> <xref:System.Windows.Controls.Canvas> . Der <xref:System.Windows.Controls.Primitives.Popup> in der ersten <xref:System.Windows.Controls.Canvas> verfügt über den <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> Satz, dessen <xref:System.Windows.Rect.X%2A> <xref:System.Windows.Rect.Y%2A> Eigenschaften,, <xref:System.Windows.Rect.Width%2A> und <xref:System.Windows.Rect.Height%2A> auf 50, 50, 50 und 100 festgelegt sind. Der <xref:System.Windows.Controls.Primitives.Popup> in der zweiten hat <xref:System.Windows.Controls.Canvas> nicht den <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> Satz.  Daher wird der erste <xref:System.Windows.Controls.Primitives.Popup> unter dem positioniert <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> und der zweite <xref:System.Windows.Controls.Primitives.Popup> unter dem positioniert <xref:System.Windows.Controls.Canvas> . Jede <xref:System.Windows.Controls.Canvas> enthält auch eine <xref:System.Windows.Shapes.Rectangle> , die die gleichen Begrenzungen wie die <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> für die erste aufweist <xref:System.Windows.Controls.Primitives.Popup> .  Beachten Sie, dass <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> von kein sichtbares Element in der Anwendung erstellt wird. im Beispiel wird ein erstellt <xref:System.Windows.Shapes.Rectangle> , das die darstellt <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> .  
  
 [!code-xaml[PopupPositionSnippet#4](~/samples/snippets/csharp/VS_Snippets_Wpf/PopupPositionSnippet/CS/Window1.xaml#4)]  
  
 Die folgende Abbildung zeigt das Ergebnis des vorherigen Beispiels.  
  
 ![Popup mit und ohne PlacementRectangle](./media/popup-placement-behavior/popup-placement-placement-rectangle.png "Popup mit und ohne placementrechteck.")  

### <a name="target-origin-and-popup-alignment-point"></a>Zielursprung und Popupausrichtungspunkt  
 Der *Zielursprung* und *Popupausrichtungspunkt* sind Bezugspunkte für die Positionierung im Zielbereich und im Popup. Sie können die-Eigenschaft und die-Eigenschaft verwenden <xref:System.Windows.Controls.Primitives.Popup.HorizontalOffset%2A> <xref:System.Windows.Controls.Primitives.Popup.VerticalOffset%2A> , um das Popup aus dem Zielbereich zu versetzen.  <xref:System.Windows.Controls.Primitives.Popup.HorizontalOffset%2A>Und <xref:System.Windows.Controls.Primitives.Popup.VerticalOffset%2A> sind relativ zum Ziel Ursprung und zum Popup Ausrichtungs Punkt. Der Wert der <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> -Eigenschaft bestimmt, wo sich der Ziel Ursprung und der Popup Ausrichtungs Punkt befinden.  
  
 Im folgenden Beispiel wird eine erstellt <xref:System.Windows.Controls.Primitives.Popup> und die <xref:System.Windows.Controls.Primitives.Popup.HorizontalOffset%2A> -Eigenschaft und die-Eigenschaft <xref:System.Windows.Controls.Primitives.Popup.VerticalOffset%2A> auf 20 festgelegt.  Die- <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> Eigenschaft wird auf <xref:System.Windows.Controls.Primitives.PlacementMode.Bottom> (die Standardeinstellung) festgelegt, sodass der Ziel Ursprung die linke untere Ecke des Zielbereichs und der Popup Ausrichtungs Punkt die linke obere Ecke des ist <xref:System.Windows.Controls.Primitives.Popup> .  
  
 [!code-xaml[PopupPositionSnippet#5](~/samples/snippets/csharp/VS_Snippets_Wpf/PopupPositionSnippet/CS/Window1.xaml#5)]  
  
 Die folgende Abbildung zeigt das Ergebnis des vorherigen Beispiels.  
  
 ![Popupplatzierung mit Zielursprung-Ausrichtungspunkt](./media/popup-placement-behavior/popup-placement-target-origin-alignment-point.png "Popup mit HorizontalOffset und VerticalOffset.")
  
<a name="How"></a>
## <a name="how-the-properties-work-together"></a>Zusammenwirken der Eigenschaften  
 Die Werte von <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> , <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> und <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> müssen in Erwägung gezogen werden, um den richtigen Zielbereich, den Ziel Ursprung und den Popup Ausrichtungs Punkt zu ermitteln.  Wenn der Wert von beispielsweise <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> ist <xref:System.Windows.Controls.Primitives.PlacementMode.Mouse> , gibt es kein Zielobjekt, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> wird ignoriert, und der Zielbereich ist die Begrenzungen des Mauszeigers. Wenn andererseits <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> ist <xref:System.Windows.Controls.Primitives.PlacementMode.Bottom> , bestimmt das übergeordnete Element <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> oder das Zielobjekt und <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> bestimmt den Zielbereich.  
  
 Die folgende Tabelle beschreibt das Zielobjekt, den Zielbereich, den Ziel Ursprung und den Popup Ausrichtungs Punkt und gibt an, ob <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> und <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> für jeden <xref:System.Windows.Controls.Primitives.PlacementMode> Enumerationswert verwendet werden.  
  
|PlacementMode|Zielobjekt|Der Zielbereich|Der Zielursprung|Der Popupausrichtungspunkt|  
|-------------------|-------------------|-----------------|-------------------|---------------------------|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Absolute>|Nicht zutreffend <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> wird ignoriert.|Der Bildschirm oder, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> Wenn er festgelegt ist.  Der <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> ist relativ zum Bildschirm.|Die linke obere Ecke des Zielbereichs|Die linke obere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.AbsolutePoint>|Nicht zutreffend <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> wird ignoriert.|Der Bildschirm oder, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> Wenn er festgelegt ist.  Der <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> ist relativ zum Bildschirm.|Die linke obere Ecke des Zielbereichs|Die linke obere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Bottom>|<xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> oder übergeordnetes Element.|Das Zielobjekt oder, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> Wenn es festgelegt ist.  Der <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> ist relativ zum Zielobjekt.|Die linke untere Ecke des Zielbereichs|Die linke obere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Center>|<xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> oder übergeordnetes Element.|Das Zielobjekt oder, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> Wenn es festgelegt ist.  Der <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> ist relativ zum Zielobjekt.|Die Mitte des Zielbereichs|Der Mittelpunkt der <xref:System.Windows.Controls.Primitives.Popup> .|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Custom>|<xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> oder übergeordnetes Element.|Das Zielobjekt oder, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> Wenn es festgelegt ist.  Der <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> ist relativ zum Zielobjekt.|Definiert durch <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> .|Definiert durch <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> .|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Left>|<xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> oder übergeordnetes Element.|Das Zielobjekt oder, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> Wenn es festgelegt ist.  Der <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> ist relativ zum Zielobjekt.|Die linke obere Ecke des Zielbereichs|Die obere rechte Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Mouse>|Nicht zutreffend <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> wird ignoriert.|Die Grenzen des Mauszeigers <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> wird ignoriert.|Die linke untere Ecke des Zielbereichs|Die linke obere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.MousePoint>|Nicht zutreffend <xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> wird ignoriert.|Die Grenzen des Mauszeigers <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> wird ignoriert.|Die linke obere Ecke des Zielbereichs|Die linke obere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Relative>|<xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> oder übergeordnetes Element.|Das Zielobjekt oder, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> Wenn es festgelegt ist.  Der <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> ist relativ zum Zielobjekt.|Die linke obere Ecke des Zielbereichs|Die linke obere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.RelativePoint>|<xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> oder übergeordnetes Element.|Das Zielobjekt oder, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> Wenn es festgelegt ist.  Der <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> ist relativ zum Zielobjekt.|Die linke obere Ecke des Zielbereichs|Die linke obere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Right>|<xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> oder übergeordnetes Element.|Das Zielobjekt oder, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> Wenn es festgelegt ist.  Der <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> ist relativ zum Zielobjekt.|Die rechte obere Ecke des Zielbereichs|Die linke obere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Top>|<xref:System.Windows.Controls.Primitives.Popup.PlacementTarget%2A> oder übergeordnetes Element.|Das Zielobjekt oder, <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> Wenn es festgelegt ist.  Der <xref:System.Windows.Controls.Primitives.Popup.PlacementRectangle%2A> ist relativ zum Zielobjekt.|Die linke obere Ecke des Zielbereichs|Die linke untere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|  
  
 Die folgenden Abbildungen zeigen die <xref:System.Windows.Controls.Primitives.Popup> , den Zielbereich, den Ziel Ursprung und den Popup Ausrichtungs Punkt für die einzelnen <xref:System.Windows.Controls.Primitives.PlacementMode> Werte. In jeder Abbildung ist der Zielbereich gelb, und <xref:System.Windows.Controls.Primitives.Popup> ist blau.  
  
 ![Popup mit Absolute- oder AbsolutePoint-Platzierung](./media/popup-placement-behavior/popup-placement-absolute.png "Die Platzierung ist absolut oder AbsolutePoint.")
  
 ![Popup mit Bottom-Platzierung](./media/popup-placement-behavior/popup-placement-bottom.png "Die Platzierung ist "Bottom".")
  
 ![Popup mit Center-Platzierung](./media/popup-placement-behavior/popup-placement-center.png "Die Platzierung ist "Center".")
  
 ![Popup mit Left-Platzierung](./media/popup-placement-behavior/popup-placement-left.png "Die Platzierung ist "Left".")
  
 ![Popup mit Mouse-Platzierung](./media/popup-placement-behavior/popup-placement-mouse.png "Die Platzierung ist "Mouse".")  
  
 ![Popup mit MousePoint-Platzierung](./media/popup-placement-behavior/popup-placement-mousepoint.png "Die Platzierung ist "moustipoint".")  
  
 ![Popup mit Relative- oder RelativePoint-Platzierung](./media/popup-placement-behavior/popup-placement-relative.png "Die Platzierung ist "relative" oder "RelativePoint".")
  
 ![Popup mit Right-Platzierung](./media/popup-placement-behavior/popup-placement-right.png "Die Platzierung ist "Right".")
  
 ![Popup mit Top-Platzierung](./media/popup-placement-behavior/popup-placement-top.png "Die Platzierung ist "Top".")
  
<a name="When"></a>
## <a name="when-the-popup-encounters-the-edge-of-the-screen"></a>Wenn das Popup auf einen Bildschirmrand trifft  
 Aus Sicherheitsgründen kann ein <xref:System.Windows.Controls.Primitives.Popup> nicht durch den Rand eines Bildschirms ausgeblendet werden. Eines der folgenden drei Dinge passiert, wenn <xref:System.Windows.Controls.Primitives.Popup> ein Bildschirmrand stößt:  
  
- Das Popup richtet sich am Bildschirmrand neu, der die verdecken würde <xref:System.Windows.Controls.Primitives.Popup> .  
  
- Das Popup verwendet einen anderen Popupausrichtungspunkt.  
  
- Das Popup verwendet einen anderen Zielursprungs und Popupausrichtungspunkt.  
  
 Diese Optionen werden weiter unten in diesem Abschnitt beschrieben.  
  
 Das Verhalten des <xref:System.Windows.Controls.Primitives.Popup> , wenn es auf einen Bildschirmrand stößt, hängt vom Wert der <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> -Eigenschaft und von dem Bildschirmrand ab, auf den das Popup trifft. In der folgenden Tabelle wird das Verhalten zusammengefasst, wenn der <xref:System.Windows.Controls.Primitives.Popup> auf einen Bildschirmrand für jeden <xref:System.Windows.Controls.Primitives.PlacementMode> Wert stößt.  
  
|PlacementMode|Oberer Rand|Unterer Rand|Linker Rand|Rechter Rand|  
|-------------------|--------------|-----------------|---------------|----------------|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Absolute>|Richtet sich am oberen Rand aus|Richtet sich am unteren Rand aus|Richtet sich am linken Rand aus|Richtet sich am rechten Rand aus|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.AbsolutePoint>|Richtet sich am oberen Rand aus|Der Popup Ausrichtungs Punkt ändert sich in die linke untere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|Richtet sich am linken Rand aus|Der Popup Ausrichtungs Punkt ändert sich in die obere rechte Ecke von <xref:System.Windows.Controls.Primitives.Popup> .|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Bottom>|Richtet sich am oberen Rand aus|Der Ziel Ursprung wird in die linke obere Ecke des Zielbereichs geändert, und der Popup Ausrichtungs Punkt ändert sich in die linke untere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|Richtet sich am linken Rand aus|Richtet sich am rechten Rand aus|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Center>|Richtet sich am oberen Rand aus|Richtet sich am unteren Rand aus|Richtet sich am linken Rand aus|Richtet sich am rechten Rand aus|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Left>|Richtet sich am oberen Rand aus|Richtet sich am unteren Rand aus|Der Ziel Ursprung ändert sich in die rechte obere Ecke des Zielbereichs, und der Popup Ausrichtungs Punkt ändert sich in die linke obere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|Richtet sich am rechten Rand aus|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Mouse>|Richtet sich am oberen Rand aus|Der Ziel Ursprung ändert sich in die linke obere Ecke des Zielbereichs (die Begrenzungen des Mauszeigers), und der Popup Ausrichtungs Punkt ändert sich in die linke untere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|Richtet sich am linken Rand aus|Richtet sich am rechten Rand aus|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.MousePoint>|Richtet sich am oberen Rand aus|Der Popup Ausrichtungs Punkt ändert sich in die linke untere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|Richtet sich am linken Rand aus|Der Ausrichtungspunkt wird auf die obere rechte Ecke des Popups geändert.|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Relative>|Richtet sich am oberen Rand aus|Richtet sich am unteren Rand aus|Richtet sich am linken Rand aus|Richtet sich am rechten Rand aus|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.RelativePoint>|Richtet sich am oberen Rand aus|Der Popup Ausrichtungs Punkt ändert sich in die linke untere Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|Richtet sich am linken Rand aus|Der Ausrichtungspunkt wird auf die obere rechte Ecke des Popups geändert.|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Right>|Richtet sich am oberen Rand aus|Richtet sich am unteren Rand aus|Richtet sich am linken Rand aus|Der Ziel Ursprung wird in die linke obere Ecke des Zielbereichs geändert, und der Popup Ausrichtungs Punkt ändert sich in die obere rechte Ecke des <xref:System.Windows.Controls.Primitives.Popup> .|  
|<xref:System.Windows.Controls.Primitives.PlacementMode.Top>|Der Ziel Ursprung wird in die linke untere Ecke des Zielbereichs geändert, und der Popup Ausrichtungs Punkt ändert sich in die linke obere Ecke des <xref:System.Windows.Controls.Primitives.Popup> . Tatsächlich ist dies identisch mit dem, wenn gleich <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> ist <xref:System.Windows.Controls.Primitives.PlacementMode.Bottom> .|Richtet sich am unteren Rand aus|Richtet sich am linken Rand aus|Richtet sich am rechten Rand aus|  
  
### <a name="aligning-to-the-screen-edge"></a>Ausrichten am Bildschirmrand  
 Eine <xref:System.Windows.Controls.Primitives.Popup> kann am Bildschirmrand ausgerichtet werden, indem Sie sich selbst neu positioniert, sodass die gesamte <xref:System.Windows.Controls.Primitives.Popup> auf dem Bildschirm sichtbar ist.  In diesem Fall kann sich der Abstand zwischen dem Ziel Ursprung und dem Popup Ausrichtungs Punkt von den Werten von und unterscheiden <xref:System.Windows.Controls.Primitives.Popup.HorizontalOffset%2A> <xref:System.Windows.Controls.Primitives.Popup.VerticalOffset%2A> . Wenn <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> <xref:System.Windows.Controls.Primitives.PlacementMode.Absolute> , <xref:System.Windows.Controls.Primitives.PlacementMode.Center> oder ist <xref:System.Windows.Controls.Primitives.PlacementMode.Relative> , <xref:System.Windows.Controls.Primitives.Popup> richtet sich der an jedem Bildschirmrand.  Nehmen Sie beispielsweise an, dass ein <xref:System.Windows.Controls.Primitives.Popup> <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> auf festgelegt ist <xref:System.Windows.Controls.Primitives.PlacementMode.Relative> und <xref:System.Windows.Controls.Primitives.Popup.VerticalOffset%2A> auf 100 festgelegt ist.  Wenn der untere Rand des Bildschirms den gesamten oder einen Teil von verbirgt <xref:System.Windows.Controls.Primitives.Popup> , <xref:System.Windows.Controls.Primitives.Popup> wird die Position am unteren Bildschirmrand neu angeordnet, und der vertikale Abstand zwischen dem Ziel Ursprung und dem Popup Ausrichtungs Punkt ist kleiner als 100. Dies wird in der folgenden Abbildung veranschaulicht.  
  
 ![Am Bildschirmrand ausgerichtetes Popup](./media/popup-placement-behavior/popup-placement-relative-screen-edge.png "Popup richtet sich am Bildschirmrand aus.")
  
### <a name="changing-the-popup-alignment-point"></a>Ändern des Popupausrichtungspunkts  
 Wenn <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> <xref:System.Windows.Controls.Primitives.PlacementMode.AbsolutePoint> , <xref:System.Windows.Controls.Primitives.PlacementMode.RelativePoint> oder ist <xref:System.Windows.Controls.Primitives.PlacementMode.MousePoint> , ändert sich der Popup Ausrichtungs Punkt, wenn das Popup auf den unteren oder rechten Bildschirmrand trifft.  
  
 In der folgenden Abbildung wird veranschaulicht, dass der <xref:System.Windows.Controls.Primitives.Popup> Popup Ausrichtungs Punkt die untere linke Ecke von ist, wenn der untere Bildschirmrand den gesamten oder einen Teil von verbirgt <xref:System.Windows.Controls.Primitives.Popup> .  
  
 ![Neuer Ausrichtungspunkt durch unteren Bildschirmrand](./media/popup-placement-behavior/popup-placement-relative-point-screen-edge.png "Popup stößt auf den unteren Rand des Bildschirms und ändert den Popup Ausrichtungs Punkt.")  

 In der folgenden Abbildung wird veranschaulicht, dass der <xref:System.Windows.Controls.Primitives.Popup> Popup Ausrichtungs Punkt die obere rechte Ecke von ist, wenn der durch den rechten Bildschirmrand ausgeblendet wird <xref:System.Windows.Controls.Primitives.Popup> .  
  
 ![Neuer Popupausrichtungspunkt durch Bildschirmrand](./media/popup-placement-behavior/popup-placement-relative-point-right-screen-edge.png "Popup trifft den rechten Rand des Bildschirms und ändert den Popup Ausrichtungs Punkt.")
  
 Wenn die <xref:System.Windows.Controls.Primitives.Popup> unteren und rechten Bildschirmränder trifft, ist der Popup Ausrichtungs Punkt die untere rechte Ecke des <xref:System.Windows.Controls.Primitives.Popup> .  
  
### <a name="changing-the-target-origin-and-popup-alignment-point"></a>Ändern des Zielursprungs und des Popupausrichtungspunkts  
 Wenn <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> <xref:System.Windows.Controls.Primitives.PlacementMode.Bottom> ,, <xref:System.Windows.Controls.Primitives.PlacementMode.Left> , oder ist, <xref:System.Windows.Controls.Primitives.PlacementMode.Mouse> <xref:System.Windows.Controls.Primitives.PlacementMode.Right> <xref:System.Windows.Controls.Primitives.PlacementMode.Top> ändern sich der Ziel Ursprung und der Popup Ausrichtungs Punkt, wenn ein bestimmter Bildschirmrand gefunden wird.  Der Bildschirmrand, der bewirkt, dass die Position geändert wird, hängt vom <xref:System.Windows.Controls.Primitives.PlacementMode> Wert ab.  
  
 In der folgenden Abbildung wird veranschaulicht, dass wenn <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> <xref:System.Windows.Controls.Primitives.PlacementMode.Bottom> und den <xref:System.Windows.Controls.Primitives.Popup> unteren Bildschirmrand trifft, der Ziel Ursprung die linke obere Ecke des Zielbereichs und der Popup Ausrichtungs Punkt die untere linke Ecke von ist <xref:System.Windows.Controls.Primitives.Popup> .  
  
 ![Neuer Ausrichtungspunkt durch unteren Bildschirmrand](./media/popup-placement-behavior/popup-placement-bottom-screen-edge.png "Die Platzierung erfolgt unten, und das Popup stößt auf den unteren Rand des Bildschirms.")
  
 In der folgenden Abbildung wird veranschaulicht, dass wenn <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> ist <xref:System.Windows.Controls.Primitives.PlacementMode.Left> und der <xref:System.Windows.Controls.Primitives.Popup> linke Bildschirmrand stößt, der Ziel Ursprung die obere rechte Ecke des Zielbereichs und der Popup Ausrichtungs Punkt die linke obere Ecke von ist <xref:System.Windows.Controls.Primitives.Popup> .  
  
 ![Neuer Ausrichtungspunkt durch linken Bildschirmrand](./media/popup-placement-behavior/popup-placement-left-screen-edge.png "Die Platzierung ist "Left", und das Popup stößt auf den linken Rand des Bildschirms.")  
  
 In der folgenden Abbildung wird veranschaulicht, dass wenn <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> <xref:System.Windows.Controls.Primitives.PlacementMode.Right> und den <xref:System.Windows.Controls.Primitives.Popup> rechten Bildschirmrand trifft, der Ziel Ursprung die linke obere Ecke des Zielbereichs und der Popup Ausrichtungs Punkt die obere rechte Ecke von ist <xref:System.Windows.Controls.Primitives.Popup> .  
  
 ![Neuer Ausrichtungspunkt durch rechten Bildschirmrand](./media/popup-placement-behavior/popup-placement-right-screen-edge.png "Die Platzierung ist "Right", und das Popup stößt auf den rechten Bildschirmrand.")  

 In der folgenden Abbildung wird veranschaulicht, dass wenn <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> ist <xref:System.Windows.Controls.Primitives.PlacementMode.Top> und der <xref:System.Windows.Controls.Primitives.Popup> obere Bildschirmrand stößt, der Ziel Ursprung die linke untere Ecke des Zielbereichs und der Popup Ausrichtungs Punkt die linke obere Ecke von ist <xref:System.Windows.Controls.Primitives.Popup> .  
  
 ![Neuer Ausrichtungspunkt durch obere Bildschirmrand](./media/popup-placement-behavior/popup-placement-top-screen-edge.png "Die Platzierung ist "Top", und das Popup stößt auf den oberen Rand des Bildschirms.")  
  
 In der folgenden Abbildung wird veranschaulicht, dass wenn <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> <xref:System.Windows.Controls.Primitives.PlacementMode.Mouse> und den <xref:System.Windows.Controls.Primitives.Popup> unteren Bildschirmrand trifft, der Ziel Ursprung die linke obere Ecke des Zielbereichs (die Begrenzungen des Mauszeigers) und der Popup Ausrichtungs Punkt die untere linke Ecke von <xref:System.Windows.Controls.Primitives.Popup> .  
  
 ![Neuer Ausrichtungspunkt durch Maus in der Nähe des Bildschirmrands](./media/popup-placement-behavior/popup-placement-mouse-screen-edge.png "Die Platzierung ist "Mouse", und das Popup stößt auf den unteren Rand des Bildschirms.")
  
### <a name="customizing-popup-placement"></a>Anpassen der Popupplatzierung  
 Sie können den Ziel Ursprung und den Popup Ausrichtungs Punkt anpassen, indem Sie die- <xref:System.Windows.Controls.Primitives.Popup.Placement%2A> Eigenschaft auf festlegen <xref:System.Windows.Controls.Primitives.PlacementMode.Custom> . Definieren Sie dann einen Delegaten <xref:System.Windows.Controls.Primitives.CustomPopupPlacementCallback> , der einen Satz möglicher Platzierungs Punkte und primäre Achsen (in der bevorzugten Reihenfolge) für den zurückgibt <xref:System.Windows.Controls.Primitives.Popup> . Der Punkt, der den größten Teil des anzeigt, <xref:System.Windows.Controls.Primitives.Popup> wird ausgewählt.  Die Position des <xref:System.Windows.Controls.Primitives.Popup> wird automatisch angepasst, wenn der am <xref:System.Windows.Controls.Primitives.Popup> Bildschirmrand ausgeblendet ist. Ein Beispiel finden Sie unter [Angeben einer benutzerdefinierten Popupposition](how-to-specify-a-custom-popup-position.md).  
  
## <a name="see-also"></a>Siehe auch

- [Beispiel für das Platzieren eines Popups](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/VS_Snippets_Wpf/PopupPositionSnippet/CS)
