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
# <a name="overview-of-using-controls-windows-forms-net"></a>Übersicht über die Verwendung von Steuerelementen (Windows Forms .NET)

Windows Forms-Steuerelemente sind wiederverwendbare Komponenten, die Funktionen der Benutzeroberfläche einschließen und in clientseitigen Windows-basierten Anwendungen verwendet werden. Windows Forms stellt nicht nur viele einsatzbereite Steuerelemente bereit, sondern auch die Infrastruktur für die Entwicklung eigener Steuerelemente. Sie können vorhandene Steuerelemente kombinieren und erweitern oder eigene benutzerdefinierte Steuerelemente erstellen. Weitere Informationen finden Sie unter [Typen von benutzerdefinierten Steuerelementen](custom.md).

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="adding-controls"></a>Hinzufügen von Steuerelementen

Steuerelemente werden über den Visual Studio-Designer hinzugefügt. Mit dem Designer können Sie Steuerelemente platzieren, anpassen, ausrichten und verschieben. Alternativ können Steuerelemente über Code hinzugefügt werden. Weitere Informationen finden Sie unter [Hinzufügen eines Steuerelements (Windows Forms)](how-to-add-to-a-form.md).

## <a name="layout-options"></a>Layoutoptionen

Die Position, an der ein Steuerelement auf einem übergeordneten Element angezeigt wird, wird durch den Wert der <xref:System.Windows.Forms.Control.Location>-Eigenschaft relativ zum oberen linken Rand der übergeordneten Oberfläche bestimmt. `(x0,y0)` ist die obere linke Positionskoordinate im übergeordneten Element. Die Größe des Steuerelements wird durch die <xref:System.Windows.Forms.Control.Size>-Eigenschaft bestimmt. Sie gibt die Breite und Höhe des Steuerelements an.

Neben der manuellen Positionierung und Größenanpassung werden verschiedene Containersteuerelemente bereitgestellt, die bei der automatischen Platzierung von Steuerelementen helfen.

Weitere Informationen finden Sie unter [Position und Layout von Steuerelementen](layout.md).
<!-- TODO

## Control events

-->

## <a name="see-also"></a>Siehe auch

- [Position und Layout von Steuerelementen](layout.md)
- [Übersicht über das Label-Steuerelement (Windows Forms .NET)](labels.md)
- [Hinzufügen eines Steuerelements (Windows Forms .NET)](how-to-add-to-a-form.md)
