---
title: Übersicht über die ToolTip-Komponente
ms.date: 03/30/2017
f1_keywords:
- ToolTip
helpviewer_keywords:
- tooltips [Windows Forms], about tooltips
- ToolTip component [Windows Forms], about ToolTip component
ms.assetid: 3fbc6f08-c882-4acd-a960-a08efe3c7e6e
ms.openlocfilehash: 731f7ad0ce6670000d8c3d3e901e1506f7ef470a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977145"
---
# <a name="tooltip-component-overview-windows-forms"></a>Übersicht über die ToolTip-Komponente (Windows Forms)
Die <xref:System.Windows.Forms.ToolTip>-Komponente in Windows Forms zeigt Text an, wenn der Benutzer auf Steuerelemente zeigt. Jedem Steuerelement kann eine QuickInfo zugeordnet werden. Ein Beispiel für die Verwendung dieser Komponente: um Speicherplatz auf einem Formular zu sparen, können Sie ein kleines Symbol auf einer Schaltfläche anzeigen und mithilfe einer QuickInfo die Funktion der Schaltfläche erläutern.  
  
## <a name="working-with-the-tooltip-component"></a>Arbeiten mit der ToolTip-Komponente  
 Eine <xref:System.Windows.Forms.ToolTip> Komponente stellt eine `ToolTip` Eigenschaft für mehrere Steuerelemente in einem Windows Form oder einem anderen Container bereit. Wenn Sie z. b. eine <xref:System.Windows.Forms.ToolTip> Komponente in einem Formular platzieren, können Sie "hier Ihren Namen eingeben" für ein <xref:System.Windows.Forms.TextBox> Steuerelement anzeigen und "klicken Sie hier, um die Änderungen zu speichern" für ein <xref:System.Windows.Forms.Button> Steuerelement.  
  
 Die Schlüsselmethoden der <xref:System.Windows.Forms.ToolTip> Komponente sind <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> und <xref:System.Windows.Forms.ToolTip.GetToolTip%2A> . Sie können die- <xref:System.Windows.Forms.ToolTip.SetToolTip%2A> Methode verwenden, um die für Steuerelemente angezeigten Quick Infos festzulegen. Weitere Informationen finden [Sie unter Gewusst wie: Festlegen von Quick Infos für Steuerelemente auf einem Windows Form zur Entwurfszeit](how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time.md). Die Schlüsseleigenschaften sind <xref:System.Windows.Forms.ToolTip.Active%2A> , die auf festgelegt werden müssen, damit die QuickInfo angezeigt wird `true` , und, womit die Zeitspanne festgelegt wird, in der die QuickInfo- <xref:System.Windows.Forms.ToolTip.AutomaticDelay%2A> Zeichenfolge angezeigt wird, wie lange der Benutzer auf das Steuerelement zeigen muss, damit die QuickInfo angezeigt wird, und wie lange es dauert, bis nachfolgende QuickInfo angezeigt werden Weitere Informationen finden Sie unter Gewusst [wie: Ändern der Verzögerung der Windows Forms ToolTip-Komponente](how-to-change-the-delay-of-the-windows-forms-tooltip-component.md).  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ToolTip>
- [Vorgehensweise: Festlegen von QuickInfos für Steuerelemente auf einem Windows Form zur Entwurfszeit](how-to-set-tooltips-for-controls-on-a-windows-form-at-design-time.md)
- [Vorgehensweise: Ändern der Verzögerung der ToolTip-Komponente in Windows Forms](how-to-change-the-delay-of-the-windows-forms-tooltip-component.md)
