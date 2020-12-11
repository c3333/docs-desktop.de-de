---
title: 'Gewusst wie: Positionieren von untergeordneten Elementen mithilfe der angefügten Eigenschaften von Canvas'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- attached properties [WPF Designer]
- Canvas control [WPF], attached properties
ms.assetid: 48f1d25d-3820-4107-a4cc-d6c1e5664a44
ms.openlocfilehash: 347c8502bd4c5fafcde7a142327f85bfb75b9954
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974656"
---
# <a name="how-to-use-the-attached-properties-of-canvas-to-position-child-elements"></a>Gewusst wie: Positionieren von untergeordneten Elementen mithilfe der angefügten Eigenschaften von Canvas
In diesem Beispiel wird gezeigt, wie die angefügten Eigenschaften von verwendet werden <xref:System.Windows.Controls.Canvas> , um untergeordnete Elemente zu positionieren.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel werden vier- <xref:System.Windows.Controls.Button> Elemente als untergeordnete Elemente eines übergeordneten Elements hinzugefügt <xref:System.Windows.Controls.Canvas> . Jedes Element wird durch <xref:System.Windows.Controls.Canvas.Bottom%2A> , <xref:System.Windows.Controls.Canvas.Left%2A> , und dargestellt <xref:System.Windows.Controls.Canvas.Right%2A> <xref:System.Windows.Controls.Canvas.Top%2A> .
Beide werden <xref:System.Windows.Controls.Button> relativ zum übergeordneten Element <xref:System.Windows.Controls.Canvas> und entsprechend dem zugewiesenen Eigenschafts Wert positioniert.  
  
 [!code-cpp[CanvasAttachedProperties#1](~/samples/snippets/cpp/VS_Snippets_Wpf/CanvasAttachedProperties/CPP/CanvasAttachedProps.cpp#1)]
 [!code-csharp[CanvasAttachedProperties#1](~/samples/snippets/csharp/VS_Snippets_Wpf/CanvasAttachedProperties/CSharp/CanvasAttachedProps.cs#1)]
 [!code-vb[CanvasAttachedProperties#1](~/samples/snippets/visualbasic/VS_Snippets_Wpf/CanvasAttachedProperties/VisualBasic/CanvasAttachedProps.vb#1)]  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Controls.Canvas>
- <xref:System.Windows.Controls.Canvas.Bottom%2A>
- <xref:System.Windows.Controls.Canvas.Left%2A>
- <xref:System.Windows.Controls.Canvas.Right%2A>
- <xref:System.Windows.Controls.Canvas.Top%2A>
- <xref:System.Windows.Controls.Button>
- [Übersicht über Panel-Elemente](panels-overview.md)
- [Artikel zu Vorgehensweisen](canvas-how-to-topics.md)
- [Übersicht über angefügte Eigenschaften](../advanced/attached-properties-overview.md)
