---
title: 'Gewusst wie: Anpassen der Größe des Ziehpunkts auf einer Bildlaufleiste'
ms.date: 03/30/2017
helpviewer_keywords:
- ScrollBar control [WPF]
- customizing thumb size [WPF]
- thumb size [WPF]
ms.assetid: fa32b866-5ca1-4e73-85e7-2ac64b80d194
ms.openlocfilehash: 60ae7c4e95801036c5deb0c485645297509b830c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977815"
---
# <a name="how-to-customize-the-thumb-size-on-a-scrollbar"></a><span data-ttu-id="7a8a8-102">Gewusst wie: Anpassen der Größe des Ziehpunkts auf einer Bildlaufleiste</span><span class="sxs-lookup"><span data-stu-id="7a8a8-102">How to: Customize the Thumb Size on a ScrollBar</span></span>
<span data-ttu-id="7a8a8-103">In diesem Thema wird erläutert, wie die <xref:System.Windows.Controls.Primitives.Thumb> eines <xref:System.Windows.Controls.Primitives.ScrollBar> auf eine festgelegte Größe festgelegt wird und wie eine minimale Größe für die eines angegeben wird <xref:System.Windows.Controls.Primitives.Thumb> <xref:System.Windows.Controls.Primitives.ScrollBar> .</span><span class="sxs-lookup"><span data-stu-id="7a8a8-103">This topic explains how to set the <xref:System.Windows.Controls.Primitives.Thumb> of a <xref:System.Windows.Controls.Primitives.ScrollBar> to a fixed size and how to specify a minimum size for the <xref:System.Windows.Controls.Primitives.Thumb> of a <xref:System.Windows.Controls.Primitives.ScrollBar>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="7a8a8-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7a8a8-104">Example</span></span>  
  
## <a name="description"></a><span data-ttu-id="7a8a8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a8a8-105">Description</span></span>  
 <span data-ttu-id="7a8a8-106">Im folgenden Beispiel wird eine erstellt <xref:System.Windows.Controls.Primitives.ScrollBar> , die eine <xref:System.Windows.Controls.Primitives.Thumb> mit fester Größe aufweist.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-106">The following example creates a <xref:System.Windows.Controls.Primitives.ScrollBar> that has a <xref:System.Windows.Controls.Primitives.Thumb> with a fixed size.</span></span> <span data-ttu-id="7a8a8-107">Im Beispiel wird die <xref:System.Windows.Controls.Primitives.Track.ViewportSize%2A> -Eigenschaft des <xref:System.Windows.Controls.Primitives.Thumb> auf festgelegt, <xref:System.Double.NaN> und die Höhe des wird festgelegt <xref:System.Windows.Controls.Primitives.Thumb> .</span><span class="sxs-lookup"><span data-stu-id="7a8a8-107">The example sets the <xref:System.Windows.Controls.Primitives.Track.ViewportSize%2A> property of the <xref:System.Windows.Controls.Primitives.Thumb> to <xref:System.Double.NaN> and sets the height of the <xref:System.Windows.Controls.Primitives.Thumb>.</span></span>  <span data-ttu-id="7a8a8-108">Zum Erstellen eines horizontalen <xref:System.Windows.Controls.Primitives.ScrollBar> mit einem mit <xref:System.Windows.Controls.Primitives.Thumb> fester Breite legen Sie die Breite des fest <xref:System.Windows.Controls.Primitives.Thumb> .</span><span class="sxs-lookup"><span data-stu-id="7a8a8-108">To create a horizontal <xref:System.Windows.Controls.Primitives.ScrollBar> with a <xref:System.Windows.Controls.Primitives.Thumb> that has a fixed width, set the width of the <xref:System.Windows.Controls.Primitives.Thumb>.</span></span>  
  
## <a name="code"></a><span data-ttu-id="7a8a8-109">Code</span><span class="sxs-lookup"><span data-stu-id="7a8a8-109">Code</span></span>  
 [!code-xaml[ScrollBarCustomThumbSize#1](~/samples/snippets/csharp/VS_Snippets_Wpf/ScrollBarCustomThumbSize/CS/Window1.xaml#1)]  
  
## <a name="description"></a><span data-ttu-id="7a8a8-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a8a8-110">Description</span></span>  
 <span data-ttu-id="7a8a8-111">Im folgenden Beispiel wird eine erstellt <xref:System.Windows.Controls.Primitives.ScrollBar> , die eine <xref:System.Windows.Controls.Primitives.Thumb> mit einer minimalen Größe aufweist.</span><span class="sxs-lookup"><span data-stu-id="7a8a8-111">The following example creates a <xref:System.Windows.Controls.Primitives.ScrollBar> that has a <xref:System.Windows.Controls.Primitives.Thumb> with a minimum size.</span></span> <span data-ttu-id="7a8a8-112">Im Beispiel wird der Wert von festgelegt <xref:System.Windows.SystemParameters.VerticalScrollBarButtonHeightKey%2A> .</span><span class="sxs-lookup"><span data-stu-id="7a8a8-112">The example sets the value of <xref:System.Windows.SystemParameters.VerticalScrollBarButtonHeightKey%2A>.</span></span> <span data-ttu-id="7a8a8-113">Legen Sie zum Erstellen eines horizontalen <xref:System.Windows.Controls.Primitives.ScrollBar> mit einem mit <xref:System.Windows.Controls.Primitives.Thumb> einer minimalen Breite den fest <xref:System.Windows.SystemParameters.HorizontalScrollBarButtonWidthKey%2A> .</span><span class="sxs-lookup"><span data-stu-id="7a8a8-113">To create a horizontal <xref:System.Windows.Controls.Primitives.ScrollBar> with a <xref:System.Windows.Controls.Primitives.Thumb> that has a minimum width, set the <xref:System.Windows.SystemParameters.HorizontalScrollBarButtonWidthKey%2A>.</span></span>  
  
## <a name="code"></a><span data-ttu-id="7a8a8-114">Code</span><span class="sxs-lookup"><span data-stu-id="7a8a8-114">Code</span></span>  
 [!code-xaml[ScrollBarCustomThumbSize#2](~/samples/snippets/csharp/VS_Snippets_Wpf/ScrollBarCustomThumbSize/CS/Window1.xaml#2)]  
  
## <a name="see-also"></a><span data-ttu-id="7a8a8-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a8a8-115">See also</span></span>

- [<span data-ttu-id="7a8a8-116">ScrollBar-Stile und -Vorlagen</span><span class="sxs-lookup"><span data-stu-id="7a8a8-116">ScrollBar Styles and Templates</span></span>](scrollbar-styles-and-templates.md)
