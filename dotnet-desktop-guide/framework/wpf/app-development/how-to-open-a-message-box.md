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
# <a name="how-to-open-a-message-box"></a><span data-ttu-id="d4bab-102">Vorgehensweise: Öffnen eines Meldungs Felds</span><span class="sxs-lookup"><span data-stu-id="d4bab-102">How to: Open a Message Box</span></span>
<span data-ttu-id="d4bab-103">Dieses Beispiel zeigt, wie ein Meldungs Feld geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="d4bab-103">This example shows how to open a message box.</span></span>  
  
## <a name="example"></a><span data-ttu-id="d4bab-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d4bab-104">Example</span></span>  
 <span data-ttu-id="d4bab-105">Ein Meldungs Feld ist ein vorgefertigtes modales Dialogfeld zum Anzeigen von Informationen für Benutzer.</span><span class="sxs-lookup"><span data-stu-id="d4bab-105">A message box is a prefabricated modal dialog box for displaying information to users.</span></span> <span data-ttu-id="d4bab-106">Ein Meldungs Feld wird geöffnet, indem die statische- <xref:System.Windows.MessageBox.Show%2A> Methode der-Klasse aufgerufen wird <xref:System.Windows.MessageBox> .</span><span class="sxs-lookup"><span data-stu-id="d4bab-106">A message box is opened by calling the static <xref:System.Windows.MessageBox.Show%2A> method of the <xref:System.Windows.MessageBox> class.</span></span> <span data-ttu-id="d4bab-107">Wenn <xref:System.Windows.MessageBox.Show%2A> aufgerufen wird, wird die Nachricht mit einem Zeichen folgen Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="d4bab-107">When <xref:System.Windows.MessageBox.Show%2A> is called, the message is passed using a string parameter.</span></span> <span data-ttu-id="d4bab-108">Mit mehreren über Ladungen von <xref:System.Windows.MessageBox.Show%2A> können Sie konfigurieren, wie ein Meldungs Feld angezeigt wird (siehe <xref:System.Windows.MessageBox> ).</span><span class="sxs-lookup"><span data-stu-id="d4bab-108">Several overloads of <xref:System.Windows.MessageBox.Show%2A> allow you to configure how a message box will appear (see <xref:System.Windows.MessageBox>).</span></span>  
  
 [!code-csharp[MessageBoxSnippets#MessageBoxShow1CODE](~/samples/snippets/csharp/VS_Snippets_Wpf/MessageBoxSnippets/CSharp/Show1Window.xaml.cs#messageboxshow1code)]
 [!code-vb[MessageBoxSnippets#MessageBoxShow1CODE](~/samples/snippets/visualbasic/VS_Snippets_Wpf/MessageBoxSnippets/visualbasic/show1window.xaml.vb#messageboxshow1code)]  
  
## <a name="see-also"></a><span data-ttu-id="d4bab-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4bab-109">See also</span></span>

- [<span data-ttu-id="d4bab-110">MessageBox-Beispiel</span><span class="sxs-lookup"><span data-stu-id="d4bab-110">MessageBox Sample</span></span>](https://github.com/Microsoft/WPF-Samples/tree/master/Windows/MessageBox)
