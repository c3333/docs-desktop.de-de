---
title: 'Vorgehensweise: Implementieren der IListSource-Schnittstelle'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [Windows Forms], implementing
- IListSource interface
ms.assetid: 63ce27aa-2e23-4fbd-8228-0c1726f6c421
ms.openlocfilehash: 718514c843bbfc0fcc56e89ca0b60bd3ec65b3cf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974723"
---
# <a name="how-to-implement-the-ilistsource-interface"></a><span data-ttu-id="d81a8-102">Vorgehensweise: Implementieren der IListSource-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="d81a8-102">How to: Implement the IListSource Interface</span></span>
<span data-ttu-id="d81a8-103">Implementieren Sie die- <xref:System.ComponentModel.IListSource> Schnittstelle, um eine bindbare Klasse zu erstellen, die nicht implementiert, <xref:System.Collections.IList> sondern eine Liste von einem anderen Speicherort bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d81a8-103">Implement the <xref:System.ComponentModel.IListSource> interface to create a bindable class that does not implement <xref:System.Collections.IList> but instead provides a list from another location.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d81a8-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d81a8-104">Example</span></span>  
 <span data-ttu-id="d81a8-105">Im folgenden Codebeispiel wird veranschaulicht, wie die- <xref:System.ComponentModel.IListSource> Schnittstelle implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="d81a8-105">The following code example demonstrates how to implement the <xref:System.ComponentModel.IListSource> interface.</span></span> <span data-ttu-id="d81a8-106">Eine Komponente namens macht `EmployeeListSource` ein <xref:System.Collections.IList> für die Datenbindung verfügbar, indem die-Methode implementiert wird <xref:System.ComponentModel.IListSource.GetList%2A> .</span><span class="sxs-lookup"><span data-stu-id="d81a8-106">A component named `EmployeeListSource` exposes an <xref:System.Collections.IList> for data binding by implementing the <xref:System.ComponentModel.IListSource.GetList%2A> method.</span></span>  
  
 [!code-csharp[System.ComponentModel.IListSource#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IListSource/CS/EmployeeListSource.cs#1)]
 [!code-vb[System.ComponentModel.IListSource#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IListSource/VB/EmployeeListSource.vb#1)]  
  
 [!code-csharp[System.ComponentModel.IListSource#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IListSource/CS/Employee.cs#10)]
 [!code-vb[System.ComponentModel.IListSource#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IListSource/VB/Employee.vb#10)]  
  
 [!code-csharp[System.ComponentModel.IListSource#100](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IListSource/CS/BusinessObjectBase.cs#100)]
 [!code-vb[System.ComponentModel.IListSource#100](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IListSource/VB/BusinessObjectBase.vb#100)]  
  
 [!code-csharp[System.ComponentModel.IListSource#1000](~/samples/snippets/csharp/VS_Snippets_Winforms/System.ComponentModel.IListSource/CS/Form1.cs#1000)]
 [!code-vb[System.ComponentModel.IListSource#1000](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.ComponentModel.IListSource/VB/Form1.vb#1000)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="d81a8-107">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="d81a8-107">Compiling the Code</span></span>  
 <span data-ttu-id="d81a8-108">Für dieses Beispiel benötigen Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d81a8-108">This example requires:</span></span>  
  
- <span data-ttu-id="d81a8-109">Verweise auf die Assemblys ""System.Drawing" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="d81a8-109">References to the System.Drawing and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d81a8-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d81a8-110">See also</span></span>

- <xref:System.ComponentModel.IListSource>
- <xref:System.ComponentModel.ITypedList>
- <xref:System.ComponentModel.BindingList%601>
- <xref:System.ComponentModel.IBindingList>
- [<span data-ttu-id="d81a8-111">Datenbindung und Windows Forms</span><span class="sxs-lookup"><span data-stu-id="d81a8-111">Data Binding and Windows Forms</span></span>](data-binding-and-windows-forms.md)
