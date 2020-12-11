---
title: 'Vorgehensweise: Erstellen eines einfach gebundenen Steuerelements in einer Windows Forms-Instanz'
ms.date: 03/30/2017
helpviewer_keywords:
- data binding [Windows Forms], simple data binding
- Windows Forms controls, data binding
ms.assetid: 3bcaded8-0f1a-4cc0-8830-f59be253bf4e
ms.openlocfilehash: bb7554831ab3698333850b71c42a5343ceb7d682
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972310"
---
# <a name="how-to-create-a-simple-bound-control-on-a-windows-form"></a>Gewusst wie: Erstellen eines einfach gebundenen Steuer Elements in einem Windows Form

Mit der *einfachen Bindung* können Sie in einem-Steuerelement ein einzelnes Datenelement, z. b. einen Spaltenwert aus einer Datasettabelle, anzeigen. Sie können eine beliebige Eigenschaft eines Steuer Elements an einen Datenwert binden.

## <a name="to-simple-bind-a-control"></a>So binden Sie ein Steuerelement einfach

1. Stellen Sie die Verbindung zu einer Datenquelle her. Weitere Informationen finden Sie unter [Herstellen einer Verbindung mit einer Datenquelle](/dotnet/framework/data/adonet/connecting-to-a-data-source).

2. Wählen Sie in Visual Studio das Steuerelement auf dem Formular aus, und zeigen Sie das **Eigenschaften** Fenster an.

3. Erweitern Sie die Eigenschaft **(DataBindings)** .

     Die Eigenschaften, die am häufigsten gebunden werden, werden unterhalb der **(DataBindings)** -Eigenschaft angezeigt. In den meisten Steuerelementen ist die **Text** -Eigenschaft z. b. am häufigsten gebunden.

4. Wenn die Eigenschaft, die Sie binden möchten, **keine der häufig** gebundenen Eigenschaften ist, klicken Sie auf die Schaltfläche mit den Auslassungs Punkten (die Schaltfläche mit den Auslassungs Punkten ![ (...) im Eigenschaftenfenster von Visual Studio. ](./media/how-to-create-a-simple-bound-control-on-a-windows-form/visual-studio-ellipsis-button.png) ) im Feld **(erweitert)** , um das Dialogfeld **Formatierung und erweiterte Bindung** mit einer kompletten Liste von Eigenschaften für dieses Steuerelement anzuzeigen.

5. Wählen Sie die Eigenschaft aus, die Sie binden möchten, und klicken Sie auf den Dropdown Pfeil unter **Bindung**.

     Nun wird eine Liste verfügbarer Datenquellen angezeigt.

6. Erweitern Sie die Datenquelle, die Sie für die Bindung verwenden möchten, bis Sie das gewünschte einzelne Datenelement finden. Wenn die Bindung beispielsweise an einen Spaltenwert in einer Dataset-Tabelle erfolgen soll, erweitern Sie den Namen des Datasets, und erweitern sie dann den Tabellennamen, um die Spaltennamen anzuzeigen.

7. Klicken Sie auf den Namen des Elements, das gebunden werden soll.

8. Wenn Sie im Dialogfeld **Formatierung und erweiterte Bindung** gearbeitet haben, klicken Sie auf **OK** , um zum **Eigenschaften** Fenster zurückzukehren.

9. Wenn Sie zusätzliche Eigenschaften für das Steuerelement binden möchten, wiederholen Sie die Schritte 3 bis 7.

    > [!NOTE]
    > Da einfach gebundene Steuerelemente nur ein einzelnes Datenelement anzeigen, ist es sehr typisch, Navigations Logik in ein Windows Form-Steuerelement mit einfachen gebundenen Steuerelementen einzubeziehen.

## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.Binding>
- [Datenbindung in Web Forms](windows-forms-data-binding.md)
- [Datenbindung und Windows Forms](data-binding-and-windows-forms.md)
