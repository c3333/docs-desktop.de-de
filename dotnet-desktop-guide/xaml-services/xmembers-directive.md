---
title: x:Members-Anweisung
ms.date: 03/30/2017
ms.assetid: 155b393d-3b49-4c5a-8c9e-b3d9893af4e4
ms.openlocfilehash: c751a4f1cdea8dce7ef5165f5225ab3a825c7344
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975389"
---
# <a name="xmembers-directive"></a>x:Members-Anweisung
Enthält eine Reihe von Membern, die im Markup definiert sind und auf die x:-Klasse des übergeordneten Elements angewendet werden.

## <a name="xaml-attribute-usage"></a>Verwendung von XAML-Attributen

```xaml
<object x:Class="className">
<x:Members>
  oneOrMoreMembers
</x:Members
</object>
```

## <a name="xaml-values"></a>XAML-Werte

|||
|-|-|
|`className`|Der Name der Sicherungsklasse oder partiellen Klasse für die XAML-Produktion. Siehe Hinweise.|
|`oneOrMoreMembers`|Ein oder mehrere Objekt Elemente, die Element Definitionen darstellen. In der Regel handelt es sich hierbei um `x:Property` Objekt Elemente. Siehe Hinweise.|

## <a name="remarks"></a>Bemerkungen

Bei der Implementierung von .net XAML-Diensten gibt es keine Unterstützungs Klasse oder zugrunde liegende Member-Implementierung für `x:Members` . `x:Members` ist ein spezieller XAML-Member, der als Member für einen beliebigen Typ vorhanden sein kann. In einem XAML-knotenstream wird im XAML- `x:Members` `Members` Namespace der XAML-Sprache als Member mit dem Namen dargestellt. Der Member `Members` enthält eine schreibgeschützte generische Liste von- `Member` Objekten. Im typischen Markup werden die einzelnen Member als `x:Property` Eigenschafts Elemente angegeben. `x:Property` ist ein genauerer Typ speziell für Eigenschaften von Typen, der zugewiesen werden kann `x:Member` . Weitere Informationen finden Sie unter [x:property-Direktive](xproperty-directive.md).

Damit eine praktische Verwendung von `x:Members` als Mittel zum Angeben von Memberdefinitionen in Markup unterstützt wird, müssen die Member einer Klasse zugeordnet sein, die geändert werden kann. Das beabsichtigte Modell besteht darin, dass `x:Members` als ein Member eines Typs vorhanden ist, der eine `x:Class` angibt. Der Mechanismus zum Zuordnen von Typen und Membern oder zum Erstellen dynamischer Element Definitionen wird jedoch auf der Ebene der .net XAML-Dienste nicht unterstützt. Dies wird von einzelnen Frameworks übernommen, die Anwendungsmodelle haben, die Memberdefinitionen von XAML unterstützen. In der Regel sind, damit dieses Feature unterstützt wird, MSBUILD-Buildvorgänge erforderlich, die XAML als Markup kompilieren und es als CodeBehind integrieren oder reine Von-XAML-Assemblys generieren.

## <a name="xmembers-for-windows-workflow-foundation"></a>x:Members für Windows Workflow Foundation

Enthält für Windows Workflow Foundation `x:Members` die Member einer benutzerdefinierten Aktivität, die vollständig in XAML erstellt wurde, oder XAML – definierte dynamische Member für einen Aktivitäts Designer mit Code Behind. `x:Class` muss auch für das Stammelement der XAML-Produktion angegeben werden. Dies ist keine Voraussetzung für die .net XAML-Dienst Ebene, sondern wird eine Anforderung, wenn die XAML-Produktion von den MSBuild-Buildaktionen geladen wird, die benutzerdefinierte Aktivitäten unterstützen, und Windows Workflow Foundation XAML im Allgemeinen. `x:Members` muss das erste untergeordnete Element im Markup des Object-Elements sein, das deklariert `x:Class` .
