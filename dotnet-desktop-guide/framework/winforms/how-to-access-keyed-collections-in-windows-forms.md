---
title: 'Gewusst wie: Zugreifen auf verschlüsselte Auflistungen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- keyed collections [Windows Forms]
- collections [Windows Forms], accessing with keys
ms.assetid: b9b79b8b-d9bf-4f8c-b9d6-9578bc3219d3
ms.openlocfilehash: 717ba9cc8605da08701de1bd13d6bc6da1c9b758
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972319"
---
# <a name="how-to-access-keyed-collections-in-windows-forms"></a><span data-ttu-id="09c35-102">Vorgehensweise: Zugreifen auf verschlüsselte Auflistungen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="09c35-102">How to: Access Keyed Collections in Windows Forms</span></span>

- <span data-ttu-id="09c35-103">Sie können auf einzelne Sammel Elemente nach Schlüssel zugreifen.</span><span class="sxs-lookup"><span data-stu-id="09c35-103">You can access individual collection items by key.</span></span> <span data-ttu-id="09c35-104">Diese Funktionalität wurde vielen Sammlungs Klassen hinzugefügt, die in der Regel von Windows Forms Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="09c35-104">This functionality has been added to many collection classes that are typically used by Windows Forms applications.</span></span> <span data-ttu-id="09c35-105">In der folgenden Liste sind einige der Auflistungs Klassen aufgeführt, für die barrierefreie Sammlungen zugänglich sind:</span><span class="sxs-lookup"><span data-stu-id="09c35-105">The following list shows some of the collection classes that have accessible keyed collections:</span></span>  
  
- <xref:System.Windows.Forms.ListView.ListViewItemCollection>  
  
- <xref:System.Windows.Forms.ListViewItem.ListViewSubItemCollection>  
  
- <xref:System.Windows.Forms.Control.ControlCollection>  
  
- <xref:System.Windows.Forms.TabControl.TabPageCollection>  
  
- <xref:System.Windows.Forms.TreeNodeCollection>  
  
 <span data-ttu-id="09c35-106">Der Schlüssel, der einem Element in einer Auflistung zugeordnet ist, ist in der Regel der Name des Elements.</span><span class="sxs-lookup"><span data-stu-id="09c35-106">The key associated with an item in a collection is typically the name of the item.</span></span> <span data-ttu-id="09c35-107">In den folgenden Verfahren wird gezeigt, wie Sie mithilfe von Auflistungs Klassen häufige Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="09c35-107">The following procedures show you how to use collection classes to perform common tasks.</span></span>  
  
### <a name="to-find-and-give-focus-to-a-nested-control-in-a-control-collection"></a><span data-ttu-id="09c35-108">So suchen und setzen Sie den Fokus auf ein in einer Steuerelement Sammlung eingefügter Steuerelement</span><span class="sxs-lookup"><span data-stu-id="09c35-108">To find and give focus to a nested control in a control collection</span></span>  
  
- <span data-ttu-id="09c35-109">Verwenden <xref:System.Windows.Forms.Control.ControlCollection.Find%2A> Sie die-Methode und die- <xref:System.Windows.Forms.Control.Focus%2A> Methode, um den Namen des Steuer Elements anzugeben, das gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="09c35-109">Use the <xref:System.Windows.Forms.Control.ControlCollection.Find%2A> and <xref:System.Windows.Forms.Control.Focus%2A> methods to specify the name of the control to find and give focus to.</span></span>  
  
     [!code-csharp[System.Windows.Forms.KeyedCollectionsEx#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.KeyedCollectionsEx/CS/Form1.cs#1)]
     [!code-vb[System.Windows.Forms.KeyedCollectionsEx#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.KeyedCollectionsEx/VB/Form1.vb#1)]  
  
### <a name="to-access-an-image-in-an-image-collection"></a><span data-ttu-id="09c35-110">So greifen Sie auf ein Bild in einer Bild Auflistung zu</span><span class="sxs-lookup"><span data-stu-id="09c35-110">To access an image in an image collection</span></span>  
  
- <span data-ttu-id="09c35-111">Verwenden Sie die- <xref:System.Windows.Forms.ImageList.ImageCollection.Item%2A> Eigenschaft, um den Namen des Abbilds anzugeben, auf das Sie zugreifen möchten.</span><span class="sxs-lookup"><span data-stu-id="09c35-111">Use the <xref:System.Windows.Forms.ImageList.ImageCollection.Item%2A> property to specify the name of the image you want to access.</span></span>  
  
     [!code-csharp[System.Windows.Forms.KeyedCollectionsEx#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.KeyedCollectionsEx/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.KeyedCollectionsEx#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.KeyedCollectionsEx/VB/Form1.vb#2)]  
  
### <a name="to-set-a-tab-page-as-the-selected-tab"></a><span data-ttu-id="09c35-112">So legen Sie eine Registerkarte als ausgewählte Registerkarte fest</span><span class="sxs-lookup"><span data-stu-id="09c35-112">To set a tab page as the selected tab</span></span>  
  
- <span data-ttu-id="09c35-113">Verwenden Sie die- <xref:System.Windows.Forms.TabControl.SelectedTab%2A> Eigenschaft in Verbindung mit der- <xref:System.Windows.Forms.TabControl.TabPageCollection.Item%2A> Eigenschaft, um den Namen der Registerkarte anzugeben, die als ausgewählte Registerkarte festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="09c35-113">Use the <xref:System.Windows.Forms.TabControl.SelectedTab%2A> property together with the <xref:System.Windows.Forms.TabControl.TabPageCollection.Item%2A> property to specify the name of the tab page to set as the selected tab.</span></span>  
  
     [!code-csharp[System.Windows.Forms.KeyedCollectionsEx#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.KeyedCollectionsEx/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.KeyedCollectionsEx#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.KeyedCollectionsEx/VB/Form1.vb#3)]  
  
## <a name="see-also"></a><span data-ttu-id="09c35-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09c35-114">See also</span></span>

- [<span data-ttu-id="09c35-115">Ersten Schritte mit Windows Forms</span><span class="sxs-lookup"><span data-stu-id="09c35-115">Getting Started with Windows Forms</span></span>](getting-started-with-windows-forms.md)
- [<span data-ttu-id="09c35-116">Vorgehensweise: Hinzufügen oder Entfernen von Bildern mit der ImageList-Komponente in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="09c35-116">How to: Add or Remove Images with the Windows Forms ImageList Component</span></span>](./controls/how-to-add-or-remove-images-with-the-windows-forms-imagelist-component.md)
