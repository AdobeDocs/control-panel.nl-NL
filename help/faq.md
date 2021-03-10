---
product: campaign
solution: Campaign
title: Veelgestelde vragen over Configuratiescherm
description: Algemene vragen over het Configuratiescherm
feature: 'Configuratiescherm '
role: Architect
level: Intermediair
translation-type: tm+mt
source-git-commit: 4b8020dfd5d1f81a81d0e20025cfabe734744d34
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 99%

---


# Veelgestelde vragen {#faq}

## IMS-organisatie-id {#ims-org-id}

**Wat is een IMS-organisatie-id?**

Dit is een unieke id die aan uw instantie wordt gegeven wanneer u zich voor het eerst aanmeldt bij Adobe Experience Cloud. De notatie moet als volgt zijn: xxx@AdobeOrg.

Raadpleeg de documentatie bij [Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/manage-users-and-products/organizations.html?lang=nl#manage-users-and-products) voor meer informatie.

**Waar kan ik mijn IMS-organisatie-id vinden?**

U kunt onder andere naar [Adobe Experience Cloud Home](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]** gaan. U vindt uw IMS-organisatie-id onderaan de sectie voor het beheer van **[!UICONTROL Quick Access]**. Meer informatie vindt u in de [documentatie van Adobe Experience Cloud](https://marketing.adobe.com/resources/help/en_US/mcloud/organizations.html).

U kunt ook **Admin Console** starten. Uw IMS-organisatie-id wordt weergegeven in uw URL en ziet er ongeveer als volgt uit: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

**Waarom moet ik mijn IMS-organisatie-id weten?**

Om ervoor te zorgen dat u de instellingen voor uw instantie kunt beheren, willen we er zeker van zijn dat u de juiste informatie voor de juiste instantie krijgt als u meerdere instanties voor uw bedrijf gebruikt.

**Wat gebeurt er als ik meerdere IMS-organisatie-id’s heb?**

U kunt meer dan één IMS-organisatie-id hebben als u toegang hebt tot meerdere Adobe-oplossingen. De id die u onder uw Adobe Campaign-instantie ziet, is in dat geval de IMS-organisatie-id die u moet gebruiken.

>[!NOTE]
>
>Het is fantastisch als u dezelfde IMS-organisatie-id hebt voor Adobe Campaign en Adobe Analytics. Dezelfde IMS-organisatie-id voor Analytics en Campaign is een vereiste als u de oplossingen wilt integreren om complexe gebruiksscenario’s te benutten, zoals het achterlaten van winkelwagens (voor AA + AC).
>
>Als u verschillende IMS-organisatie-id’s voor Adobe Campaign en Adobe Analytics hebt, neemt u contact op met de klantenservice om deze op één lijn te brengen.

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
