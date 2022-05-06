---
product: campaign
solution: Campaign
title: Connect MID/RT-instanties
description: Leer hoe u MID/RT-instanties koppelt aan Configuratiescherm.
feature: Control Panel
role: Architect
level: Intermediate
source-git-commit: 1b712300bd7a1ef8dc784fa977f938bacc4c5e5b
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 5%

---


# Connect MID/RT-instanties

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_url"
>title="Subdomeindetails"
>abstract="In dit scherm kunnen klanten met een hybride hostingmodel hun MID/RT-instanties in hun marketingexemplaar aanbieden om specifieke acties uit te voeren in het Configuratiescherm."

Met het Configuratiescherm kunnen klanten met een hybride hostingmodel specifieke acties uitvoeren in het Configuratiescherm door hun MID/RT-instanties in hun marketingexemplaar op te geven. Raadpleeg voor meer informatie over hostmodellen [Campaign Classic-documentatie](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/architecture-and-hosting-models/hosting-models-lp/hosting-models.html).

## Een MID/RT-instantie verbinden {#connect}

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_operator"
>title="Subdomeindetails"
>abstract="Id van de operator die wordt gebruikt in de Client Console om de MID/RT-instantie in de marketinginstantie toe te voegen."

>[!CONTEXTUALHELP]
>id="cp_externalaccounts_password"
>title="Subdomeindetails"
>abstract="Wachtwoord van de operator die in de clientconsole wordt gebruikt om de MID/RT-instantie in de marketinginstantie toe te voegen."

Voer de volgende stappen uit om een MID/RT-instantie op te geven in het Configuratiescherm:

1. In de **[!UICONTROL Instances Settings]** kaart, selecteert u de **[!UICONTROL External Accounts]** tab.

1. Selecteer de marketinginstantie in de vervolgkeuzelijst en klik op **[!UICONTROL Add new URL]**.

   ![](assets/external-account-addbutton.png)

1. Geef informatie over de MID/RT-instantie die moet worden verbonden:
   * **[!UICONTROL URL]**: URL van de instantie;
   * **[!UICONTROL Operator]** / **[!UICONTROL Password]**: Referenties van de operator die in de Client Console wordt gebruikt om de MID/RT-instantie in de marketinginstantie toe te voegen.

   ![](assets/external-account-add.png)

1. Klikken **[!UICONTROL Save]** ter bevestiging.

Uw exemplaar wordt nu verbonden met het Controlebord. U kunt een verbinding op elk gewenst moment verwijderen of deactiveren door deze in de lijst te selecteren.

![](assets/external-account-edit.png)

## Mogelijkheden beschikbaar voor MID/RT-instanties {#capabilities}

Zodra een instantie MID/RT met het Controlebord wordt verbonden, kunt u de hieronder vermelde mogelijkheden gebruiken om het te controleren:

* [Instantiedetails weergeven](../../instances-settings/using/instance-details.md),
* [Voeg IP-adressen aan de lijst van gewenste IP-adressen toe om toegang tot uw instanties te hebben](../../instances-settings/using/ip-allow-listing-instance-access.md),
* [Informatie weergeven over gedelegeerde subdomeinen](../../subdomains-certificates/using/setting-up-new-subdomain.md),
* [Informatie over SSL-certificaten weergeven](../../subdomains-certificates/using/monitoring-ssl-certificates.md).
