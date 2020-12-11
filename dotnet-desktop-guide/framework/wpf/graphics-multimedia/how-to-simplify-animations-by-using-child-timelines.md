---
title: 'Gewusst wie: Vereinfachen von Animationen durch untergeordnete Timeline-Objekte'
ms.date: 03/30/2017
helpviewer_keywords:
- simplifying animations by child timelines [WPF]
- animation [WPF], simplifying by child timelines
- child timelines [WPF]
ms.assetid: 8335d770-d13d-42bd-8dfa-63f92c0327e2
ms.openlocfilehash: 21a297208be045eea79d6f5ca6c8eac016d26345
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975473"
---
# <a name="how-to-simplify-animations-by-using-child-timelines"></a>Gewusst wie: Vereinfachen von Animationen durch untergeordnete Timeline-Objekte
In diesem Beispiel wird gezeigt, wie Animationen mithilfe von untergeordneten Objekten vereinfacht werden <xref:System.Windows.Media.Animation.ParallelTimeline> . Ein <xref:System.Windows.Media.Animation.Storyboard> ist ein Typ von <xref:System.Windows.Media.Animation.Timeline> , der Ziel Informationen für die in ihm enthaltenen Zeitachsen bereitstellt. Verwenden <xref:System.Windows.Media.Animation.Storyboard> Sie, um Zeitachsen-Ziel Informationen bereitzustellen, einschließlich Objekt-und Eigenschafts Informationen.  
  
 Verwenden Sie ein oder mehrere-Objekte als untergeordnete Elemente eines, um eine Animation zu starten <xref:System.Windows.Media.Animation.ParallelTimeline> <xref:System.Windows.Media.Animation.Storyboard> . Diese <xref:System.Windows.Media.Animation.ParallelTimeline> Objekte können andere Animationen enthalten und können daher die Zeit Steuerungs Sequenzen in komplexen Animationen besser Kapseln. Wenn Sie z. b. eine <xref:System.Windows.Controls.TextBlock> und mehrere Formen in der gleichen Animation erstellen <xref:System.Windows.Media.Animation.Storyboard> , können Sie die Animationen für die <xref:System.Windows.Controls.TextBlock> -und die-Formen voneinander trennen, indem Sie Sie in einen separaten einfügen <xref:System.Windows.Media.Animation.ParallelTimeline> . Da jede über <xref:System.Windows.Media.Animation.ParallelTimeline> eigene <xref:System.Windows.Media.Animation.Timeline.BeginTime%2A> und alle untergeordneten Elemente des <xref:System.Windows.Media.Animation.ParallelTimeline> anfangs relativ zu diesem verfügt <xref:System.Windows.Media.Animation.Timeline.BeginTime%2A> , ist die zeitliche Steuerung besser gekapselt.  
  
 Im folgenden Beispiel werden zwei Textabschnitte (- <xref:System.Windows.Controls.TextBlock> Objekte) von innerhalb desselben animiert <xref:System.Windows.Media.Animation.Storyboard> . Ein <xref:System.Windows.Media.Animation.ParallelTimeline> kapselt die Animationen von einem der- <xref:System.Windows.Controls.TextBlock> Objekte.  
  
 **Leistungs Hinweis:** Obwohl Sie Zeitachsen ineinander schachteln können <xref:System.Windows.Media.Animation.Storyboard> , <xref:System.Windows.Media.Animation.ParallelTimeline> sind die e für die Schachtelung besser geeignet, da Sie weniger Aufwand erfordern. (Die <xref:System.Windows.Media.Animation.Storyboard> Klasse erbt von der- <xref:System.Windows.Media.Animation.ParallelTimeline> Klasse.)  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[Timelines_snip#ParallelTimelineWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/Timelines_snip/CS/ParallelTimelineExample.xaml#paralleltimelinewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Animationen](animation-overview.md)
- [Angeben der HandoffBehavior-Enumeration zwischen Storyboard-Animationen](how-to-specify-handoffbehavior-between-storyboard-animations.md)
