---
title: 'Vorgehensweise: Verschieben eines ToolStrip aus einem ToolStripContainer auf ein Formular'
ms.date: 03/30/2017
helpviewer_keywords:
- ToolStrip control [Windows Forms], parenting to forms
- Windows Forms, parenting ToolStrip controls
ms.assetid: a1c94a7f-6fc5-4e4c-84cf-ff11dc573d33
ms.openlocfilehash: c6519add6789485d41146633abb5e11f80913649
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975620"
---
# <a name="how-to-move-a-toolstrip-out-of-a-toolstripcontainer-onto-a-form"></a>Vorgehensweise: Verschieben eines ToolStrip aus einem ToolStripContainer auf ein Formular
Verwenden Sie das folgende Verfahren, um einen <xref:System.Windows.Forms.ToolStrip> aus einem in <xref:System.Windows.Forms.ToolStripContainer> ein Formular zu verschieben.

## <a name="to-move-a-toolstrip-out-of-a-toolstripcontainer-onto-a-form"></a>So verschieben Sie ein ToolStrip aus einem ToolStripContainer auf ein Formular

1. Wählen Sie <xref:System.Windows.Forms.ToolStrip> aus.

2. Drücken Sie <xref:System.Windows.Forms.ToolStrip> STRG + X, oder klicken Sie mit der rechten Maustaste auf das, <xref:System.Windows.Forms.ToolStrip> und wählen Sie aus dem Kontextmenü die Option **Ausschneiden** aus.

3. Wählen Sie das Formular aus.

4. Fügen <xref:System.Windows.Forms.ToolStrip> Sie den durch Drücken von STRG + V ein, oder wählen Sie im Menü **Bearbeiten** die Option **Einfügen** aus.

5. Legen Sie die- <xref:System.Windows.Forms.ToolStrip.Dock%2A> Eigenschaft von <xref:System.Windows.Forms.ToolStrip> auf **oben** fest.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStrip>
- <xref:System.Windows.Forms.ToolStripContainer>
- [Übersicht über das ToolStrip-Steuerelement](toolstrip-control-overview-windows-forms.md)
