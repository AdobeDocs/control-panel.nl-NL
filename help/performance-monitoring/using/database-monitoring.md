---
product: campaign
solution: Campaign
title: Databasebewaking
description: Leer de Campaign-database controleren in het configuratiescherm
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: 71dce2340ccc3da406e29b9a650c9bcf6a5d938c
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 84%

---

# Databasebewaking {#database-monitoring}

## Versies van databases {#about-instances-databases}

Volgens uw contract wordt elk van uw Campaign-versies voorzien van een specifieke hoeveelheid gegevensbestandruimte.

Databases omvatten alle **assets**, **workflows** en **gegevens** die zijn opgeslagen in Adobe Campaign.

Na verloop van tijd kunnen databases hun maximale capaciteit bereiken, vooral als de opgeslagen bronnen nooit vanuit de versie worden verwijderd of als er veel workflows in een gepauzeerde staat zijn.

Het overlopen van een versie van een database kan leiden tot verschillende problemen (niet kunnen aanmelden, e-mails verzenden, enz.). Het is daarom van essentieel belang dat de databases van uw versies worden gecontroleerd om optimale prestaties te garanderen.

## Databasegebruik controleren{#monitoring-database-usage}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_database"
>title="Databasebewaking"
>abstract="Op dit tabblad krijgt u realtime-informatie over het meest recente en historische databasegebruik en de evolutie voor elk van uw Campaign-versies."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/performance-monitoring/about-performance-monitoring.html?lang=nl" text="Prestatiebewaking"

Met het configuratiescherm kunt u het databasegebruik voor elk van uw Campaign-versies controleren. Open hiervoor de **[!UICONTROL Performance Monitoring]**-kaart en selecteer het tabblad **[!UICONTROL Databases]**.

Selecteer de gewenste versie vanuit de **[!UICONTROL Instance List]** om informatie weer te geven over de capaciteit van de versiedatabase en de gebruikte ruimte.

Bovendien kunt u berichten ontvangen wanneer één van uw databases zijn capaciteit bereikt. Hiervoor wordt u lid van [e-mailwaarschuwingen](../../performance-monitoring/using/email-alerting.md).

>[!NOTE]
>
>Neem contact op met de klantenservice als de hoeveelheid beschikbare databaseruimte zoals weergegeven in het configuratiescherm niet overeenkomt met de hoeveelheid die in uw contract is gespecificeerd.

![](assets/databases_dashboard.png)

De gegevens van dit dashboard worden bijgewerkt op basis van de **[!UICONTROL Database cleanup technical workflow]** die op uw instantie van de Campagne loopt (zie [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/administrating/application-settings/technical-workflows.html?lang=nl#list-of-technical-workflows) en [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html?lang=nl) documentatie). U kunt de laatste keer controleren dat de workflow onder de **[!UICONTROL Used Space]** en **[!UICONTROL Provided Space]** metriek. Als de workflow al meer dan drie dagen niet meer is uitgevoerd, raden wij u aan de klantenservice van Adobe te raadplegen zodat ze kunnen onderzoeken waarom de workflow niet wordt uitgevoerd.

Dit dashboard bevat aanvullende metriek waarmee u het gebruik van de database van de instantie kunt analyseren. Deze worden in de volgende secties beschreven:

* [Databasegebruik](../../performance-monitoring/using/database-utilization.md)
* [Overzicht van opslag](../../performance-monitoring/using/database-storage-overview.md)
* [De tien belangrijkste tijdelijke bronnen](../../performance-monitoring/using/database-top-ten-resources.md)
* [Actieve query&#39;s](../../performance-monitoring/using/database-active-queries.md)

![](assets/do-not-localize/how-to-video.png) Deze functie in video ontdekken met [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=nl) of [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/performance-monitoring/monitoring-databases.html?lang=nl).
