---
product: campaign
solution: Campaign
title: Bewaking van actieve profielen
description: Leer hoe u realtime-informatie krijgt over het nieuwste en historische gebruik en de evolutie van actieve profielen voor al uw Campaign-instanties.
feature: Control Panel
role: Architect
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: cb18dbcbb3a575d88d3c13fe3f22a657caea1e7e
workflow-type: tm+mt
source-wordcount: '433'
ht-degree: 40%

---

# Actieve profielen controleren {#active-profiles-monitoring}

## Actieve profielen {#about-active-profiles}

>[!IMPORTANT]
>
>Bewaking van actieve profielen vanuit het Configuratiescherm is beschikbaar in de bètaversie en kan regelmatig en zonder kennisgeving worden bijgewerkt en gewijzigd. Het is beschikbaar bij Campaign Standard 10368 bouwstijl.

Volgens uw contract worden al uw Campaign-instanties ingericht met een specifieke hoeveelheid actieve profielen die voor factureringsdoeleinden worden geteld. Raadpleeg uw meest recente contract voor informatie over het aantal aangeschafte actieve profielen.

‘Profiel’ betreft een datarecord (bijv. een record in de nmsRecipient-tabel of een externe tabel met een cookie-id, klant-id, mobiele id of andere informatie die relevant is voor een bepaald kanaal) die een eindklant, prospect of lead vertegenwoordigt.

Profielen worden als actief beschouwd als ze de afgelopen twaalf maanden via een kanaal zijn getarget of gecommuniceerd.

>[!NOTE]
>
>Er wordt geen rekening gehouden met de kanalen Facebook en Twitter.

Raadpleeg voor meer informatie over actieve profielen de categorie [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html) en [Campagne v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html#active-profiles) documenten.

## Het gebruik van actieve profielen controleren {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="Informatie over actieve profielen controleren"
>abstract="Op dit tabblad krijgt u real-time informatie over het meest recente en historische gebruik en de evolutie van actieve profielen voor elk onderdeel van uw campagne en uw organisatie."

Informatie over het gebruik van actieve profielen wordt bijgewerkt in het Configuratiescherm op basis van speciale informatie [!DNL Campaign] technische workflows die dagelijks op uw instanties worden uitgevoerd:
* De workflow [Billing](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=nl) voor Campaign Standard,
* De [&quot;Aantal actieve factureringsprofielen&quot;](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflows/advanced-management/about-technical-workflows.html?lang=nl) workflow voor Campagne v7/v8.


Als u het actieve profielgebruik in het Configuratiescherm wilt controleren, navigeert u naar het **[!UICONTROL Performance Monitoring]** kaart > **[!UICONTROL Active Profiles]** en selecteert u de gewenste instantie in het menu **[!UICONTROL Instance List]**.

Er wordt informatie weergegeven over uw gebruik van actieve profielen.

![](assets/active-profiles-graph.png)

In het bovenste gedeelte wordt de volgende informatie weergegeven:

* Het aantal actieve profielen dat momenteel wordt gebruikt in de geselecteerde instantie, samen met het tijdstempel van de meest recente uitvoering van de factureringsworkflow voor uw instantie.

* Het totale aantal actieve profielen dat binnen uw organisatie wordt gebruikt.

  >[!NOTE]
  >
  >Deze sectie is zichtbaar slechts als u veelvoudige instanties verbonden aan uw organisatie hebt.

* Het totale aantal actieve profielen dat is toegewezen aan uw organisatie.

In de onderste sectie ziet u het actieve profielgebruik in de afgelopen 30 dagen. U kunt dit tijdkader in 1 jaar veranderen gebruikend het filter dat in de hoger-juiste hoek wordt gevestigd. Als u de cursor boven de grafiek houdt, kunt u het exacte aantal actieve profielen ophalen dat wordt gebruikt voor de geselecteerde periode.
