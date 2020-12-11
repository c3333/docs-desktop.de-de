---
title: Auswirkungen beim Ändern der Darstellung von Basisformularen
ms.date: 03/30/2017
helpviewer_keywords:
- parent forms [Windows Forms]
- inherited forms [Windows Forms], modifications to base form
- Windows Forms, base form appearance
- base forms
- inheritance [Windows Forms], forms
ms.assetid: 1c3f2b29-a05c-4c6f-aa1a-4e66b94f343a
ms.openlocfilehash: 1eda19f754d0b8d446ac9190b432ff0b6106847b
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975028"
---
# <a name="effects-of-modifying-a-base-forms-appearance"></a><span data-ttu-id="03a2d-102">Auswirkungen der Änderung der Darstellung eines Basis Formulars</span><span class="sxs-lookup"><span data-stu-id="03a2d-102">Effects of modifying a base form's appearance</span></span>

<span data-ttu-id="03a2d-103">Während der Anwendungsentwicklung müssen Sie möglicherweise häufig die Darstellung des Basisformulars ändern, dessen Merkmale an andere Formulare im Projekt (oder in anderen Projekten) vererbt werden.</span><span class="sxs-lookup"><span data-stu-id="03a2d-103">During application development, you may often need to change the appearance of the base form from which other forms in the project (or in other projects) are inheriting.</span></span>

<span data-ttu-id="03a2d-104">Zur Entwurfszeit werden Änderungen an der Darstellung des Basisformulars (z.B. das Festlegen von Eigenschaften oder die Addition und Subtraktion von Steuerelementen) in geerbten Formularen reflektiert, wenn das Projekt mit dem Basisformular erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="03a2d-104">At design time, changes to the base form's appearance (be it the setting of properties or the addition and subtraction of controls) are reflected on inherited forms when the project containing the base form is built.</span></span> <span data-ttu-id="03a2d-105">Es genügt nicht, wenn Sie die am Basisformular vorgenommenen Änderungen einfach speichern.</span><span class="sxs-lookup"><span data-stu-id="03a2d-105">It is not sufficient for you to simply save the changes to the base form.</span></span> <span data-ttu-id="03a2d-106">Wählen Sie aus dem Menü **Erstellen** die Option **Erstellen** aus, um ein Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="03a2d-106">To build a project, choose **Build** from the **Build** menu.</span></span>

<span data-ttu-id="03a2d-107">Änderungen, die zur Laufzeit am Basisformular vorgenommen werden, haben keine Auswirkungen auf geerbte Formulare, die bereits instanziiert werden.</span><span class="sxs-lookup"><span data-stu-id="03a2d-107">Modifications made to the base form at run time have no affect on inherited forms that are already instantiated.</span></span>

## <a name="see-also"></a><span data-ttu-id="03a2d-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03a2d-108">See also</span></span>

- [<span data-ttu-id="03a2d-109">base</span><span class="sxs-lookup"><span data-stu-id="03a2d-109">base</span></span>](/dotnet/csharp/language-reference/keywords/base)
- [<span data-ttu-id="03a2d-110">Vorgehensweise: Erben von Windows Forms</span><span class="sxs-lookup"><span data-stu-id="03a2d-110">How to: Inherit Windows Forms</span></span>](how-to-inherit-windows-forms.md)
- [<span data-ttu-id="03a2d-111">Visuelle Vererbung in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="03a2d-111">Windows Forms Visual Inheritance</span></span>](windows-forms-visual-inheritance.md)
