---
title: 'Vorgehensweise: Verwenden einer Steuerelementwiedergabeklasse'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- professional appearance [Windows Forms], rendering Windows Forms controls
- visual themes [Windows Forms], applying to Windows Forms controls
- visual styles [Windows Forms], rendering Windows Forms controls
ms.assetid: c0125e34-cd74-4c35-818c-3e40f462b0a3
ms.openlocfilehash: a0f450ff5f169026007002a0d2907ee35e79b29d
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976637"
---
# <a name="how-to-use-a-control-rendering-class"></a>Vorgehensweise: Verwenden einer Steuerelementwiedergabeklasse
In diesem Beispiel wird veranschaulicht, wie die <xref:System.Windows.Forms.ComboBoxRenderer> -Klasse zum Rendering des Dropdown Pfeils eines Kombinations Feld-Steuer Elements verwendet wird. Das Beispiel besteht aus der- <xref:System.Windows.Forms.Control.OnPaint%2A> Methode eines einfachen benutzerdefinierten Steuer Elements. Die- <xref:System.Windows.Forms.ComboBoxRenderer.IsSupported%2A?displayProperty=nameWithType> Eigenschaft wird verwendet, um zu bestimmen, ob visuelle Stile im Client Bereich von Anwendungs Fenstern aktiviert sind. Wenn visuelle Stile aktiviert sind, wird der <xref:System.Windows.Forms.ComboBoxRenderer.DrawDropDownButton%2A?displayProperty=nameWithType> Dropdown Pfeil von der Methode mit visuellen Stilen dargestellt <xref:System.Windows.Forms.ControlPaint.DrawComboButton%2A?displayProperty=nameWithType> . andernfalls wird die Methode den Dropdown Pfeil im klassischen Windows-Stil Rendering.  
  
## <a name="example"></a>Beispiel  
 [!code-cpp[System.Windows.Forms_ControlRenderer#10](~/samples/snippets/cpp/VS_Snippets_Winforms/System.Windows.Forms_ControlRenderer/cpp/form1.cpp#10)]
 [!code-csharp[System.Windows.Forms_ControlRenderer#10](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms_ControlRenderer/CS/form1.cs#10)]
 [!code-vb[System.Windows.Forms_ControlRenderer#10](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms_ControlRenderer/VB/form1.vb#10)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Ein benutzerdefiniertes, von der-Klasse abgeleitetes <xref:System.Windows.Forms.Control>  
  
- Ein <xref:System.Windows.Forms.Form> , der das benutzerdefinierte Steuerelement hostet.  
  
- Verweise auf die <xref:System?displayProperty=nameWithType> <xref:System.Drawing?displayProperty=nameWithType> <xref:System.Windows.Forms?displayProperty=nameWithType> <xref:System.Windows.Forms.VisualStyles?displayProperty=nameWithType> Namespaces,, und.  
  
## <a name="see-also"></a>Siehe auch

- [Rendering von Steuerelementen mit visuellen Stilen](rendering-controls-with-visual-styles.md)
