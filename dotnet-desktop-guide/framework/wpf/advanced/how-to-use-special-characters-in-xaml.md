---
title: 'Gewusst wie: Verwenden von Sonderzeichen in XAML'
description: Erfahren Sie mehr über die Syntax für das Codieren von Sonderzeichen im Unicode-UTF-8-Dateiformat in Visual Studio zur Verwendung in XAML-Dateien in Windows Presentation Foundation.
ms.date: 03/30/2017
helpviewer_keywords:
- Unicode UTF-8 file format
- UTF-8 file format
- characters [WPF], special
- typography [WPF], special characters
- special characters [WPF]
ms.assetid: a57776d1-f353-4794-afa0-bfa3c712ed1c
ms.openlocfilehash: b627f7ee1d6ab80d5d1cd14de0339a1afad3ec62
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96977838"
---
# <a name="how-to-use-special-characters-in-xaml"></a>Gewusst wie: Verwenden von Sonderzeichen in XAML
Markup Dateien, die in Visual Studio erstellt werden, werden automatisch im Unicode-UTF-8-Dateiformat gespeichert, was bedeutet, dass die meisten Sonderzeichen (z. b. Akzentzeichen) ordnungsgemäß codiert werden. Es gibt jedoch eine Reihe von häufig verwendeten Sonderzeichen, die anders behandelt werden. Diese Sonderzeichen folgen dem [W3C (World Wide Web Consortium)-XML-Standard für die Codierung](https://www.w3resource.com/xml/reserved-markup-characters.php).

Die folgende Tabelle zeigt die Syntax zum Codieren dieser Sonderzeichen:

| Zeichen | Syntax   | BESCHREIBUNG          |
|-----------|----------|----------------------|
| `<`       | `&lt;`   | Kleiner als-Zeichen.    |
| `>`       | `&gt;`   | Größer als-Zeichen   |
| `&`       | `&amp;`  | Und-Zeichen (&)    |
| `"`       | `&quot;` | Doppeltes Anführungszeichen |
| `'`       | `&apos;` | Einfache Anführungszeichen. |

> [!NOTE]
> Wenn Sie eine Markup Datei mit einem Text-Editor erstellen, z. b. Windows Notepad, müssen Sie die Datei im Unicode-UTF-8-Dateiformat speichern, um alle codierten Sonderzeichen beizubehalten.

Das folgende Beispiel zeigt, wie Sie Sonderzeichen im Text beim Erstellen von Markup verwenden können.

## <a name="example"></a>Beispiel

[!code-xaml[SpecialCharsSnippets#SpecialCharsSnippet1](~/samples/snippets/csharp/VS_Snippets_Wpf/SpecialCharsSnippets/CS/Window1.xaml#specialcharssnippet1)]
