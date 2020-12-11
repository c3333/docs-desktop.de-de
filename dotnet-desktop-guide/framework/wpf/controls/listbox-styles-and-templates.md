---
title: ListBox-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- styles [WPF], ListBox
- templates [WPF], ListBox
- states [WPF], ListBox
- ControlTemplate [WPF], ListBox
- parts [WPF], ListBox
- ListBox [WPF], styles and templates
ms.assetid: fc5764cb-c27b-495b-88d4-d969a8213ccb
ms.openlocfilehash: d97977de37924219f5b492a8659f2d55676ec2c4
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974867"
---
# <a name="listbox-styles-and-templates"></a>ListBox-Stile und -Vorlagen
In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.ListBox> . Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen. Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.  
  
## <a name="listbox-parts"></a>ListBox-Teile  
 Das- <xref:System.Windows.Controls.ListBox> Steuerelement verfügt über keine benannten Teile.  
  
 Wenn Sie einen <xref:System.Windows.Controls.ControlTemplate> für eine erstellen <xref:System.Windows.Controls.ListBox> , enthält die Vorlage möglicherweise eine <xref:System.Windows.Controls.ItemsPresenter> innerhalb eines <xref:System.Windows.Controls.ScrollViewer> . (Die <xref:System.Windows.Controls.ItemsPresenter> zeigt jedes Element in der an <xref:System.Windows.Controls.ListBox> ; das <xref:System.Windows.Controls.ScrollViewer> ermöglicht das Scrollen im-Steuerelement).  Wenn das <xref:System.Windows.Controls.ItemsPresenter> nicht das direkt untergeordnete Element von ist <xref:System.Windows.Controls.ScrollViewer> , müssen Sie den <xref:System.Windows.Controls.ItemsPresenter> Namen, `ItemsPresenter` .  
  
## <a name="listbox-states"></a>ListBox-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.ListBox> .  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Gültig|ValidationStates|Das Steuerelement ist gültig.|  
|InvalidFocused|ValidationStates|Das Steuerelement ist nicht gültig und besitzt den Fokus.|  
|InvalidUnfocused|ValidationStates|Das Steuerelement ist nicht gültig und besitzt keinen Fokus.|  
  
## <a name="listboxitem-parts"></a>ListBoxItem-Teile  
 Das- <xref:System.Windows.Controls.ListBoxItem> Steuerelement verfügt über keine benannten Teile.  
  
## <a name="listboxitem-states"></a>ListBoxItem-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.ListBox> .  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Normal|CommonStates|Der Standardzustand|  
|MouseOver|CommonStates|Der Mauszeiger ist über dem Steuerelement positioniert.|  
|Deaktiviert|CommonStates|Das Element ist deaktiviert.|  
|Focused|FocusStates|Das Element besitzt den Fokus.|  
|Ohne Fokus|FocusStates|Das Element besitzt den Fokus nicht.|  
|Nicht markiert|SelectionStates|Das Element ist nicht ausgewählt.|  
|Ausgewählt|SelectionStates|Das Element ist zurzeit ausgewählt.|  
|SelectedUnfocused|SelectionStates|Das Element ist ausgewählt, besitzt jedoch keinen Fokus.|  
|Gültig|ValidationStates|Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .|  
|InvalidFocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.|  
|InvalidUnfocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.|  
  
## <a name="listbox-controltemplate-example"></a>ListBox-ControlTemplate-Beispiel  
 Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> -Steuerelement für die Steuer <xref:System.Windows.Controls.ListBox> Elemente und definiert wird <xref:System.Windows.Controls.ListBoxItem> .  
  
 [!code-xaml[ControlTemplateExamples#ListBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/listbox.xaml#listbox)]  
  
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
