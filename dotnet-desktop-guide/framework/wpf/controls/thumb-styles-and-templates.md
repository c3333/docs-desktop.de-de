---
title: Thumb-Stile und -Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- states [WPF], Thumb
- styles [WPF], Thumb
- templates [WPF], Thumb
- Thumb [WPF], styles and templates
- ControlTemplate [WPF], Thumb
- parts [WPF], Thumb
ms.assetid: 86a49235-62d9-414e-923e-53126e3f930a
ms.openlocfilehash: 6c14280f9514e3c9b1716b55410a46cf843f6b8c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974563"
---
# <a name="thumb-styles-and-templates"></a>Thumb-Stile und -Vorlagen

In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.Primitives.Thumb> . Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen. Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.

## <a name="thumb-parts"></a>Thumb-Teile

Das- <xref:System.Windows.Controls.Primitives.Thumb> Steuerelement verfügt über keine benannten Teile.

## <a name="thumb-states"></a>Thumb-Zustände

In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.Primitives.Thumb> .

|VisualState-Name|VisualStateGroup-Name|Beschreibung|
|-|-|-|
|Normal|CommonStates|Der Standardzustand|
|MouseOver|CommonStates|Der Mauszeiger ist über dem Steuerelement positioniert.|
|Gedrückt|CommonStates|Das Steuerelement wird gedrückt.|
|Deaktiviert|CommonStates|Das Steuerelement ist deaktiviert.|
|Focused|FocusStates|Der Fokus liegt auf dem Steuerelement.|
|Ohne Fokus|FocusStates|Der Fokus liegt nicht auf dem Steuerelement.|
|Gültig|ValidationStates|Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .|
|InvalidFocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.|
|InvalidUnfocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.|

## <a name="thumb-controltemplate-example"></a>Thumb ControlTemplate-Beispiel

Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.Primitives.Thumb> .

[!code-xaml[ControlTemplateExamples#Thumb](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/slider.xaml#thumb)]

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
