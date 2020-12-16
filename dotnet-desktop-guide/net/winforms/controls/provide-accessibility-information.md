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
# <a name="providing-accessibility-information-for-controls-windows-forms-net"></a>Bereitstellen von Informationen zur Barrierefreiheit für Steuerelemente (Windows Forms .NET)

Eingabehilfen sind spezielle Programme und Geräte, die es Personen mit Behinderungen ermöglichen, einen Computer effizienter zu nutzen. Beispiele hierfür sind Sprachausgaben für Blinde sowie Spracheingabe-Hilfsprogramme für Personen, die verbale Befehle geben, statt Maus oder Tastatur zu verwenden. Diese Eingabehilfen interagieren mit den Eingabehilfeeigenschaften, die von Windows Forms-Steuerelementen verfügbar gemacht werden. Diese Eigenschaften sind:

- <xref:System.Windows.Forms.AccessibleObject?displayProperty=fullName>
- <xref:System.Windows.Forms.Control.AccessibleDefaultActionDescription?displayProperty=fullName>
- <xref:System.Windows.Forms.Control.AccessibleDescription?displayProperty=fullName>
- <xref:System.Windows.Forms.Control.AccessibleName?displayProperty=fullName>
- <xref:System.Windows.Forms.AccessibleRole?displayProperty=fullName>

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="accessibilityobject-property"></a>AccessibilityObject-Eigenschaft

Diese schreibgeschützte Eigenschaft enthält eine Instanz der <xref:System.Windows.Forms.AccessibleObject> . Die `AccessibleObject`-Klasse implementiert die <xref:Accessibility.IAccessible>-Schnittstelle, die Informationen zur Beschreibung, Bildschirmposition, zu den Navigationsfähigkeiten und zum Wert des Steuerelements enthält. Der Entwickler legt diesen Wert fest, wenn das Steuerelement zum Formular hinzugefügt wird.

## <a name="accessibledefaultactiondescription-property"></a>AccessibleDefaultActionDescription-Eigenschaft

Diese Zeichenfolge beschreibt die Aktion des Steuerelements. Sie wird nicht im Eigenschaftenfenster angezeigt und kann nur in Code festgelegt werden. Im folgenden Beispiel wird die <xref:System.Windows.Forms.Control.AccessibleDefaultActionDescription>-Eigenschaft für ein Schaltflächen-Steuerelement festgelegt:

```vb
Button1.AccessibleDefaultActionDescription = "Closes the application."
```

```csharp
button1.AccessibleDefaultActionDescription = "Closes the application.";
```

## <a name="accessibledescription-property"></a>Control.AccessibleDescription-Eigenschaft

Diese Zeichenfolge beschreibt das Steuerelement. Die <xref:System.Windows.Forms.Control.AccessibleDescription>-Eigenschaft kann im Eigenschaftenfenster oder wie folgt in Code festgelegt werden:

```vb
Button1.AccessibleDescription = "A button with text 'Exit'."
```

```csharp
button1.AccessibleDescription = "A button with text 'Exit'";
```

## <a name="accessiblename-property"></a>Control.AccessibleName-Eigenschaft

Diese Eigenschaft enthält den Namen des Steuerelements, der an Eingabehilfen gemeldet wird. Die <xref:System.Windows.Forms.Control.AccessibleName>-Eigenschaft kann im Eigenschaftenfenster oder wie folgt in Code festgelegt werden:

```vb
Button1.AccessibleName = "Order"
```

```csharp
button1.AccessibleName = "Order";
```

## <a name="accessiblerole-property"></a>AccessibleRole-Eigenschaft

Diese Eigenschaft, die eine <xref:System.Windows.Forms.AccessibleRole> enthält, beschreibt die Rolle des Steuerelements in der Benutzeroberfläche. Bei einem neuen Steuerelement ist die Eigenschaft auf `Default` festgelegt. Dies bedeutet, dass sich ein `Button`-Steuerelement standardmäßig wie eine `Button`-Klasse verhält. Sie können diese Eigenschaft auf einen anderen Wert festlegen, wenn das jeweilige Steuerelement eine andere Rolle hat. Beispielsweise könnte es sein, dass Sie ein `PictureBox`-Steuerelement als `Chart` verwenden und Eingabehilfen die Rolle als `Chart` und nicht als `PictureBox` melden sollen. Es ist auch möglich, dass Sie diese Eigenschaft für benutzerdefinierte Steuerelemente angeben, die Sie entwickelt haben. Diese Eigenschaft kann im Eigenschaftenfenster oder wie folgt in Code festgelegt werden:

```vb
PictureBox1.AccessibleRole = AccessibleRole.Chart
```

```csharp
pictureBox1.AccessibleRole = AccessibleRole.Chart;
```

## <a name="see-also"></a>Siehe auch

- [Übersicht über das Label-Steuerelement (Windows Forms .NET)](labels.md)
- <xref:System.Windows.Forms.AccessibleObject>
- <xref:System.Windows.Forms.Control.AccessibilityObject?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleDefaultActionDescription?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleDescription?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleName?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Control.AccessibleRole?displayProperty=nameWithType>
- <xref:System.Windows.Forms.AccessibleRole>
