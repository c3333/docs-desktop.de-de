---
title: Kalender
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], Calendar
- Calendar control [WPF]
ms.assetid: ee844e4a-eefe-48e2-bd0d-1d82cc5e960b
ms.openlocfilehash: c06cd34739dd25f717a5ea2cbc9803453558a400
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977360"
---
# <a name="calendar"></a>Kalender
Ein Kalender ermöglicht einem Benutzer das Auswählen eines Datums mithilfe einer visuellen Kalender Anzeige.  
  
 Ein- <xref:System.Windows.Controls.Calendar> Steuerelement kann eigenständig oder als Dropdown Teil eines-Steuer Elements verwendet werden <xref:System.Windows.Controls.DatePicker> . Weitere Informationen finden Sie unter <xref:System.Windows.Controls.DatePicker>.  
  
 In der folgenden Abbildung werden zwei Steuer <xref:System.Windows.Controls.Calendar> Elemente dargestellt: eine mit Auswahl-und Datenstrom Daten und eine ohne.  
  
 ![Calendar-Steuerelemente](./media/ndp-calendarcontrols.png "NDP_CalendarControls")  
Calendar-Steuerelemente  
  
 In der folgenden Tabelle finden Sie Informationen zu Aufgaben, die in der Regel mit verknüpft sind <xref:System.Windows.Controls.Calendar> .  
  
|Aufgabe|Implementierung|  
|----------|--------------------|  
|Angeben von Datumsangaben, die nicht ausgewählt werden können.|Verwenden Sie die <xref:System.Windows.Controls.Calendar.BlackoutDates%2A>-Eigenschaft.|  
|Lassen Sie die <xref:System.Windows.Controls.Calendar> Anzeige einen Monat, ein ganzes Jahr oder ein Jahrzehnt lang anzeigen.|Legen Sie die- <xref:System.Windows.Controls.Calendar.DisplayMode%2A> Eigenschaft auf month, Year oder Decade fest.|  
|Geben Sie an, ob der Benutzer ein Datum, einen Datumsbereich oder mehrere Datumsbereiche auswählen kann.|Verwenden Sie <xref:System.Windows.Controls.Calendar.SelectionMode%2A>.|  
|Geben Sie den Datumsbereich an, der von <xref:System.Windows.Controls.Calendar> angezeigt wird.|Verwenden Sie die <xref:System.Windows.Controls.Calendar.DisplayDateStart%2A>-Eigenschaft und die <xref:System.Windows.Controls.Calendar.DisplayDateEnd%2A>-Eigenschaft.|  
|Geben Sie an, ob das aktuelle Datum hervorgehoben ist.|Verwenden Sie die <xref:System.Windows.Controls.Calendar.IsTodayHighlighted%2A>-Eigenschaft. Standardmäßig <xref:System.Windows.Controls.Calendar.IsTodayHighlighted%2A> ist `true` .|  
|Ändern Sie die Größe des <xref:System.Windows.Controls.Calendar> .|Verwenden <xref:System.Windows.Controls.Viewbox> Sie, oder legen <xref:System.Windows.FrameworkElement.LayoutTransform%2A> Sie die-Eigenschaft auf fest <xref:System.Windows.Media.ScaleTransform> . Beachten Sie Folgendes: Wenn Sie die <xref:System.Windows.FrameworkElement.Width%2A> -Eigenschaft und die-Eigenschaft eines festlegen, wird <xref:System.Windows.FrameworkElement.Height%2A> <xref:System.Windows.Controls.Calendar> die Größe des eigentlichen Kalenders nicht geändert.|  
  
 Das- <xref:System.Windows.Controls.Calendar> Steuerelement bietet eine einfache Navigation mit der Maus oder der Tastatur. In der folgenden Tabelle wird die Tastaturnavigation zusammengefasst.  
  
|Tastenkombination|<xref:System.Windows.Controls.Calendar.DisplayMode%2A>|Aktion|  
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|------------|  
|Gift|<xref:System.Windows.Controls.CalendarMode.Month>|Ändert die- <xref:System.Windows.Controls.Calendar.SelectedDate%2A> Eigenschaft, wenn die- <xref:System.Windows.Controls.Calendar.SelectionMode%2A> Eigenschaft nicht auf festgelegt ist <xref:System.Windows.Controls.CalendarSelectionMode.None> .|  
|Gift|<xref:System.Windows.Controls.CalendarMode.Year>|Ändert den Monat der <xref:System.Windows.Controls.Calendar.DisplayDate%2A> Eigenschaft. Beachten Sie, dass sich das <xref:System.Windows.Controls.Calendar.SelectedDate%2A> nicht ändert.|  
|Gift|<xref:System.Windows.Controls.CalendarMode.Decade>|Ändert das Jahr von <xref:System.Windows.Controls.Calendar.DisplayDate%2A> . Beachten Sie, dass sich das <xref:System.Windows.Controls.Calendar.SelectedDate%2A> nicht ändert.|  
|Umschalt + Pfeil|<xref:System.Windows.Controls.CalendarMode.Month>|Wenn <xref:System.Windows.Controls.Calendar.SelectionMode%2A> nicht auf oder festgelegt ist <xref:System.Windows.Controls.CalendarSelectionMode.SingleDate> <xref:System.Windows.Controls.CalendarSelectionMode.None> , erweitert den Bereich der ausgewählten Datumsangaben.|  
|POS1|<xref:System.Windows.Controls.CalendarMode.Month>|Ändert den <xref:System.Windows.Controls.Calendar.SelectedDate%2A> auf den ersten Tag des aktuellen Monats.|  
|POS1|<xref:System.Windows.Controls.CalendarMode.Year>|Ändert den Monat des <xref:System.Windows.Controls.Calendar.DisplayDate%2A> in den ersten Monat des Jahres. Der <xref:System.Windows.Controls.Calendar.SelectedDate%2A> ändert sich nicht.|  
|POS1|<xref:System.Windows.Controls.CalendarMode.Decade>|Ändert das Jahr des <xref:System.Windows.Controls.Calendar.DisplayDate%2A> auf das erste Jahr des Jahrzehnts. Der <xref:System.Windows.Controls.Calendar.SelectedDate%2A> ändert sich nicht.|  
|ENDE|<xref:System.Windows.Controls.CalendarMode.Month>|Ändert den <xref:System.Windows.Controls.Calendar.SelectedDate%2A> auf den letzten Tag des aktuellen Monats.|  
|ENDE|<xref:System.Windows.Controls.CalendarMode.Year>|Ändert den Monat des <xref:System.Windows.Controls.Calendar.DisplayDate%2A> in den letzten Monat des Jahres. Der <xref:System.Windows.Controls.Calendar.SelectedDate%2A> ändert sich nicht.|  
|ENDE|<xref:System.Windows.Controls.CalendarMode.Decade>|Ändert das Jahr des <xref:System.Windows.Controls.Calendar.DisplayDate%2A> in das letzte Jahr des Jahrzehnts. Der <xref:System.Windows.Controls.Calendar.SelectedDate%2A> ändert sich nicht.|  
|STRG+NACH-OBEN-TASTE|Any|Wechselt zur nächsten größeren <xref:System.Windows.Controls.Calendar.DisplayMode%2A> . Wenn <xref:System.Windows.Controls.Calendar.DisplayMode%2A> bereits ist <xref:System.Windows.Controls.CalendarMode.Decade> , wird keine Aktion ausgeführt.|  
|STRG+NACH-UNTEN-TASTE|Any|Wechselt zum nächsten kleineren <xref:System.Windows.Controls.Calendar.DisplayMode%2A> . Wenn <xref:System.Windows.Controls.Calendar.DisplayMode%2A> bereits ist <xref:System.Windows.Controls.CalendarMode.Month> , wird keine Aktion ausgeführt.|  
|Leertaste oder EINGABETASTE|<xref:System.Windows.Controls.CalendarMode.Year> oder <xref:System.Windows.Controls.CalendarMode.Decade>|Wechselt <xref:System.Windows.Controls.Calendar.DisplayMode%2A> zum oder, das <xref:System.Windows.Controls.CalendarMode.Month> <xref:System.Windows.Controls.CalendarMode.Year> durch ein Fokus Element dargestellt wird.|  
  
## <a name="see-also"></a>Siehe auch

- [Steuerelemente](index.md)
- [Erstellen von Formaten und Vorlagen](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
