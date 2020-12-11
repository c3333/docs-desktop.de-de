---
title: 'Gewusst wie: Binden an eine Enumeration'
ms.date: 03/30/2017
helpviewer_keywords:
- binding data [WPF], enumeration
- data binding [WPF], enumeration
- enumeration [WPF]
ms.assetid: b9091eba-1119-424e-868b-d1a4168b3732
ms.openlocfilehash: c92f1f00aa3feb37b70aa9a3647265236a1625b2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972438"
---
# <a name="how-to-bind-to-an-enumeration"></a>Gewusst wie: Binden an eine Enumeration
Dieses Beispiel zeigt, wie Sie eine Bindung an eine Enumeration durch Binden an die GetValues-Methode der-Enumeration herstellen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel <xref:System.Windows.Controls.ListBox> zeigt die Liste der <xref:System.Windows.HorizontalAlignment> Enumerationswerte durch Datenbindung an. <xref:System.Windows.Controls.ListBox>Und <xref:System.Windows.Controls.Button> sind so gebunden, dass Sie den <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> Eigenschafts Wert von ändern können, <xref:System.Windows.Controls.Button> indem Sie einen Wert in der auswählen <xref:System.Windows.Controls.ListBox> .  
  
 [!code-xaml[BindToEnum#BindToEnum](~/samples/snippets/csharp/VS_Snippets_Wpf/BindToEnum/CS/Window1.xaml#bindtoenum)]  
  
## <a name="see-also"></a>Siehe auch

- [Binden an eine Methode](how-to-bind-to-a-method.md)
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
