---
title: Binden des Steuer Elements an einen Typ mithilfe des Designers
ms.date: 03/30/2017
helpviewer_keywords:
- controls [Windows Forms], binding to a type
- BindingSource component [Windows Forms], binding to a type
- types [Windows Forms], binding controls to
ms.assetid: 5ab984b5-c2d0-4638-a572-1c84013e8746
ms.openlocfilehash: 2257489e123ceeea819ad3538952db51b726c7e5
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975718"
---
# <a name="how-to-bind-a-windows-forms-control-to-a-type-using-the-designer"></a>Vorgehensweise: Binden eines Windows Forms-Steuerelements an einen Typ mithilfe des Designers

Beim Erstellen von Steuerelementen, die mit Daten interagieren, ist es manchmal erforderlich, ein Steuerelement an einen Typ statt an ein Objekt zu binden. Sie müssen normalerweise ein Steuerelement zur Entwurfszeit an einen Typ binden, wenn Daten möglicherweise nicht verfügbar sind, aber die datengebundenen Steuerelemente dennoch Daten von der öffentlichen Schnittstelle eines Typs anzeigen sollen. Die folgenden Prozeduren veranschaulichen, wie ein neues erstellt <xref:System.Windows.Forms.BindingSource> wird, das an einen-Typ gebunden ist, und wie eine der-Eigenschaften des Typs an die- <xref:System.Windows.Forms.TextBox.Text%2A> Eigenschaft eines gebunden wird <xref:System.Windows.Forms.TextBox> .

### <a name="to-bind-the-bindingsource-to-a-type"></a>So binden Sie die BindingSource an einen Typen

1. Erstellen Sie ein Windows Forms Projekt (**Datei**  >  **neu**  >  **Projekt**  >  **Visual c#** oder **Visual Basic**  >  **klassische Desktop**  >  **Windows Forms Anwendung**).

2. Ziehen Sie eine Komponente in der **Entwurfs** Ansicht <xref:System.Windows.Forms.BindingSource> auf das Formular.

3. Klicken Sie im **Eigenschaften** Fenster auf den Pfeil für die- <xref:System.Windows.Forms.BindingSource.DataSource%2A> Eigenschaft.

4. Klicken Sie im **DataSource-UI-Typ-Editor** auf **Projektdatenquelle hinzufügen**.

5. Wählen Sie auf der Seite **Datenquellentyp auswählen** die Option **Objekt** aus, und klicken Sie dann auf **Weiter**.

6. Wählen Sie den Typ aus, an den gebunden werden soll:

    - Wenn sich der Typ, den Sie binden möchten, im aktuellen Projekt befindet oder die Assembly, die den Typ enthält, bereits als Verweis hinzugefügt ist, müssen Sie die Knoten erweitern, um den gewünschten Typ zu suchen. Wählen Sie ihn anschließend aus.

      \- oder -

    - Wenn sich der Typ, an den Sie binden möchten, in einer anderen Assembly befindet, die derzeit nicht in der Liste der Verweise enthalten ist, klicken Sie auf **Verweis hinzufügen** und dann auf die Registerkarte **Projekte** . Wählen Sie das Projekt aus, das das gewünschte Geschäftsobjekt enthält, und klicken Sie auf **OK**. Dieses Projekt erscheint in der Liste der Assemblys. Dadurch können Sie die Knoten erweitern, um den gewünschten Typ zu suchen und ihn anschließend auszuwählen.

      > [!NOTE]
      > Deaktivieren Sie das Dialogfeld **Assemblys ausblenden, die mit „Microsoft“ oder „System“ beginnen**, wenn Sie an einen Typen in einem Framework oder einer Microsoft-Assembly binden möchten.

7. Klicken Sie auf **Weiter** und dann auf **Fertig stellen**.

### <a name="to-bind-the-control-to-the-bindingsource"></a>So binden Sie das Steuerelement an die BindingSource

1. Fügen Sie dem Formular eine <xref:System.Windows.Forms.TextBox> hinzu.

2. Erweitern Sie im Fenster **Eigenschaften** den Knoten **(DataBindings)**.

3. Klicken Sie auf den Pfeil neben der- <xref:System.Windows.Forms.TextBox.Text%2A> Eigenschaft.

4. Erweitern Sie im **DataSource-Typ-Editor für die Benutzeroberfläche** den Knoten für das <xref:System.Windows.Forms.BindingSource> zuvor hinzugefügte, und wählen Sie die Eigenschaft des gebundenen Typs aus, die Sie an die- <xref:System.Windows.Forms.TextBox.Text%2A> Eigenschaft des binden möchten <xref:System.Windows.Forms.TextBox> .

## <a name="see-also"></a>Siehe auch

- [BindingSource-Komponente](bindingsource-component.md)
- [Vorgehensweise: Binden eines Windows Forms-Steuerelements an einen Typ](how-to-bind-a-windows-forms-control-to-a-type.md)
- [Binden von Steuerelementen an Daten in Visual Studio](/visualstudio/data-tools/bind-controls-to-data-in-visual-studio)
