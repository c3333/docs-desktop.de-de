---
title: 'Gewusst wie: Erstellen einer einfachen Bindung'
description: Erstellen Sie mithilfe dieser Vorgehensweise in Windows Presentation Foundation (WPF) eine einfache Bindung für Ihre Anwendungen.
ms.date: 03/30/2017
helpviewer_keywords:
- simple binding [WPF], creating
- data binding [WPF], creating simple bindings
- binding data [WPF], creating
ms.assetid: 69b80f72-6259-44cb-8294-5bdcebca1e08
ms.openlocfilehash: 9649116427c7da805323270fe3a23e6b23d330a5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977181"
---
# <a name="how-to-create-a-simple-binding"></a><span data-ttu-id="0ed2c-103">Gewusst wie: Erstellen einer einfachen Bindung</span><span class="sxs-lookup"><span data-stu-id="0ed2c-103">How to: Create a Simple Binding</span></span>
<span data-ttu-id="0ed2c-104">In diesem Beispiel wird gezeigt, wie ein einfaches erstellt wird <xref:System.Windows.Data.Binding> .</span><span class="sxs-lookup"><span data-stu-id="0ed2c-104">This example shows you how to create a simple <xref:System.Windows.Data.Binding>.</span></span>  
  
## <a name="example"></a><span data-ttu-id="0ed2c-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0ed2c-105">Example</span></span>  
 <span data-ttu-id="0ed2c-106">In diesem Beispiel verfügen Sie über ein- `Person` Objekt mit der Zeichen folgen Eigenschaft `PersonName` .</span><span class="sxs-lookup"><span data-stu-id="0ed2c-106">In this example, you have a `Person` object with a string property named `PersonName`.</span></span> <span data-ttu-id="0ed2c-107">Das- `Person` Objekt wird im-Namespace mit dem Namen definiert `SDKSample` .</span><span class="sxs-lookup"><span data-stu-id="0ed2c-107">The `Person` object is defined in the namespace called `SDKSample`.</span></span>  
  
 <span data-ttu-id="0ed2c-108">Die markierte Zeile, die das- `<src>` Element im folgenden Beispiel enthält, instanziiert das- `Person` Objekt mit einem- `PersonName` Eigenschafts Wert von `Joe` .</span><span class="sxs-lookup"><span data-stu-id="0ed2c-108">The highlighted line that contains the `<src>` element in the following example instantiates the `Person` object with a `PersonName` property value of `Joe`.</span></span> <span data-ttu-id="0ed2c-109">Dies erfolgt im `Resources` -Abschnitt und wird zugewiesen `x:Key` .</span><span class="sxs-lookup"><span data-stu-id="0ed2c-109">This is done in the `Resources` section and assigned an `x:Key`.</span></span>  
  
 [!code-xaml[SimpleBinding](~/samples/snippets/csharp/VS_Snippets_Wpf/SimpleBinding/CSharp/Page1.xaml?highlight=9,37)]  
  
 <span data-ttu-id="0ed2c-110">Die markierte Zeile, die das-Element enthält, `<TextBlock>` bindet dann das- <xref:System.Windows.Controls.TextBlock> Steuerelement an die- `PersonName` Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="0ed2c-110">The highlighted line that contains the `<TextBlock>` element then binds the <xref:System.Windows.Controls.TextBlock> control to the `PersonName` property.</span></span> <span data-ttu-id="0ed2c-111">Folglich wird der <xref:System.Windows.Controls.TextBlock> mit dem Wert "Joe" angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0ed2c-111">As a result, the <xref:System.Windows.Controls.TextBlock> appears with the value "Joe".</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="0ed2c-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ed2c-112">See also</span></span>

- [<span data-ttu-id="0ed2c-113">Übersicht über die Datenbindung</span><span class="sxs-lookup"><span data-stu-id="0ed2c-113">Data Binding Overview</span></span>](/dotnet/desktop-wpf/data/data-binding-overview)
- [<span data-ttu-id="0ed2c-114">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="0ed2c-114">How-to Topics</span></span>](data-binding-how-to-topics.md)
