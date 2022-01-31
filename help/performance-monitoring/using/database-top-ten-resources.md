---
product: campaign
solution: Campaign
title: De tien belangrijkste tijdelijke bronnen
description: Leer hoe u in het Configuratiescherm de tien grootste tijdelijke bronnen kunt controleren die worden gegenereerd door workflows en leveringen in uw Campagne-database.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: 9accc4306bacab3bc27922f495c19138f905b1c5
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 92%

---

# De tien belangrijkste tijdelijke bronnen {#top-10}

In het gedeelte **[!UICONTROL Top 10 temporary resources]** worden de tien grootste tijdelijke bronnen weergegeven die worden gegenereerd door workflows en verzendingen.

Het controleren van workflows en verzendingen die grote tijdelijke resources maken, is een belangrijke stap bij de controle van uw database. Als een tijdelijke bron te veel databaseruimte in beslag neemt, zorg er dan voor dat deze workflow of verzending noodzakelijk is en navigeer naar uw versie om deze te stoppen.

>[!IMPORTANT]
>
>De algemene aanbeveling is om te voorkomen dat er niet **meer dan 40 kolommen** zijn in niet-standaardresources.

![](assets/database-top10.png)

>[!NOTE]
>
>Als een workflow een groot aantal tabeltellingen of een grote databaseomvang bevat, raden we aan de workflow te controleren om te onderzoeken waarom deze zoveel gegevens genereert.
>
>Bronnen voor Campaign Standard en Classic zijn ook beschikbaar aan het eind van deze pagina om u te helpen bij het voorkomen van databaseoverbelasting.

De knop **[!UICONTROL View all]** geeft u toegang tot gedetailleerde informatie over deze tijdelijke bronnen.

![](assets/database-top10-view.png)

De waarde in de kolom **[!UICONTROL Keep interim results]** geeft aan of de optie is ingeschakeld (1) of uitgeschakeld (0) in Campaign. Hiermee kunt u de resultaten van de overgangen tussen de verschillende activiteiten van een workflow opslaan (zie documentatie voor [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html?lang=nl) en [Campaign Classic](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/executing-a-workflow/managing-execution-options.html?lang=nl)).

>[!IMPORTANT]
>
>Deze optie mag nooit worden ingeschakeld in een productieworkflow. Deze wordt gebruikt om de resultaten te analyseren en is alleen ontworpen voor testdoeleinden. De optie mag daarom alleen worden gebruikt in ontwikkelings- of testomgevingen.
>
>Als de waarde in het configuratiescherm aangeeft dat de optie is ingeschakeld voor een van uw workflows, raden we u sterk aan deze optie uit te schakelen in Campaign.
