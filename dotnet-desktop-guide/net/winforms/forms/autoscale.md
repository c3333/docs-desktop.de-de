---
title: Automatische Formularskalierung
description: In diesem Artikel wird erläutert, wie Windows Forms für .NET die Skalierung der Benutzeroberfläche verarbeitet.
ms.date: 10/26/2020
ms.topic: overview
helpviewer_keywords:
- scalability [Windows Forms], automatic in Windows Forms
- Windows Forms, automatic scaling
ms.openlocfilehash: c414575c83723dc1930a0bfe298534eee9aa48c8
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96942126"
---
# <a name="automatic-scaling-windows-forms-net"></a>Automatische Skalierung (Windows Forms .NET)

Die automatische Skalierung ermöglicht, dass ein Formular und seine Steuerelemente, die auf einem Computer mit einer bestimmten Bildschirmauflösung oder Schriftart entworfen wurden, ordnungsgemäß auf einem anderen Computer angezeigt werden, der eine andere Bildschirmauflösung oder Schriftart hat. Durch sie wird sichergestellt, dass die Größen des Formulars und seiner Steuerelemente intelligent geändert werden, sodass diese sowohl auf den Computern von Benutzern als auch auf denen von anderen Entwicklern konsistent zu systemeigenen Fenstern sowie anderen Anwendungen sind. Die automatische Skalierung und visuelle Stile ermöglichen Windows Forms-Anwendungen im Vergleich zu nativen Windows-Anwendungen ein konsistentes Aussehen und Verhalten auf dem Computer jedes Benutzers.

Im Wesentlichen funktioniert die automatische Skalierung in Windows Forms wie erwartet. Änderungen des Schriftartenschemas können jedoch problematisch sein.<!-- TODO For an example of how to resolve this, see [How to: Respond to Font Scheme Changes in a Windows Forms Application](how-to-respond-to-font-scheme-changes-in-a-windows-forms-application.md). -->

[!INCLUDE [desktop guide under construction](../../includes/desktop-guide-preview-note.md)]

## <a name="need-for-automatic-scaling"></a>Notwendigkeit der automatischen Skalierung

Ohne automatische Skalierung würde eine Anwendung, die für eine bestimmte Bildschirmauflösung oder Schriftart entworfen wurde, entweder zu klein oder zu groß angezeigt, wenn diese Auflösung oder Schriftart geändert wird. Wurde die Anwendung beispielsweise mit Tahoma 9 Punkt als Basis entworfen, würde sie ohne Anpassung zu klein angezeigt, wenn sie auf einem Computer ausgeführt würde, der die Systemschriftart Tahoma 12 Punkt hat. Textelemente wie Titel, Menüs, Textfeldinhalt usw. werden kleiner gerendert als andere Anwendungen. Darüber hinaus richtet sich die Größe der Benutzeroberflächenelemente, die Text enthalten, etwa die Titelleiste, Menüs und viele Steuerelemente, nach der verwendeten Schriftart. In diesem Beispiel werden diese Elemente zusätzlich relativ kleiner angezeigt.

Die gleiche Situation ergibt sich, wenn eine Anwendung für eine bestimmte Bildschirmauflösung entworfen wurde. Die gängigste Bildschirmauflösung ist 96 DPI (Dots Per Inch), was einer Bildschirmskalierung von 100 Prozent entspricht, aber Bildschirme mit höherer Auflösung, die eine Skalierung von 125, 150, 200 Prozent (entsprechen 120, 144 und 192 DPI) oder darüber unterstützen, werden immer häufiger. Ohne Anpassung wird eine Anwendung, insbesondere eine Grafikanwendung, die für eine bestimme Auflösung entworfen wurde, entweder zu groß oder zu klein angezeigt, wenn sie mit einer anderen Auflösung ausgeführt wird.

Mit der automatischen Skalierung lassen sich diese Probleme beheben, indem die Größen des Formulars und seiner untergeordneten Steuerelemente entsprechend der relativen Schriftgröße oder Bildschirmauflösung geändert werden. Windows unterstützt die automatische Skalierung von Dialogfeldern durch Verwenden einer relativen Maßeinheit, die als Dialogeinheiten bezeichnet wird. Eine Dialogeinheit basiert auf der Systemschriftart, und ihre Beziehung zu Pixeln kann über die Win32 SDK-Funktion `GetDialogBaseUnits` bestimmt werden. Wenn ein Benutzer das von Windows verwendete Design ändert, werden alle Dialogfelder automatisch entsprechend angepasst. Zusätzlich unterstützt Windows Forms die automatische Skalierung entweder entsprechend der Standardsystemschriftart oder der Bildschirmauflösung. Optional kann die automatische Skalierung in einer Anwendung deaktiviert werden.

> [!CAUTION]
> Beliebige Kombinationen aus DPI- und Schriftartskalierungsmodi werden nicht unterstützt. Obwohl Sie ein Benutzersteuerelement mithilfe eines Modus (z. B. DPI) skalieren und ohne Probleme auf einem Formular platzieren können, für das ein anderer Modus (Schriftart) verwendet wird, kann es zu unerwarteten Ergebnissen kommen, wenn Sie ein Grundformular in einem Modus mit einem abgeleiteten Formular in einem anderen Modus mischen.

## <a name="automatic-scaling-in-action"></a>Automatische Skalierung in der Praxis

Windows Forms verwendet die folgende Logik, um Formulare und deren Inhalte automatisch zu skalieren:

01. Zur Entwurfszeit speichert jede <xref:System.Windows.Forms.ContainerControl>-Instanz den Skalierungsmodus und ihre aktuelle Auflösung in der <xref:System.Windows.Forms.ContainerControl.AutoScaleMode%2A>- bzw. der <xref:System.Windows.Forms.ContainerControl.AutoScaleDimensions%2A>-Eigenschaft.

01. Zur Laufzeit wird die tatsächliche Auflösung in der <xref:System.Windows.Forms.ContainerControl.CurrentAutoScaleDimensions%2A>-Eigenschaft gespeichert. Die <xref:System.Windows.Forms.ContainerControl.AutoScaleFactor%2A>-Eigenschaft berechnet dynamisch das Verhältnis zwischen der Laufzeit- und der Entwurfszeitskalierungsauflösung.

01. Wenn das Formular geladen wird und sich die Werte von <xref:System.Windows.Forms.ContainerControl.CurrentAutoScaleDimensions%2A> und <xref:System.Windows.Forms.ContainerControl.AutoScaleDimensions%2A> unterscheiden, wird die <xref:System.Windows.Forms.ContainerControl.PerformAutoScale%2A>-Methode aufgerufen, um das Steuerelement und dessen untergeordneten Elemente zu skalieren. Diese Methode übergeht das Layout und ruft die <xref:System.Windows.Forms.Control.Scale%2A>-Methode auf, um die tatsächliche Skalierung auszuführen. Danach wird der Wert von <xref:System.Windows.Forms.ContainerControl.AutoScaleDimensions%2A> aktualisiert, um weitere Skalierung zu vermeiden.

01. <xref:System.Windows.Forms.ContainerControl.PerformAutoScale%2A> wird auch in den folgenden Situationen automatisch aufgerufen:

    - Als Reaktion auf das <xref:System.Windows.Forms.Control.OnFontChanged%2A>-Ereignis, wenn der Skalierungsmodus gleich <xref:System.Windows.Forms.AutoScaleMode.Font> ist.

    - Wenn wieder das Layout des Containersteuerelements verwendet wird und eine Änderung in der <xref:System.Windows.Forms.ContainerControl.AutoScaleDimensions%2A>- oder der <xref:System.Windows.Forms.ContainerControl.AutoScaleMode%2A>-Eigenschaft erkannt wurde.

    - Wenn, wie soeben erwähnt, ein übergeordnetes <xref:System.Windows.Forms.ContainerControl> skaliert wird. Jedes Containersteuerelement muss seine untergeordneten Elemente mit seinen eigenen Skalierungsfaktoren skalieren, es darf dafür nicht den Faktor seines übergeordneten Containers verwenden.

01. Untergeordnete Steuerelemente können ihr Skalierungsverhalten auf mehrere Arten ändern:

    - Die <xref:System.Windows.Forms.Control.ScaleChildren%2A>-Eigenschaft kann überschrieben werden, um zu bestimmen, ob die untergeordneten Steuerelemente skaliert werden sollen oder nicht.

    - Die <xref:System.Windows.Forms.Control.GetScaledBounds%2A>-Methode kann überschrieben werden, um die Begrenzungen für die Skalierung des Steuerelements, aber nicht die Skalierungslogik anzupassen.

    - Die <xref:System.Windows.Forms.Control.ScaleControl%2A>-Methode kann überschrieben werden, um die Skalierungslogik für das aktuelle Steuerelement zu ändern.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ContainerControl.AutoScaleMode%2A>
- <xref:System.Windows.Forms.Control.Scale%2A>
- <xref:System.Windows.Forms.ContainerControl.PerformAutoScale%2A>
- <xref:System.Windows.Forms.ContainerControl.AutoScaleDimensions%2A>

<!-- TODO
- [Rendering Controls with Visual Styles](controls/rendering-controls-with-visual-styles.md)
- [How to: Improve Performance by Avoiding Automatic Scaling](advanced/how-to-improve-performance-by-avoiding-automatic-scaling.md)-->
