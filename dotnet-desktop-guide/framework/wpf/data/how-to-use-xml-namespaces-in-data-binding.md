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
# <a name="how-to-use-xml-namespaces-in-data-binding"></a>Gewusst wie: Verwenden von XML-Namespaces bei der Datenbindung
## <a name="example"></a>Beispiel
 In diesem Beispiel wird gezeigt, wie in der XML-Bindungs Quelle angegebene Namespaces behandelt werden.

 Wenn die XML-Daten die folgende XML-Namespace Definition haben:

 `<rss version="2.0" xmlns:dc="http://purl.org/dc/elements/1.1/">`

 Sie können das- <xref:System.Windows.Data.XmlNamespaceMapping> Element verwenden, um den Namespace einem zuzuordnen <xref:System.Windows.Data.XmlNamespaceMapping.Prefix%2A> , wie im folgenden Beispiel gezeigt. Anschließend können Sie den verwenden <xref:System.Windows.Data.XmlNamespaceMapping.Prefix%2A> , um auf den XML-Namespace zu verweisen. <xref:System.Windows.Controls.ListBox>In diesem Beispiel werden der *Titel* und *DC: Date* der einzelnen *Elemente* angezeigt.

 [!code-xaml[XmlnsBindSnippet#XmlNamespaceMapping](~/samples/snippets/csharp/VS_Snippets_Wpf/XmlnsBindSnippet/CS/Window1.xaml#xmlnamespacemapping)]

 Beachten Sie, dass die <xref:System.Windows.Data.XmlNamespaceMapping.Prefix%2A> von Ihnen angegebene nicht mit der in der XML-Quelle verwendeten identisch ist. wenn sich das Präfix in der XML-Quelle ändert, funktioniert Ihre Zuordnung weiterhin.

 In diesem Beispiel stammen die XML-Daten aus einem Webdienst, aber das- <xref:System.Windows.Data.XmlNamespaceMapping> Element kann auch mit Inline-XML-oder XML-Daten in einer eingebetteten Datei verwendet werden.

## <a name="see-also"></a>Siehe auch

- [Binden an XML-Daten mithilfe von XmlDataProvider-und XPath-Abfragen](how-to-bind-to-xml-data-using-an-xmldataprovider-and-xpath-queries.md)
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
