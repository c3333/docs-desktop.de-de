---
title: 'Gewusst wie: Löschen von Bindungen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bindings [WPF], clearing
- clearing bindings [WPF]
- data binding [WPF], clearing bindings
ms.assetid: 73962a93-32a9-4bcd-9240-bcfbb239093a
ms.openlocfilehash: ab89c185d1b45ab49e680135ca4c1d54395fe0f4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977187"
---
# <a name="how-to-clear-bindings"></a>Gewusst wie: Löschen von Bindungen
Dieses Beispiel zeigt, wie Bindungen aus einem Objekt gelöscht werden.  
  
## <a name="example"></a>Beispiel  
 Um eine Bindung aus einer einzelnen Eigenschaft eines Objekts zu löschen, müssen Sie <xref:System.Windows.Data.BindingOperations.ClearBinding%2A> wie im folgenden Beispiel gezeigt aufzurufen. Im folgenden Beispiel wird die-Bindung aus dem <xref:System.Windows.Controls.TextBlock.TextProperty> von *MyText*, einem-Objekt, entfernt <xref:System.Windows.Controls.TextBlock> .  
  
 [!code-csharp[CodeOnlyBinding#ClearBinding](~/samples/snippets/csharp/VS_Snippets_Wpf/CodeOnlyBinding/CSharp/binding.cs#clearbinding)]
 [!code-vb[CodeOnlyBinding#ClearBinding](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CodeOnlyBinding/VisualBasic/App.vb#clearbinding)]  
  
 Durch das Löschen einer Bindung wird diese entfernt, sodass die Abhängigkeitseigenschaft einen außerhalb der Bindung gültigen Wert annimmt. Dabei kann es sich um einen Standardwert, einen geerbten Wert oder um einen Wert aus einer Datenvorlagenbindung handeln.  
  
 Um Bindungen aus allen möglichen Eigenschaften eines Objekts zu löschen, verwenden Sie <xref:System.Windows.Data.BindingOperations.ClearAllBindings%2A> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Data.BindingOperations>
- [Übersicht über die Datenbindung](/dotnet/desktop-wpf/data/data-binding-overview)
- [Artikel zu Vorgehensweisen](data-binding-how-to-topics.md)
