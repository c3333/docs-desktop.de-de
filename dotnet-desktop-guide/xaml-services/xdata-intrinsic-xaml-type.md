---
title: Systeminterner x:XData-XAML-Typ
ms.date: 03/30/2017
f1_keywords:
- x:XData
- XData
- xXData
helpviewer_keywords:
- XAML [XAML Services], x:XData directive element
- XData in XAML [XAML Services]
- x:XData XAML directive element [XAML Services]
ms.assetid: 7ce209c2-621b-4977-b643-565f7e663534
ms.openlocfilehash: 89bdae68608db235b76d6a9b210c77f97bcebe00
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975394"
---
# <a name="xxdata-intrinsic-xaml-type"></a>Systeminterner x:XData-XAML-Typ
Ermöglicht die Platzierung von XML-Dateninseln in einer XAML-Produktion. XML-Elemente in `x:XData` sollten nicht von XAML-Prozessoren behandelt werden, als ob Sie Teil des aktiven XAML-Standard Namespace oder eines anderen XAML-Namespace sind. `x:XData` kann beliebige wohlgeformte XML-Daten enthalten.

## <a name="xaml-object-element-usage"></a>Verwendung von XAML-Objektelementen

```xaml
<x:XData>
  <elementDataRoot>
    [elementData]
  </elementDataRoot>
</x:XData>
```

## <a name="xaml-values"></a>XAML-Werte

|||
|-|-|
|`elementDataRoot`|Das einzelne Stamm Element der eingeschlossenen Daten Insel. Bei den meisten möglichen Consumern wird XML, das keinen einzelnen Stamm hat, als ungültig betrachtet. Insbesondere ist ein einzelner Stamm erforderlich, wenn der `x:XData` als XML-Datenquelle für WPF oder viele andere Technologien gedacht ist, die XML-Quellen für die Datenbindung verwenden.|
|`[elementData]`|Optional. XML-Code, der die XML-Daten darstellt. Eine beliebige Anzahl von Elementen kann als Elementdaten enthalten sein, und in anderen Elementen können sich auch die in der Tabelle enthaltenen Elemente befinden. Allerdings gelten die allgemeinen Regeln von XML.|

## <a name="remarks"></a>Bemerkungen

Die XML-Elemente in einem- `x:XData` Objekt können alle möglichen Namespaces und Präfixe des enthaltenden XMLDOM in den Daten erneut deklarieren.

Programm gesteuerter Zugriff auf XML-Daten und den systeminternen `x:XData` XAML-Typ ist in .net XAML-Diensten durch die- <xref:System.Windows.Markup.XData> Klasse möglich.

## <a name="wpf-usage-notes"></a>Hinweise zur WPF-Verwendung

Das- `x:XData` Objekt wird primär als untergeordnetes Objekt eines <xref:System.Windows.Data.XmlDataProvider> oder alternativ als untergeordnetes Objekt der- <xref:System.Windows.Data.XmlDataProvider.XmlSerializer%2A?displayProperty=nameWithType> Eigenschaft verwendet (in XAML wird dies in der Regel in der Eigenschafts Element Syntax ausgedrückt).

Die Daten sollten in der Regel den Basis-XML-Namespace innerhalb der Daten Insel neu definieren, sodass er ein neuer XML-Standard Namespace ist (auf eine leere Zeichenfolge festgelegt). Dies ist für einfache Dateninseln am einfachsten, weil die <xref:System.Windows.Data.Binding.XPath%2A> Ausdrücke, mit denen auf die Daten verwiesen und diese gebunden werden, die Einbindung von Präfixen vermeiden können. Komplexere Dateninseln definieren möglicherweise mehrere Präfixe für die Daten und verwenden ein bestimmtes Präfix für den XML-Namespace im Stammverzeichnis. In diesem Fall sollten alle <xref:System.Windows.Data.Binding.XPath%2A> Ausdrucks Verweise das entsprechende, Namespace zugeordnete Präfix enthalten. Weitere Informationen finden Sie unter [Übersicht über die Datenbindung](../net/wpf/data/data-binding-overview.md).

Technisch `x:XData` kann als Inhalt einer beliebigen Eigenschaft des Typs verwendet werden <xref:System.Xml.Serialization.IXmlSerializable> . Ist jedoch <xref:System.Windows.Data.XmlDataProvider.XmlSerializer%2A?displayProperty=nameWithType> die einzige bedeutende Implementierung.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Data.XmlDataProvider>
- [Übersicht über die Datenbindung](../net/wpf/data/data-binding-overview.md)
- [Bindungs Markup Erweiterung](../framework/wpf/advanced/binding-markup-extension.md)
