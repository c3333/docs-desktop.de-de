---
title: Übersicht über die SoundPlayer-Klasse
ms.date: 03/30/2017
helpviewer_keywords:
- playing sounds [Windows Forms], SoundPlayer class
- SoundPlayer class [Windows Forms], about SoundPlayer class
- sounds [Windows Forms], playing
ms.assetid: fcebb938-62b9-4677-9cbe-6465bc863e22
ms.openlocfilehash: 3ff23cbfa78b803d4526e7a7c389fd5d458a967c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977071"
---
# <a name="soundplayer-class-overview"></a><span data-ttu-id="58743-102">Übersicht über die SoundPlayer-Klasse</span><span class="sxs-lookup"><span data-stu-id="58743-102">SoundPlayer Class Overview</span></span>
<span data-ttu-id="58743-103">Die <xref:System.Media.SoundPlayer>-Klasse ermöglicht es Ihnen, Sounds problemlos in Ihre Anwendungen zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="58743-103">The <xref:System.Media.SoundPlayer> class enables you to easily include sounds in your applications.</span></span>  
  
 <span data-ttu-id="58743-104">Die- <xref:System.Media.SoundPlayer> Klasse kann Sounddateien im WAV-Format wiedergeben, entweder von einer Ressource oder von UNC-oder http-Speicherorten.</span><span class="sxs-lookup"><span data-stu-id="58743-104">The <xref:System.Media.SoundPlayer> class can play sound files in the .wav format, either from a resource or from UNC or HTTP locations.</span></span> <span data-ttu-id="58743-105">Außerdem <xref:System.Media.SoundPlayer> können Sie mit der-Klasse Sounds asynchron laden oder abspielen.</span><span class="sxs-lookup"><span data-stu-id="58743-105">Additionally, the <xref:System.Media.SoundPlayer> class enables you to load or play sounds asynchronously.</span></span>  
  
 <span data-ttu-id="58743-106">Sie können auch die <xref:System.Media.SystemSounds>-Klasse verwenden, um allgemeine Systemsounds wiederzugeben, einschließlich eines akustischen Signals.</span><span class="sxs-lookup"><span data-stu-id="58743-106">You can also use the <xref:System.Media.SystemSounds> class to play common system sounds, including a beep.</span></span>  
  
## <a name="commonly-used-properties-methods-and-events"></a><span data-ttu-id="58743-107">Häufig verwendete Eigenschaften, Methoden und Ereignisse</span><span class="sxs-lookup"><span data-stu-id="58743-107">Commonly Used Properties, Methods, and Events</span></span>  
  
|<span data-ttu-id="58743-108">Name</span><span class="sxs-lookup"><span data-stu-id="58743-108">Name</span></span>|<span data-ttu-id="58743-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="58743-109">Description</span></span>|  
|----------|-----------------|  
|<span data-ttu-id="58743-110"><xref:System.Media.SoundPlayer.SoundLocation%2A> -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="58743-110"><xref:System.Media.SoundPlayer.SoundLocation%2A> property</span></span>|<span data-ttu-id="58743-111">Der Dateipfad oder die Webadresse des Sounds.</span><span class="sxs-lookup"><span data-stu-id="58743-111">The file path or Web address of the sound.</span></span> <span data-ttu-id="58743-112">Zulässige Werte sind UNC oder HTTP.</span><span class="sxs-lookup"><span data-stu-id="58743-112">Acceptable values can be UNC or HTTP.</span></span>|  
|<span data-ttu-id="58743-113"><xref:System.Media.SoundPlayer.LoadTimeout%2A> -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="58743-113"><xref:System.Media.SoundPlayer.LoadTimeout%2A> property</span></span>|<span data-ttu-id="58743-114">Die Anzahl an Millisekunden, die das Programm wartet, um einen Sound zu laden, bevor es eine Ausnahme auslöst.</span><span class="sxs-lookup"><span data-stu-id="58743-114">The number of milliseconds your program will wait to load a sound before it throws an exception.</span></span> <span data-ttu-id="58743-115">Der Standardwert ist 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="58743-115">The default is 10 seconds.</span></span>|  
|<span data-ttu-id="58743-116"><xref:System.Media.SoundPlayer.IsLoadCompleted%2A> -Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="58743-116"><xref:System.Media.SoundPlayer.IsLoadCompleted%2A> property</span></span>|<span data-ttu-id="58743-117">Ein boolescher Wert, der angibt, ob der Sound fertig geladen wurde.</span><span class="sxs-lookup"><span data-stu-id="58743-117">A Boolean value indicating whether the sound has finished loading.</span></span>|  
|<span data-ttu-id="58743-118"><xref:System.Media.SoundPlayer.Load%2A>-Methode</span><span class="sxs-lookup"><span data-stu-id="58743-118"><xref:System.Media.SoundPlayer.Load%2A> method</span></span>|<span data-ttu-id="58743-119">Lädt einen Sound synchron.</span><span class="sxs-lookup"><span data-stu-id="58743-119">Loads a sound synchronously.</span></span>|  
|<span data-ttu-id="58743-120"><xref:System.Media.SoundPlayer.LoadAsync%2A>-Methode</span><span class="sxs-lookup"><span data-stu-id="58743-120"><xref:System.Media.SoundPlayer.LoadAsync%2A> method</span></span>|<span data-ttu-id="58743-121">Fängt an, einen Sound asynchron zu laden.</span><span class="sxs-lookup"><span data-stu-id="58743-121">Begins to load a sound asynchronously.</span></span> <span data-ttu-id="58743-122">Wenn das Laden beendet ist, wird das- <xref:System.Media.SoundPlayer.OnLoadCompleted%2A> Ereignis ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="58743-122">When loading is complete, it raises the <xref:System.Media.SoundPlayer.OnLoadCompleted%2A> event.</span></span>|  
|<span data-ttu-id="58743-123"><xref:System.Media.SoundPlayer.Play%2A>-Methode</span><span class="sxs-lookup"><span data-stu-id="58743-123"><xref:System.Media.SoundPlayer.Play%2A> method</span></span>|<span data-ttu-id="58743-124">Gibt den in der-Eigenschaft oder der-Eigenschaft angegebenen Sound <xref:System.Media.SoundPlayer.SoundLocation%2A> <xref:System.Media.SoundPlayer.Stream%2A> in einem neuen Thread wieder.</span><span class="sxs-lookup"><span data-stu-id="58743-124">Plays the sound specified in the <xref:System.Media.SoundPlayer.SoundLocation%2A> or <xref:System.Media.SoundPlayer.Stream%2A> property in a new thread.</span></span>|  
|<span data-ttu-id="58743-125"><xref:System.Media.SoundPlayer.PlaySync%2A>-Methode</span><span class="sxs-lookup"><span data-stu-id="58743-125"><xref:System.Media.SoundPlayer.PlaySync%2A> method</span></span>|<span data-ttu-id="58743-126">Gibt den in der-Eigenschaft oder der-Eigenschaft angegebenen Sound <xref:System.Media.SoundPlayer.SoundLocation%2A> <xref:System.Media.SoundPlayer.Stream%2A> im aktuellen Thread wieder.</span><span class="sxs-lookup"><span data-stu-id="58743-126">Plays the sound specified in the <xref:System.Media.SoundPlayer.SoundLocation%2A> or <xref:System.Media.SoundPlayer.Stream%2A> property in the current thread.</span></span>|  
|<span data-ttu-id="58743-127"><xref:System.Media.SoundPlayer.Stop%2A>-Methode</span><span class="sxs-lookup"><span data-stu-id="58743-127"><xref:System.Media.SoundPlayer.Stop%2A> method</span></span>|<span data-ttu-id="58743-128">Beendet den aktuell wiedergegebenen Sound.</span><span class="sxs-lookup"><span data-stu-id="58743-128">Stops any sound currently playing.</span></span>|  
|<span data-ttu-id="58743-129"><xref:System.Media.SoundPlayer.LoadCompleted> -Ereignis</span><span class="sxs-lookup"><span data-stu-id="58743-129"><xref:System.Media.SoundPlayer.LoadCompleted> event</span></span>|<span data-ttu-id="58743-130">Wird ausgelöst, nachdem versucht wurde, einen Sound zu laden.</span><span class="sxs-lookup"><span data-stu-id="58743-130">Raised after the load of a sound is attempted.</span></span>|  
  
## <a name="see-also"></a><span data-ttu-id="58743-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="58743-131">See also</span></span>

- <xref:System.Media.SoundPlayer>
- <xref:System.Media.SystemSounds>
