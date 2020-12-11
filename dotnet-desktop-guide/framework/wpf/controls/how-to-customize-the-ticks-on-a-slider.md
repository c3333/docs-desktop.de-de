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
# <a name="how-to-customize-the-ticks-on-a-slider"></a><span data-ttu-id="c9c5e-102">Gewusst wie: Anpassen der Teilstriche auf einem Schieberegler</span><span class="sxs-lookup"><span data-stu-id="c9c5e-102">How to: Customize the Ticks on a Slider</span></span>

<span data-ttu-id="c9c5e-103">In diesem Beispiel wird gezeigt, wie ein Steuerelement mit Teil Strichen erstellt wird <xref:System.Windows.Controls.Slider> .</span><span class="sxs-lookup"><span data-stu-id="c9c5e-103">This example shows how to create a <xref:System.Windows.Controls.Slider> control that has tick marks.</span></span>  
  
## <a name="example"></a><span data-ttu-id="c9c5e-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c9c5e-104">Example</span></span>  

 <span data-ttu-id="c9c5e-105">Der <xref:System.Windows.Controls.Primitives.TickBar> wird angezeigt, wenn Sie die- <xref:System.Windows.Controls.Slider.TickPlacement%2A> Eigenschaft auf einen anderen Wert als festlegen <xref:System.Windows.Controls.Primitives.TickPlacement.None> , d. h. auf den Standardwert.</span><span class="sxs-lookup"><span data-stu-id="c9c5e-105">The <xref:System.Windows.Controls.Primitives.TickBar> displays when you set the <xref:System.Windows.Controls.Slider.TickPlacement%2A> property to a value other than <xref:System.Windows.Controls.Primitives.TickPlacement.None>, which is the default value.</span></span>  
  
 <span data-ttu-id="c9c5e-106">Im folgenden Beispiel wird gezeigt, wie ein mit einem erstellt wird, in dem Teil Striche <xref:System.Windows.Controls.Slider> <xref:System.Windows.Controls.Primitives.TickBar> angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c9c5e-106">The following example shows how to create a <xref:System.Windows.Controls.Slider> with a <xref:System.Windows.Controls.Primitives.TickBar> that displays tick marks.</span></span> <span data-ttu-id="c9c5e-107">Die <xref:System.Windows.Controls.Slider.TickPlacement%2A> <xref:System.Windows.Controls.Slider.TickFrequency%2A> Eigenschaften und definieren die Position der Teil Striche und das Intervall zwischen Ihnen.</span><span class="sxs-lookup"><span data-stu-id="c9c5e-107">The <xref:System.Windows.Controls.Slider.TickPlacement%2A> and <xref:System.Windows.Controls.Slider.TickFrequency%2A> properties define the location of the tick marks and the interval between them.</span></span> <span data-ttu-id="c9c5e-108">Wenn Sie den verschieben <xref:System.Windows.Controls.Primitives.Thumb> , zeigen Quick Infos den Wert von an <xref:System.Windows.Controls.Slider> .</span><span class="sxs-lookup"><span data-stu-id="c9c5e-108">When you move the <xref:System.Windows.Controls.Primitives.Thumb>, tooltips display the value of the <xref:System.Windows.Controls.Slider>.</span></span> <span data-ttu-id="c9c5e-109">Die- <xref:System.Windows.Controls.Slider.AutoToolTipPlacement%2A> Eigenschaft definiert, wo die Quick Infos auftreten.</span><span class="sxs-lookup"><span data-stu-id="c9c5e-109">The <xref:System.Windows.Controls.Slider.AutoToolTipPlacement%2A> property defines where the tooltips occur.</span></span> <span data-ttu-id="c9c5e-110">Die <xref:System.Windows.Controls.Primitives.Thumb> Bewegungen entsprechen der Position der Teil Striche, da <xref:System.Windows.Controls.Slider.IsSnapToTickEnabled%2A> auf festgelegt ist `true` .</span><span class="sxs-lookup"><span data-stu-id="c9c5e-110">The <xref:System.Windows.Controls.Primitives.Thumb> movements correspond to the location of the tick marks because <xref:System.Windows.Controls.Slider.IsSnapToTickEnabled%2A> is set to `true`.</span></span>  
  
 <span data-ttu-id="c9c5e-111">Im folgenden Beispiel wird gezeigt, wie die- <xref:System.Windows.Controls.Slider.Ticks%2A> Eigenschaft zum Erstellen von Teil Strichen entlang der <xref:System.Windows.Controls.Slider> in unregelmäßigen Intervallen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c9c5e-111">The following example shows how to use the <xref:System.Windows.Controls.Slider.Ticks%2A> property to create tick marks along the <xref:System.Windows.Controls.Slider> at irregular intervals.</span></span>  
  
 [!code-xaml[Slider#4](~/samples/snippets/xaml/VS_Snippets_Wpf/Slider/xaml/window1.xaml#4)]  
  
## <a name="see-also"></a><span data-ttu-id="c9c5e-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9c5e-112">See also</span></span>

- <xref:System.Windows.Controls.Slider>
- <xref:System.Windows.Controls.Primitives.TickBar>
- <xref:System.Windows.Controls.Slider.TickPlacement%2A>
- <span data-ttu-id="c9c5e-113">[Gewusst wie: Binden eines Schiebereglers an einen Eigenschafts Wert](/previous-versions/dotnet/netframework-3.5/ms788716(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="c9c5e-113">[How to: Bind a Slider to a Property Value](/previous-versions/dotnet/netframework-3.5/ms788716(v=vs.90))</span></span>
