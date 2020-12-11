---
title: 'Vorgehensweise: Hinzufügen eines Steuerelements zu einer Registerkarte'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- TabPage control
- tab controls [Windows Forms], tab order
- tab pages [Windows Forms], adding controls
ms.assetid: b092532e-7346-469f-b9a1-897f9bea4fb7
ms.openlocfilehash: 9806583fda60f1cb8a5ef2d97f42eba158593f61
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975751"
---
# <a name="how-to-add-a-control-to-a-tab-page"></a>Vorgehensweise: Hinzufügen eines Steuerelements zu einer Registerkarte
Sie können den Windows Forms verwenden <xref:System.Windows.Forms.TabControl> , um andere Steuerelemente auf organisierte Weise anzuzeigen. Im folgenden Verfahren wird gezeigt, wie Sie der ersten Registerkarte eine Schaltfläche hinzufügen. Weitere Informationen zum Hinzufügen eines Symbols zum Bezeichnungs Teil einer Registerkarte finden Sie unter Gewusst [wie: Ändern der Darstellung des Windows Forms TabControl](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md).  
  
### <a name="to-add-a-control-programmatically"></a>So fügen Sie ein-Steuerelement Programm gesteuert hinzu  
  
1. Verwenden Sie die-Methode der Auflistung, die <xref:System.Windows.Forms.Control.ControlCollection.Add%2A> von der-Eigenschaft von zurückgegeben wird <xref:System.Windows.Forms.Control.Controls%2A> <xref:System.Windows.Forms.TabPage> :  
  
     [!code-cpp[TabPageControlCollectionHowToAdd#1](~/samples/snippets/cpp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cpp/add.cpp#1)]
     [!code-csharp[TabPageControlCollectionHowToAdd#1](~/samples/snippets/csharp/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/cs/add.cs#1)]
     [!code-vb[TabPageControlCollectionHowToAdd#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/tabpagecontrolcollectionhowtoadd/vb/add.vb#1)]  
  
## <a name="see-also"></a>Siehe auch

- [TabControl-Steuerelement](tabcontrol-control-windows-forms.md)
- [Übersicht über das TabControl-Steuerelement](tabcontrol-control-overview-windows-forms.md)
- [Vorgehensweise: Ändern der Darstellung der TabControl-Komponente in Windows Forms](how-to-change-the-appearance-of-the-windows-forms-tabcontrol.md)
- [Vorgehensweise: Deaktivieren von Registerkartenseiten](how-to-disable-tab-pages.md)
- [Vorgehensweise: Hinzufügen und Entfernen von Registerkarten mit dem TabControl-Steuerelement in Windows Forms](how-to-add-and-remove-tabs-with-the-windows-forms-tabcontrol.md)
