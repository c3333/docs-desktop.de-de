---
title: Beschleunigungsfunktionen
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- applying mathematical formulas to animations [WPF]
- applying easing functions to animations [WPF]
- mathematical formulas [WPF], applying to animations
- animations [WPF], realistic movement
- easing functions [WPF]
- customizing easing functions [WPF]
- easing functions [WPF], definition
- easing functions [WPF], customizing
- animations [WPF], applying
ms.assetid: 075b9c2b-82c4-43fa-b3cd-de0b6236eb38
ms.openlocfilehash: a25bde5098af853c3906a174a189fc35f33f0525
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977523"
---
# <a name="easing-functions"></a>Beschleunigungsfunktionen
Mit Beschleunigungsfunktionen können Sie benutzerdefinierte mathematische Formeln auf Animationen anwenden. Beispielsweise sollte Ihr Objekt realistisch springen oder sich so verhalten, als ob es sich auf einer Feder befinden würde. Sie können Keyframe- oder sogar From/To/By-Animationen verwenden, um sich diesen Effekten anzunähern, aber es würde eine erhebliche Menge an Arbeit bedeuten, und die Animation wäre weniger genau als die Verwendung einer mathematischen Formel.  
  
 Wenn Sie eine eigene benutzerdefinierte Beschleunigungs Funktion erstellen, indem <xref:System.Windows.Media.Animation.EasingFunctionBase> Sie von erben, können Sie eine von mehreren Beschleunigungsfunktionen verwenden, die von der Laufzeit bereitgestellt werden, um allgemeine Effekte zu erstellen.  
  
- <xref:System.Windows.Media.Animation.BackEase>: Zieht die Bewegung einer Animation etwas zurück, bevor die Animation im aufgeführten Pfad begonnen wird.  
  
- <xref:System.Windows.Media.Animation.BounceEase>: Erstellt einen Sprung-Effekt.  
  
- <xref:System.Windows.Media.Animation.CircleEase>: Erstellt eine Animation, die mit einer zirkulären Funktion beschleunigt und/oder verlangsamt.  
  
- <xref:System.Windows.Media.Animation.CubicEase>: Erstellt eine Animation, die mit der Formel *f*(*t*) = *t*<sup>3</sup>beschleunigt und/oder verlangsamt.  
  
- <xref:System.Windows.Media.Animation.ElasticEase>: Erstellt eine Animation, die einer springenden Bewegung ähnelt, bis Sie in den Ruhezustand versetzt wird.  
  
- <xref:System.Windows.Media.Animation.ExponentialEase>: Erstellt eine Animation, die mit einer Exponentialformel beschleunigt und/oder verlangsamt.  
  
- <xref:System.Windows.Media.Animation.PowerEase>: Erstellt eine Animation, die mit der Formel *f*(*t*) = *t*<sup>p</sup> beschleunigt und/oder verlangsamt, wobei p gleich der- <xref:System.Windows.Media.Animation.PowerEase.Power%2A> Eigenschaft ist.  
  
- <xref:System.Windows.Media.Animation.QuadraticEase>: Erstellt eine Animation, die mit der Formel *f*(*t*) = *t*<sup>2</sup>beschleunigt und/oder verlangsamt.  
  
- <xref:System.Windows.Media.Animation.QuarticEase>: Erstellt eine Animation, die mit der Formel *f*(*t*) = *t*<sup>4</sup>beschleunigt und/oder verlangsamt.  
  
- <xref:System.Windows.Media.Animation.QuinticEase>: Erstellen Sie eine Animation, die mit der Formel *f*(*t*) = *t*<sup>5</sup>beschleunigt und/oder verlangsamt.  
  
- <xref:System.Windows.Media.Animation.SineEase>: Erstellt eine Animation, die mit einer Sinus Formel beschleunigt und/oder verlangsamt.  
  
 Um eine Beschleunigungs Funktion auf eine Animation anzuwenden, verwenden Sie die- `EasingFunction` Eigenschaft der Animation, um die Beschleunigungs Funktion anzugeben, die auf die Animation angewendet werden soll. Im folgenden Beispiel wird eine Beschleunigungs <xref:System.Windows.Media.Animation.BounceEase> Funktion auf einen angewendet <xref:System.Windows.Media.Animation.DoubleAnimation> , um einen Sprung Effekt zu erstellen.  
  
 [!code-xaml[BounceEase_snippet#BounceEase](~/samples/snippets/csharp/VS_Snippets_Wpf/bounceease_snippet/CS/window1.xaml#bounceease)]  
  
 Im vorherigen Beispiel wurde die Beschleunigungsfunktion auf eine From/To/By-Animation angewendet. Sie können diese Beschleunigungsfunktionen auch auf Keyframe-Animationen anwenden. Im folgenden Beispiel wird veranschaulicht, wie mit Keyframes mit zugeordneten Beschleunigungsfunktionen verwendet werden, um eine Animation eines Rechtecks zu erstellen, das nach oben springt, verlangsamt, sich nach unten ausdehnt (als ob es fallen würde) und dann abprallt.  
  
 [!code-xaml[EasingFunctionDoubleKeyFrame_snippet#EasingFunctionDoubleKeyFrame](~/samples/snippets/csharp/VS_Snippets_Wpf/easingfunctiondoublekeyframe_snippet/CS/window1.xaml#easingfunctiondoublekeyframe)]  
  
 Sie können die- <xref:System.Windows.Media.Animation.EasingFunctionBase.EasingMode%2A> Eigenschaft verwenden, um zu ändern, wie sich die Beschleunigungs Funktion verhält, d. h., wie die Animation interpoliert. Hierfür gibt es drei mögliche Werte <xref:System.Windows.Media.Animation.EasingFunctionBase.EasingMode%2A> :  
  
- <xref:System.Windows.Media.Animation.EasingMode.EaseIn>: Interpolations folgt der mathematischen Formel, die der Beschleunigungs Funktion zugeordnet ist.  
  
- <xref:System.Windows.Media.Animation.EasingMode.EaseOut>: Interpolations folgt 100% Interpolationen abzüglich der Ausgabe der Formel, die der Beschleunigungs Funktion zugeordnet ist.  
  
- <xref:System.Windows.Media.Animation.EasingMode.EaseInOut>: Die Interpolation verwendet <xref:System.Windows.Media.Animation.EasingMode.EaseIn> für die erste Hälfte der Animation und <xref:System.Windows.Media.Animation.EasingMode.EaseOut> für die zweite Hälfte.  
  
 Die folgenden Diagramme veranschaulichen die unterschiedlichen Werte von, <xref:System.Windows.Media.Animation.EasingFunctionBase.EasingMode%2A> wobei *f*(*x*) den Animations Fortschritt darstellt und *t* die Zeit darstellt.  
  
 <xref:System.Windows.Media.Animation.BackEase>  
  
 ![BackEase-EasingMode-Diagramme](./media/backease-graph.png "BackEase_Graph")  
  
 <xref:System.Windows.Media.Animation.BounceEase>  
  
 ![BounceEase-EasingMode-Diagramme](./media/bounceease-graph.png "BounceEase_Graph")  
  
 <xref:System.Windows.Media.Animation.CircleEase>  
  
 ![CircleEase-EasingMode-Diagramme](./media/circleease-graph.png "CircleEase_Graph")  
  
 <xref:System.Windows.Media.Animation.CubicEase>  
  
 ![CubicEase-EasingMode-Diagramme](./media/cubicease-graph.png "CubicEase_Graph")  
  
 <xref:System.Windows.Media.Animation.ElasticEase>  
  
 ![ElasticEase mit Diagrammen von anderen EasingModes](./media/elasticease-graph.png "ElasticEase_Graph")  
  
 <xref:System.Windows.Media.Animation.ExponentialEase>  
  
 ![ExponentialEase-Diagramme von anderen EasingModes](./media/exponentialease-graph.png "ExponentialEase_Graph")  
  
 <xref:System.Windows.Media.Animation.PowerEase>  
  
 ![QuarticEase mit Diagrammen von anderen EasingModes](./media/quarticease-graph.png "QuarticEase_Graph")  
  
 <xref:System.Windows.Media.Animation.QuadraticEase>  
  
 ![QuadraticEase mit Diagrammen von anderen EasingModes](./media/quadraticease-graph.png "QuadraticEase_Graph")  
  
 <xref:System.Windows.Media.Animation.QuarticEase>  
  
 ![QuarticEase mit Diagrammen von anderen EasingModes](./media/quarticease-graph.png "QuarticEase_Graph")  
  
 <xref:System.Windows.Media.Animation.QuinticEase>  
  
 ![QuinticEase mit Diagrammen von anderen EasingModes](./media/quinticease-graph.png "QuinticEase_Graph")  
  
 <xref:System.Windows.Media.Animation.SineEase>  
  
 ![SineEase für andere EasingMode-Werte](./media/sineease-graph.png "SineEase_Graph")  
  
> [!NOTE]
> Sie können verwenden, <xref:System.Windows.Media.Animation.PowerEase> um das gleiche Verhalten wie <xref:System.Windows.Media.Animation.CubicEase> , <xref:System.Windows.Media.Animation.QuadraticEase> , <xref:System.Windows.Media.Animation.QuarticEase> und mit <xref:System.Windows.Media.Animation.QuinticEase> der- <xref:System.Windows.Media.Animation.PowerEase.Power%2A> Eigenschaft zu erstellen. Wenn Sie z <xref:System.Windows.Media.Animation.PowerEase> . b. zum Ersetzen von verwenden möchten <xref:System.Windows.Media.Animation.CubicEase> , geben Sie den <xref:System.Windows.Media.Animation.PowerEase.Power%2A> Wert 3 an.  
  
 Zusätzlich zur Verwendung der Beschleunigungsfunktionen, die in der Laufzeit enthalten sind, können Sie eigene benutzerdefinierte Beschleunigungsfunktionen erstellen, indem Sie von Erben <xref:System.Windows.Media.Animation.EasingFunctionBase> . Im folgenden Beispiel wird veranschaulicht, wie eine einfache benutzerdefinierte Beschleunigungsfunktion erstellt wird. Sie können Ihre eigene mathematische Logik zum Verhalten der Beschleunigungs Funktion hinzufügen, indem Sie die-Methode überschreiben <xref:System.Windows.Media.Animation.EasingFunctionBase.EaseInCore%2A> .
  
 [!code-csharp[CustomEasingFunction#CustomEasingFunction](~/samples/snippets/csharp/VS_Snippets_Wpf/customeasingfunction/csharp/customlog10easingfunction.cs#customeasingfunction)]
 [!code-vb[CustomEasingFunction#CustomEasingFunction](~/samples/snippets/visualbasic/VS_Snippets_Wpf/customeasingfunction/visualbasic/customlog10easingfunction.vb#customeasingfunction)]
 [!code-xaml[CustomEasingFunction#CustomEasingFunction](~/samples/snippets/csharp/VS_Snippets_Wpf/customeasingfunction/csharp/window1.xaml#customeasingfunction)]
