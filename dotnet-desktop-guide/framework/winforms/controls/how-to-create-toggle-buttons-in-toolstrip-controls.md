---
title: 'Vorgehensweise: Erstellen von Umschaltflächen in ToolStrip-Steuerelementen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- toggle buttons [Windows Forms], creating
- examples [Windows Forms], toolbars
- ToolStrip control [Windows Forms], creating toggle buttons
ms.assetid: d9c197df-4c65-43f2-beee-b68b52b2befc
ms.openlocfilehash: 6a003b91cd4db5db2790a20db97dbaa4d8925e96
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976328"
---
# <a name="how-to-create-toggle-buttons-in-toolstrip-controls"></a>Vorgehensweise: Erstellen von Umschaltflächen in ToolStrip-Steuerelementen

Wenn ein Benutzer auf eine UMSCHALT Fläche klickt, wird er abgeversenkt angezeigt und behält die abgesendeten Darstellung bei, bis der Benutzer erneut auf die Schaltfläche klickt.

## <a name="to-create-a-toggling-toolstripbutton"></a>So erstellen Sie ein UMSCHALT Fläche-Tool Strip Button

- Verwenden Sie Code wie im folgenden Codebeispiel. In diesem Code wird davon ausgegangen, dass das Formular ein <xref:System.Windows.Forms.ToolStrip> -Steuerelement enthält und dass die zugehörige Auflistung <xref:System.Windows.Forms.ToolStrip.Items%2A> einen <xref:System.Windows.Forms.ToolStripButton> aufgerufenen enthält `toolStripButton1` Außerdem wird davon ausgegangen, dass Sie über einen Ereignishandler namens verfügen `toolStripButton1_CheckedChanged` .

    ```vb
    toolStripButton1.CheckOnClick = True
    toolStripButton1.CheckedChanged AddressOf _
    EventHandler(toolStripButton1_CheckedChanged);
    ```

    ```csharp
    toolStripButton1.CheckOnClick = true;
    toolStripButton1.CheckedChanged += new _
    EventHandler(toolStripButton1_CheckedChanged);
    ```

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolStripButton>
- [Übersicht über das ToolStrip-Steuerelement](toolstrip-control-overview-windows-forms.md)
