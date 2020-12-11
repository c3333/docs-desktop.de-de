---
title: 'Vorgehensweise: Strecken einer ToolStripTextBox zum Ausfüllen der verbleibenden Breite eines ToolStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text boxes [Windows Forms], stretching in ToolStrip control [Windows Forms]
- ToolStrip control [Windows Forms], stretching a text box
ms.assetid: 0e610fbf-85fe-414c-900c-9704a5dd5cc6
ms.openlocfilehash: c60cc2a377f08a73159f25b2ab5f2812d41f0c10
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976455"
---
# <a name="how-to-stretch-a-toolstriptextbox-to-fill-the-remaining-width-of-a-toolstrip-windows-forms"></a>Gewusst wie: Strecken einer ToolStripTextBox zum Ausfüllen der verbleibenden Breite eines ToolStrip (Windows Forms)
Wenn Sie die- <xref:System.Windows.Forms.ToolStrip.Stretch%2A> Eigenschaft eines- <xref:System.Windows.Forms.ToolStrip> Steuer Elements auf festlegen `true` , füllt das-Steuerelement seinen Container von End-to-End und ändert seine Größe, wenn die Größe des Containers geändert wird. In dieser Konfiguration ist es möglicherweise sinnvoll, ein Element im-Steuerelement, z. b. <xref:System.Windows.Forms.ToolStripTextBox> , zu Strecken, um den verfügbaren Platz auszufüllen und die Größe zu ändern, wenn die Größe des Steuer Elements geändert wird. Diese Streckung ist beispielsweise nützlich, wenn Sie aussehen und Verhalten ähnlich der Adressleiste in Microsoft® Internet Explorer erreichen möchten.  
  
## <a name="example"></a>Beispiel  
 Das folgende Codebeispiel stellt eine von <xref:System.Windows.Forms.ToolStripTextBox> aufgeleitete Klasse bereit `ToolStripSpringTextBox` . Diese Klasse überschreibt die- <xref:System.Windows.Forms.ToolStripTextBox.GetPreferredSize%2A> Methode, um die verfügbare Breite des übergeordneten Steuer Elements zu berechnen, <xref:System.Windows.Forms.ToolStrip> nachdem die kombinierte Breite aller anderen Elemente subtrahiert wurde. Dieses Codebeispiel stellt außerdem eine <xref:System.Windows.Forms.Form> -Klasse und eine- `Program` Klasse bereit, um das neue Verhalten zu veranschaulichen.  
  
 [!code-csharp[ToolStripSpringTextBox#00](~/samples/snippets/csharp/VS_Snippets_Winforms/ToolStripSpringTextBox/cs/ToolStripSpringTextBox.cs#00)]
 [!code-vb[ToolStripSpringTextBox#00](~/samples/snippets/visualbasic/VS_Snippets_Winforms/ToolStripSpringTextBox/vb/ToolStripSpringTextBox.vb#00)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Verweise auf die Assemblys "System", "System.Drawing" und "System.Windows.Forms".  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStrip.Stretch%2A?displayProperty=nameWithType>
- <xref:System.Windows.Forms.ToolStripTextBox>
- <xref:System.Windows.Forms.ToolStripTextBox.GetPreferredSize%2A?displayProperty=nameWithType>
- [Architektur des ToolStrip-Steuerelements](toolstrip-control-architecture.md)
- [Vorgehensweise: Interaktive Verwendung der Spring-Eigenschaft in StatusStrip](how-to-use-the-spring-property-interactively-in-a-statusstrip.md)
