---
product: campaign
solution: Campaign
title: Verificatierecords voor Google-sites toevoegen voor een subdomein
description: Leer hoe u een Google Site Verification-record toevoegt voor een subdomein voor domeineigendomsverificatie.
feature: Control Panel
role: Architect
level: Experienced
exl-id: 547ca6f2-720f-4d58-b31b-5b2611ba9156
source-git-commit: 355abf48cce3036d1c3e0f6c5fe3ca8fb63cf645
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 73%

---

# Verificatiegegevens voor Google-site toevoegen {#adding-a-google-txt-record}

Om hoge inboxpercentages en lage spampercentages te waarborgen vereisen sommige services zoals Google dat u een TXT-record aan uw domeininstellingen toevoegt om te verifiëren dat u het domein bezit.

Gmail is momenteel een van de populairste aanbieders van e-mailadressen. Met Adobe Campaign kunt u speciale TXT-records voor Google-websiteverificatie toevoegen aan uw subdomeinen om ervoor te zorgen dat deze worden geverifieerd, zodat u verzekerd bent van goede bezorgbaarheid en geslaagde aflevering van e-mails op Gmail-adressen.

Ga als volgt te werk om een Google TXT-record toe te voegen aan uw subdomein dat wordt gebruikt voor het e-mailen naar Gmail-adressen:

1. Klik in de lijst met subdomeinen op de knop met de ovaal naast het gewenste subdomein en selecteer **[!UICONTROL Subdomain details]**.

1. Klik op de knop **[!UICONTROL Add TXT record]** en kies vervolgens **[!UICONTROL Google Site Verification]** van de **[!UICONTROL Record Type]** vervolgkeuzelijst.

1. Voer de waarde in die wordt gegenereerd in G Suite Admin-hulpprogramma&#39;s. Raadpleeg [G Suite-beheerder Help](https://support.google.com/a/answer/183895) voor meer informatie.

   ![](assets/txt_addtxt.png)

1. Klik op de knop **[!UICONTROL Add]** ter bevestiging.

   ![](assets/txt_txtadded.png)

Nadat de TXT-record is toegevoegd, moet u deze door Google laten verifiëren. Hiervoor navigeert u naar de G Suite Admin-tools en start u de verificatiestap (zie [G Suite-beheerder Help](https://support.google.com/a/answer/183895)).

Als u een record wilt verwijderen, selecteert u deze in de lijst met records en klikt u op de knop Verwijderen.

>[!NOTE]
>
>De enige record die u uit de DNS-recordlijst kunt verwijderen, is de record die u eerder hebt toegevoegd (in ons geval de Google-TXT-record).

![](assets/do-not-localize/how-to-video.png) Een video-uitleg van deze functie met [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html#subdomains-and-certificates) of [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/google-txt-record-management.html#subdomains-and-certificates).
