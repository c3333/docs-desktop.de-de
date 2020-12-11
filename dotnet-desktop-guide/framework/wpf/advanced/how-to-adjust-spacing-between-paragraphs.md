---
title: 'Gewusst wie: Anpassen des Abstands zwischen Absätzen'
ms.date: 03/30/2017
helpviewer_keywords:
- spacing between paragraphs [WPF]
- paragraphs [WPF], spacing between
- documents [WPF], adjusting spacing between paragraphs
ms.assetid: 7cd2f2ac-0e19-4587-bfb6-7f5b18c9536e
ms.openlocfilehash: e2a6ba34e3ab15eb316671fef7c11bea03d53c73
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976567"
---
# <a name="how-to-adjust-spacing-between-paragraphs"></a>Gewusst wie: Anpassen des Abstands zwischen Absätzen
In diesem Beispiel wird gezeigt, wie der Abstand zwischen Absätzen in fortlaufendem Inhalt angepasst oder entfernt wird.  
  
 In fortlaufendem Inhalt ist zusätzlicher Platz, der zwischen Absätzen angezeigt wird, das Ergebnis der in diesen Absätzen festgelegten Ränder. Folglich kann der Abstand zwischen Absätzen gesteuert werden, indem die Ränder in diesen Absätzen angepasst werden.  Um einen zusätzlichen Abstand zwischen zwei Absätzen zu vermeiden, legen Sie die Ränder für die Absätze auf **0** fest.  Um einen einheitlichen Abstand zwischen Absätzen innerhalb eines ganzen zu erzielen <xref:System.Windows.Documents.FlowDocument> , verwenden Sie das Format, um einen einheitlichen Rand Wert für alle Absätze in der festzulegen <xref:System.Windows.Documents.FlowDocument> .  
  
 Es ist wichtig zu beachten, dass die Ränder für zwei benachbarte Absätze auf die größere der beiden Ränder reduziert werden, anstatt sich zu verdoppeln. Wenn also zwei benachbarte Absätze jeweils über einen Rand von 20 Pixel und 40 Pixel verfügen, beträgt der resultierende Raum zwischen den Absätzen 40 Pixel, der größere der beiden Rand Werte.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird der Rand für alle Elemente in einem-Wert auf 0 (null) festgelegt <xref:System.Windows.Documents.Paragraph> <xref:System.Windows.Documents.FlowDocument> , wodurch zusätzlicher Abstand zwischen den Absätzen in vermieden wird  <xref:System.Windows.Documents.FlowDocument> .  
  
 [!code-xaml[BlockSnippets#_ParagraphSpacingXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/BlockSnippets/CSharp/Window1.xaml#_paragraphspacingxaml)]
