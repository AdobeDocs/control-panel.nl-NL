---
title: Branding van subdomeinen
description: Meer informatie over branding van subdomeinen
translation-type: ht
source-git-commit: 80b35e82116b064a7b141d957ab79ecfc9a99026
workflow-type: ht
source-wordcount: '467'
ht-degree: 100%

---


# Branding van subdomeinen {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Subdomeinen en SSL-certificaten"
>abstract="Bewaak uw subdomeinen en de bijbehorende SSL-certificaten."
>additional-url="https://docs.adobe.com/content/help/nl-NL/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="SSL-certificaten van uw subdomeinen bewaken"

>[!IMPORTANT]
>
>Delegatie van subdomeinen vanuit het Configuratiescherm is beschikbaar in de bètaversie en kan regelmatig worden bijgewerkt en gewijzigd zonder kennisgeving.

## Waarom zou ik subdomeinen instellen? {#why-setting-up-subdomains}

Een subdomein is een divisie van uw domein die kan worden gebruikt om uw merken of diverse traffictypen (transactieberichten, marketinginformatie, enz.) te isoleren.

Neem bijvoorbeeld het domein mybrand.com, dat wordt gebruikt om zowel transactionele als marketingmededelingen te verzenden. In dit geval kunt u twee subdomeinen instellen:

* Het subdomein info.mybrand.com voor uw transactionele mededelingen (bevestiging van aankopen, herstel van wachtwoorden, enz.)
* Het subdomein marketing.mybrand.com voor e-mails aan prospects

Op deze manier kunt u de reputatie van uw domein en andere subdomeinen beter in stand houden. Als de marketing.mybrand.com-subdomeinen bijvoorbeeld door internetproviders aan de lijst van afgewezen domeinen werden toegevoegd vanwege slechte leverbaarheid, zou dit voorkomen dat het hele domein mybrand.com en het subdomein info.mybrand.com aan de lijst van afgewezen domeinen worden toegevoegd.

## Methoden voor subdomeindelegatie {#subdomain-delegation-methods}

De delegatie van subdomeinen geeft u de mogelijkheid om een subsectie van uw domein (technisch een DNS-zone) voor gebruik met Adobe Campaign te delegeren. Beschikbare instelmethoden zijn:

* **Volledige subdomeindelegatie aan Adobe Campaign** (aanbevolen): Het subdomein wordt volledig gedelegeerd aan Adobe. Adobe kan Campaign als een beheerde service leveren door alle DNS-aspecten die voor het leveren, weergeven en volgen van e-mailcampagnes nodig zijn, te controleren en handhaven.

* **Gebruik van CNAME’s** (niet aanbevolen en niet ondersteund via het Configuratiescherm): Maak een subdomein en gebruik CNAME’s om te verwijzen naar Adobe-specifieke records. Met deze configuratie delen Adobe en de klant de verantwoordelijkheid voor het onderhoud van DNS.

In de onderstaande tabel wordt een overzicht gegeven van de werking van deze methoden en van het betrokken inspanningsniveau:

| Delegatiemethode | Werking | Inspanningsniveau |
|---|---|---|
| **Volledige delegatie** | Maak het subdomein en de naamruimterecord. Adobe configureert vervolgens alle DNS-records die voor Adobe Campaign nodig zijn.<br/><br/>In deze setup is Adobe volledig verantwoordelijk voor het beheer van het subdomein en alle DNS-records. | Laag |
| **CNAME, aangepaste methode** | Maak het subdomein en de naamruimterecord. Adobe verstrekt dan de records die in uw DNS servers moeten worden geplaatst en configureert de overeenkomstige waarden in de DNS-servers van Adobe Campaign.<br/><br/>In deze configuratie delen u en Adobe de verantwoordelijkheid voor het onderhoud van DNS. | Hoog |

Aanvullende informatie over domeindelegatie is beschikbaar in [deze documentatie](https://helpx.adobe.com/nl/campaign/kb/domain-name-delegation.html).

Als u vragen hebt over methoden voor subdomeindelegatie, neemt u contact op met het Afleverteam van Adobe, of met de klantenservice om advies over aflevering te vragen.

**Verwante onderwerpen:**

* [Een nieuw subdomein instellen](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Subdomeinen delegeren (videotutorial)](https://docs.adobe.com/content/help/nl-NL/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [Uw subdomeinen bewaken](../../subdomains-certificates/using/monitoring-subdomains.md)
