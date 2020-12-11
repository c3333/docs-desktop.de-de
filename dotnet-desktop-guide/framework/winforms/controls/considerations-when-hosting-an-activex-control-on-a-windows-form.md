---
title: Aspekte beim Hosten eines ActiveX-Steuerelements in Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms controls, ActiveX controls
- ActiveX controls [Windows Forms], hosting
- Windows Forms, ActiveX controls
- Windows Forms, hosting ActiveX controls
- ActiveX controls [Windows Forms], adding
ms.assetid: 2509302d-a74e-484f-9890-2acdbfa67a68
ms.openlocfilehash: d4d990bf904fbd8f89fa2a6f70117212a44d3932
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96972235"
---
# <a name="considerations-when-hosting-an-activex-control-on-a-windows-form"></a>Aspekte beim Hosten eines ActiveX-Steuerelements in Windows Forms

Obwohl Windows Forms zum Hosten von Windows Forms-Steuerelementen optimiert wurde, können Sie weiterhin ActiveX-Steuerelemente verwenden. Bei Verwendung von ActiveX-Steuerelementen in einer Anwendung sollten Sie Folgendes berücksichtigen:  
  
- **Sicherheit** Die Common Language Runtime wurde im Hinblick auf die Codezugriffssicherheit verbessert. Anwendungen mit Windows Forms können in einer voll vertrauenswürdigen Umgebung uneingeschränkt und in einer halb vertrauenswürdigen Umgebung mit Zugriff auf die meisten verfügbaren Funktionen ausgeführt werden. Windows Forms-Steuerelemente können problemlos in einem Browser integriert werden. Diese verbesserten Sicherheitsmerkmale können jedoch nicht genutzt werden, wenn ActiveX-Steuerelemente für Windows Forms verwendet werden. Das Ausführen eines ActiveX-Steuer Elements erfordert die nicht verwaltete Code-Berechtigung, die mit der-Eigenschaft festgelegt wird <xref:System.Security.Permissions.SecurityPermissionAttribute.UnmanagedCode%2A?displayProperty=nameWithType> . Weitere Informationen zur Sicherheit und zur Berechtigung für nicht verwalteten Code finden Sie unter <xref:System.Security.Permissions.SecurityPermissionAttribute> .  
  
- **Gesamtkosten** ActiveX-Steuerelemente, die einem Windows Form hinzugefügt werden, werden komplett mit diesem Windows Form weitergegeben. Dadurch können die erstellten Dateien unter Umständen sehr groß werden. Außerdem muss bei Verwendung von ActiveX-Steuerelementen für Windows Forms die Registrierung geändert werden. Damit wird stärker in den Computer des Benutzers eingegriffen als mit Windows Forms-Steuerelementen, bei denen dies nicht erforderlich ist.  
  
    > [!NOTE]
    > Zum Arbeiten mit ActiveX-Steuerelementen ist ein COM-Interop-Wrapper erforderlich. Weitere Informationen finden Sie unter [COM-Interoperabilität in Visual Basic und Visual C#](/dotnet/visual-basic/programming-guide/com-interop/com-interoperability-in-net-framework-applications).  
    > [!NOTE]
    > Wenn der Name eines Members des ActiveX-Steuer Elements mit einem Namen übereinstimmt, der in der .NET Framework definiert ist, wird das ActiveX-Steuerelement-Import Programm den Elementnamen mit **CTL** versehen, wenn die <xref:System.Windows.Forms.AxHost> abgeleitete Klasse erstellt wird. Wenn das ActiveX-Steuerelement z. b. über einen Member mit dem Namen **Layout** verfügt, wird es in der von AxHost abgeleiteten Klasse in **CtlLayout** umbenannt, da das **layoutereignis** innerhalb der .NET Framework definiert wird.  
  
## <a name="see-also"></a>Siehe auch

- [Gewusst wie: Hinzufügen von ActiveX-Steuerelementen zu Windows Forms](how-to-add-activex-controls-to-windows-forms.md)
- [Codezugriffssicherheit](/dotnet/framework/misc/code-access-security)
- [In zahlreichen Sprachen und Bibliotheken verglichene Steuerelemente und programmierbare Objekte](/previous-versions/visualstudio/visual-studio-2010/0061wezk(v=vs.100))
- [Einfügen von Steuerelementen in Windows Forms](putting-controls-on-windows-forms.md)
- [Windows Forms Steuerelemente](index.md)
