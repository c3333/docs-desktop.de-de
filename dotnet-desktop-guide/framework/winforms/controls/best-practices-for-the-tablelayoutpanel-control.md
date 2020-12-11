---
title: Empfohlene Vorgehensweisen für das TableLayoutPanel-Steuerelement
ms.date: 03/30/2017
helpviewer_keywords:
- layout [Windows Forms]
- TableLayoutPanel control [Windows Forms], best practices
- forms [Windows Forms], best practices
- AutoSize property [Windows Forms], tableLayoutPanel control
- controls [Windows Forms], sizing
- TableLayoutPanel control [Windows Forms], AutoSize behavior
- layout [Windows Forms], AutoSize
- layout [Windows Forms], best practices
- best practices [Windows Forms], tableLayoutPanel control
- sizing [Windows Forms], automatic
- automatic sizing
ms.assetid: b6706efb-d7a4-45ec-8cf4-08fa993e3afb
ms.openlocfilehash: e46d0fe6913bec61bd56199b7cb56a9b24d15bd0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975787"
---
# <a name="best-practices-for-the-tablelayoutpanel-control"></a>Empfohlene Vorgehensweisen für das TableLayoutPanel-Steuerelement
Das- <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement bietet leistungsstarke Layoutfeatures, die Sie sorgfältig berücksichtigen sollten, bevor Sie Ihre Windows Forms verwenden.

## <a name="recommendations"></a>Empfehlungen
 Anhand der folgenden Empfehlungen können Sie das- <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement optimal nutzen.

### <a name="targeted-use"></a>Gezielte Verwendung
 Verwenden Sie das <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement sparsam. Diese sollten nicht in allen Situationen verwendet werden, in denen ein Layout in der Größe geändert werden muss. In der folgenden Liste werden Layouts beschrieben, die am meisten von der Verwendung des-Steuer Elements profitieren <xref:System.Windows.Forms.TableLayoutPanel> :

- Layouts, bei denen mehrere Teile des Formulars proportional zueinander angepasst werden.

- Layouts, die zur Laufzeit dynamisch geändert oder generiert werden, z. b. Dateneingabeformulare, die auf der Grundlage von Einstellungen Benutzer anpassbare Felder hinzugefügt oder subtrahiert werden.

- Layouts, die in einer Gesamtgröße bleiben sollen. Beispielsweise können Sie über ein Dialogfeld verfügen, das kleiner als 800 x 600 sein sollte, aber Sie müssen lokalisierte Zeichen folgen unterstützen.

 In der folgenden Liste werden Layouts beschrieben, die von der Verwendung des Steuer Elements nicht stark profitieren <xref:System.Windows.Forms.TableLayoutPanel> :

- Einfache Dateneingabeformulare mit einer einzelnen Spalte von Bezeichnungen und einer einzelnen Spalte mit Texteingabe Bereichen.

- Formulare mit einem einzelnen großen Anzeigebereich, der den gesamten verfügbaren Platz ausfüllen soll, wenn eine Größenänderung auftritt. Ein Beispiel hierfür ist ein Formular, das ein einzelnes Steuerelement anzeigt <xref:System.Windows.Forms.PropertyGrid> . Verwenden Sie in diesem Fall das verankern, da nichts anderes bei der Größenänderung des Formulars erweitert werden soll.

 Wählen Sie sorgfältig aus, welche Steuerelemente sich in einem Steuerelement befinden müssen <xref:System.Windows.Forms.TableLayoutPanel> . Wenn Sie mit dem verankern Platz für Ihren Text um 30% vergrößern können, sollten Sie die- <xref:System.Windows.Forms.Control.Anchor%2A> Eigenschaft nur verwenden. Wenn Sie den für das Layout benötigten Speicherplatz einschätzen können, <xref:System.Windows.Forms.Control.Dock%2A> ist die Verwendung von und <xref:System.Windows.Forms.Control.Anchor%2A> einfacher als das Schätzen der Details des verbleibenden Speicherplatzes und des verbleibenden <xref:System.Windows.Forms.Control.AutoSize%2A> Verhaltens.

 Im Allgemeinen sollten Sie beim Entwerfen des Layouts mit dem <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement den Entwurf so einfach wie möglich halten.

### <a name="use-the-document-outline-window"></a>Verwenden des Dokument Gliederungs Fensters
 Das Dokument Gliederungs Fenster bietet eine Strukturansicht Ihres Layouts, mit der Sie die z-Reihenfolge und die Beziehungen zwischen übergeordneten und untergeordneten Elementen der Steuerelemente bearbeiten können. Wählen Sie im **Menü Ansicht** die Option **Weitere Fenster**, und klicken Sie dann auf **Dokument** Gliederung.

### <a name="avoid-nesting"></a>Schachteln vermeiden
 Vermeiden Sie das Schachteln anderer <xref:System.Windows.Forms.TableLayoutPanel> Steuerelemente in einem <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement. Das Debuggen von schsted Layouts kann schwierig sein.

### <a name="avoid-visual-inheritance"></a>Vermeiden der visuellen Vererbung
 Das- <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement unterstützt keine visuelle Vererbung in der Windows Forms-Designer in Visual Studio. Ein <xref:System.Windows.Forms.TableLayoutPanel> Steuerelement in einer abgeleiteten Klasse wird zur Entwurfszeit als "gesperrt" angezeigt.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.TableLayoutPanel>
- <xref:System.Windows.Forms.FlowLayoutPanel>
