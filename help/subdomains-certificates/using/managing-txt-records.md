---
product: campaign
solution: Campaign
title: TXT-records beheren
description: Leer hoe u TXT-records beheert voor verificatie van domeineigendom.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 547ca6f2-720f-4d58-b31b-5b2611ba9156
source-git-commit: c1c80c03a351613ec0c6870a11ab39a634e8eab7
workflow-type: tm+mt
source-wordcount: '353'
ht-degree: 92%

---

# TXT-records beheren {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="TXT-records beheren"
>abstract="Bij sommige services, zoals Google, moet u een TXT-record aan uw domeininstellingen toevoegen om te verifiëren dat u eigenaar bent van het domein."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/setting-up-new-subdomain.html?lang=nl" text="Een nieuw subdomein instellen"

## Informatie over TXT-records {#about-txt-records}

TXT-records zijn DNS-records die worden gebruikt om tekstgegevens over een domein te verstrekken en die kunnen worden gelezen door externe bronnen.

Om hoge inboxpercentages en lage spampercentages te waarborgen vereisen sommige services zoals Google dat u een TXT-record aan uw domeininstellingen toevoegt om te verifiëren dat u het domein bezit.

Gmail is momenteel een van de populairste aanbieders van e-mailadressen. Met Adobe Campaign kunt u speciale TXT-records voor Google-websiteverificatie toevoegen aan uw subdomeinen om ervoor te zorgen dat deze worden geverifieerd, zodat u verzekerd bent van goede bezorgbaarheid en geslaagde aflevering van e-mails op Gmail-adressen.

![](assets/do-not-localize/how-to-video.png) Deze functie in video detecteren met [Campagne v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html#subdomains-and-certificates) of [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html#subdomains-and-certificates)

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
