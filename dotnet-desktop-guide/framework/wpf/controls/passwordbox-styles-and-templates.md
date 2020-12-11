---
title: PasswordBox-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- styles [WPF], PasswordBox
- templates [WPF], PasswordBox
- ControlTemplate [WPF], PasswordBox
- states [WPF], PasswordBox
- PasswordBox [WPF], styles and templates
- parts [WPF], PasswordBox
ms.assetid: deb52107-959f-4a60-b303-d21a0a933060
ms.openlocfilehash: aecd625a052f097aeb2b8cb73743fd4b47df89e1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974612"
---
# <a name="passwordbox-styles-and-templates"></a>PasswordBox-Stile und -Vorlagen

In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.PasswordBox> . Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen. Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.

## <a name="passwordbox-parts"></a>PasswordBox-Teile

In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.PasswordBox> .

|Teil|type|BESCHREIBUNG|
|-|-|-|
|PART_ContentHost|<xref:System.Windows.FrameworkElement>|Ein visuelles Element, das ein enthalten kann <xref:System.Windows.FrameworkElement> . Der Text des <xref:System.Windows.Controls.PasswordBox> wird in diesem Element angezeigt.|

## <a name="passwordbox-states"></a>PasswordBox-Zustände

In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.PasswordBox> .

|VisualState-Name|VisualStateGroup-Name|Beschreibung|
|-|-|-|
|Normal|CommonStates|Der Standardzustand|
|MouseOver|CommonStates|Der Mauszeiger ist über dem Steuerelement positioniert.|
|Deaktiviert|CommonStates|Das Steuerelement ist deaktiviert.|
|Focused|FocusStates|Der Fokus liegt auf dem Steuerelement.|
|Ohne Fokus|FocusStates|Der Fokus liegt nicht auf dem Steuerelement.|
|Gültig|ValidationStates|Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .|
|InvalidFocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.|
|InvalidUnfocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.|

## <a name="passwordbox-controltemplate-example"></a>Beispiel für eine PasswordBox-ControlTemplate

Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.PasswordBox> .

[!code-xaml[ControlTemplateExamples#PasswordBox](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/textbox.xaml#passwordbox)]

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
