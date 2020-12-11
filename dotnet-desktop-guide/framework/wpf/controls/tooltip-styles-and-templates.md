---
title: ToolTip-Formate und Vorlagen
ms.date: 03/30/2017
helpviewer_keywords:
- parts [WPF], ToolTip
- styles [WPF], ToolTip
- states [WPF], ToolTip
- ToolTip [WPF], styles and templates
- ControlTemplate [WPF], ToolTip
- templates [WPF], ToolTip
ms.assetid: 405fe385-4de9-49ee-a448-d8f4d1f740dd
ms.openlocfilehash: bc77555a7663bf1e4cd8cea82d43bf3bd2c33b53
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978227"
---
# <a name="tooltip-styles-and-templates"></a>ToolTip-Formate und Vorlagen
In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.ToolTip> . Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen. Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.  
  
## <a name="tooltip-parts"></a>QuickInfo-Teile  
 Das- <xref:System.Windows.Controls.ToolTip> Steuerelement verfügt über keine benannten Teile.  
  
## <a name="tooltip-states"></a>QuickInfo-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.ToolTip> .  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Geschlossen|Openstates|Der Standardzustand|  
|Öffnen Sie den|Openstates|Der <xref:System.Windows.Controls.ToolTip> ist sichtbar.|  
|Gültig|ValidationStates|Das Steuerelement verwendet die <xref:System.Windows.Controls.Validation> -Klasse, und die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist `false` .|  
|InvalidFocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, dass `true` das Steuerelement den Fokus besitzt.|  
|InvalidUnfocused|ValidationStates|Die <xref:System.Windows.Controls.Validation.HasError%2A?displayProperty=nameWithType> angefügte-Eigenschaft ist, wenn `true` das Steuerelement keinen Fokus hat.|  
  
## <a name="tooltip-controltemplate-example"></a>QuickInfo-ControlTemplate-Beispiel  
 Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das-Steuerelement definiert wird <xref:System.Windows.Controls.ToolTip> .  
  
 [!code-xaml[ControlTemplateExamples#ToolTip](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/tooltip.xaml#tooltip)]  
  
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
