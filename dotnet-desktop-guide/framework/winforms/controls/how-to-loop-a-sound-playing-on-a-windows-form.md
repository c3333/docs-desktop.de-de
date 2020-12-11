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
# <a name="how-to-loop-a-sound-playing-on-a-windows-form"></a><span data-ttu-id="faa12-102">Vorgehensweise: Starten einer Schleife eines wiedergegebenen Sounds in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="faa12-102">How to: Loop a Sound Playing on a Windows Form</span></span>
<span data-ttu-id="faa12-103">Im folgenden Codebeispiel wird ein Sound mehrfach wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="faa12-103">The following code example plays a sound repeatedly.</span></span> <span data-ttu-id="faa12-104">Wenn der Code im `stopPlayingButton_Click`-Ereignishandler ausgeführt wird, werden alle aktuell wiedergegebenen Sounds beendet.</span><span class="sxs-lookup"><span data-stu-id="faa12-104">When the code in the `stopPlayingButton_Click` event handler runs, any sound currently playing stops.</span></span> <span data-ttu-id="faa12-105">Wenn kein Sound wiedergegeben wird, passiert nichts.</span><span class="sxs-lookup"><span data-stu-id="faa12-105">If no sound is playing, nothing happens.</span></span>  
  
## <a name="example"></a><span data-ttu-id="faa12-106">Beispiel</span><span class="sxs-lookup"><span data-stu-id="faa12-106">Example</span></span>  
 [!code-csharp[System.Media.SoundPlayer.PlayLooping#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Media.SoundPlayer.PlayLooping/CS/Form1.cs#1)]
 [!code-vb[System.Media.SoundPlayer.PlayLooping#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Media.SoundPlayer.PlayLooping/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="faa12-107">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="faa12-107">Compiling the Code</span></span>  
 <span data-ttu-id="faa12-108">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="faa12-108">This example requires:</span></span>  
  
- <span data-ttu-id="faa12-109">Verweise auf die Assemblys "System" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="faa12-109">References to the System and System.Windows.Forms assemblies.</span></span>  
  
- <span data-ttu-id="faa12-110">Ersetzen Sie den Dateinamen `"c:\Windows\Media\chimes.wav"` durch einen gültigen Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="faa12-110">That you replace the file name `"c:\Windows\Media\chimes.wav"` with a valid file name.</span></span>  
  
## <a name="robust-programming"></a><span data-ttu-id="faa12-111">Stabile Programmierung</span><span class="sxs-lookup"><span data-stu-id="faa12-111">Robust Programming</span></span>  
 <span data-ttu-id="faa12-112">Dateioperationen sollten in entsprechende Ausnahmebehandlungsblöcke eingeschlossen sein.</span><span class="sxs-lookup"><span data-stu-id="faa12-112">File operations should be enclosed within appropriate exception-handling blocks.</span></span>  
  
 <span data-ttu-id="faa12-113">Die folgenden Bedingungen können einen Ausnahmefehler verursachen:</span><span class="sxs-lookup"><span data-stu-id="faa12-113">The following conditions may cause an exception:</span></span>  
  
- <span data-ttu-id="faa12-114">Der Pfadname ist falsch formatiert.</span><span class="sxs-lookup"><span data-stu-id="faa12-114">The path name is malformed.</span></span> <span data-ttu-id="faa12-115">Er enthält beispielsweise unzulässige Zeichen oder besteht nur aus Leerzeichen (<xref:System.ArgumentException>-Klasse).</span><span class="sxs-lookup"><span data-stu-id="faa12-115">For example, it contains characters that are not valid or it is only white space (<xref:System.ArgumentException> class).</span></span>  
  
- <span data-ttu-id="faa12-116">Der Pfad ist schreibgeschützt (<xref:System.IO.IOException>-Klasse).</span><span class="sxs-lookup"><span data-stu-id="faa12-116">The path is read-only (<xref:System.IO.IOException> class).</span></span>  
  
- <span data-ttu-id="faa12-117">Der Pfadname ist `Nothing` (<xref:System.ArgumentNullException>-Klasse).</span><span class="sxs-lookup"><span data-stu-id="faa12-117">The path name is `Nothing` (<xref:System.ArgumentNullException> class).</span></span>  
  
- <span data-ttu-id="faa12-118">Der Pfadname ist zu lang (<xref:System.IO.PathTooLongException>-Klasse).</span><span class="sxs-lookup"><span data-stu-id="faa12-118">The path name is too long (<xref:System.IO.PathTooLongException> class).</span></span>  
  
- <span data-ttu-id="faa12-119">Der Pfad ist ungültig (<xref:System.IO.DirectoryNotFoundException>-Klasse).</span><span class="sxs-lookup"><span data-stu-id="faa12-119">The path is invalid (<xref:System.IO.DirectoryNotFoundException> class).</span></span>  
  
- <span data-ttu-id="faa12-120">Der Pfad besteht nur aus einem Doppelpunkt ":" (<xref:System.NotSupportedException>-Klasse).</span><span class="sxs-lookup"><span data-stu-id="faa12-120">The path is only a colon ":" (<xref:System.NotSupportedException> class).</span></span>  
  
## <a name="net-framework-security"></a><span data-ttu-id="faa12-121">.NET Framework-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="faa12-121">.NET Framework Security</span></span>  
 <span data-ttu-id="faa12-122">Beurteilen Sie den Inhalt der Datei nicht anhand des Dateinamens.</span><span class="sxs-lookup"><span data-stu-id="faa12-122">Do not make decisions about the contents of the file based on the name of the file.</span></span> <span data-ttu-id="faa12-123">Bei der Datei "Form1.vb" handelt es sich zum Beispiel nicht unbedingt um eine Visual Basic-Quelldatei.</span><span class="sxs-lookup"><span data-stu-id="faa12-123">For example, the file Form1.vb may not be a Visual Basic source file.</span></span> <span data-ttu-id="faa12-124">Überprüfen Sie alle Eingaben, bevor Sie die Daten in der Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="faa12-124">Verify all inputs before using the data in your application.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="faa12-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faa12-125">See also</span></span>

- <xref:System.Media.SoundPlayer.PlayLooping%2A>
- [<span data-ttu-id="faa12-126">Vorgehensweise: Wiedergabe von Sound in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="faa12-126">How to: Play a Sound from a Windows Form</span></span>](how-to-play-a-sound-from-a-windows-form.md)
- [<span data-ttu-id="faa12-127">Übersicht über die SoundPlayer-Klasse</span><span class="sxs-lookup"><span data-stu-id="faa12-127">SoundPlayer Class Overview</span></span>](soundplayer-class-overview.md)
