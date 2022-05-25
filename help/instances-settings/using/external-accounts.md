---
product: campaign
solution: Campaign
title: MID/RT-instanties toevoegen (hybride model)
description: Leer hoe u MID/RT-instanties toevoegt aan het Configuratiescherm met een hybride hostingmodel.
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 2458263ef5981a16d983912b498e320501df7889
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 2%

---


# MID/RT-instanties toevoegen (hybride model)

>[!CONTEXTUALHELP]
>id="cp_externalaccounts"
>title="Externe rekeningen"
>abstract="In dit scherm kunnen klanten met een hybride hostingmodel hun MID/RT-instantie-URL opgeven die in de marketinginstantie in het Configuratiescherm is geconfigureerd, om de mogelijkheden van het Configuratiescherm te benutten."

Met het Configuratiescherm kunnen klanten met een hybride hostingmodel specifieke mogelijkheden van het Configuratiescherm benutten. Hiervoor moeten ze de URL van de instantie MID/RT opgeven die in hun marketinginstantie in het Configuratiescherm is geconfigureerd.

Raadpleeg voor meer informatie over hostmodellen [Campaign Classic-documentatie](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html).

## Een MID/RT-instantie toevoegen {#add}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="URL"
>abstract="URL van de instantie, die in de Console van de Cliënt van de Campagne in het Beheer > Platform > het Externe menu van Rekeningen kan worden gevonden."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="Operator"
>abstract="Id van de operator die is opgegeven na eerste levering door Adobe Admin."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="Wachtwoord"
>abstract="Wachtwoord van de operator opgegeven na eerste levering door Adobe Admin."

Hybride klanten moeten via Experience Cloud verbinding maken met het Configuratiescherm. Bij de eerste keer dat u het Configuratiescherm opent, worden slechts twee kaarten weergegeven op de startpagina.

![](assets/hybrid-homepage.png)

>[!NOTE]
>
>Als u problemen ondervindt om toegang te krijgen tot het Configuratiescherm, is het zeer waarschijnlijk dat uw marketingexemplaar nog niet is toegewezen aan uw organisatie-id. Neem contact op met de klantenservice om deze installatie te voltooien en verder te gaan. Als de verbinding is gelukt, wordt de startpagina van het Configuratiescherm weergegeven.

Als u toegang wilt tot de mogelijkheden van het Configuratiescherm, moet u de MID/RT-instantiegegevens opgeven in het dialoogvenster **[!UICONTROL Instances Settings]** kaart. Volg de onderstaande stappen om dit te doen.

1. In de **[!UICONTROL Instances Settings]** kaart, selecteert u de **[!UICONTROL External Accounts]** tab.

1. Selecteer de gewenste marketinginstantie in de vervolgkeuzelijst en klik op **[!UICONTROL Add new URL]**.

   ![](assets/external-account-addbutton.png)

1. Geef informatie over de instantie MID/RT die u wilt toevoegen.

   ![](assets/external-account-add.png)

   * **[!UICONTROL URL]**: URL van het exemplaar, dat in de Console van de Cliënt van de Campagne in **[!UICONTROL Administration]** > **[!UICONTROL Platform]** > **[!UICONTROL External Accounts]** -menu.

      ![](assets/external-account-url.png)

   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**: Credentials van de exploitant verstrekt na eerste levering door Adobe Admin.

      >[!NOTE]
      >
      >Als deze gegevens niet beschikbaar zijn, neemt u contact op met de klantenservice.

1. Klikken **[!UICONTROL Save]** ter bevestiging.

Bij het toevoegen van MID/RT URL wordt een asynchroon proces geactiveerd om de juistheid van URLs te bevestigen. Dit proces kan een paar minuten duren. Totdat de URL van de instantie MID/RT is gevalideerd, wordt de taak in behandeling. Alleen als de validatie is voltooid, hebt u toegang tot de belangrijkste functies van het Configuratiescherm.

![](assets/external-account-pending.png)

U kunt een MID/RT-instantie-URL op elk gewenst moment verwijderen of deactiveren door deze in de lijst te selecteren.

![](assets/external-account-edit.png)

Let op: u kunt elke actie controleren die wordt uitgevoerd in het dialoogvenster **[!UICONTROL External Accounts]** tabblad op een URL van een MID/RT-instantie vanuit de **[!UICONTROL Job Logs]**:

![](assets/external-account-logs.png)

## Mogelijkheden beschikbaar voor hybride klanten {#capabilities}

Zodra een instantie MID/RT aan het Controlebord wordt toegevoegd, kunt u hefboomwerking de hieronder vermelde mogelijkheden:

* [Belangrijke contacten en gebeurtenissen bewaken](../../service-events/service-events.md)
* [Instantiedetails weergeven](../../instances-settings/using/instance-details.md),
* [IP-adressen toevoegen aan de lijst van gewenste personen](../../instances-settings/using/ip-allow-listing-instance-access.md) (voor RT-instanties),
* [Informatie weergeven over gedelegeerde subdomeinen](../../subdomains-certificates/using/monitoring-subdomains.md),
* [Informatie over SSL-certificaten weergeven](../../subdomains-certificates/using/monitoring-ssl-certificates.md).