---
title: 'Gewusst wie: Verwenden von XML-Namespaces bei der Datenbindung'
ms.date: 03/30/2017
helpviewer_keywords:
- XML [WPF], namespaces
- data binding [WPF], XML namespaces
- namespaces [WPF], XML
ms.assetid: a47c832f-dc84-48f2-96d5-cde18fc4284b
ms.openlocfilehash: ad671b81bdfc1c168294123d035ccf7287b3b2fc
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976547"
---
# <a name="how-to-use-xml-namespaces-in-data-binding"></a><span data-ttu-id="60081-102">Gewusst wie: Verwenden von XML-Namespaces bei der Datenbindung</span><span class="sxs-lookup"><span data-stu-id="60081-102">How to: Use XML Namespaces in Data Binding</span></span>
## <a name="example"></a><span data-ttu-id="60081-103">Beispiel</span><span class="sxs-lookup"><span data-stu-id="60081-103">Example</span></span>
 <span data-ttu-id="60081-104">In diesem Beispiel wird gezeigt, wie in der XML-Bindungs Quelle angegebene Namespaces behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="60081-104">This example shows how to handle namespaces specified in your XML binding source.</span></span>

 <span data-ttu-id="60081-105">Wenn die XML-Daten die folgende XML-Namespace Definition haben:</span><span class="sxs-lookup"><span data-stu-id="60081-105">If your XML data has the following XML namespace definition:</span></span>

 `<rss version="2.0" xmlns:dc="http://purl.org/dc/elements/1.1/">`

 <span data-ttu-id="60081-106">Sie können das- <xref:System.Windows.Data.XmlNamespaceMapping> Element verwenden, um den Namespace einem zuzuordnen <xref:System.Windows.Data.XmlNamespaceMapping.Prefix%2A> , wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="60081-106">You can use the <xref:System.Windows.Data.XmlNamespaceMapping> element to map the namespace to a <xref:System.Windows.Data.XmlNamespaceMapping.Prefix%2A>, as in the following example.</span></span> <span data-ttu-id="60081-107">Anschließend können Sie den verwenden <xref:System.Windows.Data.XmlNamespaceMapping.Prefix%2A> , um auf den XML-Namespace zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="60081-107">You can then use the <xref:System.Windows.Data.XmlNamespaceMapping.Prefix%2A> to refer to the XML namespace.</span></span> <span data-ttu-id="60081-108"><xref:System.Windows.Controls.ListBox>In diesem Beispiel werden der *Titel* und *DC: Date* der einzelnen *Elemente* angezeigt.</span><span class="sxs-lookup"><span data-stu-id="60081-108">The <xref:System.Windows.Controls.ListBox> in this example displays the *title* and *dc:date* of each *item*.</span></span>

 [!code-xaml[XmlnsBindSnippet#XmlNamespaceMapping](~/samples/snippets/csharp/VS_Snippets_Wpf/XmlnsBindSnippet/CS/Window1.xaml#xmlnamespacemapping)]

 <span data-ttu-id="60081-109">Beachten Sie, dass die <xref:System.Windows.Data.XmlNamespaceMapping.Prefix%2A> von Ihnen angegebene nicht mit der in der XML-Quelle verwendeten identisch ist. wenn sich das Präfix in der XML-Quelle ändert, funktioniert Ihre Zuordnung weiterhin.</span><span class="sxs-lookup"><span data-stu-id="60081-109">Note that the <xref:System.Windows.Data.XmlNamespaceMapping.Prefix%2A> you specify does not have to match the one used in the XML source; if the prefix changes in the XML source your mapping still works.</span></span>

 <span data-ttu-id="60081-110">In diesem Beispiel stammen die XML-Daten aus einem Webdienst, aber das- <xref:System.Windows.Data.XmlNamespaceMapping> Element kann auch mit Inline-XML-oder XML-Daten in einer eingebetteten Datei verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60081-110">In this particular example, the XML data comes from a web service, but the <xref:System.Windows.Data.XmlNamespaceMapping> element also works with inline XML or XML data in an embedded file.</span></span>

## <a name="see-also"></a><span data-ttu-id="60081-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60081-111">See also</span></span>

- [<span data-ttu-id="60081-112">Binden an XML-Daten mithilfe von XmlDataProvider-und XPath-Abfragen</span><span class="sxs-lookup"><span data-stu-id="60081-112">Bind to XML Data Using an XMLDataProvider and XPath Queries</span></span>](how-to-bind-to-xml-data-using-an-xmldataprovider-and-xpath-queries.md)
- [<span data-ttu-id="60081-113">Übersicht über die Datenbindung</span><span class="sxs-lookup"><span data-stu-id="60081-113">Data Binding Overview</span></span>](/dotnet/desktop-wpf/data/data-binding-overview)
- [<span data-ttu-id="60081-114">Artikel zu Vorgehensweisen</span><span class="sxs-lookup"><span data-stu-id="60081-114">How-to Topics</span></span>](data-binding-how-to-topics.md)
