---
title: 'Vorgehensweise: Implementieren der INotifyPropertyChanged-Schnittstelle'
description: Erfahren Sie, wie Sie die INotifyPropertyChanged-Schnittstelle für Geschäftsobjekte implementieren, die in Windows Forms Datenbindung verwendet werden.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- INotifyPropertyChanged interface [Windows Forms], implementing
ms.assetid: eac428af-b43b-46ac-80d9-1a5f88658725
ms.openlocfilehash: 83d2ef32787d2dbcd877bc77dcede10111098f8a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976442"
---
# <a name="how-to-implement-the-inotifypropertychanged-interface"></a><span data-ttu-id="3f71b-103">Vorgehensweise: Implementieren der INotifyPropertyChanged-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3f71b-103">How to: Implement the INotifyPropertyChanged Interface</span></span>
<span data-ttu-id="3f71b-104">Im folgenden Codebeispiel wird veranschaulicht, wie die- <xref:System.ComponentModel.INotifyPropertyChanged> Schnittstelle implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="3f71b-104">The following code example demonstrates how to implement the <xref:System.ComponentModel.INotifyPropertyChanged> interface.</span></span> <span data-ttu-id="3f71b-105">Implementieren Sie diese Schnittstelle für Geschäftsobjekte, die in Windows Forms Datenbindung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f71b-105">Implement this interface on business objects that are used in Windows Forms data binding.</span></span> <span data-ttu-id="3f71b-106">Wenn die-Schnittstelle implementiert ist, kommuniziert Sie mit einem gebundenen Steuerelement mit den Eigenschafts Änderungen für ein Geschäftsobjekt.</span><span class="sxs-lookup"><span data-stu-id="3f71b-106">When implemented, the interface  communicates to a bound control the property changes on a business object.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3f71b-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3f71b-107">Example</span></span>  
 [!code-csharp[System.ComponentModel.IPropertyChangeExample#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/CS/Form1.cs#1)]
 [!code-vb[System.ComponentModel.IPropertyChangeExample#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IPropertyChangeExample/VB/Form1.vb#1)]  
  
## <a name="see-also"></a><span data-ttu-id="3f71b-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f71b-108">See also</span></span>

- [<span data-ttu-id="3f71b-109">Vorgehensweise: Anwenden des PropertyNameChanged-Musters</span><span class="sxs-lookup"><span data-stu-id="3f71b-109">How to: Apply the PropertyNameChanged Pattern</span></span>](how-to-apply-the-propertynamechanged-pattern.md)
- [<span data-ttu-id="3f71b-110">Datenbindung in Web Forms</span><span class="sxs-lookup"><span data-stu-id="3f71b-110">Windows Forms Data Binding</span></span>](windows-forms-data-binding.md)
- [<span data-ttu-id="3f71b-111">Vorgehensweise: Auslösen von Änderungsbenachrichtigungen mithilfe von BindingSource und der INotifyPropertyChanged-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3f71b-111">How to: Raise Change Notifications Using a BindingSource and the INotifyPropertyChanged Interface</span></span>](./controls/raise-change-notifications--bindingsource.md)
- [<span data-ttu-id="3f71b-112">Änderungsbenachrichtigung in der Windows Forms-Datenbindung</span><span class="sxs-lookup"><span data-stu-id="3f71b-112">Change Notification in Windows Forms Data Binding</span></span>](change-notification-in-windows-forms-data-binding.md)
