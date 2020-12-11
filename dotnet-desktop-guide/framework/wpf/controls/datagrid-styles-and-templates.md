---
title: DataGrid-Stile und -Vorlagen
description: Erfahren Sie mehr über Stile und Vorlagen für das Windows Presentation Foundation DataGrid-Steuerelement. Ändern Sie ControlTemplate, um dem Steuerelement eine eindeutige Darstellung zu verschaffen.
ms.date: 03/30/2017
helpviewer_keywords:
- states [WPF], DataGrid
- ControlTemplate [WPF], DataGrid
- DataGrid [WPF], styles and templates
- templates [WPF], DataGrid
- styles [WPF], DataGrid
- parts [WPF], DataGrid
ms.assetid: 9cb31d63-f148-4d25-b079-816e73f988c7
ms.openlocfilehash: d6deac674b2bc7e8ed0a9857cc1504114f4ba53a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977472"
---
# <a name="datagrid-styles-and-templates"></a>DataGrid-Stile und -Vorlagen
In diesem Thema werden die Stile und Vorlagen für das-Steuerelement beschrieben <xref:System.Windows.Controls.DataGrid> . Sie können die Standardeinstellung ändern <xref:System.Windows.Controls.ControlTemplate> , um dem Steuerelement eine eindeutige Darstellung zu verschaffen. Weitere Informationen finden Sie unter [Erstellen einer Vorlage für ein-Steuer](/dotnet/desktop-wpf/themes/how-to-create-apply-template)Element.  
  
## <a name="datagrid-parts"></a>DataGrid-Teile  
 In der folgenden Tabelle sind die benannten Teile für das-Steuerelement aufgeführt <xref:System.Windows.Controls.DataGrid> .  
  
|Teil|type|BESCHREIBUNG|  
|-|-|-|  
|PART_ColumnHeadersPresenter|<xref:System.Windows.Controls.Primitives.DataGridColumnHeadersPresenter>|Die Zeile, die die Spaltenheader enthält.|  
  
 Wenn Sie einen <xref:System.Windows.Controls.ControlTemplate> für eine erstellen <xref:System.Windows.Controls.DataGrid> , enthält die Vorlage möglicherweise eine <xref:System.Windows.Controls.ItemsPresenter> innerhalb eines <xref:System.Windows.Controls.ScrollViewer> . (Die <xref:System.Windows.Controls.ItemsPresenter> zeigt jedes Element in der an <xref:System.Windows.Controls.DataGrid> ; das <xref:System.Windows.Controls.ScrollViewer> ermöglicht das Scrollen im-Steuerelement).  Wenn das <xref:System.Windows.Controls.ItemsPresenter> nicht das direkt untergeordnete Element von ist <xref:System.Windows.Controls.ScrollViewer> , müssen Sie den <xref:System.Windows.Controls.ItemsPresenter> Namen, `ItemsPresenter` .  
  
 Die Standardvorlage für das- <xref:System.Windows.Controls.DataGrid> Steuerelement enthält ein- <xref:System.Windows.Controls.ScrollViewer> Steuerelement. Weitere Informationen zu den Teilen, die von definiert <xref:System.Windows.Controls.ScrollViewer> werden, finden Sie unter [ScrollViewer-Stile und-Vorlagen](scrollviewer-styles-and-templates.md).  
  
## <a name="datagrid-states"></a>DataGrid-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das-Steuerelement aufgelistet <xref:System.Windows.Controls.DataGrid> .  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Normal|CommonStates|Der Standardzustand|  
|Deaktiviert|CommonStates|Das Steuerelement ist deaktiviert.|  
|InvalidFocused|ValidationStates|Das Steuerelement ist nicht gültig und besitzt den Fokus.|  
|InvalidUnfocused|ValidationStates|Das Steuerelement ist nicht gültig und besitzt keinen Fokus.|  
|Gültig|ValidationStates|Das Steuerelement ist gültig.|  
  
## <a name="datagridcell-parts"></a>DataGridCell-Teile  
 Das- <xref:System.Windows.Controls.DataGridCell> Element verfügt über keine benannten Teile.  
  
## <a name="datagridcell-states"></a>DataGridCell-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das- <xref:System.Windows.Controls.DataGridCell> Element aufgelistet.  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Normal|CommonStates|Der Standardzustand|  
|MouseOver|CommonStates|Der Mauszeiger wird auf der Zelle positioniert.|  
|Focused|FocusStates|Die Zelle hat den Fokus.|  
|Ohne Fokus|FocusStates|Die Zelle hat keinen Fokus.|  
|Aktuell|Currentstates|Die Zelle ist die aktuelle Zelle.|  
|Regulär|Currentstates|Die Zelle ist nicht die aktuelle Zelle.|  
|Anzeige|Interaktionstates|Die Zelle befindet sich im Anzeigemodus.|  
|Bearbeiten|Interaktionstates|Die Zelle befindet sich im Bearbeitungsmodus.|  
|Ausgewählt|SelectionStates|Die Zelle ist ausgewählt.|  
|Nicht markiert|SelectionStates|Die Zelle ist nicht ausgewählt.|  
|InvalidFocused|ValidationStates|Die Zelle ist ungültig und hat den Fokus.|  
|InvalidUnfocused|ValidationStates|Die Zelle ist ungültig und besitzt keinen Fokus.|  
|Gültig|ValidationStates|Die Zelle ist gültig.|  
  
## <a name="datagridrow-parts"></a>DataGridRow-Teile  
 Das- <xref:System.Windows.Controls.DataGridRow> Element verfügt über keine benannten Teile.  
  
## <a name="datagridrow-states"></a>DataGridRow-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das- <xref:System.Windows.Controls.DataGridRow> Element aufgelistet.  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Normal|CommonStates|Der Standardzustand|  
|MouseOver|CommonStates|Der Mauszeiger befindet sich über der Zeile.|  
|MouseOver_Editing|CommonStates|Der Mauszeiger befindet sich über der Zeile, und die Zeile befindet sich im Bearbeitungsmodus.|  
|MouseOver_Selected|CommonStates|Der Mauszeiger befindet sich über der Zeile, und die Zeile wird ausgewählt.|  
|MouseOver_Unfocused_Editing|CommonStates|Der Mauszeiger befindet sich über der Zeile, die Zeile befindet sich im Bearbeitungsmodus und hat keinen Fokus.|  
|MouseOver_Unfocused_Selected|CommonStates|Der Mauszeiger befindet sich über der Zeile, die Zeile ist ausgewählt und hat keinen Fokus.|  
|Normal_AlternatingRow|CommonStates|Die Zeile ist eine abwechselnde Zeile.|  
|Normal_Editing|CommonStates|Die Zeile befindet sich im Bearbeitungsmodus.|  
|Normal_Selected|CommonStates|Die Zeile ist ausgewählt.|  
|Unfocused_Editing|CommonStates|Die Zeile befindet sich im Bearbeitungsmodus und besitzt keinen Fokus.|  
|Unfocused_Selected|CommonStates|Die Zeile ist ausgewählt und besitzt keinen Fokus.|  
|InvalidFocused|ValidationStates|Das Steuerelement ist nicht gültig und besitzt den Fokus.|  
|InvalidUnfocused|ValidationStates|Das Steuerelement ist nicht gültig und besitzt keinen Fokus.|  
|Gültig|ValidationStates|Das Steuerelement ist gültig.|  
  
## <a name="datagridrowheader-parts"></a>DataGridRowHeader-Teile  
 In der folgenden Tabelle sind die benannten Teile für das- <xref:System.Windows.Controls.Primitives.DataGridRowHeader> Element aufgeführt.  
  
|Teil|type|BESCHREIBUNG|  
|-|-|-|  
|PART_TopHeaderGripper|<xref:System.Windows.Controls.Primitives.Thumb>|Das Element, das verwendet wird, um die Größe des Zeilen Headers vom oberen Rand zu ändern.|  
|PART_BottomHeaderGripper|<xref:System.Windows.Controls.Primitives.Thumb>|Das Element, das verwendet wird, um die Größe des Zeilen Headers von unten zu ändern.|  
  
## <a name="datagridrowheader-states"></a>DataGridRowHeader-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das- <xref:System.Windows.Controls.Primitives.DataGridRowHeader> Element aufgelistet.  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Normal|CommonStates|Der Standardzustand|  
|MouseOver|CommonStates|Der Mauszeiger befindet sich über der Zeile.|  
|MouseOver_CurrentRow|CommonStates|Der Mauszeiger befindet sich über der Zeile, und die Zeile ist die aktuelle Zeile.|  
|MouseOver_CurrentRow_Selected|CommonStates|Der Mauszeiger befindet sich über der Zeile, und die Zeile ist aktuell und ausgewählt.|  
|MouseOver_EditingRow|CommonStates|Der Mauszeiger befindet sich über der Zeile, und die Zeile befindet sich im Bearbeitungsmodus.|  
|MouseOver_Selected|CommonStates|Der Mauszeiger befindet sich über der Zeile, und die Zeile wird ausgewählt.|  
|MouseOver_Unfocused_CurrentRow_Selected|CommonStates|Der Mauszeiger befindet sich über der Zeile, die Zeile ist aktuell und ist ausgewählt und besitzt keinen Fokus.|  
|MouseOver_Unfocused_EditingRow|CommonStates|Der Mauszeiger befindet sich über der Zeile, die Zeile befindet sich im Bearbeitungsmodus und hat keinen Fokus.|  
|MouseOver_Unfocused_Selected|CommonStates|Der Mauszeiger befindet sich über der Zeile, die Zeile ist ausgewählt und hat keinen Fokus.|  
|Normal_CurrentRow|CommonStates|Die Zeile ist die aktuelle Zeile.|  
|Normal_CurrentRow_Selected|CommonStates|Die Zeile ist die aktuelle Zeile und wird ausgewählt.|  
|Normal_EditingRow|CommonStates|Die Zeile befindet sich im Bearbeitungsmodus.|  
|Normal_Selected|CommonStates|Die Zeile ist ausgewählt.|  
|Unfocused_CurrentRow_Selected|CommonStates|Die Zeile ist die aktuelle Zeile, ist ausgewählt und besitzt keinen Fokus.|  
|Unfocused_EditingRow|CommonStates|Die Zeile befindet sich im Bearbeitungsmodus und besitzt keinen Fokus.|  
|Unfocused_Selected|CommonStates|Die Zeile ist ausgewählt und besitzt keinen Fokus.|  
|InvalidFocused|ValidationStates|Das Steuerelement ist nicht gültig und besitzt den Fokus.|  
|InvalidUnfocused|ValidationStates|Das Steuerelement ist nicht gültig und besitzt keinen Fokus.|  
|Gültig|ValidationStates|Das Steuerelement ist gültig.|  
  
## <a name="datagridcolumnheaderspresenter-parts"></a>Datagridcolumnheaderationsenter-Teile  
 In der folgenden Tabelle sind die benannten Teile für das- <xref:System.Windows.Controls.Primitives.DataGridColumnHeadersPresenter> Element aufgeführt.  
  
|Teil|type|BESCHREIBUNG|  
|-|-|-|  
|PART_FillerColumnHeader|<xref:System.Windows.Controls.Primitives.DataGridColumnHeader>|Der Platzhalter für Spaltenüberschriften.|  
  
## <a name="datagridcolumnheaderspresenter-states"></a>Datagridcolumnheaderationsenter-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das- <xref:System.Windows.Controls.Primitives.DataGridColumnHeadersPresenter> Element aufgelistet.  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|InvalidFocused|ValidationStates|Die Zelle ist ungültig und hat den Fokus.|  
|InvalidUnfocused|ValidationStates|Die Zelle ist ungültig und besitzt keinen Fokus.|  
|Gültig|ValidationStates|Die Zelle ist gültig.|  
  
## <a name="datagridcolumnheader-parts"></a>DataGridColumnHeader-Teile  
 In der folgenden Tabelle sind die benannten Teile für das- <xref:System.Windows.Controls.Primitives.DataGridColumnHeader> Element aufgeführt.  
  
|Teil|type|BESCHREIBUNG|  
|-|-|-|  
|PART_LeftHeaderGripper|<xref:System.Windows.Controls.Primitives.Thumb>|Das Element, das verwendet wird, um die Größe des Spalten Headers von Links zu ändern.|  
|PART_RightHeaderGripper|<xref:System.Windows.Controls.Primitives.Thumb>|Das Element, das verwendet wird, um die Größe des Spalten Headers von rechts zu ändern.|  
  
## <a name="datagridcolumnheader-states"></a>DataGridColumnHeader-Zustände  
 In der folgenden Tabelle werden die visuellen Zustände für das- <xref:System.Windows.Controls.Primitives.DataGridColumnHeader> Element aufgelistet.  
  
|VisualState-Name|VisualStateGroup-Name|Beschreibung|  
|-|-|-|  
|Normal|CommonStates|Der Standardzustand|  
|MouseOver|CommonStates|Der Mauszeiger ist über dem Steuerelement positioniert.|  
|Gedrückt|CommonStates|Das Steuerelement wird gedrückt.|  
|SortAscending|Sortstates|Die Spalte wird in aufsteigender Reihenfolge sortiert.|  
|Sortsteigend|Sortstates|Die Spalte wird in absteigender Reihenfolge sortiert.|  
|Nicht sortiert|Sortstates|Die Spalte ist nicht sortiert.|  
|InvalidFocused|ValidationStates|Das Steuerelement ist nicht gültig und besitzt den Fokus.|  
|InvalidUnfocused|ValidationStates|Das Steuerelement ist nicht gültig und besitzt keinen Fokus.|  
|Gültig|ValidationStates|Das Steuerelement ist gültig.|  
  
## <a name="datagrid-controltemplate-example"></a>DataGrid ControlTemplate-Beispiel  
 Im folgenden Beispiel wird gezeigt, wie ein <xref:System.Windows.Controls.ControlTemplate> für das <xref:System.Windows.Controls.DataGrid> -Steuerelement und die zugehörigen Typen definiert werden.  
  
 [!code-xaml[ControlTemplateExamples#DataGrid](~/samples/snippets/csharp/VS_Snippets_Wpf/ControlTemplateExamples/CS/resources/datagrid.xaml#datagrid)]  
  
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
