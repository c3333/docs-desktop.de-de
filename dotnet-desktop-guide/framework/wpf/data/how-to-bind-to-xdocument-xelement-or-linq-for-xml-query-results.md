---
title: 'Gewusst wie: Binden an XDocument, XElement oder LINQ für XML-Abfrageergebnisse'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [WPF], binding to XDocument
- data binding [WPF], binding to XElement
ms.assetid: 6a629a49-fe1c-465d-b76a-3dcbf4307b64
ms.openlocfilehash: 070f67f30613d4522a48e08fd1c208fbe5887525
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977333"
---
# <a name="how-to-bind-to-xdocument-xelement-or-linq-for-xml-query-results"></a>Gewusst wie: Binden an XDocument, XElement oder LINQ für XML-Abfrageergebnisse

In diesem Beispiel wird veranschaulicht, wie XML-Daten mithilfe von an eine gebunden werden <xref:System.Windows.Controls.ItemsControl> <xref:System.Xml.Linq.XDocument> .

## <a name="example"></a>Beispiel

Der folgende XAML-Code definiert eine <xref:System.Windows.Controls.ItemsControl> und schließt eine Daten Vorlage für Daten vom Typ `Planet` in den `http://planetsNS` XML-Namespace ein. Ein XML-Datentyp, der in einem Namespace definiert ist, muss den Namespace in geschweiften Klammern enthalten. An einer Position, an der XAML-Markuperweiterungen auftreten können, muss dem Namespace eine Escapesequenz mit geschweiften Klammern vorangestellt werden. Dieser Code bindet an dynamische Eigenschaften, die den <xref:System.Xml.Linq.XContainer.Element%2A> -und- <xref:System.Xml.Linq.XElement.Attribute%2A> Methoden der-Klasse entsprechen <xref:System.Xml.Linq.XElement> . Dynamische Eigenschaften ermöglichen die Bindung von XAML an dynamische Eigenschaften, die die Namen von Methoden gemeinsam verwenden. Weitere Informationen finden Sie unter [LINQ to XML Dynamic Properties](linq-to-xml-dynamic-properties.md). Beachten Sie, dass die XML-Standardnamespacedeklaration nicht für Attributnamen gilt.

[!code-xaml[XLinqExample#StackPanelResources](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml#stackpanelresources)]
[!code-xaml[XLinqExample#ItemsControl](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml#itemscontrol)]

Der folgende c#-Code ruft <xref:System.Xml.Linq.XDocument.Load%2A> auf und legt den Datenkontext des Stapel Bereichs auf alle unter Elemente des Elements `SolarSystemPlanets` im `http://planetsNS` XML-Namespace fest.

[!code-csharp[XLinqExample#LoadDCFromFile](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml.cs#loaddcfromfile)]
[!code-vb[XLinqExample#LoadDCFromFile](~/samples/snippets/visualbasic/VS_Snippets_Wpf/XLinqExample/visualbasic/window1.xaml.vb#loaddcfromfile)]

XML-Daten können mithilfe von als XAML-Ressource gespeichert werden <xref:System.Windows.Data.ObjectDataProvider> . Ein vollständiges Beispiel finden Sie unter  [L2DBForm. XAML-Quellcode](l2dbform-xaml-source-code.md). Im folgenden Beispiel wird gezeigt, wie der Datenkontext in Code auf eine Objektressource festgelegt werden kann.

[!code-csharp[XLinqExample#LoadDCFromXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml.cs#loaddcfromxaml)]
[!code-vb[XLinqExample#LoadDCFromXAML](~/samples/snippets/visualbasic/VS_Snippets_Wpf/XLinqExample/visualbasic/window1.xaml.vb#loaddcfromxaml)]

Die dynamischen Eigenschaften, die zugeordnet werden <xref:System.Xml.Linq.XContainer.Element%2A> und <xref:System.Xml.Linq.XElement.Attribute%2A> Flexibilität innerhalb von XAML bieten. Der Code kann auch an die Ergebnisse einer LINQ to XML-Abfrage gebunden werden. In diesem Beispiel erfolgt die Bindung an die nach einem Elementwert sortierten Abfrageergebnisse.

[!code-csharp[XLinqExample#BindToResults](~/samples/snippets/csharp/VS_Snippets_Wpf/XLinqExample/CSharp/Window1.xaml.cs#bindtoresults)]
[!code-vb[XLinqExample#BindToResults](~/samples/snippets/visualbasic/VS_Snippets_Wpf/XLinqExample/visualbasic/window1.xaml.vb#bindtoresults)]

## <a name="see-also"></a>Siehe auch

- [Übersicht über Bindungsquellen](binding-sources-overview.md)
- [Übersicht über WPF-Datenbindung mit LINQ to XML](wpf-data-binding-with-linq-to-xml-overview.md)
- [WPF-Datenbindung mit LINQ to XML Beispiel](linq-to-xml-data-binding-sample.md)
- [Dynamische Eigenschaften in LINQ to XML](linq-to-xml-dynamic-properties.md)
