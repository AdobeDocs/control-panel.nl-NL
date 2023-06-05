---
product: campaign
solution: Campaign
title: SSL-certificaten van subdomeinen bewaken
description: Leer hoe u de SSL-certificaten van uw subdomeinen kunt bewaken
feature: Control Panel
role: Architect
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
source-git-commit: 0628e9eb12da4dcc33b2ea21c9ef31bb7ba4f9c4
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 70%

---

# SSL-certificaten van subdomeinen bewaken {#monitoring-ssl-certificates}

## Informatie over SSL-certificaten {#about-ssl-certificates}

Adobe Campaign raadt u aan de subdomeinen te beveiligen die als host dienen voor uw landingspagina’s, met name de subdomeinen die vertrouwelijke informatie van uw klanten verzamelen.

**SSL-codering (Secure Socket Layer)** zorgt ervoor dat subdomeinen die u om met Adobe vormde te werken veilig zijn. Wanneer uw klant een webformulier invult of een landingspagina bezoekt die wordt gehost door Adobe Campaign, wordt de informatie standaard verzonden via een niet-beveiligd protocol (HTTP). Verzend informatie met een HTTPS-protocol voor extra beveiliging. Bijvoorbeeld: het subdomeinadres http://info.mijnwebsite.com/ is dan https://info.mijnwebsite.com/.

**SSL-certificaten zijn niet geïnstalleerd op de geconfigureerde subdomeinen zelf**. Zij worden geïnstalleerd op bijbehorende subdomeinen, hoofdzakelijk de subdomeinen die landingspagina’s, resourcepagina’s, enz., hosten.

**SSL-certificaten worden verstrekt voor een specifieke periode** (1 jaar, 60 dagen, enz.). Zodra een certificaat verloopt, kunt u problemen ondervinden wanneer u de landingspagina’s opent of resources van het subdomein gebruikt. Om dit te verhinderen kunt u met het Configuratiescherm de SSL-certificaten van uw subdomeinen bewaken en het verlengingsproces voor deze certificaten starten.

![](assets/no_certificate.png)

## SSL-certificaten van subdomeinen delegeren aan Adobe

Wanneer u een nieuw subdomein instelt, kunt u het SSL-certificaat laten beheren door Adobe. Dit wordt ten zeerste aanbevolen, omdat Adobe het certificaat automatisch maakt en elk jaar vernieuwt voordat het certificaat verloopt.

Als u CNAMEs aan opstelling gebruikt subdomain delegatie, zal Adobe certificaatverslagen verstrekken in uw domein ontvangende oplossing te gebruiken om uw certificaat te produceren.

>[!NOTE]
>
>De delegatie van SSL-certificaten is alleen beschikbaar wanneer u een nieuw subdomein instelt. Dit is niet beschikbaar voor al gedelegeerde subdomeinen.

De delegatie van SSL-certificaten wordt ingeschakeld wanneer u een nieuw subdomein instelt. Leer hoe u verder kunt gaan in [deze sectie](setting-up-new-subdomain.md).

## SSL-certificaten bewaken {#monitoring-certificates}

>[!CONTEXTUALHELP]
>id="cp_subdomain_details"
>title="Subdomeindetails"
>abstract="Haal informatie op over de SSL-certificaten van uw subdomeinen."

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

**Verwante onderwerpen:**

* [Het SSL-certificaat van een subdomein verlengen](../../subdomains-certificates/using/renewing-subdomain-certificate.md)
* [Branding van subdomeinen](../../subdomains-certificates/using/subdomains-branding.md)
