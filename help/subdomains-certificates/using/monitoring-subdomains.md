---
title: SSL-certificaten van subdomeinen controleren
description: Leer hoe u de SSL-certificaten van uw subdomeinen kunt controleren
translation-type: tm+mt
source-git-commit: a2c19296894ff893987290cb287dc7002ab999e5
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# De subdomeinen controleren {#monitoring-subdomains}

Het is van essentieel belang dat u de subdomeinen in de gaten houdt om ervoor te zorgen dat deze allemaal correct zijn geconfigureerd voor Adobe Campaign.

De lijst met subdomeinen voor elk van uw productie-instanties is rechtstreeks toegankelijk wanneer u de **[!UICONTROL Subdomains & Certificates]** kaart selecteert.

De **[!UICONTROL Last verification]** kolom geeft aan wanneer een subdomein voor het laatst is geverifieerd. U kunt een verificatie op elk gewenst moment starten door op de knop **..** / **[!UICONTROL Verify subdomain]** knop.

![](assets/subdomain_verification.png)

>[!IMPORTANT]
>
>Adobe raadt het gebruik van subdomeinen zonder certificaatdatum af, omdat dit kan betekenen dat er voor deze subdomeinen problemen met betrekking tot de leverbaarheid optreden.

Wanneer het lanceren van een controle, worden verscheidene verrichtingen uitgevoerd om te controleren dat subdomain correct wordt gevormd (de controle van de instantiekant, e-mail die test verzendt, enz.)

Als de verificatie van het subdomein mislukt, neemt u contact op met de klantenservice van Adobe voor verder onderzoek.

**Verwante onderwerpen:**

* [SSL-certificaten toevoegen (zelfstudie video)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [SSL-certificaat van een subdomein vernieuwen](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Branding van subdomeinen](../../subdomains-certificates/using/subdomains-branding.md)
