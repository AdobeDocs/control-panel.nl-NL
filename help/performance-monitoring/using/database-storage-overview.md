---
product: campaign
solution: Campaign
title: Overzicht van opslag
description: Leer hoe u in het Configuratiescherm de verschillende campagnebronnen kunt controleren die databaseruimte op uw instanties verbruiken.
feature: Control Panel
role: Architect
level: Experienced
exl-id: bb9e1ce3-2472-4bc1-a82a-a301c6bf830e
source-git-commit: c52094b8145bdd84aa9e71430a811b8a7b32354d
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 56%

---

# Overzicht van opslag {#storage-overview}

>[!CONTEXTUALHELP]
>id="cp_dbdetails_storagedetails"
>title="Overzicht van opslag"
>abstract="Op dit tabblad krijgt u gedetailleerde informatie over de verschillende Campaign-bronnen die databaseruimte verbruiken."

Het gedeelte **[!UICONTROL Storage overview]** biedt een grafische weergave van de ruimte die wordt ingenomen door:

* **[!UICONTROL System resources]**

  Let op: als systeembronnen een groot deel van de databaseruimte verbruiken, raden wij u aan de klantenservice te raadplegen.

* **[!UICONTROL Out-of-the-box tables]** standaard geleverd bij uw Campaign-versies,
* **[!UICONTROL Temporary tables]** gemaakt door workflows en verzendingen;
* **[!UICONTROL Non-out of the box tables]** gegenereerd na het maken van aangepaste bronnen.

![](assets/database-storage-overview.png)

Klik op de knop **[!UICONTROL View details]** voor meer informatie over de verschillende assets die databaseruimte verbruiken.

U kunt de vervolgkeuzelijst gebruiken om uw zoek- en weergavetabellen alleen te verfijnen van een specifiek elementtype (workflows, leveringen, ontvangers).

![](assets/database-storage-details.png)

Merk op dat dit scherm u ook toestaat om werkschemaparameters te controleren die specifieke aandacht kunnen vereisen om het even welke kwesties op uw instanties te vermijden. Meer informatie in [deze pagina](workflow-monitoring.md).
