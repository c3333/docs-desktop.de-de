---
title: 'Gewusst wie: Wiedergeben von Medien mit Animationen'
ms.date: 03/30/2017
helpviewer_keywords:
- multimedia [WPF], playback with animations
- playback of media [WPF], with animations
- animation [WPF], media playback with
- media [WPF], playback with animations
ms.assetid: 8982b7b7-1c6c-4b24-8801-b328862975f5
ms.openlocfilehash: 200f9d62c67a02088fe5a5789cdb41a04837d430
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975314"
---
# <a name="how-to-play-media-with-animations"></a>Gewusst wie: Wiedergeben von Medien mit Animationen
Dieses Beispiel zeigt, wie Sie Medien und Animationen gleichzeitig mit der <xref:System.Windows.Media.MediaTimeline> -Klasse und der- <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames> Klasse in derselben wiedergeben können <xref:System.Windows.Media.Animation.Storyboard> .  
  
## <a name="example"></a>Beispiel  
 Sie können ein oder mehrere- <xref:System.Windows.Media.MediaTimeline> Objekte in einem-Objekt <xref:System.Windows.Media.Animation.Storyboard> und andere- <xref:System.Windows.Media.Animation.Timeline> Objekte verwenden, z. b. Animationen.  
  
 Im folgenden Beispiel wird die- <xref:System.Windows.Media.Animation.ParallelTimeline.SlipBehavior%2A> Eigenschaft von <xref:System.Windows.Media.Animation.Storyboard> auf den Wert festgelegt, der `Slip` angibt, dass die Animation nicht fortgesetzt wird, bis das Medium (in diesem Beispiel Video) ausgeführt wird. Diese Funktionalität ist hilfreich, wenn die Wiedergabe von Medien auf Grund ihrer Ladezeit verzögert wird.  
  
 [!code-xaml[MediaGallery_snippet#MediaTimelinePlusAnimationExampleWholePage](~/samples/snippets/csharp/VS_Snippets_Wpf/MediaGallery_snippet/CSharp/MediaTimelinePlusAnimationExample.xaml#mediatimelineplusanimationexamplewholepage)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.MediaTimeline>
- <xref:System.Windows.Media.Animation.DoubleAnimationUsingKeyFrames>
- <xref:System.Windows.Media.Animation.Storyboard>
- <xref:System.Windows.Media.Animation.ParallelTimeline.SlipBehavior%2A>
- [Artikel zu Vorgehensweisen](audio-and-video-how-to-topics.md)
- [Übersicht über Storyboards](storyboards-overview.md)
- [Übersicht über Keyframe-Animationen](key-frame-animations-overview.md)
- [Übersicht über Animationen](animation-overview.md)
- [Grafiken und Multimedia](index.md)
