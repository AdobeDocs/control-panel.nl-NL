---
title: Branding van subdomeinen
description: Meer informatie over branding van subdomeinen
translation-type: tm+mt
source-git-commit: 198c974d269289a6a9e5a87314662dba0bc85aff
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 0%

---


# Branding van subdomeinen {#subdomains-branding}

>[!CONTEXTUALHELP]
>id="cp_certificate_management"
>title="Subdomeinen en SSL-certificaten"
>abstract="Controleer de subdomeinen en de bijbehorende SSL-certificaten."
>additional-url="https://docs.adobe.com/content/help/en/control-panel/using/subdomains-and-certificates/monitoring-ssl-certificates.html" text="SSL-certificaten van uw subdomeinen controleren"

>[!IMPORTANT]
>
>De delegatie van subdomeinen van het Controlebord is beschikbaar in bèta, en onderworpen aan regelmatige updates en wijzigingen zonder bericht.

## Waarom instellen van subdomeinen? {#why-setting-up-subdomains}

Een subdomein is een afdeling van uw domein dat kan worden gebruikt om uw merken, of diverse types van verkeer (transactieberichten, marketing informatie, enz.) te isoleren.

Neem het voorbeeld van het &quot;mybrand.com&quot;domein, dat wordt gebruikt om zowel transactie als marketing mededelingen te verzenden. In dit geval kunt u twee subdomeinen instellen:

* &quot;info.mybrand.com&quot;subdomain voor uw transactionele mededelingen (koopt bevestiging, wachtwoordterugstellen enz.),
* Het subdomein &#39;marketing.mybrand.com&#39; voor uw prospectieve e-mails.

Op deze manier kunt u de reputatie van uw domein en andere subdomeinen beter behouden. Als de subdomeinen &quot;marketing.mybrand.com&quot; bijvoorbeeld door Internet Service Providers aan de bloklijst werden toegevoegd vanwege slechte leverantie, zou dit voorkomen dat het hele domein &quot;mybrand.com&quot; en het subdomein &quot;info.mybrand.com&quot; aan de bloklijst worden toegevoegd.

## Methoden voor subdomeindelegatie {#subdomain-delegation-methods}

De delegatie van subdomein staat u toe om een onderafdeling van uw domein (technisch een &quot;DNS streek&quot;) voor gebruik met Adobe Campaign te delegeren. Beschikbare instellingsmethoden zijn:

* **Volledige subdomeindelegatie naar Adobe Campaign** (aanbevolen): Het subdomein wordt volledig gedelegeerd aan Adobe. Adobe kan de Campagne als beheerde dienst leveren door alle aspecten van DNS te controleren en te handhaven die voor het leveren, het teruggeven en het volgen van e-mailcampagnes worden vereist.

* **Gebruik van CNAME** &#39;s (niet aanbevolen en niet ondersteund via het Configuratiescherm): Maak een subdomein en gebruik CNAME&#39;s om te verwijzen naar Adobe-specifieke records. Met deze setup delen zowel Adobe als de klant de verantwoordelijkheid voor het onderhoud van DNS.

In de onderstaande tabel wordt een overzicht gegeven van de werking van deze methoden en van het impliciete inspanningsniveau:

| Delegatiemethode | Hoe werkt het | inspanningsniveau |
|---|---|---|
| **Volledige delegatie** | Maak het subdomein en de naamruimte-record. Adobe configureert vervolgens alle DNS-records die voor Adobe Campaign zijn vereist.<br/><br/>In deze installatie is Adobe volledig verantwoordelijk voor het beheer van het subdomein en alle DNS-records. | Laag |
| **CNAME, aangepaste methode** | Maak het subdomein en de naamruimte-record. Adobe zal dan de verslagen verstrekken die in uw DNS servers moeten worden geplaatst en zal de overeenkomstige waarden in de servers van Adobe Campaign DNS vormen.<br/><br/>In deze setup delen u en Adobe de verantwoordelijkheid voor het onderhoud van DNS. | Hoog |

Aanvullende informatie over domeindelegatie is beschikbaar in [deze documentatie](https://helpx.adobe.com/campaign/kb/domain-name-delegation.html).

Als u een vraag hebt over methoden voor subdomeindelegatie, neemt u contact op met het team van Adobe Deliverability of neemt u uiteindelijk contact op met de klantenservice om advies over de leveringsbaarheid aan te vragen.

**Verwante onderwerpen:**

* [Een nieuw subdomein instellen](../../subdomains-certificates/using/setting-up-new-subdomain.md)
* [Subdomeinen delegeren (videozelfstudie)](https://docs.adobe.com/content/help/en/campaign-learn/campaign-standard-tutorials/administrating/control-panel/subdomain-delegation.html)
* [De subdomeinen controleren](../../subdomains-certificates/using/monitoring-subdomains.md)
