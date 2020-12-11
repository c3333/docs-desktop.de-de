---
title: Verbesserungen beim Windows Forms
description: Erfahren Sie mehr über die Möglichkeiten, mit denen .net Core Windows Forms versucht, die Barrierefreiheit im Vergleich mit .NET Framework Windows Forms zu verbessern.
ms.date: 04/20/2020
helpviewer_keywords:
- Windows Forms accessibility
- accessibility
author: M-Lipin
ms.openlocfilehash: 4dc477cebf35435ff2122ce21644135848985d07
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974712"
---
# <a name="accessibility-improvements-in-windows-forms-controls-for-net-core-30"></a>Verbesserungen der Barrierefreiheit in Windows Forms-Steuerelementen für .net Core 3,0

Windows Forms wird die Funktionsweise mit Barrierefreiheits Technologien weiter verbessern, um Windows Forms Kunden besser zu unterstützen. Diese Verbesserungen umfassen folgende Änderungen:

- Änderungen in verschiedenen Bereichen der Interaktion mit Client Anwendungen für die Barrierefreiheit, einschließlich Sprachausgabe.
- Änderungen an der Hierarchie der Barrierefreiheit (Verbesserung der Navigation durch die Benutzeroberflächenautomatisierungsstruktur)
- Änderungen in der Tastaturnavigation.

> [!IMPORTANT]
> Barrierefreiheits Änderungen, die in .NET Framework 4.7.1 durch .NET Framework 4,8 vorgenommen werden, sind in .net Core 3,0 und höher enthalten und sind standardmäßig aktiviert. Der .NET Framework unterstützte Kompatibilitäts Switches, mit denen Anwendungen das neue Barrierefreiheits Verhalten ablehnen konnten. Auf der anderen Seite unterstützt .net Core diese Einstellungen nicht und ermöglicht Anwendungen nicht, das Barrierefreiheits Verhalten zu entscheiden.
  
Ab .net Core 3,0 profitieren Windows Forms Anwendungen von allen neuen Barrierefreiheits Features (eingeführt in .NET Framework 4.7.1-4,8) ohne zusätzliche Konfiguration.

## <a name="listbox-accessibility-support"></a>Unterstützung für ListBox-Barrierefreiheit

Die folgenden Änderungen gelten für das- <xref:System.Windows.Forms.ListBox> Steuerelement:

- Aktivierte Benutzeroberflächenautomatisierungs-Unterstützung für `ListBox` Steuerung.
- Verbesserte `ListBox` Barrierefreiheits Unterstützung durch Hinzufügen der <xref:System.Windows.Automation.ScrollItemPattern> zu `ListBox` Elementen und durch Erweiterung des Barrierefreiheits Ereignisses auslösen und behandeln und durchlaufen der Sprachnavigation durch die Elemente (die Lock-Lock-Navigation ist nicht korrekt und löst die Navigation nicht versehentlich außerhalb des Steuer Elements aus).

## <a name="checkedlistbox-accessibility-support"></a>Unterstützung von CheckedListBox-Barrierefreiheit

Die folgenden Änderungen gelten für das- <xref:System.Windows.Forms.CheckedListBox> Steuerelement:

- `CheckedListBox`Von den Barrierefreiheits Eigenschaften für Einträge bereitgestellte Begrenzungen wurden korrigiert.
- Verbesserte allgemeine `ListBox` und `CheckedListBox` Barrierefreiheit: korrigierte Eigenschaftswerte und Ereignis Modell.

## <a name="combobox-accessibility-support"></a>Unterstützung der ComboBox-Barrierefreiheit

Die folgenden Änderungen gelten für das- <xref:System.Windows.Forms.ComboBox> Steuerelement:

- Der Prozess zum erhalten von `ComboBox` Objekten für die Barrierefreiheit von Elementen wurde aktualisiert, um das Erstellen von IDs für Elemente zu ermöglichen, anstatt Hashcodes von Elementen abzurufen. Dies ist möglicherweise unsicher, wenn die <xref:System.Object.GetHashCode%2A> Funktion überschrieben wird.

## <a name="datagridview-accessibility-support"></a>Unterstützung der DataGridView-Barrierefreiheit

Die folgenden Änderungen gelten für das- <xref:System.Windows.Forms.DataGridView> Steuerelement:

- Korrigiert `DataGridView.Bounds` durch Barrierefreiheits Eigenschaften für Spalten, Zeilen, Zellen und entsprechende Header, verbesserte Leistung bei der Berechnung des umgebenden Rechtecks. Alle Barrierefreiheits Grenzen werden korrekt dargestellt, wobei die Grenzen des gesamten Steuer Elements zusammen mit dem Viewport berücksichtigt werden.
- Der `Value.IsReadOnly` Eigenschafts Wert wurde korrigiert und bietet barrierefreie Client Anwendungen. Die-Eigenschaft zeigt nun den korrekten `IsReadOnly` Status für Zellen an.
- Das Problem mit <xref:System.Windows.Forms.DataGridView.CellParsing> der Ereignis Erhöhung für die erste Zellen Änderung wurde behoben. Der Zellwert kann ohne Probleme geändert werden, einschließlich der ersten `DataGridView` Interaktion des Steuer Elements.
- Verbesserter `DataGridView` Hintergrund Farbkontrast bei der Verwendung von Windows-hoher Kontrast Designs. Geänderte `DataGridView` Standard Hintergrundfarbe bei Verwendung von "HC # 1", "HC # 2" und "HC Black Theme".

## <a name="propertygrid-accessibility-support"></a>PropertyGrid-Barrierefreiheits Unterstützung

Die folgenden Änderungen gelten für das- <xref:System.Windows.Forms.PropertyGrid> Steuerelement:

- Korrigiert `PropertyGrid.Bounds` durch Barrierefreiheits Eigenschaften für Raster Einträge, verbesserte Leistung bei der Berechnung von umschließenden Rechtecks. Vorerst werden alle Barrierefreiheits Begrenzungen korrekt dargestellt, wobei die Grenzen des gesamten Steuer Elements zusammen mit dem Viewport berücksichtigt werden.
- Es wurden barrierefreie Namen und Beschreibungen von untergeordneten Steuerelementen korrigiert, sodass Sie keine Steuer Elementtyp Namen enthalten und keine doppelte Ankündigung für Steuer Elementtyp Namen zu vermeiden.

## <a name="toolstrip-accessibility-support"></a>ToolStrip-Barrierefreiheits Unterstützung

Die folgenden Änderungen gelten für das- <xref:System.Windows.Forms.ToolStrip> Steuerelement:

- Verbesserte Navigation durch `ToolStrip` die `MenuStrip` Elemente, und `StatusStrip` . Korrigiert `ToolStrip` und `MenuStrip` Shift-Tab-Navigation, zurück Schleife der Menü Elemente, wenn UMSCHALT-TAB-nach-oben-Taste gedrückt wird, die zum unteren Menü Element navigiert.
- Verbesserte `MenuStrip` barrierefreie Navigation, korrigierte Menü-Steuerelement Typen für Untermenüs, um Untermenüs vom Typ "Menu" anstelle von "MENUITEM" zu erstellen.

## <a name="printpreviewcontrol-and-printpreviewdialog-accessibility-support"></a>Hilfe zur Barrierefreiheit von PrintPreviewControl und PrintPreviewDialog

Die folgenden Änderungen gelten für die Druck Steuerelemente:

- Verbesserte barrierefreie Navigation (einschließlich Sprachnavigation) über Menü Elemente.
- Verbesserte Unterstützung von hoher Kontrast Designs und eine bessere Gegenüberstellung des Steuerelement Elements.

## <a name="stringcollectioneditor-accessibility-support"></a>Unterstützung der stringcollectioneditor-Barrierefreiheit

Windows Forms-Designer verwendet nun den Zeichen folgen Auflistungs-Editor mit verbesserter Barrierefreiheits Unterstützung.

## <a name="monthcalendar-accessibility-support-available-in-net-core-31"></a>Unterstützung für MonthCalendar-Barrierefreiheit (in .net Core 3,1 verfügbar)

Die folgenden Änderungen gelten für das- <xref:System.Windows.Forms.MonthCalendar> Steuerelement:

- Benutzeroberflächenautomatisierungs-Server Anbieter zum `MonthCalendar` Steuern von, hinzugefügten Benutzeroberflächenautomatisierungs-Raster Mustern und Tabellen Muster Anbietern
- Der Zugriff auf den für die _Tabelle_ zugänglichen Steuerungstyp wurde in den von _Calendar_ zugänglichen Steuerungstyp geändert, `MonthCalendar` außer wenn das Steuerelement über ein vorangestelltes Label-Steuerelement verfügt, das den `MonthCalendar` zugänglichen Namen des Steuer Elements definiert. 
- Verbesserte Ankündigung des ausgewählten Datums für die `MonthCalendar` Steuerung.
- Verbesserte `MonthCalendar` Steuerungs Unterstützung für Sprachausgaben und andere Barrierefreiheits Tools. Zu diesem Zeitpunkt können Benutzer durch die Steuerelemente navigieren und mithilfe der reinen Tastatureingabe mit diesen Elementen interagieren. Verwenden Sie bei der Sprachausgabe die Tasten "Caps + Pfeil", um die Steuerelemente zu durchlaufen, und drücken Sie "Caps + Eingabe", um die
- Verbesserte Pfeiltasten Navigation zwischen `MonthCalendar` untergeordneten Elementen und einem Fokus Rechteck: blaues Fokus Rechteck für die Sprachausgabe.
- Verbesserter Zugriff auf die Treffer Test Aktion für `MonthCalendar` Steuerelemente, um das untergeordnete `MonthCalendar` barrierefreie Element durch bereitgestellte Koordinaten zu erhalten.

## <a name="tooltips-accessibility-available-in-net-core-31"></a>Tooltips-Barrierefreiheit (in .net Core 3,1 verfügbar)

- Die Möglichkeit, QuickInfo-Text von Sprachausgabe Anwendungen wie NVDA und Sprachausgabe anzukündigen, wurde hinzugefügt. Die Sprachausgabe Anwendung kann nun den Text der Tastatur-oder Maus-QuickInfo für beliebige Windows Forms Steuerelemente ankündigen, die für die Anzeige von Quick Infos konfiguriert sind.

## <a name="ui-automation-support-for-datagridview-propertygrid-listbox-combobox-toolstrip-and-other-controls"></a>Benutzeroberflächenautomatisierungs-Unterstützung für DataGridView, PropertyGrid, ListBox, ComboBox, ToolStrip und andere Steuerelemente

Die Unterstützung der Benutzeroberflächen Automatisierung ist für Steuerelemente zur Laufzeit aktiviert, wird aber während der Entwurfszeit nicht verwendet Einen Überblick über die Benutzeroberflächenautomatisierung finden Sie unter [Benutzeroberflächenautomatisierung: Übersicht](/dotnet/framework/ui-automation/ui-automation-overview).

## <a name="see-also"></a>Siehe auch

- [Bewährte Methoden](/dotnet/framework/ui-automation/accessibility-best-practices)für die Barrierefreiheit.
