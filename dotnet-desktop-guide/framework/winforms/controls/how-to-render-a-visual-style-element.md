---
title: 'Vorgehensweise: Rendern eines visuellen Stilelements'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- visual themes [Windows Forms], applying to elements of Windows Forms applications
- professional appearance [Windows Forms], applying to elements of Windows Forms applications
- visual styles [Windows Forms], rendering Windows Forms controls
ms.assetid: a207781b-1baa-4ce9-b788-1e951bd4b5df
ms.openlocfilehash: a2b9524b6a3e3c77d3c68c4d9e138b8c0e2a9373
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975602"
---
# <a name="how-to-render-a-visual-style-element"></a>Vorgehensweise: Rendern eines visuellen Stilelements
Der- <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> Namespace macht <xref:System.Windows.Forms.VisualStyles.VisualStyleElement> Objekte verfügbar, die die von visuellen Stilen unterstützten Elemente der Windows-Benutzeroberfläche darstellen. In diesem Thema wird veranschaulicht, wie die <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> -Klasse verwendet wird, um das zu Rendering <xref:System.Windows.Forms.VisualStyles.VisualStyleElement> , das die Schaltflächen abmelden und **herunter** **fahren** im Startmenü darstellt.  
  
### <a name="to-render-a-visual-style-element"></a>So Rendering Sie ein visuelles Stilelement  
  
1. Erstellen <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> Sie ein, und legen Sie es auf das zu zeichnende Element fest. Beachten Sie die Verwendung der <xref:System.Windows.Forms.Application.RenderWithVisualStyles%2A?displayProperty=nameWithType> -Eigenschaft und der- <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.IsElementDefined%2A?displayProperty=nameWithType> Methode <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.%23ctor%2A> . der Konstruktor löst eine Ausnahme aus, wenn visuelle Stile deaktiviert sind oder ein Element nicht definiert ist.  
  
     [!code-cpp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#4](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/cpp/form1.cpp#4)]
     [!code-csharp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#4](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/CS/form1.cs#4)]
     [!code-vb[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#4](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/VB/form1.vb#4)]  
  
2. Ruft die- <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer.DrawBackground%2A> Methode auf, um das Element zu Rendering, das das <xref:System.Windows.Forms.VisualStyles.VisualStyleRenderer> gegenwärtig darstellt.  
  
     [!code-cpp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#6](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/cpp/form1.cpp#6)]
     [!code-csharp[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#6](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/CS/form1.cs#6)]
     [!code-vb[System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple#6](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.VisualStyles.VisualStyleRenderer_Simple/VB/form1.vb#6)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Ein benutzerdefiniertes, von der-Klasse abgeleitetes <xref:System.Windows.Forms.Control>  
  
- Ein <xref:System.Windows.Forms.Form> , der das benutzerdefinierte Steuerelement hostet.  
  
- Verweise auf die <xref:System?displayProperty=nameWithType> <xref:System.Drawing?displayProperty=nameWithType> <xref:System.Windows.Forms?displayProperty=nameWithType> <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> Namespaces,, und.  
  
## <a name="see-also"></a>Siehe auch

- [Rendering von Steuerelementen mit visuellen Stilen](rendering-controls-with-visual-styles.md)
