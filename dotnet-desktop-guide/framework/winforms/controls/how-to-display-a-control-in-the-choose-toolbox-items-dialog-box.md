---
title: 'Gewusst wie: Anzeigen eines Steuerelements im Dialogfeld "Toolboxelemente auswählen"'
ms.date: 08/23/2019
helpviewer_keywords:
- global assembly cache [Windows Forms], Choose Toolbox Items dialog box
- AssemblyFoldersEx [Windows Forms], Choose Toolbox Items dialog box
- controls [Windows Forms], display in Choose Toolbox Items dialog box
- assembly folder registration [Windows Forms], Choose Toolbox Items dialog box
- Choose Toolbox Items dialog box [Windows Forms], display control
ms.assetid: 01ef6eba-d044-40f0-951d-78eff7ebd9a9
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: b105c45e0d55417066c7f8658f0cb23a12c7f768
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975661"
---
# <a name="how-to-display-a-control-in-the-choose-toolbox-items-dialog-box"></a>Gewusst wie: Anzeigen eines Steuerelements im Dialogfeld "Toolboxelemente auswählen"

Wenn Sie Steuerelemente entwickeln und verteilen, möchten Sie möglicherweise, dass diese Steuerelemente im Dialogfeld **Toolbox Elemente auswählen** von Visual Studio angezeigt werden, das angezeigt wird, wenn Sie mit der rechten Maustaste auf die **Toolbox** klicken und **Elemente auswählen** auswählen. Sie können das Steuerelement in diesem Dialogfeld mithilfe der AssemblyFoldersEx-Registrierungs Prozedur anzeigen lassen.

So zeigen Sie das Steuerelement im Dialogfeld Toolbox Elemente auswählen an:

- Installieren Sie die steuerungsassembly im globalen Assemblycache. Weitere Informationen finden Sie unter Gewusst [wie: Installieren einer Assembly in den globalen Assemblycache](/dotnet/framework/app-domains/install-assembly-into-gac).

  Oder

- Registrieren Sie das Steuerelement und die zugehörigen Entwurfszeit-Assemblys mithilfe der AssemblyFoldersEx-Registrierungs Prozedur. AssemblyFoldersEx ist ein Registrierungs Speicherort, an dem Drittanbieter Pfade für jede Version des Frameworks speichern, das Sie unterstützen. Die Entwurfszeit Auflösung kann in diesem Registrierungs Speicherort nach Verweisassemblys suchen. Das Registrierungs Skript kann die Steuerelemente angeben, die in der Toolbox angezeigt werden sollen.

## <a name="see-also"></a>Siehe auch

- [Entwickeln von Windows Forms-Steuerelementen zur Entwurfszeit](developing-windows-forms-controls-at-design-time.md)
- [How to: Installieren einer Assembly im globalen Assemblycache](/dotnet/framework/app-domains/install-assembly-into-gac)
- [Exemplarische Vorgehensweise: Automatisches Füllen der Toolbox mit benutzerdefinierten Komponenten](walkthrough-automatically-populating-the-toolbox-with-custom-components.md)
