---
title: 'Gewusst wie: Aktivieren der Textverkürzung'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- text [WPF], trimming
- documents [WPF], trimming text
- trimming text [WPF]
ms.assetid: dd8c9191-d2be-45fd-9fb4-3c75b65578c5
ms.openlocfilehash: 25fff566868e792004a915fee195485c4a1f385f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977547"
---
# <a name="how-to-enable-text-trimming"></a>Gewusst wie: Aktivieren der Textverkürzung

In diesem Beispiel werden die Verwendung und die Auswirkungen der in der-Enumeration verfügbaren Werte veranschaulicht <xref:System.Windows.TextTrimming> .

## <a name="example"></a>Beispiel

Im folgenden Beispiel wird ein- <xref:System.Windows.Controls.TextBlock> Element mit dem <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> festgelegten Attribut definiert.

[!code-xaml[TextTrimmingSnippets#_TextTrimmingXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTrimmingSnippets/CSharp/Window1.xaml#_texttrimmingxaml)]

Das Festlegen der entsprechenden <xref:System.Windows.TextTrimming> Eigenschaft im Code wird unten veranschaulicht.

[!code-csharp[TextTrimmingSnippets#_TextTrimmingSetTextTrimming](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTrimmingSnippets/CSharp/Window1.xaml.cs#_texttrimmingsettexttrimming)]
[!code-vb[TextTrimmingSnippets#_TextTrimmingSetTextTrimming](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextTrimmingSnippets/VisualBasic/Window1.xaml.vb#_texttrimmingsettexttrimming)]

Es gibt derzeit drei Optionen zum Kürzen von Text: " **charakteriellipsis**", " **WordEllipsis**" und " **None**".

Wenn <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> auf " **Merkmal Auslassungs Punkte**" festgelegt ist, wird der Text gekürzt und mit einem Auslassungs Zeichen bei dem Zeichen fortgesetzt, das dem verkürzten Rand am nächsten liegt.  Diese Einstellung tendiert dazu, den Text zu kürzen, damit dieser besser an die Kürzungsgrenze passt. Dies kann jedoch dazu führen, dass Wörter teilweise abgeschnitten werden.  Die folgende Abbildung zeigt die Auswirkung dieser Einstellung auf eine <xref:System.Windows.Controls.TextBlock> ähnlich der oben definierten.

![Beispiel: TextTrimming.CharacterEllipsis](./media/texttrimming-character.png "TextTrimming_Character")

Wenn <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> auf **WordEllipsis** festgelegt wird, wird der Text gekürzt und mit einem Auslassungs Zeichen am Ende des ersten vollständigen Worts fortgesetzt, das dem gekürzten Rand am nächsten liegt.  Diese Einstellung zeigt keine teilweise gekürzten Wörter an, sondern bewirkt, dass der Text nicht so nah wie die Einstellung für die Einstellung für die unter **Zeichnungs** Begrenzung auf den verkürzten Rand gekürzt wird.  Die folgende Abbildung zeigt die Auswirkung dieser Einstellung auf den <xref:System.Windows.Controls.TextBlock> oben definierten.

![Beispiel: TextTrimming.WordEllipsis](./media/texttrimming-word.png "TextTrimming_Word")

Wenn <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> auf **None** festgelegt ist, wird keine Text Kürzung durchgeführt.  In diesem Fall wird Text einfach an der Begrenzung des übergeordneten Textcontainers zugeschnitten.  Die folgende Abbildung zeigt die Auswirkung dieser Einstellung auf eine <xref:System.Windows.Controls.TextBlock> ähnlich der oben definierten.

![Beispiel: TextTrimming.None](./media/texttrimming-none.png "TextTrimming_None")
