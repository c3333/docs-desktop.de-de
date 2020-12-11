---
title: ComboBox-Stile und -Vorlagen
description: Erfahren Sie mehr über Stile und Vorlagen für das Windows Presentation Foundation ComboBox-Steuerelement. Ändern Sie ControlTemplate, um dem Steuerelement eine eindeutige Darstellung zu verschaffen.
ms.date: 03/30/2017
helpviewer_keywords:
- ComboBox [WPF], styles and templates
- states [WPF], ComboBox
- ControlTemplate [WPF], ComboBox
- styles [WPF], ComboBox
- templates [WPF], ComboBox
- parts [WPF], ComboBox
ms.assetid: b0662fa1-16d7-4320-b26b-c1804e565a44
ms.openlocfilehash: de8d9f4671b97ac4349c2c2a1093807dadec9f7c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977346"
---
# <a name="combobox-styles-and-templates"></a>ComboBox-Stile und -Vorlagen
In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.ComboBox> . Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen. Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.  
  
## <a name="combobox-parts"></a>ComboBox-Teile  
 In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.ComboBox> .  
  
|Teil|type|BESCHREIBUNG|  
|-|-|-|  
|PART_EditableTextBox|<xref:System.Windows.Controls.TextBox>|Enthält den Text von <xref:System.Windows.Controls.ComboBox> .|  
|PART_Popup|<xref:System.Windows.Controls.Primitives.Popup>|Das Dropdown-Element, das die Elemente im Kombinations Feld enthält.|  
  
 Wenn Sie einen <xref:System.Windows.Controls.ControlTemplate> für eine erstellen <xref:System.Windows.Controls.ComboBox> , enthält die Vorlage möglicherweise eine <xref:System.Windows.Controls.ItemsPresenter> innerhalb eines <xref:System.Windows.Controls.ScrollViewer> . (Die <xref:System.Windows.Controls.ItemsPresenter> zeigt jedes Element in der an <xref:System.Windows.Controls.ComboBox> ; das <xref:System.Windows.Controls.ScrollViewer> ermöglicht das Scrollen im-Steuerelement).  Wenn das <xref:System.Windows.Controls.ItemsPresenter> nicht das direkt untergeordnete Element von ist <xref:System.Windows.Controls.ScrollViewer> , müssen Sie den <xref:System.Windows.Controls.ItemsPresenter> Namen, `ItemsPresenter` .  
  
## <a name="combobox-states"></a>ComboBox-Zustände  
 In der folgenden Tabelle sind die Zustände für das-Steuerelement aufgeführt <xref:System.Windows.Controls.ComboBox> .  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Normal|CommonStates|Der Standardzustand|  
|Deaktiviert|CommonStates|Das Steuerelement ist deaktiviert.|  
|MouseOver|CommonStates|Der Mauszeiger befindet sich über dem <xref:System.Windows.Controls.ComboBox> Steuerelement.|  
|Focused|FocusStates|Der Fokus liegt auf dem Steuerelement.|  
|Ohne Fokus|FocusStates|Der Fokus liegt nicht auf dem Steuerelement.|  
|Focuseddropdown|FocusStates|Das Dropdown-für das <xref:System.Windows.Controls.ComboBox> hat den Fokus.|  
|Gültig|ValidationStates|Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .|  
|InvalidFocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, `true` und das Steuerelement besitzt den Fokus.|  
|InvalidUnfocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, `true` und das Steuerelement besitzt keinen Fokus.|  
|Bearbeitbar|Editstates|Die <xref:System.Windows.Controls.ComboBox.IsEditable%2A>-Eigenschaft ist `true`.|  
|Editierbar|Editstates|Die <xref:System.Windows.Controls.ComboBox.IsEditable%2A>-Eigenschaft ist `false`.|  
  
## <a name="comboboxitem-parts"></a>ComboBoxItem-Teile  
 Das- <xref:System.Windows.Controls.ComboBoxItem> Steuerelement verfügt über keine benannten Teile.  
  
## <a name="comboboxitem-states"></a>ComboBoxItem-Zustände  
 In der folgenden Tabelle sind die Zustände für das-Steuerelement aufgeführt <xref:System.Windows.Controls.ComboBoxItem> .  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Normal|CommonStates|Der Standardzustand|  
|Deaktiviert|CommonStates|Das Steuerelement ist deaktiviert.|  
|MouseOver|CommonStates|Der Mauszeiger befindet sich über dem <xref:System.Windows.Controls.ComboBoxItem> Steuerelement.|  
|Focused|FocusStates|Der Fokus liegt auf dem Steuerelement.|  
|Ohne Fokus|FocusStates|Der Fokus liegt nicht auf dem Steuerelement.|  
|Ausgewählt|SelectionStates|Das Element ist zurzeit ausgewählt.|  
|Nicht markiert|SelectionStates|Das Element ist nicht ausgewählt.|  
|SelectedUnfocused|SelectionStates|Das Element ist ausgewählt, besitzt jedoch keinen Fokus.|  
|Gültig|ValidationStates|Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .|  
|InvalidFocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, `true` und das Steuerelement besitzt den Fokus.|  
|InvalidUnfocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, `true` und das Steuerelement besitzt keinen Fokus.|  
  
## <a name="combobox-controltemplate-example"></a>ComboBox ControlTemplate-Beispiel  
 Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das <xref:System.Windows.Controls.ComboBox> -Steuerelement und zugeordnete Typen definiert wird.  
  
 [!code-xaml[ControlTemplateExamples#ComboBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/combobox.xaml#combobox)]  
  
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
