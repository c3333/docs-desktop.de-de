---
title: 'Gewusst wie: Anpassen der Teilstriche auf einem Schieberegler'
ms.date: 03/30/2017
helpviewer_keywords:
- TickBar [WPF]
- Slider control [WPF], creating with TickBar
ms.assetid: 4fa694f2-a620-4b15-be78-5f4286f89361
ms.openlocfilehash: 150a546a2c94c1bd552f1f7486652d2b4ad900e3
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977820"
---
# <a name="how-to-customize-the-ticks-on-a-slider"></a>Gewusst wie: Anpassen der Teilstriche auf einem Schieberegler

In diesem Beispiel wird gezeigt, wie ein Steuerelement mit Teil Strichen erstellt wird <xref:System.Windows.Controls.Slider> .  
  
## <a name="example"></a>Beispiel  

 Der <xref:System.Windows.Controls.Primitives.TickBar> wird angezeigt, wenn Sie die- <xref:System.Windows.Controls.Slider.TickPlacement%2A> Eigenschaft auf einen anderen Wert als festlegen <xref:System.Windows.Controls.Primitives.TickPlacement.None> , d. h. auf den Standardwert.  
  
 Im folgenden Beispiel wird gezeigt, wie ein mit einem erstellt wird, in dem Teil Striche <xref:System.Windows.Controls.Slider> <xref:System.Windows.Controls.Primitives.TickBar> angezeigt werden. Die <xref:System.Windows.Controls.Slider.TickPlacement%2A> <xref:System.Windows.Controls.Slider.TickFrequency%2A> Eigenschaften und definieren die Position der Teil Striche und das Intervall zwischen Ihnen. Wenn Sie den verschieben <xref:System.Windows.Controls.Primitives.Thumb> , zeigen Quick Infos den Wert von an <xref:System.Windows.Controls.Slider> . Die- <xref:System.Windows.Controls.Slider.AutoToolTipPlacement%2A> Eigenschaft definiert, wo die Quick Infos auftreten. Die <xref:System.Windows.Controls.Primitives.Thumb> Bewegungen entsprechen der Position der Teil Striche, da <xref:System.Windows.Controls.Slider.IsSnapToTickEnabled%2A> auf festgelegt ist `true` .  
  
 Im folgenden Beispiel wird gezeigt, wie die- <xref:System.Windows.Controls.Slider.Ticks%2A> Eigenschaft zum Erstellen von Teil Strichen entlang der <xref:System.Windows.Controls.Slider> in unregelmäßigen Intervallen verwendet werden kann.  
  
 [!code-xaml[Slider#4](~/samples/snippets/xaml/VS_Snippets_Wpf/Slider/xaml/window1.xaml#4)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Slider>
- <xref:System.Windows.Controls.Primitives.TickBar>
- <xref:System.Windows.Controls.Slider.TickPlacement%2A>
- [Gewusst wie: Binden eines Schiebereglers an einen Eigenschafts Wert](/previous-versions/dotnet/netframework-3.5/ms788716(v=vs.90))
