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
# <a name="how-to-bind-a-listbox-to-data"></a>Gewusst wie: Binden eines Listenfelds an Daten
Ein Anwendungsentwickler kann Steuer <xref:System.Windows.Controls.ListBox> Elemente erstellen, ohne den Inhalt <xref:System.Windows.Controls.ListBoxItem> einzeln anzugeben. Sie können Datenbindung verwenden, um Daten an die einzelnen Elemente zu binden.  
  
 Im folgenden Beispiel wird gezeigt, wie ein erstellt <xref:System.Windows.Controls.ListBox> wird, das die <xref:System.Windows.Controls.ListBoxItem> Elemente nach Datenbindung mit einer Datenquelle mit dem Namen *Colors* auffüllt. In diesem Fall ist es nicht erforderlich, <xref:System.Windows.Controls.ListBoxItem> Tags zu verwenden, um den Inhalt der einzelnen Elemente anzugeben.  
  
## <a name="example"></a>Beispiel  
 [!code-xaml[ListBoxEvent#7](~/samples/snippets/csharp/VS_Snippets_Wpf/ListBoxEvent/CSharp/Pane1.xaml#7)]  
[!code-xaml[ListBoxEvent#3](~/samples/snippets/csharp/VS_Snippets_Wpf/ListBoxEvent/CSharp/Pane1.xaml#3)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.ListBox>
- <xref:System.Windows.Controls.ListBoxItem>
- [Steuerelemente](../advanced/optimizing-performance-controls.md)
