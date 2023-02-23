---
product: campaign
solution: Campaign
title: Belangrijke contactpersonen en gebeurtenissen identificeren
description: Leer hoe u gebeurtenissen identificeert die plaatsvinden op uw instanties en belangrijke contacten bij Adobe.
feature: Control Panel
role: Architect
level: Intermediate
exl-id: d230aae6-4f0e-4201-bb3c-0e3f83a7c1b8
source-git-commit: 5e2a5975a4a2ced4b23a18900309fc537daf13c0
workflow-type: tm+mt
source-wordcount: '749'
ht-degree: 43%

---

# Belangrijke contactpersonen en gebeurtenissen identificeren {#keycontacts-events}

>[!CONTEXTUALHELP]
>id="cp_servicecalendar_serviceevents"
>title="Servicekalender"
>abstract="De sectie Belangrijke contacten vermeldt de personen bij Adobe met wie u contact kunt opnemen voor elke aanvraag of probleem met uw instanties. In de sectie van de Kalender van de Gebeurtenis van de Dienst, kunt u vroegere/aanstaande versies en alarm voor de geselecteerde instantie identificeren, evenals opstellings herinneringen voor een bepaalde gebeurtenis."

>[!IMPORTANT]
>
>De servicekalender is beschikbaar in de bètaversie en onderhevig aan regelmatige updates en wijzigingen zonder voorafgaande kennisgeving.

Om effectief toezicht te houden op uw instanties van de Campagne, is het van cruciaal belang om belangrijke gebeurtenissen bij te houden die mogelijk uw instantie(s) kunnen beïnvloeden. Met het Configuratiescherm kunt u gebeurtenissen zoals nieuwe releases, upgrades, patches, hotfixes enzovoort identificeren. en verstrekt een lijst van zeer belangrijke contacten van de Adobe voor om het even welke verzoeken of kwesties.

Deze informatie is toegankelijk via de **[!UICONTROL Service Calendar]** kaart op de startpagina van het Configuratiescherm.

## Belangrijke contacten {#key-contacts}

De sectie **[!UICONTROL Key contacts]** bevat de personen bij Adobe met wie u contact kunt opnemen voor elke aanvraag of probleem met uw instanties.

>[!NOTE]
>
>Deze sectie toont slechts informatie voor de Beheerde Rekeningen van de Dienst.

![](assets/service-events-contacts.png)

De belangrijke contacten omvatten de volgende rollen:

* **[!UICONTROL TAM]**: Technical Account Manager,
* **[!UICONTROL CSM]**: Customer Success Manager,
* **[!UICONTROL Deliverability]**: contactpunt voor afleverbaarheid;
* **[!UICONTROL Transition Manager]**: Managed Services Transition Manager (alleen Managed Services-account),
* **[!UICONTROL On-boarding Specialist]**: specialist die aan het account is toegewezen om u te helpen bij de on-boarding van Campaign Classic (alleen Managed Services-account).

## Belangrijke gebeurtenissen bijhouden {#events}

De **[!UICONTROL Service Event Calendar]** in deze sectie worden alle eerdere en komende releases weergegeven, evenals waarschuwingen voor gebruikers die zijn geabonneerd op e-mailberichten in het Configuratiescherm. Bovendien kunnen gebruikers met het Configuratiescherm herinneringen instellen en relevante gebeurtenissen markeren zodat de geselecteerde instantie beter is georganiseerd en efficiënt is.

Gebeurtenissen worden weergegeven in een kalender of in een lijst. U kunt schakelen tussen de twee weergaven met de **[!UICONTROL Calendar]** en **[!UICONTROL List]** in de rechterbovenhoek van de sectie.

![](assets/service-events-calendar.png)

<table><tr style="border: 0;">
<td><img src="assets/do-not-localize/nav-buttons.png">
</td><td>In de kalenderweergave zijn navigatieknoppen beschikbaar in de rechterbovenhoek om u te helpen door de gebeurtenissen te bladeren. Gebruik de <b>dubbele pijlen</b> om naar de eerste gebeurtenis te navigeren die aanwezig is na/vóór de geselecteerde maand, en <b>enkele pijlen</b> om van een maand naar een andere te navigeren. Klik op de knop <b>cirkelknop</b> om terug te keren naar het standpunt van vandaag .</td>
</tr></table>

Er worden drie gebeurtenistypen weergegeven:

* **Herinneringen** door gebruikers worden ingesteld om op de hoogte te worden gebracht voordat een gebeurtenis plaatsvindt. Deze worden in het groen weergegeven in de kalenderweergave. [Leer hoe u herinnering instelt](#reminders)
* **Waarschuwingen** worden via e-mail verzonden door het Configuratiescherm om gebruikers op de hoogte te stellen van problemen met betrekking tot hun instanties, zoals overbelasting van opslagruimte of vervaldatum van SSL-certificaten. Deze worden oranje weergegeven in de kalenderweergave. In de gebeurtenisbeschrijving wordt aangegeven of de waarschuwing wordt verzonden naar de aangemelde gebruiker, afhankelijk van zijn abonnement op e-mailwaarschuwingen. [Meer informatie over de mogelijkheden voor e-mailwaarschuwingen in het Configuratiescherm](../performance-monitoring/using/email-alerting.md)

* **Uitstoot** geeft zowel oude als aanstaande implementaties aan in de instantie, die in grijs en blauw in de kalenderweergave worden weergegeven. De gebeurtenisdetails specificeren het type van versie verbonden aan elke plaatsing:

   * **[!UICONTROL General availability]**: recentste beschikbare stabiele build.
   * **[!UICONTROL Limited availability]**: alleen on-demand implementatie.
   * **[!UICONTROL Release candidate]**: engineering gevalideerd. Wachten op controle van productie.
   * **[!UICONTROL Pre release]**: eerdere beschikbaarheid voor specifieke klantbehoeften.
   * **[!UICONTROL No longer available]**: de build bevat geen grote problemen, maar er is een nieuwe beschikbaar met extra foutoplossingen. Een upgrade is vereist.
   * **[!UICONTROL Deprecated]**: ingesloten bekende regressies van de build. De build wordt niet meer ondersteund. Een upgrade is verplicht.

U kunt een markering aan een of meer aanstaande gebeurtenissen toewijzen om ze te volgen. Klik hiertoe op de knop voor de ovaal naast de naam van de gebeurtenis.

![](assets/service-events-flag.png)

## Herinneringen instellen {#reminders}

U kunt in de Servicekalender nu herinneringen instellen, zodat u een e-mail ontvangt voordat een gebeurtenis plaatsvindt.

>[!NOTE]
>
>Als u op de hoogte wilt worden gesteld van aanstaande gebeurtenissen, meldt u zich in het Configuratiescherm aan voor e-mailwaarschuwingen. [Meer informatie](../performance-monitoring/using/email-alerting.md)

Ga als volgt te werk om een waarschuwing voor een gebeurtenis in te stellen:

1. Houd de muisaanwijzer boven de gebeurtenis die u wilt herinneren aan of klik op de ovaalknop in de lijstweergave en selecteer **[!UICONTROL Set Reminder]**.

1. Geef een titel op aan de herinnering en selecteer de datum waarop u op de hoogte wilt worden gesteld voordat de gebeurtenis plaatsvindt.

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
