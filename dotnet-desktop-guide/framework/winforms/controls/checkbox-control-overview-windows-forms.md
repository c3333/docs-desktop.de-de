---
title: Übersicht über das CheckBox-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- CheckBox
helpviewer_keywords:
- CheckBox control [Windows Forms], about CheckBox control
- data binding [Windows Forms], checkbox controls
- check boxes [Windows Forms], about check boxes
ms.assetid: 085a4e0b-9046-473f-b141-d0edddfb2ebb
ms.openlocfilehash: b42816cf1bc0ce1ab6db0a2a436b17b0d4370d59
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975104"
---
# <a name="checkbox-control-overview-windows-forms"></a>Übersicht über das CheckBox-Steuerelement (Windows Forms)
Das Windows Forms-Steuerelement <xref:System.Windows.Forms.CheckBox> zeigt an, ob eine bestimmte Bedingung aktiviert oder deaktiviert ist. Es wird häufig verwendet, um dem Benutzer eine Ja/Nein- oder Wahr/Falsch-Auswahl zu präsentieren. Sie können Kontrollkästchen-Steuerelemente in Gruppen verwenden, um mehrere Optionen anzuzeigen, unter denen der Benutzer eine oder mehrere auswählen kann.  
  
 Das Kontrollkästchen-Steuerelement ähnelt dem Optionsfeld-Steuerelement in, das jeweils zum Angeben einer vom Benutzer vorgenommenen Auswahl verwendet wird. Sie unterscheiden sich darin, dass jeweils nur ein Optionsfeld in einer Gruppe ausgewählt werden kann. Mit dem Kontrollkästchen-Steuerelement kann jedoch eine beliebige Anzahl von Kontrollkästchen ausgewählt werden.  
  
 Ein Kontrollkästchen kann mithilfe einer einfachen Datenbindung mit Elementen in einer Datenbank verbunden werden. Mehrere Kontrollkästchen können mithilfe des-Steuer Elements gruppiert werden <xref:System.Windows.Forms.GroupBox> . Dies ist nützlich für die visuelle Darstellung und das Design der Benutzeroberfläche, da gruppierte Steuerelemente im Formular-Designer zusammen verschoben werden können. Weitere Informationen finden Sie unter [Windows Forms Datenbindung](../windows-forms-data-binding.md) und [GroupBox-Steuer](groupbox-control-windows-forms.md)Element.  
  
 Das <xref:System.Windows.Forms.CheckBox> -Steuerelement verfügt über zwei wichtige Eigenschaften: <xref:System.Windows.Forms.CheckBox.Checked%2A> und <xref:System.Windows.Forms.CheckBox.CheckState%2A> . Die- <xref:System.Windows.Forms.CheckBox.Checked%2A> Eigenschaft gibt entweder `true` oder zurück `false` . Die- <xref:System.Windows.Forms.CheckBox.CheckState%2A> Eigenschaft gibt entweder <xref:System.Windows.Forms.CheckState.Checked> oder zurück <xref:System.Windows.Forms.CheckState.Unchecked> . wenn die- <xref:System.Windows.Forms.CheckBox.ThreeState%2A> Eigenschaft auf festgelegt ist, gibt `true` <xref:System.Windows.Forms.CheckBox.CheckState%2A> möglicherweise ebenfalls zurück <xref:System.Windows.Forms.CheckState.Indeterminate> . Im unbestimmten Zustand wird das Feld mit einer Abbild Darstellung angezeigt, um anzugeben, dass die Option nicht verfügbar ist.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.CheckBox>
- [Gewusst wie: Festlegen von Optionen mit CheckBox-Steuerelementen in Windows Forms](how-to-set-options-with-windows-forms-checkbox-controls.md)
- [Gewusst wie: Reagieren auf das Klicken auf Kontrollkästchen in Windows Forms](how-to-respond-to-windows-forms-checkbox-clicks.md)
- [CheckBox-Steuerelement](checkbox-control-windows-forms.md)
