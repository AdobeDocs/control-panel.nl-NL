---
product: campaign
solution: Campaign
title: Het SSL-certificaat van een subdomein verlengen
description: Leer hoe u de SSL-certificaten van uw subdomeinen kunt verlengen.
feature: Control Panel
role: Architect
level: Experienced
exl-id: e9b7c67d-6afa-44f9-b19d-39c0ec9a7edd
source-git-commit: 963c2af5cdca80ebc2cd79e0708dc4dfe8c6ec1e
workflow-type: ht
source-wordcount: '0'
ht-degree: 100%

---

# Een SSL-certificaat verlengen {#renewing-subdomains-ssl-certificates}

>[!CONTEXTUALHELP]
>id="cp_add_ssl_certificate"
>title="SSL-certificaat verlengen"
>abstract="Als u een SSL-certificaat wilt verlengen, moet u een CSR genereren, het SSL-certificaat voor uw subdomeinen aanschaffen en de certificaatbundel installeren."
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=nl#generating-csr" text="Een Certificate Signing Request (CSR) genereren"
>additional-url="https://experienceleague.adobe.com/docs/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html?lang=nl#installing-ssl-certificate" text="Een SSL-certificaat installeren"

Het proces voor het verlengen van SSL-certificaten bestaat uit drie stappen:

1. **Certificate Signing Request (CSR) genereren**

   Voordat u een certificaat aanschaft, moet een Certificate Signing Request (CSR) worden gegenereerd voor de instantie en subdomeinen die u wilt beveiligen. U moet informatie verstrekken die nodig is om het CSR te genereren (zoals algemene naam, organisatienaam en -adres, enz.). [Meer informatie](generate-csr.md)

1. **Aankoop van het SSL-certificaat**

   Zodra het CSR is gegenereerd, kunt u het gebruiken om het SSL-certificaat aan te schaffen bij de certificeringsautoriteit die door uw bedrijf is goedgekeurd.

1. **Installatie van het SSL-certificaat**

   Installeer het aangeschafte SSL-certificaat op het gewenste subdomein om dit te beveiligen. [Meer informatie](install-ssl-certificate.md)

![](assets/do-not-localize/how-to-video.png) Een video-uitleg van deze functie met [Campaign v7/v8](https://experienceleague.adobe.com/docs/campaign-classic-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=nl#subdomains-and-certificates) of [Campaign Standard](https://experienceleague.adobe.com/docs/campaign-standard-learn/control-panel/subdomains-and-certificates/adding-ssl-certificates.html?lang=nl#adding-ssl-certificates).

**Verwante onderwerpen:**

* [Best Practice-gids voor levering - aanvraagproces voor een SSL-certificaat voor Adobe Campaign](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/campaign/ac-ssl-certificate-request.html?lang=nl)
* [Branding van subdomeinen](../../subdomains-certificates/using/subdomains-branding.md)
* [Uw subdomeinen bewaken](../../subdomains-certificates/using/monitoring-subdomains.md)
