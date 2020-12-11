---
title: 'Gewusst wie: Binden eines Listenfelds an Daten'
ms.date: 03/30/2017
helpviewer_keywords:
- ListBox controls [WPF], binding data to
- data binding [WPF], ListBox control
- binding data [WPF], to ListBox control
ms.assetid: de93a907-709a-44a7-84bf-578b846a3d8b
ms.openlocfilehash: 4dea53a524247d18628b3e7e7b2c06906dced53d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978094"
---
# <a name="how-to-bind-a-listbox-to-data"></a><span data-ttu-id="bc16c-102">Gewusst wie: Binden eines Listenfelds an Daten</span><span class="sxs-lookup"><span data-stu-id="bc16c-102">How to: Bind a ListBox to Data</span></span>
<span data-ttu-id="bc16c-103">Ein Anwendungsentwickler kann Steuer <xref:System.Windows.Controls.ListBox> Elemente erstellen, ohne den Inhalt <xref:System.Windows.Controls.ListBoxItem> einzeln anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bc16c-103">An application developer can create <xref:System.Windows.Controls.ListBox> controls without specifying the contents of each <xref:System.Windows.Controls.ListBoxItem> separately.</span></span> <span data-ttu-id="bc16c-104">Sie können Datenbindung verwenden, um Daten an die einzelnen Elemente zu binden.</span><span class="sxs-lookup"><span data-stu-id="bc16c-104">You can use data binding to bind data to the individual items.</span></span>  
  
 <span data-ttu-id="bc16c-105">Im folgenden Beispiel wird gezeigt, wie ein erstellt <xref:System.Windows.Controls.ListBox> wird, das die <xref:System.Windows.Controls.ListBoxItem> Elemente nach Datenbindung mit einer Datenquelle mit dem Namen *Colors* auffüllt.</span><span class="sxs-lookup"><span data-stu-id="bc16c-105">The following example shows how to create a <xref:System.Windows.Controls.ListBox> that populates the <xref:System.Windows.Controls.ListBoxItem> elements by data binding to a data source called *Colors*.</span></span> <span data-ttu-id="bc16c-106">In diesem Fall ist es nicht erforderlich, <xref:System.Windows.Controls.ListBoxItem> Tags zu verwenden, um den Inhalt der einzelnen Elemente anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bc16c-106">In this case it is not necessary to use <xref:System.Windows.Controls.ListBoxItem> tags to specify the content of each item.</span></span>  
  
## <a name="example"></a><span data-ttu-id="bc16c-107">Beispiel</span><span class="sxs-lookup"><span data-stu-id="bc16c-107">Example</span></span>  
 [!code-xaml[ListBoxEvent#7](~/samples/snippets/csharp/VS_Snippets_Wpf/ListBoxEvent/CSharp/Pane1.xaml#7)]  
[!code-xaml[ListBoxEvent#3](~/samples/snippets/csharp/VS_Snippets_Wpf/ListBoxEvent/CSharp/Pane1.xaml#3)]  
  
## <a name="see-also"></a><span data-ttu-id="bc16c-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc16c-108">See also</span></span>

- <xref:System.Windows.Controls.ListBox>
- <xref:System.Windows.Controls.ListBoxItem>
- [<span data-ttu-id="bc16c-109">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="bc16c-109">Controls</span></span>](../advanced/optimizing-performance-controls.md)
