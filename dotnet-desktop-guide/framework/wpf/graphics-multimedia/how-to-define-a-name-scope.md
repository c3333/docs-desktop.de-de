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
# <a name="how-to-define-a-name-scope"></a>Gewusst wie: Definieren eines Namensbereichs
Um mit <xref:System.Windows.Media.Animation.Storyboard> im Code zu animieren, müssen Sie einen erstellen <xref:System.Windows.NameScope> und die Namen der Zielobjekte mit dem Element registrieren, das diesen namens Bereich besitzt. Im folgenden Beispiel <xref:System.Windows.NameScope> wird ein für erstellt `myMainPanel` . Zwei Schaltflächen, `button1` und `button2` , werden dem Panel hinzugefügt, und ihre Namen werden registriert. Es werden mehrere Animationen und eine <xref:System.Windows.Media.Animation.Storyboard> erstellt. Die-Methode des Storyboards <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> wird zum Starten der Animationen verwendet.  
  
 Da `button1` , `button2` und `myMainPanel` alle denselben namens Bereich aufweisen, kann jeder von Ihnen mit der- <xref:System.Windows.Media.Animation.Storyboard> <xref:System.Windows.Media.Animation.Storyboard.Begin%2A> Methode zum Starten der Animationen verwendet werden.  
  
## <a name="example"></a>Beispiel  
 [!code-csharp[StoryboardBeginAnimation_procedural_snip#NameScopeExample](~/samples/snippets/csharp/VS_Snippets_Wpf/StoryboardBeginAnimation_procedural_snip/CSharp/ScopeExample.cs#namescopeexample)]
 [!code-vb[StoryboardBeginAnimation_procedural_snip#NameScopeExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/StoryboardBeginAnimation_procedural_snip/visualbasic/scopeexample.vb#namescopeexample)]  
  
## <a name="see-also"></a>Siehe auch

- [Animieren einer Eigenschaft unter Verwendung eines Storyboards](how-to-animate-a-property-by-using-a-storyboard.md)
- [Übersicht über Animationen](animation-overview.md)
