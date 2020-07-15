---
title: SSL-certificaten van subdomeinen bewaken
description: Leer hoe u de SSL-certificaten van uw subdomeinen kunt bewaken
translation-type: ht
source-git-commit: f22e356b283ee2601c948d5c1d514a9a59c58451
workflow-type: ht
source-wordcount: '402'
ht-degree: 100%

---


# SSL-certificaten van subdomeinen bewaken {#monitoring-ssl-certificates}

## Informatie over SSL-certificaten {#about-ssl-certificates}

Adobe Campaign raadt u aan de subdomeinen te beveiligen die als host dienen voor uw landingspagina’s, met name de subdomeinen die vertrouwelijke informatie van uw klanten verzamelen.

**SSL-versleuteling (Secure Socket Layer)** zorgt ervoor dat de subdomeinen die u aan Adobe hebt gedelegeerd, beveiligd zijn. Wanneer uw klant een webformulier invult of een landingspagina bezoekt die wordt gehost door Adobe Campaign, wordt de informatie standaard verzonden via een niet-beveiligd protocol (HTTP). Verzend informatie met een HTTPS-protocol voor extra beveiliging. Bijvoorbeeld: het subdomeinadres http://info.mijnwebsite.com/ is dan https://info.mijnwebsite.com/.

**SSL-certificaten zelf worden niet op de gedelegeerde subdomeinen geïnstalleerd**. Zij worden geïnstalleerd op bijbehorende subdomeinen, hoofdzakelijk de subdomeinen die landingspagina’s, resourcepagina’s, enz., hosten.

**SSL-certificaten worden verstrekt voor een specifieke periode** (1 jaar, 60 dagen, enz.). Zodra een certificaat verloopt, kunt u problemen ondervinden wanneer u de landingspagina’s opent of resources van het subdomein gebruikt. Om dit te verhinderen kunt u met het Configuratiescherm de SSL-certificaten van uw subdomeinen bewaken en het verlengingsproces voor deze certificaten starten.

![](assets/no_certificate.png)

## SSL-certificaten bewaken {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="Subdomeindetails"
>abstract="Haal informatie op over uw subdomeinen."

De status van de SSL-certificaten van uw subdomeinen is rechtstreeks beschikbaar in de lijst met subdomeinen wanneer u de kaart **[!UICONTROL Subdomains & Certificates]** selecteert.

Subdomeinen worden gerangschikt op de dichtstbijzijnde vervaldatum van het SSL-certificaat, met visuele informatie over de vervaldatum, in dagen:

* **Groen**: het subdomein heeft geen certificaat dat in de komende 60 dagen verloopt.
* **Oranje**: een of meer subdomeinen hebben een certificaat dat in de komende 60 dagen verloopt.
* **Rood**: een of meer subdomeinen hebben een certificaat dat in de komende 30 dagen verloopt.
* **Grijs**: er is geen certificaat geïnstalleerd voor het subdomein.

![](assets/subdomains_list.png)

Klik op de knop **[!UICONTROL Subdomain Details]** voor meer informatie over een subdomein.
De lijst met alle verwante subdomeinen wordt weergegeven. Deze omvat meestal subdomeinen van landingspagina’s, resourcepagina’s, enz.

Het tabblad **[!UICONTROL Sender info]** bevat informatie over de geconfigureerde inboxes (Sender, Reply to, Error email).

![](assets/subdomain_details.png)

Als het SSL-certificaat van een van uw subdomeinen bijna verlopen is, kunt u het rechtstreeks verlengen via het Configuratiescherm. Raadpleeg voor meer informatie deze sectie: [Het SSL-certificaat van een subdomein verlengen](../../subdomains-certificates/using/renewing-subdomain-certificate.md).

>[!IMPORTANT]
>
>Verlenging van subdomeinen vanuit het Configuratiescherm is beschikbaar in de bètaversie en kan regelmatig worden bijgewerkt en gewijzigd zonder kennisgeving.

**Verwante onderwerpen:**

* [SSL-certificaten toevoegen (videotutorial)](https://docs.adobe.com/content/help/nl-NL/campaign-learn/campaign-standard-tutorials/administrating/control-panel/adding-ssl-certificates.html)
* [Het SSL-certificaat van een subdomein verlengen](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Branding van subdomeinen](../../subdomains-certificates/using/subdomains-branding.md)
