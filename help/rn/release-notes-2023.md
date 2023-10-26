---
title: Aanvullende informatie 2023
description: Deze pagina bevat een lijst met alle in 2023 uitgebrachte releases van het Configuratiescherm.
exl-id: 9a83e32a-4c11-4784-a6fe-341ce9ebc7a7
source-git-commit: a8e2fb9789e9755aa6b9c55019816d7e748606ec
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 100%

---

# Aanvullende informatie 2023 {#rn-2023}

## September 2023 {#september-2023}

<table>
<thead>
<tr>
<th><strong>DMARC- en BIMI-recordbeheer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><p>U kunt nu DMARC- en BIMI-records rechtstreeks vanuit het Configuratiescherm toevoegen:

<ul><li><strong>DMARC-records</strong> bieden een manier om het domein van de afzender te verifiëren en ongeoorloofd gebruik van het domein voor kwaadaardige doeleinden te voorkomen. <a href="../subdomains-certificates/using/dmarc.md">Meer informatie over het toevoegen van DMARC-records</a></li>
<li>Met <strong>BIMI-records</strong> kunt u een goedgekeurd logo naast uw e-mails in het postvak IN van e-mailproviders weergeven om merkherkenning en vertrouwen te verbeteren. <a href="../subdomains-certificates/using/bimi.md">Meer informatie over het toevoegen van BIMI-records</a></li></ul>
</td>
</tr>
</tbody>
</table>

## Juni 2023 {#june-2023}

* U kunt nu de SSL-certificaten van al gedelegeerde subdomeinen rechtstreeks vanuit de lijst met subdomeinen delegeren naar Adobe. [Meer informatie](../subdomains-certificates/using/delegate-ssl.md)

* De afzender van e-mailmeldingen is gewijzigd naar `"alert@notifications.campaign.adobe.com"`.

## Verbeteringen in mei 2023 {#may-2023}

**SSL-certificaten van subdomeinen delegeren naar Adobe**

U kunt nu de SSL-certificaten van uw subdomeinen laten beheren door Adobe. Als u CNAME&#39;s gebruikt om uw subdomein in te stellen, worden er automatisch certificatenrecords gemaakt en verstrekt om een certificaat te genereren in uw domeinhostingoplossing.

Deze mogelijkheid is alleen beschikbaar als u een nieuw subdomein instelt. U kunt geen certificaten delegeren voor bestaande gedelegeerde subdomeinen. [Meer informatie](../subdomains-certificates/using/setting-up-new-subdomain.md)

>[!NOTE]
>
>Door Adobe beheerde SSL is een kosteloze functie die gratis beschikbaar is voor gebruikers.

## Maart 2023 {#march-2023}

**Subdomeindelegatie verwijderen voor CNAME&#39;s**

U kunt nu de delegatie van subdomeinen verwijderen die zijn geconfigureerd met gebruik van CNAME&#39;s. [Meer informatie](../subdomains-certificates/using/remove-delegated-subdomains.md)

## Februari 2023 {#february-2023}

**Delegatie verwijderen voor subdomeinen die zijn gedelegeerd aan Adobe**

U kunt nu de delegatie verwijderen van een subdomein dat volledig is gedelegeerd aan Adobe. [Meer informatie](../subdomains-certificates/using/remove-delegated-subdomains.md)

>[!NOTE]
>
>De verwijdering van de delegatie is momenteel niet beschikbaar voor subdomeinen die met behulp van CNAME&#39;s zijn ingesteld.

**Servicekalender**

Servicekalender biedt nu een kalenderweergave om belangrijke gebeurtenissen bij te houden die plaatsvinden in uw instanties. Daarnaast is er informatie toegevoegd over de meldingen die zijn verzonden naar gebruikers die zich hebben aangemeld voor waarschuwingen van het Configuratiescherm. [Meer informatie](../service-events/service-events.md)

![](assets/do-not-localize/gif-calendar.gif)

## Januari 2023 {#january-2023}

**Nieuwe mogelijkheid voor hybride hostingmodellen**

Klanten met een hybride hostingmodel kunnen nu IP-adressen toevoegen aan de toelatingslijst voor toegang tot MID-instanties. [Meer informatie](../instances-settings/using/ip-allow-listing-instance-access.md)

**Certificate Signing Request-uitbreiding (CSR)**

Het veld Plaats/Locatie is nu optioneel tijdens het genereren van de Certificate Signing Request (CSR).
