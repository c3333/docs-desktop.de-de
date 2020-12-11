---
title: Formular Rahmen ändern
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms, changing the borders
ms.assetid: b3d5fa56-80c6-4b10-b505-f9672307ed55
ms.openlocfilehash: 8742f137b6dc53880b02d1cd667813aa728a6cfa
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972316"
---
# <a name="how-to-change-the-borders-of-windows-forms"></a>Vorgehensweise: Ändern der Rahmen von Windows Forms

Sie können aus mehreren Rahmenformatvorlagen auswählen, wenn Sie das Aussehen und Verhalten Ihres Windows Forms-Elements festlegen möchten. Durch Ändern der <xref:System.Windows.Forms.Form.FormBorderStyle%2A>-Eigenschaft können Sie das Verhalten des Formulars bei das Größenanpassung steuern. Zudem wirkt sich das Festlegen von <xref:System.Windows.Forms.Form.FormBorderStyle%2A> darauf aus, wie die Titelleiste angezeigt wird und mit welchen Schaltflächen. Weitere Informationen finden Sie unter <xref:System.Windows.Forms.FormBorderStyle>.  
  
 Visual Studio bietet umfassende Unterstützung für diese Aufgabe.  
  
 Siehe auch Gewusst [wie: Ändern der Rahmen Windows Forms mithilfe des Designers](/previous-versions/visualstudio/visual-studio-2010/yettzh3e(v=vs.100)).  
  
### <a name="to-set-the-border-style-of-windows-forms-programmatically"></a>So legen Sie die Rahmenart von Windows Forms programmgesteuert fest  
  
- Legen Sie die Eigenschaft <xref:System.Windows.Forms.Form.FormBorderStyle%2A> auf die gewünschte Rahmenart fest. Im folgenden Codebeispiel wird die Rahmenart des Formulars `DlgBx1` auf festgelegt <xref:System.Windows.Forms.FormBorderStyle.FixedDialog> .  
  
    ```vb  
    DlgBx1.FormBorderStyle = System.Windows.Forms.FormBorderStyle.FixedDialog  
    ```  
  
    ```csharp  
    DlgBx1.FormBorderStyle = System.Windows.Forms.FormBorderStyle.FixedDialog;  
    ```  
  
    ```cpp  
    DlgBx1->FormBorderStyle =  
       System::Windows::Forms::FormBorderStyle::FixedDialog;  
    ```  
  
     Siehe auch Gewusst [wie: Erstellen von Dialog Feldern zur Entwurfszeit](/previous-versions/visualstudio/visual-studio-2010/55cz5x2c(v=vs.100)).  
  
     Wenn Sie eine Rahmenart für das Formular ausgewählt haben, das optionale Schaltflächen zum **minimieren** und **maximieren** bereitstellt, können Sie außerdem angeben, ob eine oder beide dieser Schaltflächen funktionsfähig sein sollen. Diese Schaltflächen sind hilfreich, wenn Sie die Benutzeroberfläche genau steuern möchten. Die Schaltflächen **minimieren** und **maximieren** sind standardmäßig aktiviert, und ihre Funktionalität wird über das Fenster **Eigenschaften** geändert.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.FormBorderStyle>
- <xref:System.Windows.Forms.FormBorderStyle.FixedDialog>
- [Ersten Schritte mit Windows Forms](getting-started-with-windows-forms.md)
