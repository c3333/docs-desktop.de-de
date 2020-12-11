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
# <a name="how-to-display-listview-contents-by-using-a-gridview"></a>Gewusst wie: Anzeigen von ListView-Inhalten mit GridView
In diesem Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.GridView> Ansichtsmodus für ein-Steuerelement definiert wird <xref:System.Windows.Controls.ListView> .  
  
## <a name="example"></a>Beispiel  
 Sie können den Ansichtsmodus eines <xref:System.Windows.Controls.GridView> durch Angeben von- <xref:System.Windows.Controls.GridViewColumn> Objekten definieren. Im folgenden Beispiel wird gezeigt, wie Sie- <xref:System.Windows.Controls.GridViewColumn> Objekte definieren, die an den für das-Steuerelement angegebenen Dateninhalt gebunden werden <xref:System.Windows.Controls.ListView> . <xref:System.Windows.Controls.GridView>In diesem Beispiel werden drei-Objekte angegeben, die <xref:System.Windows.Controls.GridViewColumn> den `FirstName` `LastName` Feldern, und des zugeordnet sind, `EmployeeNumber` `EmployeeInfoDataSource` das als des-Steuer Elements festgelegt wird <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A> <xref:System.Windows.Controls.ListView> .  
  
 [!code-xaml[ListViewCode#ListViewEmployee](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCode/CSharp/Window1.xaml#listviewemployee)]  
  
 In der folgenden Abbildung wird gezeigt, wie dieses Beispiel angezeigt wird.  
  
 ![Screenshot, der eine ListView mit GridView-Ausgabe zeigt.](./media/gridview-overview/listview-gridview-output.jpg)  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [Übersicht über ListView](listview-overview.md)
- [Übersicht über GridView](gridview-overview.md)
- [Artikel zu Vorgehensweisen](listview-how-to-topics.md)
