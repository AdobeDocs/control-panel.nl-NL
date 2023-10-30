---
product: campaign
solution: Campaign
title: Belangrijke contacten en gebeurtenissen identificeren
description: Leer hoe u gebeurtenissen identificeert die plaatsvinden op uw instanties en belangrijke contacten bij Adobe.
feature: Control Panel, Monitoring
role: Admin
level: Intermediate
exl-id: d230aae6-4f0e-4201-bb3c-0e3f83a7c1b8
source-git-commit: a3485766791387bd9422b4f29daf86296efafb98
workflow-type: ht
source-wordcount: '749'
ht-degree: 100%

---

# Belangrijke contacten en gebeurtenissen identificeren {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="Servicekalender"
>abstract="De sectie Belangrijke contacten vermeldt de personen bij Adobe met wie u contact kunt opnemen voor elke aanvraag of probleem met uw instanties. In de sectie Servicegebeurteniskalender kunt u eerdere/aankomende releases en waarschuwingen voor de geselecteerde instantie identificeren, evenals herinneringen instellen voor een bepaalde gebeurtenis."

>[!IMPORTANT]
>
>De servicekalender is beschikbaar in de bètaversie en onderhevig aan regelmatige updates en wijzigingen zonder voorafgaande kennisgeving.

Voor het effectief bewaken van uw Campaign-instanties is het van cruciaal belang om belangrijke gebeurtenissen bij te houden die van invloed op uw instantie(s) kunnen zijn. Met het Configuratiescherm kunt u gebeurtenissen zoals nieuwe releases, upgrades, patches, hot fixes, enzovoort, identificeren. en biedt een lijst met de belangrijkste contactpersonen van Adobe voor eventuele verzoeken of problemen.

Deze informatie is toegankelijk via de kaart **[!UICONTROL Service Calendar]** op de startpagina van het Configuratiescherm.

## Belangrijke contacten {#key-contacts}

De sectie **[!UICONTROL Key contacts]** bevat de personen bij Adobe met wie u contact kunt opnemen voor elke aanvraag of probleem met uw instanties.

>[!NOTE]
>
>In dit gedeelte wordt alleen informatie weergegeven voor Beheerde serviceaccounts.

![](assets/service-events-contacts.png)

De belangrijke contacten omvatten de volgende rollen:

* **[!UICONTROL TAM]**: Technical Account Manager,
* **[!UICONTROL CSM]**: Customer Success Manager,
* **[!UICONTROL Deliverability]**: contactpunt voor afleverbaarheid;
* **[!UICONTROL Transition Manager]**: Managed Services Transition Manager (alleen Managed Services-account),
* **[!UICONTROL On-boarding Specialist]**: specialist die aan het account is toegewezen om u te helpen bij de on-boarding van Campaign Classic (alleen Managed Services-account).

## Belangrijke gebeurtenissen bijhouden {#events}

Het gedeelte **[!UICONTROL Service Event Calendar]** toont alle eerdere en aankomende releases, evenals waarschuwingen waarvoor gebruikers zich hebben aangemeld in het gedeelte voor e-mailwaarschuwingen van het Configuratiescherm. Bovendien kunnen gebruikers met het Configuratiescherm herinneringen instellen en relevante gebeurtenissen voor de geselecteerde instantie markeren, zodat ze beter georganiseerd en efficiënt zijn.

Gebeurtenissen worden weergegeven in een kalender of een lijst. U kunt schakelen tussen de twee weergaven met de knoppen **[!UICONTROL Calendar]** en **[!UICONTROL List]** in de rechterbovenhoek van de sectie.

![](assets/service-events-calendar.png)

<table><tr style="border: 0;">
<td><img src="assets/do-not-localize/nav-buttons.png">
</td><td>In de kalenderweergave zijn navigatieknoppen beschikbaar in de rechterbovenhoek waarmee u door de gebeurtenissen kunt bladeren. Gebruik de <b>dubbele pijlen</b> om te navigeren naar de eerste gebeurtenis die aanwezig is na/vóór de geselecteerde maand, en de <b>enkele pijlen</b> om van de ene maand naar de andere te navigeren. Klik op de <b>cirkelknop</b> om terug te gaan naar de weergave van vandaag.</td>
</tr></table>

Er worden drie soorten gebeurtenissen weergegeven:

* **Herinneringen** worden door gebruikers ingesteld om op de hoogte te worden gebracht voordat een gebeurtenis plaatsvindt. Deze worden in het groen weergegeven in de kalenderweergave. [Leren hoe u een herinnering instelt](#reminders)
* **Waarschuwingen** worden via e-mail verzonden door het Configuratiescherm om gebruikers op de hoogte te stellen van problemen met hun instanties, zoals overbelasting van opslagruimte of vervaldatum van SSL-certificaten. Deze worden in het oranje weergegeven in de kalenderweergave. In de gebeurtenisbeschrijving wordt aangegeven of de waarschuwing wordt verzonden naar de aangemelde gebruiker, afhankelijk van aanmelding voor e-mailwaarschuwingen. [Meer informatie over de mogelijkheden voor e-mailwaarschuwingen in het Configuratiescherm](../performance-monitoring/using/email-alerting.md)

* **Releases** geven zowel eerdere als toekomstige implementaties aan voor de instantie, in respectievelijk grijs en blauw weergegeven in de kalenderweergave. De gebeurtenisdetails geven het type release aan dat aan elke implementatie is gekoppeld:

   * **[!UICONTROL General availability]**: recentste beschikbare stabiele build.
   * **[!UICONTROL Limited availability]**: alleen on-demand implementatie.
   * **[!UICONTROL Release candidate]**: engineering gevalideerd. Wachten op controle van productie.
   * **[!UICONTROL Pre release]**: eerdere beschikbaarheid voor specifieke klantbehoeften.
   * **[!UICONTROL No longer available]**: de build bevat geen grote problemen, maar er is een nieuwe beschikbaar met extra foutoplossingen. Een upgrade is vereist.
   * **[!UICONTROL Deprecated]**: ingesloten bekende regressies van de build. De build wordt niet meer ondersteund. Een upgrade is verplicht.

U kunt een markering aan een of meer aanstaande gebeurtenissen toewijzen om ze te volgen. Klik hiervoor op de knop met 3 puntjes naast de naam van de gebeurtenis.

![](assets/service-events-flag.png)

## Herinneringen instellen {#reminders}

U kunt in de Servicekalender nu herinneringen instellen, zodat u een e-mail ontvangt voordat een gebeurtenis plaatsvindt.

>[!NOTE]
>
>Als u op de hoogte wilt worden gesteld van aanstaande gebeurtenissen, meldt u zich in het Configuratiescherm aan voor e-mailwaarschuwingen. [Meer informatie](../performance-monitoring/using/email-alerting.md)

Ga als volgt te werk om een waarschuwing voor een gebeurtenis in te stellen:

1. Plaats de muisaanwijzer op de gebeurtenis waaraan u wilt worden herinnerd of klik op de knop met 3 puntjes in de lijstweergave en selecteer **[!UICONTROL Set Reminder]**.

1. Geef de herinnering een titel en selecteer vervolgens de datum waarop u de melding wilt ontvangen voordat de gebeurtenis plaatsvindt.

   ![](assets/service-events-set-reminder.png)

   >[!NOTE]
   >
   >Als u niet bent aangemeld voor Configuratiescherm-waarschuwingen, wordt er een bericht weergegeven en kunt u zich inschrijven om e-mailmeldingen te ontvangen.

1. De herinnering voor de geselecteerde gebeurtenis is nu ingesteld. U kunt de aanwijzer op elk gewenst moment boven de herinnering plaatsen om de titel weer te geven.

   ![](assets/service-events-reminder.png)

   >[!NOTE]
   >
   >U kunt maximaal twee herinneringen instellen voor dezelfde gebeurtenis.

1. Op de datum die in de herinnering is opgegeven, wordt een e-mail verzonden om u te herinneren aan de aanstaande gebeurtenis. De herinnering wordt dan automatisch afgetrokken van het aantal **[!UICONTROL Reminders]** in het Servicekalender-menu.
