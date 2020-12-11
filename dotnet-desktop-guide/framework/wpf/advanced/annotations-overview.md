---
title: Übersicht über Anmerkungen
ms.date: 03/30/2017
ms.topic: overview
dev_langs:
- csharp
- vb
helpviewer_keywords:
- highlights [WPF]
- documents [WPF], annotations
- sticky notes [WPF]
ms.assetid: 716bf474-29bd-4c74-84a4-8e0744bdad62
ms.openlocfilehash: 8cfd5ddd1d90e9995081cd47211e1d9b0462b100
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977504"
---
# <a name="annotations-overview"></a><span data-ttu-id="ec6ea-102">Übersicht über Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="ec6ea-102">Annotations Overview</span></span>

<span data-ttu-id="ec6ea-103">Das Schreiben von Notizen oder Kommentare auf Papierdokumenten ist solch eine verbreitete Aktivität, dass wir sie als selbstverständlich erachten.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-103">Writing notes or comments on paper documents is such a commonplace activity that we almost take it for granted.</span></span> <span data-ttu-id="ec6ea-104">Diese Notizen oder Kommentare sind „Anmerkungen“, die wir einem Dokument hinzufügen, um Informationen zu kennzeichnen oder um interessante Elemente für einen späteren Zeitpunkt zu markieren.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-104">These notes or comments are "annotations" that we add to a document to flag information or to highlight items of interest for later reference.</span></span> <span data-ttu-id="ec6ea-105">Obwohl das Schreiben von Notizen auf gedruckte Dokumente einfach und üblich ist, ist die Möglichkeit, persönliche Kommentare auf elektronischen Dokumenten hinzuzufügen, in der Regel nur sehr eingeschränkt, falls diese Möglichkeit überhaupt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-105">Although writing notes on printed documents is easy and commonplace, the ability to add personal comments to electronic documents is typically very limited, if available at all.</span></span>  
  
 <span data-ttu-id="ec6ea-106">In diesem Thema werden verschiedene häufige Typen von Anmerkungen, insbesondere kurz Notizen und Highlights, erläutert und veranschaulicht, wie das Microsoft Anmerkungen-Framework diese Arten von Anmerkungen in Anwendungen über die Steuerelemente für das Anzeigen von Windows Presentation Foundation (WPF)-Steuerelementen erleichtert.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-106">This topic reviews several common types of annotations, specifically sticky notes and highlights, and illustrates how the Microsoft Annotations Framework facilitates these types of annotations in applications through the Windows Presentation Foundation (WPF) document viewing controls.</span></span>  <span data-ttu-id="ec6ea-107">WPF-Dokument Anzeige Steuerelemente, die Anmerkungen unterstützen <xref:System.Windows.Controls.FlowDocumentReader> , umfassen und <xref:System.Windows.Controls.FlowDocumentScrollViewer> sowie Steuerelemente, die von abgeleitet werden, <xref:System.Windows.Controls.Primitives.DocumentViewerBase> z. b <xref:System.Windows.Controls.DocumentViewer> <xref:System.Windows.Controls.FlowDocumentPageViewer> . und.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-107">WPF document viewing controls that support annotations include <xref:System.Windows.Controls.FlowDocumentReader> and <xref:System.Windows.Controls.FlowDocumentScrollViewer>, as well as controls derived from <xref:System.Windows.Controls.Primitives.DocumentViewerBase> such as <xref:System.Windows.Controls.DocumentViewer> and <xref:System.Windows.Controls.FlowDocumentPageViewer>.</span></span>  

<a name="caf1_type_stickynotes"></a>

## <a name="sticky-notes"></a><span data-ttu-id="ec6ea-108">Kurznotizen</span><span class="sxs-lookup"><span data-stu-id="ec6ea-108">Sticky Notes</span></span>  

 <span data-ttu-id="ec6ea-109">Eine normale Kurznotiz enthält Informationen, die auf ein kleines Stück farbiges Papier geschrieben werden, das dann auf ein Dokument „geklebt“ wird.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-109">A typical sticky note contains information written on a small piece of colored paper that is then "stuck" to a document.</span></span> <span data-ttu-id="ec6ea-110">Digitale kurz Notizen bieten ähnliche Funktionen für elektronische Dokumente, aber mit der zusätzlichen Flexibilität, viele andere Inhaltstypen wie typisierten Text, handschriftliche Notizen (z. b. Tablet PC "Hand Eingaben") oder Weblinks einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-110">Digital sticky notes provide similar functionality for electronic documents, but with the added flexibility to include many other types of content such as typed text, handwritten notes (for example, Tablet PC "ink" strokes), or Web links.</span></span>  
  
 <span data-ttu-id="ec6ea-111">Die folgende Abbildung zeigt einige Beispiele von Hervorhebungen, Kurznotizen und Freihandnotizanmerkungen.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-111">The following illustration shows some examples of highlight, text sticky note, and ink sticky note annotations.</span></span>  
  
 <span data-ttu-id="ec6ea-112">![Textmarker-, Text- und Freihandnotizanmerkungen](./media/caf-stickynote.jpg "CAF_StickyNote")</span><span class="sxs-lookup"><span data-stu-id="ec6ea-112">![Highlight, text and ink sticky note annotations.](./media/caf-stickynote.jpg "CAF_StickyNote")</span></span>  
  
 <span data-ttu-id="ec6ea-113">Das folgende Beispiel zeigt die Methode, die Sie zum Aktivieren der Unterstützung von Kommentaren in der Anwendung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-113">The following example shows the method that you can use to enable annotation support in your application.</span></span>  
  
 [!code-csharp[DocViewerAnnotationsXml#DocViewXmlStartAnnotations](~/samples/snippets/csharp/VS_Snippets_Wpf/DocViewerAnnotationsXml/CSharp/Window1.xaml.cs#docviewxmlstartannotations)]
 [!code-vb[DocViewerAnnotationsXml#DocViewXmlStartAnnotations](~/samples/snippets/visualbasic/VS_Snippets_Wpf/DocViewerAnnotationsXml/visualbasic/window1.xaml.vb#docviewxmlstartannotations)]  
  
<a name="caf1_type_callouts"></a>

## <a name="highlights"></a><span data-ttu-id="ec6ea-114">Highlights</span><span class="sxs-lookup"><span data-stu-id="ec6ea-114">Highlights</span></span>  

 <span data-ttu-id="ec6ea-115">Personen, die kreative Methoden verwenden, können Aufmerksamkeit auf Elemente ziehen, wenn Sie ein Papierdokument beschreiben, z.B. Wörter in einem Satz unterstreichen, markieren, einkreisen oder Markierungen oder Notationen am Rand hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-115">People use creative methods to draw attention to items of interest when they mark up a paper document, such as underlining, highlighting, circling words in a sentence, or drawing marks or notations in the margin.</span></span>  <span data-ttu-id="ec6ea-116">Hervorhebungs Anmerkungen im Microsoft Anmerkungen Framework bieten ein ähnliches Feature zum Markieren von Informationen, die in WPF-Dokument Anzeige Steuerelementen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-116">Highlight annotations in Microsoft Annotations Framework provide a similar feature for marking up information displayed in WPF document viewing controls.</span></span>  
  
 <span data-ttu-id="ec6ea-117">In der folgenden Abbildung ist ein Beispiel einer markierten Anmerkung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="ec6ea-117">The following illustration shows an example of a highlight annotation.</span></span>  
  
 <span data-ttu-id="ec6ea-118">![Anmerkung hervorheben](./media/caf-callouts.png "CAF_Callouts")</span><span class="sxs-lookup"><span data-stu-id="ec6ea-118">![Highlight Annotation](./media/caf-callouts.png "CAF_Callouts")</span></span>  
  
 <span data-ttu-id="ec6ea-119">Benutzer erstellen in der Regel Anmerkungen, indem Sie zuerst Text oder ein interessantes Element auswählen und dann mit der rechten Maustaste klicken, um eine <xref:System.Windows.Controls.ContextMenu> der Anmerkung-Optionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-119">Users typically create annotations by first selecting some text or an item of interest, and then right-clicking to display a <xref:System.Windows.Controls.ContextMenu> of annotation options.</span></span>  <span data-ttu-id="ec6ea-120">Das folgende Beispiel zeigt [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] , wie Sie einen mit weitergeleiteten Befehlen deklarieren können <xref:System.Windows.Controls.ContextMenu> , auf die Benutzer zugreifen können, um Anmerkungen zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-120">The following example shows the [!INCLUDE[TLA#tla_xaml](../../../includes/tlasharptla-xaml-md.md)] you can use to declare a <xref:System.Windows.Controls.ContextMenu> with routed commands that users can access to create and manage annotations.</span></span>  
  
 [!code-xaml[DocViewerAnnotationsXps#CreateDeleteAnnotations](~/samples/snippets/csharp/VS_Snippets_Wpf/DocViewerAnnotationsXps/CSharp/Window1.xaml#createdeleteannotations)]  
  
<a name="caf1_framework_data_anchoring"></a>

## <a name="data-anchoring"></a><span data-ttu-id="ec6ea-121">Verankerung von Daten</span><span class="sxs-lookup"><span data-stu-id="ec6ea-121">Data Anchoring</span></span>  

 <span data-ttu-id="ec6ea-122">Das Anmerkungen-Framework bindet Anmerkungen an die Daten, die der Benutzer auswählt, nicht nur an eine Position in der Anzeige Ansicht.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-122">The Annotations Framework binds annotations to the data that the user selects, not just to a position on the display view.</span></span> <span data-ttu-id="ec6ea-123">Deshalb bleibt die Anmerkung bei der Datenauswahl, an die sie gebunden ist, wenn der Benutzer das Anzeigefenster nach oben oder unten verschiebt oder die Größe ändert, wenn sich die Dokumentansicht ändert.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-123">Therefore, if the document view changes, such as when the user scrolls or resizes the display window, the annotation stays with the data selection to which it is bound.</span></span> <span data-ttu-id="ec6ea-124">Die folgende Abbildung zeigt z.B. eine Anmerkung, die der Benutzer für einen Textausschnitt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-124">For example, the following graphic illustrates an annotation that the user has made on a text selection.</span></span> <span data-ttu-id="ec6ea-125">Wenn sich die Dokumentansicht ändert (durch Bildlauf, Größenänderung, Skalierung usw.), wird die hervorgehobene Anmerkung mit den ausgewählten Daten verschoben.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-125">When the document view changes (scrolls, resizes, scales, or otherwise moves), the highlight annotation moves with the original data selection.</span></span>  
  
 <span data-ttu-id="ec6ea-126">![Anmerkungsdaten-Verankerung](./media/caf-dataanchoring.png "CAF_DataAnchoring")</span><span class="sxs-lookup"><span data-stu-id="ec6ea-126">![Annotation Data Anchoring](./media/caf-dataanchoring.png "CAF_DataAnchoring")</span></span>  
  
<a name="matching_annotations_with_annotated_objects"></a>

## <a name="matching-annotations-with-annotated-objects"></a><span data-ttu-id="ec6ea-127">Abgleichen von Anmerkung mit Objekten mit Anmerkungen</span><span class="sxs-lookup"><span data-stu-id="ec6ea-127">Matching Annotations with Annotated Objects</span></span>  

 <span data-ttu-id="ec6ea-128">Sie können Anmerkungen den entsprechenden kommentierten Objekten zuordnen.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-128">You can match annotations with the corresponding annotated objects.</span></span> <span data-ttu-id="ec6ea-129">Betrachten Sie beispielsweise eine einfache Dokumentleseranwendung, die über einen Kommentarbereich verfügt.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-129">For example, consider a simple document reader application that has a comments pane.</span></span> <span data-ttu-id="ec6ea-130">Der Kommentarbereich ist möglicherweise ein Listenfeld, das den Text aus einer Liste von Anmerkungen anzeigt, die mit einem Dokument verankert sind.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-130">The comments pane might be a list box that displays the text from a list of annotations that are anchored to a document.</span></span> <span data-ttu-id="ec6ea-131">Wenn der Benutzer ein Element im Listenfeld auswählt, zeigt die Anwendung den Abschnitt im Dokument, mit dem das entsprechende Anmerkungsobjekt verankert ist.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-131">If the user selects an item in the list box, then the application brings into view the paragraph in the document that the corresponding annotation object is anchored to.</span></span>  
  
 <span data-ttu-id="ec6ea-132">Im folgenden Beispiel wird veranschaulicht, wie der Ereignishandler eines solchen Listenfelds, das als Kommentarbereich dient, implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-132">The following example demonstrates how to implement the event handler of such a list box that serves as the comments pane.</span></span>  
  
 [!code-csharp[FlowDocumentAnnotatedViewer#Handler](~/samples/snippets/csharp/VS_Snippets_Wpf/FlowDocumentAnnotatedViewer/CSharp/Window1.xaml.cs#handler)]
 [!code-vb[FlowDocumentAnnotatedViewer#Handler](~/samples/snippets/visualbasic/VS_Snippets_Wpf/FlowDocumentAnnotatedViewer/visualbasic/window1.xaml.vb#handler)]  
  
 <span data-ttu-id="ec6ea-133">Ein weiteres Beispielszenario umfasst Anwendungen, die den Austausch von Anmerkungen und kurz Notizen zwischen Dokument Lesern per e-Mail ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-133">Another example scenario involves applications that enable the exchange of annotations and sticky notes between document readers through email.</span></span> <span data-ttu-id="ec6ea-134">Diese Funktion ermöglicht diesen Programmen, den Leser zu der Seite zu navigieren, die die Anmerkung enthält, die gerade ausgetauscht wird.</span><span class="sxs-lookup"><span data-stu-id="ec6ea-134">This feature enables these applications to navigate the reader to the page that contains the annotation that is being exchanged.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="ec6ea-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec6ea-135">See also</span></span>

- <xref:System.Windows.Controls.Primitives.DocumentViewerBase>
- <xref:System.Windows.Controls.DocumentViewer>
- <xref:System.Windows.Controls.FlowDocumentPageViewer>
- <xref:System.Windows.Controls.FlowDocumentScrollViewer>
- <xref:System.Windows.Controls.FlowDocumentReader>
- <xref:System.Windows.Annotations.IAnchorInfo>
- [<span data-ttu-id="ec6ea-136">Annotations-Schema</span><span class="sxs-lookup"><span data-stu-id="ec6ea-136">Annotations Schema</span></span>](annotations-schema.md)
- [<span data-ttu-id="ec6ea-137">Übersicht über ContextMenu</span><span class="sxs-lookup"><span data-stu-id="ec6ea-137">ContextMenu Overview</span></span>](../controls/contextmenu-overview.md)
- [<span data-ttu-id="ec6ea-138">Befehlsübersicht</span><span class="sxs-lookup"><span data-stu-id="ec6ea-138">Commanding Overview</span></span>](commanding-overview.md)
- [<span data-ttu-id="ec6ea-139">Übersicht über Flussdokumente</span><span class="sxs-lookup"><span data-stu-id="ec6ea-139">Flow Document Overview</span></span>](flow-document-overview.md)
- <span data-ttu-id="ec6ea-140">[How to: Add a Command to a MenuItem (Vorgehensweise: Hinzufügen eines Befehls zu einem MenuItem)](/previous-versions/dotnet/netframework-3.5/ms741839(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="ec6ea-140">[How to: Add a Command to a MenuItem](/previous-versions/dotnet/netframework-3.5/ms741839(v=vs.90))</span></span>
