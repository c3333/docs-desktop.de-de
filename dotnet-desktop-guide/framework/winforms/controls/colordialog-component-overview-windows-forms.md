---
title: Übersicht über die ColorDialog-Komponente
ms.date: 03/30/2017
f1_keywords:
- ColorDialog
helpviewer_keywords:
- color dialog box [Windows Forms], about color dialog box
- ColorDialog component [Windows Forms], about ColorDialog
ms.assetid: 6dbdd8f0-f697-4728-bb09-7ea156f6d800
ms.openlocfilehash: 48d9d5072335908f85e65933dadafb1b69f28528
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972251"
---
# <a name="colordialog-component-overview-windows-forms"></a><span data-ttu-id="52f97-102">Übersicht über die ColorDialog-Komponente (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="52f97-102">ColorDialog Component Overview (Windows Forms)</span></span>
<span data-ttu-id="52f97-103">Bei der Windows Forms <xref:System.Windows.Forms.ColorDialog> Komponente handelt es sich um ein vorkonfiguriertes Dialogfeld, mit dem der Benutzer eine Farbe aus einer Palette auswählen und dieser Palette benutzerdefinierte Farben hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="52f97-103">The Windows Forms <xref:System.Windows.Forms.ColorDialog> component is a pre-configured dialog box that allows the user to select a color from a palette and to add custom colors to that palette.</span></span> <span data-ttu-id="52f97-104">Es entspricht dem Dialogfeld, das in anderen Windows-basierten Anwendungen zur Farbauswahl angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="52f97-104">It is the same dialog box that you see in other Windows-based applications to select colors.</span></span> <span data-ttu-id="52f97-105">Verwenden Sie es in Ihrer auf Windows basierenden Anwendung als einfache Lösung, anstatt ein eigenes Dialogfeld zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="52f97-105">Use it within your Windows-based application as a simple solution in lieu of configuring your own dialog box.</span></span>  
  
 <span data-ttu-id="52f97-106">Die im Dialogfeld ausgewählte Farbe wird in der-Eigenschaft zurückgegeben <xref:System.Windows.Forms.ColorDialog.Color%2A> .</span><span class="sxs-lookup"><span data-stu-id="52f97-106">The color selected in the dialog box is returned in the <xref:System.Windows.Forms.ColorDialog.Color%2A> property.</span></span> <span data-ttu-id="52f97-107">Wenn die- <xref:System.Windows.Forms.ColorDialog.AllowFullOpen%2A> Eigenschaft auf festgelegt ist `false` , wird die Schaltfläche "benutzerdefinierte Farben definieren" deaktiviert, und der Benutzer ist auf die vordefinierten Farben in der Palette beschränkt.</span><span class="sxs-lookup"><span data-stu-id="52f97-107">If the <xref:System.Windows.Forms.ColorDialog.AllowFullOpen%2A> property is set to `false`, the "Define Custom Colors" button is disabled and the user is restricted to the predefined colors in the palette.</span></span> <span data-ttu-id="52f97-108">Wenn die- <xref:System.Windows.Forms.ColorDialog.SolidColorOnly%2A> Eigenschaft auf festgelegt ist `true` , kann der Benutzer keine Dithering-Farben auswählen.</span><span class="sxs-lookup"><span data-stu-id="52f97-108">If the <xref:System.Windows.Forms.ColorDialog.SolidColorOnly%2A> property is set to `true`, the user cannot select dithered colors.</span></span> <span data-ttu-id="52f97-109">Um das Dialogfeld anzuzeigen, müssen Sie die zugehörige- <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="52f97-109">To display the dialog box, you must call its <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="52f97-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="52f97-110">See also</span></span>

- <xref:System.Windows.Forms.ColorDialog>
- [<span data-ttu-id="52f97-111">ColorDialog-Komponente</span><span class="sxs-lookup"><span data-stu-id="52f97-111">ColorDialog Component</span></span>](colordialog-component-windows-forms.md)
- [<span data-ttu-id="52f97-112">Dialogfeld-Steuerelemente und -Komponenten</span><span class="sxs-lookup"><span data-stu-id="52f97-112">Dialog-Box Controls and Components</span></span>](dialog-box-controls-and-components-windows-forms.md)
- [<span data-ttu-id="52f97-113">Vorgehensweise: Ändern der Darstellung der ColorDialog-Komponente in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="52f97-113">How to: Change the Appearance of the Windows Forms ColorDialog Component</span></span>](how-to-change-the-appearance-of-the-windows-forms-colordialog-component.md)
