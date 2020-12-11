---
title: 'Vorgehensweise: Starten einer Schleife eines wiedergegebenen Sounds in Windows Forms'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- sound loops
- SoundPlayer class [Windows Forms], play looping
- sounds [Windows Forms], looping
- playing sounds [Windows Forms], looping
ms.assetid: ea95dd46-10a3-46c0-8263-4b205f00df7f
ms.openlocfilehash: e14d9de2326234b86c1f24b227e86f822fbfdb71
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976668"
---
# <a name="how-to-loop-a-sound-playing-on-a-windows-form"></a>Vorgehensweise: Starten einer Schleife eines wiedergegebenen Sounds in Windows Forms
Im folgenden Codebeispiel wird ein Sound mehrfach wiedergegeben. Wenn der Code im `stopPlayingButton_Click`-Ereignishandler ausgeführt wird, werden alle aktuell wiedergegebenen Sounds beendet. Wenn kein Sound wiedergegeben wird, passiert nichts.  
  
## <a name="example"></a>Beispiel  
 [!code-csharp[System.Media.SoundPlayer.PlayLooping#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Media.SoundPlayer.PlayLooping/CS/Form1.cs#1)]
 [!code-vb[System.Media.SoundPlayer.PlayLooping#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Media.SoundPlayer.PlayLooping/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Verweise auf die Assemblys "System" und "System.Windows.Forms".  
  
- Ersetzen Sie den Dateinamen `"c:\Windows\Media\chimes.wav"` durch einen gültigen Dateinamen.  
  
## <a name="robust-programming"></a>Stabile Programmierung  
 Dateioperationen sollten in entsprechende Ausnahmebehandlungsblöcke eingeschlossen sein.  
  
 Die folgenden Bedingungen können einen Ausnahmefehler verursachen:  
  
- Der Pfadname ist falsch formatiert. Er enthält beispielsweise unzulässige Zeichen oder besteht nur aus Leerzeichen (<xref:System.ArgumentException>-Klasse).  
  
- Der Pfad ist schreibgeschützt (<xref:System.IO.IOException>-Klasse).  
  
- Der Pfadname ist `Nothing` (<xref:System.ArgumentNullException>-Klasse).  
  
- Der Pfadname ist zu lang (<xref:System.IO.PathTooLongException>-Klasse).  
  
- Der Pfad ist ungültig (<xref:System.IO.DirectoryNotFoundException>-Klasse).  
  
- Der Pfad besteht nur aus einem Doppelpunkt ":" (<xref:System.NotSupportedException>-Klasse).  
  
## <a name="net-framework-security"></a>.NET Framework-Sicherheit  
 Beurteilen Sie den Inhalt der Datei nicht anhand des Dateinamens. Bei der Datei "Form1.vb" handelt es sich zum Beispiel nicht unbedingt um eine Visual Basic-Quelldatei. Überprüfen Sie alle Eingaben, bevor Sie die Daten in der Anwendung verwenden.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Media.SoundPlayer.PlayLooping%2A>
- [Vorgehensweise: Wiedergabe von Sound in Windows Forms](how-to-play-a-sound-from-a-windows-form.md)
- [Übersicht über die SoundPlayer-Klasse](soundplayer-class-overview.md)
