---
title: 'Gewusst wie: Definieren eines Namensbereichs'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- name scope [WPF], defining
- Storyboards [WPF], animating in procedural code
- animation [WPF], Storyboards [WPF], in procedural code
ms.assetid: 4f361925-6a08-40dc-8231-a61111c6b28b
ms.openlocfilehash: a03f477dd31909e8cb9dde9cd29da6f38d665758
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972424"
---
# <a name="how-to-define-a-name-scope"></a><span data-ttu-id="62d4a-102">Gewusst wie: Definieren eines Namensbereichs</span><span class="sxs-lookup"><span data-stu-id="62d4a-102">How to: Define a Name Scope</span></span>
<span data-ttu-id="62d4a-103">Um mit <xref:System.Windows.Media.Animation.Storyboard> im Code zu animieren, müssen Sie einen erstellen <xref:System.Windows.NameScope> und die Namen der Zielobjekte mit dem Element registrieren, das diesen namens Bereich besitzt.</span><span class="sxs-lookup"><span data-stu-id="62d4a-103">To animate with <xref:System.Windows.Media.Animation.Storyboard> in code, you must create a <xref:System.Windows.NameScope> and register the target objects' names with the element that owns that name scope.</span></span> <span data-ttu-id="62d4a-104">Im folgenden Beispiel <xref:System.Windows.NameScope> wird ein für erstellt `myMainPanel` .</span><span class="sxs-lookup"><span data-stu-id="62d4a-104">In the following example, a <xref:System.Windows.NameScope> is created for `myMainPanel`.</span></span> <span data-ttu-id="62d4a-105">Zwei Schaltflächen, `button1` und `button2` , werden dem Panel hinzugefügt, und ihre Namen werden registriert.</span><span class="sxs-lookup"><span data-stu-id="62d4a-105">Two buttons, `button1` and `button2`, are added to the panel, and their names registered.</span></span> <span data-ttu-id="62d4a-106">Es werden mehrere Animationen und eine <xref:System.Windows.Media.Animation.Storyboard> erstellt.</span><span class="sxs-lookup"><span data-stu-id="62d4a-106">Several animations and a <xref:System.Windows.Media.Animation.Storyboard> are created.</span></span> <span data-ttu-id="62d4a-107">Die-Methode des Storyboards <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> wird zum Starten der Animationen verwendet.</span><span class="sxs-lookup"><span data-stu-id="62d4a-107">The storyboard's <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> method is used to start the animations.</span></span>  
  
 <span data-ttu-id="62d4a-108">Da `button1` , `button2` und `myMainPanel` alle denselben namens Bereich aufweisen, kann jeder von Ihnen mit der- <xref:System.Windows.Media.Animation.Storyboard> <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> Methode zum Starten der Animationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62d4a-108">Because `button1`, `button2`, and `myMainPanel` all share the same name scope, any one of them can be used with the <xref:System.Windows.Media.Animation.Storyboard> <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> method to start the animations.</span></span>  
  
## <a name="example"></a><span data-ttu-id="62d4a-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="62d4a-109">Example</span></span>  
 [!code-csharp[StoryboardBeginAnimation_procedural_snip#NameScopeExample](~/samples/snippets/csharp/VS_Snippets_Wpf/StoryboardBeginAnimation_procedural_snip/CSharp/ScopeExample.cs#namescopeexample)]
 [!code-vb[StoryboardBeginAnimation_procedural_snip#NameScopeExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/StoryboardBeginAnimation_procedural_snip/visualbasic/scopeexample.vb#namescopeexample)]  
  
## <a name="see-also"></a><span data-ttu-id="62d4a-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62d4a-110">See also</span></span>

- [<span data-ttu-id="62d4a-111">Animieren einer Eigenschaft unter Verwendung eines Storyboards</span><span class="sxs-lookup"><span data-stu-id="62d4a-111">Animate a Property by Using a Storyboard</span></span>](how-to-animate-a-property-by-using-a-storyboard.md)
- [<span data-ttu-id="62d4a-112">Übersicht über Animationen</span><span class="sxs-lookup"><span data-stu-id="62d4a-112">Animation Overview</span></span>](animation-overview.md)
