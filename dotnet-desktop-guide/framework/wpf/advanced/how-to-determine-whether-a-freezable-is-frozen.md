---
title: 'Gewusst wie: Bestimmen, ob ein Freezable-Objekt fixiert ist'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Freezable objects [WPF], determining if frozen
ms.assetid: 92e58baa-ee12-4a9e-ac3a-ca458807a8b2
ms.openlocfilehash: 6a63862d35f2c40289ea6445eb3dab8a2abe4a61
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976682"
---
# <a name="how-to-determine-whether-a-freezable-is-frozen"></a>Gewusst wie: Bestimmen, ob ein Freezable-Objekt fixiert ist
Dieses Beispiel zeigt, wie Sie bestimmen können, ob ein- <xref:System.Windows.Freezable> Objekt eingefroren ist. Wenn Sie versuchen, ein fixierte <xref:System.Windows.Freezable> Objekt zu ändern, wird eine ausgelöst <xref:System.InvalidOperationException> . Um das Auslösen dieser Ausnahme zu vermeiden, verwenden Sie die- <xref:System.Windows.Freezable.IsFrozen%2A> Eigenschaft des- <xref:System.Windows.Freezable> Objekts, um zu bestimmen, ob es eingefroren ist.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein-Objekt einfriert <xref:System.Windows.Media.SolidColorBrush> und dann mit der- <xref:System.Windows.Freezable.IsFrozen%2A> Eigenschaft getestet, um zu bestimmen, ob es eingefroren ist.  
  
 [!code-csharp[freezablesample_procedural#CheckIsFrozenExample](~/samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#checkisfrozenexample)]
 [!code-vb[freezablesample_procedural#CheckIsFrozenExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#checkisfrozenexample)]  
  
 Weitere Informationen zu Objekten finden Sie in der Übersicht über frei wählbare <xref:System.Windows.Freezable> [Objekte](freezable-objects-overview.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.IsFrozen%2A>
- [Übersicht über Freezable-Objekte](freezable-objects-overview.md)
- [Artikel zu Vorgehensweisen](base-elements-how-to-topics.md)
