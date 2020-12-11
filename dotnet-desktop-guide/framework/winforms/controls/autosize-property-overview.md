---
title: Übersicht über die AutoSize-Eigenschaft
ms.date: 03/30/2017
helpviewer_keywords:
- sizing [Windows Forms], automatic
- layout [Windows Forms], AutoSize
- automatic sizing
- AutoSizeMode property
ms.assetid: 62fd82a2-9565-4f65-925b-9d1e66dc4e7d
ms.openlocfilehash: eb87616c2ddcf9a4ab62245d365763ee57ffb964
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975147"
---
# <a name="autosize-property-overview"></a>Übersicht über die AutoSize-Eigenschaft
Die- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft ermöglicht es einem Steuerelement, seine Größe ggf. zu ändern, um den von der-Eigenschaft angegebenen Wert zu erreichen <xref:System.Windows.Forms.Control.PreferredSize%2A> . Sie passen das Größen Anpassungs Verhalten für bestimmte Steuerelemente an, indem Sie die- `AutoSizeMode` Eigenschaft festlegen.

## <a name="autosize-behavior"></a>AutoSize-Verhalten
 Nur einige Steuerelemente unterstützen die- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft. Darüber hinaus unterstützen einige Steuerelemente, die die-Eigenschaft unterstützen, <xref:System.Windows.Forms.Control.AutoSize%2A> auch die- `AutoSizeMode` Eigenschaft.

 Die- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft erzeugt ein etwas anderes Verhalten, abhängig vom jeweiligen Steuerelement-Typ und dem Wert der- `AutoSizeMode` Eigenschaft, wenn die-Eigenschaft vorhanden ist. In der folgenden Tabelle werden die Verhaltensweisen beschrieben, die immer zutreffen und eine kurze Beschreibung enthalten:

|Always true-Verhalten|BESCHREIBUNG|
|--------------------------|-----------------|
|Die automatische Größenanpassung ist eine Lauf Zeitfunktion.|Dies bedeutet, dass ein Steuerelement niemals vergrößert oder verkleinert wird, sodass es keine weiteren Auswirkungen hat.|
|Wenn die Größe eines Steuer Elements geändert wird, bleibt der Wert seiner <xref:System.Windows.Forms.Control.Location%2A> Eigenschaft immer konstant.|Wenn der Inhalt eines Steuer Elements vergrößert wird, wächst das Steuerelement nach rechts und unten. Steuerelemente werden nicht nach links vergrößert.|
|Die <xref:System.Windows.Forms.Control.Dock%2A> <xref:System.Windows.Forms.Control.Anchor%2A> Eigenschaften und werden berücksichtigt, wenn den Wert hat <xref:System.Windows.Forms.Control.AutoSize%2A> `true` .|Der Wert der-Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.Location%2A> wird an den korrekten Wert angepasst.<br /><br /> **Hinweis** Das- <xref:System.Windows.Forms.Label> Steuerelement ist eine Ausnahme von dieser Regel. Wenn Sie den Wert der-Eigenschaft eines angedockten <xref:System.Windows.Forms.Label> Steuer Elements <xref:System.Windows.Forms.Control.AutoSize%2A> auf festlegen `true` , wird das- <xref:System.Windows.Forms.Label> Steuerelement nicht gestreckt.|
|Die-Eigenschaft und die-Eigenschaft des-Steuer Elements <xref:System.Windows.Forms.Control.MaximumSize%2A> <xref:System.Windows.Forms.Control.MinimumSize%2A> werden immer berücksichtigt, unabhängig vom Wert der- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft.|Die <xref:System.Windows.Forms.Control.MaximumSize%2A> -Eigenschaft und die- <xref:System.Windows.Forms.Control.MinimumSize%2A> Eigenschaft werden von der-Eigenschaft nicht beeinträchtigt <xref:System.Windows.Forms.Control.AutoSize%2A> .|
|Standardmäßig ist keine Mindestgröße festgelegt.|Dies bedeutet, dass, wenn ein Steuerelement so festgelegt ist, dass es sich unter befindet <xref:System.Windows.Forms.Control.AutoSize%2A> und keinen Inhalt hat, der Wert seiner- <xref:System.Windows.Forms.Control.Size%2A> Eigenschaft 0, 0 ist. In diesem Fall wird das Steuerelement zu einem Punkt verkleinert und ist nicht sofort sichtbar.|
|Wenn ein Steuerelement die Methode nicht implementiert <xref:System.Windows.Forms.Control.GetPreferredSize%2A> , <xref:System.Windows.Forms.Control.GetPreferredSize%2A> gibt die Methode den letzten Wert zurück, der der Eigenschaft zugewiesen ist <xref:System.Windows.Forms.Control.Size%2A> .|Dies bedeutet, dass das Festlegen <xref:System.Windows.Forms.Control.AutoSize%2A> von auf `true` keine Auswirkung hat.|
|Ein Steuerelement in einer <xref:System.Windows.Forms.TableLayoutPanel> Zelle verkleinert sich immer so, dass es in die Zelle passt, bis Ihr <xref:System.Windows.Forms.Control.MinimumSize%2A> erreicht ist.|Diese Größe wird als maximale Größe erzwungen. Dies ist nicht der Fall, wenn die Zelle Teil einer <xref:System.Windows.Forms.SizeType.AutoSize> Zeile oder Spalte ist.|

## <a name="autosizemode-property"></a>AutoSizeMode-Eigenschaft
 Die `AutoSizeMode` -Eigenschaft bietet eine präzisere Kontrolle über das Standard <xref:System.Windows.Forms.Control.AutoSize%2A> Verhalten. Die- `AutoSizeMode` Eigenschaft gibt an, wie sich ein Steuerelement auf seinen Inhalt selbst Größen festlegt. Der Inhalt kann z. b. der Text für ein <xref:System.Windows.Forms.Button> Steuerelement oder die untergeordneten Steuerelemente für einen Container sein.

 In der folgenden Tabelle werden die <xref:System.Windows.Forms.AutoSizeMode> Einstellungen und die Beschreibung des Verhaltens der einzelnen Einstellungen aufgeführt.

|AutoSizeMode-Einstellung|Verhalten|
|--------------------------|--------------|
|GrowAndShrink|Das-Steuerelement wächst oder verkleinert, um seinen Inhalt zu umfassen.<br /><br /> Der <xref:System.Windows.Forms.Control.MinimumSize%2A> -Wert und der- <xref:System.Windows.Forms.Control.MaximumSize%2A> Wert werden berücksichtigt, aber der aktuelle Wert der- <xref:System.Windows.Forms.Control.Size%2A> Eigenschaft wird ignoriert.<br /><br /> Dies entspricht dem Verhalten der Steuerelemente mit der <xref:System.Windows.Forms.Control.AutoSize%2A> -Eigenschaft und der-Eigenschaft `AutoSizeMode` .|
|Groweinzierl|Das-Steuerelement wächst so stark, dass es seinen Inhalt umfasst, es wird jedoch nicht kleiner als der Wert, der durch die-Eigenschaft angegeben wird <xref:System.Windows.Forms.Control.Size%2A> .<br /><br /> Dies ist der Standardwert für `AutoSizeMode`.|

## <a name="controls-that-support-the-autosize-property"></a>Steuerelemente, die die AutoSize-Eigenschaft unterstützen
 In der folgenden Tabelle sind die Steuerelemente aufgelistet, die die <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaften und unterstützen `AutoSizeMode` .

|AutoSize-Unterstützung|Steuerelementtyp|
|----------------------|------------------|
|-   <xref:System.Windows.Forms.Control.AutoSize%2A> unterstützte Eigenschaft.<br />-Keine `AutoSizeMode` Eigenschaft.|<xref:System.Windows.Forms.CheckBox><br /><br /> <xref:System.Windows.Forms.DomainUpDown><br /><br /> <xref:System.Windows.Forms.Label><br /><br /> <xref:System.Windows.Forms.LinkLabel><br /><br /> <xref:System.Windows.Forms.MaskedTextBox> ( <xref:System.Windows.Forms.TextBox> Basis)<br /><br /> <xref:System.Windows.Forms.NumericUpDown><br /><br /> <xref:System.Windows.Forms.RadioButton><br /><br /> <xref:System.Windows.Forms.TextBox><br /><br /> <xref:System.Windows.Forms.TrackBar>|
|-   <xref:System.Windows.Forms.Control.AutoSize%2A> unterstützte Eigenschaft.<br />-   `AutoSizeMode` unterstützte Eigenschaft.|<xref:System.Windows.Forms.Button><br /><br /> <xref:System.Windows.Forms.CheckedListBox><br /><br /> <xref:System.Windows.Forms.FlowLayoutPanel><br /><br /> <xref:System.Windows.Forms.Form><br /><br /> <xref:System.Windows.Forms.GroupBox><br /><br /> <xref:System.Windows.Forms.Panel><br /><br /> <xref:System.Windows.Forms.TableLayoutPanel>|
|-Keine <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft.|<xref:System.Windows.Forms.CheckedListBox><br /><br /> <xref:System.Windows.Forms.ComboBox><br /><br /> <xref:System.Windows.Forms.DataGridView><br /><br /> <xref:System.Windows.Forms.DateTimePicker><br /><br /> <xref:System.Windows.Forms.ListBox><br /><br /> <xref:System.Windows.Forms.ListView><br /><br /> <xref:System.Windows.Forms.MaskedTextBox><br /><br /> <xref:System.Windows.Forms.MonthCalendar><br /><br /> <xref:System.Windows.Forms.ProgressBar><br /><br /> <xref:System.Windows.Forms.PropertyGrid><br /><br /> <xref:System.Windows.Forms.RichTextBox><br /><br /> <xref:System.Windows.Forms.SplitContainer><br /><br /> <xref:System.Windows.Forms.TabControl><br /><br /> <xref:System.Windows.Forms.TabPage><br /><br /> <xref:System.Windows.Forms.TreeView><br /><br /> <xref:System.Windows.Forms.WebBrowser><br /><br /> <xref:System.Windows.Forms.ScrollBar>|

## <a name="autosize-in-the-design-environment"></a>Automatische Größe in der Entwurfs Umgebung
 In der folgenden Tabelle wird das Größen Anpassungs Verhalten eines-Steuer Elements zur Entwurfszeit basierend auf dem Wert der-Eigenschaft und der-Eigenschaft beschrieben <xref:System.Windows.Forms.Control.AutoSize%2A> `AutoSizeMode` .

 Überschreiben <xref:System.Windows.Forms.Design.ControlDesigner.SelectionRules%2A> Sie die-Eigenschaft, um zu bestimmen, ob ein bestimmtes Steuerelement den Status "Benutzer in Größe" aufweist. In der folgenden Tabelle bedeutet "kann nicht" <xref:System.Windows.Forms.Design.SelectionRules.Moveable> nur, "kann" <xref:System.Windows.Forms.Design.SelectionRules.AllSizeable> und <xref:System.Windows.Forms.Design.SelectionRules.Moveable> .

|AutoSize-Einstellungen|Entwurfszeit-Anpassungs Bewegung|
|-----------------------|---------------------------------|
|-   <xref:System.Windows.Forms.Control.AutoSize%2A> = `true`<br />-Keine `AutoSizeMode` Eigenschaft.|Der Benutzer kann die Größe des Steuer Elements zur Entwurfszeit nicht ändern, mit Ausnahme der folgenden Steuerelemente:<br /><br /> -   <xref:System.Windows.Forms.TextBox><br />-   <xref:System.Windows.Forms.MaskedTextBox><br />-   <xref:System.Windows.Forms.RichTextBox><br />-   <xref:System.Windows.Forms.TrackBar>|
|-   <xref:System.Windows.Forms.Control.AutoSize%2A> = `true`<br />-   `AutoSizeMode` = <xref:System.Windows.Forms.AutoSizeMode.GrowAndShrink>|Der Benutzer kann die Größe des Steuer Elements zur Entwurfszeit nicht ändern.|
|-   <xref:System.Windows.Forms.Control.AutoSize%2A> = `true`<br />-   `AutoSizeMode` = <xref:System.Windows.Forms.AutoSizeMode.GrowOnly>|Der Benutzer kann die Größe des Steuer Elements zur Entwurfszeit ändern. Wenn die- <xref:System.Windows.Forms.Control.Size%2A> Eigenschaft festgelegt ist, kann der Benutzer die Größe des Steuer Elements nur vergrößern.|
|-   <xref:System.Windows.Forms.Control.AutoSize%2A> = `false`die-Eigenschaft oder die- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft ist ausgeblendet.|Der Benutzer kann die Größe des Steuer Elements zur Entwurfszeit ändern.|

> [!NOTE]
> Um die Produktivität zu maximieren, Shadowing der Windows Forms-Designer in Visual Studio die- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft für die- <xref:System.Windows.Forms.Form> Klasse. Zur Entwurfszeit verhält sich das Formular so, als ob die- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft auf festgelegt ist `false` , unabhängig von der eigentlichen-Einstellung. Zur Laufzeit werden keine besonderen unterrichten hergestellt, und die- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft wird gemäß der-Eigenschafts Einstellung angewendet.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Control.AutoSize%2A>
- <xref:System.Windows.Forms.Control.PreferredSize%2A>
- <xref:System.Windows.Forms.Control.GetPreferredSize%2A>
