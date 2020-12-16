---
title: Verwalten von Mauszeigern
description: Hier erfahren Sie, wie Sie in Windows Forms für .NET auf den Mauszeiger zugreifen, ihn steuern und ihn ändern.
ms.date: 10/26/2020
dev_langs:
- csharp
- vb
helpviewer_keywords:
- pointers [Windows Forms], setting
- mouse pointers
- mouse cursors
- mouse pointers [Windows Forms], setting
- cursors [Windows Forms], setting
- mouse [Windows Forms], cursors
ms.openlocfilehash: b4439c34bf7a7f41a94ce5ec5971520d9c82e469
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942098"
---
# <a name="manage-mouse-pointers-windows-forms-net"></a><span data-ttu-id="d6299-103">Verwalten von Mauszeigern (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="d6299-103">Manage mouse pointers (Windows Forms .NET)</span></span>

<span data-ttu-id="d6299-104">Beim *Mauszeiger*, der manchmal auch als Cursor bezeichnet wird, handelt es sich um eine Bitmap, die einen Fokuspunkt auf dem Bildschirm für Benutzereingabe mit der Maus angibt.</span><span class="sxs-lookup"><span data-stu-id="d6299-104">The mouse *pointer*, which is sometimes referred to as the cursor, is a bitmap that specifies a focus point on the screen for user input with the mouse.</span></span> <span data-ttu-id="d6299-105">In diesem Thema erhalten Sie eine Übersicht über den Mauszeiger in Windows Forms. Außerdem werden einige Möglichkeiten erläutert, um den Mauszeiger zu ändern und zu steuern.</span><span class="sxs-lookup"><span data-stu-id="d6299-105">This topic provides an overview of the mouse pointer in Windows Forms and describes some of the ways to modify and control the mouse pointer.</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="accessing-the-mouse-pointer"></a><span data-ttu-id="d6299-106">Zugreifen auf den Mauszeiger</span><span class="sxs-lookup"><span data-stu-id="d6299-106">Accessing the mouse pointer</span></span>

<span data-ttu-id="d6299-107">Der Mauszeiger wird von der <xref:System.Windows.Forms.Cursor>-Klasse dargestellt. Jede <xref:System.Windows.Forms.Control>-Klasse verfügt über eine <xref:System.Windows.Forms.Control.Cursor%2A?displayProperty=nameWithType>-Eigenschaft, die den Zeiger für das entsprechende Steuerelement angibt.</span><span class="sxs-lookup"><span data-stu-id="d6299-107">The mouse pointer is represented by the <xref:System.Windows.Forms.Cursor> class, and each <xref:System.Windows.Forms.Control> has a <xref:System.Windows.Forms.Control.Cursor%2A?displayProperty=nameWithType> property that specifies the pointer for that control.</span></span> <span data-ttu-id="d6299-108">Die <xref:System.Windows.Forms.Cursor>-Klasse enthält Eigenschaften, die den Zeiger beschreiben, z. B. die Eigenschaften <xref:System.Windows.Forms.Cursor.Position%2A> und <xref:System.Windows.Forms.Cursor.HotSpot%2A>, sowie Methoden, die das Aussehen des Zeigers ändern können, z. B. die Methoden <xref:System.Windows.Forms.Cursor.Show%2A>, <xref:System.Windows.Forms.Cursor.Hide%2A> und <xref:System.Windows.Forms.Cursor.DrawStretched%2A>.</span><span class="sxs-lookup"><span data-stu-id="d6299-108">The <xref:System.Windows.Forms.Cursor> class contains properties that describe the pointer, such as the <xref:System.Windows.Forms.Cursor.Position%2A> and <xref:System.Windows.Forms.Cursor.HotSpot%2A> properties, and methods that can modify the appearance of the pointer, such as the <xref:System.Windows.Forms.Cursor.Show%2A>, <xref:System.Windows.Forms.Cursor.Hide%2A>, and <xref:System.Windows.Forms.Cursor.DrawStretched%2A> methods.</span></span>

<span data-ttu-id="d6299-109">Im folgenden Beispiel wird der Cursor ausgeblendet, wenn er sich über einer Schaltfläche befindet:</span><span class="sxs-lookup"><span data-stu-id="d6299-109">The following example hides the cursor when the cursor is over a button:</span></span>

:::code language="csharp" source="snippets/how-to-manage-cursor-pointer/csharp/Form1.cs" id="ShowHideCursor":::
:::code language="vb" source="snippets/how-to-manage-cursor-pointer/vb/Form1.vb" id="ShowHideCursor":::

## <a name="controlling-the-mouse-pointer"></a><span data-ttu-id="d6299-110">Steuern des Mauszeigers</span><span class="sxs-lookup"><span data-stu-id="d6299-110">Controlling the mouse pointer</span></span>

<span data-ttu-id="d6299-111">Manchmal sollten Sie den Bereich begrenzen, in dem der Mauszeiger verwendet werden kann, oder die Position der Maus ändern.</span><span class="sxs-lookup"><span data-stu-id="d6299-111">Sometimes you may want to limit the area in which the mouse pointer can be used or change the position the mouse.</span></span> <span data-ttu-id="d6299-112">Sie können die aktuelle Position der Maus mithilfe der <xref:System.Windows.Forms.Cursor.Position%2A>-Eigenschaft von <xref:System.Windows.Forms.Cursor> abrufen oder festlegen.</span><span class="sxs-lookup"><span data-stu-id="d6299-112">You can get or set the current location of the mouse using the <xref:System.Windows.Forms.Cursor.Position%2A> property of the <xref:System.Windows.Forms.Cursor>.</span></span> <span data-ttu-id="d6299-113">Zusätzlich können Sie den Bereich einschränken, in dem der Mauszeiger verwendet werden kann, indem Sie die <xref:System.Windows.Forms.Cursor.Clip%2A>-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="d6299-113">In addition, you can limit the area the mouse pointer can be used be setting the <xref:System.Windows.Forms.Cursor.Clip%2A> property.</span></span> <span data-ttu-id="d6299-114">Der Standardbereich, der eingeschränkt werden kann, ist die gesamte Anzeige.</span><span class="sxs-lookup"><span data-stu-id="d6299-114">The clip area, by default, is the entire screen.</span></span>

<span data-ttu-id="d6299-115">Im folgenden Beispiel wird der Mauszeiger zwischen zwei Schaltflächen positioniert, wenn auf diese geklickt wird:</span><span class="sxs-lookup"><span data-stu-id="d6299-115">The following example positions the mouse pointer between two buttons when they are clicked:</span></span>

:::code language="csharp" source="snippets/how-to-manage-cursor-pointer/csharp/Form1.cs" id="MoveCursor":::
:::code language="vb" source="snippets/how-to-manage-cursor-pointer/vb/Form1.vb" id="MoveCursor":::

## <a name="changing-the-mouse-pointer"></a><span data-ttu-id="d6299-116">Ändern des Mauszeigers</span><span class="sxs-lookup"><span data-stu-id="d6299-116">Changing the mouse pointer</span></span>

<span data-ttu-id="d6299-117">Das Ändern des Mauszeigers ist eine wichtige Möglichkeit, dem Benutzer Feedback zu geben.</span><span class="sxs-lookup"><span data-stu-id="d6299-117">Changing the mouse pointer is an important way of providing feedback to the user.</span></span> <span data-ttu-id="d6299-118">Der Mauszeiger kann beispielsweise in den Handlern der Ereignisse <xref:System.Windows.Forms.Control.MouseEnter> und <xref:System.Windows.Forms.Control.MouseLeave> geändert werden, um den Benutzer darüber zu informieren, dass Berechnungen durchgeführt werden, und um die Benutzerinteraktion im Steuerelement einzuschränken.</span><span class="sxs-lookup"><span data-stu-id="d6299-118">For example, the mouse pointer can be modified in the handlers of the <xref:System.Windows.Forms.Control.MouseEnter> and <xref:System.Windows.Forms.Control.MouseLeave> events to tell the user that computations are occurring and to limit user interaction in the control.</span></span> <span data-ttu-id="d6299-119">Manchmal wird der Mauszeiger aufgrund von Systemereignissen geändert, z. B. wenn Ihre Anwendung an einem Drag & Drop-Vorgang beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="d6299-119">Sometimes, the mouse pointer will change because of system events, such as when your application is involved in a drag-and-drop operation.</span></span>

<span data-ttu-id="d6299-120">Die Hauptmöglichkeit, den Mauszeiger zu ändern, besteht darin, die Eigenschaft <xref:System.Windows.Forms.Control.Cursor%2A?displayProperty=nameWithType> oder <xref:System.Windows.Forms.Control.DefaultCursor%2A> eines Steuerelements auf eine neue <xref:System.Windows.Forms.Cursor>-Klasse festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d6299-120">The primary way to change the mouse pointer is by setting the <xref:System.Windows.Forms.Control.Cursor%2A?displayProperty=nameWithType> or <xref:System.Windows.Forms.Control.DefaultCursor%2A> property of a control to a new <xref:System.Windows.Forms.Cursor>.</span></span> <span data-ttu-id="d6299-121">Beispiele zum Ändern des Mauszeigers finden Sie im Codebeispiel in der <xref:System.Windows.Forms.Cursor>-Klasse.</span><span class="sxs-lookup"><span data-stu-id="d6299-121">For examples of changing the mouse pointer, see the code example in the <xref:System.Windows.Forms.Cursor> class.</span></span> <span data-ttu-id="d6299-122">Zusätzlich macht die <xref:System.Windows.Forms.Cursors>-Klasse mehrere <xref:System.Windows.Forms.Cursor>-Objekte für verschiedene Zeigertypen verfügbar, z. B. ein Zeiger, der einer Hand ähnelt.</span><span class="sxs-lookup"><span data-stu-id="d6299-122">In addition, the <xref:System.Windows.Forms.Cursors> class exposes a set of <xref:System.Windows.Forms.Cursor> objects for many different types of pointers, such as a pointer that resembles a hand.</span></span>

<span data-ttu-id="d6299-123">Im folgenden Beispiel wird der Cursor des Mauszeigers für eine Schaltfläche in eine Hand geändert:</span><span class="sxs-lookup"><span data-stu-id="d6299-123">The following example changes the cursor of the mouse pointer for a button to a hand:</span></span>

:::code language="csharp" source="snippets/how-to-manage-cursor-pointer/csharp/Form1.cs" id="SetControlCursor":::
:::code language="vb" source="snippets/how-to-manage-cursor-pointer/vb/Form1.vb" id="SetControlCursor":::

<span data-ttu-id="d6299-124">Verwenden Sie die <xref:System.Windows.Forms.Control.UseWaitCursor%2A>-Eigenschaft der <xref:System.Windows.Forms.Control>-Klasse, damit der Wartezeiger angezeigt wird, der einer Sanduhr ähnelt, sobald sich der Mauszeiger auf dem Steuerelement befindet.</span><span class="sxs-lookup"><span data-stu-id="d6299-124">To display the wait pointer, which resembles an hourglass, whenever the mouse pointer is on the control, use the <xref:System.Windows.Forms.Control.UseWaitCursor%2A> property of the <xref:System.Windows.Forms.Control> class.</span></span>

## <a name="see-also"></a><span data-ttu-id="d6299-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6299-125">See also</span></span>

- [<span data-ttu-id="d6299-126">Übersicht über die Mausverwendung (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="d6299-126">Overview of using the mouse (Windows Forms .NET)</span></span>](overview.md)
- [<span data-ttu-id="d6299-127">Verwenden von Mausereignissen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="d6299-127">Using mouse events (Windows Forms .NET)</span></span>](events.md)
- [<span data-ttu-id="d6299-128">Unterscheiden zwischen Klicks und Doppelklicks (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="d6299-128">How to distinguish between clicks and double-clicks (Windows Forms .NET)</span></span>](how-to-distinguish-between-clicks-and-double-clicks.md)
- [<span data-ttu-id="d6299-129">Simulieren von Mausereignissen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="d6299-129">How to simulate mouse events (Windows Forms .NET)</span></span>](how-to-simulate-events.md)
- <xref:System.Windows.Forms.Cursor?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Cursor.Position%2A?displayProperty=nameWithType>
