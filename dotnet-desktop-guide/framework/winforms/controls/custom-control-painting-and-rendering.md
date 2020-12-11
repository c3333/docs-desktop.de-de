---
title: Zeichnen und Ausgeben von benutzerdefinierten Steuerelementen
ms.date: 03/30/2017
helpviewer_keywords:
- custom controls [Windows Forms], rendering
- custom controls [Windows Forms], painting
- user controls [Windows Forms], painting
ms.assetid: a09dbf76-0966-4cbf-a66a-2083ba98e068
ms.openlocfilehash: 14abac5678bfffa3cdb61307fd3cb54681c82a99
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972198"
---
# <a name="custom-control-painting-and-rendering"></a>Zeichnen und Ausgeben von benutzerdefinierten Steuerelementen
Das benutzerdefinierte Zeichnen von Steuerelementen ist eine der vielen komplizierten Aufgaben, die durch die .NET Framework einfach gemacht werden. Wenn Sie ein benutzerdefiniertes Steuerelement erstellen, stehen Ihnen viele Optionen hinsichtlich der grafischen Darstellung des Steuer Elements zur Verfügung. Wenn Sie ein Steuerelement erstellen, das von erbt `Control` , müssen Sie Code bereitstellen, der es dem Steuerelement ermöglicht, seine grafische Darstellung zu Rendering. Wenn Sie ein Benutzer Steuerelement erstellen, indem Sie von Erben `UserControl` , oder von einem der Windows Forms Steuerelemente erben, können Sie die grafische Standarddarstellung überschreiben und ihren eigenen Grafik Code bereitstellen. Wenn Sie ein benutzerdefiniertes Rendering für die konstituierenden Steuerelemente einer erstellen möchten `UserControl` , die Sie erstellen, werden die Optionen eingeschränkt, aber Sie können dennoch eine große Bandbreite grafischer Möglichkeiten für Ihre Steuerelemente und Anwendungen erhalten.  
  
## <a name="in-this-section"></a>In diesem Abschnitt  
 [Wiedergeben eines Windows Forms-Steuerelements](rendering-a-windows-forms-control.md)  
 Zeigt, wie die Logik programmiert wird, die ein-Steuerelement anzeigt.  
  
 [Benutzerdefinierte Steuerelemente](user-drawn-controls.md)  
 Bietet einen Überblick über die Schritte zum Schreiben und Überschreiben von Renderingcode für das Steuerelement.  
  
 [Konstituierende Steuerelemente](constituent-controls.md)  
 Beschreibt, wie benutzerdefinierter Renderingcode für konstituierende Steuerelemente in den Benutzer Steuerelementen und Formularen implementiert wird.  
  
 [Vorgehensweise: Ausblenden des Steuerelements zur Laufzeit](how-to-make-your-control-invisible-at-run-time.md)  
 Zeigt, wie die <xref:System.Windows.Forms.Control.Visible%2A> -Eigenschaft verwendet wird, um ein Steuerelement auszublenden und anzuzeigen.  
  
 [Vorgehensweise: Verwenden eines transparenten Hintergrunds für ein Steuerelement](how-to-give-your-control-a-transparent-background.md)  
 Zeigt, wie die- <xref:System.Windows.Forms.Control.SetStyle%2A> Methode verwendet wird, um eine nicht transparente, transparente oder teilweise transparente Hintergrundfarbe zu erstellen.  
  
 [Rendering von Steuerelementen mit visuellen Stilen](rendering-controls-with-visual-styles.md)  
 Veranschaulicht das Rendering von Steuerelementen mit visuellen Stilen in Betriebssystemen, die diese unterstützen.  
  
## <a name="reference"></a>Verweis  
 <xref:System.Windows.Forms.Control>  
 Beschreibt diese Klasse und enthält Links zu allen Membern.  
  
 <xref:System.Windows.Forms.UserControl>  
 Beschreibt diese Klasse und enthält Links zu allen Membern.  
  
 <xref:System.Windows.Forms.Control.OnPaint%2A>  
 Beschreibt diese Methode.  
  
## <a name="related-sections"></a>Verwandte Abschnitte  
 [Vorgehensweise: Erstellen von Grafikobjekten zum Zeichnen](../advanced/how-to-create-graphics-objects-for-drawing.md)  
 Stellt die GDI+-Grafik Funktionalität aus einer Visual Studio-Perspektive vor und enthält Links zu weiteren Informationen.  
  
 [Arten von benutzerdefinierten Steuerelementen](varieties-of-custom-controls.md)  
 Beschreibt die Arten von benutzerdefinierten Steuerelementen, die Sie erstellen können.
