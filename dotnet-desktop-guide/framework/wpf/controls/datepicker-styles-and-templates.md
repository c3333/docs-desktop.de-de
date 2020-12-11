---
title: DatePicker-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- ControlTemplate [WPF], DatePicker
- DatePicker [WPF], styles and templates
- templates [WPF], DatePicker
- parts [WPF], DatePicker
- styles [WPF], DatePicker
- states [WPF], DatePicker
ms.assetid: c430a657-692f-44bd-a549-2341f92d6115
ms.openlocfilehash: c6663ae3f7f4eefc61c1a07d968ea300a485e157
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977473"
---
# <a name="datepicker-styles-and-templates"></a>DatePicker-Stile und -Vorlagen
In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.DatePicker> . Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen. Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.  
  
## <a name="datepicker-parts"></a>DatePicker-Teile  
 In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.DatePicker> .  
  
|Teil|type|BESCHREIBUNG|  
|-|-|-|  
|PART_Root|<xref:System.Windows.Controls.Grid>|Der Stamm des Steuer Elements.|  
|PART_Button|<xref:System.Windows.Controls.Button>|Die Schaltfläche, die das öffnet und schließt <xref:System.Windows.Controls.Calendar> .|  
|PART_TextBox|<xref:System.Windows.Controls.Primitives.DatePickerTextBox>|Das Textfeld, in dem Sie ein Datum eingeben können.|  
|PART_Popup|<xref:System.Windows.Controls.Primitives.Popup>|Das Popup-Element für das <xref:System.Windows.Controls.DatePicker> Steuerelement.|  
  
## <a name="datepicker-states"></a>DatePicker-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.DatePicker> .  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Normal|CommonStates|Der Standardzustand|  
|Deaktiviert|CommonStates|Der <xref:System.Windows.Controls.DatePicker> ist deaktiviert.|  
|Gültig|ValidationStates|Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .|  
|InvalidFocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.|  
|InvalidUnfocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.|  
  
## <a name="datepickertextbox-parts"></a>DatePickerTextBox-Teile  
 In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.Primitives.DatePickerTextBox> .  
  
|Teil|type|BESCHREIBUNG|  
|-|-|-|  
|PART_Watermark|<xref:System.Windows.Controls.ContentControl>|Das Element, das den Anfangstext in der enthält <xref:System.Windows.Controls.DatePicker> .|  
|PART_ContentElement|<xref:System.Windows.FrameworkElement>|Ein visuelles Element, das ein enthalten kann <xref:System.Windows.FrameworkElement> . Der Text des <xref:System.Windows.Controls.TextBox> wird in diesem Element angezeigt.|  
  
## <a name="datepickertextbox-states"></a>DatePickerTextBox-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.Primitives.DatePickerTextBox> .  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Normal|CommonStates|Der Standardzustand|  
|Deaktiviert|CommonStates|Der <xref:System.Windows.Controls.Primitives.DatePickerTextBox> ist deaktiviert.|  
|MouseOver|CommonStates|Der Mauszeiger befindet sich über dem <xref:System.Windows.Controls.Primitives.DatePickerTextBox> .|  
|ReadOnly|CommonStates|Der Benutzer kann den Text in der nicht ändern <xref:System.Windows.Controls.Primitives.DatePickerTextBox> .|  
|Focused|FocusStates|Der Fokus liegt auf dem Steuerelement.|  
|Ohne Fokus|FocusStates|Der Fokus liegt nicht auf dem Steuerelement.|  
|Genauer Beobachtung erfolgen|Watermarkstates|Das-Steuerelement zeigt den ursprünglichen Text an.  Der <xref:System.Windows.Controls.Primitives.DatePickerTextBox> befindet sich im-Zustand, wenn der Benutzer keinen Text eingegeben hat oder ein Datum ausgewählt hat.|  
|Wasserzeichen|Watermarkstates|Der Benutzer hat Text in das eingegeben <xref:System.Windows.Controls.Primitives.DatePickerTextBox> oder ein Datum in der ausgewählt <xref:System.Windows.Controls.DatePicker> .|  
|Gültig|ValidationStates|Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .|  
|InvalidFocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, `true` und das Steuerelement besitzt den Fokus.|  
|InvalidUnfocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, `true` und das Steuerelement besitzt keinen Fokus.|  
  
## <a name="datepicker-controltemplate-example"></a>DatePicker ControlTemplate-Beispiel  
 Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.DatePicker> .  
  
 [!code-xaml[ControlTemplateExamples#DatePicker](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/datepicker.xaml#datepicker)]  
  
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
