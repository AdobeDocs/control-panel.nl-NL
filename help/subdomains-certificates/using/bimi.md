---
product: campaign
solution: Campaign
title: BIMI-records toevoegen
description: Leer hoe u een BIMI-record voor een subdomein toevoegt.
feature: Control Panel, Subdomains and Certificates
role: Admin
level: Experienced
exl-id: eb7863fb-6e6d-4821-a156-03fee03cdd0e
source-git-commit: e601f74ae9e53d3a008c55e1fd568013ca0196f8
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 86%

---

# BIMI-records toevoegen {#dmarc}

## Over BIMI-records {#about}

Brand Indicators for Message Identification (BIMI) is een industriestandaard waarmee een goedgekeurd logo naast de e-mail van een afzender kan worden weergegeven in het postvak IN van e-mailproviders om de merkherkenning en het vertrouwen te vergroten. Dit helpt e-mailspoofing en phishing te voorkomen door de identiteit van de afzender te verifiëren via DMARC-verificatie, waardoor het voor kwaadwillenden moeilijker wordt om zich in e-mails voor te doen als legitieme merken.

U kunt meerdere logo&#39;s voor een bepaald subdomein hebben. Hiervoor moet u één BIMI-record instellen voor elk logo en een BIMI-kiezer aan elke record toewijzen. [Leer hoe u een BIMI-record toevoegt](#add)

Gedetailleerde informatie over BIMI-implementatie is beschikbaar in [Handleiding voor best practices inzake leverbaarheid van Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html?lang=nl)

![](assets/bimi-example.png){width="70%" align="center"}

## Beperkingen en voorwaarden {#limitations}

* SPF-, DKIM- en DMARC-records zijn vereist voor het maken van een BIMI-record.
* BIMI-records kunnen alleen worden toegevoegd voor subdomeinen die gebruikmaken van Volledige subdomeindelegatie. [Meer informatie over configuratiemethoden voor subdomeinen](subdomains-branding.md#subdomain-delegation-methods)
* Voorwaarden voor DMARC-records:

   * Het recordbeleidstype voor het subdomein moet op Quarantine of Reject worden ingesteld. Het maken van BIMI-records is niet beschikbaar als het DMARC-beleidstype is ingesteld op Geen.
   * Het percentage e-mailberichten waarop het DMARC-beleid wordt toegepast, moet 100% zijn. BIMI ondersteunt geen DMARC-beleid waarbij dit percentage is ingesteld op minder dan 100%.

[Meer informatie over het configureren van DMARC-records](dmarc.md)

## Een BIMI-record toevoegen voor een subdomein {#add}

Voer de volgende stappen uit om een BIMI-record toe te voegen voor een subdomein:

1. Klik in de lijst met subdomeinen op de knop met 3 puntjes naast het gewenste subdomein en selecteer **[!UICONTROL Subdomain details]**.

1. Klik op de knop **[!UICONTROL Add TXT record]** en kies vervolgens **[!UICONTROL BIMI]** in de vervolgkeuzelijst **[!UICONTROL Record type]**.

   ![](assets/bimi-add.png)

1. De **[!UICONTROL Selector]** kunt u een BIMI-kiezer voor de record opgeven. Een BIMI-kiezer is een unieke id die u aan een BIMI-record kunt toewijzen. Hierdoor kunt u meerdere logo&#39;s voor een bepaald subdomein definiëren.

1. In de **[!UICONTROL Company Logo URL]** geeft u de URL op van het SVG-bestand met uw logo.

1. Hoewel **[!UICONTROL Certificate URL]** optioneel is, is het vereist voor sommige e-mailproviders als Gmail en Apple, die 80% van de e-mailmarkt bestrijken. Daarom raden we aan een VMC (Verified Mark Certificate) te verkrijgen om BIMI echt te benutten.

   +++Hoe krijg ik een VMC?

   De belangrijkste stappen om VMC te krijgen zijn als volgt:

   1. Registreer uw merklogo als handelsmerk bij een bureau voor intellectuele eigendom dat is erkend door VMC-uitgevers. Als u een juridisch team hebt, raden we u aan met hen samen te werken om uw logo als handelsmerk te laten vastleggen, of om te controleren of het al als handelsmerk bestaat.

   1. Nadat u hebt gecontroleerd of uw logo al een handelsmerk is, neemt u contact op met de certificeringsinstantie DigiCert of Entrust (CA) om een VMC aan te vragen.

   1. Als uw VMC is goedgekeurd, ontvangt u een PEM-bestand (Privacy Enhanced Mail) met een entiteitscertificaat. Voeg andere tussenliggende certificaten die u van de CA krijgt, toe aan dit PEM-bestand. Upload het PEM-bestand (samen met toegevoegde bestanden) naar uw openbare webserver en noteer de URL van het PEM-bestand. U gebruikt de URL in uw BIMI TXT-record.

   1. Zodra de BIMI-record zichtbaar is op de subdomeindetailpagina voor een bepaald subdomein, kunt u de BIMI Inspector gebruiken die [hier](https://bimigroup.org/bimi-generator/) beschikbaar is om te controleren of de BIMI-record correct functioneert.

   Gedetailleerde informatie over de BIMI-implementatie is beschikbaar in de [BIMI-standaarddocumentatie](https://bimigroup.org/implementation-guide/)
+++

1. Klik op **[!UICONTROL Add]** om het maken van een BIMI-record te bevestigen.

Zodra het maken van de BIMI-record is verwerkt (ongeveer 5 minuten), wordt het weergegeven in het detailscherm van het subdomein. [Meer informatie over het bewaken van TXT-records voor uw subdomeinen](gs-txt-records.md#monitor)
