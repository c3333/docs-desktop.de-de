---
title: Label-Steuerelement
description: Hier erfahren Sie mehr über das Label-Steuerelement in Windows Forms für .NET. Bezeichnungen werden verwendet, um visuelle Elemente für den Benutzer zu identifizieren.
ms.date: 10/26/2020
ms.topic: overview
f1_keywords:
- Label
helpviewer_keywords:
- images [Windows Forms], displaying in labels
- labels
- Label control [Windows Forms], about Label control
ms.openlocfilehash: 6f669b7aef1182c35e125ff8dd3ca5ccb299b898
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942085"
---
# <a name="label-control-overview-windows-forms-net"></a>Übersicht über das Label-Steuerelement (Windows Forms .NET)

<xref:System.Windows.Forms.Label>-Steuerelemente in Windows Forms werden verwendet, um Text anzuzeigen, der vom Benutzer nicht bearbeitet werden kann. Sie werden zum Identifizieren von Objekten in einem Formular und zum Bereitstellen einer Beschreibung verwendet, was ein bestimmtes Steuerelement darstellt oder macht. Beispielsweise können Sie Bezeichnungen verwenden, um unter anderem Textfeldern, Listenfeldern und Kombinationsfeldern beschreibende Beschriftungstexte hinzuzufügen. Sie können auch Code schreiben, mit dem der Text geändert wird, der von einer Bezeichnung als Reaktion auf Ereignisse zur Laufzeit angezeigt wird.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="working-with-the-label-control"></a>Arbeiten mit dem Label-Steuerelement  

Da das <xref:System.Windows.Forms.Label>-Steuerelement keinen Fokus erhalten kann, kann es zum Erstellen von Tastenkombinationen für andere Steuerelemente verwendet werden. Mithilfe einer Tastenkombination kann ein Benutzer das nächste Steuerelement in der Aktivierreihenfolge fokussieren, indem er die <kbd>ALT-TASTE</kbd> mit der ausgewählten Tastenkombination drückt. Weitere Informationen finden Sie unter [Verwenden einer Bezeichnung zum Fokussieren eines Steuerelements](how-to-create-access-keys.md#use-a-label-to-focus-a-control).
  
Der in der Bezeichnung angezeigte Beschriftungstext ist in der <xref:System.Windows.Forms.Label.Text%2A>-Eigenschaft enthalten. Mit der <xref:System.Windows.Forms.Label.TextAlign%2A>-Eigenschaft können Sie die Ausrichtung des Texts innerhalb der Bezeichnung festlegen. Weitere Informationen finden Sie unter [Vorgehensweise: Festlegen des durch ein Windows Forms-Steuerelement angezeigten Texts](how-to-set-the-display-text.md).

## <a name="see-also"></a>Siehe auch

- [Verwenden einer Bezeichnung zum Fokussieren eines Steuerelements (Windows Forms .NET)](how-to-create-access-keys.md#use-a-label-to-focus-a-control)
- [Vorgehensweise: Festlegen des durch ein Steuerelement angezeigten Texts (Windows Forms .NET)](how-to-set-the-display-text.md)
- <xref:System.Windows.Forms.ContainerControl.AutoScaleMode%2A>
- <xref:System.Windows.Forms.Control.Scale%2A>
- <xref:System.Windows.Forms.ContainerControl.PerformAutoScale%2A>
- <xref:System.Windows.Forms.ContainerControl.AutoScaleDimensions%2A>
