---
title: Übersicht über Ereignishandler
ms.date: 03/30/2017
ms.topic: overview
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms, event handling
- event handling [Windows Forms], Windows Forms
- event handlers [Windows Forms], about event handlers
ms.assetid: 228112e1-1711-42ee-8ffa-ff3555bffe66
ms.openlocfilehash: ec8bc23ce8aba36ad456114ec645d4f0799f107f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976192"
---
# <a name="event-handlers-overview-windows-forms"></a>Übersicht über Ereignishandler (Windows Forms)
Ein Ereignishandler ist eine Methode, die an ein Ereignis gebunden ist. Wenn das-Ereignis ausgelöst wird, wird der Code im-Ereignishandler ausgeführt. Jeder Ereignishandler stellt zwei Parameter bereit, mit denen Sie das Ereignis ordnungsgemäß behandeln können. Das folgende Beispiel zeigt einen Ereignishandler für <xref:System.Windows.Forms.Button> das-Ereignis eines-Steuer Elements <xref:System.Windows.Forms.Control.Click> .  
  
```vb  
Private Sub button1_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles button1.Click  
  
End Sub  
```  
  
```csharp  
private void button1_Click(object sender, System.EventArgs e)
{  
  
}  
```  
  
```cpp  
private:  
  void button1_Click(System::Object ^ sender,  
    System::EventArgs ^ e)  
  {  
  
  }  
```  
  
 Der erste Parameter, `sender` , stellt einen Verweis auf das-Objekt bereit, das das Ereignis ausgelöst hat. Der zweite Parameter, `e` , im obigen Beispiel, übergibt ein Objekt, das für das behandelte Ereignis spezifisch ist. Wenn Sie auf die Eigenschaften des Objekts (und manchmal auf seine Methoden) verweisen, können Sie Informationen wie die Position der Maus für Mausereignisse oder Daten abrufen, die in Drag & Drop-Ereignissen übertragen werden.  
  
 In der Regel erzeugt jedes Ereignis einen Ereignishandler mit einem anderen Ereignis Objekttyp für den zweiten Parameter. Einige Ereignishandler, z. b. die für das <xref:System.Windows.Forms.Control.MouseDown> -Ereignis und das-Ereignis <xref:System.Windows.Forms.Control.MouseUp> , haben den gleichen Objekttyp für den zweiten Parameter. Für diese Ereignis Typen können Sie denselben Ereignishandler zum Verarbeiten beider Ereignisse verwenden.  
  
 Sie können auch denselben Ereignishandler verwenden, um das gleiche Ereignis für verschiedene Steuerelemente zu verarbeiten. Wenn Sie z. b. eine Gruppe von <xref:System.Windows.Forms.RadioButton> Steuerelementen in einem Formular haben, können Sie einen einzelnen Ereignishandler für das-Ereignis erstellen und festlegen, dass das <xref:System.Windows.Forms.Control.Click> -Ereignis jedes Steuer Elements <xref:System.Windows.Forms.Control.Click> an den einzelnen Ereignishandler gebunden ist. Weitere Informationen finden Sie unter Gewusst [wie: Verbinden mehrerer Ereignisse mit einem einzelnen Ereignis Handler in Windows Forms](how-to-connect-multiple-events-to-a-single-event-handler-in-windows-forms.md).  
  
## <a name="see-also"></a>Siehe auch

- [Erstellen von Ereignishandlern in Windows Forms](creating-event-handlers-in-windows-forms.md)
- [Übersicht über Ereignisse](events-overview-windows-forms.md)
