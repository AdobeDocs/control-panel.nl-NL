---
product: campaign
solution: Campaign
title: Veelgestelde vragen over Configuratiescherm
description: Algemene vragen over het Configuratiescherm
feature: Control Panel
role: Architect
level: Intermediate
exl-id: 4f329764-ed8b-4939-affc-ed994fd6101d
source-git-commit: 330733c5a025ed8f26120a38f40743bfb5023fd4
workflow-type: tm+mt
source-wordcount: '753'
ht-degree: 75%

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

Houd er voor Campaign v7 rekening mee dat uw instantie moet worden gehost op Amazon Web Services (AWS) en moet worden geüpgraded naar de nieuwste [stabiele Campaign-build](https://experienceleague.adobe.com/docs/campaign-classic/using/release-notes/rn-overview.html?lang=nl#rn-statuses) of 9032 of hoger. Lees [in dit gedeelte](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/starting-with-adobe-campaign/launching-adobe-campaign.html?lang=nl#getting-your-campaign-version) hoe u controleert welke Campaign Classic v7-versie u hebt. Volg de stappen in [deze sectie](#hosted-aws) om te controleren of uw Campaign Classic-versie wordt gehost op AWS.

### Hoe open ik het configuratiescherm?

Volg de gedetailleerde instructies in de documentatie ‘Configuratiescherm openen’.

### Kost het gebruik van het configuratiescherm extra?

Nee, er zijn geen extra kosten als u een huidige Adobe Campaign-klant bent.

## Organisatie-id {#ims-org-id}

### Wat is een organisatie-id?

Dit is een unieke id die aan uw instantie wordt gegeven wanneer u zich voor het eerst aanmeldt bij Adobe Experience Cloud. De notatie moet als volgt zijn: xxx@AdobeOrg.

Raadpleeg voor meer informatie [Adobe Experience Cloud-documentatie](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html?lang=nl){_blank}.

### Waar kan ik mijn organisatie-id vinden?

U kunt onder andere naar [Adobe Experience Cloud Home](https://experiencecloud.adobe.com/) > **[!UICONTROL Administration]** gaan. U vindt uw organisatie-id onder aan Beheer **[!UICONTROL Quick Access]** sectie. U vindt meer gedetailleerde informatie in het gedeelte [Adobe Experience Cloud-documentatie](https://experienceleague.adobe.com/docs/core-services/interface/administration/organizations.html){_blank}.

U kunt ook **Admin Console** starten. Uw organisatie-id wordt weergegeven in uw URL en ziet er ongeveer als volgt uit: `https://adminconsole.adobe.com/xxx@AdobeOrg/overview`.

### Waarom moet ik mijn organisatie-id kennen?

We willen ervoor zorgen dat u de juiste versie krijgt als u meerdere versies voor uw bedrijf gebruikt, zodat u de instellingen voor uw versies kunt beheren.

### Wat gebeurt er als ik meerdere organisatie-id&#39;s heb?

U kunt meer dan één identiteitskaart van de Organisatie hebben als u toegang tot veelvoudige oplossingen van Adobe hebt. In dit geval is de juiste organisatie-id die u moet gebruiken, die welke u onder uw Adobe Campaign-exemplaar ziet.

>[!NOTE]
>
>Als je dezelfde organisatie-id hebt voor Adobe Campaign en Adobe Analytics, is dit geweldig. U hebt één organisatie-id tussen Analytics en Campagne nodig als u de oplossingen wilt integreren om te profiteren van complexe gebruikscituaties, zoals het achterlaten van winkelwagentjes (voor AA + AC).
>
>Als u verschillende organisatie-id&#39;s voor Adobe Campaign en Adobe Analytics hebt, neemt u contact op met de klantenservice om deze op één lijn te brengen.

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
