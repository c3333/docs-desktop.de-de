---
title: Übersicht über die PageSetupDialog-Komponente
ms.date: 03/30/2017
f1_keywords:
- PageSetupDialog
helpviewer_keywords:
- Page Setup dialog box [Windows Forms], displaying
- PageSetupDialog component
ms.assetid: 791caacb-a5ca-4fca-bad9-1a5721ad697c
ms.openlocfilehash: a891cb8cc77007d7591d41461c94f61c077eb300
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976685"
---
# <a name="pagesetupdialog-component-overview-windows-forms"></a><span data-ttu-id="8eaed-102">Übersicht über die PageSetupDialog-Komponente (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="8eaed-102">PageSetupDialog Component Overview (Windows Forms)</span></span>

<span data-ttu-id="8eaed-103">Bei der Windows Forms <xref:System.Windows.Forms.PageSetupDialog> Komponente handelt es sich um ein vorkonfiguriertes Dialogfeld, mit dem Seitendetails für das Drucken in Windows-basierten Anwendungen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8eaed-103">The Windows Forms <xref:System.Windows.Forms.PageSetupDialog> component is a pre-configured dialog box used to set page details for printing in Windows-based applications.</span></span> <span data-ttu-id="8eaed-104">Verwenden Sie es in Ihrer Windows-basierten Anwendung als einfache Lösung, damit Benutzer Seiteneinstellungen festlegen können, anstatt ein eigenes Dialogfeld zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8eaed-104">Use it within your Windows-based application as a simple solution for users to set page preferences in lieu of configuring your own dialog box.</span></span> <span data-ttu-id="8eaed-105">Sie können es Benutzern ermöglichen, Rahmen-und Rand Anpassungen, Kopf-und Fußzeilen sowie hoch-oder Querformat festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8eaed-105">You can enable users to set border and margin adjustments, headers and footers, and portrait or landscape orientation.</span></span> <span data-ttu-id="8eaed-106">Durch die Verwendung von Windows-Standarddialogfeldern erstellen Sie Anwendungen, deren Basisfunktionen Benutzern sofort vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="8eaed-106">By relying on standard Windows dialog boxes, you create applications whose basic functionality is immediately familiar to users.</span></span>

## <a name="key-properties-and-methods"></a><span data-ttu-id="8eaed-107">Schlüsseleigenschaften und-Methoden</span><span class="sxs-lookup"><span data-stu-id="8eaed-107">Key Properties and Methods</span></span>

<span data-ttu-id="8eaed-108">Verwenden Sie die- <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode, um das Dialogfeld zur Laufzeit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8eaed-108">Use the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method to display the dialog at run time.</span></span> <span data-ttu-id="8eaed-109">Diese Komponente verfügt über Eigenschaften, die Sie festlegen können, die sich auf eine einzelne Seite ( <xref:System.Drawing.Printing.PrintDocument> Klasse) oder ein beliebiges Dokument ( <xref:System.Drawing.Printing.PageSettings> Klasse) beziehen.</span><span class="sxs-lookup"><span data-stu-id="8eaed-109">This component has properties you can set that relate to either a single page (<xref:System.Drawing.Printing.PrintDocument> class) or any document (<xref:System.Drawing.Printing.PageSettings> class).</span></span> <span data-ttu-id="8eaed-110">Außerdem kann die- <xref:System.Windows.Forms.PageSetupDialog> Komponente verwendet werden, um bestimmte Druckereinstellungen zu bestimmen, die in der-Klasse gespeichert werden <xref:System.Drawing.Printing.PrinterSettings> .</span><span class="sxs-lookup"><span data-stu-id="8eaed-110">Additionally, the <xref:System.Windows.Forms.PageSetupDialog> component can be used to determine specific printer settings, which are stored in the <xref:System.Drawing.Printing.PrinterSettings> class.</span></span>

<span data-ttu-id="8eaed-111">Wenn Sie einem Formular hinzugefügt wird, wird die <xref:System.Windows.Forms.PageSetupDialog> Komponente in der Leiste am unteren Rand des Windows Forms-Designer in Visual Studio angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8eaed-111">When it is added to a form, the <xref:System.Windows.Forms.PageSetupDialog> component appears in the tray at the bottom of the Windows Forms Designer in Visual Studio.</span></span>

## <a name="see-also"></a><span data-ttu-id="8eaed-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8eaed-112">See also</span></span>

- <xref:System.Windows.Forms.PageSetupDialog>
- [<span data-ttu-id="8eaed-113">PageSetupDialog-Komponente</span><span class="sxs-lookup"><span data-stu-id="8eaed-113">PageSetupDialog Component</span></span>](pagesetupdialog-component-windows-forms.md)
