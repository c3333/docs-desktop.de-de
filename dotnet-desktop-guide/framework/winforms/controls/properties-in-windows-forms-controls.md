---
title: Eigenschaften von Steuerelementen
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], properties overview (using code)
- controls [Windows Forms], properties
- properties [Windows Forms]
ms.assetid: 2785279b-fb57-4937-8f6b-2050e475db6f
ms.openlocfilehash: 3f9873ff032497a9cda6de199ed9db5ee9522d81
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972340"
---
# <a name="properties-in-windows-forms-controls"></a>Eigenschaften von Windows Forms-Steuerelementen

Ein Windows Forms-Steuerelement erbt viele Eigenschaften aus der Basisklasse <xref:System.Windows.Forms.Control?displayProperty=nameWithType> . Hierzu gehören Eigenschaften wie <xref:System.Windows.Forms.Control.Font%2A> , <xref:System.Windows.Forms.Control.ForeColor%2A> , <xref:System.Windows.Forms.Control.BackColor%2A> , <xref:System.Windows.Forms.Control.Bounds%2A> , <xref:System.Windows.Forms.Control.ClientRectangle%2A> , <xref:System.Windows.Forms.Control.DisplayRectangle%2A> ,,, <xref:System.Windows.Forms.Control.Enabled%2A> <xref:System.Windows.Forms.Control.Focused%2A> <xref:System.Windows.Forms.Control.Height%2A> , <xref:System.Windows.Forms.Control.Width%2A> , <xref:System.Windows.Forms.Control.Visible%2A> , <xref:System.Windows.Forms.Control.AutoSize%2A> und viele andere. Ausführliche Informationen zu geerbten Eigenschaften finden Sie unter <xref:System.Windows.Forms.Control?displayProperty=nameWithType> .  
  
 Sie können geerbte Eigenschaften in Ihrem Steuerelement außer Kraft setzen oder neue Eigenschaften definieren.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  

 [Definieren einer Eigenschaft](defining-a-property-in-windows-forms-controls.md)  
 Demonstriert das Implementieren einer Eigenschaft für ein benutzerdefiniertes Steuerelement oder eine Komponente und das Integrieren der Eigenschaft in die Entwurfsumgebung.  
  
 [Definieren von Standardwerten mit der ShouldSerialize-Methode und der Reset-Methode](defining-default-values-with-the-shouldserialize-and-reset-methods.md)  
 Demonstriert das Definieren von Standardeigenschaftswerten für ein benutzerdefiniertes Steuerelement oder eine Komponente.  
  
 [Durch geänderte Eigenschaften ausgelöste Ereignisse](property-changed-events.md)  
 Beschreibt das Aktivieren von Benachrichtigungen über Eigenschaftsänderungen, wenn ein Eigenschaftswert geändert wird.  
  
 [Vorgehensweise: Verfügbarmachen der Eigenschaften konstituierender Steuerelemente](how-to-expose-properties-of-constituent-controls.md)  
 Veranschaulicht, wie man Eigenschaften von konstituierenden Steuerelementen in einem benutzerdefinierten zusammengesetzten Steuerelement verfügbar macht.  
  
 [Implementierung von Methoden in benutzerdefinierten Steuerelementen](method-implementation-in-custom-controls.md)  
 Beschreibt die Implementierung von Methoden in benutzerdefinierten Steuerelementen und Komponenten.  
  
## <a name="reference"></a>Verweis  

 <xref:System.Windows.Forms.UserControl>  
 Dokumentiert die Basisklasse für das Implementieren von zusammengesetzten Steuerelementen.  
  
 <xref:System.ComponentModel.TypeConverterAttribute>  
 Dokumentiert das Attribut, das angibt, <xref:System.ComponentModel.TypeConverter> welches für einen benutzerdefinierten Eigenschaftentyp verwendet werden soll.  
  
 <xref:System.ComponentModel.EditorAttribute>  
 Dokumentiert das-Attribut, das den angibt <xref:System.Drawing.Design.UITypeEditor> , der für eine benutzerdefinierte Eigenschaft verwendet werden soll.  
  
## <a name="related-sections"></a>Verwandte Abschnitte  

 [Attribute in Windows Forms-Steuerelementen](attributes-in-windows-forms-controls.md)  
 Beschreibt die Attribute, die Sie auf Eigenschaften oder andere Member der benutzerdefinierten Steuerelemente und Komponenten anwenden können.  
  
 [Entwurfszeitattribute für Komponenten](/previous-versions/visualstudio/visual-studio-2013/tk67c2t8(v=vs.120))  
 Listet die Metadatenattribute für Komponenten und Steuerelemente auf, damit sie in visuellen Designern zur Entwurfszeit korrekt angezeigt werden.  
  
 [Erweitern der Entwurfszeitunterstützung](/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120))  
 Beschreibt die Implementierung von Klassen wie Editoren und Designern, die Entwurfszeitunterstützung bereitstellen.
