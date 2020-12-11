---
title: Erfassen digitaler Freihand
ms.date: 08/15/2018
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ink [WPF], collecting
- InkCanvas element [WPF]
- properties [WPF], DrawingAttributes
- collecting digital ink [WPF]
- digital ink [WPF], collecting
- properties [WPF], DefaultDrawingAttributes
- DefaultDrawingAttributes property [WPF]
ms.assetid: 66a3129d-9577-43eb-acbd-56c147282016
ms.openlocfilehash: 813a5313a6fbf83c36cdbed1f64ce69a217ad788
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976422"
---
# <a name="collect-ink"></a>Frei Hand Eingaben erfassen

Als einen ihrer zentralen Funktionsbestandteile erfasst die [Windows Presentation Foundation](../index.md)-Plattform Freihandeingaben. In diesem Thema werden die Methoden für die Sammlung von frei Hand Eingaben in Windows Presentation Foundation (WPF) erläutert.

## <a name="prerequisites"></a>Voraussetzungen

Um die folgenden Beispiele verwenden zu können, müssen Sie zuerst Visual Studio und den Windows SDK installieren. Außerdem sollten Sie wissen, wie Anwendungen für das WPF geschrieben werden. Weitere Informationen zu den ersten Schritten mit WPF finden Sie unter Exemplarische Vorgehensweise [: meine erste WPF-Desktop Anwendung](../getting-started/walkthrough-my-first-wpf-desktop-application.md).

## <a name="use-the-inkcanvas-element"></a>Verwenden des InkCanvas-Elements

Das- <xref:System.Windows.Controls.InkCanvas?displayProperty=fullName> Element stellt die einfachste Möglichkeit zum Erfassen von frei Hand Eingaben in WPF bereit. Verwenden <xref:System.Windows.Controls.InkCanvas> Sie ein-Element, um frei Hand Eingaben zu empfangen und anzuzeigen. Freihandeingaben erfolgen im Allgemeinen mithilfe eines Tablettstifts, der über ein Digitalisierungsgerät Freihandstriche erzeugt. Anstelle eines Tablettstifts kann auch eine Maus verwendet werden. Die erstellten Striche werden als <xref:System.Windows.Ink.Stroke> -Objekte dargestellt und können sowohl Programm gesteuert als auch durch Benutzereingaben bearbeitet werden. <xref:System.Windows.Controls.InkCanvas>Ermöglicht es Benutzern, ein vorhandenes auszuwählen, zu ändern oder zu löschen <xref:System.Windows.Ink.Stroke> .

Mithilfe von XAML können Sie die frei Hand Auflistung so einfach einrichten, wie Sie der Struktur ein **InkCanvas** -Element hinzufügen. Im folgenden Beispiel wird ein einem <xref:System.Windows.Controls.InkCanvas> standardmäßigen WPF-Projekt hinzugefügt, das in Visual Studio erstellt wurde:

[!code-xaml[DigitalInkTopics#6](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window2.xaml#6)]

Das **InkCanvas** -Element kann auch untergeordnete Elemente enthalten, sodass Sie nahezu allen Typen von XAML-Elementen frei Hand Anmerkung-Funktionen hinzufügen können. Wenn Sie z. b. einem Textelement eine Verknüpfung hinzufügen möchten, machen Sie es einfach zu einem untergeordneten Element <xref:System.Windows.Controls.InkCanvas> :

[!code-xaml[DigitalInkTopics#5](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window2.xaml#5)]

Das Hinzufügen von Unterstützung für das Markieren eines Bilds mit frei Hand Eingaben ist ebenso einfach:

[!code-xaml[DigitalInkTopics#7](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window2.xaml#7)]

### <a name="inkcollection-modes"></a>InkCollection-Modi

Der <xref:System.Windows.Controls.InkCanvas> bietet Unterstützung für verschiedene Eingabemodi durch seine- <xref:System.Windows.Controls.InkCanvas.EditingMode%2A> Eigenschaft.

### <a name="manipulate-ink"></a>Freihand bearbeiten

<xref:System.Windows.Controls.InkCanvas>Bietet Unterstützung für viele Freihand Bearbeitungsvorgänge. Unterstützt z. b. die <xref:System.Windows.Controls.InkCanvas> Löschfunktion zum Löschen, und es ist kein zusätzlicher Code erforderlich, um dem-Element die Funktionalität hinzuzufügen.

#### <a name="selection"></a>Auswahl

Das Festlegen des Auswahlmodus ist so einfach wie das Festlegen der- <xref:System.Windows.Controls.InkCanvasEditingMode> Eigenschaft auf **Select**.

Der folgende Code legt den Bearbeitungsmodus basierend auf dem Wert einer fest <xref:System.Windows.Forms.CheckBox> :

[!code-csharp[DigitalInkTopics#8](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window1.xaml.cs#8)]
[!code-vb[DigitalInkTopics#8](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DigitalInkTopics/VisualBasic/Window1.xaml.vb#8)]

#### <a name="drawingattributes"></a>DrawingAttributes

Verwenden Sie die- <xref:System.Windows.Ink.Stroke.DrawingAttributes%2A> Eigenschaft, um die Darstellung von Hand Strichen zu ändern. Beispielsweise legt der <xref:System.Windows.Ink.DrawingAttributes.Color%2A> Member von <xref:System.Windows.Ink.DrawingAttributes> die Farbe des gerenderten fest <xref:System.Windows.Ink.Stroke> .

Im folgenden Beispiel wird die Farbe der ausgewählten Striche in rot geändert:

[!code-csharp[DigitalInkTopics#9](~/samples/snippets/csharp/VS_Snippets_Wpf/DigitalInkTopics/CSharp/Window1.xaml.cs#9)]
[!code-vb[DigitalInkTopics#9](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DigitalInkTopics/VisualBasic/Window1.xaml.vb#9)]

### <a name="defaultdrawingattributes"></a>DefaultDrawingAttributes

Die- <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> Eigenschaft ermöglicht den Zugriff auf Eigenschaften, z. b. Höhe, Breite und Farbe der Striche, die in einer erstellt werden sollen <xref:System.Windows.Controls.InkCanvas> . Nachdem Sie das geändert <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> haben, werden alle zukünftigen Striche, die in eingegeben <xref:System.Windows.Controls.InkCanvas> werden, mit den neuen Eigenschafts Werten gerendert.

Zusätzlich zum Ändern der <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> in der Code Behind-Datei können Sie die XAML-Syntax zum Angeben von <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A> Eigenschaften verwenden.

Im nächsten Beispiel wird veranschaulicht, wie die-Eigenschaft festgelegt wird <xref:System.Windows.Ink.DrawingAttributes.Color%2A> . Um diesen Code zu verwenden, erstellen Sie in Visual Studio ein neues WPF-Projekt mit dem Namen "HelloInkCanvas". Ersetzen Sie den Code in der Datei " *MainWindow. XAML* " durch den folgenden Code:

[!code-xaml[HelloInkCanvas#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HelloInkCanvas/CSharp/Window1.xaml#1)]

Fügen Sie als nächstes die folgenden Ereignishandler für die Schaltfläche der Code-Behind-Datei innerhalb der MainWindow-Klasse hinzu:

[!code-csharp[HelloInkCanvas#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HelloInkCanvas/CSharp/Window1.xaml.cs#2)]

Nachdem Sie diesen Code kopiert haben, drücken Sie in Visual Studio **F5** , um das Programm im Debugger auszuführen.

Beachten Sie, wie die <xref:System.Windows.Controls.StackPanel> Schaltflächen auf dem platziert <xref:System.Windows.Controls.InkCanvas> . Wenn Sie versuchen, über den oberen Rand der Schaltflächen zu übergeben, <xref:System.Windows.Controls.InkCanvas> sammelt und rendert die frei Hand Eingaben hinter den Schaltflächen. Dies liegt daran, dass die Schaltflächen gleich geordnete Elemente von sind und nicht untergeordnete Elemente <xref:System.Windows.Controls.InkCanvas> . Außerdem sind die Schaltflächen in der Z-Reihenfolge weiter oben, weshalb die Freihandeingaben dahinter gerendert werden.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Ink.DrawingAttributes>
- <xref:System.Windows.Controls.InkCanvas.DefaultDrawingAttributes%2A>
- <xref:System.Windows.Ink>
