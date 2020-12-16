---
title: Arten von benutzerdefinierten Steuerelementen
description: In diesem Artikel erhalten Sie Informationen zu den verschiedenen Typen benutzerdefinierter Steuerelemente, die Sie in Windows Forms für .NET erstellen können.
ms.date: 10/26/2020
ms.topic: overview
f1_keywords:
- UserControl
helpviewer_keywords:
- controls [Windows Forms], user controls
- controls [Windows Forms], types of
- composite controls [Windows Forms]
- extended controls [Windows Forms]
- controls [Windows Forms], extended
- user controls [Windows Forms]
- custom controls [Windows Forms]
- controls [Windows Forms], composite
ms.openlocfilehash: 25430adf6efbb4c1f323496ce46cdea5aa0bb95c
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942086"
---
# <a name="types-of-custom-controls-windows-forms-net"></a>Arten von benutzerdefinierten Steuerelementen (Windows Forms .NET)

Mit Windows Forms können Sie neue Steuerelemente entwickeln und implementieren. Sie können ein neues Benutzersteuerelement erstellen, vorhandene Steuerelemente über Vererbung ändern und ein benutzerdefiniertes Steuerelement schreiben, das sich selbst zeichnet.

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

Es kann verwirrend sein, eine Entscheidung zu treffen, welche Art von Steuerelement erstellt werden soll. Dieser Artikel behandelt die Unterschiede zwischen verschiedenen Arten von Steuerelementen, von denen geerbt werden kann, und bietet Informationen über die Auswahl einer bestimmten Art von Steuerelement für Ihr Projekt.

<table>
<thead>
  <tr>
    <th>Szenario</th>
    <th>Lösung</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>
        <ul>
            <li>Sie möchten die Funktionalität mehrerer Windows Forms-Steuerelemente in einer einzigen wiederverwendbaren Einheit kombinieren.</li>
        </ul>
    </td>
    <td>Erstellen Sie ein <a href="#composite-controls">zusammengesetztes Steuerelement</a> durch Vererbung von <a href="/dotnet/api/system.windows.forms.usercontrol">System.Windows.Forms.UserControl</a>.</td>
  </tr>
  <tr>
    <td>
        <ul>
            <li>Ein Großteil der Funktionalität, die Sie benötigen, mit ist der Funktionalität eines vorhandenen Windows Forms-Steuerelements identisch.</li>
            <li>Sie benötigen keine benutzerdefinierte grafische Benutzeroberfläche, oder Sie möchten eine neue grafische Benutzeroberfläche für ein vorhandenes Steuerelement entwerfen.</li>
        </ul>
    </td>
    <td>Erstellen Sie ein <a href="#extended-controls">erweitertes Steuerelement</a> durch Vererbung von einem bestimmten Windows Forms-Steuerelement.</td>
  </tr>
  <tr>
    <td>
        <ul>
            <li>Sie möchten eine benutzerdefinierte grafische Darstellung Ihres Steuerelements bereitstellen.</li>
            <li>Sie müssen benutzerdefinierte Funktionalität implementieren, die über Standardsteuerelemente nicht verfügbar ist.</li>
        </ul>
    </td>
    <td>Erstellen Sie ein <a href="#custom-controls">benutzerdefiniertes Steuerelement</a> durch Vererbung von <a href="/dotnet/api/system.windows.forms.control">System.Windows.Forms.Control</a>.</td>
  </tr>
</tbody>
</table>

## <a name="base-control-class"></a>Control-Basisklasse

Die <xref:System.Windows.Forms.Control>-Klasse ist die Basisklasse für Windows Forms-Steuerelemente. Sie bietet die Infrastruktur, die für die grafische Darstellung in Windows Forms-Anwendungen benötigt wird, und die folgenden Funktionen:

- Macht ein Fensterhandle verfügbar.
- Verwaltet Meldungsrouting.
- Bietet Maus- und Tastaturereignisse und viele weitere Ereignisse der Benutzeroberfläche.
- Bietet erweiterte Layoutfunktionen.
- Die Klasse enthält viele für die grafische Darstellung spezifischen Eigenschaften wie <xref:System.Windows.Forms.Control.ForeColor%2A>, <xref:System.Windows.Forms.Control.BackColor%2A>, <xref:System.Windows.Forms.Control.Height%2A> und <xref:System.Windows.Forms.Control.Width%2A>.
- Bietet die notwendige Unterstützung für Sicherheit und Threading für ein Windows Forms-Steuerelement, um als Microsoft® ActiveX®-Steuerelement zu fungieren.

Da der Großteil der Infrastruktur von der Basisklasse bereitgestellt wird, ist es relativ einfach, Ihre eigenen Windows Forms-Steuerelemente zu entwickeln.

## <a name="composite-controls"></a>Zusammengesetzte Steuerelemente

Ein zusammengesetztes Steuerelement ist eine Sammlung von Windows Forms-Steuerelementen, die in einem gemeinsamen Container gekapselt sind. Diese Art von Steuerelement wird manchmal auch als *Benutzersteuerelement* bezeichnet. Die enthaltenen Steuerelemente werden *konstituierende Steuerelemente* genannt.

Ein zusammengesetztes Steuerelement enthält die gesamte Funktionalität, die in jedem der enthaltenen Windows Forms-Steuerelemente implementiert ist, und ermöglicht es Ihnen, deren Eigenschaften selektiv verfügbar zu machen und zu binden. Ein zusammengesetztes Steuerelement bietet auch hohe Funktionalität für die standardmäßige Tastaturbehandlung, sodass Sie keinen zusätzlichen Entwicklungsaufwand betreiben müssen.

Ein zusammengesetztes Steuerelement kann z.B. erstellt werden, um die Adressdaten von Kunden aus einer Datenbank anzuzeigen. Dieses Steuerelement würde ein <xref:System.Windows.Forms.DataGridView>-Steuerelement beinhalten, um die Datenbankfelder anzuzeigen, eine <xref:System.Windows.Forms.BindingSource>-Klasse zur Verarbeitung der Bindung an eine Datenquelle und ein <xref:System.Windows.Forms.BindingNavigator>-Steuerelement zur Navigation in den Datensätzen. Sie können Datenbindungseigenschaften selektiv verfügbar machen und das gesamte Steuerelement verpacken und von Anwendung zu Anwendung wiederverwenden.<!-- TODO For an example of this kind of composite control, see [How to: Apply Attributes in Windows Forms Controls](how-to-apply-attributes-in-windows-forms-controls.md).-->

Leiten Sie von der Klasse <xref:System.Windows.Forms.UserControl> ab, um ein zusammengesetztes Steuerelement zu erstellen. Die Basisklasse <xref:System.Windows.Forms.UserControl> ermöglicht Tastaturrouting für die untergeordneten Steuerelemente und stellt damit sicher, dass untergeordnete Steuerelemente als Gruppe arbeiten können.<!-- TODO For more information, see [Developing a Composite Windows Forms Control](developing-a-composite-windows-forms-control.md).-->

## <a name="extended-controls"></a>Erweiterte Steuerelemente

Sie können ein geerbtes Steuerelement aus jedem vorhandenen Windows Forms-Steuerelement ableiten. Diese Vorgehensweise ermöglicht es Ihnen, die in einem Windows Forms-Steuerelement implementierte Funktionalität zu übernehmen und diese Funktionalität dann durch Hinzufügen von benutzerdefinierten Eigenschaften, Methoden oder weiteren Features zu erweitern. Mit dieser Option können Sie die Farblogik des Basissteuerelements außer Kraft setzen und anschließend die Benutzeroberfläche durch Verändern des Aussehens erweitern.

Sie können z. B. ein von <xref:System.Windows.Forms.Button> abgeleitetes Steuerelement erstellen, das nachverfolgt, wie oft ein Benutzer darauf geklickt hat.

Bei einigen Steuerelementen können Sie auch eine benutzerdefinierte Darstellung der grafischen Benutzeroberfläche des Steuerelements hinzufügen, indem Sie die <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode der Basisklasse überschreiben. Für eine erweiterte Schaltfläche, die die Klicks nachverfolgt, können Sie die <xref:System.Windows.Forms.Control.OnPaint%2A>-Methode überschreiben, um die Basisimplementierung von <xref:System.Windows.Forms.Control.OnPaint%2A> aufzurufen, und dann den Klickzähler in einer Ecke des Clientbereichs des <xref:System.Windows.Forms.Button>-Steuerelements zeichnen.

## <a name="custom-controls"></a>Benutzerdefinierte Steuerelemente

Eine weitere Möglichkeit zum Erstellen eines Steuerelements besteht darin, ein Steuerelement von Grund auf neu zu erstellen, indem es von <xref:System.Windows.Forms.Control> erbt. Die Klasse <xref:System.Windows.Forms.Control> stellt die gesamte grundlegende Funktionalität bereit, die für Steuerelemente erforderlich ist, darunter Maus- und Tastaturbehandlungsereignisse, sie stellt aber weder für Steuerelemente spezifische Funktionalität noch eine grafische Oberfläche bereit.

Das Erstellen eines Steuerelement durch Erben von der <xref:System.Windows.Forms.Control>-Klasse erfordert viel mehr Überlegungen und Aufwand als ein Erben von <xref:System.Windows.Forms.UserControl> oder von einem vorhandenen Windows Forms-Steuerelement. Da ein Großteil der Implementierung Ihnen überlassen ist, hat Ihr Steuerelement größere Flexibilität als ein zusammengesetztes oder erweitertes Steuerelement, und Sie können Ihr Steuerelement exakt an Ihre Anforderungen anpassen.

Sie müssen Code für das <xref:System.Windows.Forms.Control.OnPaint%2A>-Ereignis des Steuerelements sowie featurespezifischen Code schreiben, um ein benutzerdefiniertes Steuerelement zu implementieren. Sie können auch die <xref:System.Windows.Forms.Control.WndProc%2A>-Methode überschreiben und Windows-Meldungen direkt verarbeiten. Dies ist die beste Möglichkeit, ein Steuerelement zu erstellen. Sie müssen allerdings mit der Microsoft Win32-API vertraut sein, um diese Technik effektiv einsetzen zu können.

Ein Beispiel für ein benutzerdefiniertes Steuerelement ist ein Uhren-Steuerelement, das das Erscheinungsbild und das Verhalten einer analogen Uhr dupliziert. Benutzerdefiniertes Zeichnen wird aufgerufen, um die Zeiger der Uhr als Reaktion auf <xref:System.Windows.Forms.Timer.Tick>-Ereignisse zu bewegen, die aus einer internen <xref:System.Windows.Forms.Timer>-Komponente stammen.<!-- TODO For more information, see [How to: Develop a Simple Windows Forms Control](how-to-develop-a-simple-windows-forms-control.md).-->

## <a name="activex-controls"></a>ActiveX-Steuerelemente

Obwohl die Windows Forms-Infrastruktur zum Hosten von Windows Forms-Steuerelementen optimiert wurde, können Sie weiterhin ActiveX-Steuerelemente verwenden. Visual Studio bietet Unterstützung für diese Aufgabe.<!-- TODO For more information, see [How to: Add ActiveX Controls to Windows Forms](how-to-add-activex-controls-to-windows-forms.md).-->

## <a name="windowless-controls"></a>Fensterlose Steuerelemente

Die Microsoft Visual Basic® 6.0- und ActiveX-Technologien unterstützen *fensterlose* Steuerelemente. Fensterlose Steuerelemente werden in Windows Forms nicht unterstützt.

## <a name="custom-design-experience"></a>Benutzerdefiniertes Entwurfserlebnis

Wenn Sie eine benutzerdefinierte Handhabung zur Entwurfszeit implementieren müssen, können Sie Ihren eigenen Designer erstellen. Leiten Sie für zusammengesetzte Steuerelemente Ihren benutzerdefinierten Designer von der Klasse <xref:System.Windows.Forms.Design.ParentControlDesigner> oder <xref:System.Windows.Forms.Design.DocumentDesigner> ab. Für erweiterte und benutzerdefinierte Steuerelemente leiten Sie Ihre benutzerdefinierte Designerklasse von der <xref:System.Windows.Forms.Design.ControlDesigner>-Klasse ab.

Verwenden Sie die Klasse <xref:System.ComponentModel.DesignerAttribute>, um Ihr Steuerelement Ihrem Designer zuzuordnen.

Die folgenden Informationen sind zwar nicht mehr aktuell, helfen Ihnen möglicherweise jedoch trotzdem.

- [Erweitern der Entwurfszeitunterstützung](/previous-versions/visualstudio/visual-studio-2013/37899azc(v=vs.120))
- [Vorgehensweise: Erstellen eines Windows Forms-Steuerelements, das Entwurfszeitfeatures nutzt](/previous-versions/visualstudio/visual-studio-2013/307hck25(v=vs.120))

## <a name="see-also"></a>Siehe auch

- [Übersicht über die Verwendung von Steuerelementen (Windows Forms .NET)](overview.md)

<!-- TODO: link to the ..\custom-controls\ content 

- [Developing Custom Windows Forms Controls](developing-custom-windows-forms-controls.md)
- [How to: Develop a Simple Windows Forms Control](how-to-develop-a-simple-windows-forms-control.md)
- [Developing a Composite Windows Forms Control](developing-a-composite-windows-forms-control.md)
-->
