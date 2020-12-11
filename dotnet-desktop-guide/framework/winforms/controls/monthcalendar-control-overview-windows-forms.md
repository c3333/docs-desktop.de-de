---
title: Übersicht über das MonthCalendar-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- MonthCalendar
helpviewer_keywords:
- calendars [Windows Forms], Windows Forms controls
- calendar controls [Windows Forms], Windows Forms
- MonthCalendar control [Windows Forms], setting the first day of the week
ms.assetid: 788c5325-b721-44ec-95bf-9b680ba0f6a2
ms.openlocfilehash: a9b56164339d03b380a564b21855f6d94ec06af5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976703"
---
# <a name="monthcalendar-control-overview-windows-forms"></a>Übersicht über das MonthCalendar-Steuerelement (Windows Forms)
Das Windows Forms <xref:System.Windows.Forms.MonthCalendar> -Steuerelement stellt eine intuitive grafische Oberfläche für Benutzer dar, um Datumsinformationen anzuzeigen und festzulegen. Das-Steuerelement zeigt einen Kalender an: ein Raster mit den nummerierten Tagen des Monats, angeordnet in Spalten unterhalb der Wochentage, wobei der ausgewählte Bereich von Datumsangaben hervorgehoben ist. Sie können einen anderen Monat auswählen, indem Sie auf beiden Seiten der Monats Beschriftung auf die Pfeil Schaltflächen klicken. Im Gegensatz zum ähnlichen <xref:System.Windows.Forms.DateTimePicker> Steuerelement können Sie mit diesem Steuerelement mehr als ein Datum auswählen. Weitere Informationen zum-Steuerelement finden Sie unter <xref:System.Windows.Forms.DateTimePicker> [DateTimePicker-Steuer](datetimepicker-control-windows-forms.md)Element.  
  
## <a name="configuring-the-monthcalendar-control"></a>Konfigurieren des MonthCalendar-Steuer Elements  
 Die Darstellung des <xref:System.Windows.Forms.MonthCalendar> Steuer Elements ist sehr konfigurierbar. Standardmäßig wird das heutige Datum als Kreis angezeigt und auch am unteren Ende des Rasters angegeben. Sie können diese Funktion ändern, indem Sie die <xref:System.Windows.Forms.MonthCalendar.ShowToday%2A> -Eigenschaft und die-Eigenschaft auf festlegen <xref:System.Windows.Forms.MonthCalendar.ShowTodayCircle%2A> `false` . Sie können dem Kalender auch Wochen Nummern hinzufügen, indem Sie die- <xref:System.Windows.Forms.MonthCalendar.ShowWeekNumbers%2A> Eigenschaft auf festlegen `true` . Durch Festlegen der <xref:System.Windows.Forms.MonthCalendar.CalendarDimensions%2A> -Eigenschaft können mehrere Monate horizontal und vertikal angezeigt werden. Standardmäßig wird Sonntag als erster Tag der Woche angezeigt, aber jeder Tag kann mithilfe der-Eigenschaft festgelegt werden <xref:System.Windows.Forms.MonthCalendar.FirstDayOfWeek%2A> .  
  
 Sie können auch festlegen, dass bestimmte Datumsangaben auf einmal, jährlich oder monatlich angezeigt werden, indem Sie <xref:System.DateTime> den <xref:System.Windows.Forms.MonthCalendar.BoldedDates%2A> <xref:System.Windows.Forms.MonthCalendar.AnnuallyBoldedDates%2A> -,-und-Eigenschaften-Objekte hinzufügen <xref:System.Windows.Forms.MonthCalendar.MonthlyBoldedDates%2A> . Weitere Informationen finden Sie unter Gewusst [wie: Anzeigen bestimmter Tage in Fett Schrift mit dem Windows Forms MonthCalendar-Steuer](display-specific-days-in-bold-with-wf-monthcalendar-control.md)Element.  
  
 Die Schlüsseleigenschaft des <xref:System.Windows.Forms.MonthCalendar> Steuer Elements ist <xref:System.Windows.Forms.MonthCalendar.SelectionRange%2A> , der im-Steuerelement ausgewählte Bereich von Datumsangaben. Der <xref:System.Windows.Forms.MonthCalendar.SelectionRange%2A> Wert darf die maximale Anzahl von Tagen, die ausgewählt werden können, nicht überschreiten, die in der-Eigenschaft festgelegt ist <xref:System.Windows.Forms.MonthCalendar.MaxSelectionCount%2A> . Die frühesten und aktuellsten Daten, die der Benutzer auswählen kann, werden durch die-Eigenschaft und die-Eigenschaft bestimmt <xref:System.Windows.Forms.MonthCalendar.MaxDate%2A> <xref:System.Windows.Forms.MonthCalendar.MinDate%2A> .  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.MonthCalendar>
- [MonthCalendar-Steuerelement](monthcalendar-control-windows-forms.md)
