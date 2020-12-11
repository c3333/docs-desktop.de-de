---
title: Festlegen einer Schaltfläche als Schaltfläche "Abbrechen"
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- buttons [Windows Forms], cancel buttons
- Button control [Windows Forms], designating as cancel button
ms.assetid: 252f0834-e54b-44d9-96f7-ee5f50e94f2c
ms.openlocfilehash: 123b3e275065efadd24815320ea7d855808e60b9
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976313"
---
# <a name="how-to-designate-a-windows-forms-button-as-the-cancel-button"></a><span data-ttu-id="fe7e2-102">Vorgehensweise: Definieren einer Windows Forms-Schaltfläche als „Abbrechen“-Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="fe7e2-102">How to: Designate a Windows Forms Button as the Cancel Button</span></span>
<span data-ttu-id="fe7e2-103">In jedem Windows Form können Sie ein Steuerelement als <xref:System.Windows.Forms.Button> Schaltfläche "Abbrechen" festlegen.</span><span class="sxs-lookup"><span data-stu-id="fe7e2-103">On any Windows Form, you can designate a <xref:System.Windows.Forms.Button> control to be the cancel button.</span></span> <span data-ttu-id="fe7e2-104">Wenn der Benutzer die ESC-Taste drückt, wird auf eine Schaltfläche Abbrechen geklickt, unabhängig davon, welches andere Steuerelement im Formular den Fokus besitzt.</span><span class="sxs-lookup"><span data-stu-id="fe7e2-104">A cancel button is clicked whenever the user presses the ESC key, regardless of which other control on the form has the focus.</span></span> <span data-ttu-id="fe7e2-105">Eine solche Schaltfläche wird in der Regel so programmiert, dass der Benutzer schnell einen Vorgang beenden kann, ohne dass eine Aktion ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="fe7e2-105">Such a button is usually programmed to enable the user to quickly exit an operation without committing to any action.</span></span>  
  
### <a name="to-designate-the-cancel-button"></a><span data-ttu-id="fe7e2-106">So bestimmen Sie die Schaltfläche Abbrechen</span><span class="sxs-lookup"><span data-stu-id="fe7e2-106">To designate the cancel button</span></span>  
  
1. <span data-ttu-id="fe7e2-107">Legen Sie die- <xref:System.Windows.Forms.Form.CancelButton%2A> Eigenschaft des Formulars auf das entsprechende Steuerelement fest <xref:System.Windows.Forms.Button> .</span><span class="sxs-lookup"><span data-stu-id="fe7e2-107">Set the form's <xref:System.Windows.Forms.Form.CancelButton%2A> property to the appropriate <xref:System.Windows.Forms.Button> control.</span></span>  
  
    ```vb  
    Private Sub SetCancelButton(ByVal myCancelBtn As Button)  
       Me.CancelButton = myCancelBtn  
    End Sub  
    ```  
  
    ```csharp  
    private void SetCancelButton(Button myCancelBtn)  
    {  
       this.CancelButton = myCancelBtn;  
    }  
    ```  
  
    ```cpp  
    private:  
       void SetCancelButton(Button ^ myCancelBtn)  
       {  
          this->CancelButton = myCancelBtn;  
       }  
    ```  
  
## <a name="see-also"></a><span data-ttu-id="fe7e2-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe7e2-108">See also</span></span>

- <xref:System.Windows.Forms.Form.CancelButton%2A>
- [<span data-ttu-id="fe7e2-109">Übersicht über das Button-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="fe7e2-109">Button Control Overview</span></span>](button-control-overview-windows-forms.md)
- [<span data-ttu-id="fe7e2-110">Methoden zur Auswahl eines Button-Steuerelements in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fe7e2-110">Ways to Select a Windows Forms Button Control</span></span>](ways-to-select-a-windows-forms-button-control.md)
- [<span data-ttu-id="fe7e2-111">Gewusst wie: Reagieren auf das Anklicken von Schaltflächen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="fe7e2-111">How to: Respond to Windows Forms Button Clicks</span></span>](how-to-respond-to-windows-forms-button-clicks.md)
- [<span data-ttu-id="fe7e2-112">Vorgehensweise: Definieren einer Windows Forms-Schaltfläche als „Annehmen“-Schaltfläche</span><span class="sxs-lookup"><span data-stu-id="fe7e2-112">How to: Designate a Windows Forms Button as the Accept Button</span></span>](how-to-designate-a-windows-forms-button-as-the-accept-button.md)
- [<span data-ttu-id="fe7e2-113">Button-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="fe7e2-113">Button Control</span></span>](button-control-windows-forms.md)
