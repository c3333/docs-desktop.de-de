---
title: Anzeigen der Print Dialog-Komponente
ms.date: 03/30/2017
helpviewer_keywords:
- Print dialog box [Windows Forms], displaying
- PrintDialog component [Windows Forms], displaying
- printing [Windows Forms], displaying print dialog box
ms.assetid: 745a8db7-0526-4b21-b09d-18e13ed32014
ms.openlocfilehash: de0acc655bbcf0cfc017d594545fae56cc27f981
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975654"
---
# <a name="how-to-display-the-printdialog-component"></a><span data-ttu-id="166ed-102">Anzeigen der Print Dialog-Komponente</span><span class="sxs-lookup"><span data-stu-id="166ed-102">How to display the PrintDialog component</span></span>

<span data-ttu-id="166ed-103"><xref:System.Windows.Forms.PrintDialog>Bei der Komponente handelt es sich um das Standard Dialogfeld für den Windows-Druck, das viele Ihrer Benutzer kennen.</span><span class="sxs-lookup"><span data-stu-id="166ed-103">The <xref:System.Windows.Forms.PrintDialog> component is the standard Windows print dialog box that many of your users will be familiar with.</span></span> <span data-ttu-id="166ed-104">Da Ihre Benutzer sofort damit vertraut sind, ist es vorteilhaft, die Komponente zu verwenden <xref:System.Windows.Forms.PrintDialog> .</span><span class="sxs-lookup"><span data-stu-id="166ed-104">Because your users will be immediately comfortable with it, it would be beneficial for you to use the <xref:System.Windows.Forms.PrintDialog> component.</span></span>

## <a name="to-display-the-printdialog-component"></a><span data-ttu-id="166ed-105">So zeigen Sie die PrintDialog-Komponente an</span><span class="sxs-lookup"><span data-stu-id="166ed-105">To display the PrintDialog component</span></span>

- <span data-ttu-id="166ed-106">Ruft die- <xref:System.Windows.Forms.Form.ShowDialog%2A> Methode aus dem Code der Anwendung heraus auf.</span><span class="sxs-lookup"><span data-stu-id="166ed-106">Call the <xref:System.Windows.Forms.Form.ShowDialog%2A> method from within the code of your application.</span></span>

     <span data-ttu-id="166ed-107">Sobald die Komponente angezeigt wird, können die Benutzer damit interagieren und die Eigenschaften für den Druckauftrag einstellen.</span><span class="sxs-lookup"><span data-stu-id="166ed-107">Once the component is shown, users will interact with it, setting the properties of the print job.</span></span> <span data-ttu-id="166ed-108">Diese werden in der  <xref:System.Drawing.Printing.PrinterSettings> -Klasse (und der- <xref:System.Drawing.Printing.PageSettings> Klasse) gespeichert, wenn der Benutzer über die-Komponente auf die [PageSetupDialog-Komponente](pagesetupdialog-component-windows-forms.md) zugreift, die <xref:System.Windows.Forms.PrintDialog> diesem Druckauftrag zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="166ed-108">These are saved in the  <xref:System.Drawing.Printing.PrinterSettings> class (and the <xref:System.Drawing.Printing.PageSettings> class, if the user accesses the [PageSetupDialog Component](pagesetupdialog-component-windows-forms.md) through the <xref:System.Windows.Forms.PrintDialog> component) associated with that print job.</span></span> <span data-ttu-id="166ed-109">Dann können Sie Aufrufe an die von ihnen eingestellten Eigenschaften durchführen, um die spezifischen Merkmale des Druckauftrags anzugeben.</span><span class="sxs-lookup"><span data-stu-id="166ed-109">You can then make calls to the properties they set to determine the specifics of the print job.</span></span>

## <a name="see-also"></a><span data-ttu-id="166ed-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="166ed-110">See also</span></span>

- [<span data-ttu-id="166ed-111">Vorgehensweise: Erstellen von standardmäßigen Druckaufträgen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="166ed-111">How to: Create Standard Windows Forms Print Jobs</span></span>](../advanced/how-to-create-standard-windows-forms-print-jobs.md)
- [<span data-ttu-id="166ed-112">Vorgehensweise: Erfassen von Benutzereingaben in einem „PrintDialog“ zur Laufzeit</span><span class="sxs-lookup"><span data-stu-id="166ed-112">How to: Capture User Input from a PrintDialog at Run Time</span></span>](../advanced/how-to-capture-user-input-from-a-printdialog-at-run-time.md)
- [<span data-ttu-id="166ed-113">PrintPreviewDialog-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="166ed-113">PrintPreviewDialog Control</span></span>](printpreviewdialog-control-windows-forms.md)
- [<span data-ttu-id="166ed-114">PrintDialog-Komponente</span><span class="sxs-lookup"><span data-stu-id="166ed-114">PrintDialog Component</span></span>](printdialog-component-windows-forms.md)
- [<span data-ttu-id="166ed-115">Druckunterstützung in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="166ed-115">Windows Forms Print Support</span></span>](../advanced/windows-forms-print-support.md)
- [<span data-ttu-id="166ed-116">Windows Forms Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="166ed-116">Windows Forms Controls</span></span>](index.md)
