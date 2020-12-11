---
title: 'Vorgehensweise: Erben von Formularen mithilfe des Dialogfelds „Vererbungsauswahl“'
ms.date: 03/30/2017
helpviewer_keywords:
- inheritance [Windows Forms], forms
- Inheritance Picker dialog box
- inherited forms [Windows Forms], creating
ms.assetid: 969b4c04-12aa-4297-93a2-0ae747447823
ms.openlocfilehash: ccfcc449fcd387a21edfa96b1d16e47cf1ba2833
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976161"
---
# <a name="how-to-inherit-forms-using-the-inheritance-picker"></a>Gewusst wie: Erben von Formularen mithilfe der Vererbungs Auswahl

Das Dialogfeld **Vererbungsauswahl** bietet die einfachste Möglichkeit, ein Formular oder ein anderes Objekt zu erben. Mithilfe dieser Option können Sie die Vorteile von Codezeichenfolgen oder Benutzeroberflächen (UI) nutzen, die Sie bereits in anderen Projektmappen erstellt haben.

> [!NOTE]
> Damit die Formularvererbung vom Dialogfeld **Vererbungsauswahl** unterstützt wird, muss das Projekt mit dem jeweiligen Formular in eine ausführbare Datei oder DLL integriert werden. Wählen Sie zum Erstellen des Projekts aus dem Menü **Erstellen** die Option **Projektmappe** aus.

## <a name="create-a-windows-form-by-using-the-inheritance-picker"></a>Erstellen eines Windows Forms mithilfe der Vererbungs Auswahl

1. Wählen Sie in Visual Studio im Menü **Projekt** die Option **Windows Form hinzufügen** aus.

   Das Dialogfeld **Neues Element hinzufügen** wird angezeigt.

2. Durchsuchen Sie die **geerbte Formular** Vorlage entweder über die SearchBox oder durch Klicken auf die **Windows Forms** Kategorie, wählen Sie Sie aus, und benennen Sie Sie im Feld **Name** . Klicken Sie auf die Schaltfläche **Hinzufügen**, um fortzufahren.

   Das Dialogfeld **Vererbungsauswahl** wird geöffnet. Wenn das aktuelle Projekt bereits Formulare enthält, werden diese im Dialogfeld **Vererbungsauswahl** angezeigt.

3. Um von einem Formular in einer anderen Assembly zu erben, klicken Sie auf die Schaltfläche **Durchsuchen**.

4. Navigieren Sie im Dialogfeld **Eine Datei auswählen, die eine Komponente für die Vererbung enthält** zu dem Projekt, das das gewünschte Formular oder Modul enthält.

5. Klicken Sie auf den Namen der EXE- oder DLL-Datei, um sie auszuwählen, und klicken Sie dann auf die Schaltfläche **Öffnen**.

   Daraufhin kehren Sie zum Dialogfeld **Vererbungsauswahl** zurück, in dem jetzt die Komponente zusammen mit dem Projekt, in dem sie gespeichert ist, aufgelistet wird.

6. Wählen Sie die Komponente aus.

   Die Komponente wird im **Projektmappen-Explorer** zu Ihrem Projekt hinzugefügt. Wenn Sie über eine Benutzeroberfläche verfügt, werden Steuerelemente, die Bestandteil des geerbten Formulars sind, mit einem Symbol gekennzeichnet ( ![ Screenshot des Visual Basic Vererbungs Symbols ](./media/how-to-inherit-forms-using-the-inheritance-picker-dialog-box/visual-basic-inheritance-glyph.gif) ) und, wenn Sie ausgewählt sind, einen Rahmen angeben, der die Sicherheitsstufe angibt, die das Steuerelement in der übergeordneten Form hat. In der folgenden Tabelle sind die Verhaltensweisen aufgeführt, die den verschiedenen Sicherheitsebenen entsprechen.

    |Sicherheitsebene des Steuerelements|Mögliche Interaktion mit geerbtem Formular im Designer und Code-Editor|
    |-------------------------------|--------------------------------------------------------------------------------|
    |Öffentlich|Standardrahmen mit Ziehpunkten: Das Steuerelement kann vergrößert, verkleinert und verschoben werden. Auf das Steuerelement kann intern durch die Klasse, durch die es deklariert wird, und extern durch andere Klassen zugegriffen werden.|
    |Protected|Standardrahmen mit Ziehpunkten: Das Steuerelement kann vergrößert, verkleinert und verschoben werden. Auf das Steuerelement kann intern durch die Klasse, durch die es deklariert wird, und durch alle Klassen, die von der übergeordneten Klasse erben, nicht jedoch durch externe Klassen zugegriffen werden.|
    |Protected Internal (Protected Friend in Visual Basic)|Standardrahmen mit Ziehpunkten: Das Steuerelement kann vergrößert, verkleinert und verschoben werden. Auf das Steuerelement kann intern durch die Klasse, durch die es deklariert wird, durch alle Klassen, die von der übergeordneten Klasse erben, sowie durch andere Member der Assembly, die es enthält, zugegriffen werden.|
    |Internal (Friend in Visual Basic)|Standardrahmen ohne Ziehpunkte: Das Steuerelement wird im Formular angezeigt, und seine Eigenschaften sind im Fenster **Eigenschaften** sichtbar. Sämtliche Merkmale des Steuerelements werden jedoch als schreibgeschützt betrachtet. Das Steuerelement kann nicht verschoben und Größe oder Eigenschaften können nicht geändert werden. Wenn es sich bei dem Steuerelement um einen Container für andere Steuerelemente (z. B. um ein Gruppenfeld) handelt, können keine neuen Steuerelemente hinzugefügt und keine vorhandenen Steuerelemente entfernt werden. Dies gilt auch dann, wenn diese Steuerelemente die "Public"-Eigenschaft besitzen. Auf das Steuerelement können nur andere Member der Assembly zugreifen, die es enthält.|
    |Privat|Standardrahmen ohne Ziehpunkte: Das Steuerelement wird im Formular angezeigt, und seine Eigenschaften sind im Fenster **Eigenschaften** sichtbar. Sämtliche Merkmale des Steuerelements werden jedoch als schreibgeschützt betrachtet. Das Steuerelement kann nicht verschoben und Größe oder Eigenschaften können nicht geändert werden. Wenn es sich bei dem Steuerelement um einen Container für andere Steuerelemente (z. B. um ein Gruppenfeld) handelt, können keine neuen Steuerelemente hinzugefügt und keine vorhandenen Steuerelemente entfernt werden. Dies gilt auch dann, wenn diese Steuerelemente die "Public"-Eigenschaft besitzen. Auf das Steuerelement kann nur durch die Klasse zugegriffen werden, durch die es deklariert wird.|

     Informationen zum Ändern der Darstellung eines Basisformulars finden Sie unter [Auswirkungen beim Ändern der Darstellung von Basisformularen](effects-of-modifying-base-form-appearance.md).

    > [!NOTE]
    > Wenn Sie geerbte Steuerelemente und Komponenten mit standardmäßigen Steuerelementen und Komponenten in Windows Forms kombinieren, treten möglicherweise Konflikte hinsichtlich der Z-Reihenfolge auf. Sie können diese Probleme lösen, indem Sie die Z-Reihenfolge ändern. Zeigen Sie hierzu im Menü **Format** auf **Reihenfolge** und klicken Sie anschließend auf **In den Vordergrund** oder **In den Hintergrund**. Weitere Informationen zur Z-Reihenfolge von Steuerelementen finden Sie unter [Vorgehensweise: Überlagern von Objekten in Windows Forms](../controls/how-to-layer-objects-on-windows-forms.md).

## <a name="see-also"></a>Siehe auch

- [Inherits Statement](/dotnet/visual-basic/language-reference/statements/inherits-statement)
- [using](/dotnet/csharp/language-reference/keywords/using)
- [Auswirkungen beim Ändern der Darstellung von Basisformularen](effects-of-modifying-base-form-appearance.md)
- [Visuelle Vererbung in Windows Forms](windows-forms-visual-inheritance.md)
