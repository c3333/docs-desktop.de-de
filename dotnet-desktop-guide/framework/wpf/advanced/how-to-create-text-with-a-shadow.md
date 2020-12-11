---
title: 'Gewusst wie: Erstellen von Text mit einem Schatten'
ms.date: 03/30/2017
helpviewer_keywords:
- typography [WPF], shadow effects
- shadow effects in text [WPF]
- text [WPF], shadowed
ms.assetid: 6ab9c754-6001-4708-b479-5367f2fd1a35
ms.openlocfilehash: 2b5298a4cdc2cf12c3cf44d06589c584accc7800
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977594"
---
# <a name="how-to-create-text-with-a-shadow"></a><span data-ttu-id="74228-102">Gewusst wie: Erstellen von Text mit einem Schatten</span><span class="sxs-lookup"><span data-stu-id="74228-102">How to: Create Text with a Shadow</span></span>
<span data-ttu-id="74228-103">Die Beispiele in diesem Abschnitt erklären, wie Sie einen Schatteneffekt für angezeigten Text erstellen.</span><span class="sxs-lookup"><span data-stu-id="74228-103">The examples in this section show how to create a shadow effect for displayed text.</span></span>  
  
## <a name="example"></a><span data-ttu-id="74228-104">Beispiel</span><span class="sxs-lookup"><span data-stu-id="74228-104">Example</span></span>  
 <span data-ttu-id="74228-105">Mit dem- <xref:System.Windows.Media.Effects.DropShadowEffect> Objekt können Sie eine Vielzahl von Drop Shadow-Effekten für- [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Objekte erstellen.</span><span class="sxs-lookup"><span data-stu-id="74228-105">The <xref:System.Windows.Media.Effects.DropShadowEffect> object allows you to create a variety of drop shadow effects for [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] objects.</span></span> <span data-ttu-id="74228-106">Das folgende Beispiel zeigt einen auf einen Text angewendeten Schlagschatteneffekt.</span><span class="sxs-lookup"><span data-stu-id="74228-106">The following example shows a drop shadow effect applied to text.</span></span> <span data-ttu-id="74228-107">In diesem Fall ist der Schatten ein weicher Schatten, d.h. die Schattenfarbe verwischt.</span><span class="sxs-lookup"><span data-stu-id="74228-107">In this case, the shadow is a soft shadow, which means the shadow color blurs.</span></span>  
  
 ![Text Schatten mit Weichheit &#61; 0,25](./media/how-to-create-text-with-a-shadow/drop-shadow-text-effect.jpg)
  
 <span data-ttu-id="74228-109">Sie können die Breite eines Schattens steuern, indem Sie die- <xref:System.Windows.Media.Effects.DropShadowEffect.ShadowDepth%2A> Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="74228-109">You can control the width of a shadow by setting the <xref:System.Windows.Media.Effects.DropShadowEffect.ShadowDepth%2A> property.</span></span> <span data-ttu-id="74228-110">Der Wert `4.0` gibt eine Schatten Breite von 4 Pixeln an.</span><span class="sxs-lookup"><span data-stu-id="74228-110">A value of `4.0` indicates a shadow width of 4 pixels.</span></span> <span data-ttu-id="74228-111">Durch Ändern der-Eigenschaft können Sie die Weichheit oder den weichungs Bereich eines Schattens steuern <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> .</span><span class="sxs-lookup"><span data-stu-id="74228-111">You can control the softness, or blur, of a shadow by modifying the <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> property.</span></span> <span data-ttu-id="74228-112">Der Wert gibt an, dass `0.0` kein blurring besteht.</span><span class="sxs-lookup"><span data-stu-id="74228-112">A value of `0.0` indicates no blurring.</span></span> <span data-ttu-id="74228-113">Im folgenden Codebeispiel wird gezeigt, wie ein weicher Schatten erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="74228-113">The following code example shows how to create a soft shadow.</span></span>  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet1](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/SingleShadows.xaml#textshadowsnippet1)]  
  
> [!NOTE]
> <span data-ttu-id="74228-114">Diese Schatteneffekte durchlaufen nicht die [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Text Rendering-Pipeline.</span><span class="sxs-lookup"><span data-stu-id="74228-114">These shadow effects do not go through the [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] text rendering pipeline.</span></span> <span data-ttu-id="74228-115">Daher ist ClearType bei Verwendung dieser Effekte deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="74228-115">As a result, ClearType is disabled when using these effects.</span></span>  
  
 <span data-ttu-id="74228-116">Das folgende Beispiel zeigt einen auf einen Text angewendeten harten Schlagschatteneffekt.</span><span class="sxs-lookup"><span data-stu-id="74228-116">The following example shows a hard drop shadow effect applied to text.</span></span> <span data-ttu-id="74228-117">In diesem Fall wird der Schatten nicht verwischt.</span><span class="sxs-lookup"><span data-stu-id="74228-117">In this case, the shadow is not blurred.</span></span>  
  
 ![Text Schatten mit Weichheit &#61; 0](./media/how-to-create-text-with-a-shadow/text-shadow-softness.jpg)
  
 <span data-ttu-id="74228-119">Sie können einen harten Schatten erstellen, indem Sie die- <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> Eigenschaft auf festlegen `0.0` . Dies bedeutet, dass kein Weichzeichner verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="74228-119">You can create a hard shadow by setting the <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> property to `0.0`, which indicates that no blurring is used.</span></span> <span data-ttu-id="74228-120">Sie können die Richtung des Schattens steuern, indem Sie die- <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> Eigenschaft ändern.</span><span class="sxs-lookup"><span data-stu-id="74228-120">You can control the direction of the shadow by modifying the <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> property.</span></span> <span data-ttu-id="74228-121">Legen Sie den direktionalen Wert dieser Eigenschaft auf einen Grad zwischen `0` und fest `360` .</span><span class="sxs-lookup"><span data-stu-id="74228-121">Set the directional value of this property to a degree between `0` and `360`.</span></span> <span data-ttu-id="74228-122">Die folgende Abbildung zeigt die direktionalen Werte der- <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> Eigenschaften Einstellung.</span><span class="sxs-lookup"><span data-stu-id="74228-122">The following illustration shows the directional values of the <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> property setting.</span></span>  
  
 ![DropShadow-Gradeinstellung für Schatten](./media/how-to-create-text-with-a-shadow/drop-shadow-degree-setting.png)
  
 <span data-ttu-id="74228-124">Im folgenden Codebeispiel wird das Erstellen eines harten Schattens veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="74228-124">The following code example shows how to create a hard shadow.</span></span>  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/SingleShadows.xaml#textshadowsnippet2)]  
  
## <a name="using-a-blur-effect"></a><span data-ttu-id="74228-125">Verwenden eines Weichzeichnereffekts</span><span class="sxs-lookup"><span data-stu-id="74228-125">Using a Blur Effect</span></span>  
 <span data-ttu-id="74228-126">Ein <xref:System.Windows.Media.Effects.BlurBitmapEffect> kann verwendet werden, um einen Schatten ähnlichen Effekt zu erstellen, der hinter einem Textobjekt platziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="74228-126">A <xref:System.Windows.Media.Effects.BlurBitmapEffect> can be used to create a shadow-like effect that can be placed behind a text object.</span></span> <span data-ttu-id="74228-127">Ein auf Text angewendeter Weichzeichner-Bitmapeffekt verwischt Text gleichmäßig in alle Richtungen.</span><span class="sxs-lookup"><span data-stu-id="74228-127">A blur bitmap effect applied to text blurs the text evenly in all directions.</span></span>  
  
 <span data-ttu-id="74228-128">Das folgende Beispiel zeigt einen Text mit Weichzeichnereffekt.</span><span class="sxs-lookup"><span data-stu-id="74228-128">The following example shows a blur effect applied to text.</span></span>  
  
 ![Textschatten mit einem BlurBitmapEffect](./media/how-to-create-text-with-a-shadow/text-shadow-blur-effect.jpg)  
  
 <span data-ttu-id="74228-130">Im folgenden Codebeispiel wird das Erstellen eines Weichzeichnereffekts veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="74228-130">The following code example shows how to create a blur effect.</span></span>  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet6](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/BlurShadows.xaml#textshadowsnippet6)]  
  
## <a name="using-a-translate-transform"></a><span data-ttu-id="74228-131">Verwenden von TranslateTransform</span><span class="sxs-lookup"><span data-stu-id="74228-131">Using a Translate Transform</span></span>  
 <span data-ttu-id="74228-132">Ein <xref:System.Windows.Media.TranslateTransform> kann verwendet werden, um einen Schatten ähnlichen Effekt zu erstellen, der hinter einem Textobjekt platziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="74228-132">A <xref:System.Windows.Media.TranslateTransform> can be used to create a shadow-like effect that can be placed behind a text object.</span></span>  
  
 <span data-ttu-id="74228-133">Im folgenden Codebeispiel wird ein <xref:System.Windows.Media.TranslateTransform> zum Offset von Text verwendet.</span><span class="sxs-lookup"><span data-stu-id="74228-133">The following code example uses a <xref:System.Windows.Media.TranslateTransform> to offset text.</span></span> <span data-ttu-id="74228-134">In diesem Beispiel erstellt eine geringfügig versetzte Kopie des Textes hinter dem primären Text einen Schatteneffekt.</span><span class="sxs-lookup"><span data-stu-id="74228-134">In this example, a slightly offset copy of text below the primary text creates a shadow effect.</span></span>  
  
 ![Textschatten mit einem TranslateTransform](./media/how-to-create-text-with-a-shadow/text-transform-shadow-effect.jpg)
  
 <span data-ttu-id="74228-136">Im folgenden Codebeispiel wird das Erstellen einer Transformation für einen Schatteneffekt veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="74228-136">The following code example shows how to create a transform for a shadow effect.</span></span>  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet7](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/TransformShadows.xaml#textshadowsnippet7)]
