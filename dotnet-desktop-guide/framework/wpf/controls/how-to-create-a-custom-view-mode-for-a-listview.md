---
title: 'Gewusst wie: Erstellen eines benutzerdefinierten Ansichtsmodus für eine ListView'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- ListView controls [WPF], creating custom View mode
ms.assetid: 71077349-eeb9-4344-ab29-b5df96df3314
ms.openlocfilehash: 3b9ca17bddcecb1895205fca76f0a489ecf25c4f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978073"
---
# <a name="how-to-create-a-custom-view-mode-for-a-listview"></a><span data-ttu-id="f6b74-102">Gewusst wie: Erstellen eines benutzerdefinierten Ansichtsmodus für eine ListView</span><span class="sxs-lookup"><span data-stu-id="f6b74-102">How to: Create a custom view mode for a ListView</span></span>

<span data-ttu-id="f6b74-103">Dieses Beispiel zeigt, wie ein benutzerdefinierter <xref:System.Windows.Controls.ListView.View%2A> Modus für ein Steuerelement erstellt wird <xref:System.Windows.Controls.ListView> .</span><span class="sxs-lookup"><span data-stu-id="f6b74-103">This example shows how to create a custom <xref:System.Windows.Controls.ListView.View%2A> mode for a <xref:System.Windows.Controls.ListView> control.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f6b74-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f6b74-104">Example</span></span>  
 <span data-ttu-id="f6b74-105">Sie müssen die- <xref:System.Windows.Controls.ViewBase> Klasse verwenden, wenn Sie eine benutzerdefinierte Ansicht für das-Steuerelement erstellen <xref:System.Windows.Controls.ListView> .</span><span class="sxs-lookup"><span data-stu-id="f6b74-105">You must use the <xref:System.Windows.Controls.ViewBase> class when you create a custom view for the <xref:System.Windows.Controls.ListView> control.</span></span> <span data-ttu-id="f6b74-106">Das folgende Beispiel zeigt einen Ansichtsmodus `PlainView` , der von der- <xref:System.Windows.Controls.ViewBase> Klasse abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="f6b74-106">The following example shows a view mode called `PlainView` that's derived from the <xref:System.Windows.Controls.ViewBase> class.</span></span>  
  
 [!code-csharp[ListViewCustomView#PlainView](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/PlainView.cs#plainview)]
 [!code-vb[ListViewCustomView#PlainView](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ListViewCustomView/visualbasic/plainview.vb#plainview)]  
  
 <span data-ttu-id="f6b74-107">Verwenden Sie die-Klasse, um einen Stil auf die benutzerdefinierte Ansicht anzuwenden <xref:System.Windows.Style> .</span><span class="sxs-lookup"><span data-stu-id="f6b74-107">To apply a style to the custom view, use the <xref:System.Windows.Style> class.</span></span> <span data-ttu-id="f6b74-108">Im folgenden Beispiel wird ein <xref:System.Windows.Style> für den `PlainView` Ansichtsmodus definiert.</span><span class="sxs-lookup"><span data-stu-id="f6b74-108">The following example defines a <xref:System.Windows.Style> for the `PlainView` view mode.</span></span> <span data-ttu-id="f6b74-109">Im vorherigen Beispiel wird dieser Stil als Wert der-Eigenschaft festgelegt, die <xref:System.Windows.Controls.ViewBase.DefaultStyleKey%2A> für definiert ist `PlainView` .</span><span class="sxs-lookup"><span data-stu-id="f6b74-109">In the previous example, this style is set as the value of the <xref:System.Windows.Controls.ViewBase.DefaultStyleKey%2A> property that's defined for `PlainView`.</span></span>  
  
 [!code-xaml[ListViewCustomView#PlainViewStyle](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/Themes/Generic.xaml#plainviewstyle)]  
  
 <span data-ttu-id="f6b74-110">Um das Layout der Daten in einem benutzerdefinierten Ansichtsmodus zu definieren, definieren Sie ein- <xref:System.Windows.DataTemplate> Objekt.</span><span class="sxs-lookup"><span data-stu-id="f6b74-110">To define the layout of data in a custom view mode, define a <xref:System.Windows.DataTemplate> object.</span></span> <span data-ttu-id="f6b74-111">Im folgenden Beispiel wird ein definiert <xref:System.Windows.DataTemplate> , das zum Anzeigen von Daten im `PlainView` Ansichtsmodus verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6b74-111">The following example defines a <xref:System.Windows.DataTemplate> that can be used to display data in the `PlainView` view mode.</span></span>  
  
 [!code-xaml[ListViewCustomView#PlainViewDataTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/Window1.xaml#plainviewdatatemplate)]  
  
 <span data-ttu-id="f6b74-112">Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.ResourceKey> für den `PlainView` Ansichtsmodus definiert wird, der das verwendet <xref:System.Windows.DataTemplate> , das im vorherigen Beispiel definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f6b74-112">The following example shows how to define a <xref:System.Windows.ResourceKey> for the `PlainView` view mode that uses the <xref:System.Windows.DataTemplate> that is defined in the previous example.</span></span>  
  
 [!code-xaml[ListViewCustomView#PlainViewtileView](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/Window1.xaml#plainviewtileview)]  
  
 <span data-ttu-id="f6b74-113">Ein <xref:System.Windows.Controls.ListView> Steuerelement kann eine benutzerdefinierte Ansicht verwenden, wenn Sie die- <xref:System.Windows.Controls.ListView.View%2A> Eigenschaft auf den Ressourcen Schlüssel festlegen.</span><span class="sxs-lookup"><span data-stu-id="f6b74-113">A <xref:System.Windows.Controls.ListView> control can use a custom view if you set the <xref:System.Windows.Controls.ListView.View%2A> property to the resource key.</span></span> <span data-ttu-id="f6b74-114">Im folgenden Beispiel wird gezeigt, wie `PlainView` als Ansichtsmodus für eine angegeben wird <xref:System.Windows.Controls.ListView> .</span><span class="sxs-lookup"><span data-stu-id="f6b74-114">The following example shows how to specify `PlainView` as the view mode for a <xref:System.Windows.Controls.ListView>.</span></span>  
  
 [!code-csharp[ListViewCustomView#ListViewtileViewmode](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp/Window1.xaml.cs#listviewtileviewmode)]
 [!code-vb[ListViewCustomView#ListViewtileViewmode](~/samples/snippets/visualbasic/VS_Snippets_Wpf/ListViewCustomView/visualbasic/window1.xaml.vb#listviewtileviewmode)]  
  
 <span data-ttu-id="f6b74-115">Das komplette Beispiel finden Sie unter [ListView mit mehreren Ansichten (c#)](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp) oder [ListView mit mehreren Ansichten (Visual Basic)](https://github.com/dotnet/docs/tree/master/samples/snippets/visualbasic/VS_Snippets_Wpf/ListViewCustomView/visualbasic).</span><span class="sxs-lookup"><span data-stu-id="f6b74-115">For the complete sample, see [ListView with Multiple Views (C#)](https://github.com/dotnet/docs/tree/master/samples/snippets/csharp/VS_Snippets_Wpf/ListViewCustomView/CSharp) or [ListView with Multiple Views (Visual Basic)](https://github.com/dotnet/docs/tree/master/samples/snippets/visualbasic/VS_Snippets_Wpf/ListViewCustomView/visualbasic).</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="f6b74-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f6b74-116">See also</span></span>

- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="f6b74-117">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="f6b74-117">How-to Topics</span></span>](listview-how-to-topics.md)
- [<span data-ttu-id="f6b74-118">Übersicht über ListView</span><span class="sxs-lookup"><span data-stu-id="f6b74-118">ListView Overview</span></span>](listview-overview.md)
- [<span data-ttu-id="f6b74-119">Übersicht über GridView</span><span class="sxs-lookup"><span data-stu-id="f6b74-119">GridView Overview</span></span>](gridview-overview.md)
