---
title: Erstellen eines Freihandeingabesteuerelements
ms.date: 03/30/2017
helpviewer_keywords:
- ink strokes [WPF], managing
- managing ink strokes [WPF]
- ink input control [WPF]
- input from mouse [WPF], accepting
- mouse input [WPF], accepting
- ink [WPF], rendering
- ink strokes [WPF], collecting
- rendering ink [WPF]
- collecting ink strokes [WPF]
- DynamicRenderer objects [WPF]
- StylusPlugIn objects [WPF]
ms.assetid: c31f3a67-cb3f-4ded-af9e-ed21f6575b26
ms.openlocfilehash: d9b18054154e6871925f423f539d44f12adca1f5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976410"
---
# <a name="creating-an-ink-input-control"></a>Erstellen eines Freihandeingabesteuerelements

Sie können ein benutzerdefiniertes Steuerelement erstellen, das frei Hand Eingaben dynamisch und statisch rendert. Das heißt, frei Hand Eingaben, wenn ein Benutzer einen Strich zeichnet, der bewirkt, dass die frei Hand Eingaben aus dem Tablettstift "fließen" und frei Hand Eingaben angezeigt werden, nachdem Sie dem Steuerelement hinzugefügt wurden, entweder über den Tablettstift, eingefügt aus der Zwischenablage oder aus einer Datei geladen. Zum dynamischen RenderInk muss das Steuerelement einen verwenden <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> . Zum statischen Rendern von frei Hand Eingaben müssen Sie die Stift-Ereignis Methoden ( <xref:System.Windows.UIElement.OnStylusDown%2A> , <xref:System.Windows.UIElement.OnStylusMove%2A> und <xref:System.Windows.UIElement.OnStylusUp%2A> ) überschreiben, um Daten zu erfassen <xref:System.Windows.Input.StylusPoint> , Striche zu erstellen und Sie einem hinzuzufügen <xref:System.Windows.Controls.InkPresenter> (wodurch die frei Hand Eingaben auf dem Steuerelement gerendert werden).  
  
 Dieses Thema enthält folgende Unterabschnitte:  
  
- [Gewusst wie: Sammeln von Tablettstiftpunkt-Daten und Erstellen von frei Hand Strichen](#CollectingStylusPointDataAndCreatingInkStrokes)  
  
- [Gewusst wie: Aktivieren des Steuer Elements für die Annahme von Eingaben von der Maus](#EnablingYourControlToAcceptInputTromTheMouse)  
  
- [Zusammenführung](#PuttingItTogether)  
  
- [Verwenden zusätzlicher Plug-ins und DynamicRenderer](#UsingAdditionalPluginsAndDynamicRenderers)  
  
- [Zusammenfassung](#AdvancedInkHandling_Conclusion)  
  
<a name="CollectingStylusPointDataAndCreatingInkStrokes"></a>

## <a name="how-to-collect-stylus-point-data-and-create-ink-strokes"></a>Gewusst wie: Sammeln von Tablettstiftpunkt-Daten und Erstellen von frei Hand Strichen  

 Gehen Sie folgendermaßen vor, um ein Steuerelement zu erstellen, das frei Hand Eingaben sammelt und verwaltet  
  
1. Leiten Sie eine Klasse von <xref:System.Windows.Controls.Control> oder einer der von abgeleiteten Klassen ab <xref:System.Windows.Controls.Control> , z <xref:System.Windows.Controls.Label> . b..  
  
     [!code-csharp[AdvancedInkTopicsSamples#20](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#20)]  
    [!code-csharp[AdvancedInkTopicsSamples#14](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControlSnippets.cs#14)]  
    [!code-csharp[AdvancedInkTopicsSamples#15](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControlSnippets.cs#15)]  
  
2. Fügen Sie <xref:System.Windows.Controls.InkPresenter> der-Klasse ein hinzu, und legen Sie die- <xref:System.Windows.Controls.ContentControl.Content%2A> Eigenschaft auf den neuen fest <xref:System.Windows.Controls.InkPresenter> .  
  
     [!code-csharp[AdvancedInkTopicsSamples#16](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControlSnippets.cs#16)]  
  
3. Fügen Sie den der an <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> den an <xref:System.Windows.Controls.InkPresenter> , indem <xref:System.Windows.Controls.InkPresenter.AttachVisuals%2A> Sie die-Methode aufrufen, und fügen Sie der-Auflistung hinzu <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> <xref:System.Windows.UIElement.StylusPlugIns%2A> . Dadurch kann das frei <xref:System.Windows.Controls.InkPresenter> Handzeichen anzeigen, wenn die Tablettstiftpunkt-Daten von Ihrem Steuerelement gesammelt werden.  
  
     [!code-csharp[AdvancedInkTopicsSamples#17](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControlSnippets.cs#17)]  
    [!code-csharp[AdvancedInkTopicsSamples#18](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControlSnippets.cs#18)]  
  
4. Überschreiben Sie die <xref:System.Windows.UIElement.OnStylusDown%2A> -Methode.  Erfassen Sie in dieser Methode den Tablettstift mit einem-Befehl <xref:System.Windows.Input.Stylus.Capture%2A> . Wenn Sie den Tablettstift aufzeichnen, wird das Steuerelement weiterhin <xref:System.Windows.UIElement.StylusMove> -und-Ereignisse empfangen, <xref:System.Windows.UIElement.StylusUp> auch wenn der Tablettstift die Grenzen des Steuer Elements verlässt. Dies ist nicht zwingend obligatorisch, aber fast immer für eine gute Benutzer Leistung. Erstellen Sie ein neues <xref:System.Windows.Input.StylusPointCollection> , um Daten zu erfassen <xref:System.Windows.Input.StylusPoint> . Fügen Sie schließlich den ursprünglichen Satz von <xref:System.Windows.Input.StylusPoint> Daten hinzu <xref:System.Windows.Input.StylusPointCollection> .  
  
     [!code-csharp[AdvancedInkTopicsSamples#7](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#7)]  
  
5. Überschreiben <xref:System.Windows.UIElement.OnStylusMove%2A> Sie die-Methode, und fügen Sie die <xref:System.Windows.Input.StylusPoint> Daten dem <xref:System.Windows.Input.StylusPointCollection> zuvor erstellten-Objekt hinzu.  
  
     [!code-csharp[AdvancedInkTopicsSamples#8](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#8)]  
  
6. Überschreiben Sie die <xref:System.Windows.UIElement.OnStylusUp%2A> -Methode, und erstellen Sie eine neue <xref:System.Windows.Ink.Stroke> mit den <xref:System.Windows.Input.StylusPointCollection> Daten. Fügen Sie den neuen <xref:System.Windows.Ink.Stroke> , den Sie erstellt haben, zur-Auflistung der <xref:System.Windows.Controls.InkPresenter.Strokes%2A> <xref:System.Windows.Controls.InkPresenter> und Release Stift Capture hinzu.  
  
     [!code-csharp[AdvancedInkTopicsSamples#10](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#10)]  
  
<a name="EnablingYourControlToAcceptInputTromTheMouse"></a>

## <a name="how-to-enable-your-control-to-accept-input-from-the-mouse"></a>Gewusst wie: Aktivieren des Steuer Elements für die Annahme von Eingaben von der Maus  

 Wenn Sie der Anwendung das vorangehende Steuerelement hinzufügen, es ausführen und die Maus als Eingabegerät verwenden, werden Sie feststellen, dass die Striche nicht persistent gespeichert werden. Gehen Sie folgendermaßen vor, um die Striche beizubehalten, wenn die Maus als Eingabegerät verwendet wird:  
  
1. Überschreiben <xref:System.Windows.UIElement.OnMouseLeftButtonDown%2A> Sie, und erstellen <xref:System.Windows.Input.StylusPointCollection> Sie eine neue, um die Position der Maus zu erstellen, wenn das Ereignis aufgetreten ist, und erstellen <xref:System.Windows.Input.StylusPoint> Sie mithilfe der Punktdaten einen, und fügen Sie dem hinzu <xref:System.Windows.Input.StylusPoint> <xref:System.Windows.Input.StylusPointCollection> .  
  
     [!code-csharp[AdvancedInkTopicsSamples#11](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#11)]  
  
2. Überschreiben Sie die <xref:System.Windows.UIElement.OnMouseMove%2A> -Methode. Rufen Sie die Position der Maus ab, zu der das Ereignis aufgetreten ist, und erstellen <xref:System.Windows.Input.StylusPoint> Sie mithilfe der Punktdaten einen.  Fügen Sie dem- <xref:System.Windows.Input.StylusPoint> <xref:System.Windows.Input.StylusPointCollection> Objekt hinzu, das Sie zuvor erstellt haben.  
  
     [!code-csharp[AdvancedInkTopicsSamples#12](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#12)]  
  
3. Überschreiben Sie die <xref:System.Windows.UIElement.OnMouseLeftButtonUp%2A> -Methode.  Erstellen Sie eine neue <xref:System.Windows.Ink.Stroke> mit den <xref:System.Windows.Input.StylusPointCollection> Daten, und fügen Sie den neuen, den Sie erstellt haben, der-Auflistung <xref:System.Windows.Ink.Stroke> von hinzu <xref:System.Windows.Controls.InkPresenter.Strokes%2A> <xref:System.Windows.Controls.InkPresenter> .  
  
     [!code-csharp[AdvancedInkTopicsSamples#13](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#13)]  
  
<a name="PuttingItTogether"></a>

## <a name="putting-it-together"></a>Zusammenführung  

 Das folgende Beispiel ist ein benutzerdefiniertes Steuerelement, das frei Hand Eingaben sammelt, wenn der Benutzer entweder die Maus oder den Stift verwendet.  
  
 [!code-csharp[AdvancedInkTopicsSamples#20](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#20)]  
[!code-csharp[AdvancedInkTopicsSamples#6](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/StylusControl.cs#6)]  
  
<a name="UsingAdditionalPluginsAndDynamicRenderers"></a>

## <a name="using-additional-plug-ins-and-dynamicrenderers"></a>Verwenden zusätzlicher Plug-ins und DynamicRenderer  

 Wie bei InkCanvas kann das benutzerdefinierte Steuerelement auch benutzerdefinierte <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> und zusätzliche <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> Objekte enthalten. Fügen Sie diese der-Auflistung hinzu <xref:System.Windows.UIElement.StylusPlugIns%2A> . Die Reihenfolge der <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> Objekte in der wirkt sich auf die Darstellung der frei Hand Eingabe aus, <xref:System.Windows.Input.StylusPlugIns.StylusPlugInCollection> Wenn Sie gerendert wird. Angenommen, Sie verfügen über einen <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> aufgerufenen `dynamicRenderer` und einen benutzerdefinierten <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> Namen `translatePlugin` , der die frei Hand Eingaben vom Tablettstift ablegt. Wenn `translatePlugin` der erste <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> in der ist <xref:System.Windows.Input.StylusPlugIns.StylusPlugInCollection> und der zweite Wert ist, wird die frei Hand Eingabe, die `dynamicRenderer` "Flows" ist, versetzt, wenn der Benutzer den Stift verschiebt. Wenn den Wert `dynamicRenderer` First hat und der zweite Wert ist, wird die frei Hand Eingabe `translatePlugin` nicht versetzt, bis der Benutzer den Stift hebt.  
  
<a name="AdvancedInkHandling_Conclusion"></a>

## <a name="conclusion"></a>Zusammenfassung  

 Sie können ein Steuerelement erstellen, das frei Hand Eingaben sammelt und rendert, indem Sie die Stift Ereignis Methoden überschreiben. Indem Sie Ihr eigenes Steuerelement erstellen, ihre eigenen <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> Klassen ableiten und diese in einfügen <xref:System.Windows.Input.StylusPlugIns.StylusPlugInCollection> , können Sie praktisch jedes Verhalten implementieren, das mit Digital Ink vorstellbar ist. Sie haben Zugriff auf die <xref:System.Windows.Input.StylusPoint> Daten, wenn Sie generiert werden, und haben die Möglichkeit, <xref:System.Windows.Input.Stylus> Eingaben anzupassen und auf dem Bildschirm entsprechend Ihrer Anwendung zu gestalten. Da Sie über einen solchen Zugriff auf die Daten auf niedriger Ebene verfügen <xref:System.Windows.Input.StylusPoint> , können Sie die frei Hand Erfassung implementieren und die Leistung für Ihre Anwendung mit einer optimalen Leistung erzielen.  
  
## <a name="see-also"></a>Siehe auch

- [Erweiterte Behandlung von Freihandeingaben](advanced-ink-handling.md)
- [Zugreifen auf und Bearbeiten von Stift Eingaben](/previous-versions/ms818317(v=msdn.10))
