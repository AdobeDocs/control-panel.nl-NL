---
product: campaign
solution: Campaign
title: Uw subdomeinen bewaken
description: Controleer uw subdomeinen om ervoor te zorgen dat allen behoorlijk om met Adobe Campaign worden gevormd te werken.
feature: Control Panel
role: Architect
level: Experienced
exl-id: edd55d07-bf0b-44b0-8281-be69c698d5e8
source-git-commit: f0c3df4727e89e3f6127fe4563908b955ccb820c
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 7%

---

# Uw subdomeinen bewaken {#monitoring-subdomains}

>[!CONTEXTUALHELP]
>id="cp_subdomain_undelegate"
>title="Subdomeindelegatie verwijderen"
>abstract="In dit scherm kunt u de delegatie van een subdomein naar Adobe verwijderen. Houd er rekening mee dat dit proces na verzending niet kan worden teruggedraaid of gestopt.<br><br>Als u de delegatie van een primair domein voor de geselecteerde instantie probeert te verwijderen, wordt u gevraagd het domein te kiezen dat het zal vervangen."

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
