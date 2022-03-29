---
product: campaign
solution: Campaign
title: Veelgestelde vragen over Configuratiescherm
description: Algemene vragen over het Configuratiescherm
feature: Control Panel
role: Architect
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
source-git-commit: c1c80c03a351613ec0c6870a11ab39a634e8eab7
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Veelgestelde vragen {#faq}

## Configuratiescherm  {#control-panel}

### Wat is het configuratiescherm?

Met het configuratiescherm kunnen productbeheerders verschillende instellingen rechtstreeks beheren en de capaciteit bewaken van SFTP-servers die met Adobe Campaign zijn verbonden.

### Wat zijn de huidige mogelijkheden van het configuratiescherm?

Met het Configuratiescherm kunt u de opslag bijhouden, IP-adressen toevoegen aan de lijst van gewenste IP-adressen, SSH-sleutels voor uw SFTP-servers beheren op basis van uw behoeften, enzovoort.

Raadpleeg voor meer informatie de documentatie over acties die door het Configuratiescherm worden ondersteund.

### Zijn sommige mogelijkheden nog niet ondersteund in Campaign v8, maar wel beschikbaar in Campaign Classic v7?{#v8-restrictions}

Nee. Alle mogelijkheden die beschikbaar zijn in Campaign v7, worden nu ook ondersteund via het configuratiescherm in Campaign v8, inclusief functies voor subdomein en certificaatbeheer.

### Is het configuratiescherm alleen voor Adobe Campaign?

Ja, u kunt in het configuratiescherm alleen instellingen voor Adobe Campaign beheren.

### Kan ik het configuratiescherm gebruiken?

Het Configuratiescherm is alleen toegankelijk voor productbeheerders van onze huidige klanten voor wie Adobe Campaign is gehost op AWS. Hybride omgevingen worden nog niet ondersteund.

Als u geen beheerder bent maar wel toegang wilt, vraagt u uw productbeheerder om u toe te voegen als beheerder.

### Wat zijn de toegangsvoorwaarden tot het configuratiescherm voor een gebruiker van Campaign Classic v7? {#v7-restrictions}

Het configuratiescherm is toegankelijk voor alle beheerders. [Meer info](discover/using/managing-permissions.md).

Houd er voor Campaign v7 rekening mee dat uw instantie moet worden gehost op Amazon Web Services (AWS) en moet worden geüpgraded naar de nieuwste [stabiele Campaign-build](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=nl#rn-statuses) of 9032 of hoger. Leer hoe u uw Campaign Classic v7-versie kunt controleren in [deze sectie](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=nl#getting-your-campaign-version). Volg de stappen in [deze sectie](#hosted-aws) om te controleren of uw Campaign Classic-versie wordt gehost op AWS.

### Hoe open ik het configuratiescherm?

Volg de gedetailleerde instructies in de documentatie ‘Configuratiescherm openen’.

### Kost het gebruik van het configuratiescherm extra?

Nee, er zijn geen extra kosten als u een huidige Adobe Campaign-klant bent.

## IMS-organisatie-ID {#ims-org-id}

### Wat is een IMS-organisatie-ID?

Dit is een unieke id die aan uw instantie wordt gegeven wanneer u zich voor het eerst aanmeldt bij Adobe Experience Cloud. De notatie moet als volgt zijn: xxx@AdobeOrg.

Raadpleeg de documentatie bij [Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=nl) voor meer informatie.

### Waar kan ik mijn IMS-organisatie-ID vinden?

U kunt onder andere naar [Adobe Experience Cloud Home](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]** gaan. U vindt uw IMS-organisatie-id onderaan de sectie voor het beheer van **[!UICONTROL Quick Access]**. Meer informatie vindt u in de [documentatie van Adobe Experience Cloud](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html).

U kunt ook **Admin Console** starten. Uw IMS-organisatie-id wordt weergegeven in uw URL en ziet er ongeveer als volgt uit: https://adminconsole.adobe.com/xxx@AdobeOrg/overview.

### Waarom moet ik mijn IMS-organisatie-ID weten?

We willen ervoor zorgen dat u de juiste versie krijgt als u meerdere versies voor uw bedrijf gebruikt, zodat u de instellingen voor uw versies kunt beheren.

### Wat gebeurt er als ik meerdere IMS-organisatie-ID’s heb?

U kunt meer dan één IMS-organisatie-id hebben als u toegang hebt tot meerdere Adobe-oplossingen. De id die u onder uw Adobe Campaign-instantie ziet, is in dat geval de IMS-organisatie-id die u moet gebruiken.

>[!NOTE]
>
>Het is fantastisch als u dezelfde IMS-organisatie-id hebt voor Adobe Campaign en Adobe Analytics. Dezelfde IMS-organisatie-id voor Analytics en Campaign is een vereiste als u de oplossingen wilt integreren om complexe gebruiksscenario’s te benutten, zoals het achterlaten van winkelwagens (voor AA + AC).
>
>Als u verschillende IMS-organisatie-id’s voor Adobe Campaign en Adobe Analytics hebt, neemt u contact op met de klantenservice om deze op één lijn te brengen.

### Hoe weet ik of mijn Adobe Campaign-versie wordt gehost op AWS?{#hosted-aws}

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
