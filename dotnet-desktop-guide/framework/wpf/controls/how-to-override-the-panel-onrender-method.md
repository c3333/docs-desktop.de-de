---
title: 'Gewusst wie: Überschreiben der Panel.OnRender-Methode'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- overriding OnRender method
- Panel control, overriding OnRender method
- OnRender method
- controls, Panel, overriding OnRender method
helpviewer_keywords:
- overriding OnRender method of Panel control [WPF]
- OnRender method [WPF], overriding
- Panel control [WPF], overriding OnRender method
ms.assetid: 57397834-a085-4e36-90ab-416fad98f341
ms.openlocfilehash: 23c3353e130585ed83726816a467ca73f6aa9152
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978161"
---
# <a name="how-to-override-the-panel-onrender-method"></a>Gewusst wie: Überschreiben der Panel.OnRender-Methode
In diesem Beispiel wird gezeigt, wie die-Methode von überschrieben wird, um <xref:System.Windows.Controls.Panel.OnRender%2A> <xref:System.Windows.Controls.Panel> einem Layout-Element benutzerdefinierte grafische Effekte hinzuzufügen.  
  
## <a name="example"></a>Beispiel  
 Verwenden Sie die- <xref:System.Windows.Controls.Panel.OnRender%2A> Methode, um einem gerenderten Panel-Element grafische Effekte hinzuzufügen. Beispielsweise können Sie mit dieser Methode benutzerdefinierte Rahmen-oder Hintergrundeffekte hinzufügen. Ein- <xref:System.Windows.Media.DrawingContext> Objekt wird als Argument übermittelt, das Methoden zum Zeichnen von Formen, Text, Bildern oder Videos bereitstellt. Folglich ist diese Methode nützlich für die Anpassung eines Panel-Objekts.  
  
 [!code-csharp[LightWeightCustomPanel#1](~/samples/snippets/csharp/VS_Snippets_Wpf/LightWeightCustomPanel/CSharp/OffsetPanel.cs#1)]
 [!code-vb[LightWeightCustomPanel#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/LightWeightCustomPanel/visualbasic/offsetpanel.vb#1)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Panel>
- [Übersicht über Panel-Elemente](panels-overview.md)
- [Artikel zu Vorgehensweisen](panel-how-to-topics.md)
