---
title: 'Gewusst wie: Hinzufügen von benutzerdefinierten Daten zu Freihanddaten'
ms.date: 03/30/2017
helpviewer_keywords:
- ink data [WPF], adding custom data
- InkCanvas [WPF], displaying
ms.assetid: f02aac6f-3436-4f7c-b6ea-0452cba5332c
ms.openlocfilehash: 7c59a205df5358daec101339cc6a308c8e38a9d6
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976568"
---
# <a name="how-to-add-custom-data-to-ink-data"></a>Gewusst wie: Hinzufügen von benutzerdefinierten Daten zu Freihanddaten
Sie können frei Hand Eingaben benutzerdefinierte Daten hinzufügen, die gespeichert werden, wenn die frei Hand Eingabe als frei Hand Format (Ink serialisiert Format) gespeichert wird.  Sie können die benutzerdefinierten Daten in <xref:System.Windows.Ink.DrawingAttributes> , oder speichern <xref:System.Windows.Ink.StrokeCollection> <xref:System.Windows.Ink.Stroke> .  Wenn Sie benutzerdefinierte Daten in drei Objekten speichern können, können Sie entscheiden, ob die Daten am besten gespeichert werden sollen.  Alle drei Klassen verwenden ähnliche Methoden zum Speichern und Zugreifen auf benutzerdefinierte Daten.  
  
 Nur die folgenden Typen können als benutzerdefinierte Daten gespeichert werden:  
  
- <xref:System.Boolean>  
  
- <xref:System.Boolean>[]  
  
- <xref:System.Byte>  
  
- <xref:System.Byte>[]  
  
- <xref:System.Char>  
  
- <xref:System.Char>[]  
  
- <xref:System.DateTime>  
  
- <xref:System.DateTime>[]  
  
- <xref:System.Decimal>  
  
- <xref:System.Decimal>[]  
  
- <xref:System.Double>  
  
- <xref:System.Double>[]  
  
- <xref:System.Int16>  
  
- <xref:System.Int16>[]  
  
- <xref:System.Int32>  
  
- <xref:System.Int32>[]  
  
- <xref:System.Int64>  
  
- <xref:System.Int64>[]  
  
- <xref:System.Single>  
  
- <xref:System.Single>[]  
  
- <xref:System.String>  
  
- <xref:System.UInt16>  
  
- <xref:System.UInt16>[]  
  
- <xref:System.UInt32>  
  
- <xref:System.UInt32>[]  
  
- <xref:System.UInt64>  
  
- <xref:System.UInt64>[]  
  
## <a name="example"></a>Beispiel  
 Im folgenden Beispiel wird veranschaulicht, wie benutzerdefinierte Daten aus einem hinzugefügt und abgerufen werden <xref:System.Windows.Ink.StrokeCollection> .  
  
 [!code-csharp[HowToAddCustomDataToInk#1](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAddCustomDataToInk/CSharp/Window1.xaml.cs#1)]  
  
 Im folgenden Beispiel wird eine Anwendung erstellt, die eine <xref:System.Windows.Controls.InkCanvas> und zwei Schaltflächen anzeigt.  Mit der Schaltfläche `switchAuthor` können zwei Stifte von zwei verschiedenen Autoren verwendet werden.  Die Schaltfläche `changePenColors` ändert die Farbe jedes Strichs in der <xref:System.Windows.Controls.InkCanvas> entsprechend dem Autor.  Die Anwendung definiert zwei <xref:System.Windows.Ink.DrawingAttributes> -Objekte und fügt jeder eine benutzerdefinierte Eigenschaft hinzu, die angibt, welcher Autor die gezeichnet hat <xref:System.Windows.Ink.Stroke> .  Wenn der Benutzer `changePenColors` auf klickt, ändert die Anwendung die Darstellung des Strichs entsprechend dem Wert der benutzerdefinierten Eigenschaft.  
  
 [!code-xaml[HowToAddCustomDataToInk#2](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAddCustomDataToInk/CSharp/Window1.xaml#2)]  
  
 [!code-csharp[HowToAddCustomDataToInk#3](~/samples/snippets/csharp/VS_Snippets_Wpf/HowToAddCustomDataToInk/CSharp/Window1.xaml.cs#3)]
