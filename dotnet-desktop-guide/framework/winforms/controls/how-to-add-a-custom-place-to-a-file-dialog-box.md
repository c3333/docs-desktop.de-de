---
title: 'Vorgehensweise: Hinzufügen eines benutzerdefinierten Speicherorts zum Dialogfeld „Datei“'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Custom Place to dialog box
- adding Custom Place to dialog box
- CustomPlaces collection
ms.assetid: 63f6469b-59cd-40f6-9e61-8b5831856780
ms.openlocfilehash: 7172e484451cf932413920910ec9124b3388bd76
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975748"
---
# <a name="how-to-add-a-custom-place-to-a-file-dialog-box"></a>Vorgehensweise: Hinzufügen eines benutzerdefinierten Speicherorts zum Dialogfeld „Datei“
Die Standard Dialogfelder zum Öffnen und speichern in Windows Vista haben einen Bereich auf der linken Seite des Dialog Felds mit der Bezeichnung **Favoriten Links**. Dieser Bereich wird als „Benutzerdefinierte Speicherorte“ bezeichnet. Mit der <xref:System.Windows.Forms.OpenFileDialog> -Klasse und der- <xref:System.Windows.Forms.SaveFileDialog> Klasse können Sie der Auflistung Ordner hinzufügen <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> .  
  
> [!NOTE]
> Damit ein benutzerdefinierter Speicherort in <xref:System.Windows.Forms.OpenFileDialog> oder angezeigt <xref:System.Windows.Forms.SaveFileDialog> wird, muss die- <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> Eigenschaft auf festgelegt werden `true` (Standardeinstellung).  
  
### <a name="to-add-a-custom-place-to-a-file-dialog-box"></a>So fügen Sie dem Dialogfeld „Datei“ einen benutzerdefinierten Speicherort hinzu  
  
- Fügen Sie der-Auflistung des Dialog Felds einen Pfad, eine bekannte Ordner-GUID oder ein- <xref:System.Windows.Forms.FileDialogCustomPlace> Objekt hinzu <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> .  
  
     Im folgenden Codebeispiel wird veranschaulicht, wie Sie einen Pfad hinzufügen:  
  
    ```vb  
    OpenFileDialog1.CustomPlaces.Add("C:\MyCustomPlace")  
    ```  
  
    ```csharp  
    openFileDialog1.CustomPlaces.Add("C:\\MyCustomPlace");  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.FileDialog>
- <xref:System.Windows.Forms.FileDialogCustomPlacesCollection.Add%2A?displayProperty=nameWithType>
- [GUIDs von bekannten Ordnern für benutzerdefinierte Speicherorte im Dateidialogfeld](known-folder-guids-for-file-dialog-custom-places.md)
