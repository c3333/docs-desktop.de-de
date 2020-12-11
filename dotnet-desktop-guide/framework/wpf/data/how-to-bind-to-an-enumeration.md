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
# <a name="how-to-bind-to-an-enumeration"></a><span data-ttu-id="69819-102">Gewusst wie: Binden an eine Enumeration</span><span class="sxs-lookup"><span data-stu-id="69819-102">How to: Bind to an Enumeration</span></span>
<span data-ttu-id="69819-103">Dieses Beispiel zeigt, wie Sie eine Bindung an eine Enumeration durch Binden an die GetValues-Methode der-Enumeration herstellen.</span><span class="sxs-lookup"><span data-stu-id="69819-103">This example shows how to bind to an enumeration by binding to the enumeration's GetValues method.</span></span>  
  
## <a name="example"></a><span data-ttu-id="69819-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="69819-104">Example</span></span>  
 <span data-ttu-id="69819-105">Im folgenden Beispiel <xref:System.Windows.Controls.ListBox> zeigt die Liste der <xref:System.Windows.HorizontalAlignment> Enumerationswerte durch Datenbindung an.</span><span class="sxs-lookup"><span data-stu-id="69819-105">In the following example, the <xref:System.Windows.Controls.ListBox> displays the list of <xref:System.Windows.HorizontalAlignment> enumeration values through data binding.</span></span> <span data-ttu-id="69819-106"><xref:System.Windows.Controls.ListBox>Und <xref:System.Windows.Controls.Button> sind so gebunden, dass Sie den <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> Eigenschafts Wert von ändern können, <xref:System.Windows.Controls.Button> indem Sie einen Wert in der auswählen <xref:System.Windows.Controls.ListBox> .</span><span class="sxs-lookup"><span data-stu-id="69819-106">The <xref:System.Windows.Controls.ListBox> and the <xref:System.Windows.Controls.Button> are bound such that you can change the <xref:System.Windows.FrameworkElement.HorizontalAlignment%2A> property value of the <xref:System.Windows.Controls.Button> by selecting a value in the <xref:System.Windows.Controls.ListBox>.</span></span>  
  
 [!code-xaml[BindToEnum#BindToEnum](~/samples/snippets/csharp/VS_Snippets_Wpf/BindToEnum/CS/Window1.xaml#bindtoenum)]  
  
## <a name="see-also"></a><span data-ttu-id="69819-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69819-107">See also</span></span>

- [<span data-ttu-id="69819-108">Binden an eine Methode</span><span class="sxs-lookup"><span data-stu-id="69819-108">Bind to a Method</span></span>](how-to-bind-to-a-method.md)
- [<span data-ttu-id="69819-109">Übersicht über die Datenbindung</span><span class="sxs-lookup"><span data-stu-id="69819-109">Data Binding Overview</span></span>](/dotnet/desktop-wpf/data/data-binding-overview)
- [<span data-ttu-id="69819-110">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="69819-110">How-to Topics</span></span>](data-binding-how-to-topics.md)
