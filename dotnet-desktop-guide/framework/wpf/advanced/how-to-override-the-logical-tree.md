---
title: 'Gewusst wie: Überschreiben der logischen Struktur'
ms.date: 03/30/2017
helpviewer_keywords:
- overriding the logical tree [WPF]
- logical tree [WPF], overriding
ms.assetid: 0ae4d074-8113-4b06-b4fa-e0f39d4967a6
ms.openlocfilehash: bf3459fff1a90326794d6713dd39c73596b0e960
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977751"
---
# <a name="how-to-override-the-logical-tree"></a>Gewusst wie: Überschreiben der logischen Struktur
Obwohl es in den meisten Fällen nicht erforderlich ist, können erfahrene Autoren von Steuerelementen in der logischen Struktur überschreiben.  
  
## <a name="example"></a>Beispiel  
 In diesem Beispiel wird beschrieben, wie die Unterklasse zum über <xref:System.Windows.Controls.StackPanel> Schreiben der logischen Struktur verwendet wird, in diesem Fall, um ein Verhalten zu erzwingen, dass der Bereich möglicherweise nur über ein einzelnes untergeordnetes Element verfügt. Dieses Verhalten ist nicht unbedingt praktisch und erwünscht, aber es dient hier zur Veranschaulichung des Szenarios zum Überschreiben der normalen logischen Struktur eines Elements.  
  
 [!code-csharp[LogicalOverride#SingletonPanel](~/samples/snippets/csharp/VS_Snippets_Wpf/LogicalOverride/CSharp/SDKSampleLibrary/class1.cs#singletonpanel)]  
  
 Weitere Informationen zu der logischen Struktur finden Sie unter [Strukturen in WPF](trees-in-wpf.md).
