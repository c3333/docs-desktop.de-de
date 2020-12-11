---
title: Festlegen einer Schaltfläche als "Abbrechen"-Schaltfläche mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- buttons [Windows Forms], cancel buttons
- Button control [Windows Forms], designating as cancel button
ms.assetid: 30e77d9c-d565-4ab5-a84a-62c043af8822
ms.openlocfilehash: 95d1139b6e339055f944ad0b0967a6d91283d49e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972135"
---
# <a name="how-to-designate-a-windows-forms-button-as-the-cancel-button-using-the-designer"></a>Vorgehensweise: Definieren einer Windows Forms-Schaltfläche als „Abbrechen“-Schaltfläche mithilfe des Designers
In jedem Windows Form können Sie ein Steuerelement als <xref:System.Windows.Forms.Button> Schaltfläche "Abbrechen" festlegen. Wenn der Benutzer die ESC-Taste drückt, wird auf eine Schaltfläche Abbrechen geklickt, unabhängig davon, welches andere Steuerelement im Formular den Fokus besitzt. Eine solche Schaltfläche wird in der Regel so programmiert, dass der Benutzer schnell einen Vorgang beenden kann, ohne dass eine Aktion ausgeführt werden muss.

## <a name="to-designate-the-cancel-button"></a>So bestimmen Sie die Schaltfläche Abbrechen

1. Wählen Sie das Formular aus, in dem sich die Schaltfläche befindet.

2. Legen Sie im Fenster **Eigenschaften** die-Eigenschaft des Formulars <xref:System.Windows.Forms.Form.CancelButton%2A> auf den <xref:System.Windows.Forms.Button> Namen des-Steuer Elements fest.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Form.CancelButton%2A>
- [Übersicht über das Button-Steuerelement](button-control-overview-windows-forms.md)
- [Methoden zur Auswahl eines Button-Steuerelements in Windows Forms](ways-to-select-a-windows-forms-button-control.md)
- [Gewusst wie: Reagieren auf das Anklicken von Schaltflächen in Windows Forms](how-to-respond-to-windows-forms-button-clicks.md)
- [Vorgehensweise: Definieren einer Windows Forms-Schaltfläche als „Annehmen“-Schaltfläche mithilfe des Designers](designate-a-wf-button-as-the-accept-button-using-the-designer.md)
- [Button-Steuerelement](button-control-windows-forms.md)
