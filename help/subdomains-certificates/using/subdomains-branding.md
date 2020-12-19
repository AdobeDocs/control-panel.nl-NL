---
product: campaign
solution: Campaign
title: Branding van subdomeinen
description: Meer informatie over branding van subdomeinen
translation-type: tm+mt
source-git-commit: 2d84a5ebe8dbf42264c94f882a51180aae2a58a6
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 79%

---


# Branding van subdomeinen {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Subdomeinen en SSL-certificaten"
>abstract="Bewaak uw subdomeinen en de bijbehorende SSL-certificaten."
>additional-url="https://docs.adobe.com/content/help/nl-NL/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="SSL-certificaten van uw subdomeinen bewaken"

## Waarom zou ik subdomeinen instellen? {#why-setting-up-subdomains}

>[!IMPORTANT]
>
>Subdomeinconfiguratie van het Controlebord is beschikbaar in bèta, en onderworpen aan regelmatige updates en wijzigingen zonder bericht.

Een subdomein is een divisie van uw domein die kan worden gebruikt om uw merken of diverse traffictypen (transactieberichten, marketinginformatie, enz.) te isoleren.

Neem bijvoorbeeld het domein mybrand.com, dat wordt gebruikt om zowel transactionele als marketingmededelingen te verzenden. In dit geval kunt u twee subdomeinen instellen:

* Het subdomein info.mybrand.com voor uw transactionele mededelingen (bevestiging van aankopen, herstel van wachtwoorden, enz.)
* Het subdomein marketing.mybrand.com voor e-mails aan prospects

Op deze manier kunt u de reputatie van uw domein en andere subdomeinen beter in stand houden. Als de marketing.mybrand.com-subdomeinen bijvoorbeeld door internetproviders aan de lijst van afgewezen domeinen werden toegevoegd vanwege slechte leverbaarheid, zou dit voorkomen dat het hele domein mybrand.com en het subdomein info.mybrand.com aan de lijst van afgewezen domeinen worden toegevoegd.

## Methoden voor subdomeinconfiguratie {#subdomain-delegation-methods}

De configuratie van subdomain staat u toe om een onderafdeling van uw domein (technisch een &quot;DNS streek&quot;) voor gebruik met Adobe Campaign te vormen. Beschikbare instelmethoden zijn:

* **Volledige subdomeindelegatie aan Adobe Campaign** (aanbevolen): Het subdomein wordt volledig gedelegeerd aan Adobe. Adobe kan Campaign als een beheerde service leveren door alle DNS-aspecten die voor het leveren, weergeven en volgen van e-mailcampagnes nodig zijn, te controleren en handhaven.

* **Gebruik van CNAME**&#39;s: Creeer subdomain en gebruik CNAMEs om aan Adobe-specifieke verslagen te richten. Met deze configuratie delen Adobe en de klant de verantwoordelijkheid voor het onderhoud van DNS.

In de onderstaande tabel wordt een overzicht gegeven van de werking van deze methoden en van het betrokken inspanningsniveau:

| Configuratiemethode | Werking | Inspanningsniveau |
|---|---|---|
| **Volledige delegatie** | Maak het subdomein en de naamruimterecord. Adobe configureert vervolgens alle DNS-records die voor Adobe Campaign nodig zijn.<br/><br/>In deze setup is Adobe volledig verantwoordelijk voor het beheer van het subdomein en alle DNS-records. | Laag |
| **CNAME, aangepaste methode** | Maak het subdomein en de naamruimterecord. Adobe verstrekt dan de records die in uw DNS servers moeten worden geplaatst en configureert de overeenkomstige waarden in de DNS-servers van Adobe Campaign.<br/><br/>In deze configuratie delen u en Adobe de verantwoordelijkheid voor het onderhoud van DNS. | Hoog |

Aanvullende informatie over domeinconfiguratie is beschikbaar in [deze documentatie](https://helpx.adobe.com/nl/campaign/kb/domain-name-delegation.html).

Als u om het even welke vraag betreffende de methodes van de subdomeinconfiguratie hebt, bereik uit aan het team van de Leverbaarheid van de Adobe, of uiteindelijk contacteer de Zorg van de Klant om het raadplegen van de Leverbaarheid te verzoeken.

## Gebruiksgevallen van subdomeinen (Campaign Classic){#subdomains-use-cases}

Bij het instellen van subdomeinen voor Campaign Classic-instanties moet u het geval selecteren waarvoor het subdomein wordt gebruikt (zie [Een nieuw subdomein instellen](../../subdomains-certificates/using/setting-up-new-subdomain.md)).

Mogelijke gevallen van gebruik zijn:

* **Marketing communications**: Communicatie die voor commerciële doeleinden is bestemd. Voorbeeld: e-mailcampagne voor verkoop.

* **Transactional &amp; operational communications**: Transactionele communicatie bevat informatie gericht op de voltooiing van een proces dat de ontvanger met u is begonnen. Voorbeeld: koopbevestiging, e-mail voor opnieuw instellen van wachtwoord. Operationele communicatie betreft de uitwisseling van informatie, ideeën, en meningen binnen en buiten de organisatie, zonder commercieel doel.

**Met het oog op bezorgbaarheid kunt u uw subdomeinen het beste onderverdelen op basis van gebruiksscenario’s**. Hierdoor wordt de reputatie van elk subdomein geïsoleerd en beschermd. Als uw subdomein bijvoorbeeld voor marketingmededelingen door internetproviders wordt toegevoegd aan de lijst van afgewezen domeinen, wordt uw subdomein voor transactionele communicatie niet beïnvloed en kan dit subdomein nog steeds mededelingen verzenden.

**U kunt subdomeinen voor zowel het Marketing als het Transactionele gebruiksgevallen** vormen:

* Bij marketinggebruiksscenario’s worden subdomeinen geconfigureerd op **MID**-instanties (Mid-sourcing).
* Voor transactionele gebruiksscenario’s worden subdomeinen geconfigureerd op ALLE **RT**-instanties (Message Center/Real-time messaging) om connectiviteit te verzekeren. De subdomeinen werken daarom met al uw RT-instanties.

>[!NOTE]
>
>Als u Campaign Classic gebruikt, kunt u in het Configuratiescherm zien welke RT-/MID-instanties zijn verbonden met de marketinginstantie waarmee u werkt. Raadpleeg voor meer informatie de sectie [Instantiedetails](../../instances-settings/using/instance-details.md).

**Verwante onderwerpen:**

* [Een nieuw subdomein instellen](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Uw subdomeinen bewaken](../../subdomains-certificates/using/monitoring-subdomains.md)
