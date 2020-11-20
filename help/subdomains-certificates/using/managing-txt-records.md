---
product: campaign
solution: Campaign
title: TXT-records beheren
description: Leer hoe u TXT-records beheert voor verificatie van domeineigendom.
translation-type: tm+mt
source-git-commit: 168ae32d7931497bb37d63f7dd1d14eadbb4b1bf
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 100%

---


# TXT-records beheren {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="TXT-records beheren"
>abstract="Bij sommige services, zoals Google, moet u een TXT-record aan uw domeininstellingen toevoegen om te verifiëren dat u eigenaar bent van het domein."

## Informatie over TXT-records {#about-txt-records}

TXT-records zijn DNS-records die worden gebruikt om tekstgegevens over een domein te verstrekken en die kunnen worden gelezen door externe bronnen.

Om hoge inboxpercentages en lage spampercentages te waarborgen vereisen sommige services zoals Google dat u een TXT-record aan uw domeininstellingen toevoegt om te verifiëren dat u het domein bezit.

Gmail is momenteel een van de populairste aanbieders van e-mailadressen. Met Adobe Campaign kunt u speciale TXT-records voor Google-websiteverificatie toevoegen aan uw subdomeinen om ervoor te zorgen dat deze worden geverifieerd, zodat u verzekerd bent van goede bezorgbaarheid en geslaagde aflevering van e-mails op Gmail-adressen.

Aanvullende bronnen:

* [Campaign Standard-videotutorial](https://docs.adobe.com/content/help/nl-NL/campaign-standard-learn/tutorials/administrating/control-panel/google-txt-record-management.html)
* [Campaign Classic-videotutorial](https://docs.adobe.com/content/help/en/campaign-classic-learn/tutorials/administrating/control-panel-acc/google-txt-record-management.html)

## Een Google TXT-record toevoegen voor een subdomein {#adding-a-google-txt-record}

Ga als volgt te werk om een Google TXT-record toe te voegen aan uw subdomein dat wordt gebruikt voor het e-mailen naar Gmail-adressen:

1. Ga naar de kaart **[!UICONTROL Subdomain and Certificates]**.

1. Selecteer uw instantie en open vervolgens de details van het subdomein waaraan u een DNS-record wilt toevoegen.

   ![](assets/txt_subdomaindetails.png)

1. Klik op de knop **[!UICONTROL Add TXT record]** en voer vervolgens de waarde in die wordt gegenereerd in G Suite Admin-tools. Raadpleeg [G Suite-beheerder Help](https://support.google.com/a/answer/183895) voor meer informatie.

   ![](assets/txt_addtxt.png)

1. Klik op de knop **[!UICONTROL Add]** ter bevestiging.

   ![](assets/txt_txtadded.png)

Nadat de TXT-record is toegevoegd, moet u deze door Google laten verifiëren. Hiervoor navigeert u naar de G Suite Admin-tools en start u de verificatiestap (zie [G Suite-beheerder Help](https://support.google.com/a/answer/183895)).

Als u een record wilt verwijderen, selecteert u deze in de lijst met records en klikt u op de knop Verwijderen.

>[!NOTE]
>
>De enige record die u uit de DNS-recordlijst kunt verwijderen, is de record die u eerder hebt toegevoegd (in ons geval de Google-TXT-record).
