---
title: 'Gewusst wie: Formatieren einer Zeile in einem ListView-Steuer Punkt, der eine GridView verwendet'
ms.date: 03/30/2017
helpviewer_keywords:
- GridView controls [WPF], styling rows
- styling rows in ListViews implementing GridViews [WPF]
- ListView controls [WPF], styling rows with GridViews
ms.assetid: 2e406ba2-70a0-4e62-841f-0934859de76e
ms.openlocfilehash: 586c549cca6ef3089b37427c7983bb39e56509bf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974663"
---
# <a name="how-to-style-a-row-in-a-listview-that-implements-a-gridview"></a><span data-ttu-id="3ba19-102">Gewusst wie: Formatieren einer Zeile in einem ListView, in dem ein GridView implementiert ist</span><span class="sxs-lookup"><span data-stu-id="3ba19-102">How to: Style a Row in a ListView That Implements a GridView</span></span>
<span data-ttu-id="3ba19-103">Dieses Beispiel zeigt, wie eine Zeile in einem-Steuerelement formatieren wird <xref:System.Windows.Controls.ListView> , das einen- <xref:System.Windows.Controls.GridView> <xref:System.Windows.Controls.ListView.View%2A> Modus verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ba19-103">This example shows how to style a row in a <xref:System.Windows.Controls.ListView> control that uses a <xref:System.Windows.Controls.GridView> <xref:System.Windows.Controls.ListView.View%2A> mode.</span></span>  
  
## <a name="example"></a><span data-ttu-id="3ba19-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="3ba19-104">Example</span></span>  
 <span data-ttu-id="3ba19-105">Sie können eine Zeile in einem-Steuerelement formatieren, <xref:System.Windows.Controls.ListView> indem Sie ein <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> für das-Steuerelement festlegen <xref:System.Windows.Controls.ListView> .</span><span class="sxs-lookup"><span data-stu-id="3ba19-105">You can style a row in a <xref:System.Windows.Controls.ListView> control by setting an <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> on the <xref:System.Windows.Controls.ListView> control.</span></span> <span data-ttu-id="3ba19-106">Legen Sie den Stil für die Elemente fest, die als-Objekte dargestellt werden <xref:System.Windows.Controls.ListViewItem> .</span><span class="sxs-lookup"><span data-stu-id="3ba19-106">Set the style for its items that are represented as <xref:System.Windows.Controls.ListViewItem> objects.</span></span> <span data-ttu-id="3ba19-107">Der <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> verweist <xref:System.Windows.Controls.ControlTemplate> auf die Objekte, die zum Anzeigen des Zeilen Inhalts verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ba19-107">The <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> references the <xref:System.Windows.Controls.ControlTemplate> objects that are used to display the row content.</span></span>  
  
 <span data-ttu-id="3ba19-108">Das komplette Beispiel, aus dem die folgenden Beispiele extrahiert werden, zeigt eine Auflistung von Songinformationen an, die in einer XML-Datenbank gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="3ba19-108">The complete sample, which the following examples are extracted from, displays a collection of song information that is stored in an XML database.</span></span> <span data-ttu-id="3ba19-109">Jeder Titel in der Datenbank verfügt über ein Bewertungsfeld, und der Wert dieses Felds gibt an, wie eine Zeile mit den zugehörigen Informationen angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ba19-109">Each song in the database has a rating field and the value of this field specifies how to display a row of song information.</span></span>  
  
 <span data-ttu-id="3ba19-110">Im folgenden Beispiel wird gezeigt, wie <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> für die-Objekte definiert wird <xref:System.Windows.Controls.ListViewItem> , die die-Lieder in der Song-Auflistung darstellen.</span><span class="sxs-lookup"><span data-stu-id="3ba19-110">The following example shows how to define <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> for the <xref:System.Windows.Controls.ListViewItem> objects that represent the songs in the song collection.</span></span> <span data-ttu-id="3ba19-111">Die <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> verweist <xref:System.Windows.Controls.ControlTemplate> auf-Objekte, die angeben, wie eine Zeile mit Songinformationen angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ba19-111">The <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> references <xref:System.Windows.Controls.ControlTemplate> objects that specify how to display a row of song information.</span></span>  
  
 [!code-xaml[ListViewItemStyleSnippet#ItemContainerStyle](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#itemcontainerstyle)]  
  
 <span data-ttu-id="3ba19-112">Das folgende Beispiel zeigt einen <xref:System.Windows.Controls.ControlTemplate> , der die Text Zeichenfolge der `"Strongly Recommended"` Zeile hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="3ba19-112">The following example shows a <xref:System.Windows.Controls.ControlTemplate> that adds the text string `"Strongly Recommended"` to the row.</span></span> <span data-ttu-id="3ba19-113">Auf diese Vorlage wird im verwiesen, <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> und wird angezeigt, wenn die Bewertung des Titels den Wert 5 (fünf) aufweist.</span><span class="sxs-lookup"><span data-stu-id="3ba19-113">This template is referenced in the <xref:System.Windows.Controls.ItemsControl.ItemContainerStyle%2A> and displays when the song's rating has a value of 5 (five).</span></span> <span data-ttu-id="3ba19-114"><xref:System.Windows.Controls.ControlTemplate>Enthält ein- <xref:System.Windows.Controls.GridViewRowPresenter> Objekt, das den Inhalt der Zeile in Spalten festlegt, wie im <xref:System.Windows.Controls.GridView> Ansichtsmodus definiert.</span><span class="sxs-lookup"><span data-stu-id="3ba19-114">The <xref:System.Windows.Controls.ControlTemplate> includes a <xref:System.Windows.Controls.GridViewRowPresenter> object that lays out the contents of the row in columns as defined by the <xref:System.Windows.Controls.GridView> view mode.</span></span>  
  
 [!code-xaml[ListViewItemStyleSnippet#ControlTemplate](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#controltemplate)]  
  
 <span data-ttu-id="3ba19-115">Im folgenden Beispiel wird definiert <xref:System.Windows.Controls.GridView> .</span><span class="sxs-lookup"><span data-stu-id="3ba19-115">The following example defines <xref:System.Windows.Controls.GridView>.</span></span>  
  
 [!code-xaml[ListViewItemStyleSnippet#GridView](~/samples/snippets/csharp/VS_Snippets_Wpf/ListViewItemStyleSnippet/CS/Window1.xaml#gridview)]  
  
## <a name="see-also"></a><span data-ttu-id="3ba19-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ba19-116">See also</span></span>

- <xref:System.Windows.Controls.ListView>
- <xref:System.Windows.Controls.GridView>
- [<span data-ttu-id="3ba19-117">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="3ba19-117">How-to Topics</span></span>](listview-how-to-topics.md)
- [<span data-ttu-id="3ba19-118">Übersicht über ListView</span><span class="sxs-lookup"><span data-stu-id="3ba19-118">ListView Overview</span></span>](listview-overview.md)
- [<span data-ttu-id="3ba19-119">Erstellen von Formaten und Vorlagen</span><span class="sxs-lookup"><span data-stu-id="3ba19-119">Styling and Templating</span></span>](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
