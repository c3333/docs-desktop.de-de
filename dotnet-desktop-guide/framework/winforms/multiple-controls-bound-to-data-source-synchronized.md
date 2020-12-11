---
title: 'Vorgehensweise: Sicherstellen, dass mehrere Steuerelemente, die an die gleiche Datenquelle gebunden sind, synchronisiert bleiben'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- controls [Windows Forms], binding multiple
- controls [Windows Forms], synchronizing with data source
ms.assetid: c2f0ecc6-11e6-4c2c-a1ca-0759630c451e
ms.openlocfilehash: 8a39c50bfc452c807a18a9bf0a65e56cb75d20aa
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972292"
---
# <a name="how-to-ensure-multiple-controls-bound-to-the-same-data-source-remain-synchronized"></a>Vorgehensweise: Sicherstellen, dass mehrere Steuerelemente, die an die gleiche Datenquelle gebunden sind, synchronisiert bleiben
Häufig sind beim Arbeiten mit der Datenbindung in Windows Forms mehrere Steuerelemente an dieselbe Datenquelle gebunden. In einigen Fällen kann es erforderlich sein, zusätzliche Schritte auszuführen, um sicherzustellen, dass die gebundenen Eigenschaften der Steuerelemente miteinander und mit der Datenquelle synchronisiert bleiben. Diese Schritte sind in zwei Situationen erforderlich:  
  
- , Wenn die Datenquelle nicht implementiert <xref:System.ComponentModel.IBindingList> und daher <xref:System.ComponentModel.IBindingList.ListChanged> Ereignisse vom Typ generiert <xref:System.ComponentModel.ListChangedType.ItemChanged> .  
  
- , Wenn die Datenquelle implementiert <xref:System.ComponentModel.IEditableObject> .  
  
 Im ersten Fall können Sie einen verwenden, <xref:System.Windows.Forms.BindingSource> um die Datenquelle an die Steuerelemente zu binden. Im letzteren Fall verwenden Sie eine <xref:System.Windows.Forms.BindingSource> und behandeln das- <xref:System.Windows.Forms.BindingSource.BindingComplete> Ereignis und den-Befehl für die zugeordnete <xref:System.Windows.Forms.BindingManagerBase.EndCurrentEdit%2A> <xref:System.Windows.Forms.BindingManagerBase> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird veranschaulicht, wie drei Steuerelemente – zwei Textfeld-Steuerelemente und ein- <xref:System.Windows.Forms.DataGridView> Steuerelement – an dieselbe Spalte in einer <xref:System.Data.DataSet> mithilfe einer-Komponente gebunden werden <xref:System.Windows.Forms.BindingSource> . In diesem Beispiel wird veranschaulicht, wie das <xref:System.Windows.Forms.BindingSource.BindingComplete> -Ereignis behandelt wird und sichergestellt wird, dass das zusätzliche Textfeld und das- <xref:System.Windows.Forms.DataGridView> Steuerelement mit dem richtigen Wert aktualisiert werden, wenn der Textwert eines Textfelds geändert wird.  
  
 Im Beispiel wird ein verwendet <xref:System.Windows.Forms.BindingSource> , um die Datenquelle und die Steuerelemente zu binden. Alternativ dazu können Sie die Steuerelemente direkt an die Datenquelle binden und die <xref:System.Windows.Forms.BindingManagerBase> für die Bindung aus dem des Formulars abrufen <xref:System.Windows.Forms.Control.BindingContext%2A> und dann das- <xref:System.Windows.Forms.BindingManagerBase.BindingComplete> Ereignis für das verarbeiten <xref:System.Windows.Forms.BindingManagerBase> . Ein Beispiel hierfür finden Sie auf der Hilfeseite zum- <xref:System.Windows.Forms.BindingManagerBase.BindingComplete> Ereignis von <xref:System.Windows.Forms.BindingManagerBase> .  
  
 [!code-csharp[System.Windows.Forms.BindingSourceMultipleControls#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Windows.Forms.BindingSourceMultipleControls/CS/Form1.cs#1)]
 [!code-vb[System.Windows.Forms.BindingSourceMultipleControls#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Windows.Forms.BindingSourceMultipleControls/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
  
- Dieses Codebeispiel erfordert  
  
- Verweise auf die Assemblys <xref:System>, <xref:System.Windows.Forms> und <xref:System.Drawing>.  
  
- Ein Formular mit dem <xref:System.Windows.Forms.Form.Load> Ereignis, das behandelt wird, und ein aufrufener `InitializeControlsAndDataSource` Methode im Beispiel aus dem- <xref:System.Windows.Forms.Form.Load> Ereignishandler des Formulars.  
  
## <a name="see-also"></a>Siehe auch

- [Vorgehensweise: Freigeben von gebundenen Daten in Formularen mithilfe der BindingSource-Komponente](./controls/how-to-share-bound-data-across-forms-using-the-bindingsource-component.md)
- [Änderungsbenachrichtigung in der Windows Forms-Datenbindung](change-notification-in-windows-forms-data-binding.md)
- [Auf Datenbindung bezogene Schnittstellen](interfaces-related-to-data-binding.md)
- [Datenbindung in Web Forms](windows-forms-data-binding.md)
