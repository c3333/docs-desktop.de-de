---
title: 'Vorgehensweise: Ablehnen des automatischen Upgrades des Dialogfelds „Datei“'
ms.date: 03/30/2017
helpviewer_keywords:
- OpenFileDialog [Windows Forms], opt out of automatic upgrade
- file dialog box [Windows Forms], opt out of automatic upgrade
- Windows Vista file dialog box [Windows Forms], opt out of automatic upgrade
- SaveFileDialog [Windows Forms], opt out of automatic upgrade
- AutoUpgradeEnabled property
ms.assetid: 522e482e-cc01-48b1-8d59-9617dc2c4ac1
ms.openlocfilehash: 154953680426f98a9506feb0b8f4de25c873b795
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976664"
---
# <a name="how-to-opt-out-of-file-dialog-box-automatic-upgrade"></a><span data-ttu-id="1d783-102">Vorgehensweise: Ablehnen des automatischen Upgrades des Dialogfelds „Datei“</span><span class="sxs-lookup"><span data-stu-id="1d783-102">How To: Opt Out of File Dialog Box Automatic Upgrade</span></span>
<span data-ttu-id="1d783-103">Wenn die <xref:System.Windows.Forms.OpenFileDialog> -Klasse und die- <xref:System.Windows.Forms.SaveFileDialog> Klasse in einer Anwendung verwendet werden, hängen Ihre Darstellung und das Verhalten von der Windows-Version ab, auf der die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1d783-103">When the <xref:System.Windows.Forms.OpenFileDialog> and <xref:System.Windows.Forms.SaveFileDialog> classes are used in an application, their appearance and behavior depend on the version of Windows the application is running on.</span></span> <span data-ttu-id="1d783-104">Wenn eine Anwendung, die auf dem .NET Framework 2,0 oder früher erstellt wurde, unter Windows Vista angezeigt wird, <xref:System.Windows.Forms.OpenFileDialog> <xref:System.Windows.Forms.SaveFileDialog> werden Sie automatisch mit dem Aussehen und Verhalten von Windows Vista angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1d783-104">When an application that was created on the .NET Framework 2.0 or earlier is displayed on Windows Vista, <xref:System.Windows.Forms.OpenFileDialog> and <xref:System.Windows.Forms.SaveFileDialog> are automatically displayed with the Windows Vista appearance and behavior.</span></span> <span data-ttu-id="1d783-105">Beginnend mit dem .NET Framework 3,0 können Sie das automatische Upgrade zum Anzeigen von <xref:System.Windows.Forms.OpenFileDialog> und <xref:System.Windows.Forms.SaveFileDialog> mit einem Aussehen und Verhalten von Windows XP ablehnen.</span><span class="sxs-lookup"><span data-stu-id="1d783-105">Starting in the .NET Framework 3.0, you can opt out of the automatic upgrade to display the <xref:System.Windows.Forms.OpenFileDialog> and <xref:System.Windows.Forms.SaveFileDialog> with a Windows XP-style appearance and behavior.</span></span>  
  
### <a name="to-opt-out-of-file-dialog-box-automatic-upgrade"></a><span data-ttu-id="1d783-106">So lehnen Sie die automatische Aktualisierung des Dialogfelds „Datei“ ab</span><span class="sxs-lookup"><span data-stu-id="1d783-106">To opt out of file dialog box automatic upgrade</span></span>  
  
1. <span data-ttu-id="1d783-107">Legen Sie die- <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> Eigenschaft von <xref:System.Windows.Forms.OpenFileDialog> oder <xref:System.Windows.Forms.SaveFileDialog> auf fest, `false` bevor Sie das Dialogfeld anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1d783-107">Set the <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> property of <xref:System.Windows.Forms.OpenFileDialog> or <xref:System.Windows.Forms.SaveFileDialog> to `false` before you display the dialog box.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="1d783-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d783-108">See also</span></span>

- <xref:System.Windows.Forms.FileDialog>
