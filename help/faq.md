---
title: Veelgestelde vragen over Configuratiescherm
description: Algemene vragen over het Configuratiescherm
translation-type: tm+mt
source-git-commit: 35723590195ef54df42d1d1df5b37490787f8836
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 71%

---


# Veelgestelde vragen {#faq}

## IMS Organisatie-id {#ims-org-id}

**Wat is een IMS-organisatie-id?**

Dit is een unieke id die aan uw instantie wordt gegeven wanneer u zich voor het eerst aanmeldt bij Adobe Experience Cloud. De notatie moet als volgt zijn: xxx@AdobeOrg.

Raadpleeg de documentatie bij [Adobe Experience Cloud](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html) voor meer informatie.

**Waar kan ik mijn IMS Organisatie ID vinden?**

U kunt onder andere naar [Adobe Experience Cloud Home](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]** gaan. You will find your IMS Organization ID at the bottom of Administration **[!UICONTROL Quick Access]** section. Meer informatie vindt u in de [documentatie van Adobe Experience Cloud](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html).

U kunt ook **Admin Console** starten. De IMS-organisatie-id is zichtbaar in uw URL en ziet er ongeveer als volgt uit: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**Waarom moet ik mijn IMS Organisatie-id kennen?**

We willen ervoor zorgen dat u de juiste informatie voor de juiste instantie krijgt voor het geval u meerdere instanties voor uw bedrijf gebruikt. Hierdoor kunt u de instellingen voor uw instantie beheren.

**Wat gebeurt er als ik meerdere IMS Organisatie-id&#39;s heb?**

U hebt mogelijk meer dan één IMS-organisatie-id als u toegang hebt tot meerdere Adobe-oplossingen. In dit geval is de juiste IMS Organisatie-id die u moet gebruiken, die welke u onder uw Adobe Campaign-instantie ziet.

>[!NOTE]
>
>Als u dezelfde IMS Organisatie-id hebt voor Adobe Campaign en Adobe Analytics, is dit geweldig. Een IMS-organisatie-id tussen Analytics en Campagne is een vereiste als u de oplossingen wilt integreren om te profiteren van complexe gebruikssituaties, zoals het achterlaten van winkelwagentjes (voor AA + AC).
>
>Als u verschillende IMS-organisatie-id&#39;s voor Adobe Campaign en Adobe Analytics hebt, neemt u contact op met de klantenservice om deze op één lijn te brengen.

**Hoe weet ik of mijn Adobe Campaign-instantie wordt gehost op AWS?**

Als u wilt controleren of uw instantie wordt gehost op AWS, voert u deze stappen uit:

1. Haal uw login-URL op. Dit is de URL die u gebruikt om u aan te melden bij uw Campaign-instantie. De URL eindigt meestal met .campaign.adobe.com of .neolane.net.
1. Open de terminal en voer vervolgens een **[!DNL nslookup]**-bewerking uit op de login-URL.

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. Er wordt informatie over uw instantie geretourneerd.

   ```
   doe-macOS% nslookup myinstance.campaign.adobe.com
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   myinstance.campaign.adobe.com
   canonical name = myinstance-mkt-prod1.campaign.adobe.com.
   myinstance-mkt-prod1.campaign.adobe.com
   canonical name = myinstance-mkt-prod1-1.campaign.adobe.com.
   Name: myinstance-mkt-prod1-1.campaign.adobe.com
   Address: 12.34.567.89
   ```

1. Voer een **nslookup**-bewerking op het geretourneerde IP-adres uit.

   `doe-macOS% nslookup 12.34.567.89`

1. Controleer de waarde ‘name’ in het geretourneerde resultaat. Als de waarde ‘amazonaws.com’ bevat, betekent dit dat uw instantie wordt gehost op AWS.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>Als u naar AWS wilt worden gemigreerd, start u het proces door contact op te nemen met uw Customer Success Manager.

## Configuratiescherm {#control-panel}

**Wat is het Configuratiescherm?**

Met het Configuratiescherm kunnen productbeheerders verschillende instellingen rechtstreeks beheren en de capaciteit bewaken van SFTP-servers die op Adobe Campaign zijn aangesloten.

**Wat zijn zoal de huidige mogelijkheden van het Configuratiescherm?**

Met het Configuratiescherm kunt u de opslag bijhouden, IP-adressen toevoegen aan de lijst van gewenste IP-adressen, SSH-sleutels voor uw SFTP-servers beheren op basis van uw behoeften, enzovoort.

Raadpleeg voor meer informatie de documentatie over acties die door het Configuratiescherm worden ondersteund.

**Is het Configuratiescherm alleen voor Adobe Campaign?**

Ja, u kunt alleen instellingen voor Adobe Campaign beheren in het Configuratiescherm.

**Kan ik het Configuratiescherm gebruiken?**

Het Configuratiescherm is alleen toegankelijk voor productbeheerders van onze huidige klanten voor wie Adobe Campaign is gehost op AWS. Hybride omgevingen worden nog niet ondersteund.

Als u geen beheerder bent maar wel toegang wilt, vraagt u uw productbeheerder om u toe te voegen als beheerder.

**Hoe open ik het Configuratiescherm?**

Volg de gedetailleerde instructies in de documentatie ‘Configuratiescherm openen’.

**Kost het gebruik van het Configuratiescherm extra?**

Nee, er zijn geen extra kosten als u een huidige Adobe Campaign-klant bent.
