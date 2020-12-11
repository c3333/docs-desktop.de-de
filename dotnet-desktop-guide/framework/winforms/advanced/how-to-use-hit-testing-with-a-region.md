---
title: 'Vorgehensweise: Verwenden von Treffertests mit einem Bereich'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- hit tests [Windows Forms], using regions
- regions [Windows Forms], hit testing
ms.assetid: 3a4c07cb-a40a-4d14-ad35-008f531910a8
ms.openlocfilehash: 136f15f1364fb2aed791b4a61d0f11411b055967
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975854"
---
# <a name="how-to-use-hit-testing-with-a-region"></a>Vorgehensweise: Verwenden von Treffertests mit einem Bereich
Der Zweck von Treffer Tests besteht darin, zu bestimmen, ob sich der Cursor über einem bestimmten Objekt befindet, z. b. ein Symbol oder eine Schaltfläche.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird ein Plus förmiger Bereich erstellt, indem die Union zweier rechteckiger Bereiche gebildet wird. Angenommen, die Variable `point` enthält den Speicherort des letzten Click. Der Code prüft, ob `point` im Plus-förmigen Bereich ist. Wenn sich der Punkt in der Region (einem Treffer) befindet, wird der Bereich mit einem nicht transparenten roten Pinsel gefüllt. Andernfalls wird der Bereich mit einem semitransparenten roten Pinsel gefüllt.  
  
 [!code-csharp[System.Drawing.MiscLegacyTopics#31](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/CS/Class1.cs#31)]
 [!code-vb[System.Drawing.MiscLegacyTopics#31](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.MiscLegacyTopics/VB/Class1.vb#31)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Das vorherige Beispiel wurde für die Verwendung mit Windows Forms entwickelt und erfordert <xref:System.Windows.Forms.PaintEventArgs> `e` , was ein Parameter von ist <xref:System.Windows.Forms.PaintEventHandler> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Drawing.Region>
- [Bereiche in GDI+](regions-in-gdi.md)
- [Vorgehensweise: Verwenden von Ausschneiden mit einem Bereich](how-to-use-clipping-with-a-region.md)
