---
title: Features für OpenType-Schriftarten
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- fonts [WPF], OpenType
- typography [WPF], OpenType font technology
- OpenType font technology [WPF]
ms.assetid: 4061a9d1-fe8b-4921-9e17-18ec7d2e3ea2
ms.openlocfilehash: 5f9f5b14400962af2da94dd60f5170cb2f3d2f51
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975426"
---
# <a name="opentype-font-features"></a><span data-ttu-id="7d6d0-102">Features für OpenType-Schriftarten</span><span class="sxs-lookup"><span data-stu-id="7d6d0-102">OpenType Font Features</span></span>

<span data-ttu-id="7d6d0-103">Dieses Thema enthält eine Übersicht über einige der wichtigsten Features der OpenType-Schriftart Technologie in [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-103">This topic provides an overview of some of the key features of OpenType font technology in [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)].</span></span>  
  
<a name="overview"></a>

## <a name="opentype-font-format"></a><span data-ttu-id="7d6d0-104">OpenType-Schriftartformat</span><span class="sxs-lookup"><span data-stu-id="7d6d0-104">OpenType Font Format</span></span>  

 <span data-ttu-id="7d6d0-105">Das OpenType-Schriftart Format ist eine Erweiterung des TrueType-® Schriftart Formats und fügt Unterstützung für PostScript-Schriftart Daten hinzu.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-105">The OpenType font format is an extension of the TrueType® font format, adding support for PostScript font data.</span></span> <span data-ttu-id="7d6d0-106">Das OpenType-Schriftformat wurde von Microsoft und Adobe Corporation gemeinsam entwickelt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-106">The OpenType font format was developed jointly by Microsoft and Adobe Corporation.</span></span> <span data-ttu-id="7d6d0-107">OpenType-Schriftarten und die Betriebssystem Dienste, die OpenType-Schriftarten unterstützen, bieten Benutzern eine einfache Möglichkeit zum Installieren und Verwenden von Schriftarten, unabhängig davon, ob die Schriftarten TrueType-und CFF-Gliederungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-107">OpenType fonts and the operating system services which support OpenType fonts provide users with a simple way to install and use fonts, whether the fonts contain TrueType outlines or CFF (PostScript) outlines.</span></span>  
  
 <span data-ttu-id="7d6d0-108">Das OpenType-Schriftformat behandelt die folgenden Entwickler Herausforderungen:</span><span class="sxs-lookup"><span data-stu-id="7d6d0-108">The OpenType font format addresses the following developer challenges:</span></span>  
  
- <span data-ttu-id="7d6d0-109">Breitere Multiplattform-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-109">Broader multi-platform support.</span></span>  
  
- <span data-ttu-id="7d6d0-110">Bessere Unterstützung für internationale Zeichensätze.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-110">Better support for international character sets.</span></span>  
  
- <span data-ttu-id="7d6d0-111">Besserer Schutz der Schriftartdaten.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-111">Better protection for font data.</span></span>  
  
- <span data-ttu-id="7d6d0-112">Kleinere Dateigrößen die eine effizientere Schriftartenverteilung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-112">Smaller file sizes to make font distribution more efficient.</span></span>  
  
- <span data-ttu-id="7d6d0-113">Breitere Unterstützung für erweiterte typografische Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-113">Broader support for advanced typographic control.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="7d6d0-114">Die Windows SDK enthält eine Reihe von OpenType-Beispiel Schriftarten, die Sie mit-Anwendungen verwenden können [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-114">The Windows SDK contains a set of sample OpenType fonts that you can use with [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] applications.</span></span> <span data-ttu-id="7d6d0-115">Diese Schriftarten bieten die meisten der Funktionen, wie im folgenden Thema dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-115">These fonts provide most of the features illustrated in the rest of this topic.</span></span> <span data-ttu-id="7d6d0-116">Weitere Informationen finden Sie unter [Sample OpenType Font Pack](sample-opentype-font-pack.md).</span><span class="sxs-lookup"><span data-stu-id="7d6d0-116">For more information, see [Sample OpenType Font Pack](sample-opentype-font-pack.md).</span></span>  
  
<span data-ttu-id="7d6d0-117">Ausführliche Informationen zum OpenType-Schriftformat finden Sie in der [OpenType-Spezifikation](/typography/opentype/spec/).</span><span class="sxs-lookup"><span data-stu-id="7d6d0-117">For details of the OpenType font format, see the [OpenType specification](/typography/opentype/spec/).</span></span>  
  
### <a name="advanced-typographic-extensions"></a><span data-ttu-id="7d6d0-118">Erweiterte typografische Funktionen</span><span class="sxs-lookup"><span data-stu-id="7d6d0-118">Advanced Typographic Extensions</span></span>  

 <span data-ttu-id="7d6d0-119">Die erweiterten typografischen Tabellen (OpenType-Layouttabellen) erweitern die Funktionalität von Schriftarten mit den Gliederungen von TrueType oder CFF.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-119">The Advanced Typographic tables (OpenType Layout tables) extend the functionality of fonts with either TrueType or CFF outlines.</span></span> <span data-ttu-id="7d6d0-120">OpenType-Layoutschriftarten enthalten zusätzliche Informationen, die die Funktionen der Schriftarten für die Unterstützung qualitativ hochwertiger internationaler Typografiefunktionen erweitern.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-120">OpenType Layout fonts contain additional information that extends the capabilities of the fonts to support high-quality international typography.</span></span> <span data-ttu-id="7d6d0-121">Die meisten OpenType-Schriftarten machen nur eine Teilmenge der verfügbaren OpenType-Features verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-121">Most OpenType fonts expose only a subset of the total OpenType features available.</span></span> <span data-ttu-id="7d6d0-122">OpenType-Schriftarten bieten die folgenden Funktionen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-122">OpenType fonts provide the following features.</span></span>  
  
- <span data-ttu-id="7d6d0-123">Umfangreiche Zuordnung zwischen Zeichen und Symbolen, die Ligaturen, positionelle Formen, alternative Stile und andere Schriftartersetzungen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-123">Rich mapping between characters and glyphs that support ligatures, positional forms, alternates, and other font substitutions.</span></span>  
  
- <span data-ttu-id="7d6d0-124">Unterstützung von zweidimensionaler Positionierung und Symbolanfügung.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-124">Support for two-dimensional positioning and glyph attachment.</span></span>  
  
- <span data-ttu-id="7d6d0-125">Explizite Skript- und Sprachinformationen, die in der Schriftart enthalten sind, damit Textverarbeitungsanwendungen ihr Verhalten entsprechend anpassen können.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-125">Explicit script and language information contained in font, so a text-processing application can adjust its behavior accordingly.</span></span>  
  
 <span data-ttu-id="7d6d0-126">Die OpenType-Layouttabellen werden im Abschnitt ["Schriftart Datei Tabellen"](https://www.microsoft.com/typography/otspec/otff.htm) der OpenType-Spezifikation ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-126">The OpenType Layout tables are described in more detail in the ["Font File Tables"](https://www.microsoft.com/typography/otspec/otff.htm) section of the OpenType specification.</span></span>  
  
 <span data-ttu-id="7d6d0-127">Im restlichen Teil dieser Übersicht wird die Breite und Flexibilität einiger der visuell interessanten OpenType-Funktionen eingeführt, die von den Eigenschaften des Objekts verfügbar gemacht werden <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-127">The remainder of this overview introduces the breadth and flexibility of some of the visually-interesting OpenType features that are exposed by the properties of the <xref:System.Windows.Documents.Typography> object.</span></span> <span data-ttu-id="7d6d0-128">Weitere Informationen über dieses Objekt finden Sie unter [Typografieklasse](#typography_class).</span><span class="sxs-lookup"><span data-stu-id="7d6d0-128">For more information on this object, see [Typography Class](#typography_class).</span></span>  
  
<a name="variants"></a>

## <a name="variants"></a><span data-ttu-id="7d6d0-129">Varianten</span><span class="sxs-lookup"><span data-stu-id="7d6d0-129">Variants</span></span>  

 <span data-ttu-id="7d6d0-130">Varianten werden verwendet, um verschiedene typographische Formate zu rendern, z.B. hoch- und tiefgestellte Zeichen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-130">Variants are used to render different typographic styles, such as superscripts and subscripts.</span></span>  
  
### <a name="superscripts-and-subscripts"></a><span data-ttu-id="7d6d0-131">Hoch- und tiefgestellte Zeichen</span><span class="sxs-lookup"><span data-stu-id="7d6d0-131">Superscripts and Subscripts</span></span>  

 <span data-ttu-id="7d6d0-132"><xref:System.Windows.Documents.Typography.Variants%2A>Mit der-Eigenschaft können Sie hoch gestellt und Indexwerte für eine OpenType-Schriftart festlegen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-132">The <xref:System.Windows.Documents.Typography.Variants%2A> property allows you to set superscript and subscript values for an OpenType font.</span></span>  
  
 <span data-ttu-id="7d6d0-133">Der folgende Text zeigt hochgestellte Zeichen für die Schriftart Palatino Linotype.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-133">The following text displays superscripts for the Palatino Linotype font.</span></span>  
  
 <span data-ttu-id="7d6d0-134">![Text mit hochgestellten OpenType-Zeichen](./media/opentype-font-features/opentype-superscripts.gif "Text mit hochgestellten OpenType-Zeichen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-134">![Text using OpenType superscripts](./media/opentype-font-features/opentype-superscripts.gif "Text using OpenType superscripts")</span></span>  
  
 <span data-ttu-id="7d6d0-135">Im folgenden Markup Beispiel wird gezeigt, wie Sie mithilfe der Eigenschaften des-Objekts hoch für die Schriftart Palatino Linotype definieren <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-135">The following markup example shows how to define superscripts for the Palatino Linotype font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#12](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#12)]  
  
 <span data-ttu-id="7d6d0-136">Der folgende Text zeigt tiefgestellte Zeichen für die Schriftart Palatino Linotype.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-136">The following text displays subscripts for the Palatino Linotype font.</span></span>  
  
 <span data-ttu-id="7d6d0-137">![Text mit tiefgestellten OpenType-Zeichen](./media/opentype-font-features/opentype-subscripts.gif "Text mit tiefgestellten OpenType-Zeichen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-137">![Text using OpenType subscripts](./media/opentype-font-features/opentype-subscripts.gif "Text using OpenType subscripts")</span></span>  
  
 <span data-ttu-id="7d6d0-138">Im folgenden Markup Beispiel wird gezeigt, wie Sie unter Verwendung der Eigenschaften des-Objekts unter Zeichenfolgen für die Schriftart Palatino Linotype definieren <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-138">The following markup example shows how to define subscripts for the Palatino Linotype font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#13](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#13)]  
  
### <a name="decorative-uses-of-superscripts-and-subscripts"></a><span data-ttu-id="7d6d0-139">Dekorative Verwendung von hoch- und tiefgestellten Zeichen</span><span class="sxs-lookup"><span data-stu-id="7d6d0-139">Decorative Uses of Superscripts and Subscripts</span></span>  

 <span data-ttu-id="7d6d0-140">Hoch- und tiefgestellte Zeichen können auch verwendet werden, um mit Groß- und Kleinbuchstaben aus einem Text dekorative Effekte zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-140">You can also use superscripts and subscripts to create decorative effects of mixed case text.</span></span> <span data-ttu-id="7d6d0-141">Der folgende Text zeigt hoch- und tiefgestellte Zeichen für die Schriftart Palatino Linotype.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-141">The following text displays superscript and subscript text for the Palatino Linotype font.</span></span> <span data-ttu-id="7d6d0-142">Beachten Sie, dass Großbuchstaben nicht beeinflusst werden.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-142">Note that the capitals are not affected.</span></span>  
  
 <span data-ttu-id="7d6d0-143">![Text mit hoch- und tiefgestellten Zeichen im OpenType-Format](./media/opentype-font-features/opentype-superscripts-subscripts.gif "Text mit hoch- und tiefgestellten OpenType-Zeichen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-143">![Text using OpenType superscripts and subscripts](./media/opentype-font-features/opentype-superscripts-subscripts.gif "Text using OpenType superscripts and subscripts")</span></span>  

 <span data-ttu-id="7d6d0-144">Im folgenden Markup Beispiel wird gezeigt, wie Sie mithilfe der Eigenschaften des-Objekts hoch und Index Zeichenfolgen für eine Schriftart definieren <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-144">The following markup example shows how to define superscripts and subscripts for a font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#14](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#14)]  
  
<a name="capitals"></a>

## <a name="capitals"></a><span data-ttu-id="7d6d0-145">Großbuchstaben</span><span class="sxs-lookup"><span data-stu-id="7d6d0-145">Capitals</span></span>  

 <span data-ttu-id="7d6d0-146">Großbuchstaben sind ein Satz typografischer Formen, bei dem Text mit Symbolen gerendert wird, die als Großbuchstaben formatiert sind.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-146">Capitals are a set of typographical forms that render text in capital-styled glyphs.</span></span> <span data-ttu-id="7d6d0-147">Wenn Text ausschließlich in Großbuchstaben gerendert wird, kann der Abstand zwischen den Buchstaben als zu gering, die Breite der Buchstaben als zu groß und die Proportionen der Buchstaben als zu unausgewogen erscheinen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-147">Typically, when text is rendered as all capitals, the spacing between letters can appear too tight, and the weight and proportion of the letters too heavy.</span></span> <span data-ttu-id="7d6d0-148">OpenType unterstützt eine Reihe von Formatierungs Formaten für Großbuchstaben, einschließlich Small Capitals, Petite Capitals, titult und Capital-Abstände.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-148">OpenType supports a number of styling formats for capitals, including small capitals, petite capitals, titling, and capital spacing.</span></span> <span data-ttu-id="7d6d0-149">Mit diesen Formatierungen kann die Darstellung von Großbuchstaben gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-149">These styling formats allow you to control the appearance of capitals.</span></span>  
  
 <span data-ttu-id="7d6d0-150">Der folgende Text zeigt zuerst die Standardgroßbuchstaben, gefolgt von den Buchstaben in den Formaten „SmallCaps“ und „AllSmallCaps“ für die Schriftart Pescadero.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-150">The following text displays standard capital letters for the Pescadero font, followed by the letters styled as "SmallCaps" and "AllSmallCaps".</span></span> <span data-ttu-id="7d6d0-151">Für alle drei Wörter wird der gleiche Schriftgrad verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-151">In this case, the same font size is used for all three words.</span></span>  
  
 <span data-ttu-id="7d6d0-152">![Text mit OpenType-Kapitälchen](./media/opentype-font-features/opentype-capitals.gif "Text mit OpenType-Kapitälchen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-152">![Text using OpenType capitals](./media/opentype-font-features/opentype-capitals.gif "Text using OpenType capitals")</span></span>  
  
 <span data-ttu-id="7d6d0-153">Im folgenden Markup Beispiel wird gezeigt, wie Sie mithilfe der Eigenschaften des-Objekts die Großbuchstaben für die Schriftart Pescadero definieren <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-153">The following markup example shows how to define capitals for the Pescadero font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span> <span data-ttu-id="7d6d0-154">Wenn das „SmallCaps“-Format verwendet wird, werden führende Großbuchstaben ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-154">When the "SmallCaps" format is used, any leading capital letter is ignored.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#9](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#9)]  
  
### <a name="titling-capitals"></a><span data-ttu-id="7d6d0-155">Großbuchstaben für Titel</span><span class="sxs-lookup"><span data-stu-id="7d6d0-155">Titling Capitals</span></span>  

 <span data-ttu-id="7d6d0-156">Großbuchstaben für Titel sind weniger stark ausgebildet und proportioniert und sollen im Vergleich zu normalen Großbuchstaben eine elegantere Darstellungsweise sicherstellen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-156">Titling capitals are lighter in weight and proportion and designed to give a more elegant look than normal capitals.</span></span> <span data-ttu-id="7d6d0-157">Großbuchstaben für Titel werden üblicherweise mit größeren Schriftgraden in Überschriften verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-157">Titling capitals are typically used in larger font sizes as headings.</span></span> <span data-ttu-id="7d6d0-158">Der folgende Text zeigt normale Großbuchstaben und Großbuchstaben für Titel für die Schriftart Pescadero.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-158">The following text displays normal and titling capitals for the Pescadero font.</span></span> <span data-ttu-id="7d6d0-159">Beachten Sie die geringeren Strichstärken des Texts in der zweiten Zeile.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-159">Notice the narrower stem widths of the text on the second line.</span></span>  
  
 <span data-ttu-id="7d6d0-160">![Text mit OpenType-Initialen](./media/opentype-font-features/opentype-titling-capitals.gif "Text mit OpenType-Initialen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-160">![Text using OpenType titling capitals](./media/opentype-font-features/opentype-titling-capitals.gif "Text using OpenType titling capitals")</span></span>  
  
 <span data-ttu-id="7d6d0-161">Im folgenden Markup Beispiel wird gezeigt, wie mit den Eigenschaften des-Objekts titlinger-Hauptschriften für die Schriftart Pescadero definiert werden <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-161">The following markup example shows how to define titling capitals for the Pescadero font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#OpenTypeFontSnippet17](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#opentypefontsnippet17)]  
  
### <a name="capital-spacing"></a><span data-ttu-id="7d6d0-162">Großbuchstabenabstand</span><span class="sxs-lookup"><span data-stu-id="7d6d0-162">Capital Spacing</span></span>  

 <span data-ttu-id="7d6d0-163">Der Großbuchstabenabstand ist ein Feature, mit dem Sie in einem Textabschnitt, der ausschließlich aus Großbuchstaben besteht, die Laufweite vergrößern können.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-163">Capital spacing is a feature that allows you to provide more spacing when using all capitals in text.</span></span> <span data-ttu-id="7d6d0-164">Großbuchstaben werden i. d. R. so entworfen, dass sie mit Kleinbuchstaben harmonieren.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-164">Capital letters are typically designed to blend with lowercase letters.</span></span> <span data-ttu-id="7d6d0-165">Ein Abstand, der zwischen einem Großbuchstaben und einem Kleinbuchstaben ästhetisch wirkt, kann zwischen Großbuchstaben zu gering erscheinen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-165">Spacing that appears attractive between and a capital letter and a lowercase letter may look too tight when all capital letters are used.</span></span> <span data-ttu-id="7d6d0-166">Im folgende Text werden normale Großbuchstaben und Großbuchstaben für Titel für die Schriftart Pescadero gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-166">The following text displays normal and capital spacing for the Pescadero font.</span></span>  
  
 <span data-ttu-id="7d6d0-167">![Text mit OpenType-Kapitälchenabstand](./media/opentype-font-features/opentype-capital-spacing.gif "Text mit OpenType-Kapitälchenabstand")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-167">![Text using OpenType capital spacing](./media/opentype-font-features/opentype-capital-spacing.gif "Text using OpenType capital spacing")</span></span>  

 <span data-ttu-id="7d6d0-168">Im folgenden Markup Beispiel wird gezeigt, wie Sie mithilfe der Eigenschaften des-Objekts den Großbuchstaben für die Schriftart Pescadero definieren <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-168">The following markup example shows how to define capital spacing for the Pescadero font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#OpenTypeFontSnippet18](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#opentypefontsnippet18)]  
  
<a name="ligatures"></a>

## <a name="ligatures"></a><span data-ttu-id="7d6d0-169">Ligaturen</span><span class="sxs-lookup"><span data-stu-id="7d6d0-169">Ligatures</span></span>  

 <span data-ttu-id="7d6d0-170">Ligaturen sind zwei oder mehr Symbole, die zu einem einzigen Symbol zusammengefügt werden, um einen besser lesbaren oder attraktiveren Text zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-170">Ligatures are two or more glyphs that are formed into a single glyph in order to create more readable or attractive text.</span></span> <span data-ttu-id="7d6d0-171">OpenType-Schriftarten unterstützen vier Arten von Ligaturen:</span><span class="sxs-lookup"><span data-stu-id="7d6d0-171">OpenType fonts support four types of ligatures:</span></span>  
  
- <span data-ttu-id="7d6d0-172">**Standardligaturen**.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-172">**Standard ligatures**.</span></span> <span data-ttu-id="7d6d0-173">Zur Verbesserung der Lesbarkeit.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-173">Designed to enhance readability.</span></span> <span data-ttu-id="7d6d0-174">Zu den Standardligaturen gehören „fi“, „fl“ und „ff“.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-174">Standard ligatures include "fi", "fl", and "ff".</span></span>  
  
- <span data-ttu-id="7d6d0-175">**Kontextbedingte Ligaturen**.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-175">**Contextual ligatures**.</span></span> <span data-ttu-id="7d6d0-176">Mit Kontextligaturen soll die Lesbarkeit verbessert werden, indem die Buchstaben einer Ligatur optimal verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-176">Designed to enhance readability by providing better joining behavior between the characters that make up the ligature.</span></span>  
  
- <span data-ttu-id="7d6d0-177">**Bedingte Ligaturen**.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-177">**Discretionary ligatures**.</span></span> <span data-ttu-id="7d6d0-178">Bedingte Ligaturen sollen verzierend wirken, wobei die Lesbarkeit eine untergeordnete Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-178">Designed to be ornamental, and not specifically designed for readability.</span></span>  
  
- <span data-ttu-id="7d6d0-179">**Historische Ligaturen**.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-179">**Historical ligatures**.</span></span> <span data-ttu-id="7d6d0-180">Historische Ligaturen sollen eine historische Wirkung erzielen, wobei die Lesbarkeit eine untergeordnete Rolle spielt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-180">Designed to be historical, and not specifically designed for readability.</span></span>  
  
 <span data-ttu-id="7d6d0-181">Im folgenden Text werden Symbole für Standardligaturen in der Schriftart Pericles gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-181">The following text displays standard ligature glyphs for the Pericles font.</span></span>  
  
 <span data-ttu-id="7d6d0-182">![Text mit OpenType-Standardligaturen](./media/opentype-font-features/opentype-standard-ligatures.gif "Text mit OpenType-Standardligaturen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-182">![Text using OpenType standard ligatures](./media/opentype-font-features/opentype-standard-ligatures.gif "Text using OpenType standard ligatures")</span></span>  
  
 <span data-ttu-id="7d6d0-183">Im folgenden Markup Beispiel wird gezeigt, wie standardmäßige Ligaturen-Symbole für die Schriftart Pericles mithilfe der Eigenschaften des-Objekts definiert werden <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-183">The following markup example shows how to define standard ligature glyphs for the Pericles font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#4](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#4)]  
  
 <span data-ttu-id="7d6d0-184">Im folgenden Text werden Symbole für bedingte Ligaturen in der Schriftart Pericles gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-184">The following text displays discretionary ligature glyphs for the Pericles font.</span></span>  
  
 <span data-ttu-id="7d6d0-185">![Text mit bedingten OpenType-Ligaturen](./media/opentype-font-features/opentype-discretionary-ligatures.gif "Text mit bedingten OpenType-Ligaturen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-185">![Text using OpenType discretionary ligatures](./media/opentype-font-features/opentype-discretionary-ligatures.gif "Text using OpenType discretionary ligatures")</span></span>  
  
 <span data-ttu-id="7d6d0-186">Im folgenden Markup Beispiel wird gezeigt, wie Sie mithilfe der Eigenschaften des-Objekts freigegebene Ligaturen-Symbole für die Schriftart Pericles definieren <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-186">The following markup example shows how to define discretionary ligature glyphs for the Pericles font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#5](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#5)]  
  
 <span data-ttu-id="7d6d0-187">Standardmäßig aktivieren OpenType-Schriftarten in [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Standard Ligaturen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-187">By default, OpenType fonts in [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] enable standard ligatures.</span></span> <span data-ttu-id="7d6d0-188">Wenn Sie beispielsweise die Schriftart Palatino Linotype verwenden, werden die Standardligaturen „fi“, „ff“ und „fl“ als kombiniertes Zeichensymbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-188">For example, if you use the Palatino Linotype font, the standard ligatures "fi", "ff", and "fl" appear as a combined character glyph.</span></span> <span data-ttu-id="7d6d0-189">Dabei berühren die beiden Zeichen einer Standardligatur einander.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-189">Notice that the pair of characters for each standard ligature touch each other.</span></span>  
  
 <span data-ttu-id="7d6d0-190">![Text mit OpenType-Standard Ligaturen mit Palatino Linotype](./media/opentype-font-features/opentype-standard-ligatures-palatino.gif "Text mit OpenType-Standard Ligaturen mit Palatino Linotype")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-190">![Text using OpenType standard ligatures with Palatino Linotype](./media/opentype-font-features/opentype-standard-ligatures-palatino.gif "Text using OpenType standard ligatures with Palatino Linotype")</span></span>

 <span data-ttu-id="7d6d0-191">Allerdings können Sie die Features für Standardligaturen auch deaktivieren, sodass z.B. die Standardligatur „ff“ nicht als kombiniertes Zeichensymbol, sondern als zwei einzelne Symbole angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-191">However, you can disable standard ligature features so that a standard ligature such as "ff" displays as two separate glyphs, rather than as a combined character glyph.</span></span>  
  
 <span data-ttu-id="7d6d0-192">![Text mit deaktivierten OpenType-Standardligaturen](./media/opentype-font-features/disabled-opentype-standard-ligatures.gif "Text mit deaktivierten OpenType-Standardligaturen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-192">![Text using disabled OpenType standard ligatures](./media/opentype-font-features/disabled-opentype-standard-ligatures.gif "Text using disabled OpenType standard ligatures")</span></span>  

 <span data-ttu-id="7d6d0-193">Im folgenden Markup Beispiel wird gezeigt, wie Standard Ligaturen-Symbole für die Schriftart Palatino Linotype mithilfe der Eigenschaften des- <xref:System.Windows.Documents.Typography> Objekts deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-193">The following markup example shows how to disable standard ligature glyphs for the Palatino Linotype font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#6](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#6)]  
  
<a name="swashes"></a>

## <a name="swashes"></a><span data-ttu-id="7d6d0-194">Schwünge</span><span class="sxs-lookup"><span data-stu-id="7d6d0-194">Swashes</span></span>  

 <span data-ttu-id="7d6d0-195">Schwungschrift besteht aus dekorativen Symbolen, deren ausgefeilte Verzierung häufig mit Kalligraphie assoziiert wird.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-195">Swashes are decorative glyphs that use elaborate ornamentation often associated with calligraphy.</span></span> <span data-ttu-id="7d6d0-196">Im folgenden Text werden Standard- und Schwungsymbole für die Schriftart Pescadero gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-196">The following text displays standard and swash glyphs for the Pescadero font.</span></span>  
  
 <span data-ttu-id="7d6d0-197">![Text mit OpenType-Standard- und Ziersymbolen](./media/opentype-font-features/opentype-standard-swash-glyphs.gif "Text mit OpenType-Standard- und Ziersymbolen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-197">![Text using OpenType standard and swash glyphs](./media/opentype-font-features/opentype-standard-swash-glyphs.gif "Text using OpenType standard and swash glyphs")</span></span>  

 <span data-ttu-id="7d6d0-198">Schwungschrift wird häufig als dekoratives Element in kurzen Sätzen verwendet, z.B. in Veranstaltungsankündigungen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-198">Swashes are often used as decorative elements in short phrases such as event announcements.</span></span> <span data-ttu-id="7d6d0-199">Im folgenden Text werden die Großbuchstaben eines Veranstaltungstitels mit Schwungschrift hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-199">The following text uses swashes to emphasize the capital letters of the name of the event.</span></span>  
  
 <span data-ttu-id="7d6d0-200">![Text mit OpenType-Zierbuchstaben](./media/opentype-font-features/opentype-swashes.gif "Text mit OpenType-Zierbuchstaben")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-200">![Text using OpenType swashes](./media/opentype-font-features/opentype-swashes.gif "Text using OpenType swashes")</span></span>  
  
 <span data-ttu-id="7d6d0-201">Im folgenden Markup Beispiel wird gezeigt, wie Sie mithilfe der Eigenschaften des-Objekts Schwung Schrift für eine Schriftart definieren <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-201">The following markup example shows how to define swashes for a font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#7](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#7)]  
  
### <a name="contextual-swashes"></a><span data-ttu-id="7d6d0-202">Kontextbedingte Schwungschrift</span><span class="sxs-lookup"><span data-stu-id="7d6d0-202">Contextual Swashes</span></span>  

 <span data-ttu-id="7d6d0-203">Bestimmte Kombinationen von Symbolen in Schwungschrift können unästhetisch wirken, z.B. sich überschneidende Unterlängen bei aufeinander folgenden Buchstaben.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-203">Certain combinations of swash glyphs can cause an unattractive appearance, such as overlapping descenders on adjacent letters.</span></span> <span data-ttu-id="7d6d0-204">Mit kontextbedingter Schwungschrift können Sie Varianten eines Symbols in Schwungschrift verwenden, deren Darstellung dann ästhetischer wirkt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-204">Using a contextual swash allows you to use a substitute swash glyph that produces a better appearance.</span></span> <span data-ttu-id="7d6d0-205">Im folgenden Text wird das gleiche Wort vor und nach dem Übernehmen einer kontextbedingten Variante für die Schwungschrift gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-205">The following text shows the same word before and after a contextual swash is applied.</span></span>  
  
 <span data-ttu-id="7d6d0-206">![Text mit kontextbezogenen OpenType-Zierbuchstaben](./media/opentype-font-features/opentype-contextual-swashes.gif "Text mit kontextbezogenen OpenType-Zierbuchstaben")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-206">![Text using OpenType contextual swashes](./media/opentype-font-features/opentype-contextual-swashes.gif "Text using OpenType contextual swashes")</span></span>  
  
 <span data-ttu-id="7d6d0-207">Im folgenden Markup Beispiel wird gezeigt, wie Sie mithilfe der Eigenschaften des-Objekts eine kontextabhängige Swash-Eigenschaft für die Schriftart Pescadero definieren <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-207">The following markup example shows how to define a contextual swash for the Pescadero font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#OpenTypeFontSnippet16](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#opentypefontsnippet16)]  
  
<a name="alternates"></a>

## <a name="alternates"></a><span data-ttu-id="7d6d0-208">Alternative Stile</span><span class="sxs-lookup"><span data-stu-id="7d6d0-208">Alternates</span></span>  

 <span data-ttu-id="7d6d0-209">Alternative Stilvarianten sind Symbole, die ein Standardsymbol ersetzen können.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-209">Alternates are glyphs that can be substituted for a standard glyph.</span></span> <span data-ttu-id="7d6d0-210">OpenType-Schriftarten, wie z. b. die in den folgenden Beispielen verwendete Pericles-Schriftart, können alternative Symbole enthalten, die Sie verwenden können, um einen anderen Text Text zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-210">OpenType fonts, such as the Pericles font used in the following examples, can contain alternate glyphs that you can use to create different appearances for text.</span></span> <span data-ttu-id="7d6d0-211">Im folgenden Text werden die Standardsymbole der Schriftart Pericles dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-211">The following text displays standard glyphs for the Pericles font.</span></span>  
  
 <span data-ttu-id="7d6d0-212">![Text mit OpenType-Standardsymbolen](./media/opentype-font-features/opentype-standard-glyphs.gif "Text mit OpenType-Standardsymbolen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-212">![Text using OpenType standard glyphs](./media/opentype-font-features/opentype-standard-glyphs.gif "Text using OpenType standard glyphs")</span></span>  

 <span data-ttu-id="7d6d0-213">Die Schriftart "Pericles OpenType" enthält zusätzliche Symbole, die eine stilistische Alternative zum Standardsatz von Symbolen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-213">The Pericles OpenType font contains additional glyphs that provide stylistic alternates to the standard set of glyphs.</span></span> <span data-ttu-id="7d6d0-214">Im folgenden Text werden Symbole im alternativen Stil gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-214">The following text displays stylistic alternate glyphs.</span></span>  
  
 <span data-ttu-id="7d6d0-215">![Text mit alternativen OpenType-Stilsymbolen](./media/opentype-font-features/opentype-stylistic-alternate-glyphs.gif "Text mit alternativen OpenType-Stilsymbolen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-215">![Text using OpenType stylistic alternate glyphs](./media/opentype-font-features/opentype-stylistic-alternate-glyphs.gif "Text using OpenType stylistic alternate glyphs")</span></span>  
  
 <span data-ttu-id="7d6d0-216">Im folgenden Markup Beispiel wird gezeigt, wie Sie mit den Eigenschaften des-Objekts für die Schriftart Pericles eine Alternative Symbole definieren <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-216">The following markup example shows how to define stylistic alternate glyphs for the Pericles font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#2](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#2)]  
  
 <span data-ttu-id="7d6d0-217">Im folgenden Text werden verschiedene Symbole im alternativen Stil in der Schriftart Pericles gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-217">The following text displays several other stylistic alternate glyphs for the Pericles font.</span></span>  
  
 <span data-ttu-id="7d6d0-218">![Text mit alternativen OpenType-Symbolen für die Schriftart "Pericles"](./media/opentype-font-features/opentype-stylistic-alternate-glyphs-pericles.gif "Text mit alternativen OpenType-Symbolen für die Schriftart "Pericles"")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-218">![Text using OpenType stylistic alternate glyphs  for the Pericles font](./media/opentype-font-features/opentype-stylistic-alternate-glyphs-pericles.gif "Text using OpenType stylistic alternate glyphs  for the Pericles font")</span></span>

 <span data-ttu-id="7d6d0-219">Im folgenden Markupbeispiel wird veranschaulicht, wie diese zusätzlichen Stilvarianten von Symbolen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-219">The following markup example shows how to define these other stylistic alternate glyphs.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#3](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#3)]  
  
### <a name="random-contextual-alternates"></a><span data-ttu-id="7d6d0-220">Zufällige kontextbedingte Varianten</span><span class="sxs-lookup"><span data-stu-id="7d6d0-220">Random Contextual Alternates</span></span>  

 <span data-ttu-id="7d6d0-221">Bei zufälligen kontextbedingten Varianten werden mehrere Ersatzsymbole für ein einzelnes Zeichen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-221">Random contextual alternates provide multiple substitute glyphs for a single character.</span></span> <span data-ttu-id="7d6d0-222">Wenn dieses Feature für handschriftähnliche Schriftarten implementiert ist, kann Handschrift mit einem Satz zufällig ausgewählter Symbole simuliert werden, die leicht unterschiedlich dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-222">When implemented with script-type fonts, this feature can simulate handwriting by using of a set of randomly chosen glyphs with slight differences in appearance.</span></span> <span data-ttu-id="7d6d0-223">Im folgenden Text werden zufällige kontextbedingte Varianten für die Schriftart Lindsey verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-223">The following text uses random contextual alternates for the Lindsey font.</span></span> <span data-ttu-id="7d6d0-224">Dabei wird der Buchstabe „a“ in der Darstellung leicht abgewandelt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-224">Notice that the letter "a" varies slightly in appearance</span></span>  
  
 <span data-ttu-id="7d6d0-225">![Text mit willkürlichen kontextbedingten OpenType-Varianten](./media/opentype-font-features/opentype-random-contextual-alternates.gif "Text mit willkürlichen kontextbedingten OpenType-Varianten")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-225">![Text using OpenType random contextual alternates](./media/opentype-font-features/opentype-random-contextual-alternates.gif "Text using OpenType random contextual alternates")</span></span>  
  
 <span data-ttu-id="7d6d0-226">Im folgenden Markup Beispiel wird gezeigt, wie zufällige kontextabhängige Alternativen für die Schriftart Lindsey mithilfe der Eigenschaften des- <xref:System.Windows.Documents.Typography> Objekts definiert werden.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-226">The following markup example shows how to define random contextual alternates for the Lindsey font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#OpenTypeFontSnippet20](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/Window1.xaml#opentypefontsnippet20)]  
  
### <a name="historical-forms"></a><span data-ttu-id="7d6d0-227">Historische Formen</span><span class="sxs-lookup"><span data-stu-id="7d6d0-227">Historical Forms</span></span>  

 <span data-ttu-id="7d6d0-228">Unter historischen Formen werden der Vergangenheit verbreitete typografische Konventionen verstanden.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-228">Historical forms are typographic conventions that were common in the past.</span></span> <span data-ttu-id="7d6d0-229">Im folgenden Text wird „Boston, Massachusetts“ unter Verwendung einer historischen Form der Symbole in der Schriftart Palatino Linotype gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-229">The following text displays the phrase, "Boston, Massachusetts", using an historical form of glyphs for the Palatino Linotype font.</span></span>  
  
 <span data-ttu-id="7d6d0-230">![Text mit OpenType-Mediävalen](./media/opentype-font-features/opentype-historical-forms.gif "Text mit OpenType-Mediävalen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-230">![Text using OpenType historical forms](./media/opentype-font-features/opentype-historical-forms.gif "Text using OpenType historical forms")</span></span>  

 <span data-ttu-id="7d6d0-231">Im folgenden Markup Beispiel wird gezeigt, wie Sie mithilfe der Eigenschaften des-Objekts historische Formen für die Schriftart Palatino Linotype definieren <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-231">The following markup example shows how to define historical forms for the Palatino Linotype font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#8](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#8)]  
  
<a name="numerical_styles"></a>

## <a name="numerical-styles"></a><span data-ttu-id="7d6d0-232">Numerische Formate</span><span class="sxs-lookup"><span data-stu-id="7d6d0-232">Numerical Styles</span></span>  

 <span data-ttu-id="7d6d0-233">OpenType-Schriftarten unterstützen eine große Anzahl von Features, die mit numerischen Werten im Text verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-233">OpenType fonts support a large number of features that can be used with numerical values in text.</span></span>  
  
### <a name="fractions"></a><span data-ttu-id="7d6d0-234">Brüche</span><span class="sxs-lookup"><span data-stu-id="7d6d0-234">Fractions</span></span>  

 <span data-ttu-id="7d6d0-235">OpenType-Schriftarten unterstützen Stile für Bruchteile, einschließlich Schrägstrich und gestapelter.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-235">OpenType fonts support styles for fractions, including slashed and stacked.</span></span>  
  
 <span data-ttu-id="7d6d0-236">Im folgenden Text werden Bruchformate für die Schriftart Palatino Linotype gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-236">The following text displays fraction styles for the Palatino Linotype font.</span></span>  
  
 <span data-ttu-id="7d6d0-237">![Text mit OpenType-Brüchen mit schrägem oder waagerechtem Bruchstrich](./media/opentype-font-features/opentype-slashed-stacked-fractions.gif "Text mit OpenType-Brüchen mit schrägem oder waagerechtem Bruchstrich")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-237">![Text using OpenType slashed and stacked fractions](./media/opentype-font-features/opentype-slashed-stacked-fractions.gif "Text using OpenType slashed and stacked fractions")</span></span>  

 <span data-ttu-id="7d6d0-238">Im folgenden Markup Beispiel wird gezeigt, wie Sie mithilfe der Eigenschaften des-Objekts bruchstile für die Schriftart Palatino Linotype definieren <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-238">The following markup example shows how to define fraction styles for the Palatino Linotype font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#10](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#10)]  
  
### <a name="old-style-numerals"></a><span data-ttu-id="7d6d0-239">Mediävalziffern</span><span class="sxs-lookup"><span data-stu-id="7d6d0-239">Old Style Numerals</span></span>  

 <span data-ttu-id="7d6d0-240">OpenType-Schriftarten unterstützen ein altes Format für das Zahlenformat.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-240">OpenType fonts support an old style numeral format.</span></span> <span data-ttu-id="7d6d0-241">Dieses Format dient der Anzeige von Ziffern in nicht mehr üblichen Stilen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-241">This format is useful for displaying numerals in styles that are no longer standard.</span></span> <span data-ttu-id="7d6d0-242">Im folgenden Text wird ein Datum aus dem 18. Jahrhundert im Standardformat und mit Mediävalziffern in der Schriftart Palatino Linotype gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-242">The following text displays an 18th century date in standard and old style numeral formats for the Palatino Linotype font.</span></span>  
  
 <span data-ttu-id="7d6d0-243">![Text mit OpenType-Mediävalziffern](./media/opentype-font-features/opentype-old-style-numerals.gif "Text mit OpenType-Mediävalziffern")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-243">![Text using OpenType old style numerals](./media/opentype-font-features/opentype-old-style-numerals.gif "Text using OpenType old style numerals")</span></span>  

 <span data-ttu-id="7d6d0-244">Im folgenden Text werden in der Schriftart Palatino Linotype zuerst Standardziffern und dann Mediävalziffern gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-244">The following text displays standard numerals for the Palatino Linotype font, followed by old style numerals.</span></span>  
  
 <span data-ttu-id="7d6d0-245">![Text mit OpenType-Mediävalziffernsätzen](./media/opentype-font-features/opentype-old-style-numeral-sets.gif "Text mit OpenType-Mediävalziffernsätzen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-245">![Text using OpenType old style numeral sets](./media/opentype-font-features/opentype-old-style-numeral-sets.gif "Text using OpenType old style numeral sets")</span></span>  
  
 <span data-ttu-id="7d6d0-246">Im folgenden Markup Beispiel wird gezeigt, wie Sie mithilfe der Eigenschaften des-Objekts alte Stil Zahlen für die Schriftart Palatino Linotype definieren <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-246">The following markup example shows how to define old style numerals for the Palatino Linotype font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#11](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#11)]  
  
### <a name="proportional-and-tabular-figures"></a><span data-ttu-id="7d6d0-247">Proportionale Darstellung und Tabellendarstellung</span><span class="sxs-lookup"><span data-stu-id="7d6d0-247">Proportional and Tabular Figures</span></span>  

 <span data-ttu-id="7d6d0-248">OpenType-Schriftarten unterstützen eine proportionale und tabellarische Abbildung, um die Ausrichtung von breiten bei der Verwendung von Zahlen zu steuern.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-248">OpenType fonts support a proportional and tabular figure feature to control the alignment of widths when using numerals.</span></span> <span data-ttu-id="7d6d0-249">In der proportionalen Darstellung verfügt jede Ziffer über eine eigene Breite: die „1“ ist schmaler als die „5“.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-249">Proportional figures treat each numeral as having a different width—"1" is narrower than "5".</span></span> <span data-ttu-id="7d6d0-250">In der Tabellendarstellung werden alle Ziffern mit der gleichen Breite dargestellt und vertikal ausgerichtet. Dies verbessert die Lesbarkeit z.B. bei Finanzinformationen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-250">Tabular figures are treated as equal-width numerals so that they align vertically, which increases the readability of financial type information.</span></span>  
  
 <span data-ttu-id="7d6d0-251">Im folgenden Text werden in der ersten Spalte zwei proportionale Zahlen in der Schriftart Miramonte proportional dargestellt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-251">The following text displays two proportional figures in the first column using the Miramonte font.</span></span> <span data-ttu-id="7d6d0-252">Die Ziffern „5“ und „1“ unterscheiden sich in der Breite.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-252">Note the difference in width between the numerals "5" and "1".</span></span> <span data-ttu-id="7d6d0-253">In der zweiten Spalte wurde die Breite der gleichen Zahlen mit dem Feature für die Tabellendarstellung angepasst.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-253">The second column shows the same two numeric values with the widths adjusted by using the tabular figure feature.</span></span>  
  
 <span data-ttu-id="7d6d0-254">![Text mit proportionaler und Tabellendarstellung im OpenType-Format](./media/opentype-font-features/opentype-proportional-tabular-figures.gif "Text mit proportionaler und Tabellendarstellung im OpenType-Format")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-254">![Text using OpenType proportional & tabular figures](./media/opentype-font-features/opentype-proportional-tabular-figures.gif "Text using OpenType proportional and tabular figures")</span></span>  

 <span data-ttu-id="7d6d0-255">Im folgenden Markup Beispiel wird gezeigt, wie proportionale und tabellarische Abbildungen für die Miramonte-Schriftart mithilfe der Eigenschaften des-Objekts definiert werden <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-255">The following markup example shows how to define proportional and tabular figures for the Miramonte font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#OpenTypeFontSnippet19](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/Window1.xaml#opentypefontsnippet19)]  
  
### <a name="slashed-zero"></a><span data-ttu-id="7d6d0-256">Null mit Schrägstrich</span><span class="sxs-lookup"><span data-stu-id="7d6d0-256">Slashed Zero</span></span>  

 <span data-ttu-id="7d6d0-257">OpenType-Schriftarten unterstützen ein abgekürzte 0-Ziffern Format, um den Unterschied zwischen dem Buchstaben "O" und der Ziffer "0" hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-257">OpenType fonts support a slashed zero numeral format to emphasize the difference between the letter "O" and the numeral "0".</span></span> <span data-ttu-id="7d6d0-258">Die Ziffer 0 (null) mit Schrägstrich wird häufig für Kennungen in Finanz- und Geschäftsinformationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-258">The slashed zero numeral is often used for identifiers in financial and business information.</span></span>  
  
 <span data-ttu-id="7d6d0-259">Im folgenden Text wird ein Beispiel mit einer Bestellnummer in der Schriftart Miramonte gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-259">The following text displays a sample order identifier using the Miramonte font.</span></span> <span data-ttu-id="7d6d0-260">In der ersten Zeile werden Standardziffern verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-260">The first line uses standard numerals.</span></span> <span data-ttu-id="7d6d0-261">In der zweiten wird die Ziffer 0 (null) mit Schrägstrich verwendet, um die Ziffer 0 (null) optisch besser vom Großbuchstaben „O“ zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-261">The second line used slashed zero numerals to provide better contrast with the uppercase "O" letter.</span></span>  
  
 <span data-ttu-id="7d6d0-262">![Text mit OpenType-Ziffern mit null mit Schrägstrich](./media/opentype-font-features/opentype-slashed-zero-numerals.gif "Text mit OpenType-Ziffern mit Null mit Schrägstrich")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-262">![Text using OpenType slashed zero numerals](./media/opentype-font-features/opentype-slashed-zero-numerals.gif "Text using OpenType slashed zero numerals")</span></span>  

 <span data-ttu-id="7d6d0-263">Im folgenden Markup Beispiel wird gezeigt, wie mit den Eigenschaften des-Objekts die NULL-Ziffern mit Schrägstrich für die Schriftart Miramonte definiert werden <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-263">The following markup example shows how to define slashed zero numerals for the Miramonte font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#OpenTypeFontSnippet15](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#opentypefontsnippet15)]  
  
<a name="typography_class"></a>

## <a name="typography-class"></a><span data-ttu-id="7d6d0-264">Typografieklasse</span><span class="sxs-lookup"><span data-stu-id="7d6d0-264">Typography Class</span></span>  

 <span data-ttu-id="7d6d0-265">Das- <xref:System.Windows.Documents.Typography> Objekt macht den Satz von Funktionen verfügbar, den eine OpenType-Schriftart unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-265">The <xref:System.Windows.Documents.Typography> object exposes the set of features that an OpenType font supports.</span></span> <span data-ttu-id="7d6d0-266">Durch Festlegen der Eigenschaften von <xref:System.Windows.Documents.Typography> in Markup können Sie problemlos Dokumente erstellen, die OpenType-Funktionen nutzen.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-266">By setting the properties of <xref:System.Windows.Documents.Typography> in markup, you can easily author documents that take advantage of OpenType features.</span></span>  
  
 <span data-ttu-id="7d6d0-267">Der folgende Text zeigt zuerst die Standardgroßbuchstaben, gefolgt von den Buchstaben in den Formaten „SmallCaps“ und „AllSmallCaps“ für die Schriftart Pescadero.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-267">The following text displays standard capital letters for the Pescadero font, followed by the letters styled as "SmallCaps" and "AllSmallCaps".</span></span> <span data-ttu-id="7d6d0-268">Für alle drei Wörter wird der gleiche Schriftgrad verwendet.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-268">In this case, the same font size is used for all three words.</span></span>  
  
 <span data-ttu-id="7d6d0-269">![Text mit OpenType-Kapitälchen](./media/opentype-font-features/opentype-capitals.gif "Text mit OpenType-Kapitälchen")</span><span class="sxs-lookup"><span data-stu-id="7d6d0-269">![Text using OpenType capitals](./media/opentype-font-features/opentype-capitals.gif "Text using OpenType capitals")</span></span>  

 <span data-ttu-id="7d6d0-270">Im folgenden Markup Beispiel wird gezeigt, wie Sie mithilfe der Eigenschaften des-Objekts die Großbuchstaben für die Schriftart Pescadero definieren <xref:System.Windows.Documents.Typography> .</span><span class="sxs-lookup"><span data-stu-id="7d6d0-270">The following markup example shows how to define capitals for the Pescadero font, using properties of the <xref:System.Windows.Documents.Typography> object.</span></span> <span data-ttu-id="7d6d0-271">Wenn das „SmallCaps“-Format verwendet wird, werden führende Großbuchstaben ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-271">When the "SmallCaps" format is used, any leading capital letter is ignored.</span></span>  
  
 [!code-xaml[OpenTypeFontSamples#9](~/samples/snippets/csharp/VS_Snippets_Wpf/OpenTypeFontSamples/CS/PageOne.xaml#9)]  
  
 <span data-ttu-id="7d6d0-272">Im folgenden Codebeispiel wird die gleiche Aufgabe wie im vorherigen Markupbeispiel ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-272">The following code example accomplishes the same task as the previous markup example.</span></span>  
  
 [!code-csharp[TypographyCodeSnippets#TypographyCodeSnippet1](~/samples/snippets/csharp/VS_Snippets_Wpf/TypographyCodeSnippets/CSharp/Page1.xaml.cs#typographycodesnippet1)]
 [!code-vb[TypographyCodeSnippets#TypographyCodeSnippet1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TypographyCodeSnippets/visualbasic/page1.xaml.vb#typographycodesnippet1)]  
  
### <a name="typography-class-properties"></a><span data-ttu-id="7d6d0-273">Typografieklasseneigenschaften</span><span class="sxs-lookup"><span data-stu-id="7d6d0-273">Typography Class Properties</span></span>  

 <span data-ttu-id="7d6d0-274">In der folgenden Tabelle werden die Eigenschaften, Werte und Standardeinstellungen des- <xref:System.Windows.Documents.Typography> Objekts aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7d6d0-274">The following table lists the properties, values, and default settings of the <xref:System.Windows.Documents.Typography> object.</span></span>  
  
|<span data-ttu-id="7d6d0-275">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7d6d0-275">Property</span></span>|<span data-ttu-id="7d6d0-276">Wert(e)</span><span class="sxs-lookup"><span data-stu-id="7d6d0-276">Value(s)</span></span>|<span data-ttu-id="7d6d0-277">Standardwert</span><span class="sxs-lookup"><span data-stu-id="7d6d0-277">Default Value</span></span>|  
|--------------|----------------|-------------------|  
|<xref:System.Windows.Documents.Typography.AnnotationAlternates%2A>|<span data-ttu-id="7d6d0-278">Numerischer Wert – Byte</span><span class="sxs-lookup"><span data-stu-id="7d6d0-278">Numeric value - byte</span></span>|<span data-ttu-id="7d6d0-279">0</span><span class="sxs-lookup"><span data-stu-id="7d6d0-279">0</span></span>|  
|<xref:System.Windows.Documents.Typography.Capitals%2A>|<span data-ttu-id="7d6d0-280"><xref:System.Windows.FontCapitals.AllPetiteCaps> &#124; <xref:System.Windows.FontCapitals.AllSmallCaps> &#124; <xref:System.Windows.FontCapitals.Normal> &#124; <xref:System.Windows.FontCapitals.PetiteCaps> &#124; <xref:System.Windows.FontCapitals.SmallCaps> &#124; <xref:System.Windows.FontCapitals.Titling> &#124; <xref:System.Windows.FontCapitals.Unicase></span><span class="sxs-lookup"><span data-stu-id="7d6d0-280"><xref:System.Windows.FontCapitals.AllPetiteCaps> &#124; <xref:System.Windows.FontCapitals.AllSmallCaps> &#124; <xref:System.Windows.FontCapitals.Normal> &#124; <xref:System.Windows.FontCapitals.PetiteCaps> &#124; <xref:System.Windows.FontCapitals.SmallCaps> &#124; <xref:System.Windows.FontCapitals.Titling> &#124; <xref:System.Windows.FontCapitals.Unicase></span></span>|<xref:System.Windows.FontCapitals.Normal?displayProperty=nameWithType>|  
|<xref:System.Windows.Documents.Typography.CapitalSpacing%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.CaseSensitiveForms%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.ContextualAlternates%2A>|<xref:System.Boolean>|`true`|  
|<xref:System.Windows.Documents.Typography.ContextualLigatures%2A>|<xref:System.Boolean>|`true`|  
|<xref:System.Windows.Documents.Typography.ContextualSwashes%2A>|<span data-ttu-id="7d6d0-281">Numerischer Wert – Byte</span><span class="sxs-lookup"><span data-stu-id="7d6d0-281">Numeric value - byte</span></span>|<span data-ttu-id="7d6d0-282">0</span><span class="sxs-lookup"><span data-stu-id="7d6d0-282">0</span></span>|  
|<xref:System.Windows.Documents.Typography.DiscretionaryLigatures%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.EastAsianExpertForms%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.EastAsianLanguage%2A>|<span data-ttu-id="7d6d0-283"><xref:System.Windows.FontEastAsianLanguage.HojoKanji> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis04> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis78> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis83> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis90> &#124; <xref:System.Windows.FontEastAsianLanguage.NlcKanji> &#124; <xref:System.Windows.FontEastAsianLanguage.Normal> &#124; <xref:System.Windows.FontEastAsianLanguage.Simplified> &#124; <xref:System.Windows.FontEastAsianLanguage.Traditional> &#124; <xref:System.Windows.FontEastAsianLanguage.TraditionalNames></span><span class="sxs-lookup"><span data-stu-id="7d6d0-283"><xref:System.Windows.FontEastAsianLanguage.HojoKanji> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis04> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis78> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis83> &#124; <xref:System.Windows.FontEastAsianLanguage.Jis90> &#124; <xref:System.Windows.FontEastAsianLanguage.NlcKanji> &#124; <xref:System.Windows.FontEastAsianLanguage.Normal> &#124; <xref:System.Windows.FontEastAsianLanguage.Simplified> &#124; <xref:System.Windows.FontEastAsianLanguage.Traditional> &#124; <xref:System.Windows.FontEastAsianLanguage.TraditionalNames></span></span>|<xref:System.Windows.FontEastAsianLanguage.Normal?displayProperty=nameWithType>|  
|<xref:System.Windows.Documents.Typography.EastAsianWidths%2A>|<span data-ttu-id="7d6d0-284"><xref:System.Windows.FontEastAsianWidths.Full> &#124; <xref:System.Windows.FontEastAsianWidths.Half> &#124; <xref:System.Windows.FontEastAsianWidths.Normal> &#124; <xref:System.Windows.FontEastAsianWidths.Proportional> &#124; <xref:System.Windows.FontEastAsianWidths.Quarter> &#124; <xref:System.Windows.FontEastAsianWidths.Third></span><span class="sxs-lookup"><span data-stu-id="7d6d0-284"><xref:System.Windows.FontEastAsianWidths.Full> &#124; <xref:System.Windows.FontEastAsianWidths.Half> &#124; <xref:System.Windows.FontEastAsianWidths.Normal> &#124; <xref:System.Windows.FontEastAsianWidths.Proportional> &#124; <xref:System.Windows.FontEastAsianWidths.Quarter> &#124; <xref:System.Windows.FontEastAsianWidths.Third></span></span>|<xref:System.Windows.FontEastAsianWidths.Normal?displayProperty=nameWithType>|  
|<xref:System.Windows.Documents.Typography.Fraction%2A>|<span data-ttu-id="7d6d0-285"><xref:System.Windows.FontFraction.Normal> &#124; <xref:System.Windows.FontFraction.Slashed> &#124; <xref:System.Windows.FontFraction.Stacked></span><span class="sxs-lookup"><span data-stu-id="7d6d0-285"><xref:System.Windows.FontFraction.Normal> &#124; <xref:System.Windows.FontFraction.Slashed> &#124; <xref:System.Windows.FontFraction.Stacked></span></span>|<xref:System.Windows.FontFraction.Normal?displayProperty=nameWithType>|  
|<xref:System.Windows.Documents.Typography.HistoricalForms%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.HistoricalLigatures%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.Kerning%2A>|<xref:System.Boolean>|`true`|  
|<xref:System.Windows.Documents.Typography.MathematicalGreek%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.NumeralAlignment%2A>|<span data-ttu-id="7d6d0-286"><xref:System.Windows.FontNumeralAlignment.Normal> &#124; <xref:System.Windows.FontNumeralAlignment.Proportional> &#124; <xref:System.Windows.FontNumeralAlignment.Tabular></span><span class="sxs-lookup"><span data-stu-id="7d6d0-286"><xref:System.Windows.FontNumeralAlignment.Normal> &#124; <xref:System.Windows.FontNumeralAlignment.Proportional> &#124; <xref:System.Windows.FontNumeralAlignment.Tabular></span></span>|<xref:System.Windows.FontNumeralAlignment.Normal?displayProperty=nameWithType>|  
|<xref:System.Windows.Documents.Typography.NumeralStyle%2A>|<xref:System.Boolean>|<xref:System.Windows.FontNumeralStyle.Normal?displayProperty=nameWithType>|  
|<xref:System.Windows.Documents.Typography.SlashedZero%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StandardLigatures%2A>|<xref:System.Boolean>|`true`|  
|<xref:System.Windows.Documents.Typography.StandardSwashes%2A>|<span data-ttu-id="7d6d0-287">Numerischer Wert – Byte</span><span class="sxs-lookup"><span data-stu-id="7d6d0-287">numeric value – byte</span></span>|<span data-ttu-id="7d6d0-288">0</span><span class="sxs-lookup"><span data-stu-id="7d6d0-288">0</span></span>|  
|<xref:System.Windows.Documents.Typography.StylisticAlternates%2A>|<span data-ttu-id="7d6d0-289">Numerischer Wert – Byte</span><span class="sxs-lookup"><span data-stu-id="7d6d0-289">numeric value – byte</span></span>|<span data-ttu-id="7d6d0-290">0</span><span class="sxs-lookup"><span data-stu-id="7d6d0-290">0</span></span>|  
|<xref:System.Windows.Documents.Typography.StylisticSet1%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet2%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet3%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet4%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet5%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet6%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet7%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet8%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet9%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet10%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet11%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet12%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet13%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet14%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet15%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet16%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet17%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet18%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet19%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.StylisticSet20%2A>|<xref:System.Boolean>|`false`|  
|<xref:System.Windows.Documents.Typography.Variants%2A>|<span data-ttu-id="7d6d0-291"><xref:System.Windows.FontVariants.Inferior> &#124; <xref:System.Windows.FontVariants.Normal> &#124; <xref:System.Windows.FontVariants.Ordinal> &#124; <xref:System.Windows.FontVariants.Ruby> &#124; <xref:System.Windows.FontVariants.Subscript> &#124; <xref:System.Windows.FontVariants.Superscript></span><span class="sxs-lookup"><span data-stu-id="7d6d0-291"><xref:System.Windows.FontVariants.Inferior> &#124; <xref:System.Windows.FontVariants.Normal> &#124; <xref:System.Windows.FontVariants.Ordinal> &#124; <xref:System.Windows.FontVariants.Ruby> &#124; <xref:System.Windows.FontVariants.Subscript> &#124; <xref:System.Windows.FontVariants.Superscript></span></span>|<xref:System.Windows.FontVariants.Normal?displayProperty=nameWithType>|  
  
## <a name="see-also"></a><span data-ttu-id="7d6d0-292">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d6d0-292">See also</span></span>

- <xref:System.Windows.Documents.Typography>
- [<span data-ttu-id="7d6d0-293">OpenType-Spezifikation</span><span class="sxs-lookup"><span data-stu-id="7d6d0-293">OpenType specification</span></span>](/typography/opentype/spec/)
- [<span data-ttu-id="7d6d0-294">Typografie in WPF</span><span class="sxs-lookup"><span data-stu-id="7d6d0-294">Typography in WPF</span></span>](typography-in-wpf.md)
- [<span data-ttu-id="7d6d0-295">OpenType-Beispielschriftartenpaket</span><span class="sxs-lookup"><span data-stu-id="7d6d0-295">Sample OpenType Font Pack</span></span>](sample-opentype-font-pack.md)
- [<span data-ttu-id="7d6d0-296">Verpacken von Schriftarten mit Anwendungen</span><span class="sxs-lookup"><span data-stu-id="7d6d0-296">Packaging Fonts with Applications</span></span>](packaging-fonts-with-applications.md)
