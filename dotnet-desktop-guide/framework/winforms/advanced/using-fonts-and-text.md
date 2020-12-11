---
title: Verwenden von Schriftarten und Text
ms.date: 03/30/2017
helpviewer_keywords:
- GDI [Windows Forms], drawing text [Windows Forms]
- text [Windows Forms], drawing in Windows Forms
- examples [Windows Forms], fonts and text
- fonts [Windows Forms], using in Windows Forms
- strings [Windows Forms], drawing in Windows Forms
ms.assetid: d43640f3-da94-4df2-a29d-a9d021a1c069
ms.openlocfilehash: 73a4af5fe7367e777fcb83af8c84c09be91e5b1e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976045"
---
# <a name="using-fonts-and-text"></a><span data-ttu-id="074a0-102">Verwenden von Schriftarten und Text</span><span class="sxs-lookup"><span data-stu-id="074a0-102">Using Fonts and Text</span></span>
<span data-ttu-id="074a0-103">Es gibt mehrere Klassen, die von GDI+ und GDI zum Zeichnen von Text auf Windows Forms angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="074a0-103">There are several classes offered by GDI+ and GDI for drawing text on Windows Forms.</span></span> <span data-ttu-id="074a0-104">Die GDI+- <xref:System.Drawing.Graphics> Klasse verfügt über mehrere <xref:System.Drawing.Graphics.DrawString%2A> Methoden, mit denen Sie verschiedene Funktionen von Text, z. b. Speicherort, umgebenden Rechteck, Schriftart und Format, angeben können.</span><span class="sxs-lookup"><span data-stu-id="074a0-104">The GDI+ <xref:System.Drawing.Graphics> class has several <xref:System.Drawing.Graphics.DrawString%2A> methods that allow you to specify various features of text, such as location, bounding rectangle, font, and format.</span></span> <span data-ttu-id="074a0-105">Außerdem können Sie mithilfe der statischen <xref:System.Windows.Forms.TextRenderer.DrawText%2A> -und-Methoden, die <xref:System.Windows.Forms.TextRenderer.MeasureText%2A> von der-Klasse angeboten werden, Text mit GDI Zeichnen und Messen `TextRenderer` .</span><span class="sxs-lookup"><span data-stu-id="074a0-105">In addition, you can draw and measure text with GDI using the static <xref:System.Windows.Forms.TextRenderer.DrawText%2A> and <xref:System.Windows.Forms.TextRenderer.MeasureText%2A> methods offered by the `TextRenderer` class.</span></span> <span data-ttu-id="074a0-106">Mit den GDI-Methoden können Sie auch den Speicherort, die Schriftart und das Format angeben.</span><span class="sxs-lookup"><span data-stu-id="074a0-106">The GDI methods also allow you to specify location, font, and format.</span></span> <span data-ttu-id="074a0-107">Sie können entweder GDI oder GDI+ für Text Rendering auswählen. GDI bietet jedoch im Allgemeinen eine bessere Leistung und eine genauere Text Messung.</span><span class="sxs-lookup"><span data-stu-id="074a0-107">You can choose either GDI or GDI+ for text rendering; however, GDI generally offers better performance and more accurate text measuring.</span></span> <span data-ttu-id="074a0-108">Weitere Klassen, die zum Text Rendering beitragen `FontFamily` , sind, `Font` , <xref:System.Drawing.StringFormat> und `TextFormatFlags` .</span><span class="sxs-lookup"><span data-stu-id="074a0-108">Other classes that contribute to text rendering include `FontFamily`, `Font`, <xref:System.Drawing.StringFormat>, and `TextFormatFlags`.</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="074a0-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="074a0-109">In This Section</span></span>  
 [<span data-ttu-id="074a0-110">Vorgehensweise: Erstellen von Schriftartfamilien und Schriftarten</span><span class="sxs-lookup"><span data-stu-id="074a0-110">How to: Construct Font Families and Fonts</span></span>](how-to-construct-font-families-and-fonts.md)  
 <span data-ttu-id="074a0-111">Zeigt, wie `Font` -Objekte und-Objekte erstellt werden `FontFamily` .</span><span class="sxs-lookup"><span data-stu-id="074a0-111">Shows how to create `Font` and `FontFamily` objects.</span></span>  
  
 [<span data-ttu-id="074a0-112">Vorgehensweise: Zeichnen von Text an einer angegebenen Position</span><span class="sxs-lookup"><span data-stu-id="074a0-112">How to: Draw Text at a Specified Location</span></span>](how-to-draw-text-at-a-specified-location.md)  
 <span data-ttu-id="074a0-113">Beschreibt das Zeichnen von Text an einem bestimmten Speicherort mithilfe von GDI+ und GDI.</span><span class="sxs-lookup"><span data-stu-id="074a0-113">Describes how to draw text in a certain location using GDI+ and GDI.</span></span>  
  
 [<span data-ttu-id="074a0-114">Vorgehensweise: Zeichnen von umbrochenem Text in einem Rechteck</span><span class="sxs-lookup"><span data-stu-id="074a0-114">How to: Draw Wrapped Text in a Rectangle</span></span>](how-to-draw-wrapped-text-in-a-rectangle.md)  
 <span data-ttu-id="074a0-115">Erläutert das Zeichnen von Text in einem Rechteck mithilfe von GDI+ und GDI.</span><span class="sxs-lookup"><span data-stu-id="074a0-115">Explains how to draw text in a rectangle using GDI+ and GDI.</span></span>  
  
 [<span data-ttu-id="074a0-116">Vorgehensweise: Zeichnen von Text mit GDI</span><span class="sxs-lookup"><span data-stu-id="074a0-116">How to: Draw Text with GDI</span></span>](how-to-draw-text-with-gdi.md)  
 <span data-ttu-id="074a0-117">Veranschaulicht, wie GDI zum Zeichnen von Text verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="074a0-117">Demonstrates how to use GDI for drawing text.</span></span>  
  
 [<span data-ttu-id="074a0-118">Vorgehensweise: Ausrichten von gezeichnetem Text</span><span class="sxs-lookup"><span data-stu-id="074a0-118">How to: Align Drawn Text</span></span>](how-to-align-drawn-text.md)  
 <span data-ttu-id="074a0-119">Zeigt, wie Sie GDI+-und GDI-Text formatieren.</span><span class="sxs-lookup"><span data-stu-id="074a0-119">Shows how to format GDI+ and GDI text.</span></span>  
  
 [<span data-ttu-id="074a0-120">Vorgehensweise: Erstellen von vertikalem Text</span><span class="sxs-lookup"><span data-stu-id="074a0-120">How to: Create Vertical Text</span></span>](how-to-create-vertical-text.md)  
 <span data-ttu-id="074a0-121">Beschreibt, wie vertikal ausgerichteten Text mit GDI+ gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="074a0-121">Describes how to draw vertically aligned text with GDI+.</span></span>  
  
 [<span data-ttu-id="074a0-122">Vorgehensweise: Festlegen von Tabstopps in gezeichnetem Text</span><span class="sxs-lookup"><span data-stu-id="074a0-122">How to: Set Tab Stops in Drawn Text</span></span>](how-to-set-tab-stops-in-drawn-text.md)  
 <span data-ttu-id="074a0-123">Zeigt, wie Text mit Tabstopps mit GDI+ gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="074a0-123">Shows how draw text with tab stops with GDI+.</span></span>  
  
 [<span data-ttu-id="074a0-124">Vorgehensweise: Auflisten installierter Schriftarten</span><span class="sxs-lookup"><span data-stu-id="074a0-124">How to: Enumerate Installed Fonts</span></span>](how-to-enumerate-installed-fonts.md)  
 <span data-ttu-id="074a0-125">Erläutert, wie Sie die Namen der installierten Schriftarten auflisten.</span><span class="sxs-lookup"><span data-stu-id="074a0-125">Explains how to list the names of installed fonts.</span></span>  
  
 [<span data-ttu-id="074a0-126">Vorgehensweise: Erstellen einer privaten Schriftartenauflistung</span><span class="sxs-lookup"><span data-stu-id="074a0-126">How to: Create a Private Font Collection</span></span>](how-to-create-a-private-font-collection.md)  
 <span data-ttu-id="074a0-127">Beschreibt, wie ein- <xref:System.Drawing.Text.PrivateFontCollection> Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="074a0-127">Describes how to create a <xref:System.Drawing.Text.PrivateFontCollection> object.</span></span>  
  
 [<span data-ttu-id="074a0-128">Vorgehensweise: Abrufen von Schriftarteigenschaften</span><span class="sxs-lookup"><span data-stu-id="074a0-128">How to: Obtain Font Metrics</span></span>](how-to-obtain-font-metrics.md)  
 <span data-ttu-id="074a0-129">Zeigt, wie Sie Schriftart Metriken wie z. b. den Zellen Aufstieg und den Abstieg abrufen</span><span class="sxs-lookup"><span data-stu-id="074a0-129">Shows how to obtain font metrics such as cell ascent and descent.</span></span>  
  
 [<span data-ttu-id="074a0-130">Vorgehensweise: Verwenden der Bildkantenglättung mit Text</span><span class="sxs-lookup"><span data-stu-id="074a0-130">How to: Use Antialiasing with Text</span></span>](how-to-use-antialiasing-with-text.md)  
 <span data-ttu-id="074a0-131">Erläutert, wie Antialiasing beim Zeichnen von Text verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="074a0-131">Explains how to use antialiasing when drawing text.</span></span>  
  
## <a name="reference"></a><span data-ttu-id="074a0-132">Verweis</span><span class="sxs-lookup"><span data-stu-id="074a0-132">Reference</span></span>  
 <xref:System.Drawing.Font>  
 <span data-ttu-id="074a0-133">Beschreibt diese Klasse und enthält Links zu allen Membern.</span><span class="sxs-lookup"><span data-stu-id="074a0-133">Describes this class and contains links to all of its members.</span></span>  
  
 <xref:System.Drawing.FontFamily>  
 <span data-ttu-id="074a0-134">Beschreibt diese Klasse und enthält Links zu allen Membern.</span><span class="sxs-lookup"><span data-stu-id="074a0-134">Describes this class and contains links to all of its members.</span></span>  
  
 <xref:System.Drawing.Text.PrivateFontCollection>  
 <span data-ttu-id="074a0-135">Beschreibt diese Klasse und enthält Links zu allen Membern.</span><span class="sxs-lookup"><span data-stu-id="074a0-135">Describes this class and contains links to all of its members.</span></span>  
  
 <xref:System.Windows.Forms.TextRenderer>  
 <span data-ttu-id="074a0-136">Beschreibt diese Klasse und enthält Links zu allen Membern.</span><span class="sxs-lookup"><span data-stu-id="074a0-136">Describes this class and contains links to all of its members.</span></span>  
  
 <xref:System.Windows.Forms.TextFormatFlags>  
 <span data-ttu-id="074a0-137">Beschreibt diese Klasse und enthält Links zu allen Membern.</span><span class="sxs-lookup"><span data-stu-id="074a0-137">Describes this class and contains links to all of its members.</span></span>
