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
# <a name="how-to-display-data-by-using-gridviewrowpresenter"></a>Gewusst wie: Anzeigen von Daten durch Verwenden von GridViewRowPresenter
Dieses Beispiel zeigt, wie das <xref:System.Windows.Controls.GridViewRowPresenter> -Objekt und das-Objekt verwendet werden <xref:System.Windows.Controls.GridViewHeaderRowPresenter> , um Daten in Spalten anzuzeigen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird gezeigt, wie ein angegeben <xref:System.Windows.Controls.GridViewColumnCollection> wird, das den <xref:System.DateTime.DayOfWeek%2A> und den <xref:System.DateTime.Year%2A> eines- <xref:System.DateTime> Objekts mithilfe der <xref:System.Windows.Controls.GridViewRowPresenter> -und- <xref:System.Windows.Controls.GridViewHeaderRowPresenter> Objekte anzeigt. Im Beispiel wird auch ein <xref:System.Windows.Style> für die <xref:System.Windows.Controls.GridViewColumn.Header%2A> eines definiert <xref:System.Windows.Controls.GridViewColumn> .  
  
 [!code-xaml[GridViewRowPresenterSample#GridViewRowPresenter](~/samples/snippets/csharp/VS_Snippets_Wpf/GridViewRowPresenterSample/CS/Window1.xaml#gridviewrowpresenter)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.GridViewHeaderRowPresenter>
- <xref:System.Windows.Controls.GridViewRowPresenter>
- <xref:System.Windows.Controls.GridViewColumnCollection>
- [Übersicht über GridView](gridview-overview.md)
