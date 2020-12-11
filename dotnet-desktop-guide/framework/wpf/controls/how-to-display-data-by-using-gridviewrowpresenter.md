---
title: 'Gewusst wie: Anzeigen von Daten durch Verwenden von GridViewRowPresenter'
ms.date: 03/30/2017
helpviewer_keywords:
- displaying data with GridViewRowPresenter [WPF]
- GridViewRowPresenter [WPF]
ms.assetid: bdb785a5-a262-44d5-a517-ea14383e5f70
ms.openlocfilehash: 0e471df3ab6fd10417fc58ece4cdb8ff1c457c95
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977811"
---
# <a name="how-to-display-data-by-using-gridviewrowpresenter"></a><span data-ttu-id="dcaac-102">Gewusst wie: Anzeigen von Daten durch Verwenden von GridViewRowPresenter</span><span class="sxs-lookup"><span data-stu-id="dcaac-102">How to: Display Data by Using GridViewRowPresenter</span></span>
<span data-ttu-id="dcaac-103">Dieses Beispiel zeigt, wie das <xref:System.Windows.Controls.GridViewRowPresenter> -Objekt und das-Objekt verwendet werden <xref:System.Windows.Controls.GridViewHeaderRowPresenter> , um Daten in Spalten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dcaac-103">This example shows how to use the <xref:System.Windows.Controls.GridViewRowPresenter> and <xref:System.Windows.Controls.GridViewHeaderRowPresenter> objects to display data in columns.</span></span>  
  
## <a name="example"></a><span data-ttu-id="dcaac-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="dcaac-104">Example</span></span>  
 <span data-ttu-id="dcaac-105">Im folgenden Beispiel wird gezeigt, wie ein angegeben <xref:System.Windows.Controls.GridViewColumnCollection> wird, das den <xref:System.DateTime.DayOfWeek%2A> und den <xref:System.DateTime.Year%2A> eines- <xref:System.DateTime> Objekts mithilfe der <xref:System.Windows.Controls.GridViewRowPresenter> -und- <xref:System.Windows.Controls.GridViewHeaderRowPresenter> Objekte anzeigt.</span><span class="sxs-lookup"><span data-stu-id="dcaac-105">The following example shows how to specify a <xref:System.Windows.Controls.GridViewColumnCollection> that displays the <xref:System.DateTime.DayOfWeek%2A> and <xref:System.DateTime.Year%2A> of a <xref:System.DateTime> object by using <xref:System.Windows.Controls.GridViewRowPresenter> and <xref:System.Windows.Controls.GridViewHeaderRowPresenter> objects.</span></span> <span data-ttu-id="dcaac-106">Im Beispiel wird auch ein <xref:System.Windows.Style> für die <xref:System.Windows.Controls.GridViewColumn.Header%2A> eines definiert <xref:System.Windows.Controls.GridViewColumn> .</span><span class="sxs-lookup"><span data-stu-id="dcaac-106">The example also defines a <xref:System.Windows.Style> for the <xref:System.Windows.Controls.GridViewColumn.Header%2A> of a <xref:System.Windows.Controls.GridViewColumn>.</span></span>  
  
 [!code-xaml[GridViewRowPresenterSample#GridViewRowPresenter](~/samples/snippets/csharp/VS_Snippets_Wpf/GridViewRowPresenterSample/CS/Window1.xaml#gridviewrowpresenter)]  
  
## <a name="see-also"></a><span data-ttu-id="dcaac-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcaac-107">See also</span></span>

- <xref:System.Windows.Controls.GridViewHeaderRowPresenter>
- <xref:System.Windows.Controls.GridViewRowPresenter>
- <xref:System.Windows.Controls.GridViewColumnCollection>
- [<span data-ttu-id="dcaac-108">Übersicht über GridView</span><span class="sxs-lookup"><span data-stu-id="dcaac-108">GridView Overview</span></span>](gridview-overview.md)
