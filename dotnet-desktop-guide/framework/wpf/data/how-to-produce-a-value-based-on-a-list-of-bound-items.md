---
title: 'Gewusst wie: Erzeugen eines Werts auf Grundlage einer Liste gebundener Elemente'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- data binding [WPF], MultiBinding
- Multibinding [WPF]
ms.assetid: b3d06378-b511-4181-95aa-316d60c9229b
ms.openlocfilehash: ab030fbf4335a5bfd12834cb7b19c280487dc2f7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974652"
---
# <a name="how-to-produce-a-value-based-on-a-list-of-bound-items"></a>Gewusst wie: Erzeugen eines Werts auf Grundlage einer Liste gebundener Elemente
<xref:System.Windows.Data.MultiBinding> ermöglicht das Binden einer Bindungs Ziel Eigenschaft an eine Liste von Quell Eigenschaften und das anschließende Anwenden von Logik, um einen Wert mit den angegebenen Eingaben zu erhalten. In diesem Beispiel wird die Verwendung von veranschaulicht <xref:System.Windows.Data.MultiBinding> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel verweist `NameListData` auf eine Auflistung von `PersonName`-Objekten, bei denen es sich um Objekte handelt, die zwei Eigenschaften enthalten, `firstName` und `lastName`. Im folgenden Beispiel wird ein <xref:System.Windows.Controls.TextBlock> -Wert erstellt, der den vor-und Nachnamen einer Person anzeigt, deren Nachname zuerst ist.  
  
 [!code-xaml[MultiBinding#Resources1](~/samples/snippets/csharp/VS_Snippets_Wpf/MultiBinding/CSharp/Window1.xaml#resources1)]  
[!code-xaml[MultiBinding#Resources2](~/samples/snippets/csharp/VS_Snippets_Wpf/MultiBinding/CSharp/Window1.xaml#resources2)]  
[!code-xaml[MultiBinding#MultiBindingTextBox2](~/samples/snippets/csharp/VS_Snippets_Wpf/MultiBinding/CSharp/Window1.xaml#multibindingtextbox2)]  
[!code-xaml[MultiBinding#Window](~/samples/snippets/csharp/VS_Snippets_Wpf/MultiBinding/CSharp/Window1.xaml#window)]  
  
 Um zu verstehen, wie das Format „Nachname-Vorname“ erzeugt wird, betrachten Sie zunächst die Implementierung von `NameConverter`:  
  
 [!code-csharp[MultiBinding#3](~/samples/snippets/csharp/VS_Snippets_Wpf/MultiBinding/CSharp/NameConverter.cs#3)]
 [!code-vb[MultiBinding#3](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MultiBinding/VisualBasic/NameConverter.vb#3)]  
  
 `NameConverter` implementiert die <xref:System.Windows.Data.IMultiValueConverter>-Schnittstelle. `NameConverter` übernimmt die Werte aus den einzelnen Bindungen und speichert sie im Werteobjektarray. Die Reihenfolge, in der die <xref:System.Windows.Data.Binding> Elemente unter dem- <xref:System.Windows.Data.MultiBinding> Element angezeigt werden, ist die Reihenfolge, in der diese Werte im Array gespeichert werden. Auf den Wert des- <xref:System.Windows.Data.MultiBinding.ConverterParameter%2A> Attributs wird durch das Parameter-Argument der- <xref:System.Windows.Data.MultiBinding.Converter%2A> Methode verwiesen, das einen Switch für den-Parameter ausführt, um zu bestimmen, wie der Name formatiert werden soll.  
  
## <a name="see-also"></a>Siehe auch

- [Gebundene Daten konvertieren](how-to-convert-bound-data.md)
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
