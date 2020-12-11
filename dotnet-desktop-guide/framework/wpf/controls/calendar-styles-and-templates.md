---
title: Calendar-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- styles [WPF], Calendar
- templates [WPF], Calendar
- states [WPF], Calendar
- parts [WPF], Calendar
- Calendar [WPF], styles and templates
- ControlTemplate [WPF], Calendar
ms.assetid: f4fcf046-7a8f-41b8-b5a8-534b64e0345c
ms.openlocfilehash: 3639a6f012aae7e15bae0e765e46f92015273286
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977363"
---
# <a name="calendar-styles-and-templates"></a>Calendar-Stile und -Vorlagen
In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.Calendar> . Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen. Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.  
  
## <a name="calendar-parts"></a>Kalender Teile  
 In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.Calendar> .  
  
|Teil|type|BESCHREIBUNG|  
|-|-|-|  
|PART_CalendarItem|<xref:System.Windows.Controls.Primitives.CalendarItem>|Der derzeit auf dem angezeigte Monat oder Jahr <xref:System.Windows.Controls.Calendar> .|  
|PART_Root|<xref:System.Windows.Controls.Panel>|Der Bereich, der die enthält <xref:System.Windows.Controls.Primitives.CalendarItem> .|  
  
## <a name="calendar-states"></a>Kalender Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.Calendar> .  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|----------------------|---------------------------|-----------------|  
|Gültig|ValidationStates|Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .|  
|InvalidFocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.|  
|InvalidUnfocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.|  
  
## <a name="calendaritem-parts"></a>CalendarItem-Teile  
 In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.Primitives.CalendarItem> .  
  
|Teil|type|BESCHREIBUNG|  
|-|-|-|  
|PART_Root|<xref:System.Windows.FrameworkElement>|Der Stamm des Steuer Elements.|  
|PART_PreviousButton|<xref:System.Windows.Controls.Button>|Die Schaltfläche, die die vorherige Seite des Kalenders anzeigt, wenn darauf geklickt wird.|  
|PART_NextButton|<xref:System.Windows.Controls.Button>|Die Schaltfläche, die die nächste Seite des Kalenders anzeigt, wenn darauf geklickt wird.|  
|PART_HeaderButton|<xref:System.Windows.Controls.Button>|Die Schaltfläche, die das Wechseln zwischen Monats Modus, Jahr Modus und Jahrzehnt Modus ermöglicht.|  
|PART_MonthView|<xref:System.Windows.Controls.Grid>|Hostet den Inhalt im Monats Modus.|  
|PART_YearView|<xref:System.Windows.Controls.Grid>|Hostet den Inhalt im Jahr-oder Jahrzehnten-Modus.|  
|PART_DisabledVisual|<xref:System.Windows.FrameworkElement>|Das Overlay für den deaktivierten Zustand.|  
|Daytitletemplate|<xref:System.Windows.DataTemplate>|Der <xref:System.Windows.DataTemplate> , der die visuelle Struktur beschreibt.|  
  
## <a name="calendaritem-states"></a>CalendarItem-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.Primitives.CalendarItem> .  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Normaler Zustand|CommonStates|Der Standardzustand|  
|Deaktivierter Zustand|CommonStates|Der Status des Kalenders, wenn die- <xref:System.Windows.UIElement.IsEnabled%2A> Eigenschaft ist `false` .|  
|Gültig|ValidationStates|Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .|  
|InvalidFocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.|  
|InvalidUnfocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.|  
|Gültig|ValidationStates|Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .|  
|InvalidFocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.|  
|InvalidUnfocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.|  
  
## <a name="calendardaybutton-parts"></a>CalendarDayButton-Teile  
 Das- <xref:System.Windows.Controls.Primitives.CalendarDayButton> Steuerelement verfügt über keine benannten Teile.  
  
## <a name="calendardaybutton-states"></a>CalendarDayButton-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.Primitives.CalendarDayButton> .  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Normal|CommonStates|Der Standardzustand|  
|Deaktiviert|CommonStates|Der <xref:System.Windows.Controls.Primitives.CalendarDayButton> ist deaktiviert.|  
|MouseOver|CommonStates|Der Mauszeiger befindet sich über dem <xref:System.Windows.Controls.Primitives.CalendarDayButton> .|  
|Gedrückt|CommonStates|Der <xref:System.Windows.Controls.Primitives.CalendarDayButton> wird gedrückt.|  
|Ausgewählt|SelectionStates|Die Schaltfläche ist ausgewählt.|  
|Nicht markiert|SelectionStates|Die Schaltfläche ist nicht ausgewählt.|  
|Calendarbuttonfokussierte|Calendarbuttonfocusstates|Die Schaltfläche hat den Fokus.|  
|Calendarbuttonunfokussiert|Calendarbuttonfocusstates|Die Schaltfläche hat keinen Fokus.|  
|Focused|FocusStates|Die Schaltfläche hat den Fokus.|  
|Ohne Fokus|FocusStates|Die Schaltfläche hat keinen Fokus.|  
|Aktiv|Activestates|Die Schaltfläche ist aktiv.|  
|Inaktiv|Activestates|Die Schaltfläche ist inaktiv.|  
|Regularday|Daystates|Die Schaltfläche stellt nicht dar <xref:System.DateTime.Today%2A?displayProperty=nameWithType> .|  
|Heute|Daystates|Die Schaltfläche stellt dar <xref:System.DateTime.Today%2A?displayProperty=nameWithType> .|  
|Normaltag|Blackoutdaystates|Die Schaltfläche stellt einen Tag dar, der ausgewählt werden kann.|  
|Blackoutday|Blackoutdaystates|Die Schaltfläche stellt einen Tag dar, der nicht ausgewählt werden kann.|  
|Gültig|ValidationStates|Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .|  
|InvalidFocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.|  
|InvalidUnfocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.|  
  
## <a name="calendarbutton-parts"></a>CalendarButton-Teile  
 Das- <xref:System.Windows.Controls.Primitives.CalendarButton> Steuerelement verfügt über keine benannten Teile.  
  
## <a name="calendarbutton-states"></a>CalendarButton-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.Primitives.CalendarButton> .  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Normal|CommonStates|Der Standardzustand|  
|Deaktiviert|CommonStates|Der <xref:System.Windows.Controls.Primitives.CalendarButton> ist deaktiviert.|  
|MouseOver|CommonStates|Der Mauszeiger befindet sich über dem <xref:System.Windows.Controls.Primitives.CalendarButton> .|  
|Gedrückt|CommonStates|Der <xref:System.Windows.Controls.Primitives.CalendarButton> wird gedrückt.|  
|Ausgewählt|SelectionStates|Die Schaltfläche ist ausgewählt.|  
|Nicht markiert|SelectionStates|Die Schaltfläche ist nicht ausgewählt.|  
|Calendarbuttonfokussierte|Calendarbuttonfocusstates|Die Schaltfläche hat den Fokus.|  
|Calendarbuttonunfokussiert|Calendarbuttonfocusstates|Die Schaltfläche hat keinen Fokus.|  
|Focused|FocusStates|Die Schaltfläche hat den Fokus.|  
|Ohne Fokus|FocusStates|Die Schaltfläche hat keinen Fokus.|  
|Aktiv|Activestates|Die Schaltfläche ist aktiv.|  
|Inaktiv|Activestates|Die Schaltfläche ist inaktiv.|  
|Gültig|ValidationStates|Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .|  
|InvalidFocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.|  
|InvalidUnfocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.|  
  
## <a name="calendar-controltemplate-example"></a>Beispiel für Calendar ControlTemplate  
 Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das <xref:System.Windows.Controls.Calendar> -Steuerelement und zugeordnete Typen definiert wird.  
  
 [!code-xaml[ControlTemplateExamples#Calendar](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/calendar.xaml#calendar)]  
  
 Im vorhergehenden Beispiel wird mindestens eine der folgenden Ressourcen verwendet.  
  
 [!code-xaml[ControlTemplateExamples#Resources](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/shared.xaml#resources)]  
  
 Das vollständige Beispiel finden Sie unter [Beispiel zum Formatieren mit ControlTemplates](https://github.com/Microsoft/WPF-Samples/tree/master/Styles%20&%20Templates/IntroToStylingAndTemplating).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.FrameworkElement.Style%2A>
- <xref:System.Windows.Controls.ControlTemplate>
- [Steuerelementformate und -vorlagen](control-styles-and-templates.md)
- [Anpassung von Steuerelementen](control-customization.md)
- [Erstellen von Formaten und Vorlagen](/dotnet/desktop-wpf/fundamentals/styles-templates-overview)
- [Erstellen einer Vorlage für ein Steuerelement](/dotnet/desktop-wpf/themes/how-to-create-apply-template)
