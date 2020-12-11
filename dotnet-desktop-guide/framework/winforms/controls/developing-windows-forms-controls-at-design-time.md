---
title: Entwickeln von Steuerelementen zur Entwurfszeit
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls [Windows Forms]
- Windows Forms controls, creating
- controls [Windows Forms]
- controls [Windows Forms], creating
- user controls [Windows Forms]
- custom controls [Windows Forms]
ms.assetid: e5a8e088-7ec8-4fd9-bcb3-9078fd134829
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: 4e192983c5818ddb81ed4581d91ae61375bb808e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972122"
---
# <a name="develop-windows-forms-controls-at-design-time"></a>Entwickeln von Windows Forms-Steuerelementen zur Entwurfszeit

NET Framework bietet Autoren von Steuerelementen eine Fülle von Technologien zum Erstellen von Steuerelementen. Autoren sind nicht mehr darauf beschränkt, zusammengesetzte Steuerelemente zu entwerfen, die als Auflistung bereits vorhandener Steuerelemente verwendet werden. Durch Vererbung können Sie eigene Steuerelemente aus bereits vorhandenen zusammengesetzten Steuerelementen bzw. bereits vorhandenen Windows Forms-Steuerelementen erstellen. Sie können auch eigene Steuerelemente entwerfen, durch die das benutzerdefinierte Zeichnen implementiert wird. Dank dieser Möglichkeiten zeichnen sich sowohl die Entwurfsfeatures als auch die Funktionalität der grafischen Oberfläche durch eine hohe Flexibilität aus. Um die Vorteile dieser Features nutzen zu können, sollten Sie mit den Konzepten der objektbasierten Programmierung vertraut sein.

> [!NOTE]
> Es ist nicht erforderlich, ein umfassendes Verständnis der Vererbung zu haben, aber Sie finden es möglicherweise hilfreich, wenn Sie auf [Grundlagen der Vererbung (Visual Basic)](/dotnet/visual-basic/programming-guide/language-features/objects-and-classes/inheritance-basics)verweisen.

Informationen zum Erstellen benutzerdefinierter Steuerelemente zur Verwendung in Web Forms finden Sie unter [Entwickeln von benutzerdefinierten ASP.NET-Serversteuerelementen](/previous-versions/aspnet/zt27tfhy(v=vs.100)).

## <a name="in-this-section"></a>In diesem Abschnitt

[Exemplarische Vorgehensweise: Erstellen eines zusammengesetzten Steuer Elements](walkthrough-authoring-a-composite-control-with-visual-csharp.md)\
Veranschaulicht das Erstellen eines einfachen zusammengesetzten Steuerelements in Visual C#.

[Exemplarische Vorgehensweise: Vererben von einem Windows Forms-Steuerelement](walkthrough-inheriting-from-a-windows-forms-control-with-visual-csharp.md)\
Veranschaulicht, wie ein einfaches Windows Forms-Steuerelement unter Verwendung der Vererbung in Visual C# erstellt wird.

[Exemplarische Vorgehensweise: Ausführen allgemeiner Aufgaben mit Designaktionen](perform-common-tasks-design-actions.md)\
Veranschaulicht, wie das Smarttagfeature auf Windows Forms-Steuerelemente angewendet wird.

[Exemplarische Vorgehensweise: Serialisieren von Auflistungen von Standard Typen mit dem DesignerSerializationVisibilityAttribute](serializing-collections-designerserializationvisibilityattribute.md)\
Zeigt, wie das- <xref:System.ComponentModel.DesignerSerializationVisibilityAttribute.Content?displayProperty=nameWithType> Attribut verwendet wird, um eine Auflistung zu serialisieren.

[Exemplarische Vorgehensweise: Debuggen von benutzerdefinierten Windows Forms-Steuerelementen](walkthrough-debugging-custom-windows-forms-controls-at-design-time.md)\
Veranschaulicht das Debuggen des Verhaltens eines Windows Forms-Steuerelements zur Entwurfszeit.

[Exemplarische Vorgehensweise: Erstellen eines Windows Forms-Steuer Elements, das Visual Studio-Design-Time Features nutzt](creating-a-wf-control-design-time-features.md)\
Zeigt, wie ein zusammengesetztes Steuerelement nahtlos in die Entwurfsumgebung integriert wird.

[Gewusst wie: Erstellen von Steuerelementen für Windows Forms](how-to-author-controls-for-windows-forms.md)\
Bietet einen Überblick über die Aspekte der Implementierung eines Windows Forms-Steuerelements.

[Gewusst wie: Erstellen von zusammengesetzten Steuerelementen](how-to-author-composite-controls.md)\
Veranschaulicht, wie ein Steuerelement durch Vererbung von einem zusammengesetzten Steuerelement erstellt wird.

[Gewusst wie: Erben von der UserControl-Klasse](how-to-inherit-from-the-usercontrol-class.md)\
Bietet eine Übersicht über das Verfahren zum Erstellen eines zusammengesetzten Steuerelements.

[Gewusst wie: Erben von vorhandenen Windows Forms Steuerelementen](how-to-inherit-from-existing-windows-forms-controls.md)\
Zeigt, wie ein erweitertes Steuerelement durch Erben von der Control-Klasse erstellt wird <xref:System.Windows.Forms.Button> .

[Gewusst wie: Erben von der Control-Klasse](how-to-inherit-from-the-control-class.md)\
Bietet eine Übersicht über das Erstellen eines erweiterten Steuerelements.

[Gewusst wie: Ausrichten eines Steuer Elements an den Kanten von Formularen zur Entwurfszeit](how-to-align-a-control-to-the-edges-of-forms-at-design-time.md)\
Zeigt, wie Sie die- <xref:System.Windows.Forms.Control.Dock%2A> Eigenschaft verwenden, um das Steuerelement an der Kante des Formulars auszurichten, das es einnimmt.

[Gewusst wie: Anzeigen eines Steuer Elements im Dialog Feld "Toolbox Elemente auswählen"](how-to-display-a-control-in-the-choose-toolbox-items-dialog-box.md)\
Veranschaulicht das Verfahren, in dem das Steuerelement so installiert wird, dass es im Dialogfeld **Toolbox anpassen** angezeigt wird.

[Gewusst wie: Bereitstellen einer Toolbox Bitmap für ein Steuerelement](how-to-provide-a-toolbox-bitmap-for-a-control.md)\
Zeigt, wie das verwendet wird <xref:System.Drawing.ToolboxBitmapAttribute> , um ein Symbol neben dem benutzerdefinierten Steuerelement in der **Toolbox** anzuzeigen.

[Vorgehensweise: Testen des Run-Time Verhaltens eines UserControl-Steuer Elements](how-to-test-the-run-time-behavior-of-a-usercontrol.md)\
Veranschaulicht, wie der **UserControl-Testcontainer** verwendet wird, um das Verhalten eines zusammengesetzten Steuerelements zu testen.

[Entwurfs Zeitfehler im Windows Forms-Designer](design-time-errors-in-the-windows-forms-designer.md)\
Erläutert die Bedeutung und den Verwendungszweck der Entwurfszeitfehlerliste, die in Microsoft Visual Studio angezeigt wird, wenn der Windows Forms-Designer nicht geladen werden kann.

[Problembehandlung bei der Steuerung und Komponenten Erstellung](troubleshooting-control-and-component-authoring.md)\
Veranschaulicht, wie häufige Probleme diagnostiziert und behoben werden, die beim Erstellen einer benutzerdefinierten Komponente bzw. eines benutzerdefinierten Steuerelements auftreten können.

## <a name="reference"></a>Verweis

- <xref:System.Windows.Forms.Control?displayProperty=nameWithType>

- <xref:System.Windows.Forms.UserControl?displayProperty=nameWithType>

## <a name="related-sections"></a>Verwandte Abschnitte

[Entwickeln von benutzerdefinierten Windows Forms-Steuerelementen mit dem .NET Framework](developing-custom-windows-forms-controls.md)\
Erörtert, wie Sie mit .NET Framework eigene benutzerdefinierte Steuerelemente erstellen können.

[Sprachunabhängigkeit und Language-Independent Komponenten](/dotnet/standard/language-independence-and-language-independent-components)\
Bietet eine Einführung in die Common Language Runtime, die zum Vereinfachen der Erstellung und Verwendung von Komponenten entworfen wurde. Ein wichtiger Aspekt dieser Vereinfachung ist die verbesserte Interoperabilität zwischen Komponenten, die mit verschiedenen Programmiersprachen geschrieben wurden. Durch die Common Language Specification (CLS) wird das Erstellen von Tools und Komponenten ermöglicht, die für mehrere Programmiersprachen ausgelegt sind.

[Exemplarische Vorgehensweise: Automatisches Auffüllen der Toolbox mit benutzerdefinierten Komponenten](walkthrough-automatically-populating-the-toolbox-with-custom-components.md)\
Erläutert, wie Sie vorgehen müssen, damit eine Komponente oder ein Steuerelement im Dialogfeld **Toolbox anpassen** angezeigt wird.
