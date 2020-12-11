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
# <a name="how-to-add-a-custom-place-to-a-file-dialog-box"></a><span data-ttu-id="ea304-102">Vorgehensweise: Hinzufügen eines benutzerdefinierten Speicherorts zum Dialogfeld „Datei“</span><span class="sxs-lookup"><span data-stu-id="ea304-102">How To: Add a Custom Place to a File Dialog Box</span></span>
<span data-ttu-id="ea304-103">Die Standard Dialogfelder zum Öffnen und speichern in Windows Vista haben einen Bereich auf der linken Seite des Dialog Felds mit der Bezeichnung **Favoriten Links**.</span><span class="sxs-lookup"><span data-stu-id="ea304-103">The default open and save dialog boxes on Windows Vista have an area on the left side of the dialog box titled **Favorite Links**.</span></span> <span data-ttu-id="ea304-104">Dieser Bereich wird als „Benutzerdefinierte Speicherorte“ bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ea304-104">This area is called custom places.</span></span> <span data-ttu-id="ea304-105">Mit der <xref:System.Windows.Forms.OpenFileDialog> -Klasse und der- <xref:System.Windows.Forms.SaveFileDialog> Klasse können Sie der Auflistung Ordner hinzufügen <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> .</span><span class="sxs-lookup"><span data-stu-id="ea304-105">The <xref:System.Windows.Forms.OpenFileDialog> and <xref:System.Windows.Forms.SaveFileDialog> classes allow you to add folders to the <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="ea304-106">Damit ein benutzerdefinierter Speicherort in <xref:System.Windows.Forms.OpenFileDialog> oder angezeigt <xref:System.Windows.Forms.SaveFileDialog> wird, muss die- <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> Eigenschaft auf festgelegt werden `true` (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="ea304-106">In order for a custom place to appear in the <xref:System.Windows.Forms.OpenFileDialog> or <xref:System.Windows.Forms.SaveFileDialog>, the <xref:System.Windows.Forms.FileDialog.AutoUpgradeEnabled%2A> property must be set to `true` (the default).</span></span>  
  
### <a name="to-add-a-custom-place-to-a-file-dialog-box"></a><span data-ttu-id="ea304-107">So fügen Sie dem Dialogfeld „Datei“ einen benutzerdefinierten Speicherort hinzu</span><span class="sxs-lookup"><span data-stu-id="ea304-107">To add a custom place to a file dialog box</span></span>  
  
- <span data-ttu-id="ea304-108">Fügen Sie der-Auflistung des Dialog Felds einen Pfad, eine bekannte Ordner-GUID oder ein- <xref:System.Windows.Forms.FileDialogCustomPlace> Objekt hinzu <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> .</span><span class="sxs-lookup"><span data-stu-id="ea304-108">Add a path, a Known Folder GUID, or a <xref:System.Windows.Forms.FileDialogCustomPlace> object to the <xref:System.Windows.Forms.FileDialog.CustomPlaces%2A> collection of the dialog box.</span></span>  
  
     <span data-ttu-id="ea304-109">Im folgenden Codebeispiel wird veranschaulicht, wie Sie einen Pfad hinzufügen:</span><span class="sxs-lookup"><span data-stu-id="ea304-109">The following code example shows how to add a path:</span></span>  
  
    ```vb  
    OpenFileDialog1.CustomPlaces.Add("C:\MyCustomPlace")  
    ```  
  
    ```csharp  
    openFileDialog1.CustomPlaces.Add("C:\\MyCustomPlace");  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="ea304-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea304-110">See also</span></span>

- <xref:System.Windows.Forms.FileDialog>
- <xref:System.Windows.Forms.FileDialogCustomPlacesCollection.Add%2A?displayProperty=nameWithType>
- [<span data-ttu-id="ea304-111">GUIDs von bekannten Ordnern für benutzerdefinierte Speicherorte im Dateidialogfeld</span><span class="sxs-lookup"><span data-stu-id="ea304-111">Known Folder GUIDs for File Dialog Custom Places</span></span>](known-folder-guids-for-file-dialog-custom-places.md)
