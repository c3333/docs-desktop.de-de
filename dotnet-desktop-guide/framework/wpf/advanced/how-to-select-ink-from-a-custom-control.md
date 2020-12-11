---
title: 'Gewusst wie: Auswählen von Freihandeingaben aus einem benutzerdefinierten Steuerelement'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [WPF], ink selection
- ink [WPF], selecting from custom control
- custom controls [WPF], ink selection
ms.assetid: 5f3a45c6-6d40-4017-9b47-933f134ceba3
ms.openlocfilehash: 5c9b2f3d64e4cbb309772d6a1d9fa88f589df84c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977789"
---
# <a name="how-to-select-ink-from-a-custom-control"></a>Gewusst wie: Auswählen von Freihandeingaben aus einem benutzerdefinierten Steuerelement
Durch Hinzufügen eines <xref:System.Windows.Ink.IncrementalLassoHitTester> zum benutzerdefinierten Steuerelement können Sie das Steuerelement aktivieren, sodass ein Benutzer frei Hand Eingaben mit einem Lassopfad-Tool auswählen kann, ähnlich wie beim auswählen <xref:System.Windows.Controls.InkCanvas> von frei Hand Eingaben mit Lassopfad.  
  
 In diesem Beispiel wird davon ausgegangen, dass Sie mit dem Erstellen eines benutzerdefinierten Steuer Elements vertraut sind  Informationen zum Erstellen eines benutzerdefinierten Steuer Elements, das frei Hand Eingaben annimmt, finden Sie unter [Creating an Ink Input Control](creating-an-ink-input-control.md)  
  
## <a name="example"></a>Beispiel  
 Wenn der Benutzer eine Lassopfad zeichnet, <xref:System.Windows.Ink.IncrementalLassoHitTester> sagt der vorher, welche Striche innerhalb der Grenzen des Lassopfad-Pfads liegen, nachdem der Benutzer das Lassopfad abgeschlossen hat.  Striche, die festgelegt werden, dass Sie sich innerhalb der Lassopfad-Pfad Grenzen befinden, können als ausgewählt betrachtet werden.  Ausgewählte Striche können auch deaktiviert werden.  Wenn der Benutzer z. b. die Richtung beim Zeichnen des Lasso umkehrt, <xref:System.Windows.Ink.IncrementalLassoHitTester> kann die Auswahl einiger Striche aufgehoben werden.  
  
 Löst <xref:System.Windows.Ink.IncrementalLassoHitTester> das- <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged> Ereignis aus, mit dem das benutzerdefinierte Steuerelement reagieren kann, während der Benutzer die Lasso zeichnet.  Beispielsweise können Sie die Darstellung von Strichen ändern, wenn der Benutzer Sie auswählt und deaktiviert.  
  
## <a name="managing-the-ink-mode"></a>Verwalten des frei Hand Modus  
 Es ist hilfreich für den Benutzer, wenn das Lassopfad anders aussieht als die frei Hand Eingabe auf dem Steuerelement. Um dies zu erreichen, muss das benutzerdefinierte Steuerelement verfolgen, ob der Benutzer frei Hand Eingaben schreibt oder diese auswählt. Die einfachste Möglichkeit hierzu besteht darin, eine Enumeration mit zwei Werten zu deklarieren: eine, die angibt, dass der Benutzer frei Hand Eingaben schreibt, und eine Enumeration, die angibt, dass der Benutzer frei Hand Eingaben auswählt.  
  
 [!code-csharp[HowToSelectInk#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#2)]
 [!code-vb[HowToSelectInk#2](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#2)]  
  
 Fügen Sie als nächstes zwei <xref:System.Windows.Ink.DrawingAttributes> zur-Klasse hinzu: eine, die verwendet werden soll, wenn der Benutzer frei Hand Eingaben schreibt.  Initialisieren Sie im Konstruktor, <xref:System.Windows.Ink.DrawingAttributes> und fügen Sie beide <xref:System.Windows.Ink.DrawingAttributes.AttributeChanged> Ereignisse an denselben Ereignishandler an. Legen Sie dann die- <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.DrawingAttributes%2A> Eigenschaft von <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> auf die frei Hand Eingabe fest <xref:System.Windows.Ink.DrawingAttributes> .  
  
 [!code-csharp[HowToSelectInk#3](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#3)]
 [!code-vb[HowToSelectInk#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#3)]  
[!code-csharp[HowToSelectInk#4](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#4)]
[!code-vb[HowToSelectInk#4](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#4)]  
  
 Fügen Sie eine Eigenschaft hinzu, die den Auswahlmodus verfügbar macht. Wenn der Benutzer den Auswahlmodus ändert, legen <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.DrawingAttributes%2A> Sie die-Eigenschaft von <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> auf das entsprechende <xref:System.Windows.Ink.DrawingAttributes> -Objekt fest, und fügen Sie dann die-Eigenschaft erneut <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> an <xref:System.Windows.Controls.InkPresenter> .  
  
 [!code-csharp[HowToSelectInk#5](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#5)]
 [!code-vb[HowToSelectInk#5](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#5)]  
  
 Machen Sie die <xref:System.Windows.Ink.DrawingAttributes> As-Eigenschaften verfügbar, damit Anwendungen das Aussehen der Hand Striche und Auswahl Striche bestimmen können.  
  
 [!code-csharp[HowToSelectInk#6](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#6)]
 [!code-vb[HowToSelectInk#6](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#6)]  
  
 Wenn sich eine Eigenschaft eines- <xref:System.Windows.Ink.DrawingAttributes> Objekts ändert, <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> muss erneut an das angefügt werden <xref:System.Windows.Controls.InkPresenter> .  Fügen Sie im Ereignishandler für das- <xref:System.Windows.Ink.DrawingAttributes.AttributeChanged> Ereignis den erneut <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer.RootVisual%2A> an <xref:System.Windows.Controls.InkPresenter> .  
  
 [!code-csharp[HowToSelectInk#7](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#7)]
 [!code-vb[HowToSelectInk#7](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#7)]  
  
## <a name="using-the-incrementallassohittester"></a>Verwenden von IncrementalLassoHitTester  
 Erstellt und Initialisiert eine <xref:System.Windows.Ink.StrokeCollection> , die die ausgewählten Striche enthält.  
  
 [!code-csharp[HowToSelectInk#8](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#8)]
 [!code-vb[HowToSelectInk#8](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#8)]  
  
 Wenn der Benutzer mit dem Zeichnen eines Strichs beginnt (entweder frei Hand Eingaben oder Lasso), heben Sie die Auswahl ausgewählter Striche auf. Wenn der Benutzer dann einen Lasso-Wert erstellt, erstellen <xref:System.Windows.Ink.IncrementalLassoHitTester> <xref:System.Windows.Ink.StrokeCollection.GetIncrementalLassoHitTester%2A> Sie einen, indem Sie aufrufen, abonnieren Sie das <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged> -Ereignis, und rufen Sie auf <xref:System.Windows.Ink.IncrementalHitTester.AddPoints%2A> . Dieser Code kann eine separate Methode sein und von der-Methode und der-Methode aufgerufen werden <xref:System.Windows.UIElement.OnStylusDown%2A> <xref:System.Windows.UIElement.OnMouseDown%2A> .  
  
 [!code-csharp[HowToSelectInk#9](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#9)]
 [!code-vb[HowToSelectInk#9](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#9)]  
  
 Fügen Sie die Tablettstiftpunkte hinzu, <xref:System.Windows.Ink.IncrementalLassoHitTester> während der Benutzer den Lasso zeichnet.  Nennen Sie die folgende Methode aus <xref:System.Windows.UIElement.OnStylusMove%2A> den <xref:System.Windows.UIElement.OnStylusUp%2A> Methoden,, <xref:System.Windows.UIElement.OnMouseMove%2A> und <xref:System.Windows.UIElement.OnMouseLeftButtonUp%2A> .  
  
 [!code-csharp[HowToSelectInk#10](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#10)]
 [!code-vb[HowToSelectInk#10](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#10)]  
  
 Behandeln Sie das- <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged?displayProperty=nameWithType> Ereignis, um zu reagieren, wenn der Benutzer Striche auswählt und deaktiviert.  Die <xref:System.Windows.Ink.LassoSelectionChangedEventArgs> -Klasse verfügt über die <xref:System.Windows.Ink.LassoSelectionChangedEventArgs.SelectedStrokes%2A> -Eigenschaft und die-Eigenschaft, mit <xref:System.Windows.Ink.LassoSelectionChangedEventArgs.DeselectedStrokes%2A> der die jeweils ausgewählten bzw. nicht ausgewählten Striche angezeigt werden.  
  
 [!code-csharp[HowToSelectInk#11](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#11)]
 [!code-vb[HowToSelectInk#11](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#11)]  
  
 Wenn der Benutzer das Zeichnen des Lasso abschließt, kündigen Sie das Ereignis an, <xref:System.Windows.Ink.IncrementalLassoHitTester.SelectionChanged> und rufen Sie auf <xref:System.Windows.Ink.IncrementalHitTester.EndHitTesting%2A> .  
  
 [!code-csharp[HowToSelectInk#12](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#12)]
 [!code-vb[HowToSelectInk#12](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#12)]  
  
## <a name="putting-it-all-together"></a>Alles, was alles vereint.  
 Das folgende Beispiel ist ein benutzerdefiniertes Steuerelement, das es einem Benutzer ermöglicht, frei Hand Eingaben mit einem Lasso auszuwählen.  
  
 [!code-csharp[HowToSelectInk#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToSelectInk/CSharp/InkSelector.cs#1)]
 [!code-vb[HowToSelectInk#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/HowToSelectInk/VisualBasic/InkSelector.vb#1)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Ink.IncrementalLassoHitTester>
- <xref:System.Windows.Ink.StrokeCollection>
- <xref:System.Windows.Input.StylusPointCollection>
- [Erstellen eines Freihandeingabesteuerelements](creating-an-ink-input-control.md)
