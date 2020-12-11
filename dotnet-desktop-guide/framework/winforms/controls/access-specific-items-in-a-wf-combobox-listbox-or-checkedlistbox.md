---
title: Zugreifen auf bestimmte Elemente in der ComboBox-, ListBox-oder CheckedListBox-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ComboBox control [Windows Forms], accessing items
- ListBox control [Windows Forms], returning item information
- list boxes [Windows Forms], accessing items
- ListBox control [Windows Forms], accessing items
- combo boxes [Windows Forms], accessing items
- CheckedListBox control [Windows Forms], accessing items
ms.assetid: 1216742f-bcf9-4ff8-8a62-d7c9053c2b96
ms.openlocfilehash: 67673ec7f136f1466d4fd091e691324c53e7de06
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975806"
---
# <a name="how-to-access-specific-items-in-a-windows-forms-combobox-listbox-or-checkedlistbox-control"></a><span data-ttu-id="a3cf6-102">Vorgehensweise: Zugreifen auf spezifische Elemente in ComboBox-, ListBox- oder CheckedListBox-Steuerelementen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="a3cf6-102">How to: Access Specific Items in a Windows Forms ComboBox, ListBox, or CheckedListBox Control</span></span>
<span data-ttu-id="a3cf6-103">Der Zugriff auf bestimmte Elemente in einem Kombinations Feld (Windows Forms), einem Listenfeld oder einem aktivierten Listenfeld ist eine wesentliche Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="a3cf6-103">Accessing specific items in a Windows Forms combo box, list box, or checked list box is an essential task.</span></span> <span data-ttu-id="a3cf6-104">Mit dieser Option können Sie Programm gesteuert ermitteln, was in einer Liste an einer beliebigen Position vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a3cf6-104">It enables you to programmatically determine what is in a list, at any given position.</span></span>  
  
### <a name="to-access-a-specific-item"></a><span data-ttu-id="a3cf6-105">So greifen Sie auf ein bestimmtes Element zu</span><span class="sxs-lookup"><span data-stu-id="a3cf6-105">To access a specific item</span></span>  
  
1. <span data-ttu-id="a3cf6-106">Abfragen der Auflistung `Items` mit dem Index des bestimmten Elements:</span><span class="sxs-lookup"><span data-stu-id="a3cf6-106">Query the `Items` collection using the index of the specific item:</span></span>  
  
    ```vb  
    Private Function GetItemText(i As Integer) As String  
       ' Return the text of the item using the index:  
       Return ComboBox1.Items(i).ToString  
    End Function  
    ```  
  
    ```csharp  
    private string GetItemText(int i)  
    {  
       // Return the text of the item using the index:  
       return (comboBox1.Items[i].ToString());  
    }  
    ```  
  
    ```cpp  
    private:  
       String^ GetItemText(int i)  
       {  
          // Return the text of the item using the index:  
          return (comboBox1->Items->Item[i]->ToString());  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="a3cf6-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3cf6-107">See also</span></span>

- <xref:System.Windows.Forms.ComboBox>
- <xref:System.Windows.Forms.ListBox>
- <xref:System.Windows.Forms.CheckedListBox>
- [<span data-ttu-id="a3cf6-108">Steuerelemente in Windows Forms zum Auflisten von Optionen</span><span class="sxs-lookup"><span data-stu-id="a3cf6-108">Windows Forms Controls Used to List Options</span></span>](windows-forms-controls-used-to-list-options.md)
