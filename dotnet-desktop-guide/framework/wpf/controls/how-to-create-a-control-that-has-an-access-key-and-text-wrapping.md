---
title: 'Gewusst wie: Erstellen eines Steuerelements, das über eine Tastenkombination und Textumbruch verfügt'
ms.date: 03/30/2017
helpviewer_keywords:
- access keys [WPF], control for
- controls [WPF], text wrapping
- wrapping text [WPF]
- keys [WPF], control for
- controls [WPF], access keys
- text wrapping [WPF]
ms.assetid: 205099d9-2551-4302-a25e-a15af9f67e04
ms.openlocfilehash: 86239374ca9cb3bd3d71415496e32d4a27fbae5a
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96978076"
---
# <a name="how-to-create-a-control-that-has-an-access-key-and-text-wrapping"></a><span data-ttu-id="f7dda-102">Gewusst wie: Erstellen eines Steuerelements, das über eine Tastenkombination und Textumbruch verfügt</span><span class="sxs-lookup"><span data-stu-id="f7dda-102">How to: Create a Control That Has an Access Key and Text Wrapping</span></span>

<span data-ttu-id="f7dda-103">Diese Beispiel veranschaulicht, wie Sie ein Steuerelement erstellen, das über eine Tastenkombination verfügt und das Umbrechen von Text unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f7dda-103">This example shows how to create a control that has an access key and supports text wrapping.</span></span> <span data-ttu-id="f7dda-104">Im Beispiel wird ein-Steuerelement verwendet <xref:System.Windows.Controls.Label> , um diese Konzepte zu veranschaulichen.</span><span class="sxs-lookup"><span data-stu-id="f7dda-104">The example uses a <xref:System.Windows.Controls.Label> control to illustrate these concepts.</span></span>  
  
## <a name="example"></a><span data-ttu-id="f7dda-105">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f7dda-105">Example</span></span>  

 <span data-ttu-id="f7dda-106">**Umbrechen des Texts einer Bezeichnung**</span><span class="sxs-lookup"><span data-stu-id="f7dda-106">**Add Text Wrapping to Your Label**</span></span>  
  
 <span data-ttu-id="f7dda-107">Das- <xref:System.Windows.Controls.Label> Steuerelement unterstützt keine Text Umbrüchen.</span><span class="sxs-lookup"><span data-stu-id="f7dda-107">The <xref:System.Windows.Controls.Label> control does not support text wrapping.</span></span> <span data-ttu-id="f7dda-108">Wenn sich eine Bezeichnung über mehrere Zeilen erstrecken soll, können Sie ein anderes Element verschachteln, das das Umbrechen von Text unterstützt, und es innerhalb der Bezeichnung platzieren.</span><span class="sxs-lookup"><span data-stu-id="f7dda-108">If you need a label that wraps across multiple lines, you can nest another element that does support text wrapping and put the element inside the label.</span></span> <span data-ttu-id="f7dda-109">Im folgenden Beispiel wird gezeigt, wie Sie mit einem <xref:System.Windows.Controls.TextBlock> eine Bezeichnung erstellen, die mehrere Textzeilen umschließt.</span><span class="sxs-lookup"><span data-stu-id="f7dda-109">The following example shows how to use a <xref:System.Windows.Controls.TextBlock> to make a label that wraps several lines of text.</span></span>  
  
 [!code-xaml[LabelSnippet#5](~/samples/snippets/csharp/VS_Snippets_Wpf/LabelSnippet/CS/Pane1.xaml#5)]  
  
 <span data-ttu-id="f7dda-110">**Hinzufügen von Textumbruch und einer Tastenkombination zu einer Bezeichnung**</span><span class="sxs-lookup"><span data-stu-id="f7dda-110">**Add an Access Key and Text Wrapping to Your Label**</span></span>  
  
 <span data-ttu-id="f7dda-111">Wenn Sie ein- <xref:System.Windows.Controls.Label> Element benötigen, das über eine Zugriffstaste (mnetmonic) verfügt, verwenden Sie das-Element, das <xref:System.Windows.Controls.AccessText> sich in befindet <xref:System.Windows.Controls.Label> .</span><span class="sxs-lookup"><span data-stu-id="f7dda-111">If you need a <xref:System.Windows.Controls.Label> that has an access key (mnemonic), use the <xref:System.Windows.Controls.AccessText> element that is inside the <xref:System.Windows.Controls.Label>.</span></span>  
  
 <span data-ttu-id="f7dda-112">Steuerelemente wie <xref:System.Windows.Controls.Label> , <xref:System.Windows.Controls.Button> , <xref:System.Windows.Controls.RadioButton> , <xref:System.Windows.Controls.CheckBox> , <xref:System.Windows.Controls.MenuItem> , <xref:System.Windows.Controls.TabItem> , <xref:System.Windows.Controls.Expander> und <xref:System.Windows.Controls.GroupBox> verfügen über Standard Steuerelement Vorlagen.</span><span class="sxs-lookup"><span data-stu-id="f7dda-112">Controls such as <xref:System.Windows.Controls.Label>, <xref:System.Windows.Controls.Button>, <xref:System.Windows.Controls.RadioButton>, <xref:System.Windows.Controls.CheckBox>, <xref:System.Windows.Controls.MenuItem>, <xref:System.Windows.Controls.TabItem>, <xref:System.Windows.Controls.Expander>, and <xref:System.Windows.Controls.GroupBox> have default control templates.</span></span> <span data-ttu-id="f7dda-113">Diese Vorlagen enthalten einen <xref:System.Windows.Controls.ContentPresenter> .</span><span class="sxs-lookup"><span data-stu-id="f7dda-113">These templates contain a <xref:System.Windows.Controls.ContentPresenter>.</span></span> <span data-ttu-id="f7dda-114">Eine der Eigenschaften, die Sie für das festlegen können <xref:System.Windows.Controls.ContentPresenter> <xref:System.Windows.Controls.ContentPresenter.RecognizesAccessKey%2A> , ist = "true", mit dem Sie einen Zugriffsschlüssel für das Steuerelement angeben können.</span><span class="sxs-lookup"><span data-stu-id="f7dda-114">One of the properties that you can set on the <xref:System.Windows.Controls.ContentPresenter> is <xref:System.Windows.Controls.ContentPresenter.RecognizesAccessKey%2A>="true", which you can use to specify an access key for the control.</span></span>  
  
 <span data-ttu-id="f7dda-115">Im folgenden Beispiel wird gezeigt, wie ein erstellt wird <xref:System.Windows.Controls.Label> , das über eine Zugriffstaste verfügt und Text Umbrüchen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f7dda-115">The following example shows how to create a <xref:System.Windows.Controls.Label> that has an access key and supports text wrapping.</span></span> <span data-ttu-id="f7dda-116">Um das Umbenennen von Text zu aktivieren, wird im Beispiel die <xref:System.Windows.Controls.AccessText.TextWrapping%2A> -Eigenschaft festgelegt und ein Unterstrich verwendet, um die Zugriffstaste anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f7dda-116">To enable text wrapping, the example sets the <xref:System.Windows.Controls.AccessText.TextWrapping%2A> property and uses an underline character to specify the access key.</span></span> <span data-ttu-id="f7dda-117">(Das Zeichen, das unmittelbar auf den Unterstrich folgt, ist die Tastenkombination.)</span><span class="sxs-lookup"><span data-stu-id="f7dda-117">(The character that immediately follows the underline character is the access key.)</span></span>  
  
 [!code-xaml[LabelSnippet#4](~/samples/snippets/csharp/VS_Snippets_Wpf/LabelSnippet/CS/Pane1.xaml#4)]  
  
## <a name="see-also"></a><span data-ttu-id="f7dda-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7dda-118">See also</span></span>

- <span data-ttu-id="f7dda-119">[Vorgehensweise: Festlegen der Eigenschaft „Target“ einer Bezeichnung](/previous-versions/dotnet/netframework-3.5/ms752101(v=vs.90))</span><span class="sxs-lookup"><span data-stu-id="f7dda-119">[How to: Set the Target Property of a Label](/previous-versions/dotnet/netframework-3.5/ms752101(v=vs.90))</span></span>
