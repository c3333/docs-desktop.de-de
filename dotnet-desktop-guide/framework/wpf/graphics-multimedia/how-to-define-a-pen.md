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
# <a name="how-to-define-a-pen"></a>Gewusst wie: Definieren eines Stifts
In diesem Beispiel wird gezeigt, wie eine Form mit einem <xref:System.Windows.Media.Pen> Umriss wird. Zum Erstellen eines einfachen <xref:System.Windows.Media.Pen> müssen Sie nur sein und angeben <xref:System.Windows.Media.Pen.Thickness%2A> <xref:System.Windows.Media.Pen.Brush%2A> . Sie können komplexere Pen erstellen, indem Sie <xref:System.Windows.Media.Pen.DashStyle%2A> , <xref:System.Windows.Media.Pen.DashCap%2A> , <xref:System.Windows.Media.Pen.LineJoin%2A> , und angeben <xref:System.Windows.Media.Pen.StartLineCap%2A> <xref:System.Windows.Media.Pen.EndLineCap%2A> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein verwendet <xref:System.Windows.Media.Pen> , um eine durch eine definierte Form zu gliedern <xref:System.Windows.Media.GeometryDrawing> .  
  
 [!code-csharp[PenExamples_snip#PenExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/PenExamples_snip/CSharp/PenExample.cs#penexamplewholepage)]
 [!code-vb[PenExamples_snip#PenExampleWholePage](~/samples/snippets/visualbasic/VS_Snippets_Wpf/PenExamples_snip/VisualBasic/PenExample.vb#penexamplewholepage)]  
  
 ![Mit einem Stift erstellte Konturen](./media/graphicsmm-simple-pen.jpg "graphicsmm_simple_pen")  
Eine GeometryDrawing
