---
title: 'Vorgehensweise: Einrichten des automatischem Zusammenführens von Menüs für MDI-Anwendungen (Multiple Document Interface)'
ms.date: 03/30/2017
helpviewer_keywords:
- MenuStrip [Windows Forms], merging
- Merging [Windows Forms], automatic menu
ms.assetid: 55e32cad-1141-4a56-aa33-d9543ca3d393
ms.openlocfilehash: 33e07bb655d81c6a802ebdce871a2fed845a5c96
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976644"
---
# <a name="how-to-set-up-automatic-menu-merging-for-mdi-applications"></a>Vorgehensweise: Einrichten des automatischem Zusammenführens von Menüs für MDI-Anwendungen (Multiple Document Interface)
Das folgende Verfahren enthält die grundlegenden Schritte zum Einrichten der automatischen Zusammenführung in einer MDI-Anwendung (Multiple Document Interface) mit <xref:System.Windows.Forms.MenuStrip> .  
  
### <a name="to-set-up-automatic-menu-merging"></a>So richten Sie die automatische Zusammenführung des Menüs ein  
  
1. Erstellen Sie das übergeordnete MDI-Formular <xref:System.Windows.Forms.Form.IsMdiContainer%2A> , indem Sie dessen-Eigenschaft auf festlegen `true` .  
  
2. Fügen Sie <xref:System.Windows.Forms.MenuStrip> das übergeordnete MDI-Element hinzu, und legen Sie dessen- <xref:System.Windows.Forms.Form.MainMenuStrip%2A> Eigenschaft auf fest <xref:System.Windows.Forms.MenuStrip> .  
  
3. Erstellen Sie ein untergeordnetes MDI-Formular, und legen Sie dessen- <xref:System.Windows.Forms.Form.MdiParent%2A> Eigenschaft auf den Namen des übergeordneten Formulars fest.  
  
4. Fügen Sie <xref:System.Windows.Forms.MenuStrip> dem untergeordneten MDI-Formular ein hinzu.  
  
5. Legen Sie im untergeordneten Formular die- <xref:System.Windows.Forms.ToolStripItem.Visible%2A> Eigenschaft von <xref:System.Windows.Forms.MenuStrip> auf fest `false` .  
  
6. Fügen Sie dem untergeordneten Formular Menü Elemente hinzu, die Sie im übergeordneten Formular zusammen <xref:System.Windows.Forms.MenuStrip> führen möchten, <xref:System.Windows.Forms.MenuStrip> Wenn das untergeordnete Formular aktiviert wird.  
  
7. Verwenden <xref:System.Windows.Forms.ToolStripItem.MergeAction%2A> Sie die-Eigenschaft in den Menü Elementen im unter <xref:System.Windows.Forms.MenuStrip> geordneten Formular, um zu steuern, wie Sie im übergeordneten Formular zusammengeführt werden.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.MenuStrip>
- <xref:System.Windows.Forms.ToolStripMenuItem>
- [Übersicht über das MenuStrip-Steuerelement](menustrip-control-overview-windows-forms.md)
