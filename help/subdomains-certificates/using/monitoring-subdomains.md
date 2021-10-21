---
product: campaign
solution: Campaign
title: SSL-certificaten van subdomeinen bewaken
description: Leer hoe u de SSL-certificaten van uw subdomeinen kunt bewaken
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: 8dce5b9d1eb59b7ebc8ef1f73f7552dcf61077a1
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 21%

---

# Uw subdomeinen controleren {#monitoring-subdomains}

>[!AVAILABILITY]
>
>Deze functie is niet beschikbaar voor Campaign v8.

Het is van essentieel belang om uw subdomeinen te controleren om ervoor te zorgen dat alle behoorlijk worden gevormd om met Adobe Campaign te werken.

De lijst met subdomeinen voor elk van uw productie-instanties is rechtstreeks toegankelijk wanneer u de **[!UICONTROL Subdomains & Certificates]** kaart.

De **[!UICONTROL Last verification]** de kolom geeft aan wanneer een subdomein voor het laatst is geverifieerd. U kunt een verificatie op elk gewenst moment starten door te klikken op de knop **...** / **[!UICONTROL Verify subdomain]** knop.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe raadt het gebruik van subdomeinen zonder certificaatdatum niet aan, omdat dit kan betekenen dat deze subdomeinen problemen met betrekking tot de leverbaarheid hebben.

Wanneer het lanceren van een controle, worden verscheidene verrichtingen uitgevoerd om te controleren dat subdomain correct wordt gevormd (de controle van de instantiekant, e-mail die test verzendt, enz.)

Als de verificatie van het subdomein mislukt, neemt u contact op met de klantenservice van Adobe voor verder onderzoek.

**Verwante onderwerpen:**

* [Het SSL-certificaat van een subdomein verlengen](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Branding van subdomeinen](../../subdomains-certificates/using/subdomains-branding.md)
