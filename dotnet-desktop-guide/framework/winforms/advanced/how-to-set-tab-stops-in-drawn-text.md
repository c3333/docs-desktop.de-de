---
title: 'Vorgehensweise: Festlegen von Tabstopps in gezeichnetem Text'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [Windows Forms], drawing with tab stops
- tabs [Windows Forms], drawn text
ms.assetid: 64878f98-39ba-4303-b63f-0859ab682eeb
ms.openlocfilehash: 8821f6170b8ba588e3197ef54eab14c2719a6cc3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975881"
---
# <a name="how-to-set-tab-stops-in-drawn-text"></a><span data-ttu-id="600ab-102">Vorgehensweise: Festlegen von Tabstopps in gezeichnetem Text</span><span class="sxs-lookup"><span data-stu-id="600ab-102">How to: Set Tab Stops in Drawn Text</span></span>
<span data-ttu-id="600ab-103">Sie können Tabstopps für Text festlegen, indem Sie die <xref:System.Drawing.StringFormat.SetTabStops%2A> -Methode eines <xref:System.Drawing.StringFormat> -Objekts aufrufen und dieses <xref:System.Drawing.StringFormat> Objekt anschließend an die- <xref:System.Drawing.Graphics.DrawString%2A> Methode der-Klasse übergeben <xref:System.Drawing.Graphics> .</span><span class="sxs-lookup"><span data-stu-id="600ab-103">You can set tab stops for text by calling the <xref:System.Drawing.StringFormat.SetTabStops%2A> method of a <xref:System.Drawing.StringFormat> object and then passing that <xref:System.Drawing.StringFormat> object to the <xref:System.Drawing.Graphics.DrawString%2A> method of the <xref:System.Drawing.Graphics> class.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="600ab-104"><xref:System.Windows.Forms.TextRenderer?displayProperty=nameWithType>Unterstützt das Hinzufügen von Tabstopps zum Zeichnen von Text nicht, obwohl Sie vorhandene Tabstopps mit dem-Flag erweitern können <xref:System.Windows.Forms.TextFormatFlags.ExpandTabs?displayProperty=nameWithType> .</span><span class="sxs-lookup"><span data-stu-id="600ab-104">The <xref:System.Windows.Forms.TextRenderer?displayProperty=nameWithType> does not support adding tab stops to drawn text, although you can expand existing tab stops using the <xref:System.Windows.Forms.TextFormatFlags.ExpandTabs?displayProperty=nameWithType> flag.</span></span>  
  
## <a name="example"></a><span data-ttu-id="600ab-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="600ab-105">Example</span></span>  
 <span data-ttu-id="600ab-106">Im folgenden Beispiel wird der Tabstopp bei 150, 250 und 350 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="600ab-106">The following example sets tab stops at 150, 250, and 350.</span></span> <span data-ttu-id="600ab-107">Anschließend wird im Code eine Liste mit Namen und testbewertungen im Registerkarten Format angezeigt.</span><span class="sxs-lookup"><span data-stu-id="600ab-107">Then, the code displays a tabbed list of names and test scores.</span></span>  
  
 <span data-ttu-id="600ab-108">Die folgende Abbildung zeigt den Text im Registerkarten Format:</span><span class="sxs-lookup"><span data-stu-id="600ab-108">The following illustration shows the tabbed text:</span></span>  
  
 ![Screenshot, der eine Liste mit Namen und Bewertungen im Registerkarten Format anzeigt.](./media/how-to-set-tab-stops-in-drawn-text/tab-list-names-test-scores.png)  
  
 <span data-ttu-id="600ab-110">Der folgende Code übergibt zwei Argumente an die- <xref:System.Drawing.StringFormat.SetTabStops%2A> Methode.</span><span class="sxs-lookup"><span data-stu-id="600ab-110">The following code passes two arguments to the <xref:System.Drawing.StringFormat.SetTabStops%2A> method.</span></span> <span data-ttu-id="600ab-111">Das zweite Argument ist ein Array, das Tabulator Offsets enthält.</span><span class="sxs-lookup"><span data-stu-id="600ab-111">The second argument is an array that contains tab offsets.</span></span> <span data-ttu-id="600ab-112">Das erste an übergebenen Argument ist 0 (null) <xref:System.Drawing.StringFormat.SetTabStops%2A> , womit angegeben wird, dass der erste Offset im Array von Position 0, dem linken Rand des umgebenden Rechtecks, gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="600ab-112">The first argument passed to <xref:System.Drawing.StringFormat.SetTabStops%2A> is 0, which indicates that the first offset in the array is measured from position 0, the left edge of the bounding rectangle.</span></span>  
  
 [!code-csharp[System.Drawing.FontsAndText#41](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#41)]
 [!code-vb[System.Drawing.FontsAndText#41](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#41)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="600ab-113">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="600ab-113">Compiling the Code</span></span>  
  
- <span data-ttu-id="600ab-114">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .</span><span class="sxs-lookup"><span data-stu-id="600ab-114">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="600ab-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="600ab-115">See also</span></span>

- [<span data-ttu-id="600ab-116">Verwenden von Schriftarten und Text</span><span class="sxs-lookup"><span data-stu-id="600ab-116">Using Fonts and Text</span></span>](using-fonts-and-text.md)
- [<span data-ttu-id="600ab-117">Vorgehensweise: Zeichnen von Text mit GDI</span><span class="sxs-lookup"><span data-stu-id="600ab-117">How to: Draw Text with GDI</span></span>](how-to-draw-text-with-gdi.md)
