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
# <a name="how-to-create-outlined-text"></a><span data-ttu-id="fb092-102">Gewusst wie: Erstellen von umrissenen Text</span><span class="sxs-lookup"><span data-stu-id="fb092-102">How to: Create outlined text</span></span>

<span data-ttu-id="fb092-103">In den meisten Fällen, wenn Sie Text Zeichenfolgen in Ihrer Anwendung Verzierung hinzufügen [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] , verwenden Sie Text in Bezug auf eine Auflistung von diskreten Zeichen oder Glyphen.</span><span class="sxs-lookup"><span data-stu-id="fb092-103">In most cases, when you're adding ornamentation to text strings in your [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] application, you are using text in terms of a collection of discrete characters, or glyphs.</span></span> <span data-ttu-id="fb092-104">Beispielsweise können Sie einen linearen Farbverlaufs Pinsel erstellen und ihn auf die- <xref:System.Windows.Controls.Control.Foreground%2A> Eigenschaft eines- <xref:System.Windows.Controls.TextBox> Objekts anwenden.</span><span class="sxs-lookup"><span data-stu-id="fb092-104">For example, you could create a linear gradient brush and apply it to the <xref:System.Windows.Controls.Control.Foreground%2A> property of a <xref:System.Windows.Controls.TextBox> object.</span></span> <span data-ttu-id="fb092-105">Wenn Sie das Textfeld anzeigen oder bearbeiten, wird der lineare Farbverlaufs Pinsel automatisch auf den aktuellen Satz von Zeichen in der Text Zeichenfolge angewendet.</span><span class="sxs-lookup"><span data-stu-id="fb092-105">When you display or edit the text box, the linear gradient brush is automatically applied to the current set of characters in the text string.</span></span>  
  
 ![Angezeigter Text mit einem linearen Farbverlaufspinsel](./media/how-to-create-outlined-text/text-linear-gradient.jpg)
  
 <span data-ttu-id="fb092-107">Sie können jedoch auch Text in Objekte konvertieren <xref:System.Windows.Media.Geometry> , sodass Sie andere Typen von visuell reichem Text erstellen können.</span><span class="sxs-lookup"><span data-stu-id="fb092-107">However, you can also convert text into <xref:System.Windows.Media.Geometry> objects, allowing you to create other types of visually rich text.</span></span> <span data-ttu-id="fb092-108">Beispielsweise können Sie ein- <xref:System.Windows.Media.Geometry> Objekt auf Grundlage der Gliederung einer Text Zeichenfolge erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb092-108">For example, you could create a <xref:System.Windows.Media.Geometry> object based on the outline of a text string.</span></span>  
  
 ![Textkontur mit einem linearen Farbverlaufspinsel](./media/how-to-create-outlined-text/text-outline-linear-gradient.jpg)  
  
 <span data-ttu-id="fb092-110">Wenn Text in ein-Objekt konvertiert wird <xref:System.Windows.Media.Geometry> , ist er keine Zeichen Auflistung mehr – Sie können die Zeichen in der Text Zeichenfolge nicht mehr ändern.</span><span class="sxs-lookup"><span data-stu-id="fb092-110">When text is converted to a <xref:System.Windows.Media.Geometry> object, it is no longer a collection of characters—you cannot modify the characters in the text string.</span></span> <span data-ttu-id="fb092-111">Sie können jedoch die Darstellung des konvertierten Texts durch Ändern der Strich- und Füllungseigenschaften ändern.</span><span class="sxs-lookup"><span data-stu-id="fb092-111">However, you can affect the appearance of the converted text by modifying its stroke and fill properties.</span></span> <span data-ttu-id="fb092-112">Der Strich bezieht sich auf die Kontur des konvertierten Texts und die Füllung auf den Bereich innerhalb der Kontur.</span><span class="sxs-lookup"><span data-stu-id="fb092-112">The stroke refers to the outline of the converted text; the fill refers to the area inside the outline of the converted text.</span></span>  
  
 <span data-ttu-id="fb092-113">In den folgenden Beispielen werden verschiedene Möglichkeiten zum Erstellen von visuellen Effekten veranschaulicht, indem der Strich und die Füllung des konvertierten Texts geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fb092-113">The following examples illustrate several ways of creating visual effects by modifying the stroke and fill of converted text.</span></span>  
  
 ![Text mit unterschiedlichen Farben für Füllung und Strich](./media/how-to-create-outlined-text/fill-stroke-text-effect.jpg)  
  
 ![Text mit auf Strich angewendeten Bildpinsel](./media/how-to-create-outlined-text/image-brush-application.jpg)
  
 <span data-ttu-id="fb092-116">Es ist auch möglich, das umgebende Rechteck oder die Markierung des konvertierten Texts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="fb092-116">It is also possible to modify the bounding box rectangle, or highlight, of the converted text.</span></span> <span data-ttu-id="fb092-117">Das folgende Beispiel veranschaulicht eine Möglichkeit zum Erstellen von visuellen Effekten durch Ändern des Strichs und der Hervorhebung des konvertierten Texts.</span><span class="sxs-lookup"><span data-stu-id="fb092-117">The following example illustrates a way to create visual effects by modifying the stroke and highlight of converted text.</span></span>  
  
 ![Text mit angewendetem Bild Pinsel auf Strich und Hervorhebung](./media/how-to-create-outlined-text/image-brush-text-application.jpg)

## <a name="example"></a><span data-ttu-id="fb092-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fb092-119">Example</span></span>  
 <span data-ttu-id="fb092-120">Der Schlüssel zum Umrechnen von Text in ein- <xref:System.Windows.Media.Geometry> Objekt ist die Verwendung des- <xref:System.Windows.Media.FormattedText> Objekts.</span><span class="sxs-lookup"><span data-stu-id="fb092-120">The key to converting text to a <xref:System.Windows.Media.Geometry> object is to use the <xref:System.Windows.Media.FormattedText> object.</span></span> <span data-ttu-id="fb092-121">Nachdem Sie dieses Objekt erstellt haben, können Sie die <xref:System.Windows.Media.FormattedText.BuildGeometry%2A> -Methode und die-Methode verwenden, <xref:System.Windows.Media.FormattedText.BuildHighlightGeometry%2A> um den Text in-Objekte zu konvertieren <xref:System.Windows.Media.Geometry> .</span><span class="sxs-lookup"><span data-stu-id="fb092-121">Once you have created this object, you can use the <xref:System.Windows.Media.FormattedText.BuildGeometry%2A> and <xref:System.Windows.Media.FormattedText.BuildHighlightGeometry%2A> methods to convert the text to <xref:System.Windows.Media.Geometry> objects.</span></span> <span data-ttu-id="fb092-122">Die erste Methode gibt die Geometrie des formatierten Texts zurück. die zweite Methode gibt die Geometrie des umgebenden Felds des formatierten Texts zurück.</span><span class="sxs-lookup"><span data-stu-id="fb092-122">The first method returns the geometry of the formatted text; the second method returns the geometry of the formatted text's bounding box.</span></span> <span data-ttu-id="fb092-123">Im folgenden Codebeispiel wird veranschaulicht, wie ein <xref:System.Windows.Media.FormattedText> -Objekt erstellt und die Geometrien des formatierten Texts und das umgebende Feld abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="fb092-123">The following code example shows how to create a <xref:System.Windows.Media.FormattedText> object and to retrieve the geometries of the formatted text and its bounding box.</span></span>  
  
 [!code-csharp[OutlineTextControlViewer#CreateText](~/samples/snippets/csharp/VS_Snippets_Wpf/OutlineTextControlViewer/CSharp/OutlineTextControl.cs#createtext)]
 [!code-vb[OutlineTextControlViewer#CreateText](~/samples/snippets/visualbasic/VS_Snippets_Wpf/OutlineTextControlViewer/visualbasic/outlinetextcontrol.vb#createtext)]  
  
 <span data-ttu-id="fb092-124">Um die abgerufenen <xref:System.Windows.Media.Geometry> Objekte anzuzeigen, müssen Sie auf den <xref:System.Windows.Media.DrawingContext> des Objekts zugreifen, das den konvertierten Text anzeigt.</span><span class="sxs-lookup"><span data-stu-id="fb092-124">In order to display the retrieved the <xref:System.Windows.Media.Geometry> objects, you need to access the <xref:System.Windows.Media.DrawingContext> of the object that's displaying the converted text.</span></span> <span data-ttu-id="fb092-125">In diesen Codebeispielen wird dieser Zugriff erreicht, indem ein benutzerdefiniertes Steuerelement Objekt erstellt wird, das von einer Klasse abgeleitet ist, die das benutzerdefinierte Rendering unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fb092-125">In these code examples, this access is achieved by creating a custom control object that's derived from a class that supports user-defined rendering.</span></span>  
  
 <span data-ttu-id="fb092-126">Wenn Sie <xref:System.Windows.Media.Geometry> Objekte im benutzerdefinierten Steuerelement anzeigen möchten, stellen Sie eine Überschreibung für die- <xref:System.Windows.UIElement.OnRender%2A> Methode bereit.</span><span class="sxs-lookup"><span data-stu-id="fb092-126">To display <xref:System.Windows.Media.Geometry> objects in the custom control, provide an override for the <xref:System.Windows.UIElement.OnRender%2A> method.</span></span> <span data-ttu-id="fb092-127">Die überschriebene Methode sollte die- <xref:System.Windows.Media.DrawingContext.DrawGeometry%2A> Methode verwenden, um die-Objekte zu zeichnen <xref:System.Windows.Media.Geometry> .</span><span class="sxs-lookup"><span data-stu-id="fb092-127">Your overridden method should use the <xref:System.Windows.Media.DrawingContext.DrawGeometry%2A> method to draw the <xref:System.Windows.Media.Geometry> objects.</span></span>  
  
 [!code-csharp[OutlineTextControlViewer#OnRender](~/samples/snippets/csharp/VS_Snippets_Wpf/OutlineTextControlViewer/CSharp/OutlineTextControl.cs#onrender)]
 [!code-vb[OutlineTextControlViewer#OnRender](~/samples/snippets/visualbasic/VS_Snippets_Wpf/OutlineTextControlViewer/visualbasic/outlinetextcontrol.vb#onrender)]  
  
  <span data-ttu-id="fb092-128">Die Quelle des benutzerdefinierten Beispiel-Benutzer Steuerelement Objekts finden Sie unter [OutlineTextControl.cs for c#](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/VS_Snippets_Wpf/OutlineTextControlViewer/CSharp/OutlineTextControl.cs) und [outlinetextcontrol. vb for Visual Basic](https://github.com/dotnet/docs/blob/master/samples/snippets/visualbasic/VS_Snippets_Wpf/OutlineTextControlViewer/visualbasic/outlinetextcontrol.vb).</span><span class="sxs-lookup"><span data-stu-id="fb092-128">For the source of the example custom user control object, see [OutlineTextControl.cs for C#](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/VS_Snippets_Wpf/OutlineTextControlViewer/CSharp/OutlineTextControl.cs) and [OutlineTextControl.vb for Visual Basic](https://github.com/dotnet/docs/blob/master/samples/snippets/visualbasic/VS_Snippets_Wpf/OutlineTextControlViewer/visualbasic/outlinetextcontrol.vb).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fb092-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb092-129">See also</span></span>

- [<span data-ttu-id="fb092-130">Zeichnen von formatiertem Text</span><span class="sxs-lookup"><span data-stu-id="fb092-130">Drawing Formatted Text</span></span>](drawing-formatted-text.md)
