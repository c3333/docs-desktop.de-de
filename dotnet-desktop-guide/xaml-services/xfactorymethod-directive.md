---
title: x:FactoryMethod-Anweisung
ms.date: 03/30/2017
helpviewer_keywords:
- XAML. x:FactoryMethod directive [XAML Services]
- FactoryMethod directive in XAML [XAML Services]
- x:FactoryMethod directive [XAML Services]
ms.assetid: 829bcbdf-5318-4afb-9a03-c310e0d2f23d
ms.openlocfilehash: 5e864b6f5d664b079036a5d915e2f6f81b83639f
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975393"
---
# <a name="xfactorymethod-directive"></a>x:FactoryMethod-Anweisung
Gibt eine andere Methode als einen Konstruktor an, der von einem XAML-Prozessor zum Initialisieren eines Objekts nach der Auflösung des Unterstützungs Typs verwendet werden soll.  
  
## <a name="xaml-attribute-usage-no-xarguments"></a>Verwendung von XAML-Attributen, keine x:Arguments  
  
```xaml  
<object x:FactoryMethod="methodname"...>  
  ...  
</object>  
```  
  
## <a name="xaml-attribute-usage-xarguments-as-elements"></a>Verwendung von XAML-Attributen, x:Arguments als Element (e)  
  
```xaml  
<object x:FactoryMethod="methodname"...>  
  <x:Arguments>  
    oneOrMoreObjectElements  
  </x:Arguments>  
</object>  
```  
  
## <a name="xaml-values"></a>XAML-Werte  
  
|||  
|-|-|  
|`methodname`|Der Name der Zeichen folgen Methode einer Methode, die XAML-Prozessoren aufruft, um die Instanz zu initialisieren, die als angegeben wird `object` . Siehe Hinweise.|  
|`oneOrMoreObjectElements`|Ein oder mehrere Objekt Elemente für-Objekte, die factorymethodenparameter angeben. Die Reihenfolge ist wichtig. Sie gibt die Reihenfolge an, in der Argumente an die Factorymethode geleitet werden sollen.|  
  
## <a name="remarks"></a>Bemerkungen  
 Wenn `methodname` eine Instanzmethode ist, kann Sie nicht qualifiziert werden.  
  
 Statische Methoden als Factorymethoden werden unterstützt. Wenn `methodname` eine statische Methode ist, `methodname` wird als Kombination bereitgestellt `typeName.methodName` , wobei `typeName` die Klasse benennt, die die statische Factorymethode definiert. `typeName` kann als Präfix qualifiziert werden, wenn auf einen Typ in einem zugeordneten xmlns verwiesen wird. `typeName` kann ein anderer Typ sein als `typeof(object)` .  
  
 Die Factorymethode muss eine deklarierte öffentliche Methode des Typs sein, der das relevante Objekt Element unterstützt.  
  
 Die Factorymethode muss eine Instanz zurückgeben, die dem relevanten Objekt zugewiesen werden kann. Factorymethoden sollten niemals NULL zurückgeben.  
  
 `x:Arguments` arbeitet mit einem Prinzip der besten Entsprechung für Signaturen von Factorymethoden. Bei der Übereinstimmung wird die Parameter Anzahl zuerst ausgewertet. Wenn mehr als eine mögliche Entsprechung für eine Parameter Anzahl vorhanden ist, wird der Parametertyp ausgewertet und die beste Entsprechung festgelegt. Wenn nach dieser Evaluierungsphase immer noch Mehrdeutigkeit vorliegt, ist das XAML-Prozessor Verhalten nicht definiert.  
  
 Die `x:FactoryMethod` Element Verwendung ist im typischen Sinn nicht die Verwendung von Eigenschafts Elementen, da das direktivenmarkup nicht auf den Typ des enthaltenden Objekt Elements verweist. Es wird erwartet, dass die Element Verwendung weniger häufig ist als die Attribut Verwendung. `x:Arguments` (entweder Attribut-oder Element Verwendung) kann zusammen mit `x:FactoryMethod` der Verwendung von Elementen verwendet werden, dies wird jedoch nicht speziell in den Verwendungs Abschnitten veranschaulicht.  
  
 `x:FactoryMethod` Da ein Element vor allen anderen Eigenschaften Elementen stehen muss, muss vor allen Elementen `x:Arguments` stehen, die ebenfalls als-Elemente bereitgestellt werden, und vor jedem Text-/InnerText-/Initialisierungstext stehen muss.  
  
## <a name="see-also"></a>Siehe auch

- [x:Arguments-Anweisung](xarguments-directive.md)
