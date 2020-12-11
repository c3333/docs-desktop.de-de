---
title: 'Vorgehensweise: Ausblenden des Steuerelements zur Laufzeit'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms], making invisible at run time
- invisible controls
- user controls [Windows Forms], invisible
- custom controls [Windows Forms], invisible
- run time [Windows Forms], making controls invisible
ms.assetid: 69eb2e72-32f5-4f79-a157-c2c5f60c1628
ms.openlocfilehash: e9af529541a40a951d6defea180dbbef04c8f3be
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974808"
---
# <a name="how-to-make-your-control-invisible-at-run-time"></a>Vorgehensweise: Ausblenden des Steuerelements zur Laufzeit
Es kann vorkommen, dass Sie ein Benutzer Steuerelement erstellen möchten, das zur Laufzeit unsichtbar ist. Beispielsweise ist ein Steuerelement, das eine Wecker-Uhr ist, möglicherweise unsichtbar, außer wenn der Alarm ertönt. Dies lässt sich problemlos erreichen, indem die-Eigenschaft festgelegt wird <xref:System.Windows.Forms.Control.Visible%2A> . Wenn die- <xref:System.Windows.Forms.Control.Visible%2A> Eigenschaft ist `true` , wird das Steuerelement normal angezeigt. Wenn `false` , wird das Steuerelement ausgeblendet. Obwohl Code in Ihrem Steuerelement möglicherweise weiterhin ausgeführt wird und unsichtbar ist, können Sie nicht über die Benutzeroberfläche mit dem Steuerelement interagieren. Wenn Sie ein unsichtbares Steuerelement erstellen möchten, das weiterhin auf Benutzereingaben antwortet (z. b. Mausklicks), sollten Sie ein transparentes Steuerelement erstellen. Weitere Informationen finden Sie unter [Erteilen eines transparenten Hintergrunds für ein Steuer](how-to-give-your-control-a-transparent-background.md)Element.  
  
### <a name="to-make-your-control-invisible-at-run-time"></a>So machen Sie das Steuerelement zur Laufzeit unsichtbar  
  
1. Legen Sie die <xref:System.Windows.Forms.Control.Visible%2A> -Eigenschaft auf `false`fest.  
  
    ```vb  
    ' To set the Visible property from within your object's own code.  
    Me.Visible = False  
    ' To set the Visible property from another object.  
    myControl1.Visible = False  
    ```  
  
    ```csharp  
    // To set the Visible property from within your object's own code.  
    this.Visible = false;  
    // To set the Visible property from another object.  
    myControl1.Visible = false;  
    ```  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Control.Visible%2A>
- [Entwickeln benutzerdefinierter Windows Forms-Steuerelemente mit .NET Framework](developing-custom-windows-forms-controls.md)
- [Vorgehensweise: Verwenden eines transparenten Hintergrunds für ein Steuerelement](how-to-give-your-control-a-transparent-background.md)
