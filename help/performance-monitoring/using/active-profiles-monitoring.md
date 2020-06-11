---
title: Controle van actieve profielen
description: Leer hoe u real-time informatie krijgt over het nieuwste en historische gebruik en de evolutie van Active Profiles voor elk van uw campagneinstanties.
translation-type: tm+mt
source-git-commit: 024eb750021ff2446b34d648b5abfb016eabc289
workflow-type: tm+mt
source-wordcount: '389'
ht-degree: 1%

---


# Controle van actieve profielen {#active-profiles-monitoring}

>[!IMPORTANT]
>
>De controle van actieve profielen van het Controlebord is beschikbaar in bèta, en voor regelmatige updates en aanpassingen zonder bericht.
>
>De functie is beschikbaar voor klanten die op AWS worden gehost vanuit de Campagne Standard 10368 build and Campaign Classic 8931 build. Als u een vorige build gebruikt, moet u een upgrade uitvoeren om deze functie te gebruiken.

## Actieve profielen {#about-active-profiles}

Volgens uw contract wordt elk van uw campagneexemplaren voorzien van een specifieke hoeveelheid actieve profielen die voor factureringsdoeleinden worden geteld. Raadpleeg het meest recente contract voor informatie over het aantal aangeschafte actieve profielen.

&quot;profiel&quot;: een register van informatie (bv.: een record in de nmsRecipient-tabel of een externe tabel met een cookie-id, de klant-id, de mobiele id of andere informatie die relevant is voor een bepaald kanaal) die een eindklant, perspectief of lead vertegenwoordigt.

Profielen worden als actief beschouwd als ze de afgelopen twaalf maanden via een kanaal zijn aangewezen of gebruikt.

>[!NOTE]
>
>Er wordt geen rekening gehouden met de kanalen Facebook en Twitter.

Raadpleeg [Campagnestandaard](https://docs.adobe.com/content/help/en/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) - en [Campagne Classic](https://docs.adobe.com/content/help/en/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) -documenten voor meer informatie over actieve profielen.

## Actieve profielen controleren {#monitoring-active-profiles}

Met het Configuratiescherm kunt u het gebruik van actieve profielen voor elk van uw campagneinstanties controleren.

Ga als volgt te werk om dit te doen:

1. Open de **[!UICONTROL Performance Monitoring]**-kaart en selecteer vervolgens het tabblad **[!UICONTROL Active Profiles]**.

1. Selecteer de gewenste instantie in het **[!UICONTROL Instance List]** menu.

1. Het aantal actieve profielen dat door de instantie wordt gebruikt, en de laatste keer dat de factureringsworkflow op uw instantie werd uitgevoerd.

![](assets/active-profiles-graph.png)

>[!NOTE]
>
>Actieve profielen worden geteld op basis van toegewijde technische workflows die dagelijks op uw instanties worden uitgevoerd:
>
>* De [&quot;factureringsworkflow&quot;](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html) voor de standaard van de campagne,
>* De workflow [&quot;Aantal actieve factureringsprofielen&quot;](https://docs.adobe.com/content/help/en/campaign-classic/using/automating-with-workflows/technical-workflows/deliveries.html) voor Campagne Classic.


Het onderste gebied biedt een grafische weergave van het gebruik van actieve profielen in de afgelopen 30 dagen. Met de beschikbare filters in de rechterbovenhoek kunt u de weergegeven periode wijzigen in 1 jaar.

Als u de cursor boven een van de grafiekbalken houdt, kunt u het exacte aantal actieve profielen ophalen dat wordt gebruikt voor de geselecteerde periode.
