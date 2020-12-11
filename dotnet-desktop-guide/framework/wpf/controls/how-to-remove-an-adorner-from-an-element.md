---
title: 'Gewusst wie: Entfernen eines Adorners aus einem Element'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], removing
ms.assetid: 97cf4d9f-0596-429e-8526-32a30aa4ae99
ms.openlocfilehash: 256dd6fa0117f88aec2ef6b60c6dcd4c33b57855
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977035"
---
# <a name="how-to-remove-an-adorner-from-an-element"></a>Gewusst wie: Entfernen eines Adorners aus einem Element
In diesem Beispiel wird gezeigt, wie ein bestimmter Funktions Indikator Programm gesteuert aus einem angegebenen entfernt wird <xref:System.Windows.UIElement> .  
  
## <a name="example"></a>Beispiel  
 In diesem ausführlichen Codebeispiel wird der erste Funktions Indikator in dem Array von Adornern entfernt, das von zurückgegeben wird <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> .  In diesem Beispiel werden die Adorner für ein <xref:System.Windows.UIElement> benanntes *MyTextBox*-Element abgerufen.  Wenn das im-aufrufelement angegebene Element <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> keine Adorner hat, `null` wird zurückgegeben.  Dieser Code prüft explizit nach einem NULL-Array und eignet sich am besten für Anwendungen, bei denen erwartet wird, dass ein NULL-Array relativ häufig ist.  
  
 [!code-csharp[AdornersMiscCode#_RemoveSpecificAdornerLong](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removespecificadornerlong)]
 [!code-vb[AdornersMiscCode#_RemoveSpecificAdornerLong](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removespecificadornerlong)]  
  
## <a name="example"></a>Beispiel  
 Dieses komprimierte Codebeispiel ist funktional äquivalent zu dem oben gezeigten ausführlichen Beispiel. In diesem Code wird nicht explizit nach einem NULL-Array gesucht, daher ist es möglich, dass eine- <xref:System.NullReferenceException> Ausnahme ausgelöst wird.  Dieser Code eignet sich am besten für Anwendungen, bei denen erwartet wird, dass ein NULL-Array selten vorkommt.  
  
 [!code-csharp[AdornersMiscCode#_RemoveSpecificAdornerShort](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removespecificadornershort)]
 [!code-vb[AdornersMiscCode#_RemoveSpecificAdornerShort](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removespecificadornershort)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Adorner](adorners-overview.md)
