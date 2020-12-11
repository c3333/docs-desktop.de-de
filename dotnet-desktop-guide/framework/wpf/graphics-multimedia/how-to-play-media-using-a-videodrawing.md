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
# <a name="how-to-play-media-using-a-videodrawing"></a><span data-ttu-id="f7fc5-102">Gewusst wie: Wiedergeben von Medien mit einer VideoDrawing</span><span class="sxs-lookup"><span data-stu-id="f7fc5-102">How to: Play Media using a VideoDrawing</span></span>
<span data-ttu-id="f7fc5-103">Um eine Audiodatei oder Videodatei wiederzugeben, verwenden Sie eine <xref:System.Windows.Media.VideoDrawing> und eine <xref:System.Windows.Media.MediaPlayer> .</span><span class="sxs-lookup"><span data-stu-id="f7fc5-103">To play an audio or video file, you use a <xref:System.Windows.Media.VideoDrawing> and a <xref:System.Windows.Media.MediaPlayer>.</span></span> <span data-ttu-id="f7fc5-104">Es gibt zwei Methoden zum Laden und Wiedergeben von Medien.</span><span class="sxs-lookup"><span data-stu-id="f7fc5-104">There are two ways to load and play media.</span></span> <span data-ttu-id="f7fc5-105">Der erste besteht darin, ein <xref:System.Windows.Media.MediaPlayer> und ein eigenständig zu verwenden <xref:System.Windows.Media.VideoDrawing> , und die zweite Möglichkeit besteht darin, einen eigenen <xref:System.Windows.Media.MediaTimeline> zu erstellen, der mit und verwendet werden kann <xref:System.Windows.Media.MediaPlayer> <xref:System.Windows.Media.VideoDrawing> .</span><span class="sxs-lookup"><span data-stu-id="f7fc5-105">The first is to use a <xref:System.Windows.Media.MediaPlayer> and a <xref:System.Windows.Media.VideoDrawing> by themselves, and the second way is to create your own <xref:System.Windows.Media.MediaTimeline> to use with the <xref:System.Windows.Media.MediaPlayer> and <xref:System.Windows.Media.VideoDrawing>.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="f7fc5-106">Wenn Sie Medien mit Ihrer Anwendung verteilen, können Sie keine Mediendatei als Ressource verwenden, wie Sie das mit einem Bild machen würden.</span><span class="sxs-lookup"><span data-stu-id="f7fc5-106">When distributing media with your application, you cannot use a media file as a project resource, like you would an image.</span></span> <span data-ttu-id="f7fc5-107">In der Projektdatei müssen Sie stattdessen den Medientyp auf `Content` festlegen, und `CopyToOutputDirectory` auf `PreserveNewest` oder `Always`.</span><span class="sxs-lookup"><span data-stu-id="f7fc5-107">In your project file, you must instead set the media type to `Content` and set `CopyToOutputDirectory` to `PreserveNewest` or `Always`.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f7fc5-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7fc5-108">Example</span></span>  
 <span data-ttu-id="f7fc5-109">Im folgenden Beispiel wird ein <xref:System.Windows.Media.VideoDrawing> und ein verwendet <xref:System.Windows.Media.MediaPlayer> , um eine Videodatei einmal wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="f7fc5-109">The following example uses a <xref:System.Windows.Media.VideoDrawing> and a <xref:System.Windows.Media.MediaPlayer> to play a video file once.</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#VideoDrawingExampleInline](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/VideoDrawingExample.cs#videodrawingexampleinline)]  
  
 <span data-ttu-id="f7fc5-110">Verwenden Sie ein <xref:System.Windows.Media.MediaTimeline> <xref:System.Windows.Media.MediaPlayer> -Objekt mit dem-Objekt und dem-Objekt, um zusätzliche zeitliche Steuerung des Mediums zu erhalten <xref:System.Windows.Media.VideoDrawing> .</span><span class="sxs-lookup"><span data-stu-id="f7fc5-110">To gain additional timing control over the media, use a <xref:System.Windows.Media.MediaTimeline> with the <xref:System.Windows.Media.MediaPlayer> and <xref:System.Windows.Media.VideoDrawing> objects.</span></span> <span data-ttu-id="f7fc5-111"><xref:System.Windows.Media.MediaTimeline>Mit können Sie angeben, ob das Video wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7fc5-111">The <xref:System.Windows.Media.MediaTimeline> enables you to specify whether the video should repeat.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f7fc5-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7fc5-112">Example</span></span>  
 <span data-ttu-id="f7fc5-113">Im folgenden Beispiel wird ein <xref:System.Windows.Media.MediaTimeline> <xref:System.Windows.Media.MediaPlayer> -Objekt mit dem-Objekt und dem- <xref:System.Windows.Media.VideoDrawing> Objekt verwendet, um ein Video wiederholt</span><span class="sxs-lookup"><span data-stu-id="f7fc5-113">The following example uses a <xref:System.Windows.Media.MediaTimeline> with the <xref:System.Windows.Media.MediaPlayer> and <xref:System.Windows.Media.VideoDrawing> objects to play a video repeatedly.</span></span>  
  
 [!code-csharp[DrawingMiscSnippets_snip#RepeatingVideoDrawingExampleInline](~/samples/snippets/csharp/VS_Snippets_Wpf/DrawingMiscSnippets_snip/CSharp/VideoDrawingExample.cs#repeatingvideodrawingexampleinline)]  
  
 <span data-ttu-id="f7fc5-114">Beachten Sie, dass Sie, wenn Sie einen verwenden <xref:System.Windows.Media.MediaTimeline> , die <xref:System.Windows.Media.Animation.ClockController> von der-Eigenschaft von zurückgegebene interaktive verwenden, <xref:System.Windows.Media.Animation.Clock.Controller%2A> <xref:System.Windows.Media.MediaClock> um die Medienwiedergabe anstelle der interaktiven Methoden von zu steuern <xref:System.Windows.Media.MediaPlayer> .</span><span class="sxs-lookup"><span data-stu-id="f7fc5-114">Note that, when you use a <xref:System.Windows.Media.MediaTimeline>, you use the interactive <xref:System.Windows.Media.Animation.ClockController> returned from the <xref:System.Windows.Media.Animation.Clock.Controller%2A> property of the <xref:System.Windows.Media.MediaClock> to control media playback instead of the interactive methods of <xref:System.Windows.Media.MediaPlayer>.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f7fc5-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7fc5-115">See also</span></span>

- <xref:System.Windows.Media.VideoDrawing>
- [<span data-ttu-id="f7fc5-116">Übersicht über Zeichnungsobjekte</span><span class="sxs-lookup"><span data-stu-id="f7fc5-116">Drawing Objects Overview</span></span>](drawing-objects-overview.md)
