---
title: Host Steuerelemente in DataGridView-Zellen
description: Erfahren Sie, wie Sie Steuerelemente in Windows Forms DataGridView-Zellen hosten, damit Benutzer auf unterschiedliche Weise Werte eingeben und bearbeiten können.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms], hosting in cells
- DataGridView control [Windows Forms], hosting controls in cells
- cells [Windows Forms], hosting controls
ms.assetid: e79a9d4e-64ec-41f5-93ec-f5492633cbb2
ms.openlocfilehash: 87901cbf86689bec49f5692feeabdae79f6b93ba
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975627"
---
# <a name="how-to-host-controls-in-windows-forms-datagridview-cells"></a><span data-ttu-id="eb8cf-103">Vorgehensweise: Hosten von Steuerelementen in DataGridView-Zellen in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="eb8cf-103">How to: Host Controls in Windows Forms DataGridView Cells</span></span>
<span data-ttu-id="eb8cf-104">Das <xref:System.Windows.Forms.DataGridView>Steuerelement bietet mehrere Spaltentypen, die es den Benutzern ermöglichen, Werte auf vielfältige Weise einzugeben und zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="eb8cf-104">The <xref:System.Windows.Forms.DataGridView> control provides several column types, enabling your users to enter and edit values in a variety of ways.</span></span> <span data-ttu-id="eb8cf-105">Wenn diese Spaltentypen Ihre Anforderungen an die Dateneingabe nicht erfüllen, können Sie jedoch auch eigene Spaltentypen mit Zellen erstellen, die von Ihnen gewählte Steuerelemente aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="eb8cf-105">If these column types do not meet your data-entry needs, however, you can create your own column types with cells that host controls of your choosing.</span></span> <span data-ttu-id="eb8cf-106">Zu diesem Zweck müssen Sie Klassen definieren, die von <xref:System.Windows.Forms.DataGridViewColumn> und <xref:System.Windows.Forms.DataGridViewCell> abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="eb8cf-106">To do this, you must define classes that derive from <xref:System.Windows.Forms.DataGridViewColumn> and <xref:System.Windows.Forms.DataGridViewCell>.</span></span> <span data-ttu-id="eb8cf-107">Außerdem müssen Sie eine Klasse definieren, die von <xref:System.Windows.Forms.Control> abgeleitet wird und die <xref:System.Windows.Forms.IDataGridViewEditingControl>-Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="eb8cf-107">You must also define a class that derives from <xref:System.Windows.Forms.Control> and implements the <xref:System.Windows.Forms.IDataGridViewEditingControl> interface.</span></span>  
  
 <span data-ttu-id="eb8cf-108">Im folgenden Codebeispiel wird das Erstellen einer Kalenderspalte veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="eb8cf-108">The following code example shows how to create a calendar column.</span></span> <span data-ttu-id="eb8cf-109">Die Zellen dieser Spalte zeigen Daten in einfachen Textfeldzellen an. Wenn der Benutzer jedoch eine Zelle bearbeitet, wird ein <xref:System.Windows.Forms.DateTimePicker>-Steuerelement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="eb8cf-109">The cells of this column display dates in ordinary text box cells, but when the user edits a cell, a <xref:System.Windows.Forms.DateTimePicker> control appears.</span></span> <span data-ttu-id="eb8cf-110">Um das erneute Implementieren der Funktionen für die Textfeldanzeige zu vermeiden, wird die `CalendarCell`Klasse von der <xref:System.Windows.Forms.DataGridViewTextBoxCell>-Klasse abgeleitet, anstatt die <xref:System.Windows.Forms.DataGridViewCell>-Klasse direkt zu erben.</span><span class="sxs-lookup"><span data-stu-id="eb8cf-110">In order to avoid having to implement text box display functionality again, the `CalendarCell` class derives from the <xref:System.Windows.Forms.DataGridViewTextBoxCell> class rather than inheriting the <xref:System.Windows.Forms.DataGridViewCell> class directly.</span></span>  
  
> [!NOTE]
> <span data-ttu-id="eb8cf-111">Wenn Sie aus <xref:System.Windows.Forms.DataGridViewCell> oder <xref:System.Windows.Forms.DataGridViewColumn> ableiten und der abgeleiteten Klasse neue Eigenschaften hinzufügen, müssen Sie die `Clone`-Methode überschreiben, damit die neuen Eigenschaften bei Klonvorgängen kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb8cf-111">When you derive from <xref:System.Windows.Forms.DataGridViewCell> or <xref:System.Windows.Forms.DataGridViewColumn> and add new properties to the derived class, be sure to override the `Clone` method to copy the new properties during cloning operations.</span></span> <span data-ttu-id="eb8cf-112">Außerdem sollten Sie die `Clone`-Methode der Basisklasse aufrufen, damit die Eigenschaften der Basisklasse in die neue Zelle oder Spalte kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb8cf-112">You should also call the base class's `Clone` method so that the properties of the base class are copied to the new cell or column.</span></span>  
  
## <a name="example"></a><span data-ttu-id="eb8cf-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="eb8cf-113">Example</span></span>  
 [!code-csharp[System.Windows.Forms.DataGridViewCalendarColumn#000](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCalendarColumn/CS/datagridviewcalendarcolumn.cs#000)]
 [!code-vb[System.Windows.Forms.DataGridViewCalendarColumn#000](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.DataGridViewCalendarColumn/VB/datagridviewcalendarcolumn.vb#000)]  
  
## <a name="compiling-the-code"></a><span data-ttu-id="eb8cf-114">Kompilieren des Codes</span><span class="sxs-lookup"><span data-stu-id="eb8cf-114">Compiling the Code</span></span>  
 <span data-ttu-id="eb8cf-115">Anforderungen für das folgende Beispiel:</span><span class="sxs-lookup"><span data-stu-id="eb8cf-115">The following example requires:</span></span>  
  
- <span data-ttu-id="eb8cf-116">Verweise auf die Assemblys "System" und "System.Windows.Forms".</span><span class="sxs-lookup"><span data-stu-id="eb8cf-116">References to the System and System.Windows.Forms assemblies.</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="eb8cf-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eb8cf-117">See also</span></span>

- <xref:System.Windows.Forms.DataGridView>
- <xref:System.Windows.Forms.DataGridViewColumn>
- <xref:System.Windows.Forms.DataGridViewCell>
- <xref:System.Windows.Forms.DataGridViewTextBoxCell>
- <xref:System.Windows.Forms.IDataGridViewEditingControl>
- <xref:System.Windows.Forms.DateTimePicker>
- [<span data-ttu-id="eb8cf-118">Anpassen des DataGridView-Steuerelements von Windows Forms</span><span class="sxs-lookup"><span data-stu-id="eb8cf-118">Customizing the Windows Forms DataGridView Control</span></span>](customizing-the-windows-forms-datagridview-control.md)
- [<span data-ttu-id="eb8cf-119">Architektur des DataGridView-Steuerelements</span><span class="sxs-lookup"><span data-stu-id="eb8cf-119">DataGridView Control Architecture</span></span>](datagridview-control-architecture-windows-forms.md)
- [<span data-ttu-id="eb8cf-120">Spaltentypen im DataGridView-Steuerelement in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="eb8cf-120">Column Types in the Windows Forms DataGridView Control</span></span>](column-types-in-the-windows-forms-datagridview-control.md)
