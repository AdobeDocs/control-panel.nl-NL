---
product: campaign
solution: Campaign
title: Configuratiescherm-releases
description: Deze pagina bevat alle nieuwe functies en verbeteringen voor het Configuratiescherm
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 84fe0aeb10bc5e535a7ab54a3316a51a1a32b3ca
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Configuratiescherm-releases {#control-panel-releases}

Deze pagina bevat een overzicht van alle nieuwe functies en verbeteringen voor het Configuratiescherm.

>[!NOTE]
>
>Het Configuratiescherm is alleen toegankelijk voor Admin-gebruikers. Meer informatie over machtigingen in [deze sectie](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=nl#discover-control-panel).
>
>Voor Campaign v7 moet uw exemplaar worden gehost op Amazon Web Services (AWS) en worden bijgewerkt naar de nieuwste [Stabiele build campagne](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=nl#rn-statuses) (of om 9032 of hoger te bouwen). Leer hoe u uw versie kunt controleren in [dit gedeelte](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=nl#getting-your-campaign-version). Controleer of uw versie wordt gehost op AWS door de volgende stappen te volgen op [deze pagina](faq.md#hosted-aws).

## Maart 2022 {#march-2022}

<table>
<thead>
<tr>
<th><strong>Producties en beschikbaarheid van bewaking van wachttijden</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Throughputs en latency monitoring zijn nu beschikbaar aan alle Campaign Standard en v8 klanten met bouwstijlaantallen 9032,9330, 9346 of 9349 die standalone plaatsingen (zonder enige middeninstantie) hebben.</p><p>Raadpleeg voor meer informatie de <a href="performance-monitoring/using/thoughputs-latencies.md">gedetailleerde documentatie.</a></p>
</td>
</tr>
</tbody>
</table>

## Februari 2022 {#february-2022}

<table>
<thead>
<tr>
<th><strong>Workflowparameters bewaken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu workflowparameters bewaken waarvoor specifieke aandacht nodig kan zijn om problemen met uw instanties te voorkomen. </p><p>Raadpleeg de <a href="performance-monitoring/using/workflow-monitoring.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

## Januari 2022 {#january-2022}

<table>
<thead>
<tr>
<th><strong>Actieve query's bewaken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In het configuratiescherm kunt u nu query's bewaken die het langst op uw instanties worden uitgevoerd.</p><p>Raadpleeg de <a href="performance-monitoring/using/database-active-queries.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Doorvoer en latentiebewaking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu bewaken hoe de leveringsdoorvoer en latentie zich gedurende een bepaalde periode ontwikkelen op uw instanties.</p><p>Raadpleeg de <a href="performance-monitoring/using/thoughputs-latencies.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>SSL-certificaatbewerkingen op nieuwe subdomeinen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>SSL-certificaatbewerkingen kunnen nu worden uitgevoerd op een nieuw ingestelde subdomein, zelfs als de leverbaarheidscontrole nog wordt uitgevoerd.</p><p>Raadpleeg de <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

## Oktober 2021 {#october-2021}

<table>
<thead>
<tr>
<th><strong>IP-bereik en geldigheidsperiode openbare sleutel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Het is nu mogelijk om een duur voor de beschikbaarheid van IP waaiers en openbare sleutels te plaatsen. </p><p>Raadpleeg voor meer informatie de <a href="sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list">Aanbieding in IP-bereik toegestaan</a> en <a href="sftp/using/key-management.md#installing-ssh-key">Sleutelbeheer</a> secties.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>IP-bereik en openbare-sleuteluitgave</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>U kunt nu de <a href="sftp/using/ip-range-allow-listing.md#editing-ip-ranges">IP-bereiken</a> en <a href="sftp/using/key-management.md#editing-public-keys">openbare sleutels</a> die u maakt. Deze functie is niet beschikbaar voor de items die zijn gemaakt vóór de huidige release van het Configuratiescherm.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Waarschuwing bij SFTP IP-bereik en vervaldatum van openbare sleutel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De functie voor e-mailwaarschuwingen bevat nu waarschuwingen over SFTP IP waarmee lijsten kunnen verlopen en de vervaldatum van de openbare sleutel voor SFTP.</p><p>Raadpleeg de <a href="performance-monitoring/using/email-alerting.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Volledige ondersteuning met Campaign v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De <strong>Subdomein</strong> en <strong>Certificaat</strong> beheermogelijkheden worden nu ondersteund door het Configuratiescherm in Adobe Campaign v8.</a>.</p>
</td>
</tr>
</tbody>
</table>

## Augustus 2021 {#august-2021}

<table>
<thead>
<tr>
<th><strong>Ondersteuning voor Campagne v8</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Het Configuratiescherm is nu beschikbaar voor Adobe Campaign v8, behalve voor de <strong>Subdomein</strong> en <strong>Certificaat</strong> beheermogelijkheden, die nog niet worden ondersteund.</p><p>Raadpleeg voor meer informatie de <a href="https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html" target="blank">Campagne v8-documentatie</a>.</p>
</td>
</tr>
</tbody>
</table>

## Oktober 2020 {#october-2020}

<table>
<thead>
<tr>
<th><strong>Subdomeinconfiguratie met gebruik van CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met het Configuratiescherm kunt u nu rechtstreeks vanuit de interface met gebruik van CNAME-records een subdomein configureren om met Adobe te werken.</p><p>Raadpleeg de <a href="subdomains-certificates/using/setting-up-new-subdomain.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Verbeteringen voor databasebewaking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De controle van het gegevensbestand is verbeterd met extra metriek die u toestaan om gedetailleerde informatie over de middelen te krijgen die ruimte op uw gegevensbestand verbruiken.</p><p>Raadpleeg de <a href="performance-monitoring/using/database-monitoring.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

## Juni 2020 {#june-2020}

<table>
<thead>
<tr>
<th><strong>Leveringsontrole voor subdomein</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Na het delegeren van een nieuw subdomein kunt u nu met behulp van Configuratiescherm de controle volgen die door het Afleverteam wordt uitgevoerd.</p><p>Raadpleeg de <a href="subdomains-certificates/using/setting-up-new-subdomain.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Beheer van GPG-sleutels</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Configuratiescherm kunt u nu twee GPG-sleutels genereren, zodat u de data die in Campaign binnenkomen, gemakkelijk kunt ontsleutelen. Bovendien hebben we een functie toegevoegd waarmee u een openbare GPG-sleutel kunt installeren om data te versleutelen die Campaign verlaten.</p><p>Raadpleeg de <a href="instances-settings/using/gpg-keys-management.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Actieve profielen bewaken</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met Configuratiescherm kunt u nu het aantal actieve profielen bewaken dat door uw instanties wordt gebruikt en dat voor factureringsdoeleinden wordt geteld.</p><p>Raadpleeg de <a href="performance-monitoring/using/active-profiles-monitoring.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

>[!IMPORTANT]
>
>Bewaking van actieve profielen vanuit het Configuratiescherm is beschikbaar in de bètaversie en kan regelmatig worden bijgewerkt en gewijzigd zonder kennisgeving.

## Mei 2020 {#may-2020}

<table>
<thead>
<tr>
<th><strong>Certificaatbeheer voor CNAME-subdomeinen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Met het Configuratiescherm kunt u nu de SSL-certificaten verlengen van de subdomeinen die met de CNAME-methode zijn geconfigureerd.</p><p>Raadpleeg de <a href="subdomains-certificates/using/renewing-subdomain-certificate.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

## April 2020 {#april-2020}

<table>
<thead>
<tr>
<th><strong>Beheer van Google-TXT-records</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Voeg een Google-TXT-record voor websiteverificatie toe aan al uw subdomeinen die worden gebruikt om e-mails naar Gmail-adressen te verzenden via het Configuratiescherm van Campaign.</p><p>Raadpleeg de <a href="subdomains-certificates/using/managing-txt-records.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Bewaking van databaseruimte</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Het Configuratiescherm van Campaign is uitgerust met mogelijkheden voor databasecontrole, waarmee u uw gebruik van de databaseruimte op aanvraag en na verloop van tijd kunt weergeven.</p><p>Raadpleeg de <a href="performance-monitoring/using/database-monitoring.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>E-mailwaarschuwingen</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Het Configuratiescherm van Campaign is uitgerust met mogelijkheden voor realtime-e-mailwaarschuwingen, zodat u kunt inloggen bij het Configuratiescherm en zich kunt aanmelden voor waarschuwingen als de prestaties van uw systeem kunnen verslechteren of als een handeling nodig is om hoge prestaties voor de toekomst te garanderen.</p><p>Raadpleeg de <a href="performance-monitoring/using/email-alerting.md">gedetailleerde documentatie</a> voor meer informatie.</p>
</td>
</tr>
</tbody>
</table>

## Januari 2020 {#january-2020}

We hebben nieuwe mogelijkheden voor Admin-gebruikers toegevoegd om subdomeinen te configureren en SSL-certificaten te verlengen via het Configuratiescherm.

Raadpleeg deze pagina’s voor meer informatie:
* [Een nieuw subdomein instellen](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Het SSL-certificaat van een subdomein verlengen](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Deze functies zijn beschikbaar in de bètaversie en kunnen regelmatig worden bijgewerkt en gewijzigd zonder kennisgeving.

## September 2019 {#september-2019}

Er zijn nieuwe mogelijkheden toegevoegd waarmee Admin-gebruikers IP-adressen aan de lijst van gewenste personen kunnen toevoegen om verbinding te maken met instanties van Campagne v7/v8.
Bovendien kunnen Admin-gebruikers nu de lijst met Campagne v7/v8-instanties en de mogelijkheid om upgrades voor build uit te voeren, weergeven.

Raadpleeg de [desbetreffende documentatie](instances-settings/using/ip-allow-listing-instance-access.md) voor meer informatie.

## Augustus 2019 {#august-2019}

Er zijn nieuwe mogelijkheden toegevoegd waarmee Admin-gebruikers berichten kunnen ontvangen voordat SSL-certificaten voor hun domeinen verlopen. Raadpleeg de [gedetailleerde documentatie](subdomains-certificates/using/monitoring-ssl-certificates.md)voor meer informatie.

Bovendien kunnen Admin-gebruikers nu SSH-sleutels verwijderen die zijn toegevoegd om toegang te verkrijgen tot SFTP-servers.

## Juli 2019 {#july-2019}

We hebben nieuwe functies toegevoegd om beheergebruikers meer controle te geven over de instantie-instellingen van Campagne v7/v8. De nieuwe mogelijkheden van het Configuratiescherm omvatten de mogelijkheid om URL’s toe te voegen waarmee Adobe Campaign verbinding maakt voor data-/bestandsoverdracht.

Raadpleeg de [gedetailleerde documentatie](instances-settings/using/url-permissions.md)voor meer informatie.
