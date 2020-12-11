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
# <a name="how-to-enable-text-trimming"></a><span data-ttu-id="5423f-102">Gewusst wie: Aktivieren der Textverkürzung</span><span class="sxs-lookup"><span data-stu-id="5423f-102">How to: Enable Text Trimming</span></span>

<span data-ttu-id="5423f-103">In diesem Beispiel werden die Verwendung und die Auswirkungen der in der-Enumeration verfügbaren Werte veranschaulicht <xref:System.Windows.TextTrimming> .</span><span class="sxs-lookup"><span data-stu-id="5423f-103">This example demonstrates the usage and effects of the values available in the <xref:System.Windows.TextTrimming> enumeration.</span></span>

## <a name="example"></a><span data-ttu-id="5423f-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5423f-104">Example</span></span>

<span data-ttu-id="5423f-105">Im folgenden Beispiel wird ein- <xref:System.Windows.Controls.TextBlock> Element mit dem <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> festgelegten Attribut definiert.</span><span class="sxs-lookup"><span data-stu-id="5423f-105">The following example defines a <xref:System.Windows.Controls.TextBlock> element with the <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> attribute set.</span></span>

[!code-xaml[TextTrimmingSnippets#_TextTrimmingXAML](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTrimmingSnippets/CSharp/Window1.xaml#_texttrimmingxaml)]

<span data-ttu-id="5423f-106">Das Festlegen der entsprechenden <xref:System.Windows.TextTrimming> Eigenschaft im Code wird unten veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5423f-106">Setting the corresponding <xref:System.Windows.TextTrimming> property in code is demonstrated below.</span></span>

[!code-csharp[TextTrimmingSnippets#_TextTrimmingSetTextTrimming](~/samples/snippets/csharp/VS_Snippets_Wpf/TextTrimmingSnippets/CSharp/Window1.xaml.cs#_texttrimmingsettexttrimming)]
[!code-vb[TextTrimmingSnippets#_TextTrimmingSetTextTrimming](~/samples/snippets/visualbasic/VS_Snippets_Wpf/TextTrimmingSnippets/VisualBasic/Window1.xaml.vb#_texttrimmingsettexttrimming)]

<span data-ttu-id="5423f-107">Es gibt derzeit drei Optionen zum Kürzen von Text: " **charakteriellipsis**", " **WordEllipsis**" und " **None**".</span><span class="sxs-lookup"><span data-stu-id="5423f-107">There are currently three options for trimming text: **CharacterEllipsis**, **WordEllipsis**, and **None**.</span></span>

<span data-ttu-id="5423f-108">Wenn <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> auf " **Merkmal Auslassungs Punkte**" festgelegt ist, wird der Text gekürzt und mit einem Auslassungs Zeichen bei dem Zeichen fortgesetzt, das dem verkürzten Rand am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="5423f-108">When <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> is set to **CharacterEllipsis**, text is trimmed and continued with an ellipsis at the character closest to the trimming edge.</span></span>  <span data-ttu-id="5423f-109">Diese Einstellung tendiert dazu, den Text zu kürzen, damit dieser besser an die Kürzungsgrenze passt. Dies kann jedoch dazu führen, dass Wörter teilweise abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="5423f-109">This setting tends to trim text to fit more closely to the trimming boundary, but may result in words being partially trimmed.</span></span>  <span data-ttu-id="5423f-110">Die folgende Abbildung zeigt die Auswirkung dieser Einstellung auf eine <xref:System.Windows.Controls.TextBlock> ähnlich der oben definierten.</span><span class="sxs-lookup"><span data-stu-id="5423f-110">The following figure shows the effect of this setting on a <xref:System.Windows.Controls.TextBlock> similar to the one defined above.</span></span>

<span data-ttu-id="5423f-111">![Beispiel: TextTrimming.CharacterEllipsis](./media/texttrimming-character.png "TextTrimming_Character")</span><span class="sxs-lookup"><span data-stu-id="5423f-111">![Example: TextTrimming.CharacterEllipsis](./media/texttrimming-character.png "TextTrimming_Character")</span></span>

<span data-ttu-id="5423f-112">Wenn <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> auf **WordEllipsis** festgelegt wird, wird der Text gekürzt und mit einem Auslassungs Zeichen am Ende des ersten vollständigen Worts fortgesetzt, das dem gekürzten Rand am nächsten liegt.</span><span class="sxs-lookup"><span data-stu-id="5423f-112">When <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> is set to **WordEllipsis**, text is trimmed and continued with an ellipsis at the end of the first full word closest to the trimming edge.</span></span>  <span data-ttu-id="5423f-113">Diese Einstellung zeigt keine teilweise gekürzten Wörter an, sondern bewirkt, dass der Text nicht so nah wie die Einstellung für die Einstellung für die unter **Zeichnungs** Begrenzung auf den verkürzten Rand gekürzt wird.</span><span class="sxs-lookup"><span data-stu-id="5423f-113">This setting will not show partially trimmed words, but tends not to trim text as closely to the trimming edge as the **CharacterEllipsis** setting.</span></span>  <span data-ttu-id="5423f-114">Die folgende Abbildung zeigt die Auswirkung dieser Einstellung auf den <xref:System.Windows.Controls.TextBlock> oben definierten.</span><span class="sxs-lookup"><span data-stu-id="5423f-114">The following figure shows the effect of this setting on the <xref:System.Windows.Controls.TextBlock> defined above.</span></span>

<span data-ttu-id="5423f-115">![Beispiel: TextTrimming.WordEllipsis](./media/texttrimming-word.png "TextTrimming_Word")</span><span class="sxs-lookup"><span data-stu-id="5423f-115">![Example: TextTrimming.WordEllipsis](./media/texttrimming-word.png "TextTrimming_Word")</span></span>

<span data-ttu-id="5423f-116">Wenn <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> auf **None** festgelegt ist, wird keine Text Kürzung durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="5423f-116">When <xref:System.Windows.Controls.TextBlock.TextTrimming%2A> is set to **None**, no text trimming is performed.</span></span>  <span data-ttu-id="5423f-117">In diesem Fall wird Text einfach an der Begrenzung des übergeordneten Textcontainers zugeschnitten.</span><span class="sxs-lookup"><span data-stu-id="5423f-117">In this case, text is simply cropped to the boundary of the parent text container.</span></span>  <span data-ttu-id="5423f-118">Die folgende Abbildung zeigt die Auswirkung dieser Einstellung auf eine <xref:System.Windows.Controls.TextBlock> ähnlich der oben definierten.</span><span class="sxs-lookup"><span data-stu-id="5423f-118">The following figure shows the effect of this setting on a <xref:System.Windows.Controls.TextBlock> similar to the one defined above.</span></span>

<span data-ttu-id="5423f-119">![Beispiel: TextTrimming.None](./media/texttrimming-none.png "TextTrimming_None")</span><span class="sxs-lookup"><span data-stu-id="5423f-119">![Example: TextTrimming.None](./media/texttrimming-none.png "TextTrimming_None")</span></span>
