---
title: Übersicht über das LinkLabel-Steuerelement
ms.date: 03/30/2017
f1_keywords:
- LinkLabel
helpviewer_keywords:
- links [Windows Forms], LinkLabel control
- Label control [Windows Forms], about Label control
- LinkLabel control [Windows Forms], about LinkLabel control
ms.assetid: 9e248549-10ca-43a3-bb5e-60f583d369f1
ms.openlocfilehash: 3e8607644c858ae804e384c974b5e81c1786c6a1
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976721"
---
# <a name="linklabel-control-overview-windows-forms"></a>Übersicht über das LinkLabel-Steuerelement (Windows Forms)
Mit dem Windows Forms- <xref:System.Windows.Forms.LinkLabel> Steuerelement können Sie Windows Forms Anwendungen Links im Webstil hinzufügen. Sie können das-Steuerelement für alle Elemente verwenden, <xref:System.Windows.Forms.LinkLabel> für die Sie das Steuerelement verwenden können <xref:System.Windows.Forms.Label> . Sie können einen Textabschnitt auch als Link zu einer Datei, einem Ordner oder einer Webseite festlegen.  
  
## <a name="what-you-can-do-with-the-linklabel-control"></a>Was Sie mit dem LinkLabel-Steuerelement tun können  
 Zusätzlich zu allen Eigenschaften, Methoden und Ereignissen des- <xref:System.Windows.Forms.Label> Steuer Elements enthält das- <xref:System.Windows.Forms.LinkLabel> Steuerelement Eigenschaften für Hyperlinks und Verknüpfungs Farben. Die- <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> Eigenschaft legt den Bereich des Texts fest, mit dem der Link aktiviert wird. Die <xref:System.Windows.Forms.LinkLabel.LinkColor%2A> <xref:System.Windows.Forms.LinkLabel.VisitedLinkColor%2A> Eigenschaften, und <xref:System.Windows.Forms.LinkLabel.ActiveLinkColor%2A> legen die Farben des Links fest. Das <xref:System.Windows.Forms.LinkLabel.LinkClicked> Ereignis bestimmt, was geschieht, wenn der Linktext ausgewählt wird.  
  
 Die einfachste Verwendung des- <xref:System.Windows.Forms.LinkLabel> Steuer Elements besteht darin, einen einzelnen Link mithilfe der- <xref:System.Windows.Forms.LinkLabel.LinkArea%2A> Eigenschaft anzuzeigen. Sie können jedoch auch mehrere Hyperlinks mithilfe der- <xref:System.Windows.Forms.LinkLabel.Links%2A> Eigenschaft anzeigen. Mit der- <xref:System.Windows.Forms.LinkLabel.Links%2A> Eigenschaft können Sie auf eine Auflistung von Links zugreifen. Sie können auch Daten in der- <xref:System.Windows.Forms.LinkLabel.Link.LinkData%2A> Eigenschaft jedes einzelnen <xref:System.Windows.Forms.LinkLabel.Link> Objekts angeben. Der Wert der- <xref:System.Windows.Forms.LinkLabel.Link.LinkData%2A> Eigenschaft kann verwendet werden, um den Speicherort einer Datei zu speichern, die angezeigt werden soll, oder die Adresse einer Website.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.LinkLabel>
- [Übersicht über das Label-Steuerelement](label-control-overview-windows-forms.md)
- [Vorgehensweise: Verknüpfen eines Objekts oder einer Webseite mit dem LinkLabel-Steuerelement in Windows Forms](link-to-an-object-or-web-page-with-wf-linklabel-control.md)
- [Vorgehensweise: Ändern der Darstellung des LinkLabel-Steuerelements in Windows Forms](how-to-change-the-appearance-of-the-windows-forms-linklabel-control.md)
