---
title: Übersicht über die ErrorProvider-Komponente
ms.date: 03/30/2017
f1_keywords:
- ErrorProvider
helpviewer_keywords:
- errors [Windows Forms], displaying to users
- error messages [Windows Forms], displaying
- ErrorProvider component [Windows Forms], about ErrorProvider component
ms.assetid: ced189f2-b5c8-46a7-a6f1-37f5af95dc99
ms.openlocfilehash: b66e97d97d0d8c2ea4e9bdba29f8ff35e486e1f6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975775"
---
# <a name="errorprovider-component-overview-windows-forms"></a>Übersicht über die ErrorProvider-Komponente (Windows Forms)
Die Windows Forms [ErrorProvider](errorprovider-component-windows-forms.md) -Komponente wird verwendet, um Benutzereingaben in einem Formular oder Steuerelement zu validieren. Sie wird in der Regel in Verbindung mit dem Validieren von Benutzereingaben in einem Formular oder dem Anzeigen von Fehlern in einem DataSet verwendet. Ein Fehler Anbieter ist eine bessere Alternative als das Anzeigen einer Fehlermeldung in einem Meldungs Feld, da die Fehlermeldung nach dem verwerfen eines Meldungs Felds nicht mehr sichtbar ist. Die <xref:System.Windows.Forms.ErrorProvider> Komponente zeigt ein Fehler Symbol an ( ![ ein weißes Ausrufezeichen innerhalb eines roten Kreises ](./media/errorprovider-component-overview-windows-forms/vb-error-provider-icon.gif) ) neben dem entsprechenden Steuerelement, z. b. einem Textfeld. wenn der Benutzer den Mauszeiger auf das Fehler Symbol positioniert, wird eine QuickInfo mit der Zeichenfolge der Fehlermeldung angezeigt.  
  
## <a name="key-properties"></a>Schlüsseleigenschaften  
 Die <xref:System.Windows.Forms.ErrorProvider> Schlüsseleigenschaften der Komponente sind <xref:System.Windows.Forms.ErrorProvider.DataSource%2A> , <xref:System.Windows.Forms.ErrorProvider.ContainerControl%2A> und <xref:System.Windows.Forms.ErrorProvider.Icon%2A> . Wenn Sie die <xref:System.Windows.Forms.ErrorProvider> -Komponente mit Daten gebundenen Steuerelementen verwenden, muss die- <xref:System.Windows.Forms.ErrorProvider.ContainerControl%2A> Eigenschaft auf den entsprechenden Container festgelegt werden (normalerweise das Windows Form), damit die Komponente ein Fehler Symbol im Formular anzeigt. Wenn die Komponente im-Designer hinzugefügt wird, <xref:System.Windows.Forms.ErrorProvider.ContainerControl%2A> wird die-Eigenschaft auf das enthaltende Formular festgelegt. Wenn Sie das Steuerelement im Code hinzufügen, müssen Sie es selbst festlegen.  
  
 Die- <xref:System.Windows.Forms.ErrorProvider.Icon%2A> Eigenschaft kann auf ein benutzerdefiniertes Fehler Symbol anstatt auf den Standardwert festgelegt werden. Wenn die- <xref:System.Windows.Forms.ErrorProvider.DataSource%2A> Eigenschaft festgelegt ist, <xref:System.Windows.Forms.ErrorProvider> kann die Komponente Fehlermeldungen für ein Dataset anzeigen. Die Schlüsselmethode der- <xref:System.Windows.Forms.ErrorProvider> Komponente ist die- <xref:System.Windows.Forms.ErrorProvider.SetError%2A> Methode, die die Fehlermeldungs Zeichenfolge angibt und in der das Fehler Symbol angezeigt werden soll.  
  
> [!NOTE]
> Die <xref:System.Windows.Forms.ErrorProvider> Komponente bietet keine integrierte Unterstützung für Barrierefreiheits Clients. Um auf die Anwendung zugreifen zu können, wenn Sie diese Komponente verwenden, müssen Sie einen zusätzlichen, zugänglichen Feedback Mechanismus bereitstellen.  
  
## <a name="see-also"></a>Siehe auch

- <xref:System.Windows.Forms.ErrorProvider>
- [Vorgehensweise: Anzeigen von Fehlern innerhalb eines Datasets mit der ErrorProvider-Komponente in Windows Forms](view-errors-within-a-dataset-with-wf-errorprovider-component.md)
- [Vorgehensweise: Anzeigen von Fehlersymbolen für die Formularvalidierung mit der ErrorProvider-Komponente in Windows Forms](display-error-icons-for-form-validation-with-wf-errorprovider.md)
