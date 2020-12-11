---
title: 'Vorgehensweise: Erneutes Zuweisen von vorhandenen Steuerelementen zu einem anderen übergeordneten Element'
ms.date: 03/30/2017
helpviewer_keywords:
- container controls [Windows Forms], Windows Forms
- layout [Windows Forms], resizing
- layout [Windows Forms], child controls
ms.assetid: 5a5723ff-34e0-4b6f-a57b-be4ebe35cb34
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: 1767fcff1742f4ad630b4b996c709b7ded53a129
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96974768"
---
# <a name="how-to-reassign-existing-controls-to-a-different-parent"></a>Gewusst wie: Neuzuweisen vorhandener Steuerelemente zu einem anderen übergeordneten Element

Sie können auf Ihrem Formular vorhandene Steuerelemente einem neuen Containersteuerelement zuordnen.

1. Ziehen Sie in Visual Studio drei Steuer <xref:System.Windows.Forms.Button> Elemente aus der **Toolbox** auf das Formular. Positionieren Sie sie nahe beieinander, ohne sie aber auszurichten.

2. Klicken Sie in der **Toolbox** auf das Symbol des <xref:System.Windows.Forms.FlowLayoutPanel> -Steuerelements. (Ziehen Sie das Symbol nicht auf das Formular.)

3. Bewegen Sie den Mauszeiger in die Nähe der drei <xref:System.Windows.Forms.Button> -Steuerelemente.

   Der Mauszeiger nimmt die Form eines Fadenkreuzes an, an das das Symbol des <xref:System.Windows.Forms.FlowLayoutPanel> -Steuerelements angefügt ist.

4. Klicken Sie, und halten Sie die Maustaste gedrückt.

5. Ziehen Sie den Mauszeiger, um die Kontur des <xref:System.Windows.Forms.FlowLayoutPanel> -Steuerelements zu zeichnen.

6. Ziehen Sie die Kontur um die drei <xref:System.Windows.Forms.Button> -Steuerelemente.

7. Lassen Sie die Maustaste los.

   Die drei <xref:System.Windows.Forms.Button> -Steuerelemente werden jetzt in das <xref:System.Windows.Forms.FlowLayoutPanel> -Steuerelement eingefügt.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.FlowLayoutPanel>
- <xref:System.Windows.Forms.TableLayoutPanel>
- [Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von TableLayoutPanel](walkthrough-arranging-controls-on-windows-forms-using-a-tablelayoutpanel.md)
- [Exemplarische Vorgehensweise: Anordnen von Steuerelementen in Windows Forms mithilfe von Ausrichtungslinien](walkthrough-arranging-controls-on-windows-forms-using-snaplines.md)
