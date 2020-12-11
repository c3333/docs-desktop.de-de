---
title: Übersicht über Durchlässigkeitsmasken
ms.date: 03/30/2017
helpviewer_keywords:
- brushes [WPF], opacity masks
- masks [WPF], opacity
- opacity [WPF], masks
ms.assetid: 22367fab-5f59-4583-abfd-db2bf86eaef7
ms.openlocfilehash: fc3c0057416449bed56c69d1caa823a93e66037e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975297"
---
# <a name="opacity-masks-overview"></a>Übersicht über Durchlässigkeitsmasken
Mit Deckkraftmasken können Sie Teile eines Elements oder visuellen Objekts transparent bzw. teilweise transparent machen. Um eine Deckkraft Maske zu erstellen, wenden Sie ein <xref:System.Windows.Media.Brush> auf die- <xref:System.Windows.UIElement.OpacityMask%2A> Eigenschaft eines Elements oder an <xref:System.Windows.Media.Visual> .  Der Pinsel wird dem Element oder visuellen Objekt zugeordnet, und der Durchlässigkeitswert jedes Pinselpixels bestimmt die resultierende Durchlässigkeit der entsprechenden Pixel des Elements oder visuellen Objekts.  
  
<a name="prereqs"></a>
## <a name="prerequisites"></a>Voraussetzungen  
 In dieser Übersicht wird davon ausgegangen, dass Sie mit-Objekten vertraut sind <xref:System.Windows.Media.Brush> . Eine Einführung in die Verwendung von Pinseln finden Sie unter [Übersicht über das Zeichnen mit Volltonfarben und Farbverläufen](painting-with-solid-colors-and-gradients-overview.md). Weitere Informationen zu <xref:System.Windows.Media.ImageBrush> und <xref:System.Windows.Media.DrawingBrush> finden Sie unterzeichnen [mit Bildern, Zeichnungen und visuellen](painting-with-images-drawings-and-visuals.md)Elementen.  
  
<a name="opacitymasks"></a>
## <a name="creating-visual-effects-with-opacity-masks"></a>Erstellen von visuellen Effekten mit Deckkraftmasken  
 Eine Deckkraftmaske ordnet seine Inhalte dem Element oder visuellen Objekt zu. Der Alphakanal der einzelnen Pinselpixel bestimmt die resultierende Durchlässigkeit der entsprechenden Pixel des Elements oder visuellen Objekts. Die tatsächliche Farbe des Pinsels wird ignoriert. Wenn ein bestimmter Teil des Pinsels transparent ist, wird der entsprechende Teil des Elements oder visuellen Objekts transparent. Wenn ein bestimmter Teil des Pinsels nicht transparent ist, bleibt die Durchlässigkeit des entsprechenden Teils des Elements oder visuellen Objekts unverändert. Die von der Deckkraftmaske angegebene Deckkraft wird mit allen Deckkrafteinstellungen im Element oder visuellen Objekt kombiniert. Wenn ein Element z.B. zu 25 Prozent deckend ist und eine Deckkraftmaske angewendet wird, die von vollständig deckend in vollständig transparent übergeht, ist das Ergebnis ein Element, das von 25 Prozent deckend in vollständig transparent übergeht.  
  
> [!NOTE]
> Obwohl in den Beispielen in dieser Übersicht die Verwendung von Deck Kraft Masken für Bildelemente veranschaulicht wird, kann eine Deckkraft Maske auf jedes Element oder, einschließlich der Bereiche und Steuerelemente, angewendet werden <xref:System.Windows.Media.Visual> .  
  
 Deckkraftmasken dienen zum Erstellen interessanter visueller Effekte, z.B. zum Erstellen von Bildern oder Schaltflächen, die ausgeblendet werden, zum Hinzufügen von Texturen zu Elementen oder Kombinieren von Farbverläufen, um glasähnliche Oberflächen zu erzeugen. Die folgende Abbildung veranschaulicht die Verwendung einer Deckkraftmaske. Ein Hintergrund im Schachbrettmuster zeigt die transparenten Teile der Maske.  
  
 ![Objekt mit einer LinearGradientBrush-Deckkraftmaske](./media/wcpsdk-graphicsmm-opacitymask-imageexample.png "wcpsdk_graphicsmm_opacitymask_imageexample")  
Beispiel für eine Deckkraftmaske  
  
<a name="creatingopacitymasks"></a>
## <a name="creating-an-opacity-mask"></a>Erstellen einer Deckkraftmaske  
 Um eine Deckkraft Maske zu erstellen, erstellen Sie eine <xref:System.Windows.Media.Brush> und wenden Sie auf die- <xref:System.Windows.UIElement.OpacityMask%2A> Eigenschaft eines Elements oder visuellen Elements an. Sie können jede Art von <xref:System.Windows.Media.Brush> als Deck Kraft Maske verwenden.  
  
- <xref:System.Windows.Media.LinearGradientBrush>, <xref:System.Windows.Media.RadialGradientBrush> : Wird verwendet, um ein Element oder ein visuelles Element aus der Ansicht zu blenden.  
  
     Die folgende Abbildung zeigt eine, die <xref:System.Windows.Media.LinearGradientBrush> als Deck Kraft Maske verwendet wird.  
  
     ![Ein Objekt mit einer LinearGradiantBrush-Deckkraftmaske](./media/wcpsdk-graphicsmm-brushes-lineagradientopacitymasksingle.jpg "wcpsdk_graphicsmm_brushes_lineagradientopacitymasksingle")  
Beispiel für eine LinearGradientBrush-Deckkraftmaske  
  
- <xref:System.Windows.Media.ImageBrush>: Wird verwendet, um Textur-und weiche oder zerrissene Edge-Effekte zu erstellen.  
  
     Die folgende Abbildung zeigt eine, die <xref:System.Windows.Media.ImageBrush> als Deck Kraft Maske verwendet wird.  
  
     ![Objekt mit einer ImageBrush-Deckkraftmaske](./media/wcpsdk-graphicsmm-brushes-imageasopacitymasksingle.jpg "wcpsdk_graphicsmm_brushes_imageasopacitymasksingle")  
Beispiel für eine LinearGradientBrush-Deckkraftmaske  
  
- <xref:System.Windows.Media.DrawingBrush>: Wird verwendet, um komplexe Deck Kraft Masken aus Mustern von Formen, Bildern und Farbverläufen zu erstellen.  
  
     Die folgende Abbildung zeigt eine, die <xref:System.Windows.Media.DrawingBrush> als Deck Kraft Maske verwendet wird.  
  
     ![Objekt mit einer DrawingBrush-Deckkraftmaske](./media/wcpsdk-drawingbrushasopacitymask-single.jpg "wcpsdk_drawingbrushasopacitymask_single")  
Beispiel für eine DrawingBrush-Deckkraftmaske  
  
 Die Farb <xref:System.Windows.Media.LinearGradientBrush> Verlaufs Pinsel (und <xref:System.Windows.Media.RadialGradientBrush> ) eignen sich besonders gut für die Verwendung als Deck Kraft Maske. Da ein einen <xref:System.Windows.Media.SolidColorBrush> Bereich mit einer einheitlichen Farbe füllt, machen Sie schlechte Deck Kraft Masken. die Verwendung eines <xref:System.Windows.Media.SolidColorBrush> entspricht dem Festlegen der-Eigenschaft des Elements oder des visuellen Elements <xref:System.Windows.UIElement.OpacityMask%2A> .  
  
<a name="creatingopacitymaskswithgradients"></a>
## <a name="using-a-gradient-as-an-opacity-mask"></a>Verwenden eines Farbverlaufs als Deckkraftmaske  
 Um eine graduelle Füllung zu erstellen, geben Sie mindestens zwei Farbverlaufsstopp an. Jeder Farbverlaufsstopp beschreibt eine Farbe und eine Position (weitere Informationen zum Erstellen und Verwenden von Farbverläufen finden Sie unter [Übersicht über das Zeichnen mit Volltonfarben und Farbverläufen](painting-with-solid-colors-and-gradients-overview.md)). Es handelt sich um den gleichen Vorgang wie bei der Verwendung eines Farbverlaufs als Deckkraftmaske, außer dass der Farbverlauf der Deckkraftmaske anstelle von Farben Alphakanalwerte mischt. Daher spielt die tatsächliche Farbe der Farbverlaufsinhalte keine Rolle. Nur der Alphakanal oder die Deckkraft jeder Farbe ist relevant. Nachfolgend finden Sie ein Beispiel:  
  
 [!code-xaml[OpacityMasksSnippet#LinearGradientOpacityMaskonImage](~/samples/snippets/csharp/VS_Snippets_Wpf/OpacityMasksSnippet/CS/GradientBrushExample.xaml#lineargradientopacitymaskonimage)]  
  
<a name="specifyinggradientcolors"></a>
## <a name="specifying-gradient-stops-for-an-opacity-mask"></a>Angeben von Farbverlaufsstopps für eine Deckkraftmaske  
 Im vorherigen Beispiel wird die System definierte Farbe <xref:System.Windows.Media.Colors.Black%2A> als Start Farbe des Farbverlaufs verwendet. Da alle Farben in der- <xref:System.Windows.Media.Colors> Klasse, außer <xref:System.Windows.Media.Colors.Transparent%2A> , vollständig deckend sind, können Sie verwendet werden, um einfach eine Anfangs Farbe für eine Farbverlaufs Deck Kraft Maske zu definieren.  
  
 Um beim Definieren einer Deck Kraft Maske zusätzliche Kontrolle über Alpha Werte zu erhalten, können Sie den Alphakanal von Farben mithilfe der ARGB-hexadezimal Notation im Markup oder mithilfe der- <xref:System.Windows.Media.Color.FromScRgb%2A?displayProperty=nameWithType> Methode angeben.  
  
<a name="argbsyntax"></a>
### <a name="specifying-color-opacity-in-xaml"></a>Angeben der Deckkraft einer Farbe in „XAML“  
 In [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] verwenden Sie die hexadezimale Notation ARGB, um die Deckkraft einzelner Farben anzugeben. Bei der ARGB-hexadezimal Notation wird die folgende Syntax verwendet:  
  
 `#` **aa** *rrggbb*  
  
 *aa* in der vorherigen Zeile stellt einen zweistelligen Hexadezimalwert dar, der verwendet wird, um die Deckkraft der Farbe anzugeben. *rr*, *gg* und *bb* repräsentieren jeweils einen zweistelligen Hexadezimalwert, der die Anteile von Rot, Grün und Blau einer Farbe angibt. Jede Hexadezimalziffer kann einen Wert von 0-9 bzw. A-F haben. 0 ist der kleinste und F der größte Wert. Der Alphawert 00 gibt eine Farbe an, die vollständig transparent ist, während ein Alphawert FF eine vollständig deckende Farbe erstellt.  Im folgenden Beispiel wird die hexadezimale ARGB-Notation verwendet, um zwei Farben anzugeben. Die erste ist vollständig deckend, während die zweite vollkommen transparent ist.  
  
 [!code-xaml[OpacityMasksSnippet#AARRGGBBValueonOpacityMask](~/samples/snippets/csharp/VS_Snippets_Wpf/OpacityMasksSnippet/CS/GradientBrushExample.xaml#aarrggbbvalueonopacitymask)]  
  
<a name="usingimageasopacitymask"></a>
## <a name="using-an-image-as-an-opacity-mask"></a>Verwenden eines Bilds als Deckkraftmaske  
 Bilder können auch als Deckkraftmaske verwendet werden. Die folgende Abbildung zeigt ein Beispiel. Ein Hintergrund im Schachbrettmuster zeigt die transparenten Teile der Maske.  
  
 ![Ein Objekt mit einer ImageBrush-Deckkraftmaske](./media/wcpsdk-graphicsmm-imageasopacitymask.png "wcpsdk_graphicsmm_imageasopacitymask")  
Beispiel für eine Deckkraftmaske  
  
 Um ein Bild als Deck Kraft Maske zu verwenden, verwenden Sie eine- <xref:System.Windows.Media.ImageBrush> Datei, die das Bild enthält. Beim Erstellen eines Bilds, das als Deck Kraft Maske verwendet werden soll, speichern Sie das Bild in einem Format, das mehrere Transparenz Ebenen unterstützt, wie z. b. Portable Network Graphics (PNG). Das folgende Beispiel zeigt den Code, der zum Erstellen der vorherigen Abbildung erforderlich ist.  
  
 [!code-xaml[OpacityMasksSnippet#UIElementOpacityMask](~/samples/snippets/csharp/VS_Snippets_Wpf/OpacityMasksSnippet/CS/ImageBrushExample.xaml#uielementopacitymask)]  
  
<a name="tilingimageopacitymask"></a>
### <a name="using-a-tiled-image-as-an-opacity-mask"></a>Verwenden eines gekachelten Bilds als Deckkraftmaske  
 Im folgenden Beispiel wird das gleiche Bild mit einem anderen verwendet <xref:System.Windows.Media.ImageBrush> , aber die Tick-Funktionen des Pinsels werden verwendet, um Kacheln des Quadrats mit dem Bild 50 Pixel zu entwickeln.  
  
 [!code-xaml[OpacityMasksSnippet#TiledImageasOpacityMask](~/samples/snippets/csharp/VS_Snippets_Wpf/OpacityMasksSnippet/CS/ImageBrushExample.xaml#tiledimageasopacitymask)]  
  
<a name="drawingbrushasopacitymask"></a>
## <a name="creating-an-opacity-mask-from-a-drawing"></a>Erstellen einer Deckkraftmaske aus einer Zeichnung  
 Zeichnungen können als Deckkraftmaske verwendet verwenden. Die Formen innerhalb der Zeichnung können selbst mit Farbverläufen, Volltonfarben, Bildern oder sogar anderen Zeichnungen gefüllt werden. Die folgende Abbildung zeigt ein Beispiel einer Zeichnung, die als Deckkraftmaske verwendet wird. Ein Hintergrund im Schachbrettmuster zeigt die transparenten Teile der Maske.  
  
 ![Ein Objekt mit einer DrawingBrush-Deckkraftmaske](./media/wcpsdk-drawingbrushasopacitymask.png "wcpsdk_drawingbrushasopacitymask")  
Beispiel für eine DrawingBrush-Deckkraftmaske  
  
 Um eine Zeichnung als Deck Kraft Maske zu verwenden, verwenden <xref:System.Windows.Media.DrawingBrush> Sie eine, die die Zeichnung enthält. Das folgende Beispiel zeigt den Code, der zum Erstellen der vorherigen Abbildung erforderlich ist:  
  
 [!code-xaml[OpacityMasksSnippet#OpacityMaskfromDrawing](~/samples/snippets/csharp/VS_Snippets_Wpf/OpacityMasksSnippet/CS/DrawingBrushExample.xaml#opacitymaskfromdrawing)]  
  
<a name="tileddrawingbrush"></a>
### <a name="using-a-tiled-drawing-as-an-opacity-mask"></a>Verwenden einer gekachelten Zeichnung als Deckkraftmaske  
 Wie <xref:System.Windows.Media.ImageBrush> <xref:System.Windows.Media.DrawingBrush> bei kann auch die gezeichnet werden, um die Zeichnung zu Kacheln. Im folgenden Beispiel wird ein Zeichenpinsel verwendet, um eine gekachelte Deckkraftmaske zu erstellen.  
  
 [!code-xaml[OpacityMasksSnippet#TiledDrawingasOpacityMask](~/samples/snippets/csharp/VS_Snippets_Wpf/OpacityMasksSnippet/CS/DrawingBrushExample.xaml#tileddrawingasopacitymask)]  
  
## <a name="see-also"></a>Siehe auch

- [Zeichnen mit Bildern, Zeichnungen und visuellen Elementen](painting-with-images-drawings-and-visuals.md)
- [Übersicht über das Zeichnen mit Volltonfarben und Farbverläufen](painting-with-solid-colors-and-gradients-overview.md)
