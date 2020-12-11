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
# <a name="how-to-play-a-beep-from-a-windows-form"></a><span data-ttu-id="7536b-102">Vorgehensweise: Wiedergabe eines Signaltons in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7536b-102">How to: Play a Beep from a Windows Form</span></span>
<span data-ttu-id="7536b-103">In diesem Beispiel wird einen Signalton zur Laufzeit wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="7536b-103">This example plays a beep at run time.</span></span>

## <a name="example"></a><span data-ttu-id="7536b-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7536b-104">Example</span></span>

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
> <span data-ttu-id="7536b-105">Der im c#-Codebeispiel wiedergegebene Sound wird von der <xref:System.Media.SystemSounds.Beep%2A> System Sound Einstellung bestimmt.</span><span class="sxs-lookup"><span data-stu-id="7536b-105">The sound played in the C# code sample is determined by the <xref:System.Media.SystemSounds.Beep%2A> system sound setting.</span></span> <span data-ttu-id="7536b-106">Weitere Informationen finden Sie unter <xref:System.Media.SystemSounds>.</span><span class="sxs-lookup"><span data-stu-id="7536b-106">For more information, see <xref:System.Media.SystemSounds>.</span></span>

## <a name="compiling-the-code"></a><span data-ttu-id="7536b-107">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="7536b-107">Compiling the Code</span></span>
 <span data-ttu-id="7536b-108">Für c# erfordert dieses Beispiel einen Verweis auf den- <xref:System.Media?displayProperty=nameWithType> Namespace.</span><span class="sxs-lookup"><span data-stu-id="7536b-108">For C#, this example requires  a reference to the <xref:System.Media?displayProperty=nameWithType> namespace.</span></span>

## <a name="see-also"></a><span data-ttu-id="7536b-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7536b-109">See also</span></span>

- <xref:Microsoft.VisualBasic.Interaction.Beep%2A>
- <xref:System.Media.SoundPlayer>
- [<span data-ttu-id="7536b-110">Vorgehensweise: Wiedergabe eines Systemsounds in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7536b-110">How to: Play a System Sound from a Windows Form</span></span>](how-to-play-a-system-sound-from-a-windows-form.md)
- [<span data-ttu-id="7536b-111">Vorgehensweise: Wiedergabe von Sound in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="7536b-111">How to: Play a Sound from a Windows Form</span></span>](how-to-play-a-sound-from-a-windows-form.md)
