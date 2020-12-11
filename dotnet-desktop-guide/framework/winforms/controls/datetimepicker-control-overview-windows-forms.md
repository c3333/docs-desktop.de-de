---
title: Übersicht über das DateTimePicker-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- DateTimePicker
helpviewer_keywords:
- DateTimePicker control [Windows Forms], about
- date and time picker controls
ms.assetid: 501af106-e9fc-4efc-b9b3-c9d8dcaf8c5c
ms.openlocfilehash: 63271dd91116c1f68d426f3ed5aa710644ded928
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972159"
---
# <a name="datetimepicker-control-overview-windows-forms"></a>Übersicht über das DateTimePicker-Steuerelement (Windows Forms)
Das Windows Forms <xref:System.Windows.Forms.DateTimePicker> Steuerelement ermöglicht es dem Benutzer, ein einzelnes Element aus einer Liste von Datumsangaben oder Uhrzeiten auszuwählen. Wenn ein Datum verwendet wird, wird es in zwei Teilen angezeigt: in einer Dropdown Liste mit einem Datum, das in Text dargestellt ist, und in einem Raster, das angezeigt wird, wenn Sie auf den Pfeil nach unten neben der Liste klicken. Das Raster sieht wie das-Steuerelement aus <xref:System.Windows.Forms.MonthCalendar> , das zum Auswählen mehrerer Datumsangaben verwendet werden kann. Weitere Informationen zum Steuerelement finden Sie unter Übersicht über das <xref:System.Windows.Forms.MonthCalendar> [MonthCalendar-Steuer](monthcalendar-control-overview-windows-forms.md)Element.  
  
## <a name="key-properties"></a>Schlüsseleigenschaften  
 Wenn das <xref:System.Windows.Forms.DateTimePicker> als Steuerelement zum auswählen oder Bearbeiten von Zeiten anstelle von Datumsangaben angezeigt werden soll, legen Sie die <xref:System.Windows.Forms.DateTimePicker.ShowUpDown%2A> -Eigenschaft auf `true` und die- <xref:System.Windows.Forms.DateTimePicker.Format%2A> Eigenschaft auf fest <xref:System.Windows.Forms.DateTimePickerFormat.Time> . Weitere Informationen finden Sie unter Gewusst [wie: Anzeigen der Zeit mithilfe des DateTimePicker-Steuer](how-to-display-time-with-the-datetimepicker-control.md)Elements.  
  
 Wenn die- <xref:System.Windows.Forms.DateTimePicker.ShowCheckBox%2A> Eigenschaft auf festgelegt ist `true` , wird im-Steuerelement neben dem ausgewählten Datum ein Kontrollkästchen angezeigt. Wenn das Kontrollkästchen aktiviert ist, kann der ausgewählte Datums-/Uhrzeitwert aktualisiert werden. Wenn das Kontrollkästchen leer ist, wird der Wert nicht verfügbar angezeigt.  
  
 Die-und-Eigenschaften des-Steuer Elements <xref:System.Windows.Forms.DateTimePicker.MaxDate%2A> <xref:System.Windows.Forms.DateTimePicker.MinDate%2A> bestimmen den Datums-und uhrzeitanbereich. Die- <xref:System.Windows.Forms.DateTimePicker.Value%2A> Eigenschaft enthält das aktuelle Datum und die Uhrzeit, zu der das Steuerelement auf festgelegt ist Weitere Informationen finden Sie unter Gewusst [wie: festlegen und Zurückgeben von Datumsangaben mit dem Windows Forms DateTimePicker-Steuer](how-to-set-and-return-dates-with-the-windows-forms-datetimepicker-control.md)Element. Die Werte können in vier Formaten angezeigt werden, die von der-Eigenschaft festgelegt werden <xref:System.Windows.Forms.DateTimePicker.Format%2A> : <xref:System.Windows.Forms.DateTimePickerFormat.Long> , <xref:System.Windows.Forms.DateTimePickerFormat.Short> , <xref:System.Windows.Forms.DateTimePickerFormat.Time> oder <xref:System.Windows.Forms.DateTimePickerFormat.Custom> . Wenn ein benutzerdefiniertes Format ausgewählt ist, müssen Sie die- <xref:System.Windows.Forms.DateTimePicker.CustomFormat%2A> Eigenschaft auf eine entsprechende Zeichenfolge festlegen. Weitere Informationen finden Sie unter Gewusst [wie: Anzeigen eines Datums in einem benutzerdefinierten Format mit dem Windows Forms DateTimePicker-Steuer](display-a-date-in-a-custom-format-with-wf-datetimepicker-control.md)Element.  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Anzeigen eines Datums im benutzerdefinierten Format mit dem DateTimePicker-Steuerelement in Windows Forms](display-a-date-in-a-custom-format-with-wf-datetimepicker-control.md)
- [Vorgehensweise: Festlegen und Zurückgeben von Datumsangaben mit dem DateTimePicker-Steuerelement in Windows Forms](how-to-set-and-return-dates-with-the-windows-forms-datetimepicker-control.md)
