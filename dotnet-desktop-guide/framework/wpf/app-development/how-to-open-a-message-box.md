---
title: 'Vorgehensweise: Öffnen eines Meldungs Felds'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- message boxes [WPF], opening
- opening message boxes [WPF]
ms.assetid: acaad17f-af43-4eca-a004-f1c9e7c6f292
ms.openlocfilehash: bd2c4dce78e46163eb4628cb3aab829fc0173edf
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977417"
---
# <a name="how-to-open-a-message-box"></a>Vorgehensweise: Öffnen eines Meldungs Felds
Dieses Beispiel zeigt, wie ein Meldungs Feld geöffnet wird.  
  
## <a name="example"></a>Beispiel  
 Ein Meldungs Feld ist ein vorgefertigtes modales Dialogfeld zum Anzeigen von Informationen für Benutzer. Ein Meldungs Feld wird geöffnet, indem die statische- <xref:System.Windows.MessageBox.Show%2A> Methode der-Klasse aufgerufen wird <xref:System.Windows.MessageBox> . Wenn <xref:System.Windows.MessageBox.Show%2A> aufgerufen wird, wird die Nachricht mit einem Zeichen folgen Parameter übergeben. Mit mehreren über Ladungen von <xref:System.Windows.MessageBox.Show%2A> können Sie konfigurieren, wie ein Meldungs Feld angezeigt wird (siehe <xref:System.Windows.MessageBox> ).  
  
 [!code-csharp[MessageBoxSnippets#MessageBoxShow1CODE](~/samples/snippets/csharp/VS_Snippets_Wpf/MessageBoxSnippets/CSharp/Show1Window.xaml.cs#messageboxshow1code)]
 [!code-vb[MessageBoxSnippets#MessageBoxShow1CODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MessageBoxSnippets/visualbasic/show1window.xaml.vb#messageboxshow1code)]  
  
## <a name="see-also"></a>Siehe auch

- [MessageBox-Beispiel](https://github.com/Microsoft/WPF-Samples/tree/master/Windows/MessageBox)
