---
title: 'Gewusst wie: Definieren eines Stifts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- pens [WPF], defining
- creating [WPF], pens
ms.assetid: 7a4f2900-cdf9-49de-84e0-ba5d0ded4d33
ms.openlocfilehash: 1d69a40604dbf2f7a73c17279ae946faeb6c634a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976188"
---
# <a name="how-to-define-a-pen"></a><span data-ttu-id="22268-102">Gewusst wie: Definieren eines Stifts</span><span class="sxs-lookup"><span data-stu-id="22268-102">How to: Define a Pen</span></span>
<span data-ttu-id="22268-103">In diesem Beispiel wird gezeigt, wie eine Form mit einem <xref:System.Windows.Media.Pen> Umriss wird.</span><span class="sxs-lookup"><span data-stu-id="22268-103">This example shows how use a <xref:System.Windows.Media.Pen> to outline a shape.</span></span> <span data-ttu-id="22268-104">Zum Erstellen eines einfachen <xref:System.Windows.Media.Pen> müssen Sie nur sein und angeben <xref:System.Windows.Media.Pen.Thickness%2A> <xref:System.Windows.Media.Pen.Brush%2A> .</span><span class="sxs-lookup"><span data-stu-id="22268-104">To create a simple <xref:System.Windows.Media.Pen>, you need only specify its <xref:System.Windows.Media.Pen.Thickness%2A> and <xref:System.Windows.Media.Pen.Brush%2A>.</span></span> <span data-ttu-id="22268-105">Sie können komplexere Pen erstellen, indem Sie <xref:System.Windows.Media.Pen.DashStyle%2A> , <xref:System.Windows.Media.Pen.DashCap%2A> , <xref:System.Windows.Media.Pen.LineJoin%2A> , und angeben <xref:System.Windows.Media.Pen.StartLineCap%2A> <xref:System.Windows.Media.Pen.EndLineCap%2A> .</span><span class="sxs-lookup"><span data-stu-id="22268-105">You can create more complex pen's by specifying a <xref:System.Windows.Media.Pen.DashStyle%2A>, <xref:System.Windows.Media.Pen.DashCap%2A>, <xref:System.Windows.Media.Pen.LineJoin%2A>, <xref:System.Windows.Media.Pen.StartLineCap%2A>, and <xref:System.Windows.Media.Pen.EndLineCap%2A>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="22268-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="22268-106">Example</span></span>  
 <span data-ttu-id="22268-107">Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.Pen> , um eine durch eine definierte Form zu gliedern <xref:System.Windows.Media.GeometryDrawing> .</span><span class="sxs-lookup"><span data-stu-id="22268-107">The following example uses a <xref:System.Windows.Media.Pen> to outline a shape defined by a <xref:System.Windows.Media.GeometryDrawing>.</span></span>  
  
 [!code-csharp[PenExamples_snip#PenExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PenExamples_snip/CSharp/PenExample.cs#penexamplewholepage)]
 [!code-vb[PenExamples_snip#PenExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PenExamples_snip/VisualBasic/PenExample.vb#penexamplewholepage)]  
  
 <span data-ttu-id="22268-108">![Mit einem Stift erstellte Konturen](./media/graphicsmm-simple-pen.jpg "graphicsmm_simple_pen")</span><span class="sxs-lookup"><span data-stu-id="22268-108">![Outlines produces by a Pen](./media/graphicsmm-simple-pen.jpg "graphicsmm_simple_pen")</span></span>  
<span data-ttu-id="22268-109">Eine GeometryDrawing</span><span class="sxs-lookup"><span data-stu-id="22268-109">A GeometryDrawing</span></span>
