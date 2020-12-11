---
title: 'Gewusst wie: Auslösen einer Animation bei Änderung eines Eigenschaftswerts'
ms.date: 03/30/2017
helpviewer_keywords:
- animation [WPF], starting when property values change
- triggering animation [WPF]
- Storyboards [WPF], starting when property values change
ms.assetid: 12399c21-0300-4f4f-9e3a-d92d9907e5f5
ms.openlocfilehash: 7e3eecedf7d464eeb8e4f60f2f05fa06d2e23e09
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977604"
---
# <a name="how-to-trigger-an-animation-when-a-property-value-changes"></a>Gewusst wie: Auslösen einer Animation bei Änderung eines Eigenschaftswerts
Dieses Beispiel zeigt, wie ein verwendet wird <xref:System.Windows.Trigger> , um eine zu starten, <xref:System.Windows.Media.Animation.Storyboard> Wenn sich ein Eigenschafts Wert ändert. Sie können eine <xref:System.Windows.Trigger> innerhalb von <xref:System.Windows.Style> , oder verwenden <xref:System.Windows.Controls.ControlTemplate> <xref:System.Windows.DataTemplate> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein- <xref:System.Windows.Trigger> Objekt verwendet, um den eines zu animieren, <xref:System.Windows.UIElement.Opacity%2A> <xref:System.Windows.Controls.Button> wenn seine- <xref:System.Windows.UIElement.IsMouseOver%2A> Eigenschaft zu wird `true` .  
  
 [!code-xaml[AnimatePropertyStoryboards#PropertyTriggerExample](~/samples/snippets/xaml/VS_Snippets_Wpf/AnimatePropertyStoryboards/XAML/PropertyTriggerExample.xaml#propertytriggerexample)]  
  
 Durch Eigenschafts Objekte angewendete Animationen <xref:System.Windows.Trigger> Verhalten sich komplexer als <xref:System.Windows.EventTrigger> Animationen oder Animationen, die mithilfe von Methoden gestartet wurden <xref:System.Windows.Media.Animation.Storyboard> .  Sie "Handoff" mit Animationen, die von anderen <xref:System.Windows.Trigger> Objekten definiert werden, verfassen jedoch mit <xref:System.Windows.EventTrigger> und durch Methoden ausgelöste Animationen.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Trigger>
- [Übersicht über die Verfahren zur Animation von Eigenschaften](property-animation-techniques-overview.md)
- [Übersicht über Storyboards](storyboards-overview.md)
