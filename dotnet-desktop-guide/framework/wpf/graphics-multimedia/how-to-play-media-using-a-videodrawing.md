---
title: 'Gewusst wie: Wiedergeben von Medien mit einer VideoDrawing'
ms.date: 03/30/2017
helpviewer_keywords:
- playback of media [WPF]
- classes [WPF], MediaPlayer
ms.assetid: 165d47ed-22ce-4ded-aa6a-aa9b7467de87
ms.openlocfilehash: 2e2007525be770186a17cf9d2d42a7c52ba93fba
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977112"
---
# <a name="how-to-play-media-using-a-videodrawing"></a>Gewusst wie: Wiedergeben von Medien mit einer VideoDrawing
Um eine Audiodatei oder Videodatei wiederzugeben, verwenden Sie eine <xref:System.Windows.Media.VideoDrawing> und eine <xref:System.Windows.Media.MediaPlayer> . Es gibt zwei Methoden zum Laden und Wiedergeben von Medien. Der erste besteht darin, ein <xref:System.Windows.Media.MediaPlayer> und ein eigenständig zu verwenden <xref:System.Windows.Media.VideoDrawing> , und die zweite Möglichkeit besteht darin, einen eigenen <xref:System.Windows.Media.MediaTimeline> zu erstellen, der mit und verwendet werden kann <xref:System.Windows.Media.MediaPlayer> <xref:System.Windows.Media.VideoDrawing> .  
  
> [!NOTE]
> Wenn Sie Medien mit Ihrer Anwendung verteilen, können Sie keine Mediendatei als Ressource verwenden, wie Sie das mit einem Bild machen würden. In der Projektdatei müssen Sie stattdessen den Medientyp auf `Content` festlegen, und `CopyToOutputDirectory` auf `PreserveNewest` oder `Always`.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein <xref:System.Windows.Media.VideoDrawing> und ein verwendet <xref:System.Windows.Media.MediaPlayer> , um eine Videodatei einmal wiederzugeben.  
  
 [!code-csharp[DrawingMiscSnippets_snip#VideoDrawingExampleInline](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/VideoDrawingExample.cs#videodrawingexampleinline)]  
  
 Verwenden Sie ein <xref:System.Windows.Media.MediaTimeline> <xref:System.Windows.Media.MediaPlayer> -Objekt mit dem-Objekt und dem-Objekt, um zusätzliche zeitliche Steuerung des Mediums zu erhalten <xref:System.Windows.Media.VideoDrawing> . <xref:System.Windows.Media.MediaTimeline>Mit können Sie angeben, ob das Video wiederholt werden soll.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein <xref:System.Windows.Media.MediaTimeline> <xref:System.Windows.Media.MediaPlayer> -Objekt mit dem-Objekt und dem- <xref:System.Windows.Media.VideoDrawing> Objekt verwendet, um ein Video wiederholt  
  
 [!code-csharp[DrawingMiscSnippets_snip#RepeatingVideoDrawingExampleInline](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/VideoDrawingExample.cs#repeatingvideodrawingexampleinline)]  
  
 Beachten Sie, dass Sie, wenn Sie einen verwenden <xref:System.Windows.Media.MediaTimeline> , die <xref:System.Windows.Media.Animation.ClockController> von der-Eigenschaft von zurückgegebene interaktive verwenden, <xref:System.Windows.Media.Animation.Clock.Controller%2A> <xref:System.Windows.Media.MediaClock> um die Medienwiedergabe anstelle der interaktiven Methoden von zu steuern <xref:System.Windows.Media.MediaPlayer> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Media.VideoDrawing>
- [Übersicht über Zeichnungsobjekte](drawing-objects-overview.md)
