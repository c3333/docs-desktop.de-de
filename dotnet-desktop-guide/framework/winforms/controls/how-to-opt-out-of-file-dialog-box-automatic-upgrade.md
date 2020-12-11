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
# <a name="how-to-opt-out-of-file-dialog-box-automatic-upgrade"></a>Vorgehensweise: Ablehnen des automatischen Upgrades des Dialogfelds „Datei“
Wenn die <xref:System.Windows.Forms.OpenFileDialog> -Klasse und die- <xref:System.Windows.Forms.SaveFileDialog> Klasse in einer Anwendung verwendet werden, hängen Ihre Darstellung und das Verhalten von der Windows-Version ab, auf der die Anwendung ausgeführt wird. Wenn eine Anwendung, die auf dem .NET Framework 2,0 oder früher erstellt wurde, unter Windows Vista angezeigt wird, <xref:System.Windows.Forms.OpenFileDialog> <xref:System.Windows.Forms.SaveFileDialog> werden Sie automatisch mit dem Aussehen und Verhalten von Windows Vista angezeigt. Beginnend mit dem .NET Framework 3,0 können Sie das automatische Upgrade zum Anzeigen von <xref:System.Windows.Forms.OpenFileDialog> und <xref:System.Windows.Forms.SaveFileDialog> mit einem Aussehen und Verhalten von Windows XP ablehnen.  
  
### <a name="to-opt-out-of-file-dialog-box-automatic-upgrade"></a>So lehnen Sie die automatische Aktualisierung des Dialogfelds „Datei“ ab  
  
1. Legen Sie die- <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> Eigenschaft von <xref:System.Windows.Forms.OpenFileDialog> oder <xref:System.Windows.Forms.SaveFileDialog> auf fest, `false` bevor Sie das Dialogfeld anzeigen.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.FileDialog>
