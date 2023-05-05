---
product: campaign
solution: Campaign
title: Doorvoer en latentiebewaking
description: Ontdek hoe u de doorvoer en latentie van uw Campaign-instanties kunt controleren in het configuratiescherm.
feature: Control Panel
role: Architect
level: Experienced
exl-id: eddef17f-0667-4b43-bc56-2b1aeeae61bb
source-git-commit: ea738ea3764e4651e0eb7b4bcc68a9f7b3c8d1e5
workflow-type: ht
source-wordcount: '424'
ht-degree: 100%

---

# Doorvoer en latentiebewaking {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="Doorvoer en latentiebewaking "
>abstract="Op dit tabblad kunt u controleren hoe de leveringsdoorvoer en latentie zich gedurende een bepaalde periode ontwikkelen op uw instanties. Schakel over naar de tabelweergave voor informatie over leveringen die bijdragen aan de doorvoer."

Met het Configuratiescherm kunt u de doorvoer en latentie van de levering voor elk van uw instanties controleren.

>[!IMPORTANT]
>
>Deze functie is beschikbaar voor alle Campaign Standard v8-klanten en voor Campaign v7-klanten met buildnummer 9032 en hoger, inclusief [zelfstandige implementaties](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/deployment-types-/standalone-deployment.html?lang=nl) (zonder mid-instantie).

Het is belangrijk om te bewaken hoe de leveringsdoorvoer en latentie zich ontwikkelen over een bepaalde periode om het gebruik van uw instanties te begrijpen en ervoor te zorgen dat ze goed presteren.

Deze informatie wordt beschikbaar gemaakt in het configuratiescherm voor elk van uw Campaign-instanties op de kaart **[!UICONTROL Performance Monitoring]**, het tabblad **[!UICONTROL Throughputs & Latency]** (het kan maximaal 1 uur duren voordat de cijfers worden weergegeven in het configuratiescherm).

>[!NOTE]
>
>Alle cijfers in dit gebied zijn schattingen en alleen ter informatie.

![](assets/throughput-latencies-overview.png)

Standaard worden gegevens voor de huidige dag weergegeven. U kunt de weergegeven tijdsduur wijzigen met de knoppen **[!UICONTROL 6 months]**, **[!UICONTROL 30 days]** en **[!UICONTROL 7 days]**. Gegevens worden gepresenteerd:
* per uur voor 1 dag en weergave van 7 dagen,
* elke 6 uur voor een weergave van 30 dagen,
* dagelijkse weergave gedurende 6 maanden.

U kunt informatie ook visualiseren in tabelindeling met sorteerbare kolommen in plaats van een grafiek. Klik hiervoor op de knop **[!UICONTROL Visualization settings]** en selecteer vervolgens **[!UICONTROL Table]**.

![](assets/throughput-latencies-table.png)

## Doorvoercontrole {#throughput}

Het gebied **[!UICONTROL Throughput]** geeft informatie over het aantal berichten dat per uur wordt verzonden vanuit de geselecteerde Campaign-instantie voor alle communicatiekanalen waar u recht op hebt.

>[!NOTE]
>
>Voor Campaign v7/v8 is het getoonde doorvoernummer de doorvoer die van MID-instanties (midsourcing) wordt bereikt. Voor MKT-implementaties (standalone marketing) (zonder enige MID-instantie) wordt in plaats daarvan de doorvoer van de MKT-instantie getoond.

Bovendien kunt u met het configuratiescherm de ID&#39;s van de top 5 leveringen identificeren die bijdragen aan de doorvoer voor de geselecteerde periode. Deze informatie is alleen beschikbaar in de tabelweergave:

![](assets/throughput-latencies-top5.png)

## Latentie controleren {#latency}

Het gebied **[!UICONTROL Latency]** biedt informatie over de latentie die op de geselecteerde instantie wordt aangetroffen bij het verzenden van realtimetransactiecommunicatie.

>[!NOTE]
>
>Houd er rekening mee dat informatie over de **Profiellatentie** ook alleen beschikbaar is voor [!DNL Campaign Standard]-instanties.

Latenties worden vastgelegd en visualiseerd met een percentiel van 95 en 99, wat betekent dat 95% en 99% van de verzoeken sneller moeten zijn dan de opgegeven latentie.

![](assets/throughput-latencies-latency.png)

Standaard wordt de latentie voor alle kanalen weergegeven. Met de vervolgkeuzelijst kunt u de latentie voor een specifiek kanaal visualiseren.

![](assets/throughput-latencies-filter.png)

>[!NOTE]
>
>Kanaalfilters zijn alleen beschikbaar voor Campaign Classic v7/v8-instanties.
