---
title: 'Gewusst wie: Erstellen eines schreibgeschützten Freezable-Objekts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Freezable objects [WPF], making read-only
ms.assetid: 6c544b7d-d3c9-4736-aa90-4b8728234ccb
ms.openlocfilehash: b8dcbec18977d46bd47b82f528deb2eeccc4e441
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976879"
---
# <a name="how-to-make-a-freezable-read-only"></a>Gewusst wie: Erstellen eines schreibgeschützten Freezable-Objekts
Dieses Beispiel zeigt, wie Sie einen schreibgeschützten Vorgang <xref:System.Windows.Freezable> durch Aufrufen seiner-Methode durchführen <xref:System.Windows.Freezable.Freeze%2A> .  
  
 Ein-Objekt kann nicht fixiert <xref:System.Windows.Freezable> werden, wenn eine der folgenden Bedingungen `true` dem-Objekt entspricht:  
  
- Sie verfügt über animierte oder Daten gebundene Eigenschaften.  
  
- Sie verfügt über Eigenschaften, die durch eine dynamische Ressource festgelegt werden. Weitere Informationen zu dynamischen Ressourcen finden Sie in den [XAML-Ressourcen](/dotnet/desktop-wpf/fundamentals/xaml-resources-define).  
  
- Sie enthält <xref:System.Windows.Freezable> untergeordnete Objekte, die nicht eingefroren werden können.  
  
 Wenn diese Bedingungen `false` für Ihr <xref:System.Windows.Freezable> Objekt gelten und Sie diese nicht ändern möchten, sollten Sie es in Erwägung gezogen, um Leistungsvorteile zu erzielen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein- <xref:System.Windows.Media.SolidColorBrush> Objekt, das einen Objekttyp ist, eingefroren <xref:System.Windows.Freezable> .  
  
 [!code-csharp[freezablesample_procedural#FreezeExample1](~/samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#freezeexample1)]
 [!code-vb[freezablesample_procedural#FreezeExample1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#freezeexample1)]  
  
 Weitere Informationen zu Objekten finden Sie in der Übersicht über frei wählbare <xref:System.Windows.Freezable> [Objekte](freezable-objects-overview.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.CanFreeze%2A>
- <xref:System.Windows.Freezable.Freeze%2A>
- [Übersicht über Freezable-Objekte](freezable-objects-overview.md)
- [Artikel zu Vorgehensweisen](base-elements-how-to-topics.md)
