---
title: 'Vorgehensweise: Anwenden des PropertyNameChanged-Musters'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- custom controls [Windows Forms], property changes (using code)
- data binding [Windows Forms], custom controls
- PropertyNameChanged pattern [Windows Forms], applying
ms.assetid: aa47ddf6-5223-40c4-833f-a78992194836
ms.openlocfilehash: 01afa713e97206ea192ba55dc2affad20163f872
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972318"
---
# <a name="how-to-apply-the-propertynamechanged-pattern"></a><span data-ttu-id="a20c9-102">Vorgehensweise: Anwenden des PropertyNameChanged-Musters</span><span class="sxs-lookup"><span data-stu-id="a20c9-102">How to: Apply the PropertyNameChanged Pattern</span></span>
<span data-ttu-id="a20c9-103">Im folgenden Codebeispiel wird veranschaulicht, wie das geänderte *propertyName*-Muster auf ein benutzerdefiniertes Steuerelement angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="a20c9-103">The following code example demonstrates how to apply the *PropertyName* Changed pattern to a custom control.</span></span> <span data-ttu-id="a20c9-104">Wenden Sie dieses Muster an, wenn Sie benutzerdefinierte Steuerelemente implementieren, die mit dem Windows Forms Datenbindungs-Engine verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a20c9-104">Apply this pattern when you implement custom controls that are used with the Windows Forms data binding engine.</span></span>  
  
## <a name="example"></a><span data-ttu-id="a20c9-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a20c9-105">Example</span></span>  
 [!code-csharp[System.Windows.Forms.ChangeNotification#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ChangeNotification/CS/Form1.cs#3)]
 [!code-vb[System.Windows.Forms.ChangeNotification#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ChangeNotification/VB/Form1.vb#3)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="a20c9-106">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="a20c9-106">Compiling the Code</span></span>  
 <span data-ttu-id="a20c9-107">So kompilieren Sie das vorherige Codebeispiel:</span><span class="sxs-lookup"><span data-stu-id="a20c9-107">To compile the previous code example:</span></span>  
  
- <span data-ttu-id="a20c9-108">Fügen Sie den Code in eine leere Codedatei ein.</span><span class="sxs-lookup"><span data-stu-id="a20c9-108">Paste the code into an empty code file.</span></span> <span data-ttu-id="a20c9-109">Sie müssen das benutzerdefinierte Steuerelement in einem Windows Form verwenden, das eine- `Main` Methode enthält.</span><span class="sxs-lookup"><span data-stu-id="a20c9-109">You must use the custom control on a Windows Form that contains a `Main` method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="a20c9-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a20c9-110">See also</span></span>

- [<span data-ttu-id="a20c9-111">Vorgehensweise: Implementieren der INotifyPropertyChanged-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a20c9-111">How to: Implement the INotifyPropertyChanged Interface</span></span>](how-to-implement-the-inotifypropertychanged-interface.md)
- [<span data-ttu-id="a20c9-112">Änderungsbenachrichtigung in der Windows Forms-Datenbindung</span><span class="sxs-lookup"><span data-stu-id="a20c9-112">Change Notification in Windows Forms Data Binding</span></span>](change-notification-in-windows-forms-data-binding.md)
- [<span data-ttu-id="a20c9-113">Datenbindung in Web Forms</span><span class="sxs-lookup"><span data-stu-id="a20c9-113">Windows Forms Data Binding</span></span>](windows-forms-data-binding.md)
