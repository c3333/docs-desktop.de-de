---
title: Verwenden von WPF-Steuerelementen
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms Designer [Windows Forms], interoperability with WPF
- interoperability [WPF]
ms.assetid: 03c85dce-26ad-44cd-bc1d-8e0cb56de096
author: jillre
ms.author: jillfra
manager: jillfra
ms.openlocfilehash: dfc086b4873c41bf1919b680d472807283e8a340
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96975203"
---
# <a name="use-wpf-controls-in-windows-forms-apps"></a>Verwenden von WPF-Steuerelementen in Windows Forms-apps

Sie können Windows Presentation Foundation (WPF)-Steuerelemente in Windows Forms-basierten Anwendungen verwenden. Obwohl es sich um zwei verschiedene Ansichts Technologien handelt, funktionieren Sie problemlos.

Der Windows Forms-Designer in Visual Studio stellt eine visuelle Entwurfs Umgebung zum Hosting von Windows Presentation Foundation Steuerelementen bereit. Ein WPF-Steuerelement wird von einem speziellen Windows Forms Steuerelement mit dem Namen gehostet <xref:System.Windows.Forms.Integration.ElementHost> . Mit diesem Steuerelement kann das WPF-Steuerelement am Layout des Formulars teilnehmen und Tastatur-und Maus Meldungen empfangen. Zur Entwurfszeit können Sie das Steuerelement <xref:System.Windows.Forms.Integration.ElementHost> genauso anordnen wie alle Windows Forms Steuerelemente.

Sie können auch Windows Forms-Steuerelemente in WPF-basierten Anwendungen verwenden. Weitere Informationen finden Sie unter [Entwerfen von XAML in Visual Studio](/visualstudio/xaml-tools/designing-xaml-in-visual-studio).

## <a name="see-also"></a>Siehe auch

- [WPF-und Windows Forms Interoperation](/dotnet/framework/wpf/advanced/wpf-and-windows-forms-interoperation)
