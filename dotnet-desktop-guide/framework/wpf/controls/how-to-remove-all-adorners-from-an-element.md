---
title: 'Gewusst wie: Entfernen aller Adorner aus einem Element'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- adorners [WPF], removing
ms.assetid: fe5303a3-b76e-4643-aafb-51419032b47b
ms.openlocfilehash: 8504bb1ec70de188033b2b092bbb66cf9da3dc11
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978149"
---
# <a name="how-to-remove-all-adorners-from-an-element"></a>Gewusst wie: Entfernen aller Adorner aus einem Element
In diesem Beispiel wird gezeigt, wie alle Adorner aus einem angegebenen Programm gesteuert entfernt werden <xref:System.Windows.UIElement> .  
  
## <a name="example"></a>Beispiel  
 Dieses ausführliche Codebeispiel entfernt alle Adorner in dem Array von Adornern, die von zurückgegeben werden <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> .  In diesem Beispiel werden die Adorner für ein <xref:System.Windows.UIElement> benanntes *MyTextBox*-Element abgerufen.  Wenn das im-aufrufelement angegebene Element <xref:System.Windows.Documents.AdornerLayer.GetAdorners%2A> keine Adorner hat, `null` wird zurückgegeben.  Dieser Code prüft explizit nach einem NULL-Array und eignet sich am besten für Anwendungen, bei denen erwartet wird, dass ein NULL-Array relativ häufig ist.  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersLong](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornerslong)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersLong](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornerslong)]  
  
## <a name="example"></a>Beispiel  
 Dieses komprimierte Codebeispiel ist funktional äquivalent zu dem oben gezeigten ausführlichen Beispiel. In diesem Code wird nicht explizit nach einem NULL-Array gesucht, daher ist es möglich, dass eine- <xref:System.NullReferenceException> Ausnahme ausgelöst wird.  Dieser Code eignet sich am besten für Anwendungen, bei denen erwartet wird, dass ein NULL-Array selten vorkommt.  
  
 [!code-csharp[AdornersMiscCode#_RemoveAllAdornersShort](~/samples/snippets/csharp/VS_Snippets_Wpf/AdornersMiscCode/CSharp/Window1.xaml.cs#_removealladornersshort)]
 [!code-vb[AdornersMiscCode#_RemoveAllAdornersShort](~/samples/snippets/visualbasic/VS_Snippets_Wpf/AdornersMiscCode/visualbasic/window1.xaml.vb#_removealladornersshort)]  
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über Adorner](adorners-overview.md)
