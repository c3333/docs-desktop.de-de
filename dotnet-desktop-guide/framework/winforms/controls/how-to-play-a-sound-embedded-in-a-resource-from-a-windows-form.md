---
title: 'Vorgehensweise: Wiedergeben eines in einer Ressource aus Windows Forms eingebetteten Sounds'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sounds [Windows Forms], playing from resources
- resources [Windows Forms], playing sounds
- playing sounds [Windows Forms], from resources
- SoundPlayer class [Windows Forms], playing sounds from resources
ms.assetid: 7d148bb6-8a1e-47d7-a08d-35828d2e688f
ms.openlocfilehash: 49235f9cb035c5a09c26b427f855fc00e818fe1c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974791"
---
# <a name="how-to-play-a-sound-embedded-in-a-resource-from-a-windows-form"></a>Vorgehensweise: Wiedergeben eines in einer Ressource aus Windows Forms eingebetteten Sounds
Mit der-Klasse können Sie <xref:System.Media.SoundPlayer> einen Sound von einer eingebetteten Ressource abspielen.  
  
## <a name="example"></a>Beispiel  
 [!code-csharp[System.Windows.Forms.Sound#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.Sound/CS/soundtestform.cs#10)]
 [!code-vb[System.Windows.Forms.Sound#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.Sound/VB/soundtestform.vb#10)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
 Der <xref:System.Media?displayProperty=nameWithType> Namespace wird importiert.  
  
 Die Sounddatei wird als eingebettete Ressource in das Projekt aufgenommen.  
  
 Ersetzen Sie " \<AssemblyName> " durch den Namen der Assembly, in die die Audiodatei eingebettet ist. Das Suffix „.dll“ wird nicht angegeben.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Media.SoundPlayer>
- [Vorgehensweise: Wiedergabe von Sound in Windows Forms](how-to-play-a-sound-from-a-windows-form.md)
- [Vorgehensweise: Starten einer Schleife eines wiedergegebenen Sounds in Windows Forms](how-to-loop-a-sound-playing-on-a-windows-form.md)
