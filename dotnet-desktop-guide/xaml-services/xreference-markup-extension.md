---
title: x:Reference-Markuperweiterung
ms.date: 03/30/2017
helpviewer_keywords:
- x:Reference markup extension [XAML Services]
- XAML [XAML Services], x:Reference Markup Extension
- Reference markup extension [XAML Services]
ms.assetid: 2982e68b-d26b-4aa3-826a-34c57a9c5199
ms.openlocfilehash: f06e259893111a436e5afe2df754c3edee326d54
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975374"
---
# <a name="xreference-markup-extension"></a>x:Reference-Markuperweiterung

Verweist auf eine-Instanz, die an anderer Stelle in XAML-Markup deklariert wird. Der Verweis bezieht sich auf die eines Elements `x:Name` .

## <a name="xaml-attribute-usage"></a>Verwendung von XAML-Attributen

```xaml
<object property="{x:Reference instancexName}" .../>
```

## <a name="xaml-object-element-usage"></a>Verwendung von XAML-Objektelementen

```xaml
<object>
  <object.property>
    <x:Reference Name="instancexName"/>
  </object.property>
</object>
```

## <a name="xaml-values"></a>XAML-Werte

|||
|-|-|
|`instancexName`|Der `x:Name` Wert (oder Wert der <xref:System.Windows.Markup.RuntimeNamePropertyAttribute> identifizierten Eigenschaft) der Instanz, auf die verwiesen wird.|

## <a name="remarks"></a>Bemerkungen

`x:Reference` bietet Unterstützung auf XAML-Sprachebene für ein Element Verweis Konzept, das anderweitig in bestimmten Frameworks wie WPF implementiert wurde.

## <a name="xreference-and-wpf"></a>x:Reference und WPF

In WPF und XAML 2006 werden Element Verweise durch die Funktion der Bindung auf Frameworkebene adressiert <xref:System.Windows.Data.Binding.ElementName%2A> . Für die meisten WPF-Anwendungen und-Szenarien <xref:System.Windows.Data.Binding.ElementName%2A> sollte die Bindung weiterhin verwendet werden. Ausnahmen zu dieser allgemeinen Anleitung können Fälle enthalten, in denen Datenkontext oder andere Bereichs Überlegungen vorhanden sind, die die Datenbindung nicht praktikabel machen und bei denen die Markup Kompilierung nicht beteiligt ist.

`x:Reference` ist ein Konstrukt, das in XAML 2009 definiert ist. In WPF können Sie XAML 2009-Funktionen verwenden, jedoch nur für XAML, das nicht WPF-markupkompiliert ist. Markupkompilierte XAML und die BAML-Form von XAML unterstützen die XAML 2009-Schlüsselwörter und -Funktionen derzeit nicht.
