---
title: 'Vorgehensweise: Verwenden von Modifizierern und GenerateMember-Eigenschaften'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
f1_keywords:
- Designer_GenerateMember
- Designer_Modifiers
helpviewer_keywords:
- base forms
- inheritance [Windows Forms], forms
- inherited forms [Windows Forms], Windows Forms
- inherited forms
- form inheritance
- Windows Forms, inheritance
ms.assetid: 3381a5e4-e1a3-44e2-a765-a0b758937b85
ms.openlocfilehash: 3fbaaae53aa60f6356c3a8daa0513de86ef2dacb
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975853"
---
# <a name="how-to-use-the-modifiers-and-generatemember-properties"></a>Vorgehensweise: Verwenden von Modifizierern und GenerateMember-Eigenschaften

Wenn Sie eine Komponente in einem Windows Form platzieren, werden zwei Eigenschaften von der Entwurfs Umgebung bereitgestellt: `GenerateMember` und `Modifiers` . Die- `GenerateMember` Eigenschaft gibt an, wann die Windows Forms-Designer eine Element Variable für eine Komponente generiert. Die `Modifiers` Eigenschaft ist der Zugriffsmodifizierer, der dieser Element Variablen zugewiesen ist. Wenn der Wert der- `GenerateMember` Eigenschaft ist `false` , hat der Wert der- `Modifiers` Eigenschaft keine Auswirkung.

## <a name="specify-whether-a-component-is-a-member-of-the-form"></a>Geben Sie an, ob eine Komponente ein Member des Formulars ist.

1. Öffnen Sie in Visual Studio im Windows Forms-Designer das Formular.

2. Öffnen Sie die **Toolbox**, und platzieren Sie im Formular drei-Steuer <xref:System.Windows.Forms.Button> Elemente.

3. Legen `GenerateMember` Sie die `Modifiers` Eigenschaften und für jedes <xref:System.Windows.Forms.Button> Steuerelement entsprechend der folgenden Tabelle fest.

    |Schaltflächenname|GenerateMember-Wert|Modifiziererwert|
    |-----------------|--------------------------|---------------------|
    |`button1`|`true`|`private`|
    |`button2`|`true`|`protected`|
    |`button3`|`false`|Keine Änderung|

4. Erstellen Sie die Projektmappe.

5. Klicken Sie im **Projektmappen-Explorer** auf die Schaltfläche **Alle Dateien anzeigen**.

6. Öffnen Sie den Knoten **Form1** , und öffnen Sie im **Code-Editor** die Datei **Form1. Designer. vb** oder **Form1.Designer.cs** . Diese Datei enthält den Code, der vom Windows Forms-Designer ausgegeben wird.

7. Suchen Sie die Deklarationen für die drei Schaltflächen. Das folgende Codebeispiel zeigt die Unterschiede, die in den `GenerateMember` Eigenschaften und angegeben sind `Modifiers` .

     [!code-csharp[System.Windows.Forms.GenerateMember#3](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/CS/Form1.cs#3)]
     [!code-vb[System.Windows.Forms.GenerateMember#3](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/VB/Form1.vb#3)]

     [!code-csharp[System.Windows.Forms.GenerateMember#2](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/CS/Form1.cs#2)]
     [!code-vb[System.Windows.Forms.GenerateMember#2](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.GenerateMember/VB/Form1.vb#2)]

> [!NOTE]
> Standardmäßig weist das-Windows Forms-Designer `private` Container Steuer `Friend` Elementen wie den-Modifizierer (in Visual Basic) zu <xref:System.Windows.Forms.Panel> . Wenn Ihre Basis <xref:System.Windows.Forms.UserControl> oder <xref:System.Windows.Forms.Form> ein Container Steuerelement enthält, werden keine neuen untergeordneten Elemente in geerbten Steuerelementen und Formularen akzeptiert. Die Lösung besteht darin, den-Modifizierer des Basis Container-Steuer Elements in oder zu ändern `protected` `public` .

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Button>
- [Visuelle Vererbung in Windows Forms](windows-forms-visual-inheritance.md)
- [Exemplarische Vorgehensweise: Demonstrieren der visuellen Vererbung](walkthrough-demonstrating-visual-inheritance.md)
- [Vorgehensweise: Erben von Windows Forms](how-to-inherit-windows-forms.md)
