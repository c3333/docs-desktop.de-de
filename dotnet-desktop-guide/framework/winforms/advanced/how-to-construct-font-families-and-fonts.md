---
title: 'Vorgehensweise: Erstellen von Schriftartfamilien und Schriftarten'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- font families [Windows Forms], constructing
- fonts [Windows Forms], constructing
ms.assetid: d3a4a223-9492-4b54-9afd-db1c31c3cefd
ms.openlocfilehash: 2d609525858c7a8ff77c0b86900b4fc7d6b4e39a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972380"
---
# <a name="how-to-construct-font-families-and-fonts"></a><span data-ttu-id="c73c5-102">Vorgehensweise: Erstellen von Schriftartfamilien und Schriftarten</span><span class="sxs-lookup"><span data-stu-id="c73c5-102">How to: Construct Font Families and Fonts</span></span>
<span data-ttu-id="c73c5-103">GDI+ gruppiert Schriftarten mit derselben Schriftart, aber unterschiedlichen Stilen in Schriftfamilien.</span><span class="sxs-lookup"><span data-stu-id="c73c5-103">GDI+ groups fonts with the same typeface but different styles into font families.</span></span> <span data-ttu-id="c73c5-104">Beispielsweise enthält die Familie "Arial Font" die folgenden Schriftarten:</span><span class="sxs-lookup"><span data-stu-id="c73c5-104">For example, the Arial font family contains the following fonts:</span></span>  
  
- <span data-ttu-id="c73c5-105">Arial Normal</span><span class="sxs-lookup"><span data-stu-id="c73c5-105">Arial Regular</span></span>  
  
- <span data-ttu-id="c73c5-106">Arial Fett</span><span class="sxs-lookup"><span data-stu-id="c73c5-106">Arial Bold</span></span>  
  
- <span data-ttu-id="c73c5-107">Arial kursiv</span><span class="sxs-lookup"><span data-stu-id="c73c5-107">Arial Italic</span></span>  
  
- <span data-ttu-id="c73c5-108">Arial Fett kursiv</span><span class="sxs-lookup"><span data-stu-id="c73c5-108">Arial Bold Italic</span></span>  
  
 <span data-ttu-id="c73c5-109">GDI+ verwendet vier Stile zum bilden von Familien: regulär, Fett, kursiv und fett formatiert.</span><span class="sxs-lookup"><span data-stu-id="c73c5-109">GDI+ uses four styles to form families: regular, bold, italic, and bold italic.</span></span> <span data-ttu-id="c73c5-110">Adjektive, z. b. *schmale* und *abgerundete* , werden nicht als Stile betrachtet. Sie sind nicht Teil des Familiennamens.</span><span class="sxs-lookup"><span data-stu-id="c73c5-110">Adjectives such as *narrow* and *rounded* are not considered styles; rather they are part of the family name.</span></span> <span data-ttu-id="c73c5-111">Beispielsweise ist Arial Narrow eine Schriftfamilie mit den folgenden Membern:</span><span class="sxs-lookup"><span data-stu-id="c73c5-111">For example, Arial Narrow is a font family with the following members:</span></span>  
  
- <span data-ttu-id="c73c5-112">Arial schmale reguläre</span><span class="sxs-lookup"><span data-stu-id="c73c5-112">Arial Narrow Regular</span></span>  
  
- <span data-ttu-id="c73c5-113">Arial schmale Fett Formatierung</span><span class="sxs-lookup"><span data-stu-id="c73c5-113">Arial Narrow Bold</span></span>  
  
- <span data-ttu-id="c73c5-114">Arial, schmale kursiv</span><span class="sxs-lookup"><span data-stu-id="c73c5-114">Arial Narrow Italic</span></span>  
  
- <span data-ttu-id="c73c5-115">Arial schmale Fett kursiv</span><span class="sxs-lookup"><span data-stu-id="c73c5-115">Arial Narrow Bold Italic</span></span>  
  
 <span data-ttu-id="c73c5-116">Bevor Sie Text mit GDI+ zeichnen können, müssen Sie ein <xref:System.Drawing.FontFamily> -Objekt und ein- <xref:System.Drawing.Font> Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="c73c5-116">Before you can draw text with GDI+, you need to construct a <xref:System.Drawing.FontFamily> object and a <xref:System.Drawing.Font> object.</span></span> <span data-ttu-id="c73c5-117">Das <xref:System.Drawing.FontFamily> -Objekt gibt die Schriftart (z. b. Arial) an, und das- <xref:System.Drawing.Font> Objekt gibt die Größe, den Stil und die Einheiten an.</span><span class="sxs-lookup"><span data-stu-id="c73c5-117">The <xref:System.Drawing.FontFamily> object specifies the typeface (for example, Arial), and the <xref:System.Drawing.Font> object specifies the size, style, and units.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c73c5-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c73c5-118">Example</span></span>  
 <span data-ttu-id="c73c5-119">Im folgenden Beispiel wird eine Schriftart mit einem regulären Stil mit einer Größe von 16 Pixeln erstellt.</span><span class="sxs-lookup"><span data-stu-id="c73c5-119">The following example constructs a regular style Arial font with a size of 16 pixels.</span></span> <span data-ttu-id="c73c5-120">Im folgenden Code ist das erste Argument, das an den- <xref:System.Drawing.Font.%23ctor%2A> Konstruktor übergeben wird, das- <xref:System.Drawing.FontFamily> Objekt.</span><span class="sxs-lookup"><span data-stu-id="c73c5-120">In the following code, the first argument passed to the <xref:System.Drawing.Font.%23ctor%2A> constructor is the <xref:System.Drawing.FontFamily> object.</span></span> <span data-ttu-id="c73c5-121">Das zweite Argument gibt die Größe der Schriftart an, die in Einheiten gemessen wird, die durch das vierte Argument identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="c73c5-121">The second argument specifies the size of the font measured in units identified by the fourth argument.</span></span> <span data-ttu-id="c73c5-122">Das dritte Argument identifiziert den Stil.</span><span class="sxs-lookup"><span data-stu-id="c73c5-122">The third argument identifies the style.</span></span>  
  
 <span data-ttu-id="c73c5-123"><xref:System.Drawing.GraphicsUnit.Pixel> ist ein Member der <xref:System.Drawing.GraphicsUnit> -Enumeration und <xref:System.Drawing.FontStyle.Regular> ist ein Member der- <xref:System.Drawing.FontStyle> Enumeration.</span><span class="sxs-lookup"><span data-stu-id="c73c5-123"><xref:System.Drawing.GraphicsUnit.Pixel> is a member of the <xref:System.Drawing.GraphicsUnit> enumeration, and <xref:System.Drawing.FontStyle.Regular> is a member of the <xref:System.Drawing.FontStyle> enumeration.</span></span>  
  
 [!code-csharp[System.Drawing.FontsAndText#61](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#61)]
 [!code-vb[System.Drawing.FontsAndText#61](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#61)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="c73c5-124">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="c73c5-124">Compiling the Code</span></span>  
 <span data-ttu-id="c73c5-125">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .</span><span class="sxs-lookup"><span data-stu-id="c73c5-125">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="c73c5-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c73c5-126">See also</span></span>

- [<span data-ttu-id="c73c5-127">Verwenden von Schriftarten und Text</span><span class="sxs-lookup"><span data-stu-id="c73c5-127">Using Fonts and Text</span></span>](using-fonts-and-text.md)
- [<span data-ttu-id="c73c5-128">Grafik und Zeichnen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="c73c5-128">Graphics and Drawing in Windows Forms</span></span>](graphics-and-drawing-in-windows-forms.md)
