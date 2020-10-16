---
title: Configuratiescherm-releases
translation-type: tm+mt
source-git-commit: 1c7e5a830ff9a6b6a726cfbe30ca2ad264f1d8c6
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 79%

---


# Configuratiescherm-releases {#control-panel-releases}

Hier vindt u informatie over de nieuwste versies van het Configuratiescherm.

>[!NOTE]
>
>Houd er rekening mee dat Configuratiescherm alleen beschikbaar is voor klanten die op AWS worden gehost, behalve voor hybride omgevingen die nog niet worden ondersteund. U hebt geen upgrades nodig om toegang te krijgen tot het Configuratiescherm. Zorg ervoor dat u een Admin-gebruiker bent om het te kunnen openen.

## Oktober 2020 {#october-2020}

**Subdomeinconfiguratie die CNAMEs gebruikt**

Het Comité van de controle staat u nu toe om subdomain te vormen om met Adobe te werken gebruikend CNAMEs direct van de interface. [Meer informatie](subdomains-certificates/using/setting-up-new-subdomain.md)

**Verbeteringen voor databasecontrole**

Het **[!UICONTROL Database monitoring]** tabblad is uitgebreid met extra metriek, zodat u gedetailleerde informatie kunt krijgen over de bronnen die ruimte in uw database verbruiken. [Meer informatie](performance-monitoring/using/database-monitoring.md)

## Juni 2020 {#june-2020}

**Leveringsontrole voor subdomein**

Na het delegeren van een nieuw subdomein kunt u nu met behulp van Configuratiescherm de controle volgen die door het Afleverteam wordt uitgevoerd. [Meer informatie](subdomains-certificates/using/setting-up-new-subdomain.md)

**Beheer van GPG-sleutels**

Met Configuratiescherm kunt u nu twee GPG-sleutels genereren, zodat u de data die in Campaign binnenkomen, gemakkelijk kunt ontsleutelen. Bovendien hebben we een functie toegevoegd waarmee u een openbare GPG-sleutel kunt installeren om data te versleutelen die Campaign verlaten. [Meer informatie](instances-settings/using/gpg-keys-management.md)
* [Campaign Standard-zelfstudievideo&#39;s](https://docs.adobe.com/content/help/en/campaign-standard-learn/tutorials/administrating/control-panel/gpg-key-management/gpg-key-management-overview.html)
* [Campaign Classic-zelfstudievideo&#39;s](https://docs.adobe.com/content/help/en/campaign-classic-learn/tutorials/administrating/control-panel-acc/gpg-key-management/gpg-key-management-overview.html)

**Bewaking van actieve profielen**

Met Configuratiescherm kunt u nu het aantal actieve profielen bewaken dat door uw instanties wordt gebruikt en dat voor factureringsdoeleinden wordt geteld. [Meer informatie](performance-monitoring/using/active-profiles-monitoring.md)

>[!IMPORTANT]
>
>Bewaking van actieve profielen vanuit het Configuratiescherm is beschikbaar in de bètaversie en kan regelmatig worden bijgewerkt en gewijzigd zonder kennisgeving.
>
>Deze functie is beschikbaar voor klanten die op AWS worden gehost via de Campaign Standard-build 10368 en de Campaign Classic-build 8931. Als u een eerdere build gebruikt, moet u een upgrade uitvoeren om deze functie te kunnen gebruiken.

## Mei 2020 {#may-2020}

**Certificaatbeheer voor CNAME-subdomeinen**

Het Comité van de controle staat u nu toe om de SSL certificaten van uw subdomeinen te vernieuwen die met de methode CNAME zijn gevormd. [Meer informatie](subdomains-certificates/using/renewing-subdomain-certificate.md)

## April 2020 {#april-2020}

**Beheer van Google-TXT-records**

Voeg een Google-TXT-record voor websiteverificatie toe aan al uw subdomeinen die worden gebruikt om e-mails naar Gmail-adressen te verzenden via het Configuratiescherm van Campaign. [Meer informatie](subdomains-certificates/using/managing-txt-records.md)

**Bewaking van databaseruimte**

Het Configuratiescherm van Campaign is uitgerust met mogelijkheden voor databasecontrole, waarmee u uw gebruik van de databaseruimte op aanvraag en na verloop van tijd kunt weergeven. [Meer informatie](performance-monitoring/using/database-monitoring.md)

**E-mailwaarschuwingen**

Het Configuratiescherm van Campaign is uitgerust met mogelijkheden voor realtime-e-mailwaarschuwingen, zodat u kunt inloggen bij het Configuratiescherm en zich kunt aanmelden voor waarschuwingen als de prestaties van uw systeem kunnen verslechteren of als een handeling nodig is om hoge prestaties voor de toekomst te garanderen. [Meer informatie](performance-monitoring/using/email-alerting.md)

## Januari 2020 {#january-2020}

*22 januari 2020*

We hebben nieuwe mogelijkheden voor Admin-gebruikers toegevoegd om subdomeinen te configureren en SSL-certificaten te vernieuwen via het Configuratiescherm.

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
