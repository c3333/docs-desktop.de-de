---
title: DatePicker
ms.date: 03/30/2017
helpviewer_keywords:
- controls [WPF], DatePicker
- DatePicker control [WPF]
ms.assetid: 619765c8-8d25-4315-aec2-79aea08fed9f
ms.openlocfilehash: 4e4b536aca768872a0729a9b34a5dc1cc17e04fb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977471"
---
# <a name="datepicker"></a>DatePicker
Das- <xref:System.Windows.Controls.DatePicker> Steuerelement ermöglicht es dem Benutzer, ein Datum auszuwählen, indem es entweder in ein Textfeld eingegeben oder ein Dropdown-Steuerelement verwendet wird <xref:System.Windows.Controls.Calendar> .  
  
 In der folgenden Abbildung wird ein gezeigt <xref:System.Windows.Controls.DatePicker> .  
  
 ![DatePicker-Steuerelement](./media/ndp-datepicker.png "NDP_DatePicker")  
DatePicker-Steuerelement  
  
 Viele der <xref:System.Windows.Controls.DatePicker> Eigenschaften eines Steuer Elements dienen der Verwaltung seiner integrierten <xref:System.Windows.Controls.Calendar> und der entsprechenden-Funktion in <xref:System.Windows.Controls.Calendar> . Insbesondere die <xref:System.Windows.Controls.DatePicker.IsTodayHighlighted%2A?displayProperty=nameWithType> <xref:System.Windows.Controls.DatePicker.FirstDayOfWeek%2A?displayProperty=nameWithType> Eigenschaften,, <xref:System.Windows.Controls.DatePicker.BlackoutDates%2A?displayProperty=nameWithType> ,, <xref:System.Windows.Controls.DatePicker.DisplayDateStart%2A?displayProperty=nameWithType> <xref:System.Windows.Controls.DatePicker.DisplayDateEnd%2A?displayProperty=nameWithType> , <xref:System.Windows.Controls.DatePicker.DisplayDate%2A?displayProperty=nameWithType> und <xref:System.Windows.Controls.DatePicker.SelectedDate%2A?displayProperty=nameWithType> funktionieren identisch mit Ihren <xref:System.Windows.Controls.Calendar> Entsprechungen. Weitere Informationen finden Sie unter <xref:System.Windows.Controls.Calendar>.  
  
 Benutzer können ein Datum direkt in ein Textfeld eingeben, mit dem die-Eigenschaft festgelegt wird <xref:System.Windows.Controls.DatePicker.Text%2A> . Wenn die <xref:System.Windows.Controls.DatePicker> eingegebene Zeichenfolge nicht in ein gültiges Datum konvertieren kann, wird das- <xref:System.Windows.Controls.DatePicker.DateValidationError> Ereignis ausgelöst. Standardmäßig verursacht dies eine Ausnahme, aber ein Ereignishandler für <xref:System.Windows.Controls.DatePicker.DateValidationError> kann die <xref:System.Windows.Controls.DatePickerDateValidationErrorEventArgs.ThrowException%2A> -Eigenschaft auf festlegen `false` und verhindern, dass eine Ausnahme ausgelöst wird.  
  
## <a name="see-also"></a>Siehe auch

- [Steuerelemente](index.md)
- [Erstellen von Formaten und Vorlagen](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
