---
title: 'Vorgehensweise: Verwenden der Bildkantenglättung mit Text'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- strings [Windows Forms], smoothing drawn
- antialiasing [Windows Forms], using with text
- text [Windows Forms], smoothing
- text [Windows Forms], antialiasing
- strings [Windows Forms], antialiasing when drawing
ms.assetid: 48fc34f3-f236-4b01-a0cb-f0752e6d22ae
ms.openlocfilehash: 632ed329173d134495a424b34ca7c71e402607bf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976105"
---
# <a name="how-to-use-antialiasing-with-text"></a><span data-ttu-id="8326f-102">Vorgehensweise: Verwenden der Bildkantenglättung mit Text</span><span class="sxs-lookup"><span data-stu-id="8326f-102">How to: Use Antialiasing with Text</span></span>
<span data-ttu-id="8326f-103">*Antialiasing* bezieht sich auf die Glättung von verzweigten Kanten von gezeichneten Grafiken und Text, um deren Darstellung oder Lesbarkeit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="8326f-103">*Antialiasing* refers to the smoothing of jagged edges of drawn graphics and text to improve their appearance or readability.</span></span> <span data-ttu-id="8326f-104">Mit den verwalteten GDI+-Klassen können Sie einen hochwertigen Text mit Antialiasing und niedrigerer Qualität rendert.</span><span class="sxs-lookup"><span data-stu-id="8326f-104">With the managed GDI+ classes, you can render high quality antialiased text, as well as lower quality text.</span></span> <span data-ttu-id="8326f-105">In der Regel benötigt das Rendern höherer Qualität mehr Verarbeitungszeit als das Rendering mit niedrigerer Qualität.</span><span class="sxs-lookup"><span data-stu-id="8326f-105">Typically, higher quality rendering takes more processing time than lower quality rendering.</span></span> <span data-ttu-id="8326f-106">Um den Text Qualitätsgrad festzulegen, legen <xref:System.Drawing.Graphics.TextRenderingHint%2A> Sie die-Eigenschaft eines <xref:System.Drawing.Graphics> auf eines der Elemente der- <xref:System.Drawing.Text.TextRenderingHint> Enumeration fest.</span><span class="sxs-lookup"><span data-stu-id="8326f-106">To set the text quality level, set the <xref:System.Drawing.Graphics.TextRenderingHint%2A> property of a <xref:System.Drawing.Graphics> to one of the elements of the <xref:System.Drawing.Text.TextRenderingHint> enumeration</span></span>  
  
## <a name="example"></a><span data-ttu-id="8326f-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="8326f-107">Example</span></span>  
 <span data-ttu-id="8326f-108">Im folgenden Codebeispiel wird Text mit zwei verschiedenen Qualitätseinstellungen gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8326f-108">The following code example draws text with two different quality settings.</span></span>  
  
 [!code-csharp[System.Drawing.FontsAndText#21](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.FontsAndText/CS/Class1.cs#21)]
 [!code-vb[System.Drawing.FontsAndText#21](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.FontsAndText/VB/Class1.vb#21)]  

 <span data-ttu-id="8326f-109">Die folgende Abbildung zeigt die Ausgabe des Beispielcodes:</span><span class="sxs-lookup"><span data-stu-id="8326f-109">The following illustration shows the output of the example code:</span></span>  
  
 ![Screenshot, der Text mit zwei verschiedenen Qualitätseinstellungen anzeigt.](./media/how-to-use-antialiasing-with-text/antialiasing-text-quality-settings.png)  
  
## <a name="compiling-the-code"></a><span data-ttu-id="8326f-111">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="8326f-111">Compiling the Code</span></span>  
 <span data-ttu-id="8326f-112">Das vorangehende Codebeispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , dass ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .</span><span class="sxs-lookup"><span data-stu-id="8326f-112">The preceding code example is designed for use with Windows Forms, and it requires <xref:System.Windows.Forms.PaintEventArgs> `e`, which is a parameter of <xref:System.Windows.Forms.PaintEventHandler>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="8326f-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8326f-113">See also</span></span>

- [<span data-ttu-id="8326f-114">Verwenden von Schriftarten und Text</span><span class="sxs-lookup"><span data-stu-id="8326f-114">Using Fonts and Text</span></span>](using-fonts-and-text.md)
