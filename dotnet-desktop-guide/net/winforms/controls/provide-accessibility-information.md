---
title: Informationen über Eingabehilfen für Steuerelemente in Windows Forms
description: Hier erfahren Sie, wie Sie einem Steuerelement Informationen zur Barrierefreiheit hinzufügen. Mit Windows Forms können Sie einem Steuerelement Barrierefreiheitseinstellungen hinzufügen, um Menschen mit Behinderungen Unterstützung zu bieten.
ms.date: 10/26/2020
helpviewer_keywords:
- Windows Forms controls, accessibility
- controls [Windows Forms], accessibility
- accessibility [Windows Forms], Windows Forms controls
dev_langs:
- csharp
- vb
ms.openlocfilehash: 27c06a7d01cb98ecb2f7216c09dc292d2fe68a6f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942116"
---
# <a name="providing-accessibility-information-for-controls-windows-forms-net"></a><span data-ttu-id="38b0f-104">Bereitstellen von Informationen zur Barrierefreiheit für Steuerelemente (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="38b0f-104">Providing Accessibility Information for Controls (Windows Forms .NET)</span></span>

<span data-ttu-id="38b0f-105">Eingabehilfen sind spezielle Programme und Geräte, die es Personen mit Behinderungen ermöglichen, einen Computer effizienter zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="38b0f-105">Accessibility aids are specialized programs and devices that help people with disabilities use computers more effectively.</span></span> <span data-ttu-id="38b0f-106">Beispiele hierfür sind Sprachausgaben für Blinde sowie Spracheingabe-Hilfsprogramme für Personen, die verbale Befehle geben, statt Maus oder Tastatur zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="38b0f-106">Examples include screen readers for people who are blind and voice input utilities for people who provide verbal commands instead of using the mouse or keyboard.</span></span> <span data-ttu-id="38b0f-107">Diese Eingabehilfen interagieren mit den Eingabehilfeeigenschaften, die von Windows Forms-Steuerelementen verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="38b0f-107">These accessibility aids interact with the accessibility properties exposed by Windows Forms controls.</span></span> <span data-ttu-id="38b0f-108">Diese Eigenschaften sind:</span><span class="sxs-lookup"><span data-stu-id="38b0f-108">These properties are:</span></span>

- <xref:System.Windows.Forms.AccessibleObject?displayProperty=fullName>
- <xref:System.Windows.Forms.Control.AccessibleDefaultActionDescription?displayProperty=fullName>
- <xref:System.Windows.Forms.Control.AccessibleDescription?displayProperty=fullName>
- <xref:System.Windows.Forms.Control.AccessibleName?displayProperty=fullName>
- <xref:System.Windows.Forms.AccessibleRole?displayProperty=fullName>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="accessibilityobject-property"></a><span data-ttu-id="38b0f-109">AccessibilityObject-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="38b0f-109">AccessibilityObject Property</span></span>

<span data-ttu-id="38b0f-110">Diese schreibgeschützte Eigenschaft enthält eine Instanz der <xref:System.Windows.Forms.AccessibleObject> .</span><span class="sxs-lookup"><span data-stu-id="38b0f-110">This read-only property contains an <xref:System.Windows.Forms.AccessibleObject> instance.</span></span> <span data-ttu-id="38b0f-111">Die `AccessibleObject`-Klasse implementiert die <xref:Accessibility.IAccessible>-Schnittstelle, die Informationen zur Beschreibung, Bildschirmposition, zu den Navigationsfähigkeiten und zum Wert des Steuerelements enthält.</span><span class="sxs-lookup"><span data-stu-id="38b0f-111">The `AccessibleObject` implements the <xref:Accessibility.IAccessible> interface, which provides information about the control's description, screen location, navigational abilities, and value.</span></span> <span data-ttu-id="38b0f-112">Der Entwickler legt diesen Wert fest, wenn das Steuerelement zum Formular hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="38b0f-112">The designer sets this value when the control is added to the form.</span></span>

## <a name="accessibledefaultactiondescription-property"></a><span data-ttu-id="38b0f-113">AccessibleDefaultActionDescription-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="38b0f-113">AccessibleDefaultActionDescription Property</span></span>

<span data-ttu-id="38b0f-114">Diese Zeichenfolge beschreibt die Aktion des Steuerelements.</span><span class="sxs-lookup"><span data-stu-id="38b0f-114">This string describes the action of the control.</span></span> <span data-ttu-id="38b0f-115">Sie wird nicht im Eigenschaftenfenster angezeigt und kann nur in Code festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="38b0f-115">It does not appear in the Properties window and may only be set in code.</span></span> <span data-ttu-id="38b0f-116">Im folgenden Beispiel wird die <xref:System.Windows.Forms.Control.AccessibleDefaultActionDescription>-Eigenschaft für ein Schaltflächen-Steuerelement festgelegt:</span><span class="sxs-lookup"><span data-stu-id="38b0f-116">The following example sets the <xref:System.Windows.Forms.Control.AccessibleDefaultActionDescription> property for a button control:</span></span>

```vb
Button1.AccessibleDefaultActionDescription = "Closes the application."
```

```csharp
button1.AccessibleDefaultActionDescription = "Closes the application.";
```

## <a name="accessibledescription-property"></a><span data-ttu-id="38b0f-117">Control.AccessibleDescription-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="38b0f-117">AccessibleDescription Property</span></span>

<span data-ttu-id="38b0f-118">Diese Zeichenfolge beschreibt das Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="38b0f-118">This string describes the control.</span></span> <span data-ttu-id="38b0f-119">Die <xref:System.Windows.Forms.Control.AccessibleDescription>-Eigenschaft kann im Eigenschaftenfenster oder wie folgt in Code festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="38b0f-119">The <xref:System.Windows.Forms.Control.AccessibleDescription> property may be set in the Properties window, or in code as follows:</span></span>

```vb
Button1.AccessibleDescription = "A button with text 'Exit'."
```

```csharp
button1.AccessibleDescription = "A button with text 'Exit'";
```

## <a name="accessiblename-property"></a><span data-ttu-id="38b0f-120">Control.AccessibleName-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="38b0f-120">AccessibleName Property</span></span>

<span data-ttu-id="38b0f-121">Diese Eigenschaft enthält den Namen des Steuerelements, der an Eingabehilfen gemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="38b0f-121">This is the name of a control reported to accessibility aids.</span></span> <span data-ttu-id="38b0f-122">Die <xref:System.Windows.Forms.Control.AccessibleName>-Eigenschaft kann im Eigenschaftenfenster oder wie folgt in Code festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="38b0f-122">The <xref:System.Windows.Forms.Control.AccessibleName> property may be set in the Properties window, or in code as follows:</span></span>

```vb
Button1.AccessibleName = "Order"
```

```csharp
button1.AccessibleName = "Order";
```

## <a name="accessiblerole-property"></a><span data-ttu-id="38b0f-123">AccessibleRole-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="38b0f-123">AccessibleRole Property</span></span>

<span data-ttu-id="38b0f-124">Diese Eigenschaft, die eine <xref:System.Windows.Forms.AccessibleRole> enthält, beschreibt die Rolle des Steuerelements in der Benutzeroberfläche.</span><span class="sxs-lookup"><span data-stu-id="38b0f-124">This property, which contains an <xref:System.Windows.Forms.AccessibleRole> enumeration, describes the user interface role of the control.</span></span> <span data-ttu-id="38b0f-125">Bei einem neuen Steuerelement ist die Eigenschaft auf `Default` festgelegt.</span><span class="sxs-lookup"><span data-stu-id="38b0f-125">A new control has the value set to `Default`.</span></span> <span data-ttu-id="38b0f-126">Dies bedeutet, dass sich ein `Button`-Steuerelement standardmäßig wie eine `Button`-Klasse verhält.</span><span class="sxs-lookup"><span data-stu-id="38b0f-126">This would mean that by default, a `Button` control acts as a `Button`.</span></span> <span data-ttu-id="38b0f-127">Sie können diese Eigenschaft auf einen anderen Wert festlegen, wenn das jeweilige Steuerelement eine andere Rolle hat.</span><span class="sxs-lookup"><span data-stu-id="38b0f-127">You may want to reset this property if a control has another role.</span></span> <span data-ttu-id="38b0f-128">Beispielsweise könnte es sein, dass Sie ein `PictureBox`-Steuerelement als `Chart` verwenden und Eingabehilfen die Rolle als `Chart` und nicht als `PictureBox` melden sollen.</span><span class="sxs-lookup"><span data-stu-id="38b0f-128">For example, you may be using a `PictureBox` control as a `Chart`, and you may want accessibility aids to report the role as a `Chart`, not as a `PictureBox`.</span></span> <span data-ttu-id="38b0f-129">Es ist auch möglich, dass Sie diese Eigenschaft für benutzerdefinierte Steuerelemente angeben, die Sie entwickelt haben.</span><span class="sxs-lookup"><span data-stu-id="38b0f-129">You may also want to specify this property for custom controls you have developed.</span></span> <span data-ttu-id="38b0f-130">Diese Eigenschaft kann im Eigenschaftenfenster oder wie folgt in Code festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="38b0f-130">This property may be set in the Properties window, or in code as follows:</span></span>

```vb
PictureBox1.AccessibleRole = AccessibleRole.Chart
```

```csharp
pictureBox1.AccessibleRole = AccessibleRole.Chart;
```

## <a name="see-also"></a><span data-ttu-id="38b0f-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38b0f-131">See also</span></span>

- [<span data-ttu-id="38b0f-132">Übersicht über das Label-Steuerelement (Windows Forms .NET)</span><span class="sxs-lookup"><span data-stu-id="38b0f-132">Label control overview (Windows Forms .NET)</span></span>](labels.md)
- <xref:System.Windows.Forms.AccessibleObject>
- <xref:System.Windows.Forms.Control.AccessibilityObject?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleDefaultActionDescription?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleDescription?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleName?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleRole?displayProperty=nameWithType>
- <xref:System.Windows.Forms.AccessibleRole>
