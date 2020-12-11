---
title: 'Vorgehensweise: Erstellen von vertikalem Text'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [Windows Forms], drawing vertical
- Windows Forms, drawing vertical text
- strings [Windows Forms], drawing vertical
- vertical text [Windows Forms], drawing
ms.assetid: 50c69046-4188-47d9-b949-cc2610ffd337
ms.openlocfilehash: 86401342625f593945b801f7619ef9ca9681317c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972362"
---
# <a name="how-to-create-vertical-text"></a><span data-ttu-id="25f3c-102">Vorgehensweise: Erstellen von vertikalem Text</span><span class="sxs-lookup"><span data-stu-id="25f3c-102">How to: Create Vertical Text</span></span>
<span data-ttu-id="25f3c-103">Sie können ein- <xref:System.Drawing.StringFormat> Objekt verwenden, um anzugeben, dass Text vertikal und nicht horizontal gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="25f3c-103">You can use a <xref:System.Drawing.StringFormat> object to specify that text be drawn vertically rather than horizontally.</span></span>  
  
## <a name="example"></a><span data-ttu-id="25f3c-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="25f3c-104">Example</span></span>  
 <span data-ttu-id="25f3c-105">Im folgenden Beispiel wird der-Wert der- <xref:System.Drawing.StringFormatFlags.DirectionVertical> <xref:System.Drawing.StringFormat.FormatFlags%2A> Eigenschaft eines- <xref:System.Drawing.StringFormat> Objekts zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="25f3c-105">The following example assigns the value <xref:System.Drawing.StringFormatFlags.DirectionVertical> to the <xref:System.Drawing.StringFormat.FormatFlags%2A> property of a <xref:System.Drawing.StringFormat> object.</span></span> <span data-ttu-id="25f3c-106">Dieses <xref:System.Drawing.StringFormat> Objekt wird an die- <xref:System.Drawing.Graphics.DrawString%2A> Methode der- <xref:System.Drawing.Graphics> Klasse übermittelt.</span><span class="sxs-lookup"><span data-stu-id="25f3c-106">That <xref:System.Drawing.StringFormat> object is passed to the <xref:System.Drawing.Graphics.DrawString%2A> method of the <xref:System.Drawing.Graphics> class.</span></span> <span data-ttu-id="25f3c-107">Der Wert <xref:System.Drawing.StringFormatFlags.DirectionVertical> ist ein Member der- <xref:System.Drawing.StringFormatFlags> Enumeration.</span><span class="sxs-lookup"><span data-stu-id="25f3c-107">The value <xref:System.Drawing.StringFormatFlags.DirectionVertical> is a member of the <xref:System.Drawing.StringFormatFlags> enumeration.</span></span>  
  
 <span data-ttu-id="25f3c-108">Die folgende Abbildung zeigt den vertikalen Text:</span><span class="sxs-lookup"><span data-stu-id="25f3c-108">The following illustration shows the vertical text:</span></span>
  
 ![Grafik, die vertikalen Schriftart Text zeigt.](./media/how-to-create-vertical-text/vertical-font-text-graphic.png)  
  
 [!code-csharp[System.Drawing.FontsAndText#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.FontsAndText#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="25f3c-110">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="25f3c-110">Compiling the Code</span></span>  
  
- <span data-ttu-id="25f3c-111">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .</span><span class="sxs-lookup"><span data-stu-id="25f3c-111">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e` , which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="25f3c-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25f3c-112">See also</span></span>

- [<span data-ttu-id="25f3c-113">Vorgehensweise: Zeichnen von Text mit GDI</span><span class="sxs-lookup"><span data-stu-id="25f3c-113">How to: Draw Text with GDI</span></span>](how-to-draw-text-with-gdi.md)
