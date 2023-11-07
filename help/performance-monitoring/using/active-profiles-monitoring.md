---
product: campaign
solution: Campaign
title: Bewaking van actieve profielen
description: Leer hoe u realtime-informatie krijgt over het nieuwste en historische gebruik en de evolutie van actieve profielen voor al uw Campaign-instanties.
feature: Control Panel, Monitoring
role: Admin
level: Experienced
exl-id: a157cc27-577f-490f-8c4f-0f203219cfb5
source-git-commit: 9d0686cd3bb0a037ae66b1a090c3f77d215ff61c
workflow-type: tm+mt
source-wordcount: '432'
ht-degree: 90%

---

# Actieve profielen controleren {#active-profiles-monitoring}

## Actieve profielen {#about-active-profiles}

>[!IMPORTANT]
>
>Bewaking van actieve profielen vanuit het Configuratiescherm is beschikbaar in de bètaversie en kan regelmatig en zonder kennisgeving worden bijgewerkt en gewijzigd. Dit is beschikbaar vanaf de Campaign Standard 10368-build.

Volgens uw contract worden al uw Campaign-instanties ingericht met een specifieke hoeveelheid actieve profielen die voor factureringsdoeleinden worden geteld. Raadpleeg uw meest recente contract voor informatie over het aantal aangeschafte actieve profielen.

‘Profiel’ betreft een datarecord (bijv. een record in de nmsRecipient-tabel of een externe tabel met een cookie-id, klant-id, mobiele id of andere informatie die relevant is voor een bepaald kanaal) die een eindklant, prospect of lead vertegenwoordigt.

Profielen worden als actief beschouwd als ze de afgelopen twaalf maanden via een kanaal zijn getarget of gecommuniceerd.

>[!NOTE]
>
>Er wordt geen rekening gehouden met de kanalen Facebook en Twitter.

Voor meer informatie over actieve profielen raadpleegt u de documentaties voor [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/profiles-and-audiences/managing-profiles/active-profiles.html?lang=nl) en [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/profile-management/about-profiles.html?lang=nl#active-profiles).

## Het gebruik van actieve profielen controleren {#monitoring-active-profiles}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_active_profile"
>title="Informatie over actieve profielen controleren"
>abstract="Op dit tabblad kunt u realtime-informatie krijgen over het nieuwste en historische gebruik en de evolutie van actieve profielen voor elk in uw Campaign-instanties en uw organisatie."

Om uw actieve profielgebruik in het Configuratiescherm te controleren gaat u naar het tabblad **[!UICONTROL Performance Monitoring]** > **[!UICONTROL Active Profiles]** en selecteert u de gewenste instantie van **[!UICONTROL Instance List]**.

Er wordt informatie weergegeven over uw gebruik van actieve profielen.

![](assets/active-profiles-graph.png)

In het bovenste gedeelte wordt de volgende informatie weergegeven:

* Het aantal actieve profielen dat momenteel wordt gebruikt in de geselecteerde instantie, samen met het tijdstempel van de meest recente uitvoering van de factureringsworkflow voor uw instantie.

* Het totale aantal actieve profielen dat binnen uw organisatie wordt gebruikt.

  >[!NOTE]
  >
  >Dit gedeelte is alleen zichtbaar als er meerdere exemplaren aan uw organisatie zijn gekoppeld.

* Het totale aantal actieve profielen dat is toegewezen aan uw organisatie.

Het onderste gedeelte biedt een visuele weergave van het actieve profielgebruik gedurende de afgelopen 30 dagen. U kunt dit tijdschema wijzigen naar 1 jaar met behulp van het filter in de rechterbovenhoek. Als u een van de grafiekbalken aanwijst, kunt u het exacte aantal actieve profielen ophalen dat in de geselecteerde periode is gebruikt.

Informatie over het gebruik van actieve profielen wordt bijgewerkt in het Configuratiescherm op basis van speciale informatie [!DNL Campaign] Technische workflows voor facturering die regelmatig op uw exemplaar worden uitgevoerd.

| Campaign-versie | Technische workflow | Runs |
|  ---  |  ---  |  ---  |
| Campaign Standard | [Facturering](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=nl) | Dagelijks |
| Campagne v7/v8 | [Facturering](https://experienceleague.adobe.com/docs/campaign-classic/using/automating-with-workflowsadvanced-management/about-technical-workflows.html) | Maandelijks |
