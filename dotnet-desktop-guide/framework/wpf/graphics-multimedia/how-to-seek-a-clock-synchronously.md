---
title: 'Gewusst wie: Synchrones Suchen einer Uhr'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- clocks [WPF], seeking synchronously
- seeking clocks synchronously [WPF]
ms.assetid: e5b7529b-b7d0-40d2-9e1d-fa4b5e736e96
ms.openlocfilehash: 9b6b1f5523effc56ccd9ddaa4f478e1d3a20ada8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976185"
---
# <a name="how-to-seek-a-clock-synchronously"></a>Gewusst wie: Synchrones Suchen einer Uhr
Verwenden Sie die- <xref:System.Windows.Media.Animation.ClockController.SeekAlignedToLastTick%2A> Methode, um eine Uhr synchron zu einem bestimmten Punkt zu suchen. Im folgenden Beispiel werden sowohl die <xref:System.Windows.Media.Animation.ClockController.Seek%2A> -Methode als auch die- <xref:System.Windows.Media.Animation.ClockController.SeekAlignedToLastTick%2A> Methode eines veranschaulicht <xref:System.Windows.Media.Animation.ClockController> .  
  
 In diesem Beispiel wird gezeigt, wie eine gesucht <xref:System.Windows.Media.Animation.Clock> wird. ein Beispiel für die Suche nach einem Storyboard finden Sie unter [Synchrones Suchen eines Storyboards](how-to-seek-a-storyboard-synchronously.md) .  
  
## <a name="example"></a>Beispiel  
 [!code-csharp[ClockController_procedural_snip#ClockControllerSeekExample](~/samples/snippets/csharp/VS_Snippets_Wpf/ClockController_procedural_snip/CSharp/SeekAlignedToLastTickExample.cs#clockcontrollerseekexample)]
 [!code-vb[ClockController_procedural_snip#ClockControllerSeekExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ClockController_procedural_snip/visualbasic/seekalignedtolasttickexample.vb#clockcontrollerseekexample)]
