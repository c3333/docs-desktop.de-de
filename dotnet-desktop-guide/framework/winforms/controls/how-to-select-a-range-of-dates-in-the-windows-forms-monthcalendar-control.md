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
# <a name="how-to-select-a-range-of-dates-in-the-windows-forms-monthcalendar-control"></a><span data-ttu-id="b2cf8-102">Gewusst wie: Auswählen eines Datumsbereichs mithilfe des MonthCalendar-Steuerelements in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b2cf8-102">How to: Select a Range of Dates in the Windows Forms MonthCalendar Control</span></span>
<span data-ttu-id="b2cf8-103">Ein wichtiges Feature des Windows Forms- <xref:System.Windows.Forms.MonthCalendar> Steuer Elements besteht darin, dass der Benutzer einen Datumsbereich auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-103">An important feature of the Windows Forms <xref:System.Windows.Forms.MonthCalendar> control is that the user can select a range of dates.</span></span> <span data-ttu-id="b2cf8-104">Diese Funktion ist eine Verbesserung gegenüber der Datumsauswahl Funktion des Steuer Elements <xref:System.Windows.Forms.DateTimePicker> , sodass der Benutzer nur einen Datums-/Uhrzeitwert auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-104">This feature is an improvement over the date-selection feature of the <xref:System.Windows.Forms.DateTimePicker> control, which only enables the user to select a single date/time value.</span></span> <span data-ttu-id="b2cf8-105">Mithilfe der Eigenschaften des-Steuer Elements können Sie einen Datumsbereich festlegen oder einen vom Benutzer festgelegten Auswahlbereich erhalten <xref:System.Windows.Forms.MonthCalendar> .</span><span class="sxs-lookup"><span data-stu-id="b2cf8-105">You can set a range of dates or get a selection range set by the user by using properties of the <xref:System.Windows.Forms.MonthCalendar> control.</span></span> <span data-ttu-id="b2cf8-106">Im folgenden Codebeispiel wird veranschaulicht, wie ein Auswahlbereich festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-106">The following code example demonstrates how to set a selection range.</span></span>  
  
### <a name="to-select-a-range-of-dates"></a><span data-ttu-id="b2cf8-107">So wählen Sie einen Datumsbereich aus</span><span class="sxs-lookup"><span data-stu-id="b2cf8-107">To select a range of dates</span></span>  
  
1. <span data-ttu-id="b2cf8-108">Erstellen Sie <xref:System.DateTime> -Objekte, die das erste und letzte Datum in einem Bereich darstellen.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-108">Create <xref:System.DateTime> objects that represent the first and last dates in a range.</span></span>  
  
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
  
2. <span data-ttu-id="b2cf8-109">Legen Sie die <xref:System.Windows.Forms.MonthCalendar.SelectionRange%2A>-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-109">Set the <xref:System.Windows.Forms.MonthCalendar.SelectionRange%2A> property.</span></span>  
  
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
  
     <span data-ttu-id="b2cf8-110">– oder –</span><span class="sxs-lookup"><span data-stu-id="b2cf8-110">–or–</span></span>  
  
     <span data-ttu-id="b2cf8-111">Legen Sie die Eigenschaften <xref:System.Windows.Forms.MonthCalendar.SelectionStart%2A> und <xref:System.Windows.Forms.MonthCalendar.SelectionEnd%2A> fest.</span><span class="sxs-lookup"><span data-stu-id="b2cf8-111">Set the <xref:System.Windows.Forms.MonthCalendar.SelectionStart%2A> and <xref:System.Windows.Forms.MonthCalendar.SelectionEnd%2A> properties.</span></span>  
  
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
  
## <a name="see-also"></a><span data-ttu-id="b2cf8-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2cf8-112">See also</span></span>

- [<span data-ttu-id="b2cf8-113">MonthCalendar-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="b2cf8-113">MonthCalendar Control</span></span>](monthcalendar-control-windows-forms.md)
- [<span data-ttu-id="b2cf8-114">Gewusst wie: Ändern der Darstellung des MonthCalendar-Steuerelements in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b2cf8-114">How to: Change the Windows Forms MonthCalendar Control's Appearance</span></span>](how-to-change-monthcalendar-control-appearance.md)
- [<span data-ttu-id="b2cf8-115">Gewusst wie: Anzeigen einzelner Tage in Fettschrift mit dem MonthCalendar-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b2cf8-115">How to: Display Specific Days in Bold with the Windows Forms MonthCalendar Control</span></span>](display-specific-days-in-bold-with-wf-monthcalendar-control.md)
- [<span data-ttu-id="b2cf8-116">Gewusst wie: Anzeigen mehrerer Monate mit dem MonthCalendar-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="b2cf8-116">How to: Display More than One Month in the Windows Forms MonthCalendar Control</span></span>](display-more-than-one-month-wf-monthcalendar-control.md)
