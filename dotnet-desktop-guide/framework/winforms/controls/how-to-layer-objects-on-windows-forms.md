---
title: Überlagern von Objekten
description: Erfahren Sie, wie Sie Objekte auf Windows Forms Steuerelementen und untergeordneten Formularen Ebenen, um komplexere Benutzeroberflächen zu erstellen.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- Windows Forms controls, layering
- controls [Windows Forms], layering
- z order
- controls [Windows Forms], positioning
- z-order
ms.assetid: 1acc4281-2976-4715-86f4-bda68134baaf
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: 6269b09c56963fefd500b9e1e6c9d7f51f9619cf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976606"
---
# <a name="how-to-layer-objects-on-windows-forms"></a>Gewusst wie: Ebenenobjekte auf Windows Forms

Beim Erstellen einer komplexen Benutzeroberfläche oder bei Verwendung eines MDI-Formulars (Multiple Document Interface) empfiehlt es sich, sowohl Steuerelemente als auch untergeordnete Formulare zu verlagern, um komplexere Benutzeroberflächen (UI) zu erstellen. Um Steuerelemente und Fenster innerhalb des Kontexts einer Gruppe zu verschieben und zu verfolgen, bearbeiten Sie Ihre *z-Reihenfolge*. Die z-Reihenfolge ist das visuelle Schichten von Steuerelementen in einem Formular entlang der z-Achse (Tiefe) des Formulars. Das Fenster oben in der z-Reihenfolge überlappt alle anderen Fenster. Alle anderen Fenster überlappen das Fenster am unteren Rand der z-Reihenfolge.

## <a name="to-layer-controls-at-design-time"></a>Auf ebenensteuerelemente zur Entwurfszeit

1. Wählen Sie in Visual Studio ein Steuerelement aus, das Sie Ebenen möchten.

2. Wählen Sie im Menü **Format** die Option **Reihenfolge** aus, und wählen Sie dann **in den Vorder** Grund oder in den **Hintergrund**.

## <a name="to-layer-controls-programmatically"></a>Zum programmgesteuerten ebenensteuerelement

Verwenden <xref:System.Windows.Forms.Control.BringToFront%2A> Sie die <xref:System.Windows.Forms.Control.SendToBack%2A> Methoden und, um die z-Reihenfolge der Steuerelemente zu bearbeiten.

Wenn sich z. b. ein <xref:System.Windows.Forms.TextBox> Steuerelement, `txtFirstName` , unter einem anderen Steuerelement befindet und Sie es oben verwenden möchten, verwenden Sie den folgenden Code:

```vb
txtFirstName.BringToFront()
```

```csharp
txtFirstName.BringToFront();
```

```cpp
txtFirstName->BringToFront();
```

> [!NOTE]
> Windows Forms unterstützt die Einschluss *Steuerung*. Die Einschluss Steuerung umfasst das Platzieren einer Reihe von Steuerelementen innerhalb eines enthaltenden Steuer Elements, z. b. eine Reihe von Steuer <xref:System.Windows.Forms.RadioButton> Elementen in einem <xref:System.Windows.Forms.GroupBox> Steuerelement Anschließend können Sie die Steuerelemente innerhalb des enthaltenden Steuer Elements Schichten. Wenn Sie das Gruppenfeld verschieben, werden auch die Steuerelemente verschoben, da Sie darin enthalten sind.

## <a name="see-also"></a>Siehe auch

- [Windows Forms Steuerelemente](index.md)
- [Beschriften einzelner Steuerelemente für Windows Forms und Konfigurieren von Shortcuts für diese Elemente](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [Steuerelemente für Windows Forms](controls-to-use-on-windows-forms.md)
- [Windows Forms-Steuerelemente nach Funktion](windows-forms-controls-by-function.md)
