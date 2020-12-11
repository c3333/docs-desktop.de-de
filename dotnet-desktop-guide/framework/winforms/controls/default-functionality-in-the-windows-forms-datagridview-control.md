---
title: Standardfunktionen im DataGridView-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- data grids [Windows Forms], default functionality in DataGridView control
- DataGridView control [Windows Forms], default functionality
ms.assetid: 4405f697-cad1-4839-9bcd-8ddb09d9f00e
ms.openlocfilehash: b695883ac7ec3fb0c459adb66214b0eceab3a128
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972156"
---
# <a name="default-functionality-in-the-windows-forms-datagridview-control"></a>Standardfunktionalität des DataGridView-Steuerelements von Windows Forms
Das Windows Forms- <xref:System.Windows.Forms.DataGridView> Steuerelement bietet Benutzern eine beträchtliche Menge an Standardfunktionen.  
  
## <a name="default-functionality"></a>Standardfunktionalität  
 Standardmäßig ist ein- <xref:System.Windows.Forms.DataGridView> Steuerelement:  
  
- Zeigt automatisch Spaltenkopfzeilen und Zeilen Header an, die sichtbar bleiben, wenn die Tabelle vertikal scrollt.  
  
- Verfügt über einen Zeilen Header, der einen Auswahl Indikator für die aktuelle Zeile enthält.  
  
- Hat ein Auswahl Rechteck in der ersten Zelle.  
  
- Enthält Spalten, deren Größe automatisch geändert werden kann, wenn der Benutzer auf die Spalten unter Teiler doppelklickt.  
  
- Unterstützt automatisch visuelle Stile unter Windows XP und der Windows Server 2003-Produktfamilie, wenn die <xref:System.Windows.Forms.Application.EnableVisualStyles%2A> -Methode von der-Methode der Anwendung aufgerufen wird `Main` .  
  
 Außerdem kann der Inhalt eines <xref:System.Windows.Forms.DataGridView> Steuer Elements standardmäßig bearbeitet werden:  
  
- Wenn der Benutzer auf F2 in einer Zelle doppelklickt oder diese drückt, versetzt das Steuerelement die Zelle automatisch in den Bearbeitungsmodus und aktualisiert den Inhalt der Zelle als Benutzer.  
  
- Wenn der Benutzer einen Bildlauf zum Ende des Rasters durchführt, wird dem Benutzer angezeigt, dass eine Zeile zum Hinzufügen neuer Datensätze vorhanden ist. Wenn der Benutzer auf diese Zeile klickt, wird dem Steuerelement eine neue Zeile <xref:System.Windows.Forms.DataGridView> mit Standardwerten hinzugefügt. Wenn der Benutzer ESC drückt, verschwindet diese neue Zeile.  
  
- Wenn der Benutzer auf einen Zeilen Header klickt, wird die gesamte Zeile ausgewählt.  
  
 Wenn Sie ein <xref:System.Windows.Forms.DataGridView> Steuerelement durch Festlegen der-Eigenschaft an eine Datenquelle binden <xref:System.Windows.Forms.DataGridView.DataSource%2A> , wird das-Steuerelement:  
  
- Verwendet automatisch die Namen der Datenquellen Spalten als Spaltenheader Text.  
  
- Wird mit dem Inhalt der Datenquelle aufgefüllt. <xref:System.Windows.Forms.DataGridView> Spalten werden für jede Spalte in der Datenquelle automatisch erstellt.  
  
- Erstellt eine Zeile für jede sichtbare Zeile in der Tabelle.  
  
- Sortiert die Zeilen automatisch basierend auf den zugrunde liegenden Daten, wenn der Benutzer auf einen Spaltenheader klickt.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.DataGridView>
- [DataGridView-Steuerelement](datagridview-control-windows-forms.md)
