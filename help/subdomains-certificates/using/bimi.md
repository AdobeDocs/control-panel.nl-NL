---
product: campaign
solution: Campaign
title: BIMI-records toevoegen
description: Leer hoe u een BIMI-record voor een subdomein toevoegt.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 0ad4c1f12eb035c8d543777be2a8806d507be5be
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# BIMI-records toevoegen {#dmarc}

## BIMI-records {#about}

Merk Indicators for Message Identification (BIMI) is een industrienorm die het mogelijk maakt een goedgekeurd logo te gebruiken naast de e-mail van een afzender in de postvakjes van postbusaanbieders om de merkherkenning en het vertrouwen te vergroten. Het helpt e-mailspoofing en phishing te verhinderen door de identiteit van de afzender door authentificatie te verifiëren DMARC, die het voor kwaadwillige acteurs moeilijker maakt om zich van wettige merken in e-mails te doen gevoelen. Gedetailleerde informatie over de BIMI-implementatie is beschikbaar op [Handleiding voor beste praktijken bij de levering van Adobe](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/technotes/implement-bimi.html)

![](assets/bimi-example.png){width="70%" align="center"}

## Beperkingen en voorwaarden {#limitations}

* SPF-, DKIM- en DMARC-records zijn voorwaarden voor het maken van een BIMI-record.
* BIMI-records kunnen alleen worden toegevoegd voor subdomeinen die gebruikmaken van Volledige subdomeindelegatie. [Meer informatie over configuratiemethoden voor subdomeinen](subdomains-branding.md#subdomain-delegation-methods)
* Voorwaarden voor DMARC-records:

   * Het beleidstype van het verslag voor subdomain moet aan &quot;Quarantine&quot;of &quot;Weigeren&quot;worden geplaatst. BIMI-bestanden worden niet gemaakt als het DMARC-beleidstype is ingesteld op Geen.
   * Het percentage e-mailberichten waarop het DMARC-beleid wordt toegepast, moet 100% zijn. BIMI ondersteunt geen DMARC-beleid met dit percentage ingesteld op minder dan 100%.

[Leer hoe te om DMARC verslagen te vormen](dmarc.md)

## Een BIMI-record toevoegen voor een subdomein {#add}

Voer de volgende stappen uit om een BIMI-record toe te voegen voor een subdomein:

1. Klik in de lijst met subdomeinen op de knop met de ovaal naast het gewenste subdomein en selecteer **[!UICONTROL Subdomain details]**.

1. Klik op de knop **[!UICONTROL Add TXT record]** en kies vervolgens **[!UICONTROL BIMI]** van de **[!UICONTROL Record type]** vervolgkeuzelijst.

   ![](assets/bimi-add.png)

1. In de **[!UICONTROL Company Logo URL]**, geeft u de URL op van het SVG-bestand dat uw logo bevat.

1. De **[!UICONTROL Certificate URL]** veld is optioneel. Hiermee kunt u een URL (Verified Mark Certificate of VMC) toevoegen om te bevestigen dat uw organisatie de wettelijke eigenaar van het logo is, zodat spammers en andere kwaadwillige gebruikers geen merklogo&#39;s kunnen gebruiken die zij niet hebben.

   +++Hoe krijg ik een VMC?

   De belangrijkste stappen om VMC te krijgen zijn als volgt:

   1. Registreer uw merklogo als een handelsmerk bij een bureau voor intellectuele eigendom dat door VMC-emittenten wordt erkend. Als u een legaal team hebt, raden we u aan met hen samen te werken om uw logo te laten markeren of om te controleren of het al gedeponeerd is.

   1. Nadat u hebt gecontroleerd of uw logo een handelsmerk heeft, neemt u contact op met de certificeringsinstantie DigiCert of Entrust (CA) om een VMC aan te vragen.

   1. Als uw VMC is goedgekeurd, ontvangt u een PEM-bestand (Privacy Enhanced Mail) van een entiteitscertificaat. Voeg andere tussenliggende certificaten die u van de CA krijgt, toe aan dit PEM-bestand. Upload het PEM-bestand (samen met toegevoegde bestanden) naar uw openbare webserver en noteer de URL van het PEM-bestand. U gebruikt de URL in uw BIMI TXT-record.

   Gedetailleerde informatie over de BIMI-implementatie is beschikbaar in de [BIMI-standaarddocumentatie](https://bimigroup.org/implementation-guide/)
+++

1. Klikken **[!UICONTROL Add]** ter bevestiging van de aanmaak van BIMI-bestanden.

Nadat de BIMI-record is gemaakt (ongeveer 5 minuten), wordt deze weergegeven in het detailscherm van de subdomeinen. [Leer hoe u TXT-records voor uw subdomeinen kunt controleren](gs-txt-records.md#monitor)
