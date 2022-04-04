---
product: campaign
solution: Campaign
title: Doorvoer en latentiebewaking
description: Ontdek hoe u de doorvoer en latentie van uw Campaign-instanties kunt bewaken in het configuratiescherm.
feature: Control Panel
role: Architect
level: Experienced
exl-id: eddef17f-0667-4b43-bc56-2b1aeeae61bb
source-git-commit: 84fe0aeb10bc5e535a7ab54a3316a51a1a32b3ca
workflow-type: ht
source-wordcount: '314'
ht-degree: 100%

---

# Doorvoer en latentiebewaking {#throughputs-latency-monitoring}

>[!CONTEXTUALHELP]
>id="cp_performancemonitoring_throughputslatencies"
>title="Doorvoer en latentiebewaking "
>abstract="Op dit tabblad kunt u bewaken hoe de leveringsdoorvoer en latentie zich gedurende een bepaalde periode ontwikkelen op uw instanties."

Met het Configuratiescherm kunt u de doorvoer en latentie van de levering voor elk van uw instanties controleren.

>[!IMPORTANT]
>
>Deze functie is beschikbaar voor alle Campaign Standard- en v8-klanten en voor Campaign V7-klanten met buildnummers 9032,9330, 9346 of 9349 die [standalone](https://experienceleague.adobe.com/docs/campaign-classic/using/installing-campaign-classic/deployment-types-/standalone-deployment.html?lang=nl) implementaties (zonder tussenkomst).

Het is belangrijk om te bewaken hoe de leveringsdoorvoer en latentie zich ontwikkelen over een bepaalde periode om het gebruik van uw instanties te begrijpen en ervoor te zorgen dat ze goed presteren.

Deze informatie wordt beschikbaar gemaakt in het configuratiescherm voor elk van uw Campaign-instanties op de kaart **[!UICONTROL Performance Monitoring]**, het tabblad **[!UICONTROL Throughputs & Latency]** (het kan maximaal 1 uur duren voordat de cijfers worden weergegeven in het configuratiescherm).

* Het gebied **[!UICONTROL Throughput]** geeft informatie over het aantal berichten dat per uur wordt verzonden vanuit de geselecteerde Campaign-instantie voor alle communicatiekanalen waar u recht op hebt.

   >[!NOTE]
   >
   >Voor Campaign v7/v8 is het getoonde doorvoernummer de doorvoer die van MID-instanties (midsourcing) wordt bereikt. Voor MKT-implementaties (standalone marketing) (zonder enige MID-instantie) wordt in plaats daarvan de doorvoer van de MKT-instantie getoond.

* Het gebied **[!UICONTROL Latency]** biedt informatie over de latentie die op de geselecteerde instantie wordt aangetroffen bij het verzenden van realtimetransactiecommunicatie. Latenties worden vastgelegd en visualiseerd met een percentiel van 95 en 99, wat betekent dat 95% en 99% van de verzoeken sneller moeten zijn dan de opgegeven latentie.

![](assets/throughput-latencies-overview.png)

>[!NOTE]
>
>Alle cijfers in dit gebied zijn schattingen en alleen ter informatie.

Standaard worden gegevens voor de huidige dag weergegeven. U kunt de weergegeven tijdsduur wijzigen met de knoppen **[!UICONTROL 6 months]**, **[!UICONTROL 30 days]** en **[!UICONTROL 7 days]**.

U kunt informatie ook visualiseren in tabelindeling met sorteerbare kolommen in plaats van een grafiek. Klik hiervoor op de knop **[!UICONTROL Visualization settings]** en selecteer vervolgens **[!UICONTROL Table]**.

![](assets/throughput-latencies-table.png)
