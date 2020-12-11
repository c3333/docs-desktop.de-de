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
# <a name="soundplayer-class-overview"></a>Übersicht über die SoundPlayer-Klasse
Die <xref:System.Media.SoundPlayer>-Klasse ermöglicht es Ihnen, Sounds problemlos in Ihre Anwendungen zu integrieren.  
  
 Die- <xref:System.Media.SoundPlayer> Klasse kann Sounddateien im WAV-Format wiedergeben, entweder von einer Ressource oder von UNC-oder http-Speicherorten. Außerdem <xref:System.Media.SoundPlayer> können Sie mit der-Klasse Sounds asynchron laden oder abspielen.  
  
 Sie können auch die <xref:System.Media.SystemSounds>-Klasse verwenden, um allgemeine Systemsounds wiederzugeben, einschließlich eines akustischen Signals.  
  
## <a name="commonly-used-properties-methods-and-events"></a>Häufig verwendete Eigenschaften, Methoden und Ereignisse  
  
|Name|BESCHREIBUNG|  
|----------|-----------------|  
|<xref:System.Media.SoundPlayer.SoundLocation%2A> -Eigenschaft|Der Dateipfad oder die Webadresse des Sounds. Zulässige Werte sind UNC oder HTTP.|  
|<xref:System.Media.SoundPlayer.LoadTimeout%2A> -Eigenschaft|Die Anzahl an Millisekunden, die das Programm wartet, um einen Sound zu laden, bevor es eine Ausnahme auslöst. Der Standardwert ist 10 Sekunden.|  
|<xref:System.Media.SoundPlayer.IsLoadCompleted%2A> -Eigenschaft|Ein boolescher Wert, der angibt, ob der Sound fertig geladen wurde.|  
|<xref:System.Media.SoundPlayer.Load%2A>-Methode|Lädt einen Sound synchron.|  
|<xref:System.Media.SoundPlayer.LoadAsync%2A>-Methode|Fängt an, einen Sound asynchron zu laden. Wenn das Laden beendet ist, wird das- <xref:System.Media.SoundPlayer.OnLoadCompleted%2A> Ereignis ausgelöst.|  
|<xref:System.Media.SoundPlayer.Play%2A>-Methode|Gibt den in der-Eigenschaft oder der-Eigenschaft angegebenen Sound <xref:System.Media.SoundPlayer.SoundLocation%2A> <xref:System.Media.SoundPlayer.Stream%2A> in einem neuen Thread wieder.|  
|<xref:System.Media.SoundPlayer.PlaySync%2A>-Methode|Gibt den in der-Eigenschaft oder der-Eigenschaft angegebenen Sound <xref:System.Media.SoundPlayer.SoundLocation%2A> <xref:System.Media.SoundPlayer.Stream%2A> im aktuellen Thread wieder.|  
|<xref:System.Media.SoundPlayer.Stop%2A>-Methode|Beendet den aktuell wiedergegebenen Sound.|  
|<xref:System.Media.SoundPlayer.LoadCompleted> -Ereignis|Wird ausgelöst, nachdem versucht wurde, einen Sound zu laden.|  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Media.SoundPlayer>
- <xref:System.Media.SystemSounds>
