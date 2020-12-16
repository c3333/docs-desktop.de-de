---
title: Übersicht über die Verwendung von Steuerelementen
description: Hier erfahren Sie mehr über die Verwendung von Steuerelementen in Windows Forms für .NET. Steuerelemente sind wiederverwendbare Komponenten, die dem Benutzer eine bestimmte Funktionalität bieten. Es werden viele sofort einsatzbereite Steuerelemente bereitgestellt. Sie können auch neue Steuerelemente erstellen.
ms.date: 10/26/2020
ms.topic: overview
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Windows Forms, controls
- controls [Windows Forms]
- custom controls [Windows Forms]
ms.openlocfilehash: 7476ce47a1767a2ab13c25a7408f5861014e7de8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942117"
---
# <a name="overview-of-using-controls-windows-forms-net"></a><span data-ttu-id="0edae-106">Übersicht über die Verwendung von Steuerelementen (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="0edae-106">Overview of using controls (Windows Forms .NET)</span></span>

<span data-ttu-id="0edae-107">Windows Forms-Steuerelemente sind wiederverwendbare Komponenten, die Funktionen der Benutzeroberfläche einschließen und in clientseitigen Windows-basierten Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0edae-107">Windows Forms controls are reusable components that encapsulate user interface functionality and are used in client-side, Windows-based applications.</span></span> <span data-ttu-id="0edae-108">Windows Forms stellt nicht nur viele einsatzbereite Steuerelemente bereit, sondern auch die Infrastruktur für die Entwicklung eigener Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="0edae-108">Not only does Windows Forms provide many ready-to-use controls, it also provides the infrastructure for developing your own controls.</span></span> <span data-ttu-id="0edae-109">Sie können vorhandene Steuerelemente kombinieren und erweitern oder eigene benutzerdefinierte Steuerelemente erstellen.</span><span class="sxs-lookup"><span data-stu-id="0edae-109">You can combine existing controls, extend existing controls, or author your own custom controls.</span></span> <span data-ttu-id="0edae-110">Weitere Informationen finden Sie unter [Typen von benutzerdefinierten Steuerelementen](custom.md).</span><span class="sxs-lookup"><span data-stu-id="0edae-110">For more information, see [Types of custom controls](custom.md).</span></span>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="adding-controls"></a><span data-ttu-id="0edae-111">Hinzufügen von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="0edae-111">Adding controls</span></span>

<span data-ttu-id="0edae-112">Steuerelemente werden über den Visual Studio-Designer hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0edae-112">Controls are added through the Visual Studio Designer.</span></span> <span data-ttu-id="0edae-113">Mit dem Designer können Sie Steuerelemente platzieren, anpassen, ausrichten und verschieben.</span><span class="sxs-lookup"><span data-stu-id="0edae-113">With the Designer, you can place, size, align, and move controls.</span></span> <span data-ttu-id="0edae-114">Alternativ können Steuerelemente über Code hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0edae-114">Alternatively, controls can be added through code.</span></span> <span data-ttu-id="0edae-115">Weitere Informationen finden Sie unter [Hinzufügen eines Steuerelements (Windows Forms)](how-to-add-to-a-form.md).</span><span class="sxs-lookup"><span data-stu-id="0edae-115">For more information, see [Add a control (Windows Forms)](how-to-add-to-a-form.md).</span></span>

## <a name="layout-options"></a><span data-ttu-id="0edae-116">Layoutoptionen</span><span class="sxs-lookup"><span data-stu-id="0edae-116">Layout options</span></span>

<span data-ttu-id="0edae-117">Die Position, an der ein Steuerelement auf einem übergeordneten Element angezeigt wird, wird durch den Wert der <xref:System.Windows.Forms.Control.Location>-Eigenschaft relativ zum oberen linken Rand der übergeordneten Oberfläche bestimmt.</span><span class="sxs-lookup"><span data-stu-id="0edae-117">The position a control appears on a parent is determined by the value of the <xref:System.Windows.Forms.Control.Location> property relative to the top-left of the parent surface.</span></span> <span data-ttu-id="0edae-118">`(x0,y0)` ist die obere linke Positionskoordinate im übergeordneten Element.</span><span class="sxs-lookup"><span data-stu-id="0edae-118">The top-left position coordinate in the parent is `(x0,y0)`.</span></span> <span data-ttu-id="0edae-119">Die Größe des Steuerelements wird durch die <xref:System.Windows.Forms.Control.Size>-Eigenschaft bestimmt. Sie gibt die Breite und Höhe des Steuerelements an.</span><span class="sxs-lookup"><span data-stu-id="0edae-119">The size of the control is determined by the <xref:System.Windows.Forms.Control.Size> property and represents the width and height of the control.</span></span>

<span data-ttu-id="0edae-120">Neben der manuellen Positionierung und Größenanpassung werden verschiedene Containersteuerelemente bereitgestellt, die bei der automatischen Platzierung von Steuerelementen helfen.</span><span class="sxs-lookup"><span data-stu-id="0edae-120">Besides manual positioning and sizing, various container controls are provided that help with automatic placement of controls.</span></span>

<span data-ttu-id="0edae-121">Weitere Informationen finden Sie unter [Position und Layout von Steuerelementen](layout.md).</span><span class="sxs-lookup"><span data-stu-id="0edae-121">For more information, see [Position and layout of controls](layout.md).</span></span>
<!-- TODO

## Control events

-->

## <a name="see-also"></a><span data-ttu-id="0edae-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0edae-122">See also</span></span>

- [<span data-ttu-id="0edae-123">Position und Layout von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="0edae-123">Position and layout of controls</span></span>](layout.md)
- [<span data-ttu-id="0edae-124">Übersicht über das Label-Steuerelement (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="0edae-124">Label control overview (Windows Forms .NET)</span></span>](labels.md)
- [<span data-ttu-id="0edae-125">Hinzufügen eines Steuerelements (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="0edae-125">Add a control (Windows Forms .NET)</span></span>](how-to-add-to-a-form.md)
