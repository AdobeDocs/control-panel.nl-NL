---
title: Bewaking van databases
description: Leer hoe u uw Campagne-database kunt controleren in het Configuratiescherm
translation-type: tm+mt
source-git-commit: e5646fdccd47b4180fd0f9d561f61c04cd515c01
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 1%

---


# Bewaking van databases {#database-monitoring}


## Over databases {#about-instances-databases}

Volgens uw contract, wordt elk van uw instanties van de Campagne provisioned met een specifieke hoeveelheid gegevensbestandruimte.

Databases omvatten alle **middelen**, **workflows** en **gegevens** die in Adobe Campaign zijn opgeslagen.

In tijd, kunnen de gegevensbestanden hun maximumcapaciteit bereiken, vooral als de opgeslagen middelen nooit van de instantie worden geschrapt, of als er vele werkschema&#39;s in een gepauzeerde staat zijn.

Het overlopen van een instantiedatabase kan leiden tot verschillende problemen (het niet aanmelden, e-mails verzenden enz.). Het is daarom van essentieel belang dat de databases van uw instanties worden gecontroleerd om optimale prestaties te garanderen.

>[!NOTE]
>
>De hoeveelheid databaseruimte die in het Configuratiescherm wordt weergegeven, geeft mogelijk niet de hoeveelheid databaseruimte weer die in het contract is opgegeven. Meestal krijgt u tijdelijk meer databaseruimte om de prestaties van uw systeem te garanderen.

## Gebruik van databases controleren {#monitoring-instances-database}

Met het Configuratiescherm kunt u het databasegebruik voor elk van uw campagneinstanties controleren. Volg de onderstaande stappen om dit te doen.

1. Open de **[!UICONTROL Performance Monitoring]**-kaart en selecteer vervolgens het tabblad **[!UICONTROL Databases]**.

1. Selecteer de gewenste instantie in het **[!UICONTROL Instance List]** menu.

   Het bovenste gebied biedt informatie over de databasecapaciteit van de instantie en de gebruikte ruimte.

   ![](assets/databases_dashboard.png)

   Het onderste gebied biedt een grafische weergave van het minimum-, gemiddelde en maximale databasegebruik in de afgelopen 7 dagen, plus de drempel van 90% databasegebruik, weergegeven door een rode stippelcurve.

   U kunt de weergegeven tijdsperiode wijzigen met de beschikbare filters in de rechterbovenhoek.

   Voor een betere leesbaarheid kunt u ook een of meer curven in de grafiek markeren. U doet dit door ze te selecteren in de **[!UICONTROL Aggregation Type]** legenda.

   Als u de muis boven de grafiek houdt, kunt u gedetailleerde informatie over de geselecteerde tijdsperiode ophalen.

   ![](assets/databases_dashboard_detail.png)

>[!NOTE]
>
>Naast dit dashboard kunt u meldingen ontvangen wanneer een van uw databases zijn capaciteit bereikt. Meld u aan voor [e-mailwaarschuwingen om dit te doen](../../performance-monitoring/using/email-alerting.md)

## Overbelasting van database voorkomen {#preventing-database-overload}

De Norm van de campagne en Klassiek bieden diverse manieren om overconsumptie van gegevensbestandschijfruimte te verhinderen.

In de onderstaande sectie vindt u nuttige informatie uit Campagne-documentatie om u te helpen uw databasegebruik te optimaliseren:

**Workflows bewaken**

* [Aanbevolen werkstromen](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/workflow-general-operation/best-practices-workflows.html) (campagnestandaard)
* [Uitvoering](https://docs.adobe.com/help/en/campaign-classic/using/automating-with-workflows/monitoring-workflows/monitoring-workflow-execution.html) van workflows controleren (Campagne Classic)

**Database-onderhoud**

* Technisch werkschema voor opschonen van databases ([Campagne Standard](https://docs.adobe.com/help/en/campaign-standard/using/administrating/application-settings/technical-workflows.html#list-of-technical-workflows) / [Campagne Classic](https://docs.adobe.com/help/en/campaign-classic/using/monitoring-campaign-classic/data-processing/database-cleanup-workflow.html))
* [Handleiding voor](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/database-maintenance/recommendations.html) databaseonderhoud (Campagne Classic)
* [Problemen met](https://docs.adobe.com/content/help/en/campaign-classic/using/monitoring-campaign-classic/troubleshooting/database-performances.html) databaseprestaties oplossen (Campagne Classic)
* [Databasegerelateerde opties](https://docs.adobe.com/help/en/campaign-classic/using/installing-campaign-classic/appendices/configuring-campaign-options.html#database) (Campagne Classic)
