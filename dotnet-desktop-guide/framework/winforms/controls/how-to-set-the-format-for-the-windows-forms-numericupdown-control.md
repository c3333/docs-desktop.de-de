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
# <a name="how-to-set-the-format-for-the-windows-forms-numericupdown-control"></a><span data-ttu-id="e6ad8-102">Vorgehensweise: Festlegen des Formats für das NumericUpDown-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="e6ad8-102">How to: Set the Format for the Windows Forms NumericUpDown Control</span></span>
<span data-ttu-id="e6ad8-103">Sie können konfigurieren, wie Werte im Windows Forms Steuerelement angezeigt werden <xref:System.Windows.Forms.NumericUpDown> .</span><span class="sxs-lookup"><span data-stu-id="e6ad8-103">You can configure how values are displayed in the Windows Forms <xref:System.Windows.Forms.NumericUpDown> control.</span></span> <span data-ttu-id="e6ad8-104">Die- <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> Eigenschaft bestimmt, wie viele Zahlen nach dem Dezimaltrennzeichen angezeigt werden. der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="e6ad8-104">The <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> property determines how many numbers appear after the decimal point; the default is 0.</span></span> <span data-ttu-id="e6ad8-105">Die- <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> Eigenschaft bestimmt, ob zwischen allen drei Dezimalziffern ein Trennzeichen eingefügt wird. der Standardwert ist `false` .</span><span class="sxs-lookup"><span data-stu-id="e6ad8-105">The <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> property determines whether a separator will be inserted between every three decimal digits; the default is `false`.</span></span> <span data-ttu-id="e6ad8-106">Das-Steuerelement kann Werte im Hexadezimal Format anstelle des Dezimal Formats anzeigen, wenn die- <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> Eigenschaft auf festgelegt ist `true` . der Standardwert ist `false` .</span><span class="sxs-lookup"><span data-stu-id="e6ad8-106">The control can display values in hexadecimal instead of decimal format, if the <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> property is set to `true`; the default is `false`.</span></span>  
  
### <a name="to-format-the-numeric-value"></a><span data-ttu-id="e6ad8-107">So formatieren Sie den numerischen Wert</span><span class="sxs-lookup"><span data-stu-id="e6ad8-107">To format the numeric value</span></span>  
  
- <span data-ttu-id="e6ad8-108">Zeigen Sie einen Dezimalwert an <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> , indem Sie die-Eigenschaft auf eine ganze Zahl festlegen und die- <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> Eigenschaft auf `true` oder festlegen `false` .</span><span class="sxs-lookup"><span data-stu-id="e6ad8-108">Display a decimal value by setting the <xref:System.Windows.Forms.NumericUpDown.DecimalPlaces%2A> property to an integer and setting the <xref:System.Windows.Forms.NumericUpDown.ThousandsSeparator%2A> property to `true` or `false`.</span></span>  
  
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
  
     <span data-ttu-id="e6ad8-109">Oder</span><span class="sxs-lookup"><span data-stu-id="e6ad8-109">-or-</span></span>  
  
- <span data-ttu-id="e6ad8-110">Zeigen Sie einen Hexadezimalwert <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> an, indem Sie die-Eigenschaft auf festlegen `true` .</span><span class="sxs-lookup"><span data-stu-id="e6ad8-110">Display a hexadecimal value by setting the <xref:System.Windows.Forms.NumericUpDown.Hexadecimal%2A> property to `true`.</span></span>  
  
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
    > <span data-ttu-id="e6ad8-111">Auch wenn der Wert im Formular als hexadezimal angezeigt wird, testen alle Tests, die Sie für die Eigenschaft ausführen, den <xref:System.Windows.Forms.NumericUpDown.Value%2A> Dezimalwert.</span><span class="sxs-lookup"><span data-stu-id="e6ad8-111">Even if the value is displayed on the form as hexadecimal, any tests you perform on the <xref:System.Windows.Forms.NumericUpDown.Value%2A> property will be testing its decimal value.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e6ad8-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6ad8-112">See also</span></span>

- <xref:System.Windows.Forms.NumericUpDown>
- [<span data-ttu-id="e6ad8-113">NumericUpDown-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e6ad8-113">NumericUpDown Control</span></span>](numericupdown-control-windows-forms.md)
- [<span data-ttu-id="e6ad8-114">Übersicht über das NumericUpDown-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="e6ad8-114">NumericUpDown Control Overview</span></span>](numericupdown-control-overview-windows-forms.md)
