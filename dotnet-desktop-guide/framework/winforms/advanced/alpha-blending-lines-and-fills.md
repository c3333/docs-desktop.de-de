---
title: Alphablending von Linien und Füllungen
ms.date: 03/30/2017
helpviewer_keywords:
- lines [Windows Forms], adding transparency
- examples [Windows Forms], alpha blending
- alpha blending [Windows Forms], using with lines
- alpha blending
- lines [Windows Forms], alpha blending
- fills [Windows Forms], alpha blending
- alpha blending [Windows Forms], using with fills
- shapes [Windows Forms], adding transparency
ms.assetid: 5440f48c-3ac9-44c3-b170-c1c110bdbab8
ms.openlocfilehash: 66061341ee6539e2172c537a0b2a6ec9ff87565c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974911"
---
# <a name="alpha-blending-lines-and-fills"></a><span data-ttu-id="ce15c-102">Alphablending von Linien und Füllungen</span><span class="sxs-lookup"><span data-stu-id="ce15c-102">Alpha Blending Lines and Fills</span></span>
<span data-ttu-id="ce15c-103">In GDI+ ist eine Farbe ein 32-Bit-Wert mit 8 Bits für Alpha, rot, grün und blau.</span><span class="sxs-lookup"><span data-stu-id="ce15c-103">In GDI+, a color is a 32-bit value with 8 bits each for alpha, red, green, and blue.</span></span> <span data-ttu-id="ce15c-104">Der Alpha-Wert gibt die Transparenz der Farbe an – das Ausmaß, in dem die Farbe mit der Hintergrundfarbe gemischt wird.</span><span class="sxs-lookup"><span data-stu-id="ce15c-104">The alpha value indicates the transparency of the color — the extent to which the color is blended with the background color.</span></span> <span data-ttu-id="ce15c-105">Alpha Werte reichen von 0 bis 255, wobei 0 eine vollständig transparente Farbe darstellt und 255 eine vollständig nicht transparente Farbe darstellt.</span><span class="sxs-lookup"><span data-stu-id="ce15c-105">Alpha values range from 0 through 255, where 0 represents a fully transparent color, and 255 represents a fully opaque color.</span></span>  
  
 <span data-ttu-id="ce15c-106">Alpha Blending ist eine pixelweise Mischung aus Quell-und Hintergrund Farbdaten.</span><span class="sxs-lookup"><span data-stu-id="ce15c-106">Alpha blending is a pixel-by-pixel blending of source and background color data.</span></span> <span data-ttu-id="ce15c-107">Jede der drei Komponenten (rot, grün, blau) einer angegebenen Quellfarbe wird mit der entsprechenden Komponente der Hintergrundfarbe entsprechend der folgenden Formel gemischt:</span><span class="sxs-lookup"><span data-stu-id="ce15c-107">Each of the three components (red, green, blue) of a given source color is blended with the corresponding component of the background color according to the following formula:</span></span>  
  
 <span data-ttu-id="ce15c-108">Display Color = sourcecolor × Alpha/255 + BackgroundColor × (255 – Alpha)/255</span><span class="sxs-lookup"><span data-stu-id="ce15c-108">displayColor = sourceColor × alpha / 255 + backgroundColor × (255 – alpha) / 255</span></span>  
  
 <span data-ttu-id="ce15c-109">Nehmen wir beispielsweise an, die rote Komponente der Quellfarbe ist 150, und die rote Komponente der Hintergrundfarbe ist 100.</span><span class="sxs-lookup"><span data-stu-id="ce15c-109">For example, suppose the red component of the source color is 150 and the red component of the background color is 100.</span></span> <span data-ttu-id="ce15c-110">Wenn der Alpha-Wert 200 ist, wird die rote Komponente der resultierenden Farbe wie folgt berechnet:</span><span class="sxs-lookup"><span data-stu-id="ce15c-110">If the alpha value is 200, the red component of the resultant color is calculated as follows:</span></span>  
  
 <span data-ttu-id="ce15c-111">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span><span class="sxs-lookup"><span data-stu-id="ce15c-111">150 × 200 / 255 + 100 × (255 – 200) / 255 = 139</span></span>  
  
## <a name="in-this-section"></a><span data-ttu-id="ce15c-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ce15c-112">In This Section</span></span>  
 [<span data-ttu-id="ce15c-113">Vorgehensweise: Zeichnen deckender und halbtransparenter Linien</span><span class="sxs-lookup"><span data-stu-id="ce15c-113">How to: Draw Opaque and Semitransparent Lines</span></span>](how-to-draw-opaque-and-semitransparent-lines.md)  
 <span data-ttu-id="ce15c-114">Zeigt, wie Alpha gemischte Linien gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="ce15c-114">Shows how to draw alpha-blended lines.</span></span>  
  
 [<span data-ttu-id="ce15c-115">Vorgehensweise: Zeichnen mit nicht transparenten und halb transparenten Pinseln</span><span class="sxs-lookup"><span data-stu-id="ce15c-115">How to: Draw with Opaque and Semitransparent Brushes</span></span>](how-to-draw-with-opaque-and-semitransparent-brushes.md)  
 <span data-ttu-id="ce15c-116">Erläutert die Alpha Mischung mit Pinseln.</span><span class="sxs-lookup"><span data-stu-id="ce15c-116">Explains how to alpha-blend with brushes.</span></span>  
  
 [<span data-ttu-id="ce15c-117">Vorgehensweise: Verwenden des Mischmodus zum Steuern des Alphablendings</span><span class="sxs-lookup"><span data-stu-id="ce15c-117">How to: Use Compositing Mode to Control Alpha Blending</span></span>](how-to-use-compositing-mode-to-control-alpha-blending.md)  
 <span data-ttu-id="ce15c-118">Beschreibt, wie die Alpha Mischung mithilfe von gesteuert wird <xref:System.Drawing.Drawing2D.CompositingMode> .</span><span class="sxs-lookup"><span data-stu-id="ce15c-118">Describes how to control alpha blending using <xref:System.Drawing.Drawing2D.CompositingMode>.</span></span>  
  
 [<span data-ttu-id="ce15c-119">Vorgehensweise: Verwenden einer Farbmatrix zum Festlegen von Alphawerten in Bildern</span><span class="sxs-lookup"><span data-stu-id="ce15c-119">How to: Use a Color Matrix to Set Alpha Values in Images</span></span>](how-to-use-a-color-matrix-to-set-alpha-values-in-images.md)  
 <span data-ttu-id="ce15c-120">Erläutert, wie ein- <xref:System.Drawing.Imaging.ColorMatrix> Objekt verwendet wird, um Alpha Blending zu steuern.</span><span class="sxs-lookup"><span data-stu-id="ce15c-120">Explains how to use a <xref:System.Drawing.Imaging.ColorMatrix> object to control alpha blending.</span></span>
