---
title: Festlegen des Formats für das NumericUpDown-Steuerelement
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- NumericUpDown control [Windows Forms], formatting values
- up-down controls [Windows Forms], formatting numeric values
ms.assetid: fa7c5557-6bfb-45b2-975d-8887b23b0ba0
ms.openlocfilehash: 5ef1c801e96bef7b92e7e69dc36491144c456eeb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976661"
---
# <a name="how-to-set-the-format-for-the-windows-forms-numericupdown-control"></a>Vorgehensweise: Festlegen des Formats für das NumericUpDown-Steuerelement in Windows Forms
Sie können konfigurieren, wie Werte im Windows Forms Steuerelement angezeigt werden <xref:System.Windows.Forms.NumericUpDown> . Die- <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> Eigenschaft bestimmt, wie viele Zahlen nach dem Dezimaltrennzeichen angezeigt werden. der Standardwert ist 0. Die- <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> Eigenschaft bestimmt, ob zwischen allen drei Dezimalziffern ein Trennzeichen eingefügt wird. der Standardwert ist `false` . Das-Steuerelement kann Werte im Hexadezimal Format anstelle des Dezimal Formats anzeigen, wenn die- <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> Eigenschaft auf festgelegt ist `true` . der Standardwert ist `false` .  
  
### <a name="to-format-the-numeric-value"></a>So formatieren Sie den numerischen Wert  
  
- Zeigen Sie einen Dezimalwert an <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> , indem Sie die-Eigenschaft auf eine ganze Zahl festlegen und die- <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> Eigenschaft auf `true` oder festlegen `false` .  
  
    ```vb  
    NumericUpDown1.DecimalPlaces = 2  
    NumericUpDown1.ThousandsSeparator = True  
    ```  
  
    ```csharp  
    numericUpDown1.DecimalPlaces = 2;  
    numericUpDown1.ThousandsSeparator = true;  
    ```  
  
    ```cpp  
    numericUpDown1->DecimalPlaces = 2;  
    numericUpDown1->ThousandsSeparator = true;  
    ```  
  
     Oder  
  
- Zeigen Sie einen Hexadezimalwert <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> an, indem Sie die-Eigenschaft auf festlegen `true` .  
  
    ```vb  
    NumericUpDown1.Hexadecimal = True  
    ```  
  
    ```csharp  
    numericUpDown1.Hexadecimal = true;  
    ```  
  
    ```cpp  
    numericUpDown1->Hexadecimal = true;  
    ```  
  
    > [!NOTE]
    > Auch wenn der Wert im Formular als hexadezimal angezeigt wird, testen alle Tests, die Sie für die Eigenschaft ausführen, den <xref:System.Windows.Forms.NumericUpDown.Value%2A> Dezimalwert.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.NumericUpDown>
- [NumericUpDown-Steuerelement](numericupdown-control-windows-forms.md)
- [Übersicht über das NumericUpDown-Steuerelement](numericupdown-control-overview-windows-forms.md)
