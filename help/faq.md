---
title: Veelgestelde vragen over regelpaneel
description: Algemene vragen met betrekking tot het Configuratiescherm
translation-type: tm+mt
source-git-commit: 35723590195ef54df42d1d1df5b37490787f8836
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Veelgestelde vragen {#faq}

## IMS Organisatie-id {#ims-org-id}

**Wat is een IMS-organisatie-id?**

Dit is een unieke id die aan uw exemplaar wordt gegeven wanneer u zich voor het eerst aanmeldt bij Adobe Experience Cloud. De notatie moet als volgt zijn: xxx@AdobeOrg.

Raadpleeg de documentatie bij [Adobe Experience Cloud voor meer informatie](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html).

**Waar kan ik mijn IMS Organisatie ID vinden?**

U kunt onder andere naar [Adobe Experience Cloud Home](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]** gaan. You will find your IMS Organization ID at the bottom of Administration **[!UICONTROL Quick Access]** section. Meer informatie vindt u in de [documentatie van Adobe Experience Cloud](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html).

De andere manier is om **Admin Console** te lanceren. De IMS-organisatie-id is zichtbaar in uw URL en ziet er ongeveer als volgt uit: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**Waarom moet ik mijn IMS Organisatie-id kennen?**

Opdat u montages voor uw instantie beheert, willen wij ervoor zorgen dat u de juiste informatie voor de juiste instantie krijgt voor het geval u veelvoudige instanties voor uw bedrijf gebruikt.

**Wat gebeurt er als ik meerdere IMS Organisatie-id&#39;s heb?**

U hebt mogelijk meer dan één IMS-organisatie-id als u toegang hebt tot meerdere Adobe-oplossingen. In dit geval is de juiste IMS Organisatie-id die u moet gebruiken, die welke u onder uw Adobe Campaign-instantie ziet.

>[!NOTE]
>
>Als u dezelfde IMS Organisatie-id hebt voor Adobe Campaign en Adobe Analytics, is dit geweldig. Een IMS-organisatie-id tussen Analytics en Campagne is een vereiste als u de oplossingen wilt integreren om te profiteren van complexe gebruikssituaties, zoals het achterlaten van winkelwagentjes (voor AA + AC).
>
>Als u verschillende IMS-organisatie-id&#39;s voor Adobe Campaign en Adobe Analytics hebt, neemt u contact op met de klantenservice om deze op één lijn te brengen.

**Hoe kan ik weten dat mijn Adobe Campaign-exemplaar al dan niet wordt gehost op AWS?**

Ga als volgt te werk om te controleren of uw instantie wordt gehost op AWS:

1. Win uw login URL terug. Het is de URL die u gebruikt om u aan te melden bij uw Campagne-instantie. Deze eindigt meestal met &quot;.campagne.adobe.com&quot; of&quot;.neolane.net&quot;.
1. Open de terminal en voer vervolgens een **[!DNL nslookup]** bewerking uit op de aanmeldings-URL.

   `doe-macOS% nslookup myinstance.campaign.adobe.com`

1. De reactie retourneert informatie over uw instantie.

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

1. Voer een **nslookup** verrichting op het teruggekeerde IP adres uit.

   `doe-macOS% nslookup 12.34.567.89`

1. Controleer de waarde &quot;name&quot; in het geretourneerde resultaat. Als het bestand &quot;amazonaws.com&quot; bevat, betekent dit dat uw instantie wordt gehost op AWS.

   ```
   doe-macOS% nslookup 12.34.567.89
   Server:     12.34.5.678
   Address:    12.34.5.678#99
   
   Non-authoritative answer:
   89.567.34.12.in-addr.arpa   name = ec2-12-34-567-89.address.amazonaws.com.
   ```

>[!NOTE]
>
>Als u naar AWS wilt worden gemigreerd, start u het proces door contact op te nemen met de succesmanager van de klant.

## Deelvenster Beheer {#control-panel}

**Wat is het Configuratiescherm?**

Met het Configuratiescherm kunnen productbeheerders verschillende instellingen rechtstreeks beheren en de capaciteit controleren van SFTP-servers die op Adobe Campaign zijn aangesloten.

**Wat zijn sommige huidige mogelijkheden van het Controlebord?**

Met het Configuratiescherm kunt u opslag bijhouden, IP&#39;s toevoegen aan de lijst van gewenste personen en SSH-sleutels voor uw SFTP-servers beheren op basis van uw behoeften en andere acties.

Raadpleeg de documentatie over door het Configuratiescherm ondersteunde acties voor meer informatie.

**Is het Controlebord slechts voor Adobe Campaign?**

Ja, u kunt de instellingen voor Adobe Campaign alleen beheren in het Configuratiescherm.

**Kan ik het Configuratiescherm gebruiken?**

Het Configuratiescherm is alleen toegankelijk voor productbeheerders van onze huidige klanten die Adobe Campaign hebben gehost op AWS. Hybride omgevingen worden nog niet ondersteund.

Als u geen beheerder bent maar wel toegang wilt, neemt u contact op met uw productbeheerder om u toe te voegen als beheerder.

**Hoe kan ik tot het Controlebord toegang hebben?**

Volg de gedetailleerde instructies in de documentatie van het Configuratiescherm.

**Is er een extra vergoeding voor het gebruik van het Configuratiescherm?**

Nee, er zijn geen extra kosten als u een huidige klant van Adobe Campaign bent.
