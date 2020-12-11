---
title: 'Vorgehensweise: Ausfüllen offener Körper'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- open figures [Windows Forms], filling
- figures [Windows Forms], filling
ms.assetid: 5a36b0e4-f1f4-46c0-a85a-22ae98491950
ms.openlocfilehash: 6ecea7d3edb0c3e25fb4e69ff12b88019e530021
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975910"
---
# <a name="how-to-fill-open-figures"></a><span data-ttu-id="57f27-102">Vorgehensweise: Ausfüllen offener Körper</span><span class="sxs-lookup"><span data-stu-id="57f27-102">How to: Fill Open Figures</span></span>
<span data-ttu-id="57f27-103">Sie können einen Pfad ausfüllen, indem Sie ein- <xref:System.Drawing.Drawing2D.GraphicsPath> Objekt an die- <xref:System.Drawing.Graphics.FillPath%2A> Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="57f27-103">You can fill a path by passing a <xref:System.Drawing.Drawing2D.GraphicsPath> object to the <xref:System.Drawing.Graphics.FillPath%2A> method.</span></span> <span data-ttu-id="57f27-104">Die- <xref:System.Drawing.Graphics.FillPath%2A> Methode füllt den Pfad gemäß dem Füll Modus (Alternative oder Winding), der derzeit für den Pfad festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="57f27-104">The <xref:System.Drawing.Graphics.FillPath%2A> method fills the path according to the fill mode (alternate or winding) currently set for the path.</span></span> <span data-ttu-id="57f27-105">Wenn für den Pfad offene Abbildungen vorhanden sind, wird der Pfad so aufgefüllt, als ob diese Abbildungen geschlossen wurden.</span><span class="sxs-lookup"><span data-stu-id="57f27-105">If the path has any open figures, the path is filled as if those figures were closed.</span></span> <span data-ttu-id="57f27-106">GDI+ schließt eine Abbildung, indem eine gerade Linie von ihrem Endpunkt zum Ausgangspunkt gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="57f27-106">GDI+ closes a figure by drawing a straight line from its ending point to its starting point.</span></span>  
  
## <a name="example"></a><span data-ttu-id="57f27-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="57f27-107">Example</span></span>  
 <span data-ttu-id="57f27-108">Im folgenden Beispiel wird ein Pfad erstellt, der über eine offene Abbildung (einen Bogen) und eine geschlossene Abbildung (eine Ellipse) verfügt.</span><span class="sxs-lookup"><span data-stu-id="57f27-108">The following example creates a path that has one open figure (an arc) and one closed figure (an ellipse).</span></span> <span data-ttu-id="57f27-109">Die- <xref:System.Drawing.Graphics.FillPath%2A> Methode füllt den Pfad gemäß dem Standard Füll Modus, d <xref:System.Drawing.Drawing2D.FillMode.Alternate> . h..</span><span class="sxs-lookup"><span data-stu-id="57f27-109">The <xref:System.Drawing.Graphics.FillPath%2A> method fills the path according to the default fill mode, which is <xref:System.Drawing.Drawing2D.FillMode.Alternate>.</span></span>  
  
 <span data-ttu-id="57f27-110">Die folgende Abbildung zeigt die Ausgabe des Beispielcodes.</span><span class="sxs-lookup"><span data-stu-id="57f27-110">The following illustration shows the output of the example code.</span></span> <span data-ttu-id="57f27-111">Beachten Sie, dass der Pfad (entsprechend) ausgefüllt wird, <xref:System.Drawing.Drawing2D.FillMode.Alternate> als ob die öffnende Figur durch eine gerade Linie von ihrem Endpunkt bis zum Ausgangspunkt geschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="57f27-111">Note that the path is filled (according to <xref:System.Drawing.Drawing2D.FillMode.Alternate>) as if the open figure were closed by a straight line from its ending point to its starting point.</span></span>  
  
 ![Diagramm, das die Ausgabe der FillPath-Methode anzeigt](./media/how-to-fill-open-figures/fill-path-alternate-mode.png)  
  
 [!code-csharp[System.Drawing.ConstructingDrawingPaths#11](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/CS/Class1.cs#11)]
 [!code-vb[System.Drawing.ConstructingDrawingPaths#11](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.ConstructingDrawingPaths/VB/Class1.vb#11)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="57f27-113">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="57f27-113">Compiling the Code</span></span>  
 <span data-ttu-id="57f27-114">Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter des- <xref:System.Windows.Forms.Control.Paint> Ereignis Handlers ist.</span><span class="sxs-lookup"><span data-stu-id="57f27-114">The preceding example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of the <xref:System.Windows.Forms.Control.Paint> event handler.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="57f27-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="57f27-115">See also</span></span>

- <xref:System.Drawing.Drawing2D.GraphicsPath>
- [<span data-ttu-id="57f27-116">Grafikpfade in GDI+</span><span class="sxs-lookup"><span data-stu-id="57f27-116">Graphics Paths in GDI+</span></span>](graphics-paths-in-gdi.md)
