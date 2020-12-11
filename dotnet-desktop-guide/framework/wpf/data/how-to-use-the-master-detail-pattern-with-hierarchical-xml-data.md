---
title: 'Gewusst wie: Verwenden des Master/Detail-Musters mit hierarchischen XML-Daten'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], Master-Detail data paradigm
- Master-Detail data paradigm
ms.assetid: eb8dbdd8-5871-42bb-a16b-04e655fea677
ms.openlocfilehash: 0fe42d57fcaf4acee09340fdb3f5df73d7291566
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976549"
---
# <a name="how-to-use-the-master-detail-pattern-with-hierarchical-xml-data"></a>Gewusst wie: Verwenden des Master/Detail-Musters mit hierarchischen XML-Daten
Dieses Beispiel zeigt, wie das Master/Detail-Szenario mit XML-Daten implementiert wird.  
  
## <a name="example"></a>Beispiel  
 Dieses Beispiel ist die XML-Daten Version des Beispiels, das unter [Verwenden des Master-Detail Musters mit hierarchischen Daten](how-to-use-the-master-detail-pattern-with-hierarchical-data.md)beschrieben wird. In diesem Beispiel werden die Daten aus der Datei entfernt `League.xml` . Beachten Sie, wie das dritte-Steuerelement die <xref:System.Windows.Controls.ListBox> Auswahl Änderungen im zweiten-Steuerelement nachverfolgt <xref:System.Windows.Controls.ListBox> , indem es an die <xref:System.Windows.Controls.Primitives.Selector.SelectedValue%2A>  
  
 [!code-xaml[MasterDetailXml#HowTo1](~/samples/snippets/csharp/VS_Snippets_Wpf/MasterDetailXml/CS/Window1.xaml#howto1)]  
[!code-xaml[MasterDetailXml#HowTo2](~/samples/snippets/csharp/VS_Snippets_Wpf/MasterDetailXml/CS/Window1.xaml#howto2)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.HierarchicalDataTemplate>
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
