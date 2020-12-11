---
title: Abfangen von Tablettstifteingaben
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- 'architecture [WPF], '
- ', '
- ', '
- ', '
ms.assetid: 791bb2f0-4e5c-4569-ac3c-211996808d44
ms.openlocfilehash: f05a3c25a61e90ec91cd1db725ba9a40763f0a7f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974623"
---
# <a name="intercepting-input-from-the-stylus"></a>Abfangen von Tablettstifteingaben

Die <xref:System.Windows.Input.StylusPlugIns> -Architektur bietet einen Mechanismus zum Implementieren der Steuerung auf niedriger Ebene für <xref:System.Windows.Input.Stylus> die Eingabe und die Erstellung von Digital Ink- <xref:System.Windows.Ink.Stroke> Objekten. Die- <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> Klasse stellt einen Mechanismus bereit, mit dem Sie benutzerdefiniertes Verhalten implementieren und auf den Datenstrom des Tablettstiftgeräts anwenden können, um die optimale Leistung zu erzielen.  
  
 Dieses Thema enthält folgende Unterabschnitte:  
  
- [Architektur](#Architecture)  
  
- [Implementieren von Tablettstift-Plug-ins](#ImplementingStylusPlugins)  
  
- [Hinzufügen des Plug-ins zu einem InkCanvas](#AddingYourPluginToAnInkCanvas)  
  
- [Zusammenfassung](#Conclusion)  
  
<a name="Architecture"></a>

## <a name="architecture"></a>Aufbau  

 Der <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> ist die Entwicklung der [StylusInput](/previous-versions/dotnet/netframework-3.5/ms574861(v=vs.90)) -APIs, die unter [zugreifen auf und manipulieren von Stift Eingaben](/previous-versions/ms818317(v%3dmsdn.10))beschrieben werden.  
  
 Jede <xref:System.Windows.UIElement> verfügt über eine- <xref:System.Windows.UIElement.StylusPlugIns%2A> Eigenschaft, die eine ist <xref:System.Windows.Input.StylusPlugIns.StylusPlugInCollection> . Sie können <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> der-Eigenschaft eines Elements eine hinzufügen <xref:System.Windows.UIElement.StylusPlugIns%2A> , um die Daten zu bearbeiten, <xref:System.Windows.Input.StylusPoint> Wenn Sie generiert werden. <xref:System.Windows.Input.StylusPoint> Daten bestehen aus allen Eigenschaften, die vom System-Digitalisierer unterstützt werden, einschließlich der <xref:System.Windows.Input.StylusPoint.X%2A> -und- <xref:System.Windows.Input.StylusPoint.Y%2A> Punktdaten sowie von <xref:System.Windows.Input.StylusPoint.PressureFactor%2A> Daten.  
  
 Die <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> Objekte werden direkt in den Datenstrom des <xref:System.Windows.Input.Stylus> Geräts eingefügt, wenn Sie der-Eigenschaft hinzufügen <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> <xref:System.Windows.UIElement.StylusPlugIns%2A> . Die Reihenfolge, in der Plug-Ins zur Auflistung hinzugefügt werden, legt <xref:System.Windows.UIElement.StylusPlugIns%2A> die Reihenfolge fest, in der Sie <xref:System.Windows.Input.StylusPoint> Daten erhalten. Wenn Sie z. b. ein Filter-Plug-in hinzufügen, das die Eingabe für eine bestimmte Region einschränkt, und dann ein Plug-in hinzufügen, das Gesten beim Schreiben erkennt, empfängt das Plug-in, das Gesten erkennt, gefilterte <xref:System.Windows.Input.StylusPoint> Daten.  
  
<a name="ImplementingStylusPlugins"></a>

## <a name="implementing-stylus-plug-ins"></a>Implementieren von Tablettstift-Plug-ins  

 Um ein Plug-in zu implementieren, leiten Sie eine Klasse von ab <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> . Diese Klasse wird auf den Datenstrom angewendet, der aus dem stammt <xref:System.Windows.Input.Stylus> . In dieser Klasse können Sie die Werte der Daten ändern <xref:System.Windows.Input.StylusPoint> .  
  
> [!CAUTION]
> Wenn eine <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> Ausnahme auslöst oder eine Ausnahme auslöst, wird die Anwendung geschlossen. Sie sollten Steuerelemente, die einen nutzen, gründlich testen <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> und nur dann ein Steuerelement verwenden, wenn Sie sicher sind, dass <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> keine Ausnahme auslöst.  
  
 Das folgende Beispiel veranschaulicht ein Plug-in, das die Stift Eingabe einschränkt, indem die <xref:System.Windows.Input.StylusPoint.X%2A> -und- <xref:System.Windows.Input.StylusPoint.Y%2A> Werte in den <xref:System.Windows.Input.StylusPoint> Daten vom Gerät geändert werden <xref:System.Windows.Input.Stylus> .  
  
 [!code-csharp[AdvancedInkTopicsSamples#19](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/DynamicRenderer.cs#19)]
 [!code-vb[AdvancedInkTopicsSamples#19](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdvancedInkTopicsSamples/VisualBasic/DynamicRenderer.vb#19)]  
[!code-csharp[AdvancedInkTopicsSamples#3](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/DynamicRenderer.cs#3)]
[!code-vb[AdvancedInkTopicsSamples#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdvancedInkTopicsSamples/VisualBasic/DynamicRenderer.vb#3)]  
  
<a name="AddingYourPluginToAnInkCanvas"></a>

## <a name="adding-your-plug-in-to-an-inkcanvas"></a>Hinzufügen des Plug-ins zu einem InkCanvas  

 Die einfachste Möglichkeit, Ihr benutzerdefiniertes Plug-in zu verwenden, ist die Implementierung einer Klasse, die von InkCanvas abgeleitet und der-Eigenschaft hinzugefügt wird <xref:System.Windows.UIElement.StylusPlugIns%2A> .  
  
 Das folgende Beispiel veranschaulicht eine benutzerdefinierte, die die frei Hand Eingabe <xref:System.Windows.Controls.InkCanvas> filtert.  
  
 [!code-csharp[AdvancedInkTopicsSamples#4](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/Window1.xaml.cs#4)]  
  
 Wenn Sie Ihrer Anwendung eine hinzufügen `FilterInkCanvas` und diese ausführen, werden Sie feststellen, dass die frei Hand Eingabe nicht auf eine Region beschränkt ist, bis der Benutzer einen Strich abschließt. Dies liegt daran, dass die <xref:System.Windows.Controls.InkCanvas> über eine <xref:System.Windows.Controls.InkCanvas.DynamicRenderer%2A> -Eigenschaft verfügt, die ein ist <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> und bereits ein Member der-Auflistung ist <xref:System.Windows.UIElement.StylusPlugIns%2A> . Das benutzerdefinierte <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> , das Sie der Auflistung hinzugefügt haben, <xref:System.Windows.UIElement.StylusPlugIns%2A> empfängt die Daten nach dem Empfang von <xref:System.Windows.Input.StylusPoint> <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> Daten Infolgedessen <xref:System.Windows.Input.StylusPoint> werden die Daten erst gefiltert, wenn der Benutzer den Stift zum Beenden eines Strichs anhebt. Um die frei Hand Eingaben zu filtern, während Sie vom Benutzer gezeichnet werden, müssen Sie die `FilterPlugin` vor dem Einfügen <xref:System.Windows.Input.StylusPlugIns.DynamicRenderer> .  
  
 Der folgende c#-Code veranschaulicht eine benutzerdefinierte, die die frei Hand Eingabe <xref:System.Windows.Controls.InkCanvas> filtert, während Sie gezeichnet wird.  
  
 [!code-csharp[AdvancedInkTopicsSamples#5](~/samples/snippets/csharp/VS_Snippets_Wpf/AdvancedInkTopicsSamples/CSharp/Window1.xaml.cs#5)]  
  
<a name="Conclusion"></a>

## <a name="conclusion"></a>Zusammenfassung  

 Indem Sie Ihre eigenen <xref:System.Windows.Input.StylusPlugIns.StylusPlugIn> Klassen ableiten und in Auflistungen einfügen <xref:System.Windows.Input.StylusPlugIns.StylusPlugInCollection> , können Sie das Verhalten Ihrer digitalen Handschrift erheblich verbessern. Sie haben Zugriff auf die <xref:System.Windows.Input.StylusPoint> Daten, wenn Sie generiert werden, und haben die Möglichkeit, die <xref:System.Windows.Input.Stylus> Eingabe anzupassen. Da Sie über einen solchen Zugriff auf die Daten auf niedriger Ebene verfügen <xref:System.Windows.Input.StylusPoint> , können Sie die frei Hand Erfassung und das Rendering mit optimaler Leistung für Ihre Anwendung implementieren.  
  
## <a name="see-also"></a>Siehe auch

- [Erweiterte Behandlung von Freihandeingaben](advanced-ink-handling.md)
- [Zugreifen auf und Bearbeiten von Stift Eingaben](/previous-versions/ms818317(v%3dmsdn.10))
