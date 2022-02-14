---
product: campaign
solution: Campaign
title: Configuratiescherm-releases
description: Opmerkingen bij de nieuwste release van het Configuratiescherm.
feature: Control Panel
role: Architect
level: Beginner
exl-id: 13aceffb-ceaa-4cfe-8741-95d66c5c6caa
source-git-commit: 76301a1e222da17a2b4fd58d68d24efd04b07b1c
workflow-type: tm+mt
source-wordcount: '858'
ht-degree: 70%

---

# Configuratiescherm-releases {#control-panel-releases}

Hier vindt u informatie over de meest recente Configuratiescherm-releases.

>[!NOTE]
>
>Het Configuratiescherm is alleen toegankelijk voor Admin-gebruikers. Meer informatie over machtigingen in [deze sectie](https://experienceleague.adobe.com/docs/control-panel/using/discover-control-panel/managing-permissions.html?lang=nl#discover-control-panel).
>
>Voor Campaign Classic v7 moet uw exemplaar worden gehost op Amazon Web Services (AWS) en worden bijgewerkt naar de nieuwste [Stabiele build campagne](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=nl#rn-statuses) (of om 9032 of hoger te bouwen). Leer hoe u uw versie kunt controleren in [dit gedeelte](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=nl#getting-your-campaign-version). Controleer of uw versie wordt gehost op AWS door de volgende stappen te volgen op [deze pagina](faq.md#hosted-aws).

## Januari 2022 {#january-2022}

**Actieve query&#39;s bewaken**

In het configuratiescherm kunt u nu query&#39;s bewaken die het langst op uw instanties worden uitgevoerd. [Meer informatie](performance-monitoring/using/database-active-queries.md)

**Doorvoer en latentiebewaking**

U kunt nu bewaken hoe de leveringsdoorvoer en latentie zich gedurende een bepaalde periode ontwikkelen op uw instanties. [Meer informatie](performance-monitoring/using/thoughputs-latencies.md)

**SSL-certificaatbewerkingen op nieuwe subdomeinen**

SSL-certificaatbewerkingen kunnen nu worden uitgevoerd op een nieuw ingestelde subdomein, zelfs als de leverbaarheidscontrole nog wordt uitgevoerd. [Meer informatie](subdomains-certificates/using/renewing-subdomain-certificate.md)

## Oktober 2021 {#october-2021}

**IP-bereik en geldigheidsperiode openbare sleutel**

Het is nu mogelijk om een duur voor de beschikbaarheid van IP waaiers en openbare sleutels te plaatsen. Lees meer in de [Aanbieding in IP-bereik toegestaan](sftp/using/ip-range-allow-listing.md#adding-ip-addresses-allow-list) en [Sleutelbeheer](sftp/using/key-management.md#installing-ssh-key) secties.

**IP-bereik en openbare-sleuteluitgave**

U kunt nu de [IP-bereiken](sftp/using/ip-range-allow-listing.md#editing-ip-ranges) en [openbare sleutels](sftp/using/key-management.md#editing-public-keys) die u maakt. Deze functie is niet beschikbaar voor de items die zijn gemaakt vóór de huidige release van het Configuratiescherm.

**Waarschuwing bij SFTP IP-bereik en vervaldatum van openbare sleutel**

De functie voor e-mailwaarschuwingen bevat nu waarschuwingen over SFTP IP waarmee lijsten kunnen verlopen en de vervaldatum van de openbare sleutel voor SFTP. [Meer informatie](performance-monitoring/using/email-alerting.md)

**Volledige ondersteuning met Campaign v8**

De **Subdomein** en **Certificaat** beheermogelijkheden worden nu ondersteund door het Configuratiescherm in Adobe Campaign v8.

## Augustus 2021 {#august-2021}

**Ondersteuning voor Campagne v8**

Het Configuratiescherm is nu beschikbaar voor Adobe Campaign v8, behalve voor de **Subdomein** en **Certificaat** beheermogelijkheden, die nog niet worden ondersteund. Meer informatie in [Campagne v8-documentatie](https://experienceleague.adobe.com/docs/campaign/campaign-v8/deploy/self-service.html){target=&quot;_blank&quot;}

## Oktober 2020 {#october-2020}

**Subdomeinconfiguratie met gebruik van CNAME-records**

Met het Configuratiescherm kunt u nu rechtstreeks vanuit de interface met gebruik van CNAME-records een subdomein configureren om met Adobe te werken. [Meer informatie](subdomains-certificates/using/setting-up-new-subdomain.md)

**Verbeteringen voor databasebewaking**

De controle van het gegevensbestand is verbeterd met extra metriek die u toestaan om gedetailleerde informatie over de middelen te krijgen die ruimte op uw gegevensbestand verbruiken. [Meer informatie](performance-monitoring/using/database-monitoring.md)

## Juni 2020 {#june-2020}

**Leveringsontrole voor subdomein**

Na het delegeren van een nieuw subdomein kunt u nu met behulp van Configuratiescherm de controle volgen die door het Afleverteam wordt uitgevoerd. [Meer informatie](subdomains-certificates/using/setting-up-new-subdomain.md)

**Beheer van GPG-sleutels**

Met Configuratiescherm kunt u nu twee GPG-sleutels genereren, zodat u de data die in Campaign binnenkomen, gemakkelijk kunt ontsleutelen. Bovendien hebben we een functie toegevoegd waarmee u een openbare GPG-sleutel kunt installeren om data te versleutelen die Campaign verlaten. [Meer informatie](instances-settings/using/gpg-keys-management.md)

**Bewaking van actieve profielen**

Met Configuratiescherm kunt u nu het aantal actieve profielen bewaken dat door uw instanties wordt gebruikt en dat voor factureringsdoeleinden wordt geteld. [Meer informatie](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>Bewaking van actieve profielen vanuit het Configuratiescherm is beschikbaar in de bètaversie en kan regelmatig worden bijgewerkt en gewijzigd zonder kennisgeving.

## Mei 2020 {#may-2020}

**Certificaatbeheer voor CNAME-subdomeinen**

Met het Configuratiescherm kunt u nu de SSL-certificaten verlengen van de subdomeinen die met de CNAME-methode zijn geconfigureerd. [Meer informatie](subdomains-certificates/using/renewing-subdomain-certificate.md)

## April 2020 {#april-2020}

**Beheer van Google-TXT-records**

Voeg een Google-TXT-record voor websiteverificatie toe aan al uw subdomeinen die worden gebruikt om e-mails naar Gmail-adressen te verzenden via het Configuratiescherm van Campaign. [Meer informatie](subdomains-certificates/using/managing-txt-records.md)

**Bewaking van databaseruimte**

Het Configuratiescherm van Campaign is uitgerust met mogelijkheden voor databasecontrole, waarmee u uw gebruik van de databaseruimte op aanvraag en na verloop van tijd kunt weergeven. [Meer informatie](performance-monitoring/using/database-monitoring.md)

**E-mailwaarschuwingen**

Het Configuratiescherm van Campaign is uitgerust met mogelijkheden voor realtime-e-mailwaarschuwingen, zodat u kunt inloggen bij het Configuratiescherm en zich kunt aanmelden voor waarschuwingen als de prestaties van uw systeem kunnen verslechteren of als een handeling nodig is om hoge prestaties voor de toekomst te garanderen. [Meer informatie](performance-monitoring/using/email-alerting.md)

## Januari 2020 {#january-2020}

*22 januari 2020*

We hebben nieuwe mogelijkheden voor Admin-gebruikers toegevoegd om subdomeinen te configureren en SSL-certificaten te verlengen via het Configuratiescherm.

Raadpleeg deze pagina’s voor meer informatie:
* [Een nieuw subdomein instellen](subdomains-certificates/using/setting-up-new-subdomain.md)
* [Het SSL-certificaat van een subdomein verlengen](subdomains-certificates/using/renewing-subdomain-certificate.md)

>[!IMPORTANT]
>
>Deze functies zijn beschikbaar in de bètaversie en kunnen regelmatig worden bijgewerkt en gewijzigd zonder kennisgeving.

## September 2019 {#september-2019}

*16 september 2019*

Er zijn nieuwe mogelijkheden toegevoegd waarmee Admin-gebruikers IP-adressen aan de lijst van gewenste IP-adressen kunnen toevoegen om verbinding te maken met Campaign Classic-instanties.
Bovendien kunnen Admin-gebruikers nu de lijst met Campaign Classic-instanties en geschiktheid voor het ontvangen van build-upgrades weergeven.

Raadpleeg de [desbetreffende documentatie](instances-settings/using/ip-allow-listing-instance-access.md) voor meer informatie.

## Augustus 2019 {#august-2019}

Er zijn nieuwe mogelijkheden toegevoegd waarmee Admin-gebruikers berichten kunnen ontvangen voordat SSL-certificaten voor hun domeinen verlopen. Raadpleeg de [gedetailleerde documentatie](subdomains-certificates/using/monitoring-ssl-certificates.md)voor meer informatie.

Bovendien kunnen Admin-gebruikers nu SSH-sleutels verwijderen die zijn toegevoegd om toegang te verkrijgen tot SFTP-servers.

## Juli 2019 {#july-2019}

We hebben nieuwe functies toegevoegd waarmee Admin-gebruikers meer controle kunnen krijgen over Campaign Classic-instantie-instellingen. De nieuwe mogelijkheden van het Configuratiescherm omvatten de mogelijkheid om URL’s toe te voegen waarmee Adobe Campaign verbinding maakt voor data-/bestandsoverdracht.

Raadpleeg de [gedetailleerde documentatie](instances-settings/using/url-permissions.md)voor meer informatie.
