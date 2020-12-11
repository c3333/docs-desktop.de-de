---
title: Animieren in einem Stil
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], properties [WPF], within styles
- styles [WPF], animating properties within
ms.assetid: 6a791f3d-6b1f-4972-a2f9-35880bcfd954
ms.openlocfilehash: 82a1406f180de26a48808f7a094a8addab29a042
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977927"
---
# <a name="how-to-animate-in-a-style"></a>Animieren in einem Stil

Dieses Beispiel zeigt, wie Eigenschaften innerhalb eines Stils animiert werden. Bei der Animation innerhalb eines Stils kann nur das Framework-Element, für das der Stil definiert ist, direkt als Ziel festgelegt werden. Um ein frei wählbares Objekt als Ziel festzulegen, müssen Sie einen "punktdown" von einer Eigenschaft des formatierten Elements durchsetzen.

Im folgenden Beispiel werden mehrere Animationen innerhalb eines Stils definiert und auf einen angewendet <xref:System.Windows.Controls.Button> . Wenn der Benutzer den Mauszeiger über die Schaltfläche bewegt, wird er wiederholt von der nicht transparenten zur teilweise durchlässigen und wieder zurückgeführt. Wenn der Benutzer den Mauszeiger aus der Schaltfläche bewegt, wird er vollständig nicht transparent. Wenn auf die Schaltfläche geklickt wird, ändert sich die Hintergrundfarbe von Orange in weiß und wieder zurück. Da der <xref:System.Windows.Media.SolidColorBrush> , der zum Zeichnen der Schaltfläche verwendet wird, nicht direkt als Ziel verwendet werden kann, erfolgt der Zugriff durch doup aus der-Eigenschaft der Schaltfläche <xref:System.Windows.Controls.Control.Background%2A> .

## <a name="example"></a>Beispiel

[!code-xaml[timingbehaviors_snip#21](~/samples/snippets/csharp/VS_Snippets_Wpf/timingbehaviors_snip/CSharp/StyleStoryboardsExample.xaml#21)]

Beachten Sie, dass es bei der Animation innerhalb eines Stils möglich ist, Objekte zu erstellen, die nicht vorhanden sind. Angenommen, Ihr Stil verwendet einen, <xref:System.Windows.Media.SolidColorBrush> um die Background-Eigenschaft einer Schaltfläche festzulegen, aber an einem bestimmten Punkt wird der Stil überschrieben, und der Hintergrund der Schaltfläche wird mit einem festgelegt <xref:System.Windows.Media.LinearGradientBrush> .  Wenn Sie versuchen, den zu animieren <xref:System.Windows.Media.SolidColorBrush> , wird keine Ausnahme ausgelöst. die Animation wird einfach im Hintergrund fehlschlagen.

Weitere Informationen zur Syntax der Storyboard-Zielplattform finden Sie in der [Übersicht über Storyboards](storyboards-overview.md). Weitere Informationen zur Animation finden Sie unter [Übersicht über Animationen](animation-overview.md). Weitere Informationen zu Stilen finden Sie unter [formatieren und](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)Vorlagen.
