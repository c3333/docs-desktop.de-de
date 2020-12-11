---
title: Andocken von Steuerelementen
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], docking
- Explorer-style applications [Windows Forms], creating
- Windows Forms controls, filling client area
ms.assetid: bc11f2e4-e90a-4830-b0e2-f43b6e2b8bec
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: 02f1c26dcb322a39c41781c83d8c820bd2fd27e0
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976503"
---
# <a name="how-to-dock-controls-on-windows-forms"></a>Gewusst wie: Andocken von Steuerelementen auf Windows Forms

Sie können Steuerelemente an die Ränder Ihres Formulars andocken, oder Sie können den Container des Steuer Elements ausfüllen (entweder ein Formular oder ein Container Steuerelement). Windows-Explorer Dockt das Steuerelement beispielsweise <xref:System.Windows.Forms.TreeView> an die linke Seite des Fensters und dessen <xref:System.Windows.Forms.ListView> Steuerelement auf der rechten Seite des Fensters an. Verwenden Sie die- <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft für alle sichtbaren Windows Forms Steuerelemente, um den Docking Modus zu definieren.

> [!NOTE]
> Steuerelemente werden in umgekehrter z-Reihenfolge angedockt.

Die- <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft interagiert mit der- <xref:System.Windows.Forms.Control.AutoSize%2A> Eigenschaft. Weitere Informationen finden Sie unter [Übersicht über die AutoSize-Eigenschaft](autosize-property-overview.md).

## <a name="to-dock-a-control"></a>Zum Andocken eines Steuer Elements

1. Wählen Sie in Visual Studio das Steuerelement aus, das Sie andocken möchten.

2. Klicken Sie im **Eigenschaften** Fenster auf den Pfeil rechts neben der- <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft.

   Es wird ein Editor angezeigt, der eine Reihe von Feldern anzeigt, die die Ränder und den Mittelpunkt des Formulars darstellen.

3. Klicken Sie auf die Schaltfläche, die den Rand des Formulars darstellt, in dem Sie das Steuerelement andocken möchten. Um den Inhalt des Formular-oder Container Steuer Elements des Steuer Elements auszufüllen, klicken Sie auf das Feld Center. Klicken Sie zum Deaktivieren des Andock auf **(keine)** .

   Die Größe des Steuer Elements wird automatisch an die Grenzen des angedockten Rands angepasst.

   > [!NOTE]
   > Geerbte Steuerelemente müssen in der Lage sein, `Protected` angedockt zu werden. Um die Zugriffsebene eines Steuer Elements zu ändern, legen Sie seine **modifizierereigenschaft** im Fenster **Eigenschaften** fest.

## <a name="see-also"></a>Siehe auch

- [Windows Forms Steuerelemente](index.md)
- [Beschriften einzelner Steuerelemente für Windows Forms und Konfigurieren von Shortcuts für diese Elemente](labeling-individual-windows-forms-controls-and-providing-shortcuts-to-them.md)
- [Steuerelemente für Windows Forms](controls-to-use-on-windows-forms.md)
- [Windows Forms-Steuerelemente nach Funktion](windows-forms-controls-by-function.md)
- [Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem FlowLayoutPanel-Steuerelement](how-to-anchor-and-dock-child-controls-in-a-flowlayoutpanel-control.md)
- [Vorgehensweise: Verankern und Andocken von untergeordneten Steuerelementen in einem TableLayoutPanel-Steuerelement](how-to-anchor-and-dock-child-controls-in-a-tablelayoutpanel-control.md)
- [Übersicht über die AutoSize-Eigenschaft](autosize-property-overview.md)
- [Gewusst wie: Verankern von Steuerelementen in Windows Forms](how-to-anchor-controls-on-windows-forms.md)
