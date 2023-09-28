---
product: campaign
solution: Campaign
title: TXT-records beheren
description: Leer hoe u TXT-records beheert voor verificatie van domeineigendom.
feature: Control Panel
role: Architect
level: Experienced
source-git-commit: 118fa4d722980e507d15647453e96a8b6189f837
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 25%

---


# Aan de slag met TXT-records {#managing-txt-records}

>[!CONTEXTUALHELP]
>id="cp_siteverification_add"
>title="TXT-records beheren"
>abstract="TXT-records zijn DNS-records die worden gebruikt om tekstgegevens over een domein te verstrekken en die kunnen worden gelezen door externe bronnen. Met het Configuratiescherm kunt u drie typen records toevoegen aan uw subdomeinen: Google Site Verification, DMARC en BIMI-records."

## Informatie over TXT-records {#about}

TXT-records zijn DNS-records die worden gebruikt om tekstgegevens over een domein te verstrekken en die kunnen worden gelezen door externe bronnen. Met het Configuratiescherm kunt u drie typen records toevoegen aan uw subdomeinen:

* **Google TXT-records** staat u toe om te verklaren dat u uw domein bezitten, die hoge inbox tarieven en lage spamtarieven voor uw e-mails verzekert. [Meer informatie over het toevoegen van Google TXT-records](managing-txt-records.md)
* **DMARC-records** verstrek een manier om het domein van de afzender voor authentiek te verklaren en onbevoegd gebruik van het domein voor kwaadwillige doeleinden te verhinderen. [Leer hoe u DMARC-records toevoegt](dmarc.md)
* **BIMI-records** staat u toe om een goedgekeurd logo naast uw e-mails in postvakjes van brievenbusleveranciers te tonen om merkherkenning en vertrouwen te verbeteren. [Meer informatie over het toevoegen van BIMI-records](bimi.md)

## De records van uw subdomeinen controleren {#monitor}

U kunt alle verslagen controleren TXT die voor elk subdomein zijn toegevoegd door tot de details van subdomeinen toegang te hebben.

In dit scherm, alle TXT-type verslagen voor de geselecteerde subdomeinvertoning, met informatie in de kolom &quot;Waarde&quot;op hun configuratie. Als u een Google TXT-, DMARC- of BIMI-record wilt verwijderen, klikt u op de knop voor weglatingen en selecteert u Verwijderen. Indien nodig kunt u ook DMARC- en BIMI-records bewerken.

![](assets/txt-records.png)
