---
title: Übersicht über das Button-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- Button
helpviewer_keywords:
- Button control [Windows Forms], about Button control
- buttons [Windows Forms], about buttons
ms.assetid: 255b291b-51a9-4a92-a1a4-2400cd82443f
ms.openlocfilehash: 4ba7b333e5414efb4814d64ce50c55e08b27f859
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976019"
---
# <a name="button-control-overview-windows-forms"></a>Übersicht über das Button-Steuerelement (Windows Forms)
Das Windows Forms <xref:System.Windows.Forms.Button>-Steuerelement ermöglicht es dem Benutzer, durch Klicken eine Aktion auszuführen. Wenn der Benutzer auf die Schaltfläche klickt, wird sie als gedrückt bzw. nicht gedrückt angezeigt. Wenn der Benutzer auf eine Schaltfläche klickt, <xref:System.Windows.Forms.Control.Click> wird der Ereignishandler aufgerufen. Sie platzieren Code im- <xref:System.Windows.Forms.Control.Click> Ereignishandler, um die von Ihnen gewählte Aktion auszuführen.  
  
 Der auf der Schaltfläche angezeigte Text ist in der- <xref:System.Windows.Forms.Control.Text%2A> Eigenschaft enthalten. Wenn der Text die Breite der Schaltfläche überschreitet, wird er mit der nächsten Zeile Umbruch. Es wird jedoch abgeschnitten, wenn das Steuerelement seine Gesamthöhe nicht erfüllen kann. Weitere Informationen finden Sie unter Gewusst [wie: Festlegen des Texts, der von einem Windows Forms-Steuerelement angezeigt wird](how-to-set-the-text-displayed-by-a-windows-forms-control.md). Die- <xref:System.Windows.Forms.Control.Text%2A> Eigenschaft kann eine Zugriffstaste enthalten, die einem Benutzer ermöglicht, durch Drücken der Alt-Taste mit der Zugriffstaste auf das Steuerelement zu klicken. Weitere Informationen finden Sie unter Gewusst [wie: Erstellen von Zugriffs Schlüsseln für Windows Forms](how-to-create-access-keys-for-windows-forms-controls.md)-Steuerelemente. Die Darstellung des Texts wird von der <xref:System.Windows.Forms.Control.Font%2A> -Eigenschaft und der- <xref:System.Windows.Forms.ButtonBase.TextAlign%2A> Eigenschaft gesteuert.  
  
 Das <xref:System.Windows.Forms.Button> Steuerelement kann auch Bilder mithilfe der <xref:System.Windows.Forms.ButtonBase.Image%2A> -Eigenschaft und der-Eigenschaft anzeigen <xref:System.Windows.Forms.ButtonBase.ImageList%2A> . Weitere Informationen finden Sie unter Gewusst [wie: Festlegen des Bilds, das von einem Windows Forms-Steuerelement angezeigt wird](how-to-set-the-image-displayed-by-a-windows-forms-control.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Button>
- [Gewusst wie: Reagieren auf das Anklicken von Schaltflächen in Windows Forms](how-to-respond-to-windows-forms-button-clicks.md)
- [Methoden zur Auswahl eines Button-Steuerelements in Windows Forms](ways-to-select-a-windows-forms-button-control.md)
- [Vorgehensweise: Definieren einer Windows Forms-Schaltfläche als „Annehmen“-Schaltfläche mithilfe des Designers](designate-a-wf-button-as-the-accept-button-using-the-designer.md)
- [Vorgehensweise: Definieren einer Windows Forms-Schaltfläche als „Abbrechen“-Schaltfläche mithilfe des Designers](designate-a-wf-button-as-the-cancel-button-using-the-designer.md)
- [Button-Steuerelement](button-control-windows-forms.md)
