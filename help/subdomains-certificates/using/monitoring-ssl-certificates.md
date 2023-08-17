---
product: campaign
solution: Campaign
title: SSL-certificaten van subdomeinen bewaken
description: Leer hoe u de SSL-certificaten van uw subdomeinen kunt bewaken
feature: Control Panel
role: Architect
level: Experienced
exl-id: a7888e1c-259d-4601-951b-0f1062d90dc2
source-git-commit: 01da21a883804b9c79c7ee4056d984f3df6cb96c
workflow-type: tm+mt
source-wordcount: '567'
ht-degree: 64%

---

# SSL-certificaten van subdomeinen bewaken {#monitoring-ssl-certificates}

## Informatie over SSL-certificaten {#about-ssl-certificates}

Adobe Campaign raadt u aan de subdomeinen te beveiligen die als host dienen voor uw landingspagina’s, met name de subdomeinen die vertrouwelijke informatie van uw klanten verzamelen.

**SSL-codering (Secure Socket Layer)** zorgt ervoor dat subdomeinen die u om met Adobe vormde te werken veilig zijn. Wanneer uw klant een webformulier invult of een landingspagina bezoekt die wordt gehost door Adobe Campaign, wordt de informatie standaard verzonden via een niet-beveiligd protocol (HTTP). Verzend informatie met een HTTPS-protocol voor extra beveiliging. Bijvoorbeeld: het subdomeinadres http://info.mijnwebsite.com/ is dan https://info.mijnwebsite.com/.

**SSL-certificaten zijn niet geïnstalleerd op de geconfigureerde subdomeinen zelf**. Zij worden geïnstalleerd op bijbehorende subdomeinen, hoofdzakelijk de subdomeinen die landingspagina’s, resourcepagina’s, enz., hosten.

**SSL-certificaten worden verstrekt voor een specifieke periode** (1 jaar, 60 dagen, enz.). Zodra een certificaat verloopt, kunt u problemen ondervinden wanneer u de landingspagina’s opent of resources van het subdomein gebruikt. Om dit te verhinderen kunt u met het Configuratiescherm de SSL-certificaten van uw subdomeinen bewaken en het verlengingsproces voor deze certificaten starten.

![](assets/no_certificate.png)

## SSL-certificaatbeheer {#management}

De controle van SSL-certificaten is een sleutel om ervoor te zorgen dat uw subdomeinen veilig zijn. Met het Controlebord, kunt u de SSL certificaten van uw subdomeinen direct installeren en vernieuwen door zich, of hen delegeren aan Adobe zodat dit proces automatisch zonder actie wordt uitgevoerd die van uw kant wordt vereist.

Het delegeren van SSL-certificaten van uw subdomeinen aan Adobe wordt sterk aanbevolen, omdat Adobe het certificaat automatisch maakt en elk jaar vernieuwt voordat het certificaat verloopt. Hierdoor wordt het risico op fouten verminderd die kunnen optreden wanneer certificaten handmatig worden beheerd. [Leer hoe u SSL-certificaten van subdomeinen kunt delegeren aan Adobe](delegate-ssl.md)

Hieronder vindt u een uitgebreid overzicht van de effecten die zijn gekoppeld aan handmatig certificaatbeheer, in tegenstelling tot het delegeren van deze bewerking naar Adobe:

|       | Door de klant beheerd certificaat | Certificaat met beheerde Adobe |
|  ---  |  ---  |  ---  |
| Certificaatprovider | Certificeringsinstanties van derden | Adobe via AWS Certificate Managers |
| Handmatige stappen | CSR-productie, aanschaf en installatie van certificaten | Geen |
| Vernieuwingsproces | Verantwoordelijkheid van de klant | Automatisch beheerd door Adobe |
| Subdomeinbeveiliging | Domein kan onbeveiligde subdomeinen (tracking, mirror en res) hebben, tenzij u certificaten installeert/vernieuwt. | Elk nieuw domein (als gekozen voor beheerde Adobe) zal alle subdomeinen hebben die door gebrek worden beveiligd. |
| Certificaatkosten | De klant draagt de kosten van certificaten | Gratis |

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
