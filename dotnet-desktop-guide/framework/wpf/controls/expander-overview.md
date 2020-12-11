---
title: Übersicht über Expander-Steuerelemente
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], Expander
- Expander control [WPF], about Expander control
ms.assetid: 877bf425-0e54-49ec-8fd2-13a211377abb
ms.openlocfilehash: 3fcbcc67b65383133eef8d3e59cb1f8f0ff06f20
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976563"
---
# <a name="expander-overview"></a>Übersicht über Expander-Steuerelemente
Ein <xref:System.Windows.Controls.Expander> -Steuerelement bietet eine Möglichkeit zum Bereitstellen von Inhalt in einem erweiterbaren Bereich, der einem Fenster ähnelt und einen Header enthält.  

<a name="CreatinganExpanderinXAML"></a>
## <a name="creating-a-simple-expander"></a>Erstellen einer einfachen Expanders  
 Im folgenden Beispiel wird gezeigt, wie ein einfaches-Steuerelement erstellt wird <xref:System.Windows.Controls.Expander> . In diesem Beispiel wird ein erstellt <xref:System.Windows.Controls.Expander> , das wie die vorherige Abbildung aussieht.  
  
 [!code-xaml[ExpanderExample#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpanderExample/CSharp/Page1.xaml#2)]  
  
 <xref:System.Windows.Controls.ContentControl.Content%2A>Und <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> von <xref:System.Windows.Controls.Expander> können auch komplexe Inhalte enthalten, wie z. b <xref:System.Windows.Controls.RadioButton> .-und- <xref:System.Windows.Controls.Image> Objekte.  
  
<a name="SettingtheDirectionoftheExpandingWindow"></a>
## <a name="setting-the-direction-of-the-expanding-content-area"></a>Festlegen der Erweiterungsrichtung des Inhaltsbereichs  
 Mithilfe der-Eigenschaft können Sie den Inhalts Bereich eines- <xref:System.Windows.Controls.Expander> Steuer Elements auf eine von vier Richtungen ( <xref:System.Windows.Controls.ExpandDirection.Down> , <xref:System.Windows.Controls.ExpandDirection.Up> , <xref:System.Windows.Controls.ExpandDirection.Left> oder <xref:System.Windows.Controls.ExpandDirection.Right> ) festlegen <xref:System.Windows.Controls.ExpandDirection> . Wenn der Inhalts Bereich reduziert wird, werden nur die <xref:System.Windows.Controls.Expander> <xref:System.Windows.Controls.HeaderedContentControl.Header%2A> UMSCHALT Fläche und die zugehörige UMSCHALT Fläche angezeigt. Ein <xref:System.Windows.Controls.Button> Steuerelement, das einen Richtungspfeil anzeigt, wird als UMSCHALT Fläche verwendet, um den Inhalts Bereich zu erweitern oder zu reduzieren. Wenn Sie erweitert ist, versucht, den <xref:System.Windows.Controls.Expander> gesamten Inhalt in einem Fenster ähnlichen Bereich anzuzeigen.  
  
<a name="SettingSizeDimensionsonanExpanderinaPanel"></a>
## <a name="controlling-the-size-of-an-expander-in-a-panel"></a>Steuerung der Größe eines Expanders in einem Panel  
 Wenn sich ein- <xref:System.Windows.Controls.Expander> Steuerelement in einem Layoutsteuerelement befindet, das von erbt, z. b. <xref:System.Windows.Controls.Panel> <xref:System.Windows.Controls.StackPanel> , geben Sie keinen <xref:System.Windows.FrameworkElement.Height%2A> für den an, <xref:System.Windows.Controls.Expander> Wenn die- <xref:System.Windows.Controls.Expander.ExpandDirection%2A> Eigenschaft auf oder festgelegt ist <xref:System.Windows.Controls.ExpandDirection.Down> <xref:System.Windows.Controls.ExpandDirection.Up> Geben Sie auf ähnliche Weise keinen <xref:System.Windows.FrameworkElement.Width%2A> an, <xref:System.Windows.Controls.Expander> Wenn die- <xref:System.Windows.Controls.Expander.ExpandDirection%2A> Eigenschaft auf oder festgelegt ist <xref:System.Windows.Controls.ExpandDirection.Left> <xref:System.Windows.Controls.ExpandDirection.Right> .  
  
 Wenn Sie in einem-Steuerelement eine Größen Dimension <xref:System.Windows.Controls.Expander> in der Richtung festlegen, in der der erweiterte Inhalt angezeigt wird, übernimmt das die <xref:System.Windows.Controls.Expander> Kontrolle über den Bereich, der vom Inhalt verwendet wird, und zeigt einen Rahmen um ihn an. Der Rahmen wird auch angezeigt, wenn der Inhalt reduziert ist. Um die Größe des erweiterten Inhalts Bereichs festzulegen, legen Sie Größen Dimensionen für den Inhalt des fest <xref:System.Windows.Controls.Expander> , oder wenn Sie scrollfunktionen wünschen, auf dem, der <xref:System.Windows.Controls.ScrollViewer> den Inhalt einschließt.  
  
 Wenn ein- <xref:System.Windows.Controls.Expander> Steuerelement das letzte Element in einem-Element ist <xref:System.Windows.Controls.DockPanel> , werden [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] die <xref:System.Windows.Controls.Expander> Dimensionen von automatisch auf den restlichen Bereich von festgelegt <xref:System.Windows.Controls.DockPanel> . Um dieses Standardverhalten zu verhindern, legen Sie die- <xref:System.Windows.Controls.DockPanel.LastChildFill%2A> Eigenschaft des-Objekts auf fest <xref:System.Windows.Controls.DockPanel> `false` , oder stellen Sie sicher, dass das <xref:System.Windows.Controls.Expander> nicht das letzte Element in einem ist <xref:System.Windows.Controls.DockPanel> .  
  
<a name="CreatingScrollableContent"></a>
## <a name="creating-scrollable-content"></a>Erstellen vom bildlauffähigem Inhalt  
 Wenn der Inhalt für die Größe des Inhalts Bereichs zu groß ist, können Sie den Inhalt einer <xref:System.Windows.Controls.Expander> in einem einschließen, um <xref:System.Windows.Controls.ScrollViewer> scrollbaren Inhalt bereitzustellen. Das- <xref:System.Windows.Controls.Expander> Steuerelement stellt keine automatische Scrollfunktion bereit. Die folgende Abbildung zeigt ein- <xref:System.Windows.Controls.Expander> Steuerelement, das ein-Steuerelement enthält <xref:System.Windows.Controls.ScrollViewer> .  
  
 **Expander-Steuerelement in einem ScrollViewer**  
  
 ![Screenshot, der einen Expander mit ScrollBar anzeigt.](./media/expander-overview/expander-scrollbar-control.jpg)  
  
 Wenn Sie ein- <xref:System.Windows.Controls.Expander> Steuerelement in einem platzieren <xref:System.Windows.Controls.ScrollViewer> , legen Sie die Dimensions Eigenschaft fest, die <xref:System.Windows.Controls.ScrollViewer> der Richtung entspricht, in der der <xref:System.Windows.Controls.Expander> Inhalt für die Größe des <xref:System.Windows.Controls.Expander> Inhalts Bereichs geöffnet wird. Wenn Sie z. b. die-Eigenschaft für den auf festlegen <xref:System.Windows.Controls.Expander.ExpandDirection%2A> <xref:System.Windows.Controls.Expander> <xref:System.Windows.Controls.ExpandDirection.Down> (der Inhalts Bereich wird geöffnet), legen Sie die-Eigenschaft des-Steuer Elements auf <xref:System.Windows.FrameworkElement.Height%2A> <xref:System.Windows.Controls.ScrollViewer> die erforderliche Höhe für den Inhalts Bereich fest. Wenn Sie stattdessen die Height-Dimension für den eigentlichen Inhalt festlegen, <xref:System.Windows.Controls.ScrollViewer> erkennt diese Einstellung nicht und stellt daher keinen scrollfähigen Inhalt bereit.  
  
 Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.Expander> -Steuerelement erstellt wird, das überkomplexen Inhalt verfügt und ein-Steuerelement enthält <xref:System.Windows.Controls.ScrollViewer> . In diesem Beispiel wird ein-Wert erstellt <xref:System.Windows.Controls.Expander> , der der Abbildung am Anfang dieses Abschnitts ähnelt.  
  
 [!code-csharp[ExpanderRichContent#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpanderRichContent/CSharp/Window1.xaml.cs#1)]
 [!code-vb[ExpanderRichContent#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ExpanderRichContent/VisualBasic/Window1.xaml.vb#1)]
 [!code-xaml[ExpanderRichContent#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ExpanderRichContent/CSharp/Window1.xaml#1)]  
  
<a name="UsingtheAlignmentProperties"></a>
## <a name="using-the-alignment-properties"></a>Verwenden der Ausrichtungseigenschaften  
 Sie können den Inhalt ausrichten, indem Sie die-Eigenschaft und die-Eigenschaft des <xref:System.Windows.Controls.Control.HorizontalContentAlignment%2A> <xref:System.Windows.Controls.Control.VerticalContentAlignment%2A> <xref:System.Windows.Controls.Expander> Steuer Elements festlegen Wenn Sie diese Eigenschaften festlegen, wird die Ausrichtung sowohl auf den Header, als auch auf den erweiterten Inhalt angewendet.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Expander>
- <xref:System.Windows.Controls.ExpandDirection>
- [Artikel zu Vorgehensweisen](expander-how-to-topics.md)
