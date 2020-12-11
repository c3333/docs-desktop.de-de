---
title: 'Gewusst wie: Anzeigen von ListView-Inhalten mit GridView'
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], displaying contents with GridView
- GridView [WPF], displaying ListView contents
ms.assetid: 5bc1e767-ab46-4f14-bd41-3d5d39e1d000
ms.openlocfilehash: 9b467c95d541c326a41d1ed4bd9eb5c87e25bd5c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977803"
---
# <a name="how-to-display-listview-contents-by-using-a-gridview"></a><span data-ttu-id="f3536-102">Gewusst wie: Anzeigen von ListView-Inhalten mit GridView</span><span class="sxs-lookup"><span data-stu-id="f3536-102">How to: Display ListView Contents by Using a GridView</span></span>
<span data-ttu-id="f3536-103">In diesem Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.GridView> Ansichtsmodus für ein-Steuerelement definiert wird <xref:System.Windows.Controls.ListView> .</span><span class="sxs-lookup"><span data-stu-id="f3536-103">This example shows how to define a <xref:System.Windows.Controls.GridView> view mode for a <xref:System.Windows.Controls.ListView> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f3536-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f3536-104">Example</span></span>  
 <span data-ttu-id="f3536-105">Sie können den Ansichtsmodus eines <xref:System.Windows.Controls.GridView> durch Angeben von- <xref:System.Windows.Controls.GridViewColumn> Objekten definieren.</span><span class="sxs-lookup"><span data-stu-id="f3536-105">You can define the view mode of a <xref:System.Windows.Controls.GridView> by specifying <xref:System.Windows.Controls.GridViewColumn> objects.</span></span> <span data-ttu-id="f3536-106">Im folgenden Beispiel wird gezeigt, wie Sie- <xref:System.Windows.Controls.GridViewColumn> Objekte definieren, die an den für das-Steuerelement angegebenen Dateninhalt gebunden werden <xref:System.Windows.Controls.ListView> .</span><span class="sxs-lookup"><span data-stu-id="f3536-106">The following example shows how to define <xref:System.Windows.Controls.GridViewColumn> objects that bind to the data content that is specified for the <xref:System.Windows.Controls.ListView> control.</span></span> <span data-ttu-id="f3536-107"><xref:System.Windows.Controls.GridView>In diesem Beispiel werden drei-Objekte angegeben, die <xref:System.Windows.Controls.GridViewColumn> den `FirstName` `LastName` Feldern, und des zugeordnet sind, `EmployeeNumber` `EmployeeInfoDataSource` das als des-Steuer Elements festgelegt wird <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> <xref:System.Windows.Controls.ListView> .</span><span class="sxs-lookup"><span data-stu-id="f3536-107">This <xref:System.Windows.Controls.GridView> example specifies three <xref:System.Windows.Controls.GridViewColumn> objects that map to the `FirstName`, `LastName`, and `EmployeeNumber` fields of the `EmployeeInfoDataSource` that is set as the <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> of the <xref:System.Windows.Controls.ListView> control.</span></span>  
  
 [!code-xaml[ListViewCode#ListViewEmployee](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCode/CSharp/Window1.xaml#listviewemployee)]  
  
 <span data-ttu-id="f3536-108">In der folgenden Abbildung wird gezeigt, wie dieses Beispiel angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f3536-108">The following illustration shows how this example appears.</span></span>  
  
 ![Screenshot, der eine ListView mit GridView-Ausgabe zeigt.](./media/gridview-overview/listview-gridview-output.jpg)  
  
## <a name="see-also"></a><span data-ttu-id="f3536-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f3536-110">See also</span></span>

- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="f3536-111">Übersicht über ListView</span><span class="sxs-lookup"><span data-stu-id="f3536-111">ListView Overview</span></span>](listview-overview.md)
- [<span data-ttu-id="f3536-112">Übersicht über GridView</span><span class="sxs-lookup"><span data-stu-id="f3536-112">GridView Overview</span></span>](gridview-overview.md)
- [<span data-ttu-id="f3536-113">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="f3536-113">How-to Topics</span></span>](listview-how-to-topics.md)
