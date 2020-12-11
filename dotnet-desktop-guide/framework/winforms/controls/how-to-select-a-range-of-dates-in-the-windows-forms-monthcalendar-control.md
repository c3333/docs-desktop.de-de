---
title: Wählen Sie einen Datumsbereich im MonthCalendar-Steuerelement aus.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- dates [Windows Forms], selecting range in calendar controls
- examples [Windows Forms], calendar controls
- calendars [Windows Forms], selecting date range
- MonthCalendar control [Windows Forms], selecting date range
ms.assetid: 95d9ab95-b0f8-4c19-9f63-b5cd4593a5d0
ms.openlocfilehash: bda96af21a8f86a54d5c0fe0204546b980076d26
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975597"
---
# <a name="how-to-select-a-range-of-dates-in-the-windows-forms-monthcalendar-control"></a>Gewusst wie: Auswählen eines Datumsbereichs mithilfe des MonthCalendar-Steuerelements in Windows Forms
Ein wichtiges Feature des Windows Forms- <xref:System.Windows.Forms.MonthCalendar> Steuer Elements besteht darin, dass der Benutzer einen Datumsbereich auswählen kann. Diese Funktion ist eine Verbesserung gegenüber der Datumsauswahl Funktion des Steuer Elements <xref:System.Windows.Forms.DateTimePicker> , sodass der Benutzer nur einen Datums-/Uhrzeitwert auswählen kann. Mithilfe der Eigenschaften des-Steuer Elements können Sie einen Datumsbereich festlegen oder einen vom Benutzer festgelegten Auswahlbereich erhalten <xref:System.Windows.Forms.MonthCalendar> . Im folgenden Codebeispiel wird veranschaulicht, wie ein Auswahlbereich festgelegt wird.  
  
### <a name="to-select-a-range-of-dates"></a>So wählen Sie einen Datumsbereich aus  
  
1. Erstellen Sie <xref:System.DateTime> -Objekte, die das erste und letzte Datum in einem Bereich darstellen.  
  
    ```vb  
    Dim projectStart As Date = New DateTime(2001, 2, 13)  
    Dim projectEnd As Date = New DateTime(2001, 2, 28)  
    ```  
  
    ```csharp  
    DateTime projectStart = new DateTime(2001, 2, 13);  
    DateTime projectEnd = new DateTime(2001, 2, 28);  
    ```  
  
    ```cpp  
    DateTime projectStart = DateTime(2001, 2, 13);  
    DateTime projectEnd = DateTime(2001, 2, 28);  
    ```  
  
2. Legen Sie die <xref:System.Windows.Forms.MonthCalendar.SelectionRange%2A>-Eigenschaft fest.  
  
    ```vb  
    MonthCalendar1.SelectionRange = New SelectionRange(projectStart, projectEnd)  
    ```  
  
    ```csharp  
    monthCalendar1.SelectionRange = new SelectionRange(projectStart, projectEnd);  
    ```  
  
    ```cpp  
    monthCalendar1->SelectionRange = gcnew  
       SelectionRange(projectStart, projectEnd);  
    ```  
  
     – oder –  
  
     Legen Sie die Eigenschaften <xref:System.Windows.Forms.MonthCalendar.SelectionStart%2A> und <xref:System.Windows.Forms.MonthCalendar.SelectionEnd%2A> fest.  
  
    ```vb  
    MonthCalendar1.SelectionStart = projectStart  
    MonthCalendar1.SelectionEnd = projectEnd  
    ```  
  
    ```csharp  
    monthCalendar1.SelectionStart = projectStart;  
    monthCalendar1.SelectionEnd = projectEnd;  
    ```  
  
    ```cpp  
    monthCalendar1->SelectionStart = projectStart;  
    monthCalendar1->SelectionEnd = projectEnd;  
    ```  
  
## <a name="see-also"></a>Siehe auch

- [MonthCalendar-Steuerelement](monthcalendar-control-windows-forms.md)
- [Gewusst wie: Ändern der Darstellung des MonthCalendar-Steuerelements in Windows Forms](how-to-change-monthcalendar-control-appearance.md)
- [Gewusst wie: Anzeigen einzelner Tage in Fettschrift mit dem MonthCalendar-Steuerelement in Windows Forms](display-specific-days-in-bold-with-wf-monthcalendar-control.md)
- [Gewusst wie: Anzeigen mehrerer Monate mit dem MonthCalendar-Steuerelement in Windows Forms](display-more-than-one-month-wf-monthcalendar-control.md)
