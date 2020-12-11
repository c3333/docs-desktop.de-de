---
title: 'Vorgehensweise: Wiedergabe eines Signaltons in Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sounds [Windows Forms], beep
- Windows Forms, sounds
- sounds [Windows Forms], playing
- forms [Windows Forms], sounds
- examples [Windows Forms], sounds
ms.assetid: 7ea5cded-4888-4f35-8f28-5cab1a55c973
ms.openlocfilehash: 7fecc5d5b7259b743926713f87d9303596803582
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975615"
---
# <a name="how-to-play-a-beep-from-a-windows-form"></a>Vorgehensweise: Wiedergabe eines Signaltons in Windows Forms
In diesem Beispiel wird einen Signalton zur Laufzeit wiedergegeben.

## <a name="example"></a>Beispiel

```vb
Public Sub OnePing()
    Beep()
End Sub
```

```csharp
public void onePing()
{
    SystemSounds.Beep.Play();
}
```

> [!NOTE]
> Der im c#-Codebeispiel wiedergegebene Sound wird von der <xref:System.Media.SystemSounds.Beep%2A> System Sound Einstellung bestimmt. Weitere Informationen finden Sie unter <xref:System.Media.SystemSounds>.

## <a name="compiling-the-code"></a>Kompilieren des Codes
 Für c# erfordert dieses Beispiel einen Verweis auf den- <xref:System.Media?displayProperty=nameWithType> Namespace.

## <a name="see-also"></a>Siehe auch

- <xref:Microsoft.VisualBasic.Interaction.Beep%2A>
- <xref:System.Media.SoundPlayer>
- [Vorgehensweise: Wiedergabe eines Systemsounds in Windows Forms](how-to-play-a-system-sound-from-a-windows-form.md)
- [Vorgehensweise: Wiedergabe von Sound in Windows Forms](how-to-play-a-sound-from-a-windows-form.md)
