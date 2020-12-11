---
title: 'Vorgehensweise: Interaktive Verwendung der Spring-Eigenschaft in StatusStrip'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- StatusStrip control [Windows Forms]
- ToolStrip control [Windows Forms]
- status bars [Windows Forms], examples
- Spring property [Windows Forms]
ms.assetid: 18bde842-a93c-48dd-9db3-15738a1775ce
ms.openlocfilehash: 8750c48d08161260a1dba6ab69098980f25a5d55
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975581"
---
# <a name="how-to-use-the-spring-property-interactively-in-a-statusstrip"></a>Vorgehensweise: Interaktive Verwendung der Spring-Eigenschaft in StatusStrip
Sie können die Eigenschaft <xref:System.Windows.Forms.ToolStripStatusLabel.Spring%2A> verwenden, um ein <xref:System.Windows.Forms.ToolStripStatusLabel>-Steuerelement in einem <xref:System.Windows.Forms.StatusStrip>-Steuerelement zu positionieren. Die Eigenschaft <xref:System.Windows.Forms.ToolStripStatusLabel.Spring%2A> bestimmt, ob das <xref:System.Windows.Forms.ToolStripStatusLabel>-Steuerelement den verfügbaren Platz für das <xref:System.Windows.Forms.StatusStrip>-Steuerelement ausfüllt.  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird veranschaulicht, wie die Eigenschaft <xref:System.Windows.Forms.ToolStripStatusLabel.Spring%2A> zum Positionieren eines <xref:System.Windows.Forms.ToolStripStatusLabel>-Steuerelements in einem <xref:System.Windows.Forms.StatusStrip>-Steuerelement verwendet wird. Der <xref:System.Windows.Forms.ToolStripItem.Click>-Ereignishandler führt einen exklusiven oder Oder-Vorgang (XOR) aus, um den Wert der Eigenschaft <xref:System.Windows.Forms.ToolStripStatusLabel.Spring%2A> zu wechseln.  
  
 Um dieses Codebeispiel zu verwenden, kompilieren Sie die Anwendung, und führen Sie Sie aus, und klicken Sie dann auf **Mittel (Spring)** im-Steuerelement, <xref:System.Windows.Forms.StatusStrip> um den Wert der-Eigenschaft zu wechseln <xref:System.Windows.Forms.ToolStripStatusLabel.Spring%2A>  
  
 [!code-csharp[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#1)]
 [!code-vb[System.Windows.Forms.ToolStrip.Misc#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#1)]  
[!code-csharp[System.Windows.Forms.ToolStrip.Misc#50](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/CS/Program.cs#50)]
[!code-vb[System.Windows.Forms.ToolStrip.Misc#50](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.ToolStrip.Misc/VB/Program.vb#50)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 Für dieses Beispiel benötigen Sie Folgendes:  
  
- Verweise auf die Assemblys "System.Design", "System.Drawing" und "System.Windows.Forms".  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStripStatusLabel>
- <xref:System.Windows.Forms.StatusStrip>
- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripItem>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [ToolStrip-Steuerelement](toolstrip-control-windows-forms.md)
