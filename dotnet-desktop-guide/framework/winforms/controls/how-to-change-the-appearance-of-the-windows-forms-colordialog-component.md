---
title: Darstellung der Color Dialog-Komponente ändern
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- ColorDialog component [Windows Forms], examples
- ColorDialog component [Windows Forms], formatting appearance
- color dialog box [Windows Forms], configuring appearance
ms.assetid: bba4e262-1cd7-4f63-89cf-330a36f7b539
ms.openlocfilehash: 0402d7f3c03a0771512a03ac54e1b093c9fe6e9b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976353"
---
# <a name="how-to-change-the-appearance-of-the-windows-forms-colordialog-component"></a>Vorgehensweise: Ändern der Darstellung der ColorDialog-Komponente in Windows Forms
Sie können die Darstellung der Windows Forms <xref:System.Windows.Forms.ColorDialog> Komponente mit einer Reihe von Eigenschaften konfigurieren. Das Dialogfeld enthält zwei Abschnitte – eine, in der die Grundfarben angezeigt werden, und eine, mit der Benutzer benutzerdefinierte Farben definieren können.  
  
 Die meisten Eigenschaften schränken die Farben ein, die der Benutzer im Dialogfeld auswählen kann. Wenn die- <xref:System.Windows.Forms.ColorDialog.AllowFullOpen%2A> Eigenschaft auf festgelegt ist `true` , darf der Benutzer benutzerdefinierte Farben definieren. Die- <xref:System.Windows.Forms.ColorDialog.FullOpen%2A> Eigenschaft ist `true` , wenn das Dialogfeld erweitert wird, um benutzerdefinierte Farben zu definieren. andernfalls muss der Benutzer auf die Schaltfläche "benutzerdefinierte Farben definieren" klicken. Wenn die- <xref:System.Windows.Forms.ColorDialog.AnyColor%2A> Eigenschaft auf festgelegt ist `true` , werden im Dialogfeld alle verfügbaren Farben im Satz der Grundfarben angezeigt. Wenn die- <xref:System.Windows.Forms.ColorDialog.SolidColorOnly%2A> Eigenschaft auf festgelegt ist `true` , kann der Benutzer keine Dithering-Farben auswählen; nur voll Tonfarben können ausgewählt werden.  
  
 Wenn die- <xref:System.Windows.Forms.ColorDialog.ShowHelp%2A> Eigenschaft auf festgelegt ist `true` , wird im Dialogfeld eine Schaltfläche "Hilfe" angezeigt. Wenn der Benutzer auf die Schaltfläche "Hilfe" klickt, <xref:System.Windows.Forms.ColorDialog> wird das-Ereignis der Komponente <xref:System.Windows.Forms.CommonDialog.HelpRequest> ausgelöst.  
  
### <a name="to-configure-the-appearance-of-the-color-dialog-box"></a>So konfigurieren Sie die Darstellung des Dialog Felds "Farbe"  
  
1. Legen <xref:System.Windows.Forms.ColorDialog.AllowFullOpen%2A> Sie die <xref:System.Windows.Forms.ColorDialog.AnyColor%2A> Eigenschaften,, <xref:System.Windows.Forms.ColorDialog.SolidColorOnly%2A> und <xref:System.Windows.Forms.ColorDialog.ShowHelp%2A> auf die gewünschten Werte fest.  
  
    ```vb  
    ColorDialog1.AllowFullOpen = True  
    ColorDialog1.AnyColor = True  
    ColorDialog1.SolidColorOnly = False  
    ColorDialog1.ShowHelp = True  
    ```  
  
    ```csharp  
    colorDialog1.AllowFullOpen = true;  
    colorDialog1.AnyColor = true;  
    colorDialog1.SolidColorOnly = false;  
    colorDialog1.ShowHelp = true;  
    ```  
  
    ```cpp  
    colorDialog1->AllowFullOpen = true;  
    colorDialog1->AnyColor = true;  
    colorDialog1->SolidColorOnly = false;  
    colorDialog1->ShowHelp = true;  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ColorDialog>
- [ColorDialog-Komponente](colordialog-component-windows-forms.md)
- [Übersicht über die ColorDialog-Komponente](colordialog-component-overview-windows-forms.md)
