---
title: 'Vorgehensweise: Überprüfen von Anwendungseinstellungen'
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
helpviewer_keywords:
- validating application settings
- application settings [Windows Forms], Windows Forms
- application settings [Windows Forms], validating
ms.assetid: 9f145ada-4267-436a-aa4c-c4dcffd0afb7
ms.openlocfilehash: e2a364aacfbd1b6ac2542c5500380647a09a33ab
ms.sourcegitcommit: 9f6df084c53a3da0ea657ed0d708a72213683084
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/09/2020
ms.locfileid: "96976099"
---
# <a name="how-to-validate-application-settings"></a><span data-ttu-id="5efba-102">Vorgehensweise: Überprüfen von Anwendungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="5efba-102">How to: Validate Application Settings</span></span>

<span data-ttu-id="5efba-103">In diesem Thema wird veranschaulicht, wie Anwendungseinstellungen überprüft werden, bevor sie persistent gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="5efba-103">This topic demonstrates how to validate application settings before they are persisted.</span></span>

<span data-ttu-id="5efba-104">Da die Anwendungseinstellungen stark typisiert sind, müssen Sie darauf vertrauen, dass Benutzer Daten mit einem falschen Typ keiner bestimmten Einstellung zuweisen können.</span><span class="sxs-lookup"><span data-stu-id="5efba-104">Because application settings are strongly typed, you have some confidence that users cannot assign data of an incorrect type to a given setting.</span></span> <span data-ttu-id="5efba-105">Ein Benutzer kann weiterhin versuchen, einer Einstellung einen Wert zuzuweisen, der außerhalb der zulässigen Grenzen liegt, z.B. die Angabe eines in der Zukunft liegenden Geburtsdatums.</span><span class="sxs-lookup"><span data-stu-id="5efba-105">However, a user still may attempt to assign a value to a setting that falls outside of acceptable bounds—for example, supplying a birth date that occurs in the future.</span></span> <span data-ttu-id="5efba-106"><xref:System.Configuration.ApplicationSettingsBase>, die übergeordnete Klasse aller Anwendungs Einstellungs Klassen, macht vier Ereignisse verfügbar, um die Überprüfung dieser Begrenzungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5efba-106"><xref:System.Configuration.ApplicationSettingsBase>, the parent class of all application settings classes, exposes four events to enable such bounds checking.</span></span> <span data-ttu-id="5efba-107">Durch die Bearbeitung dieser Ereignisse befinden sich alle Überprüfungscodes an einem einzigen Speicherort und sind nicht im gesamten Projekt verteilt.</span><span class="sxs-lookup"><span data-stu-id="5efba-107">Handling these events puts all of your validation code in a single location, rather than scattering it throughout your project.</span></span>

<span data-ttu-id="5efba-108">Welches Ereignis Sie verwenden, hängt davon ob, wann Sie Ihre Einstellungen überprüfen müssen, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5efba-108">The event you use depends upon when you need to validate your settings, as described in the following table.</span></span>

|<span data-ttu-id="5efba-109">Ereignis</span><span class="sxs-lookup"><span data-stu-id="5efba-109">Event</span></span>|<span data-ttu-id="5efba-110">Vorkommen und Verwendung</span><span class="sxs-lookup"><span data-stu-id="5efba-110">Occurrence and use</span></span>|
|-----------|------------------------|
|<xref:System.Configuration.ApplicationSettingsBase.SettingsLoaded>|<span data-ttu-id="5efba-111">Tritt nach dem ersten Laden der Eigenschaftengruppe einer Einstellung auf.</span><span class="sxs-lookup"><span data-stu-id="5efba-111">Occurs after the initial loading of a settings property group.</span></span><br /><br /> <span data-ttu-id="5efba-112">Verwenden Sie dieses Ereignis, um die Anfangswerte der gesamten Eigenschaftengruppe zu überprüfen, bevor sie in der Anwendung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5efba-112">Use this event to validate initial values for the entire property group before they are used within the application.</span></span>|
|<xref:System.Configuration.ApplicationSettingsBase.SettingChanging>|<span data-ttu-id="5efba-113">Tritt auf, bevor der Wert einer einzelnen Einstellungseigenschaft geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5efba-113">Occurs before the value of a single settings property is changed.</span></span><br /><br /> <span data-ttu-id="5efba-114">Verwenden Sie dieses Ereignis, um eine einzelne Eigenschaft zu überprüfen, bevor sie geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5efba-114">Use this event to validate a single property before it is changed.</span></span> <span data-ttu-id="5efba-115">Sie kann Benutzern unmittelbares Feedback hinsichtlich ihrer Aktionen und Auswahl geben.</span><span class="sxs-lookup"><span data-stu-id="5efba-115">It can provide immediate feedback to users regarding their actions and choices.</span></span>|
|<xref:System.Configuration.ApplicationSettingsBase.PropertyChanged>|<span data-ttu-id="5efba-116">Tritt auf, nachdem der Wert einer einzelnen Einstellungseigenschaft geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5efba-116">Occurs after the value of a single settings property is changed.</span></span><br /><br /> <span data-ttu-id="5efba-117">Verwenden Sie dieses Ereignis, um eine einzelne Eigenschaft zu überprüfen, nachdem sie geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5efba-117">Use this event to validate a single property after it is changed.</span></span> <span data-ttu-id="5efba-118">Dieses Ereignis wird selten zur Überprüfung verwendet, es sei denn, es ist ein langer, asynchroner Überprüfungsprozess erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5efba-118">This event is rarely used for validation unless a lengthy, asynchronous validation process is required.</span></span>|
|<xref:System.Configuration.ApplicationSettingsBase.SettingsSaving>|<span data-ttu-id="5efba-119">Tritt auf, bevor die Eingenschaftengruppe der Einstellung gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="5efba-119">Occurs before the settings property group is stored.</span></span><br /><br /> <span data-ttu-id="5efba-120">Verwenden Sie dieses Ereignis, um Werte der gesamten Eigenschaftengruppe zu überprüfen, bevor sie persistent auf dem Datenträger gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="5efba-120">Use this event to validate values for the entire property group before they are persisted to disk.</span></span>|

<span data-ttu-id="5efba-121">Normalerweise verwenden Sie zu Überprüfungszwecken nicht alle diese Ereignisse innerhalb der gleichen Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5efba-121">Typically, you will not use all of these events within the same application for validation purposes.</span></span> <span data-ttu-id="5efba-122">Beispielsweise ist es oft möglich, alle Überprüfungsanforderungen zu erfüllen, indem nur das-Ereignis verarbeitet wird <xref:System.Configuration.ApplicationSettingsBase.SettingChanging> .</span><span class="sxs-lookup"><span data-stu-id="5efba-122">For example, it is often possible to fulfill all validation requirements by handling only the <xref:System.Configuration.ApplicationSettingsBase.SettingChanging> event.</span></span>

<span data-ttu-id="5efba-123">Ein Ereignishandler führt in der Regel eine der folgenden Aktionen aus, wenn ein ungültiger Wert erkannt wurde:</span><span class="sxs-lookup"><span data-stu-id="5efba-123">An event handler generally performs one of the following actions when it detects an invalid value:</span></span>

- <span data-ttu-id="5efba-124">Er gibt automatisch einen Wert an, der bekanntermaßen richtig ist, z.B. der Standardwert.</span><span class="sxs-lookup"><span data-stu-id="5efba-124">Automatically supplies a value known to be correct, such as the default value.</span></span>

- <span data-ttu-id="5efba-125">Er fragt den Benutzer des Servercodes erneut nach Informationen.</span><span class="sxs-lookup"><span data-stu-id="5efba-125">Re-queries the user of server code for information.</span></span>

- <span data-ttu-id="5efba-126">Für Ereignisse, die vor den zugehörigen Aktionen ausgelöst werden, z. b. <xref:System.Configuration.ApplicationSettingsBase.SettingChanging> und <xref:System.Configuration.ApplicationSettingsBase.SettingsSaving> , verwendet das- <xref:System.ComponentModel.CancelEventArgs> Argument, um den Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="5efba-126">For events raised before their associated actions, such as <xref:System.Configuration.ApplicationSettingsBase.SettingChanging> and <xref:System.Configuration.ApplicationSettingsBase.SettingsSaving>, uses the <xref:System.ComponentModel.CancelEventArgs> argument to cancel the operation.</span></span>

<span data-ttu-id="5efba-127">Weitere Informationen zur Behandlung von Ereignissen finden Sie unter [Übersicht über Ereignishandler](../event-handlers-overview-windows-forms.md).</span><span class="sxs-lookup"><span data-stu-id="5efba-127">For more information about event handling, see [Event Handlers Overview](../event-handlers-overview-windows-forms.md).</span></span>

<span data-ttu-id="5efba-128">Die folgenden Prozeduren zeigen, wie Sie mit dem-Ereignis oder dem-Ereignis auf ein gültiges Geburtsdatum testen <xref:System.Configuration.ApplicationSettingsBase.SettingChanging> <xref:System.Configuration.ApplicationSettingsBase.SettingsSaving> .</span><span class="sxs-lookup"><span data-stu-id="5efba-128">The following procedures show how to test for a valid birth date using either the <xref:System.Configuration.ApplicationSettingsBase.SettingChanging> or the <xref:System.Configuration.ApplicationSettingsBase.SettingsSaving> event.</span></span> <span data-ttu-id="5efba-129">Die Verfahren wurden unter der Annahme geschrieben, dass Sie Ihre Anwendungseinstellungen bereits erstellt haben. In diesem Beispiel wird für die Einstellung mit dem Namen `DateOfBirth` eine Überprüfung der Begrenzungen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="5efba-129">The procedures were written under the assumption that you have already created your application settings; in this example, we will perform bounds checking on a setting named `DateOfBirth`.</span></span> <span data-ttu-id="5efba-130">Weitere Informationen zum Erstellen von Einstellungen finden Sie unter [Vorgehensweise: Erstellen von Anwendungseinstellungen](how-to-create-application-settings.md).</span><span class="sxs-lookup"><span data-stu-id="5efba-130">For more information about creating settings, see [How to: Create Application Settings](how-to-create-application-settings.md).</span></span>

### <a name="to-obtain-the-application-settings-object"></a><span data-ttu-id="5efba-131">So rufen Sie das Anwendungseinstellungsobjekt ab</span><span class="sxs-lookup"><span data-stu-id="5efba-131">To obtain the application settings object</span></span>

- <span data-ttu-id="5efba-132">Rufen Sie einen Verweis auf das Anwendungseinstellungsobjekt (die Wrapperinstanz) ab, indem Sie eines der folgenden gegliederten Elemente abschließen:</span><span class="sxs-lookup"><span data-stu-id="5efba-132">Obtain a reference to the application settings object (the wrapper instance) by completing one of the following bulleted items:</span></span>

  - <span data-ttu-id="5efba-133">Wenn Sie die Einstellungen über das Dialogfeld „Anwendungseinstellungen von Visual Studio“ im **-Eigenschaften-Editor** erstellt haben, können Sie das Standardeinstellungsobjekt abrufen, das über den folgenden Ausdruck für Ihre Sprache generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5efba-133">If you created your settings using the Visual Studio Application Settings dialog box in the **Property Editor**, you can retrieve the default settings object generated for your language through the following expression.</span></span>

    ```csharp
    Properties.Settings.Default
    ```

    ```vb
    MySettings.Default
    ```

    <span data-ttu-id="5efba-134">Oder</span><span class="sxs-lookup"><span data-stu-id="5efba-134">-or-</span></span>

  - <span data-ttu-id="5efba-135">Wenn Sie Entwickler von Visual Basic sind und Sie Ihre Anwendungseinstellungen mit dem Projekt-Designer erstellt haben, können Sie Ihre Einstellungen über das [My.Settings-Objekt](/dotnet/visual-basic/language-reference/objects/my-settings-object) abrufen.</span><span class="sxs-lookup"><span data-stu-id="5efba-135">If you are a Visual Basic developer and you created your application settings using the Project Designer, you can retrieve your settings by using the [My.Settings Object](/dotnet/visual-basic/language-reference/objects/my-settings-object).</span></span>

    <span data-ttu-id="5efba-136">Oder</span><span class="sxs-lookup"><span data-stu-id="5efba-136">-or-</span></span>

  - <span data-ttu-id="5efba-137">Wenn Sie die Einstellungen durch direktes ableiten von erstellt <xref:System.Configuration.ApplicationSettingsBase> haben, müssen Sie die Klasse manuell instanziieren.</span><span class="sxs-lookup"><span data-stu-id="5efba-137">If you created your settings by deriving from <xref:System.Configuration.ApplicationSettingsBase> directly, you need to instantiate your class manually.</span></span>

    ```csharp
    MyCustomSettings settings = new MyCustomSettings();
    ```

    ```vb
    Dim Settings as New MyCustomSettings()
    ```

<span data-ttu-id="5efba-138">Die folgenden Prozeduren wurden unter der Annahme geschrieben, dass das Anwendungseinstellungsobjekt abgerufen wurde, indem das letzte gegliederte Element in dieser Prozedur abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="5efba-138">The following procedures were written under the assumption that the application settings object was obtained by completing the last bulleted item in this procedure.</span></span>

### <a name="to-validate-application-settings-when-a-setting-is-changing"></a><span data-ttu-id="5efba-139">So überprüfen Sie Anwendungseinstellungen, wenn eine Einstellung geändert wird</span><span class="sxs-lookup"><span data-stu-id="5efba-139">To validate Application Settings when a setting is changing</span></span>

1. <span data-ttu-id="5efba-140">Wenn Sie ein c#-Entwickler sind, fügen Sie im-Ereignis des Formulars oder Steuer Elements `Load` einen Ereignishandler für das- <xref:System.Configuration.ApplicationSettingsBase.SettingChanging> Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="5efba-140">If you are a C# developer, in your form or control's `Load` event, add an event handler for the <xref:System.Configuration.ApplicationSettingsBase.SettingChanging> event.</span></span>

    <span data-ttu-id="5efba-141">Oder</span><span class="sxs-lookup"><span data-stu-id="5efba-141">-or-</span></span>

    <span data-ttu-id="5efba-142">Wenn Sie Visual Basic-Entwickler sind, sollten Sie die `Settings`-Variablen mithilfe des `WithEvents`-Schlüsselworts deklarieren.</span><span class="sxs-lookup"><span data-stu-id="5efba-142">If you are a Visual Basic developer, you should declare the `Settings` variable using the `WithEvents` keyword.</span></span>

    ```csharp
    public void Form1_Load(Object sender, EventArgs e)
    {
        settings.SettingChanging += new SettingChangingEventHandler(MyCustomSettings_SettingChanging);
    }
    ```

    ```vb
    Public Sub Form1_Load(sender as Object, e as EventArgs)
        AddHandler settings.SettingChanging, AddressOf MyCustomSettings_SettingChanging
    End Sub
    ```

2. <span data-ttu-id="5efba-143">Definieren Sie den Ereignishandler, und schreiben Sie den Code in den Ereignishandler, um eine Überprüfung der Begrenzungen für das Geburtsdatum durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="5efba-143">Define the event handler, and write the code inside of it to perform bounds checking on the birth date.</span></span>

    ```csharp
    private void MyCustomSettings_SettingChanging(Object sender, SettingChangingEventArgs e)
    {
        if (e.SettingName.Equals("DateOfBirth"))
        {
            var newDate = (DateTime)e.NewValue;
            if (newDate > DateTime.Now)
            {
                e.Cancel = true;
                // Inform the user.
            }
        }
    }
    ```

    ```vb
    Private Sub MyCustomSettings_SettingChanging(sender as Object, e as SettingChangingEventArgs) Handles Settings.SettingChanging
        If (e.SettingName.Equals("DateOfBirth")) Then
            Dim NewDate as Date = CType(e.NewValue, Date)
            If (NewDate > Date.Now) Then
                e.Cancel = True
                ' Inform the user.
            End If
        End If
    End Sub
    ```

### <a name="to-validate-application-settings-when-a-save-occurs"></a><span data-ttu-id="5efba-144">So überprüfen Sie Anwendungseinstellungen, sobald ein Speichervorgang auftritt</span><span class="sxs-lookup"><span data-stu-id="5efba-144">To validate Application Settings when a Save occurs</span></span>

1. <span data-ttu-id="5efba-145">Fügen Sie im-Ereignis des Formulars oder Steuer Elements `Load` einen Ereignishandler für das- <xref:System.Configuration.ApplicationSettingsBase.SettingsSaving> Ereignis hinzu.</span><span class="sxs-lookup"><span data-stu-id="5efba-145">In your form or control's `Load` event, add an event handler for the <xref:System.Configuration.ApplicationSettingsBase.SettingsSaving> event.</span></span>

    ```csharp
    public void Form1_Load(Object sender, EventArgs e)
    {
        settings.SettingsSaving += new SettingsSavingEventHandler(MyCustomSettings_SettingsSaving);
    }
    ```

    ```vb
    Public Sub Form1_Load(Sender as Object, e as EventArgs)
        AddHandler settings.SettingsSaving, AddressOf MyCustomSettings_SettingsSaving
    End Sub
    ```

2. <span data-ttu-id="5efba-146">Definieren Sie den Ereignishandler, und schreiben Sie den Code in den Ereignishandler, um eine Überprüfung der Begrenzungen für das Geburtsdatum durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="5efba-146">Define the event handler, and write the code inside of it to perform bounds checking on the birth date.</span></span>

    ```csharp
    private void MyCustomSettings_SettingsSaving(Object sender, SettingsSavingEventArgs e)
    {
        if (this["DateOfBirth"] > Date.Now) {
            e.Cancel = true;
        }
    }
    ```

    ```vb
    Private Sub MyCustomSettings_SettingsSaving(Sender as Object, e as SettingsSavingEventArgs)
        If (Me["DateOfBirth"] > Date.Now) Then
            e.Cancel = True
        End If
    End Sub
    ```

## <a name="see-also"></a><span data-ttu-id="5efba-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5efba-147">See also</span></span>

- [<span data-ttu-id="5efba-148">Erstellen von Ereignishandlern in Windows Forms</span><span class="sxs-lookup"><span data-stu-id="5efba-148">Creating Event Handlers in Windows Forms</span></span>](../creating-event-handlers-in-windows-forms.md)
- [<span data-ttu-id="5efba-149">Vorgehensweise: Erstellen von Anwendungseinstellungen</span><span class="sxs-lookup"><span data-stu-id="5efba-149">How to: Create Application Settings</span></span>](how-to-create-application-settings.md)
