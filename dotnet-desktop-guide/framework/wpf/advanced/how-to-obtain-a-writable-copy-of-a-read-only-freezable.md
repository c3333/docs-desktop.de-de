---
title: 'Gewusst wie: Erstellen einer überschreibbaren Kopie eines schreibgeschützten Freezable-Objekts'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- cloning Freezable objects [WPF]
- Freezable objects [WPF], modifiable clones
ms.assetid: d028de61-bbe9-4d62-b656-8fe3b1b2ca24
ms.openlocfilehash: 910c5dada6ca82f68992722e4df6b35f9f7497c7
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977752"
---
# <a name="how-to-obtain-a-writable-copy-of-a-read-only-freezable"></a>Gewusst wie: Erstellen einer überschreibbaren Kopie eines schreibgeschützten Freezable-Objekts
Dieses Beispiel zeigt, wie Sie die- <xref:System.Windows.Freezable.Clone%2A> Methode verwenden, um eine schreibgeschützte Kopie eines schreibgeschützten zu erstellen <xref:System.Windows.Freezable> .  
  
 Nachdem ein- <xref:System.Windows.Freezable> Objekt als schreibgeschützt ("eingefroren") markiert wurde, kann es nicht mehr geändert werden. Sie können jedoch die- <xref:System.Windows.Freezable.Clone%2A> Methode verwenden, um einen änderbaren Klon des fixierten Objekts zu erstellen.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein änderbarer Klon eines fixierten <xref:System.Windows.Media.SolidColorBrush> Objekts erstellt.  
  
 [!code-csharp[freezablesample_procedural#CloneExample](~/samples/snippets/csharp/VS_Snippets_Wpf/freezablesample_procedural/CSharp/freezablesample.cs#cloneexample)]
 [!code-vb[freezablesample_procedural#CloneExample](~/samples/snippets/visualbasic/VS_Snippets_Wpf/freezablesample_procedural/visualbasic/freezablesample.vb#cloneexample)]  
  
 Weitere Informationen zu Objekten finden Sie in der Übersicht über frei wählbare <xref:System.Windows.Freezable> [Objekte](freezable-objects-overview.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Freezable>
- <xref:System.Windows.Freezable.CloneCurrentValue%2A>
- [Übersicht über Freezable-Objekte](freezable-objects-overview.md)
- [Artikel zu Vorgehensweisen](base-elements-how-to-topics.md)
