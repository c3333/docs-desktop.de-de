---
title: 'Gewusst wie: Überschreiben der logischen Struktur'
ms.date: 03/30/2017
helpviewer_keywords:
- overriding the logical tree [WPF]
- logical tree [WPF], overriding
ms.assetid: 0ae4d074-8113-4b06-b4fa-e0f39d4967a6
ms.openlocfilehash: bf3459fff1a90326794d6713dd39c73596b0e960
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977751"
---
# <a name="how-to-override-the-logical-tree"></a><span data-ttu-id="bec48-102">Gewusst wie: Überschreiben der logischen Struktur</span><span class="sxs-lookup"><span data-stu-id="bec48-102">How to: Override the Logical Tree</span></span>
<span data-ttu-id="bec48-103">Obwohl es in den meisten Fällen nicht erforderlich ist, können erfahrene Autoren von Steuerelementen in der logischen Struktur überschreiben.</span><span class="sxs-lookup"><span data-stu-id="bec48-103">Although it is not necessary in most cases, advanced control authors have the option to override the logical tree.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bec48-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bec48-104">Example</span></span>  
 <span data-ttu-id="bec48-105">In diesem Beispiel wird beschrieben, wie die Unterklasse zum über <xref:System.Windows.Controls.StackPanel> Schreiben der logischen Struktur verwendet wird, in diesem Fall, um ein Verhalten zu erzwingen, dass der Bereich möglicherweise nur über ein einzelnes untergeordnetes Element verfügt.</span><span class="sxs-lookup"><span data-stu-id="bec48-105">This example describes how to subclass <xref:System.Windows.Controls.StackPanel> to override the logical tree, in this case to enforce a behavior that the panel may only have and will only render a single child element.</span></span> <span data-ttu-id="bec48-106">Dieses Verhalten ist nicht unbedingt praktisch und erwünscht, aber es dient hier zur Veranschaulichung des Szenarios zum Überschreiben der normalen logischen Struktur eines Elements.</span><span class="sxs-lookup"><span data-stu-id="bec48-106">This isn't necessarily a practically desirable behavior, but is shown here as a means of illustrating the scenario for overriding an element's normal logical tree.</span></span>  
  
 [!code-csharp[LogicalOverride#SingletonPanel](~/samples/snippets/csharp/VS_Snippets_Wpf/LogicalOverride/CSharp/SDKSampleLibrary/class1.cs#singletonpanel)]  
  
 <span data-ttu-id="bec48-107">Weitere Informationen zu der logischen Struktur finden Sie unter [Strukturen in WPF](trees-in-wpf.md).</span><span class="sxs-lookup"><span data-stu-id="bec48-107">For more information on the logical tree, see [Trees in WPF](trees-in-wpf.md).</span></span>
