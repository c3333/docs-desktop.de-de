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
# <a name="how-to-create-text-with-a-shadow"></a>Gewusst wie: Erstellen von Text mit einem Schatten
Die Beispiele in diesem Abschnitt erklären, wie Sie einen Schatteneffekt für angezeigten Text erstellen.  
  
## <a name="example"></a>Beispiel  
 Mit dem- <xref:System.Windows.Media.Effects.DropShadowEffect> Objekt können Sie eine Vielzahl von Drop Shadow-Effekten für- [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Objekte erstellen. Das folgende Beispiel zeigt einen auf einen Text angewendeten Schlagschatteneffekt. In diesem Fall ist der Schatten ein weicher Schatten, d.h. die Schattenfarbe verwischt.  
  
 ![Text Schatten mit Weichheit &#61; 0,25](./media/how-to-create-text-with-a-shadow/drop-shadow-text-effect.jpg)
  
 Sie können die Breite eines Schattens steuern, indem Sie die- <xref:System.Windows.Media.Effects.DropShadowEffect.ShadowDepth%2A> Eigenschaft festlegen. Der Wert `4.0` gibt eine Schatten Breite von 4 Pixeln an. Durch Ändern der-Eigenschaft können Sie die Weichheit oder den weichungs Bereich eines Schattens steuern <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> . Der Wert gibt an, dass `0.0` kein blurring besteht. Im folgenden Codebeispiel wird gezeigt, wie ein weicher Schatten erstellt wird.  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet1](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/SingleShadows.xaml#textshadowsnippet1)]  
  
> [!NOTE]
> Diese Schatteneffekte durchlaufen nicht die [!INCLUDE[TLA#tla_winclient](../../../includes/tlasharptla-winclient-md.md)] Text Rendering-Pipeline. Daher ist ClearType bei Verwendung dieser Effekte deaktiviert.  
  
 Das folgende Beispiel zeigt einen auf einen Text angewendeten harten Schlagschatteneffekt. In diesem Fall wird der Schatten nicht verwischt.  
  
 ![Text Schatten mit Weichheit &#61; 0](./media/how-to-create-text-with-a-shadow/text-shadow-softness.jpg)
  
 Sie können einen harten Schatten erstellen, indem Sie die- <xref:System.Windows.Media.Effects.DropShadowEffect.BlurRadius%2A> Eigenschaft auf festlegen `0.0` . Dies bedeutet, dass kein Weichzeichner verwendet wird. Sie können die Richtung des Schattens steuern, indem Sie die- <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> Eigenschaft ändern. Legen Sie den direktionalen Wert dieser Eigenschaft auf einen Grad zwischen `0` und fest `360` . Die folgende Abbildung zeigt die direktionalen Werte der- <xref:System.Windows.Media.Effects.DropShadowEffect.Direction%2A> Eigenschaften Einstellung.  
  
 ![DropShadow-Gradeinstellung für Schatten](./media/how-to-create-text-with-a-shadow/drop-shadow-degree-setting.png)
  
 Im folgenden Codebeispiel wird das Erstellen eines harten Schattens veranschaulicht.  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet2](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/SingleShadows.xaml#textshadowsnippet2)]  
  
## <a name="using-a-blur-effect"></a>Verwenden eines Weichzeichnereffekts  
 Ein <xref:System.Windows.Media.Effects.BlurBitmapEffect> kann verwendet werden, um einen Schatten ähnlichen Effekt zu erstellen, der hinter einem Textobjekt platziert werden kann. Ein auf Text angewendeter Weichzeichner-Bitmapeffekt verwischt Text gleichmäßig in alle Richtungen.  
  
 Das folgende Beispiel zeigt einen Text mit Weichzeichnereffekt.  
  
 ![Textschatten mit einem BlurBitmapEffect](./media/how-to-create-text-with-a-shadow/text-shadow-blur-effect.jpg)  
  
 Im folgenden Codebeispiel wird das Erstellen eines Weichzeichnereffekts veranschaulicht.  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet6](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/BlurShadows.xaml#textshadowsnippet6)]  
  
## <a name="using-a-translate-transform"></a>Verwenden von TranslateTransform  
 Ein <xref:System.Windows.Media.TranslateTransform> kann verwendet werden, um einen Schatten ähnlichen Effekt zu erstellen, der hinter einem Textobjekt platziert werden kann.  
  
 Im folgenden Codebeispiel wird ein <xref:System.Windows.Media.TranslateTransform> zum Offset von Text verwendet. In diesem Beispiel erstellt eine geringfügig versetzte Kopie des Textes hinter dem primären Text einen Schatteneffekt.  
  
 ![Textschatten mit einem TranslateTransform](./media/how-to-create-text-with-a-shadow/text-transform-shadow-effect.jpg)
  
 Im folgenden Codebeispiel wird das Erstellen einer Transformation für einen Schatteneffekt veranschaulicht.  
  
 [!code-xaml[TextShadowSnippets#TextShadowSnippet7](~/samples/snippets/csharp/VS_Snippets_Wpf/TextShadowSnippets/CS/TransformShadows.xaml#textshadowsnippet7)]
