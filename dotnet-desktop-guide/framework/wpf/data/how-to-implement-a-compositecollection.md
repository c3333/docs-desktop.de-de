---
title: 'Gewusst wie: Implementieren von CompositeCollection'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [WPF], CompositeCollection class
ms.assetid: 0d8fc84c-7920-427f-8ad7-d55ca656c170
ms.openlocfilehash: fe3b7fb1020ac8022113246453d8247ca241449c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978140"
---
# <a name="how-to-implement-a-compositecollection"></a><span data-ttu-id="1e97d-102">Gewusst wie: Implementieren von CompositeCollection</span><span class="sxs-lookup"><span data-stu-id="1e97d-102">How to: Implement a CompositeCollection</span></span>
## <a name="example"></a><span data-ttu-id="1e97d-103">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1e97d-103">Example</span></span>  
 <span data-ttu-id="1e97d-104">Im folgenden Beispiel wird gezeigt, wie mehrere Auflistungen und Elemente mithilfe der-Klasse als eine Liste angezeigt werden <xref:System.Windows.Data.CompositeCollection> .</span><span class="sxs-lookup"><span data-stu-id="1e97d-104">The following example shows how to display multiple collections and items as one list using the <xref:System.Windows.Data.CompositeCollection> class.</span></span> <span data-ttu-id="1e97d-105">In diesem Beispiel `GreekGods` ist ein <xref:System.Collections.ObjectModel.ObservableCollection%601> von `GreekGod` benutzerdefinierten-Objekten.</span><span class="sxs-lookup"><span data-stu-id="1e97d-105">In this example, `GreekGods` is an <xref:System.Collections.ObjectModel.ObservableCollection%601> of `GreekGod` custom objects.</span></span> <span data-ttu-id="1e97d-106">Datenvorlagen werden so definiert, dass `GreekGod` -Objekte und `GreekHero` -Objekte jeweils mit einer Gold-und einer Zyan-Vordergrundfarbe angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1e97d-106">Data templates are defined so that `GreekGod` objects and `GreekHero` objects appear with a gold and a cyan foreground color respectively.</span></span>  
  
 [!code-xaml[CompositeCollections#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CompositeCollections/CS/Window1.xaml#1)]  
  
## <a name="see-also"></a><span data-ttu-id="1e97d-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e97d-107">See also</span></span>

- <xref:System.Windows.Data.CollectionContainer>
- <xref:System.Windows.Controls.ItemsControl.ItemsSource%2A>
- <xref:System.Windows.Data.XmlDataProvider>
- <xref:System.Windows.DataTemplate>
- [<span data-ttu-id="1e97d-108">Übersicht über die Datenbindung</span><span class="sxs-lookup"><span data-stu-id="1e97d-108">Data Binding Overview</span></span>](/dotnet/desktop-wpf/data/data-binding-overview)
- [<span data-ttu-id="1e97d-109">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="1e97d-109">How-to Topics</span></span>](data-binding-how-to-topics.md)
