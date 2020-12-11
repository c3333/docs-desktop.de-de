---
title: 'Gewusst wie: Erstellen von Text mit Kontur'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- typography [WPF], linear gradient brush
- outlined text [WPF]
- gradient brush [WPF]
- linear gradient brush [WPF]
- typography [WPF], outline effects
ms.assetid: 4aa3cf6e-1953-4f26-8230-7c1409e5f28d
ms.openlocfilehash: 44d9d1ecfa3a541ad499da83ffd0792b768c2662
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974679"
---
# <a name="how-to-create-outlined-text"></a>Gewusst wie: Erstellen von umrissenen Text

In den meisten Fällen, wenn Sie Text Zeichenfolgen in Ihrer Anwendung Verzierung hinzufügen [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] , verwenden Sie Text in Bezug auf eine Auflistung von diskreten Zeichen oder Glyphen. Beispielsweise können Sie einen linearen Farbverlaufs Pinsel erstellen und ihn auf die- <xref:System.Windows.Controls.Control.Foreground%2A> Eigenschaft eines- <xref:System.Windows.Controls.TextBox> Objekts anwenden. Wenn Sie das Textfeld anzeigen oder bearbeiten, wird der lineare Farbverlaufs Pinsel automatisch auf den aktuellen Satz von Zeichen in der Text Zeichenfolge angewendet.  
  
 ![Angezeigter Text mit einem linearen Farbverlaufspinsel](./media/how-to-create-outlined-text/text-linear-gradient.jpg)
  
 Sie können jedoch auch Text in Objekte konvertieren <xref:System.Windows.Media.Geometry> , sodass Sie andere Typen von visuell reichem Text erstellen können. Beispielsweise können Sie ein- <xref:System.Windows.Media.Geometry> Objekt auf Grundlage der Gliederung einer Text Zeichenfolge erstellen.  
  
 ![Textkontur mit einem linearen Farbverlaufspinsel](./media/how-to-create-outlined-text/text-outline-linear-gradient.jpg)  
  
 Wenn Text in ein-Objekt konvertiert wird <xref:System.Windows.Media.Geometry> , ist er keine Zeichen Auflistung mehr – Sie können die Zeichen in der Text Zeichenfolge nicht mehr ändern. Sie können jedoch die Darstellung des konvertierten Texts durch Ändern der Strich- und Füllungseigenschaften ändern. Der Strich bezieht sich auf die Kontur des konvertierten Texts und die Füllung auf den Bereich innerhalb der Kontur.  
  
 In den folgenden Beispielen werden verschiedene Möglichkeiten zum Erstellen von visuellen Effekten veranschaulicht, indem der Strich und die Füllung des konvertierten Texts geändert werden.  
  
 ![Text mit unterschiedlichen Farben für Füllung und Strich](./media/how-to-create-outlined-text/fill-stroke-text-effect.jpg)  
  
 ![Text mit auf Strich angewendeten Bildpinsel](./media/how-to-create-outlined-text/image-brush-application.jpg)
  
 Es ist auch möglich, das umgebende Rechteck oder die Markierung des konvertierten Texts zu ändern. Das folgende Beispiel veranschaulicht eine Möglichkeit zum Erstellen von visuellen Effekten durch Ändern des Strichs und der Hervorhebung des konvertierten Texts.  
  
 ![Text mit angewendetem Bild Pinsel auf Strich und Hervorhebung](./media/how-to-create-outlined-text/image-brush-text-application.jpg)

## <a name="example"></a>Beispiel  
 Der Schlüssel zum Umrechnen von Text in ein- <xref:System.Windows.Media.Geometry> Objekt ist die Verwendung des- <xref:System.Windows.Media.FormattedText> Objekts. Nachdem Sie dieses Objekt erstellt haben, können Sie die <xref:System.Windows.Media.FormattedText.BuildGeometry%2A> -Methode und die-Methode verwenden, <xref:System.Windows.Media.FormattedText.BuildHighlightGeometry%2A> um den Text in-Objekte zu konvertieren <xref:System.Windows.Media.Geometry> . Die erste Methode gibt die Geometrie des formatierten Texts zurück. die zweite Methode gibt die Geometrie des umgebenden Felds des formatierten Texts zurück. Im folgenden Codebeispiel wird veranschaulicht, wie ein <xref:System.Windows.Media.FormattedText> -Objekt erstellt und die Geometrien des formatierten Texts und das umgebende Feld abgerufen werden.  
  
 [!code-csharp[OutlineTextControlViewer#CreateText](~/samples/snippets/csharp/VS_Snippets_Wpf/OutlineTextControlViewer/CSharp/OutlineTextControl.cs#createtext)]
 [!code-vb[OutlineTextControlViewer#CreateText](~/samples/snippets/visualbasic/VS_Snippets_Wpf/OutlineTextControlViewer/visualbasic/outlinetextcontrol.vb#createtext)]  
  
 Um die abgerufenen <xref:System.Windows.Media.Geometry> Objekte anzuzeigen, müssen Sie auf den <xref:System.Windows.Media.DrawingContext> des Objekts zugreifen, das den konvertierten Text anzeigt. In diesen Codebeispielen wird dieser Zugriff erreicht, indem ein benutzerdefiniertes Steuerelement Objekt erstellt wird, das von einer Klasse abgeleitet ist, die das benutzerdefinierte Rendering unterstützt.  
  
 Wenn Sie <xref:System.Windows.Media.Geometry> Objekte im benutzerdefinierten Steuerelement anzeigen möchten, stellen Sie eine Überschreibung für die- <xref:System.Windows.UIElement.OnRender%2A> Methode bereit. Die überschriebene Methode sollte die- <xref:System.Windows.Media.DrawingContext.DrawGeometry%2A> Methode verwenden, um die-Objekte zu zeichnen <xref:System.Windows.Media.Geometry> .  
  
 [!code-csharp[OutlineTextControlViewer#OnRender](~/samples/snippets/csharp/VS_Snippets_Wpf/OutlineTextControlViewer/CSharp/OutlineTextControl.cs#onrender)]
 [!code-vb[OutlineTextControlViewer#OnRender](~/samples/snippets/visualbasic/VS_Snippets_Wpf/OutlineTextControlViewer/visualbasic/outlinetextcontrol.vb#onrender)]  
  
  Die Quelle des benutzerdefinierten Beispiel-Benutzer Steuerelement Objekts finden Sie unter [OutlineTextControl.cs for c#](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/VS_Snippets_Wpf/OutlineTextControlViewer/CSharp/OutlineTextControl.cs) und [outlinetextcontrol. vb for Visual Basic](https://github.com/dotnet/docs/blob/master/samples/snippets/visualbasic/VS_Snippets_Wpf/OutlineTextControlViewer/visualbasic/outlinetextcontrol.vb).
  
## <a name="see-also"></a>Siehe auch

- [Zeichnen von formatiertem Text](drawing-formatted-text.md)
