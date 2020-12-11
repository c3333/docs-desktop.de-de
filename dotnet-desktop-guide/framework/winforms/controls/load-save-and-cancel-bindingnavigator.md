---
title: Schaltflächen zum Laden, speichern und Abbrechen zum BindingNavigator-Steuerelement hinzufügen
description: Erfahren Sie, wie Sie Schaltflächen zum Laden, speichern und Abbrechen zum Windows Forms BindingNavigator-Steuerelement hinzufügen.
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms], manipulating
- BindingNavigator control [Windows Forms], adding buttons
ms.assetid: faa33042-186e-4bb2-8798-17ceb987ec62
ms.openlocfilehash: d4db91b8cfaf2df253d0c4cf5d8a66e9157d4986
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976717"
---
# <a name="how-to-add-load-save-and-cancel-buttons-to-the-windows-forms-bindingnavigator-control"></a>Vorgehensweise: Hinzufügen der Schaltflächen für das Laden, Speichern und Abbrechen zum BindingNavigator-Steuerelement in Windows Forms

Das <xref:System.Windows.Forms.BindingNavigator> -Steuerelement ist ein spezielles <xref:System.Windows.Forms.ToolStrip> Steuerelement, das zum Navigieren und Bearbeiten von Steuerelementen auf dem Formular gedacht ist, die an Daten gebunden sind.

Da es <xref:System.Windows.Forms.ToolStrip> sich um ein Steuerelement handelt, <xref:System.Windows.Forms.BindingNavigator> kann die Komponente problemlos geändert werden, um zusätzliche oder Alternative Befehle für den Benutzer einzuschließen.

In der folgenden Prozedur ist ein <xref:System.Windows.Forms.TextBox> -Steuerelement an Daten gebunden, und das <xref:System.Windows.Forms.ToolStrip> Steuerelement, das dem Formular hinzugefügt wird, wird so geändert, dass es die Schaltflächen laden, speichern und Abbrechen enthält.

## <a name="add-load-save-and-cancel-buttons-to-the-bindingnavigator-component"></a>Hinzufügen von Schaltflächen zum Laden, speichern und Abbrechen zur BindingNavigator-Komponente

1. Fügen Sie in Visual Studio ein- <xref:System.Windows.Forms.TextBox> Steuerelement zum Formular hinzu.

2. Binden Sie es an eine <xref:System.Windows.Forms.BindingSource> , die an eine Datenquelle gebunden ist. In diesem Beispiel ist der <xref:System.Windows.Forms.BindingSource> an eine Datenbank gebunden.

3. Nachdem das DataSet und der Tabellen Adapter generiert wurden, ziehen <xref:System.Windows.Forms.BindingNavigator> Sie ein-Steuerelement in das Formular.

4. Legen <xref:System.Windows.Forms.BindingNavigator> Sie die-Eigenschaft des-Steuer Elements auf dem Formular fest <xref:System.Windows.Forms.BindingNavigator.BindingSource%2A> <xref:System.Windows.Forms.BindingSource> , das an die Steuerelemente gebunden ist.

5. Wählen Sie das <xref:System.Windows.Forms.BindingNavigator>-Steuerelement.

6. Klicken Sie auf das Symbol Designer Aktionen ( ![ kleiner schwarzer Pfeil ](./media/designer-actions-glyph.gif) ), damit das Dialogfeld **BindingNavigator-Aufgaben** angezeigt wird, und klicken Sie auf **Elemente bearbeiten**.

     Der Elementauflistungs- **Editor** wird angezeigt.

7. Führen Sie im Elementauflistungs- **Editor** die folgenden Schritte aus:

    1. Fügen Sie ein <xref:System.Windows.Forms.ToolStripSeparator> und drei Elemente hinzu, <xref:System.Windows.Forms.ToolStripButton> indem Sie den entsprechenden Typ von auswählen <xref:System.Windows.Forms.ToolStripItem> und auf die Schaltfläche **Hinzufügen** klicken.

    2. Legen <xref:System.Windows.Forms.ToolStripItem.Name%2A> Sie die-Eigenschaft der Schaltflächen auf **loadButton**, **SaveButton** bzw. **CancelButton** fest.

    3. Legen Sie die- <xref:System.Windows.Forms.ToolStripItem.Text%2A> Eigenschaft der Schaltflächen auf **Laden**, **Speichern** und **Abbrechen** fest.

    4. Legen Sie die- <xref:System.Windows.Forms.ToolStripItem.DisplayStyle%2A> Eigenschaft für jede der Schaltflächen auf **Text** fest. Alternativ können Sie diese Eigenschaft auf **Image** oder **ImageAndText** festlegen und das Bild so festlegen, dass es in der- <xref:System.Windows.Forms.ToolStripItem.Image%2A> Eigenschaft angezeigt wird.

    5. Klicken Sie auf **OK** , um das Dialogfeld zu schließen. Die Schaltflächen werden dem hinzugefügt <xref:System.Windows.Forms.ToolStrip> .

8. Klicken Sie mit der rechten Maustaste, und wählen Sie **Code anzeigen** aus.

9. Suchen Sie im Code-Editor nach der Codezeile, die Daten in den Tabellen Adapter lädt. Dieser Code wurde generiert, als Sie die Datenbindung in Schritt 2 eingerichtet haben. Der Code sollte in etwa wie folgt aussehen: `TableAdapterName.Fill(DataSetName.TableName)` . Sie wird wahrscheinlich im-Ereignis des Formulars angezeigt <xref:System.Windows.Forms.Form.Load> .

10. Erstellen Sie einen Ereignishandler für das- <xref:System.Windows.Forms.ToolStripItem.Click> Ereignis der **Last** , die <xref:System.Windows.Forms.ToolStripButton> Sie zuvor erstellt haben, und verschieben Sie diesen datenladencode hinein.

     Der Code sollte nun in etwa wie folgt aussehen:

    ```vb
    Private Sub LoadButton_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles LoadButton.Click
        TableAdapterName.Fill(DataSetName.TableName)
    End Sub
    ```

    ```csharp
    private void LoadButton_Click(System.Object sender,
        System.EventArgs e)
    {
        TableAdapterName.Fill(DataSetName.TableName);
    }
    ```

11. Erstellen Sie einen Ereignishandler für das- <xref:System.Windows.Forms.ToolStripItem.Click> Ereignis  der <xref:System.Windows.Forms.ToolStripButton> zuvor erstellten Speicherung, und schreiben Sie Code, um die Daten in der Tabelle zu aktualisieren, an die das Steuerelement gebunden ist.

    ```vb
    Private Sub SaveButton_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles SaveButton.Click
        TableAdapterName.Update(DataSetName.TableName)
    End Sub
    ```

    ```csharp
    private void SaveButton_Click(System.Object sender,
        System.EventArgs e)
    {
        TableAdapterName.Update(DataSetName.TableName);
    }
    ```

    > [!NOTE]
    > In einigen Fällen verfügt die <xref:System.Windows.Forms.BindingNavigator> Komponente bereits über eine Schaltfläche zum **Speichern** , aber es wurde kein Code vom Windows Forms-Designer generiert. In diesem Fall können Sie den vorangehenden Code im- <xref:System.Windows.Forms.ToolStripItem.Click> Ereignishandler für diese Schaltfläche platzieren, anstatt eine völlig neue Schaltfläche in der zu erstellen <xref:System.Windows.Forms.ToolStrip> . Die Schaltfläche ist jedoch standardmäßig deaktiviert, sodass Sie die- <xref:System.Windows.Forms.ToolBarButton.Enabled%2A> Eigenschaft der Schaltfläche auf festlegen müssen, damit `true` die Schaltfläche ordnungsgemäß funktioniert.

12. Erstellen Sie einen Ereignishandler für das- <xref:System.Windows.Forms.ToolStripItem.Click> Ereignis  von <xref:System.Windows.Forms.ToolStripButton> , den Sie zuvor erstellt haben, und schreiben Sie Code, um alle Änderungen am angezeigten Daten Satz abzubrechen.

    ```vb
    Private Sub CancelButton_Click(ByVal sender As System.Object, ByVal e As System.EventArgs) Handles CancelButton.Click
        BindingSourceName.CancelEdit()
    End Sub
    ```

    ```csharp
    private void CancelButton_Click(System.Object sender, System.EventArgs e)
    {
        BindingSourceName.CancelEdit();
    }
    ```

    > [!NOTE]
    > Die- <xref:System.Windows.Forms.BindingSource.CancelEdit%2A> Methode wird auf die Daten Zeile festgelegt. Speichern Sie alle Änderungen, die Sie vornehmen, während Sie den einzelnen Datensatz anzeigen, bevor Sie zum nächsten Datensatz navigieren.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.BindingNavigator>
- <xref:System.Windows.Forms.BindingSource>
- <xref:System.Windows.Forms.ToolStrip>
- [BindingNavigator-Steuerelement](bindingnavigator-control-windows-forms.md)
- [Übersicht über die BindingSource-Komponente](bindingsource-component-overview.md)
