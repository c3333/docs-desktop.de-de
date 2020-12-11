---
title: Übersicht über die SaveFileDialog-Komponente
ms.date: 03/30/2017
f1_keywords:
- SaveFileDialog
helpviewer_keywords:
- Save File dialog box [Windows Forms], displaying
- SaveFileDialog component [Windows Forms], about SaveFileDialog
ms.assetid: be7a625f-46fd-4d06-9985-b613dcbf9bd2
ms.openlocfilehash: 7609c29b7e932ecee7dc8a289617094bd8d480e2
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972338"
---
# <a name="savefiledialog-component-overview-windows-forms"></a><span data-ttu-id="8c482-102">Übersicht über die SaveFileDialog-Komponente (Windows Forms)</span><span class="sxs-lookup"><span data-stu-id="8c482-102">SaveFileDialog Component Overview (Windows Forms)</span></span>

<span data-ttu-id="8c482-103">Bei der Windows Forms-Komponente <xref:System.Windows.Forms.SaveFileDialog> handelt es sich um ein vorkonfiguriertes Dialogfeld.</span><span class="sxs-lookup"><span data-stu-id="8c482-103">The Windows Forms <xref:System.Windows.Forms.SaveFileDialog> component is a pre-configured dialog box.</span></span> <span data-ttu-id="8c482-104">Dies ist das gleiche wie das von Windows verwendete Standard Dialogfeld zum **Speichern von Dateien** .</span><span class="sxs-lookup"><span data-stu-id="8c482-104">It is the same as the standard **Save File** dialog box used by Windows.</span></span> <span data-ttu-id="8c482-105">Sie erbt von der <xref:System.Windows.Forms.CommonDialog>-Klasse.</span><span class="sxs-lookup"><span data-stu-id="8c482-105">It inherits from the <xref:System.Windows.Forms.CommonDialog> class.</span></span>

## <a name="working-with-the-savefiledialog-component"></a><span data-ttu-id="8c482-106">Arbeiten mit der SaveFileDialog-Komponente</span><span class="sxs-lookup"><span data-stu-id="8c482-106">Working with the SaveFileDialog Component</span></span>

<span data-ttu-id="8c482-107">Verwenden Sie es als einfache Lösung, um Benutzern das Speichern von Dateien zu ermöglichen, anstatt ein eigenes Dialogfeld zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="8c482-107">Use it as a simple solution for enabling users to save files instead of configuring your own dialog box.</span></span> <span data-ttu-id="8c482-108">Wenn Sie sich auf standardmäßige Windows-Dialogfelder verlassen, sind die grundlegenden Funktionen der Anwendungen, die Sie erstellen, Benutzern sofort vertraut.</span><span class="sxs-lookup"><span data-stu-id="8c482-108">By relying on standard Windows dialog boxes, the basic functionality of applications you create is immediately familiar to users.</span></span> <span data-ttu-id="8c482-109">Beachten Sie jedoch, dass Sie bei der Verwendung der- <xref:System.Windows.Forms.SaveFileDialog> Komponente eine eigene Logik zum Speichern von Dateien schreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="8c482-109">Be aware, however, that when using the <xref:System.Windows.Forms.SaveFileDialog> component, you must write your own file-saving logic.</span></span>

<span data-ttu-id="8c482-110">Sie können die- <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> Methode verwenden, um das Dialogfeld zur Laufzeit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c482-110">You can use the <xref:System.Windows.Forms.CommonDialog.ShowDialog%2A> method to display the dialog box at run time.</span></span> <span data-ttu-id="8c482-111">Sie können eine Datei im Lese-/Schreibmodus mit der- <xref:System.Windows.Forms.SaveFileDialog.OpenFile%2A> Methode öffnen.</span><span class="sxs-lookup"><span data-stu-id="8c482-111">You can open a file in read/write mode using the <xref:System.Windows.Forms.SaveFileDialog.OpenFile%2A> method.</span></span>

<span data-ttu-id="8c482-112">Wenn Sie einem Formular hinzugefügt wird, wird die <xref:System.Windows.Forms.SaveFileDialog> Komponente in der Leiste am unteren Rand des Windows Forms-Designer in Visual Studio angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c482-112">When it is added to a form, the <xref:System.Windows.Forms.SaveFileDialog> component appears in the tray at the bottom of the Windows Forms Designer in Visual Studio.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c482-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c482-113">See also</span></span>

- <xref:System.Windows.Forms.SaveFileDialog>
- [<span data-ttu-id="8c482-114">SaveFileDialog-Komponente</span><span class="sxs-lookup"><span data-stu-id="8c482-114">SaveFileDialog Component</span></span>](savefiledialog-component-windows-forms.md)
