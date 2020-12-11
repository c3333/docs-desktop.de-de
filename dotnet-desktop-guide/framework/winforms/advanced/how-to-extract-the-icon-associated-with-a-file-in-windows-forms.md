---
title: 'Gewusst wie: Extrahieren eines mit einer Datei verknüpften Symbols'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- displaying a file name and its file type icon in a ListView control [Windows Forms]
- file name extension icons [Windows Forms], displaying in a ListView
- extracting icons associated with a file type [Windows Forms]
ms.assetid: 88e2ad8b-c34f-415a-84f2-dad756b5c928
ms.openlocfilehash: 28769144b0e1c631a31c3c541747a6215f861d0e
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975912"
---
# <a name="how-to-extract-the-icon-associated-with-a-file-in-windows-forms"></a>Vorgehensweise: Extrahieren eines mit einer Datei verknüpften Symbols in Windows Forms
Viele Dateien verfügen über eingebettete Symbole, die eine visuelle Darstellung des zugeordneten Dateityps bereitstellen. Beispielsweise enthalten Microsoft Word-Dokumente ein Symbol, mit dem Sie als Word-Dokumente identifiziert werden. Wenn Sie Dateien in einem Listen Steuerelement oder Tabellen Steuerelement anzeigen, möchten Sie möglicherweise das Symbol anzeigen, das den Dateityp neben den einzelnen Dateinamen darstellt. Dies kann problemlos mithilfe der-Methode durchzuführen sein <xref:System.Drawing.Icon.ExtractAssociatedIcon%2A> .  
  
## <a name="example"></a>Beispiel  
 Im folgenden Codebeispiel wird veranschaulicht, wie das Symbol, das einer Datei zugeordnet ist, extrahiert und der Dateiname und das zugehörige Symbol in einem-Steuerelement angezeigt werden <xref:System.Windows.Forms.ListView> .  
  
 [!code-csharp[System.Drawing.Icon.ExtractAssociatedIconEx#1](~/samples/snippets/csharp/VS_Snippets_Winforms/System.Drawing.Icon.ExtractAssociatedIconEx/CS/Form1.cs#1)]
 [!code-vb[System.Drawing.Icon.ExtractAssociatedIconEx#1](~/samples/snippets/visualbasic/VS_Snippets_Winforms/System.Drawing.Icon.ExtractAssociatedIconEx/VB/Form1.vb#1)]  
  
## <a name="compiling-the-code"></a>Kompilieren des Codes  
 So kompilieren Sie das Beispiel:  
  
- Fügen Sie den vorangehenden Code in ein Windows Form ein, und nennen Sie die `ExtractAssociatedIconExample` -Methode aus dem Konstruktor des Formulars oder der <xref:System.Windows.Forms.Form.Load> Ereignis Behandlungsmethode.  
  
     Sie müssen sicherstellen, dass das Formular den <xref:System.IO> Namespace importiert.  
  
## <a name="see-also"></a>Siehe auch

- [Bilder, Bitmaps und Metadatendateien](images-bitmaps-and-metafiles.md)
- [ListView-Steuerelement](../controls/listview-control-windows-forms.md)
